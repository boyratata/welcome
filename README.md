
#!/bin/bash

echo "<html>"
echo "<head>"
echo "<title>Welcome Page</title>"
echo "</head>"
echo "<body>"

welcome_message="Welcome to my GitHub page!"

IFS=' ' read -ra words <<< "$welcome_message"

colors=("red" "green" "blue" "yellow" "orange" "purple" "pink")

for ((i=0; i<${#words[@]}; i++)); do
    color_index=$((i % ${#colors[@]}))
    echo "<span style='background-color:${colors[$color_index]}'>${words[$i]}</span> "
done

echo "</body>"
echo "</html>"
