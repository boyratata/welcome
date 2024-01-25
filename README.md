
#!/bin/bash

echo "<html>"
echo "<head>"
echo "<title>Welcome Page</title>"
echo "</head>"
echo "<body>"

welcome_message="Welcome to my GitHub page!"

# Split the welcome message into words
IFS=' ' read -ra words <<< "$welcome_message"

# Define an array of colors
colors=("red" "green" "blue" "yellow" "orange" "purple" "pink")

# Loop through each word and apply a different color
for ((i=0; i<${#words[@]}; i++)); do
    color_index=$((i % ${#colors[@]}))
    echo "<span style='background-color:${colors[$color_index]}'>${words[$i]}</span> "
done

echo "</body>"
echo "</html>"
