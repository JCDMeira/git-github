<h1 align='center' name='inicio' id='inicio'>
    Git e GitHub: um guia de estudo, procedimentos e tópicos importantes
</h1>

<div align='center'>
    <img src="./images/git-giHub.png" alt="git and gitHub">
</div>
</br>

# 📋 Indíce

- [1.0 - O que é git ?](#id01)
  - [1.1 - Detalhes importantes](#id01.1)
- [2.0 - Ta, mas como o git funciona?](#id02.0)
  - [2.1 - Ciclos de vida](#id02.1)
- [3.0 - Criando um gitHub](#id03.0)
- [4.0 - Criando um repositório](#id04.0)
- [5.0 - Adicionar credenciais ao vs code](#id05.0)
- [6.0 - Conectando um repositório a uma origen remota](#id06.0)
- [7.0 - Comandos](#id07.0)
  - [7.1 - Git status](#id07.1)
  - [7.2 - Git log](#id07.2)
  - [7.3 - Git add](#id07.3)
  - [7.4 - Git commit](#id07.4)
  - [7.5 - Git push](#id07.5)
  - [7.6 - Git pull](#id07.6)
  - [7.7 - Git checkout](#i70.7)

</br>
<p>
    Esse repositório reúne meus estudos e testes sobre git e gitHub. Será um apanhado de informações, se sinta livre
    para ler, salvar, forkar ou compartilhar o projeto, e se achar correções ou melhorias sua contribuição é bem vinda.
</p>

</br>

<p>
    Lembrando que todo tipo de opinião sobre o uso de algum conceito ou ferramenta também está atrelado a minha visão da
    forma de se usar ou proceder. Sendo então parcial e não passando de uma recomendação, se acaso algo for normativo
    irei indicar em conjunto a própria informação da mesma.
</p>

</br>

<p align="center">
    E se gostou do conteúdo deixe uma estrela para incentivar o trabalho.
</p>

</br>
<a name="id01"></a>
<h2>1.0 - O que é git ?</h2>
<div align='right'>
    <a href="#inicio">⬆ Voltar ao top</a>
</div>

</br>

<p>
    Git é uma ferramenta de versionamento de código, e serve literalmente para criar versões, igual quando temos
    aplicativos com 1.0, 1.2, 2.5 e por aí vai.
    Não entrando em questões de como isso é numerado, a ideia é a mesma, é criado múltiplas versões do item em questão,
    que no caso se faça de código, ou mais especificamente arquivos de código.
    Porém o git é tão poderoso que pode criar versões de qualquer arquivo que se desejar.
</p>

</br>

<p>
    Para explicar melhor o conceito de versionamento pode-se citar os diversos trabalhos de escola ou um TCC de curso ou
    graduação. Sempre se inicia com um nome, porém conforme passa por revisões tende-se a mudar o nome do arquivo,
    virando algo como:
</p>

</br>

<p align="center">
    Trabalho-revisado
</p>
<p align="center">
    Trabalho-revisado-final
</p>
<p align="center">
    Trabalho-revisado-final-agoraVai
</p>

</br>

<div align='center'>
    <img src="./images/versoes-tcc.jpeg" alt="git and gitHub">
</div>

<p>
    E isso dificulta muito o controle por que não é possível saber o que foi feito em cada parte, nem mesmo olhando
    daria pra saber exatamente qual a ordem em que vieram. Pois se houverem mais marcações pode gerar confuções.
</p>

</br>

<p>
    Com git poderia se manter o nome e geral códigos de marcação e comentários, marcando as versões.
</p>

</br>

<p>Git te responde algumas perguntas básicas sobre as alterações feitas.</p>

</br>
<ol>
    <li>O que mudou ?</li>
    <li>Quando mudou ?</li>
    <li>Por que mudou?</li>
    <li>Quem fez a mudança?</li>
    <li>Podemos reproduzir essa mudança?</li>
</ol>
</br>

<p>Isso gera uma estrutura de marcações de commit, que evidencia essas informações.</p>
</br>

<p align="center">
    nome do Trabalho(arquivo) - data de alteração - código único de alteração (hash do commit) - comentário de alteração
    - quem alterou
</p>

</br>
<p>E quanto a replicação do comportamento, podemos conferir nas descrições de alteração dos arquivos alterados ou clonar
    o repositório em si</p>

</br>

<p>
    Seria muito mais fácil de fazer trabalho em grupo usando um versionador, e a ideia é essa mesma, porém com códigos.
</p>

</br>
<a name="id01.1"></a>
<h3>1.1 - Detalhes importantes</h3>
<div align='right'>
    <a href="#inicio">⬆ Voltar ao top</a>
</div>
<br>

<li>
    Mais especificamente o git é um sistema de controle distribuido e isso que facilita e permite a colaboração em grupo
    para um mesmo projeto
</li>

<li>Git na verdade é chamado de GIT-SCM -> source control management</li>

<li>Foi criado por Linus Torvalds em 2005, o mesmo criador do linux</li>

<li>Nasceu com o propósito de auxiliar no desenvolvimento do linux</li>

<br>
<div align='center'>
    <img src="./images/linus.jpeg" alt="Linus Torvalds">
</div>

</br>
<a name="id02.0"></a>
<h3>2.0 - Ta, mas como o git funciona?</h3>
<div align='right'>
    <a href="#inicio">⬆ Voltar ao top</a>
</div>
<br>

<p>
    Como o git é um sistema de gerenciamento de controle de versões de código (arquivos e documentos se olhar de modo mais geral), ele possui recursos avançados para monitorar e acompanhar o que os arquivos do projeto em si.
</p>

<p>
    Isso conta tanto em alterações no arquivo quanto o caminho dentro das pastas (diretórios).
</p>
<p>
    Isso o permite monitorar todas as mudanças ocorridas, logo a partir do momento que é iniciado no projeto. Geralmente esse processo ocorre no repositório local, e a cada alteração isso é indicado e mapeado pela ferramenta.
</p>

<br>
<div align='center'>
    <img src="./images/mudancas.png" alt="mostra mudanças ocorridas em arquivos supervisionados pelo sistema git">
</div>
</br>

<p>
    A primeira parte indicada mostra que o código era como estava a esquerda, mas isso foi removido e então está em vermelho.
    E então ficou como está a direita, e como foi adicionado está em verde.
</p>
<p>
    Sendo na realidade apenas uma mudança de formatação, por isso indica que algo foi removido e agora se tem um novo bloco.
</p>

<p>
    Já a segunda parte que mostra um espaço vazio a esquerda e um texto em com fundo em verde a direita mostra adição de parte totalmente novas.
</p>

</br>
<a name="id02.1"></a>
<h3>2.1 - Ciclos de vida</h3>
<div align='right'>
    <a href="#inicio">⬆ Voltar ao top</a>
</div>
<br>

<p>
    As mudanças monitoradas são demonstrada através de um poderoso sistema que pode ser chamado como relativo a estágios ou fases.
</p>
<img src="./images/git-lifecycle.png" alt="ciclos de vida dos arquivos no git">
<br>
<p>Cada fase representa algo que ocorre com os arquivos, há imagens com mais detalhes ou até mais comandos ou relações a estados. Mas o primeiro contato está relativo a um ciclo resumido.</p>
<p>
    De modo geral, após se linkar um repositório ao git, o sistema git está monitorando esses arquivos, mas eles não foram se quer adicionados para o monitoramentos, então ficam contando estado como untracked.
</p>
<p>
    Ao usar o comando git add, e o estado do arquivo se torna staged, ou seja, agora o arquivo se torna monitorado pelo sistema git.
</p>
<p>
    Após isso, se usar o git commit se torna unmodified, que diz que as alterações do arquivo estão fixadas, e também estão como não modificados e podem ser upados para o repositório remoto.
</p>
<p>
    Qualquer alterações a partir do momento que o arquivo foi adicionado ao monitoramento git, ele se torna modified, indicando que a modificações que devem ser adicionadas.
</p>
<p>
    Esses são os estados ou fases básicas dp git, a seguir será mencionado com mais detalhes os comandos e ações em geral.
</p>
</br>
<a name="id03.0"></a>
<h3>3.0 - Criando um gitHub</h3>
<div align='right'>
    <a href="#inicio">⬆ Voltar ao top</a>
</div>
<br>

<p>
    O processo de criação de um gitHub é bem simples é preciso acessar o site do gitHub através do link <a href="https://github.com">https://github.com</a>.
</p>

<p>
    A tela será a seguinte:
</p>
<div align='center'>
<img style='width: 800px' src="./images/gitHub.png" alt="página gitHub">
</div>
</br>
<p>
    Deve se clicar em <strong>Sign up</strong> no canto superior direito.
</p>

<p>
    Então preencher os dados comuns, que são email, senha e nome de usuário.
</p>
<p>
    Também será pedido um número de código que foi enviado para e-mail informado nos daos. Como uma confirmação para e-mail válido.
</p>
<p>
    Daí é só escolher se você quer receber notificações do gitHub e responder o captcha para concluir a primeira etapa.
</p>
<p>
    O procedimento pode ser visto na gif abaixo :
</p>
</br>

<div align='center'>
    <img style='width: 800px' src="./images/criando00.gif" alt="procedimento de criar um gitHub">
</div>

</br>

<p>
    Logo depois há algumas configurações a se preencher
</p>

<p>
    O primeiro é a pergunta de quantas pessaos atuam na equipe, no geral será respondido "apenas eu", porque é sua conta pessoal. 
</p>

</br>
<div align='center'>
    <img style='width: 800px' src="./images/criando01.png" alt="procedimento de criar um gitHub">
</div>

</br>
<p>
    O segundo são possíveis usos para sua conta do gitHub, se tiver focos em mente já é legal colocar. Se não tiver, recomendo colocar pelo menos o último, que menciona comunidade. 
</p>

</br>
<div align='center'>
    <img style='width: 800px' src="./images/criando02.png" alt="procedimento de criar um gitHub">
    <img style='width: 800px' src="./images/criando03.png" alt="procedimento de criar um gitHub">
    <img style='width: 800px' src="./images/criando04.png" alt="procedimento de criar um gitHub">
</div>

</br>
<p>
    O terceiro tópico é sobre escolher modalidade free ou modalidade paga, aqui escolha o free que é mais que suficiente.
</p>

</br>
<div align='center'>
    <img style='width: 800px' src="./images/criando05.png" alt="procedimento de criar um gitHub">
</div>

<p>
    E pronto, sua conta esta criada e já é possível criar repositórios com projetos, gerar commits e participar da comunidade em si.
</p>

</br>
<a name="id04.0"></a>
<h3>4.0 - Criando um repositório</h3>
<div align='right'>
    <a href="#inicio">⬆ Voltar ao top</a>
</div>
<br>

<p>
    Primeiramente, cabe dizer que um repositório é no sentido do dicionário, um lugar onde se armazena, guarda, arquiva ou coleciona alguma coisa. E nesse caso, um repositório git se destina, primáriamente, a guardar projetos e códigos. Assim como temos a ferramenta git monitorando as versões dos nossos arquivos dentro de um projeto, teremos os repositórios para alocar os projetos e suas estruturas de pastas e arquivos. 
</p>

<p>
    Esses repositórios são um ambiente remoto, que alocam os dados em uma espécie de nuvem. Assim, nossos códigos versionados podem ficar em um lugar seguro. E nos permite compartilhar códigos e projetos, demonstrar a evolução dos projetos em si e da nossa maneira de codar e trabalhar com projetos. Além de também nos permitir criar uma espécie de portfólio e mapa de trajetória. 
</p>
<p>
    Sendo também possível ter contato com códigos e projetos de outros programadores e projetos open source.
</p>

<p>
    Para criar um repositório é um processo bem simples. Basta clicar no simbolo + (de mais) no canto direito superior da página. Estará entre o sininho de notificações e a foto de perfil.
</p>

<br>
<div align='center'>
    <img style='width: 800px' src="./images/repositorio01.png" alt="procedimento de criar um gitHub">
</div>

<p>
    Ao clicar aparecerá opções. Então aparecerá opções, a primeira é para criar um novo repositório.
</p>

<br>
<div align='center'>
    <img style='width: 600px' src="./images/repositorio02.png" alt="procedimento de criar um gitHub">
</div>

<p>
    Irá abrir uma janela conforme abaixo.
</p>

<br>
<div align='center'>
    <img style='width: 800px' src="./images/repositorio03.png" alt="procedimento de criar um gitHub">
</div>

<p>
    você estará colocado como dono do repositório (owner), e será necessário um nome para ele (repository name). A descrição (Description) do que é esse repositório é opicional, eu costumo colocar após já fazer coisas no repositório, pois terei uma visão mais clara de como descrevê-lo, porém se decidir adicionar já na abertura já pode também.
</p>
<p>
    Uma opção logo abaixo da descrição é se o repositório será público (public) ou privado (private), se for público qualquer pessoa que acessar seu perfil poderá ver o repositório, se for privado apenas você ou quem tiver permição poderá ver. É importante colocar como público caso sejam projetos pessoais e para portfólio.
</p>
<p>
    Outro detalhe é que commits em repositórios privados só contam se você ativar a opção de mostrar contribuições privadas. Caso contrário, qualquer commit feito em repositórios privados não irão contar no seu histórico de contribuições.
</p>

<br>
<div align='center'>
    <img style='width: 800px' src="./images/repositorio03.05.png" alt="procedimento de criar um gitHub">
</div>

<p>
    A última parte de configurações é adicionar ou não um readme (para descrever o repositório e informações importantes), um .gitignore (que indica arquivos e diretórios que o git não irá monitorar) e uma licença. Esses inicialmente ficam como opcionais mesmo, mesmo criando sem é possível criar depois.
</p>

<p>
    <strong>Preenchendo tudo é só clicar em 'create repository'</strong> e pronto, já temos o repositório criado.
</p>

</br>
<a name="id05.0"></a> 
<h3>5.0 - Adicionar credenciais ao vs code</h3>
<div align='right'>
    <a href="#inicio">⬆ Voltar ao top</a>
</div>
<br>

<p>
    Adicionar suas credenciais é necessário para que os commits fiquem registrados no seu nome. Sendo fácil de entender quem fez que alteração e também para preencher o histórico de commits na página inicial do seu gitHub.
</p>
<p>
    O processo todo é bem fácil, podendo entrar no terminal integrado do vs code pra isso, sendo esse terminal qual for. O processo vai ser clicar em terminal na parte superior esquerda.
</p>

<br>
<div align='center'>
    <img style='width: 800px' src="./images/credenciais01.png" alt="procedimento de criar um gitHub">
</div>
<br>

<p>
    E então o terminal que está definido como padrão do vs code irá abrir na parte inferior. Sendo o meu o ZSH.
</p>

<br>
<div align='center'>
    <img style='width: 800px' src="./images/credenciais02.png" alt="procedimento de criar um gitHub">
</div>
<br>

<p>
    O processo pode ser visto abaixo:
</p>

<br>
<div align='center'>
    <img style='width: 800px' src="./images/credenciais03.gif" alt="procedimento de criar um gitHub">
</div>
<br>

<p>
    Então será inserido o nome e e-mail de usuário.
</p>

<p>
    Para configurar as credenciais para apenas o projeto que está mexendo no momento, deve se usar os comandos abaixo, setando nome e e-mail para o projeto, de modo local.
</p>

```bash
# configura o nome de usuário de modo local
git config  user.name "Um nome maneiro"
```

```bash
# configura o email de usuário de modo local
git config  user.email "email.maneiro@exemplo.br"
```

<p>
    Já para configurar o nome e e-mail de forma global, se usa o mesmo comando, mas adicionando a flag --global. Que faz com que o nome e usuário sejam definidos para o computador. E todo projeto que você mexer com esse computador irá usar essas credenciais por padrão, a não ser que seja mudado ou configurado um outro nome e e-mail localmente para um projeto após sua abertura.
</p>

```bash
# configura o nome de usuário de modo global
git config --global user.name "Um nome maneiro"
```

```bash
# configura o email de usuário de modo global
git config --global user.email "email.maneiro@exemplo.br"
```

<p>
    Após qualquer um dos comandos de configuração o usuário está configurado e é possível enviar commits assinados por você.
</p>

<strong>Só cabe lembrar que não é recomendado usar configurações globais em um computador que possa ser acessado por várias pessoas.</strong>

</br>
<a name="id06.0"></a> 
<h3>6.0 - Conectando um repositório a uma origen remota</h3>
<div align='right'>
    <a href="#inicio">⬆ Voltar ao top</a>
</div>
<br>

<p>
    Para enviar os commits feitos localmente para um repositório remoto é preciso definir a origem em que se encontra esse repositório. Há mais de uma maneira de fazer isso, mas talvez a mais rápida e simples é via um endereço HTTPS. Que já é fornecido pelo gutHub ao criar uma repositório.
</p>

<br>
<img src="./images//conectando01.png" alt="conectando repositório">
<br>

<p>
    Após criar o repositório no github, crie uma pasta local que conterá seu projeto, servindo como um repositório local. Nele digite o comando de git init para iniciar o monitoramento git nos arquivos.
</p>
<br>

```bash
git init
```

<p>
    Então pegue o comando da primeira linha do segundo bloco da imagem anterior.
</p>

```bash
git remote add origin https://github.com/JCDMeira/creando-rep.gi
```

<p>
    Isso adicionará a origin ao repositório, sendo possível agora adicionar os arquivos e subir para o repositório remoto.
</p>

<P>
    Já quanto ao processo de subir os dados propriamente ditos vamos ver em breve mais a frente.
</P>

</br>
<a name="id07.0"></a>
<h2>7.0 - Comandos</h2>
<div align='right'>
    <a href="#inicio">⬆ Voltar ao top</a>
</div>
</br>

<p>
    No geral tudo no git será realizado por comandos, e aprender a manipular as situações via comandos é essencial. Até é possível hoje em dia manipular tudo via interface, mas isso te torna nada mais que um apertador de botões.
</p>
<p>
    Aprender realmente a usar os comandos é que te torna um melhor profissional, e após masterizar os comandos, mesmo que não seja completamente (isso seria muito difícil), é possível usar a interface a seu favor em alguns casos.
</p>

</br>
<a name="id07.1"></a>
<h2>7.1 - Git status</h2>
<div align='right'>
    <a href="#inicio">⬆ Voltar ao top</a>
</div>
</br>

<p>
    O comando <strong>git status</strong> serve para ver os status atuais de cada arquivo no projeto. Permitindo ver em que momento do ciclo de vida eles estão.
</p>
<p>
    Permitindo com isso entender quais são os próximos passos para manipular esses arquivos.
</p>

</br>
<a name="id07.2"></a>
<h2>7.1 - Git log</h2>
<div align='right'>
    <a href="#inicio">⬆ Voltar ao top</a>
</div>
</br>

<p>
    O comando <strong>git log</strong> permite que seja visto o histórico de commits do projeto. 
</p>
<p>
    O log simples mostra apenas os últimos commits feitos, mas é possível usar <strong>git log --all</strong> para mostrar todos os commits feitos. Ou o <strong>git log --oneline</strong> para mostrar os últimos com informações resumidas.
</p>
<p>
    Outro fator importante de se notar é que o comando abre um modo diferente no terminal. <strong>E para sair do modo log é só apertar a tecla q do teclado</strong>
</p>

<img src="./images/log01.png" alt="">

<p>
    Outra função importante do log, mas que é pouco conhecida, é que há uma função de pesquisa no comando. Enquanto na tela de log se teclar <strong>/</strong> entra em um modo de pesquisa, que permite pesquisar por palavras que aparecem nas mensagens dos commits.
</p>

<img src="./images/log02.png" alt="">

<p>
    Após executar uma pesquisa é possível voltar para o todo dos commits apertando a tecla <strong>b</strong>
</p>

<p>
    Além disso há outras flags além de all que podem ser úteis
</p>

<p>
    Pesquisar commits anteriores a uma data:
    <strong>git log --before="2022-04-01"</strong>
</p>

<p>
    Pesquisar commits posteriores a uma data:
    <strong>git log --after="2022-04-01"</strong>
</p>

<p>
    Pesquisar commits entre datas:
    <strong>
        git log --before="2022-04-01" --after="2022-06-01" 
    </strong>
</p>

<p>
    Pesquisar commits desde:
    <strong>
        git log --since="2 days ago"
    </strong>
</p>

<p>
    pesquisar commits por autor:
    <strong>
        git log --author="jean"
    </strong>
</p>

<p>
    Esses recursos permitem fazer uma busca mais focada nos commits feitos. 
</p>

</br>
<a name="id07.3"></a>
<h2>7.1 - Git add</h2>
<div align='right'>
    <a href="#inicio">⬆ Voltar ao top</a>
</div>
</br>

<p>
    O comando <strong>git add</strong> permite adicionar os arquivos e diretórios para o estado de tracked, ou seja, monitorados. Há diversas formas diferentes de se usar o comando, divergindo o comportamento do mesmo.
</p>

<strong>Adicionar um arquivo ou diretório</strong>

<p>git add caminho_do_arquivo-diretorio</p>
<p>
    Um exemplo para algo que esteja na raiz.
</p>

<strong>
    Para o arquivo readme que está na raiz.
</strong>
<p>
    git add readme.md
</p>
<strong>
    Para o diretório images que está na raiz.
</strong>
<p>
    git add images/
</p>

<strong>
    Adicionar todos arquivos e diretórios novos, modificados e deletados. do diretório atual em diante.
</strong>
<p>git add .</p>
<p>
    Ao usar o ponto, todos os arquivos e pastas são registrados. Sejam novos arquivos, as mudanças feitas em um arquivo já monitorado ou mesmo arquivos que foram deletados. Todas alterações são computadas.
</p>
<p>
    Um ponto de alerta para usar o ponto é que se estiver dentro de um diretório no projeto e não na raiz. As alterações que serão contadas é do ponto do projeto em que se está em diantes (pastas e arquivos dentro da pasta atual).
</p>

<strong>
    Adicionar todos arquivos e diretórios todos arquivos, da raiz em diante
</strong>
<p>git add --all ou git add -A </p>
<p>
    Usar --all ou -A garante o mesmo comportamento do git add . com a diferença que o ponto de partida vai ser a raiz do projeto. Sendo sempre adicionada todas as alterações do projeto.
</p>

<strong>
    Adicionar no Stage apenas arquivos modificados e removidos, não adicionando os novos arquivos.
</strong>
<p>
    git add -u
</p>
<p>
    A flag -u faz com que os novos arquivos não tenham suas mudanças adicionadas. Apenas arquivos que já existiam, e pode haver alterações no arquivo ou mesmo o a ação de deletar o arquivo todo.
</p>

<strong>
    Adicionar todos arquivos novos e diretórios, do repositório em diante. Mas não conta os arquivos deletados.
</strong>
<p>git add * </p>

<p>
    O git add * não computa deleções, e por isso serve um grande aviso aqui, dependendo de como estiver seu projeto, usar muito o comando com o asterisco irá gerar conflitos. Pois o uso de pull e push não irão contar arquivos deletados, e isso pode conflitar em algum momento (tende fortemente a gerar conflitos).
</p>

<p>
    Em pesquisas vi dizeres de que o comando com o asterisco não adicionava arquivos começados em . também, mas nos testes que fiz a única diferença dele para o git add . foi não computar deleções.
</p>

</br>
<a name="id07.4"></a>
<h2>7.4 - Git commit</h2>
<div align='right'>
    <a href="#inicio">⬆ Voltar ao top</a>
</div>
</br>

<p>
    commits são a passagem dos arquivos que estão trackeados para o estatus staged.
    Deixando eles prontos para enviar ou submeter para o repositório remoto (principal).
</p>
<p>
    Os commits são o ato de efetivar as mudanças feitas, sejam ela alterações, remoções ou adições.
</p>
<p>
    O commit cria uma espécie de "fotografia" do momento atual do projeto, e essa fotografia é marcada por um hash_id. Que nada mais é que uma sequencia alfa numérica única, que define aquele momento do projeto. 
</p>
<p>
    Com momento se entende o estado que cada arquivo tinha, a estrutura de pastas e tudo que o projeto continha naquele commit. Sendo possível assim criar um histórico de alterações e voltar a um determinado commit se necessário.
</p>

<p>
    Em geral nos commmits se passa uma mensagem, através da flag -m, essa mensagem fala de modo resumido o que foi a alteração causada por aquele commit.
</p>

<p>
    <strong>
        gi commit -m 'mensagem do commit'
    </strong>
</p>

</br>
<a name="id07.5"></a>
<h2>7.5 - Git push</h2>
<div align='right'>
    <a href="#inicio">⬆ Voltar ao top</a>
</div>
</br>

<p>
    O git push envia as alterações commitadas localmente para o repositório marcado como a origin remota. Do ingles push é empurrar, e é de certa forma isso que é feito, os commits são "empurrados" para o repositório remoto.
</p>

<p>
    <strong>
        git push
    </strong>
</p>

<p>
    Uma informação importante é que geralmente o push precisa indicar a origin a qual se quer enviar os commits. Que geralmente será a branch que se quer que receba os commits.
</p>

<p>
    <strong>
        git push origin minha_origin
    </strong>
</p>

<p>
    Para facilitar é possivel configurar uma origin para aquela branch. E assim ela fica salva e todo commit após isso fica direcionado aquela origin.
</p>

<p>
    <strong>
        git push --set-upstrean origin minha_origin
    </strong>
</p>

<p>
    O que também pode ser feito usando a flag -u que vem de upstrean
</p>

<p>
    <strong>
        git push -u origin minha_origin
    </strong>
</p>

<br>[⬆ Voltar ao top](#inicio) <br>
