# 👩🏻‍💻 Lucas Coriolano

**`Desenvolvedor Front-end`**

💻 Sobre mim:

👋 Olá! Meu nome é Lucas Coriolano, tenho 18 anos e sou do Rio de Janeiro - RJ.
<br>
🎓 Atualmente curso Análise e Desenvolvimento de Sistemas na UNISUAM (Centro Universitário Augusto Motta), em Bonsucesso, com previsão de conclusão em julho de 2027.
<br>
🚀 Objetivo: Busco uma oportunidade de estágio em TI/Desenvolvimento para aplicar meus conhecimentos, adquirir experiência prática e contribuir ativamente em projetos reais, enquanto continuo evoluindo como desenvolvedor.
<br>

---

### 🤖 Linguagens e Tecnologias

<img 
    align="left" 
    alt="HTML"
    title="HTML" 
    width="30px" 
    style="padding-right: 10px;" 
    src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/html5/html5-original.svg" 
/>
<img 
    align="left" 
    alt="CSS" 
    title="CSS"
    width="30px" 
    style="padding-right: 10px;" 
    src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/css3/css3-original.svg" 
/>
<img 
    align="left" 
    alt="JavaScript" 
    title="JavaScript"
    width="30px" 
    style="padding-right: 10px;" 
    src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-original.svg" 
/>

<br/>
<br/>

---

### 📊 Estatísticas

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=LucasCoriolano&hide_title=false&hide_rank=false&show_icons=true&include_all_commits=true&count_private=true&disable_animations=false&theme=dracula&locale=en&hide_border=false&order=1" height="150" alt="stats graph"  />
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=LucasCoriolano&locale=pt-br&hide_title=false&layout=compact&card_width=320&langs_count=5&theme=dracula&hide_border=false&order=2&custom_title=Tecnologias" height="150" alt="languages graph"  />
</div>


###

nome: gerar animação

sobre:
  # executar automaticamente a cada 24 horas
  agendar:
    - cron: "0 */24 * * *"
  
  # permite executar o trabalho manualmente a qualquer momento
  fluxo de trabalho_despacho:
  
  # executar em cada push no branch master
  empurrar:
    galhos:
    - mestre
    



empregos:
  gerar:
    permissões:
      conteúdo: escrever
    em execução: ubuntu-latest
    tempo limite-minutos: 5
    
    passos:
      # gera um jogo de cobra a partir do gráfico de contribuições de um usuário do github (<github_user_name>), gera uma animação svg em <svg_out_path>
      - nome: gerar github-contribution-grid-snake.svg
        usos: Platane/snk/svg-only@v3
        com:
          nome_de_usuário_github: ${{ github.repository_owner }}
          saídas: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
          
          
      # envie o conteúdo de <build_dir> para uma ramificação
      # o conteúdo estará disponível em https://raw.githubusercontent.com/<github_user>/<repository>/<target_branch>/<file > ou como página do github
      - nome: envie github-contribution-grid-snake.svg para o branch de saída
        usos: crazy-max/ghaction-github-pages@v3.1.0
        com:
          target_branch: saída
          diretório de compilação: dist
        ambiente:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
