# <div align="center"> Git Flow  :memo: ​ </div>

<div align="center"> <img alt="GitHub forks" src="https://img.shields.io/github/forks/tayhsn/git-flow?logoColor=blue&style=social"> <img alt="GitHub Repo stars" src="https://img.shields.io/github/stars/tayhsn/git-flow?logoColor=black&style=social"> </div>

### Workflow para projetos colaborativos :octocat:

Para facilitar, faça um FORK para copiar o repositório ou deixe uma STAR para salva-ló. :sparkles:

<hr>
<h3 align="center"> Você precisa ter o git previamente instalado. </h3>

<div align="center">  <a href="#init"> INIT </a> | <a href="#features"> FEATURES </a> | <a href="#release"> RELEASE </a> | <a href="#hotfix"> HOTFIX </a></div>
<br>
<div align="center">
    <img src="https://danielkummer.github.io/git-flow-cheatsheet/img/git-flow-commands.png" alt="Git Flow Cheatsheet"/> 
</div>

<hr>

## Init

* Faça a inicialização do git-flow  dentro de um repositório git existente com

  ​	``` GIT FLOW INIT ```

Você precisa responder algumas questões relativas às convenções de nomenclatura dos suas branches. **É recomendado que sejam usados os valores padrões.** 

<hr>

## Features

!Important: O desenvolvimento acontece na branch 'develop'

* Para comecar a desenvolver, digite

  ​	``` GIT FLOW FEATURE START my_feature ```

Esse comando cria uma nova branch dentro de 'develop' e alterna para ela

* Finalize o desenvolvimento com

  ​	``` GIT FLOW FEATURE FINISH my_feature ```

Esse comando merge 'my_feature' em 'develop', remove 'my_feature' e segue na 'develop'

* Publique uma funcionalidade

  ​	``` GIT FLOW FEATURE PUBLISH my_feature ```

Assim ela pode ser utilizada por outras pessoas do time.

* Veja as funcionalidades publicadas

  ​	```GIT FLOW FEATURE PULL my_feature ```

E acompanhe o desenvolvimento

<hr>

## Release

Permite correções de bugs menores e a preparação de metadados de uma versão

* Para começar uma versão

  ​	```GIT FLOW RELEASE START my_release [commit] ```

Você pode opcionalmente fornecer a hash sha-1 do commit de onde começar a versão. O commit precisa estar no branch 'develop'

* É sensato publicar a branch da versão depois de criá-la, para permitir commits por outros desenvolvedores

  ​	``` GIT FLOW RELEASE PUBLISH my_release```

(Você pode acompanhar uma versão remota com o comando ```GIT FLOW RELEASE TRACK release ```)

* A finalização de uma versão é um dos grandes passos na ramificação/branching do git. 

  ​	``` GIT FLOW RELEASE FINISH release ```

Ele executa várias ações: merge a 'release' no 'main' e na 'develop', etiqueta a versão com seu nome e remove a branch.

<hr>

## HotFix

Os hotfixes surgem da necessidade de agir imediatamente sobre uma situação indesejada na versão de produção ativa. Pode ser criado a partir da tag correspondente no branch main que indica a versão em produção.

* Assim como os outros comandos do git flow, um hotfix inicia com

  ​	```GIT FLOW HOTFIX START version [basename] ```

O argumento version marca o nome do novo hotfix. Opcionalmente, você pode especificar um basename para começar.

* Ao finalizar um hotfix ele é mesclado tanto no 'develop' quanto no 'main'.

  ​	```GIT FLOW HOTFIX FINISH version ```

Além disso, o merge no main é etiquetado.

<hr>

Documentação: https://danielkummer.github.io/git-flow-cheatsheet/index.pt_BR.html
