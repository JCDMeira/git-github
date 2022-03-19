<h1 align='center' name='inicio'>
  Git e GitHub: um guia de estudo de procedimentos e tópicos importantes
  </h1>

  <div align='center'>
    <img src="./images/git-giHub.png" alt="git and gitHub">
  </div>
  </br>

# 📋 Indíce

-[1.0 - O que é git ?](#id01)

-[1.1 - Detalhes importantes](#id01.1)

</br>
  <p>
    Esse repositório reúne meus estudos e testes sobre git e gitHub. Será um apanhado de informações, se sinta livre para ler, salvar, forkar ou compartilhar o projeto, e se achar correções ou melhorias sua contribuição é bem vinda.
  </p>

  </br>

  <p>
    Lembrando que todo tipo de opinião sobre o uso de algum conceito ou ferramenta também está atrelado a minha visão da forma de se usar ou proceder. Sendo então parcial e não passando de uma recomendação, se acaso algo for normativo irei indicar em conjunto a própria informação da mesma.
  </p>

  </br>

  <p align="center">
   E se gostou do conteúdo deixe uma estrela para incentivar o trabalho.
  </p>
  
</br>
<a name="id01"></a>

  <h2>1.0 - O que é git ?</h2>

  </br>

  <p>
  Git é uma ferramenta de versionamento de código, e serve literalmente para criar versões, igual quando temos aplicativos com 1.0, 1.2, 2.5 e por aí vai.
  Não entrando em questões de como isso é numerado, a ideia é a mesma, é criado múltiplas versões do item em questão, que no caso se faça de código, ou mais especificamente arquivos de código.
  Porém o git é tão poderoso que pode criar versões de qualquer arquivo que se desejar.
  </p>

  </br>

  <p>
  Para explicar melhor o conceito de versionamento pode-se citar os diversos trabalhos de escola ou um TCC de curso ou graduação. Sempre se inicia com um nome, porém conforme passa por revisões tende-se a mudar o nome do arquivo, virando algo como:
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
  E isso dificulta muito o controle por que não é possível saber o que foi feito em cada parte, nem mesmo olhando daria pra saber exatamente qual a ordem em que vieram. Pois se houverem mais marcações pode gerar confuções.
  </p>

  </br>

  <p>
  Com git poderia se manter o nome e geral códigos de marcação e comentários, marcando as versões.
  </p>

  </br>

  <p>Git tenta responder algumas perguntas básicas</p>

</br>
  <ol>
    <li>O que mudou ?</li>
    <li>Quando mudou ?</li>
    <li>Por que mudou?</li>
    <li>Quem fez a mudança?</li>
    <li>Podemos reproduzir essa mudança?</li>
  </ol>
</br>

  <p>Isso gera uma estrutura de marcações de commit</p>
</br>

  <p align="center" >
  nome do Trabalho(arquivo) - data de alteração - código único de alteração (hash do commit) - comentário de alteração - quem alterou
  </p>

</br>
  <p>E quanto a replicação do comportamento, podemos conferir nas descrições de alteração dos arquivos alterados ou clonar o repositório em si</p>

  </br>

  <p>
  Seria muito mais fácil de fazer trabalho em grupo usando um versionador, e a ideia é essa mesma, porém com códigos.
  </p>

</br>
<a name="id01.1"></a>
  <h3>1.1 - Detalhes importantes</h3>
  <br>

  <li>
  Mais especificamente o git é um sistema de controle distribuido e isso que facilita e permite a colaboração em grupo para um mesmo projeto
  </li>

  <li>Git na verdade é chamado de GIT-SCM -> source control management</li>

  <li>Foi criado por Linus Torvalds em 2005, o mesmo criador do linux</li>

  <li>Nasceu com o propósito de auxiliar no desenvolvimento do linux</li>

  <br>
  <div align='center'>
    <img src="./images//linus.jpeg" alt="Linus Torvalds">
  </div>

<br>[⬆ Voltar ao top](#inicio) <br>
