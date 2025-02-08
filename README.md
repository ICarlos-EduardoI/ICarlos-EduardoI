import datetime

def generate_readme():
    username = "Carlos"
    bio = "Estudante de Ciência da Computação e entusiasta em tecnologia. Apaixonado por desenvolvimento, segurança e investimentos. 🚀"
    skills = ["Python", "C", "JavaScript", "HTML & CSS", "LabVIEW", "Git", "Linux"]
    projects = [
        {"name": "Projeto de Automação", "repo": "https://github.com/ICarlos-EduardoI/automacao"},
        {"name": "Portfolio Web", "repo": "https://github.com/ICarlos-EduardoI/portfolio"},
    ]
    social_links = {
        "LinkedIn": "https://www.linkedin.com/in/seuusuario/",
        "GitHub": "https://github.com/seuusuario",
    }
    
    # Criando o conteúdo do README
    readme_content = f"""
# Olá, eu sou {username}! 👋

{bio}

## 🚀 Habilidades
"""
    for skill in skills:
        readme_content += f"- {skill}\n"
    
    readme_content += "\n## 📂 Projetos\n"
    for project in projects:
        readme_content += f"- [{project['name']}]({project['repo']})\n"
    
    readme_content += "\n## 🌍 Conecte-se comigo\n"
    for platform, link in social_links.items():
        readme_content += f"- [{platform}]({link})\n"
    
    readme_content += f"\n_Última atualização: {datetime.date.today()}_\n"
    
    # Escrevendo o arquivo README.md
    with open("README.md", "w", encoding="utf-8") as file:
        file.write(readme_content)
    
    print("README.md gerado com sucesso!")

if __name__ == "__main__":
    generate_readme()
 



