from GitHub import ReadMe

class BoyRatata(ReadMe):
    README_PATH = "/ayyournotreal/ayyournotreal/README.md"

    def __init__(self):
        self.username = "Boyratata"
        self.contacts = {
            "Discord": "clownmeme",
            "Youtube": "@animeboy"
        }
        self.aliases = [
            "ayyournotreal"
        ]
        self.location = "Los Angeles, California"
        self.hobbies = "everything"

    def generate_readme_content(self):
        readme_content = f"# {self.username}'s README\n\n"
        readme_content += "## Contacts\n"
        
        for platform, handle in self.contacts.items():
            readme_content += f"- {platform}: {handle}\n"

        readme_content += "\n## Aliases\n"
        for alias in self.aliases:
            readme_content += f"- {alias}\n"

        readme_content += f"\n## Location\n{self.location}\n"
        readme_content += f"\n## Hobbies\n{self.hobbies}\n"

        return readme_content

if __name__ == "__main__":
    boy_ratata_instance = BoyRatata()
    readme_content = boy_ratata_instance.generate_readme_content()

    with open(BoyRatata.README_PATH, "w") as readme_file:
        readme_file.write(readme_content)
