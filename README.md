Olá, eu sou Cainã Reis! 👋

<p align="center">
<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&duration=4000&pause=500&color=1EB980&center=true&vCenter=true&width=600&lines=Desenvolvedor+em+formação.;DevOps+%7C+Automação+%7C+Python;Apaixonado+por+tecnologia+e+games.;Bem-vindo+ao+meu+GitHub+%F0%9F%91%BE" alt="Typing SVG" />
</p> <p align="center">
  <img src="https://komarev.com/ghpvc/?username=Cainareiss&label=Visualizações+do+perfil&color=1EB980&style=flat" alt="Visualizações do perfil"/>
</p>




👨‍💻 Sobre mim

🎮 Apaixonado por tecnologia, videogames e programação.
📚 Estudante de Análise e Desenvolvimento de Sistemas.
🚀 Estagiário em DevOps / Automação.
🛠️ Desenvolvimento de soluções em Python, scripts e projetos pessoais.
🎯 Focado em automação, infraestrutura e software.




🧰 Tecnologias Principais

<p align="center">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width="55" title="Python" alt="Python"/>&nbsp;
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" width="55" title="GitHub" alt="GitHub"/>&nbsp;
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg" width="55" title="Linux" alt="Linux"/>&nbsp;
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" width="55" title="Docker" alt="Docker"/>
</p>




📚 Em aprendizado contínuo

<p align="center">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-plain.svg" width="50" title="PHP" alt="PHP"/>&nbsp;
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" width="50" title="Java" alt="Java"/>&nbsp;
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" width="50" title="MySQL" alt="MySQL"/>&nbsp;
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/android/android-plain-wordmark.svg" width="50" title="Android" alt="Android"/>&nbsp;
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg" width="50" title="C" alt="C"/>
</p>




📬 Onde me encontrar

<p align="center">
<a href="https://instagram.com/caina.darc" target="_blank">
    <img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white" alt="Instagram"/>
  </a>
  <a href="https://www.linkedin.com/in/cain%C3%A3-reis-9b1622152" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
  <a href="mailto:darkreis2@gmail.com">
    <img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail"/>
  </a>
  <a href="https://api.whatsapp.com/send?phone=5585988768488" target="_blank">
    <img src="https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp"/>
  </a>
</p>




🚀 Projetos em Destaque

<p align="center">
<a href="https://github.com/Cainareiss/Gerador_projetos_CFTV">
    <img src="https://github-readme-stats.vercel.app/api/pin?username=Cainareiss&repo=Gerador_projetos_CFTV&theme=dracula" alt="Repo CFTV"/>
  </a>
  <a href="https://github.com/Cainareiss/Zeo-store-s">
    <img src="https://github-readme-stats.vercel.app/api/pin?username=Cainareiss&repo=Zeo-store-s&theme=dracula" alt="Repo Zeo Store"/>
  </a>
</p>




📊 Estatísticas GitHub (Geradas via GitHub Actions )

Para garantir a estabilidade e evitar dependências de serviços externos como o Vercel, as estatísticas abaixo podem ser geradas e atualizadas automaticamente usando GitHub Actions. Isso garante que seu perfil sempre exiba os dados mais recentes sem interrupções.

Configuração para github-readme-stats e github-readme-streak-stats via GitHub Actions:

1.
Crie um repositório com seu nome de usuário: Se ainda não tiver, crie um repositório público com o mesmo nome de seu usuário GitHub (ex: Cainareiss/Cainareiss). Este será seu repositório de perfil.

2.
Crie um Personal Access Token (PAT): Vá em Settings > Developer settings > Personal access tokens > Tokens (classic) e gere um novo token. Não são necessárias permissões especiais (scopes) para as estatísticas públicas. Copie o token.

3.
Adicione o PAT como um Secret no seu repositório de perfil: No seu repositório de perfil, vá em Settings > Secrets and variables > Actions > New repository secret. Crie um secret com um nome como GH_TOKEN e cole o PAT que você gerou.

