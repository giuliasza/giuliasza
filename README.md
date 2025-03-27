
# 👋 HELLO WORLD!

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Roboto&size=25&duration=4000&color=333&center=true&vCenter=true&lines=Eu+sou+M.Giulia!;Bem-vindo+ao+meu+perfil!">
</p>

<p align="center">
  <img src="link_para_sua_imagem.gif" alt="Animação ou Foto" width="400px">
</p>

## 🛠️ Sobre mim
- 🌱 Estou aprendendo: **[Tecnologias/Áreas]**
- 🎯 Objetivo atual: **[Seu objetivo atual]**
- 💬 Pergunte-me sobre: **[Tópicos com que você pode ajudar]**

## 🚀 Minhas Tecnologias
![Linguagem1](https://img.shields.io/badge/-Linguagem1-333?style=for-the-badge&logo=LogoLinguagem)
![Linguagem2](https://img.shields.io/badge/-Linguagem2-333?style=for-the-badge&logo=LogoLinguagem)

![Estatísticas do GitHub](https://github-readme-stats.vercel.app/api?username=giuliasza&show_icons=true&theme=radical)

## 📊 Minhas Contribuições
![Estatísticas do GitHub](https://github-readme-stats.vercel.app/api?username=SeuUsuario&show_icons=true&theme=radical)

## 📫 Contato
[![LinkedIn](https://img.shields.io/badge/-LinkedIn-333?style=for-the-badge&logo=linkedin)](https://linkedin.com/in/SeuPerfil)
[![E-mail](https://img.shields.io/badge/-Email-333?style=for-the-badge&logo=gmail)](mailto:seuemail@example.com)

name: Generate Snake Animation

on:
  schedule: # Executa diariamente
    - cron: "0 0 * * *"
  workflow_dispatch: # Permite rodar manualmente

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v3
      - uses: Platane/snk@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-snake.svg
            dist/github-snake-dark.svg?palette=github-dark
            dist/ocean.gif?color_snake=orange&color_dots=#bfd6f6,#8dbdff,#64a1f4,#4b91f1,#3c7dd9
      - name: Commit e enviar a animação
        uses: crazy-max/ghaction-github-pages@v3
        with:
          target_branch: output
          build_dir: dist

          ![Snake animation](https://github.com/<giuliasza>/<giuliasza>/blob/output/dist/github-snake.svg)