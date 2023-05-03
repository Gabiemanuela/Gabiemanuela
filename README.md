### Olá! Eu sou a Gabriela Emanuela 

- ⚡Técnica em Mecatrônica
- ⚡Engenheira Elétrica 
- 🌱 Estudante de Análise e Desenvolvimento de Sistemas

<div>
  <a href="https://github.com/Gabiemanuela">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=gabiemanuela&show_icons=true&theme=dracula&include_all_commits=true&count_private=true"/>
</div>
<div style="display: inline_block"><br>
  <img align="center" alt="Gabi-Jv" height="30" width="40" src="https://user-images.githubusercontent.com/25181517/121405384-444d7300-c95d-11eb-959f-913020d3bf90.png">
  <img align="center" alt="Gabi-C#" height="30" width="40" src="https://user-images.githubusercontent.com/25181517/117201156-9a724800-adec-11eb-9a9d-3cd0f67da4bc.png">
  </div>
  
  ![Snake animation](https://github.com/rafaballerine/blob/output/github-contribution-grid-snake.svg)

  name: Generate Datas
on:
schedule: # execute every 12 hours
- cron: "* */12 * * *"
workflow_dispatch:
jobs:
build:
name: Jobs to update datas
runs-on: ubuntu-latest
steps:
# Summary Cards
- uses: actions/checkout@v2
- uses: vn7n24fzkq/github-profile-summary-cards@release
env:
GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
with:
USERNAME: ${{ github.repository_owner }}

  # Snake Animation
  - uses: Platane/snk@master
    id: snake-gif
    with:
      github_user_name: camilamaraschin
      svg_out_path: dist/github-contribution-grid-snake.svg
  - uses: crazy-max/ghaction-github-pages@v2.1.3
    with:
      target_branch: output
      build_dir: dist
    env:
      GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