4.
Crie um workflow de GitHub Actions: No seu repositório de perfil, crie o arquivo .github/workflows/metrics.yml (ou outro nome de sua preferência) com o seguinte conteúdo:

YAML


name: GitHub Metrics





on:
schedule:
- cron: "0 0 * * *" # Executa todos os dias à meia-noite UTC
workflow_dispatch:

jobs:
build:
runs-on: ubuntu-latest
permissions:
contents: write

Plain Text


steps:
  - uses: actions/checkout@v4

  - name: Generate GitHub Stats
    uses: anuraghazra/github-readme-stats@master
    with:
      username: ${{ github.repository_owner }}
      token: ${{ secrets.GH_TOKEN }}
      output: "./profile-images/github-stats.svg"
      theme: dracula
      hide_border: true
      include_all_commits: true
      count_private: true

  - name: Generate GitHub Streak Stats
    uses: DenverCoder1/github-readme-streak-stats@main
    with:
      user: ${{ github.repository_owner }}
      token: ${{ secrets.GH_TOKEN }}
      output: "./profile-images/github-streak-stats.svg"
      theme: dracula
      hide_border: true

  - name: Commit and Push
    run: |
      git config user.name "github-actions[bot]"
      git config user.email "41898282+github-actions[bot]@users.noreply.github.com"
      git add ./profile-images/*.svg
      git commit -m "Update GitHub Stats and Streak Stats" || exit 0
      git push
```



5. Atualize seu README.md: Substitua as imagens antigas pelas novas referências aos arquivos gerados:

Plain Text


```markdown
<p align="center">
  <img height="170" src="./profile-images/github-stats.svg" alt="Estatísticas Gerais"/>
  <img height="170" src="./profile-images/github-streak-stats.svg" alt="Streak Stats"/>
</p>
```






🐍 Contribuições (Animação da Cobrinha)

A animação da cobrinha (Platane/snk) é gerada a partir do seu gráfico de contribuições do GitHub. Para garantir que ela sempre reflita suas atividades mais recentes, é crucial que o workflow de GitHub Actions que a gera esteja configurado para rodar regularmente.

Observação sobre commits recentes: A ferramenta Platane/snk gera a animação com base no histórico completo de contribuições. Se a cobrinha não está "comendo" commits recentes, verifique se o workflow está sendo executado com a frequência desejada (geralmente diária) e se não há problemas de cache no GitHub. A ferramenta não possui uma opção nativa para limitar a animação a um período específico (ex: últimos 30 dias).

Configuração para Platane/snk via GitHub Actions:

1.
Crie ou edite o workflow: No seu repositório de perfil, crie ou edite o arquivo .github/workflows/snake.yml (ou outro nome) com o seguinte conteúdo:

YAML


name: Generate Snake





on:
schedule:
- cron: "0 0 * * *" # Executa todos os dias à meia-noite UTC
workflow_dispatch:

jobs:
build:
runs-on: ubuntu-latest
permissions:
contents: write

Plain Text


steps:
  - uses: actions/checkout@v4
  - uses: Platane/snk@v3
    with:
      github_user_name: ${{ github.repository_owner }}
      outputs: |
        dist/github-snake.svg
        dist/github-snake-dark.svg?palette=github-dark

  - name: Commit and Push
    run: |
      git config user.name "github-actions[bot]"
      git config user.email "41898282+github-actions[bot]@users.noreply.github.com"
      git add dist/*.svg
      git commit -m "Update snake animation" || exit 0
      git push
```



2. Atualize seu README.md: Para suportar modos claro e escuro, use a seguinte estrutura:

Plain Text


```markdown
<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./dist/github-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="./dist/github-snake.svg" />
    <img alt="github-snake" src="./dist/github-snake.svg" />
  </picture>
</p>
```






<p align="center">
✨ Obrigado por visitar meu perfil!  

Sempre aberto a aprender, colaborar e evoluir 🚀👾
</p>

