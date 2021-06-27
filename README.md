# <div align="center"> Git Flow  :memo: ​ </div>

<div align="center"> <img alt="GitHub forks" src="https://img.shields.io/github/forks/tayhsn/git-flow?logoColor=blue&style=social"> <img alt="GitHub Repo stars" src="https://img.shields.io/github/stars/tayhsn/git-flow?logoColor=black&style=social"> </div>

### O melhor workflow para projetos colaborativos :octocat:

Para facilitar, faça um FORK para copiar o repositório ou deixe uma STAR para salva-ló. :sparkles:

<hr>

<div align="center">
<p>Git Flow Cheatsheet (Comandos) <p>
<img src="https://danielkummer.github.io/git-flow-cheatsheet/img/git-flow-commands.png" alt="Git Flow Cheatsheet"/>
</div>

<h3 align="center"> Você precisa do git instalado como pré-requisito. </h3>

<hr>

### Init

* Comece o uso do git-flow fazendo sua inicialização dentro de um repositório git existente

``` GIT FLOW INIT ```

Você precisa responder algumas questões relativas às convenções de nomenclatura dos seus branches. **É recomendado que sejam usados os valores padrões.** 

<hr>

### Features

- Desenvolva novas funcionalidades para as versões futuras
- Normalmente existem apenas nos repositórios dos desenvolvedores

Tip: O desenvolvimento começa no branch 'develop'

* Comece o desenvolvimento da nova funcionalidade com

``` GIT FLOW FEATURE START my_feature ```

Esse comando cria um novo branch da funcionalidade baseado no 'develop' e alterna para ele

* Finalizando o desenvolvimento da funcionalidade

``` GIT FLOW FEATURE FINISH my_feature ```

Esse comando mescla my_feature no 'develop', remove o branch da funcionalidade e volta para o branch 'develop'

* Publique a funcionalidade

``` GIT FLOW FEATURE PUBLISH my_feature ```

Assim ela pode ser utilizada por outras pessoas do time.

* Receba as funcionalidades publicadas

```GIT FLOW FEATURE PULL my_feature ```

Para acompanhar o desenvolvimento

<hr>

### Release

* Para começar uma versão, cria-se um branch da versão baseado no branch 'develop'.

```GIT FLOW RELEASE START my_release [commit] ```

Você pode opcionalmente fornecer um hash sha-1 do commit [commit] de onde começar a versão. O commit precisa estar no branch 'develop'

*  É sensato publicar o branch da versão depois de criá-lo, para permitir commits por outros desenvolvedores

``` GIT FLOW RELEASE PUBLISH my_release```

(Você pode acompanhar uma versão remota com o comando ```GIT FLOW RELEASE TRACK release ```)

* A finalização de uma versão é um dos grandes passos na ramificação/branching do git. 

``` GIT FLOW RELEASE FINISH release ```

Ele executa várias ações: Mescla o branch da versão no 'master', Etiqueta a versão com seu nome, Mescla o branch da versão de volta no 'develop', Remove o branch da versão

<hr>

### HotFix

- Os hotfixes surgem da necessidade de agir imediatamente sobre uma situação indesejada na versão de produção ativa
- Pode ser criado a partir da tag correspondente no branch master que indica a versão em produção.

* Assim como os outros comandos do git flow, um hotfix inicia com

```GIT FLOW HOTFIX START version [basename] ```

O argumento version marca o nome do novo hotfix. Opcionalmente, você pode especificar um basename para começar.

* Ao finalizar um hotfix ele é mesclado tanto no develop quanto no master.

```GIT FLOW HOTFIX FINISH version ```

Além disso, o merge no master é etiquetado.

<hr>

Documentação: https://danielkummer.github.io/git-flow-cheatsheet/index.pt_BR.html
