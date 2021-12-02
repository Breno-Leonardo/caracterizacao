# Caracterização de Linguagens de Programação

## Linguagem de Programação: Java

  * [Apresentação e histórico](#apresentação-e-histórico)
   * [Características da Linguagem](#características-da-linguagem)
  * [Capacidades da Linguagem](#capacidades-da-linguagem)
  * [Produtividade do Desenvolvedor](#produtividade-do-desenvolvedor)
  * [Ecossistema](#ecossistema)
 

## Apresentação e histórico

Java foi originalmente designada para interagir com televisão, mas também foi avançada para a indústria de TV a cabo digital no momento. A história do java começa com o time Green. Os membros da equipe java (também conhecido como Time Green), iniciaram este projeto para desenvolver uma linguagem para dispositivos digitais tais como receptor de televisão, TVs, etc. Entretanto, foi adaptada para programação no âmbito da internet. Mais tarde, a tecnologia java foi incorporada pelo Netscape.

Os princípios para criação de programas java eram "simplicidade, robustez, portabilidade, Independência de plataforma, segurança, alta performance, multithread, arquitetura neutra, orientação a objeto, interpretada e dinâmica". Java foi desenvolvida por James Gosling, que é conhecido como o pai do java, em 1995. James Gosling e os membros do seu time começaram o projeto no início dos anos 90.

![image](https://user-images.githubusercontent.com/58619307/144495180-dba02911-e3d4-43cf-b436-6ea602f6ee3d.png)

## Características da Linguagem

## Paradigma

Java é multi-paradigma, alguns exemplos são : Programação Orientada a objetos, Programação Funcional, Imperativo, Genérico, mas o pricipal é Programação Orientada a objetos é por ele que a linguagem é mais reconhecida.

## Propósito 

Seu propósito é permitir que os desenvolvedores escrevam o programa apenas uma vez e o executem por meio de qualquer dispositivo.

## Sistema de Tipagem

O Java é uma linguagem de tipagem estática, ou seja, existe um sistema de tipos bem definido e que é validado durante o tempo de compilação do código. Para isso, é necessário definir tipos explícitos para as variáveis que são criadas.

Existem algumas vantagens atreladas à utilização de sistemas de tipos estáticos como: equívocos de tipagem geralmente são percebidos com mais facilidade, além de que os processos de refatoração tendem a ser mais a prova de equívocos. Se acaba sendo necessário trocar o tipo de um parâmetro de uma função, por exemplo, o código não irá compilar até que todos os locais que referenciam o método passem a especificar o tipo correto.

## Ambiente de Execução

### Modelo de tradução
Um programa Java é primeiro compilado para uma versão binária dos bytecodes Java, após isso é executado no interpretador Java Virtual Machine (JVM). A JVM por sua vez link-edita os métodos desejados na biblioteca Java enquanto o programa está sendo executado, para conseguir um melhor desempenho, a JVM chama o compilador Just-In-Time (JIT), que compila métodos seletivamente para a linguagem nativa da máquina em que está executando. Detalhando melhor:
### Compilação
O arquivo '.java' é passado para o compilador. Este será convertido em um código-fonte (bytecode). Após isso o compilador executa os seguintes passos:

Parse: Lê um conjunto de arquivos de origem * .java e mapeia a sequência de tokens resultante em nós AST (Abstract Syntax Tree).

Enter : Insere símbolos para as definições na tabela de símbolos.

Process annotations: Se solicitado, processa as anotações encontradas nas unidades de compilação especificadas.

Attribute: Atribui as árvores de sintaxe. Esta etapa inclui resolução de nome, verificação de tipo e constant folding.

Flow : Analisa o fluxo de dados nas árvores, realizando verificação de atributos e também acessibilidade.

Desugar : Reescreve as AST e traduz algum Sintatic Sugar

Generate: São gerados arquivos '.Class'.

### Execução
Os arquivos de classe gerados pelo compilador são independentes da máquina ou do sistema operacional, o que permite que sejam executados em qualquer sistema. Para executar, o arquivo de classe principal (a classe que contém o método main) é passado para a JVM e, em seguida, passa por três estágios principais antes que o código de máquina final seja executado. Essas etapas são:

**Class Loader**

A classe principal é carregada na memória passando seu arquivo ‘.class’ para a JVM, chamando a última. Todas as outras classes referenciadas no programa são carregadas por meio do carregador de classes. 
Existem dois tipos de carregadores de classes: primordial e não primordial. O carregador de classes primordial está integrado em todas as JVMs e é o carregador de classes padrão. Um carregador de classes não primordial é um carregador de classes definido pelo usuário, que pode ser codificado para personalizar o processo de carregamento de classes. O carregador de classes não primordial, se definido, é preferível ao padrão, para carregar classes.

**Bytecode Verifier**

Depois que o bytecode de uma classe é carregado pelo carregador de classe, ele deve ser inspecionado pelo verificador de bytecode, cujo trabalho é verificar se as instruções não executam ações prejudiciais. A seguir estão algumas das verificações realizadas:

As variáveis são inicializadas antes de serem usadas.

As chamadas de método correspondem aos tipos de referências de objeto.

As regras para acessar dados e métodos privados não são violadas.

Os acessos de variáveis locais se enquadram na pilha de tempo de execução.

A pilha de tempo de execução não transborda.

Se alguma das verificações acima falhar, o verificador não permitirá que a classe seja carregada.

**Just-In-Time Compiler**

Este é o estágio final encontrado pelo programa java e seu trabalho é converter o bytecode carregado em código de máquina. Ao usar um compilador JIT, o hardware pode executar o código nativo, ao contrário de ter o JVM interpretando a mesma sequência de bytecode repetidamente e incorrendo na penalidade de um processo de tradução relativamente longo. Isso pode levar a ganhos de desempenho na velocidade de execução, a menos que os métodos sejam executados com menos frequência.

## Nomes, variáveis e vinculação

### Nomes

As convenções de nomenclatura padrão do Java, você facilita a leitura do código. A legibilidade do programa Java é muito importante. Isso indica que menos tempo é gasto para descobrir o que o código faz.

As principais regras que devem ser seguidas por todos os identificadores:

  o	O nome não deve conter espaços em branco.

  o	O nome não deve começar com caracteres especiais como & (e comercial), $ (dólar), _ (sublinhado).

**Classe**

  o	Deve começar com a letra maiúscula.
  
  o	Deve ser um substantivo como Cor, Botão, Sistema, Tópico, etc.
  
  o	Use palavras apropriadas, em vez de siglas.
  
**Interface**

  o	Deve começar com a letra maiúscula.
  
  o	Deve ser um adjetivo como Runnable, Remote, ActionListener.
  
  o	Use palavras apropriadas, em vez de siglas.
  
**Método**

  o	Deve começar com letra minúscula.
  
  o	Deve ser um verbo como main(), print(), println().
  
  o	Se o nome contiver várias palavras, inicie-o com uma letra minúscula seguida por uma letra maiúscula, como actionPerformed().
  
**Variável**

  o	Ele deve começar com uma letra minúscula, como id, nome.
  
  o	Não deve começar com caracteres especiais como & (e comercial), $ (dólar), _ (sublinhado).
  
  o	Se o nome contiver várias palavras, inicie-o com a letra minúscula seguida por uma letra maiúscula como firstName, lastName.
  
  o	Evite usar variáveis de um caractere, como x, y, z.
  
**Pacote**

  o	Deve ser uma letra minúscula, como java, lang.
  
  o	Se o nome contiver várias palavras, ele deverá ser separado por pontos (.) Como java.util, java.lang
  
**Constante**

  o	Deve estar em letras maiúsculas, como VERMELHO, AMARELO.
  
  o	Se o nome contiver várias palavras, ele deverá ser separado por um sublinhado (_), como MAX_PRIORITY.
  
  o	Pode conter dígitos, mas não como a primeira letra.
  
**CamelCase em convenções de nomenclatura java**

Java segue a sintaxe camelCase para nomear a classe, interface, método e variável.
Se o nome for combinado com duas palavras, a segunda palavra começará com letras maiúsculas sempre como actionPerformed(), firstName, ActionEvent, ActionListener, etc.

### Variáveis

Em Java as variáveis são:

**Variável de instância**

Variável cujo valor é específico ao objeto e não à classe. Uma variável de instância em geral possui uma valor diferente em cada objeto representante da classe.

**Variável de classe**

Uma variável cujo valor é comum a todos os objetos representantes da classe. Mudar o valor de uma variável de classe em um objeto automaticamente muda o valor para todos os objetos instâncias da mesma classe. Um exemplo óbvio de uma variável de classe seria o número de instâncias desta classe que já foram criadas.

Uma variável é considerada como de instância por "default". Para declarar uma variável de classe, acrescenta-se a palavra-chave static.

**Variáveis globais** 

São declaradas fora de qualquer método (usualmente no cabeçalho da classe) e são acessíveis por qualquer método da classe

**Variáveis locais**

São declaradas dentro de um determinado método, ou até dentro de um bloco.

**Variáveis constantes**

Refere-se a variáveis cujo valor não pode mudar durante a execução do programa. Tais variáveis são caracterizadas pela palavra-chave final, e por convenção recebem usualmente nomes escritos inteiramente em maiúsculas.

 **Tipos de variáveis**

O Java é uma linguagem fortemente tipada, ou seja, é obrigatório que toda variável tenha um tipo definido na sua declaração.

Os tipos de dados/variáveis primitivas no Java são: byte, short, char, int, long, float, double e boolean.

### Vinculação

Em Java, a vinculação é a conexão entre uma chamada de função ao corpo do método. Existem dois tipos de vinculação: vinculação estática e dinâmica. Quando a ligação acontece durante em tempo de compilação, chama-se estático. Quando a ligação acontece durante run-time, chama-se dinâmico.

**Vinculação estática**

Geralmente, os métodos que são estáticos, privados e finais são vinculativos estáticos. Isso ocorre porque a substituição de método não é possível para esses métodos. Portanto, o compilador sabe qual método de classe chamar durante o próprio tempo de compilação.

**Vinculação dinâmica**

Ocorre principalmente na substituição de métodos. Na substituição de métodos, a superclasse e as subclasses têm o mesmo nome de método. Com base no tipo de objeto, que é determinado em tempo de execução, ele chama o método de classe correspondente durante o processo de vinculação.

 **Diferença entre vinculação estática e dinâmica**
 Vinculação estática | Vinculação Dinâmica
 ------------------- | -------------------
Também chamado de vinculação inicial ou vinculação em tempo de compilação	| Também chamado de late binding ou runtime binding
A sobrecarga de método é uma ligação estática | Substituição de método é vinculação dinâmica
Usa tipo de classe para resolver a ligação | Usa o tipo de objeto para resolver a ligação
Execução mais rápida | Execução lenta

## Escopo, tempo de vida e ambientes de referência

 **Variáveis locais** 
 
 Escopo: No bloco onde foi declarada
 
 Tempo de vida: Até o fim do bloco

 **Variáveis de instância** 
 
 Escopo: Por toda classe, exceto nos métodos estáticos
 
 Tempo de vida: Até que o lixo do objeto seja coletado
 
 **Variáveis de classe** 
 
 Escopo: Por toda classe
 
 Tempo de vida: Até o final do programa
 
 
## Capacidades da Linguagem 

### Metaprogramação

Metaprogramação consiste em escrever programas que manipulam outros programas ou a si mesmos com base em metadados. A API Reflection é a mais famosa nesse contexto, ela disponibiliza recursos para reflexão sobre classes e objetos que estão sendo usados na JVM, permiti inspecionar e manipular classes, interfaces, atributos, métodos e outros recursos em tempo de execução. 

###  Gerenciamento de Ciclo de Vida

 Antes de um objeto poder ser criado a partir de uma classe, a classe deve ser carregado. Para isso, o tempo de execução Java localiza a classe no disco (em um arquivo .class) e lê-lo na memória. Então Java procura por quaisquer inicializadores estáticos que inicializar campos estáticos - campos que não pertencem a qualquer instância específica da classe, mas sim pertencem a própria classe e são compartilhados por todos os objetos criados a partir da classe.
 
 Um objeto é criado a partir de uma classe quando você usa a nova palavra-chave. Para inicializar a classe, Java aloca memória para o objeto e define uma referência para o objeto de modo que o tempo de execução Java pode acompanhar isso. Então, Java chama o construtor da classe, que é como um método, mas é chamado apenas uma vez, quando o objeto é criado. O construtor é responsável por fazer qualquer processamento necessário para inicializar o objeto, como inicialização de variáveis, abrir arquivos ou bancos de dados, e assim por diante.
 
 O objeto vive sua vida, proporcionando acesso a seus métodos públicos e campos para quem quer e precisa deles.
 
 Quando é hora para o objeto a morrer, o objeto é removido da memória e Java deixa cair a referência interna para isso. Você não tem que destruir objetos si mesmo. Uma parte especial do tempo de execução Java chamado o coletor de lixo cuida de destruir todos os objetos quando eles não estão mais em uso.
 
 
###  Segurança 
 Por causa de toda estrutura como gerenciamento de memória  e usar uma máquina virtual (JVM) é um linguagem segura. Um programa sempre é verificado antes de ser executado. Essa verificação também é realizada nos navegadores e visa impedir que os applets possam provocar quaisquer danos ao computador do usuário. Ademais, como o Java não permite acesso direto à memória, impede seu uso para desenvolvimento de vírus.
 
Java fornece garantias e ferramentas de segurança, como :

Nenhuma exploração de buffer overflow

Verificação de código de bytes

Permissões de segurança para diferentes bases de código

APIs relacionadas à segurança

###  Performance

Por ser uma linguagem interpretada Java é um pouco lento quando comparada a linguagens compiladas, mas é mais rápida que outras linguagens interpretadas.

###  Escalabilidade

Escalabilidade consiste em um aumento de uso do software objetivando idealmente a menor perca de qualidade possivel, em Java a plataforma Java EE é a responsavvel por isso.
A plataforma Java Enterprise Edition (Java EE) é formada por um conjunto de especificações e tecnologias que vislumbram a redução da complexidade, custo e tempo de desenvolvimento, além de agregar maior valor a qualidade dos sistemas desenvolvidos sobe ela e por consequência a manutenibilidade. O Java EE teve seu espaço cada vez mais ampliado por fornecer como diferencial a permissão e suporte a rápida construção de aplicações seguras, com alta disponibilidade e escalável com baixo custo de manutenção. Seu escopo é largamente abrangente englobando aspectos transacionais, de persistência de dados, acesso remoto, balanceamento de cargas, cache de objetos, controle de threads, serviços web (web services – ws), páginas web, gerenciamento de conexões em diversos protocolos como por exemplo o Hypertext Transfer Protocol (HTTP), mensageira, dentre outros.


###  Confiabilidade

O Java  garante a confiabilidade dos programas produzidos. O processo de compilação elimina uma gama enorme de possíveis problemas e uma checagem dinâmica (realizada em tempo de execução) contorna muitas situações que poderiam gerar erros.

A confiabilidade dos programas escritos com o Java também é incrementada com um mecanismo eficiente para contornar situações inesperadas que podem ocorrer em tempo de execução. Essas condições excepcionais, chamas exceções, podem ser devidamente tratadas para evitar que o programa aborte, mesmo frente a situações de erro.

###  Concorrência e Threading 

Em Java, as threads são, o único mecanismo de concorrência suportado. É possivel entender esse recurso como trechos de código que operam independentemente da sequência de execução principal. Como diferencial, enquanto os processos de software não dividem um mesmo espaço de memória, as threads, sim, e isso lhes permite compartilhar dados e informações dentro do contexto do software.

Cada objeto de thread possui um identificador único e inalterável, um nome, uma prioridade, um estado, um gerenciador de exceções, um espaço para armazenamento local e uma série de estruturas utilizadas pela JVM e pelo sistema operacional, salvando seu contexto enquanto ela permanece pausada pelo escalonador.

Na JVM, as threads são escalonadas de forma preemptiva seguindo a metodologia “round-robin”. Isso quer dizer que o escalonador pode pausá-las e dar espaço e tempo para outra thread ser executada. O tempo que cada thread recebe para processar se dá conforme a prioridade que ela possui, ou seja, threads com prioridade mais alta ganham mais tempo para processar e são escalonadas com mais frequência do que as outras.

## Produtividade do Desenvolvedor

  ### Frameworks e Contâiners
  
  Frameworks Java são grupos de códigos previamente escritos e reutilizáveis, usados como templates pelos desenvolvedores na criação de aplicações. Esses frameworks elimina o trabalho manual excessivo ao programar uma aplicação uma vez que os desenvolvedores só precisam incluir código personalizado se for necessário.

Os frameworks Java podem incluir funções e classes predefinidas (como categorias de objetos), que são usadas para processar, inserir e gerenciar dispositivos de hardware, além de interagir com o software do sistema.

Alguns frameworks open source muito usados:

Quarkus: framework Java de stack completo, compatível com infraestruturas nativas em nuvem e baseadas em microsserviços

Grails: escrito na linguagem de programação Groovy, oferece frameworks de aplicação web com recursos de exibição para plugins CSS e HTML

Hibernate: framework de mapeamento objeto-relacional (ORM) usado no gerenciamento de bancos de dados relacionais. Pode executar consultas SQL com a ajuda das APIs da Java Database Connectivity (JDBC)

Google Web Toolkit (GWT): conecta as equipes de desenvolvimento de front-end às de back-end

Outros frameworks Java muito usados:

Vaadin: voltado às interfaces de usuário

Play: compatível com a linguagem de programação Scala, simplifica o desenvolvimento de aplicações web

Apache Struts: voltado a aplicações empresariais e compatíveis com técnicas assíncronas de JavaScript e XML (AJAX). É uma ótima maneira de fazer alterações em web pages sem precisar atualizar tudo

JavaServer Faces (JSF) do Oracle: oferece frameworks de front-end aos desenvolvedores de back-end

  ### Ferramentas Disponíveis
  
  Ant: O Ant é o padrão oficial para compilar projetos Java. Assim como o Make, ele trabalha com targets, dependências e comandos, porém a sintaxe é completamente diferente do Make.
  
  Make: O Make é a ferramenta de linha de comando original para o processo de build. Compila executáveis baseando-se em regras, dependências e comandos.
  
  CruiseControl: O CruiseControl é uma das ferramentas de integração contínua mais utilizadas pelas organizações. A ferramenta inclui dezenas de plugins para uma grande variedade de funcionalidades como controle de código-fonte, tecnologias de build, notificações incluindo e-mail e mensagens instantâneas, entre outras funcionalidades.
  
  Jenkins: O Jenkins é uma ferramenta de integração contínua open source que realiza rapidamente tarefas que são demoradas como compilação do projeto, execução dos testes automatizados e alerta aos desenvolvedores a cada mudança de código no repositório ou em caso de erros ou falhas nos testes automatizados.
  
  ## Sintaxe, Semântica e Operações Predefinidas
  
  #### Legibilidade
  
  Um dos critérios mais importantes de linguagens de programação é a legibilidade, que é facilidade com a qual os programas podem ser lidos e entendidos. Java é considerado por ter uma boa legibilidade, mas alguns reclamam do uso de ponto e vírgula e dos blocos.
  
  #### Redigibilidade
  
  Redigibilidade é uma característica das linguagens de programação relacionada à possibilidade de se escrever programas de modo natural ao problema. Muitos reclamam do Java possuir nomes extensos, mas existem alternativas para isso como por exemplo uma boa configuração de IDE com atalhos.
  
 ## Estruturas de controle

Todas as expressões condicionais usadas nas estruturas de controle são expressões booleanas. O resultado das expressões deve ser sempre true ou false. Não há conversões automáticas envolvendo booleanos em Java (evita erros de programação comuns em C/C++). Como por exemplo:

Esse codigo é aceito em C, já em Java não compila.
```
int x= 10;
if(x=5){
 ...
}
```

Codigo correto:
```
int x= 10;
if(x==5){
 ...
}
```

As estruturas de controle se dividem em:

**Estruturas de seleção**

 if, if-else, switch

**Estruturas de repetição**

 for, while, do-while
 
 **Desvios (somente em estruturas de repetição)**
 
 continue, break, rótulos
 
Java não possui um comando goto, porém “goto” é uma
palavra reservada.

**Controle Condicional: Seleção simples e dupla**

![image](https://user-images.githubusercontent.com/58619307/139143309-5ffca8c8-7a5d-43ca-a5ac-c29720a79527.png)

Os operadores relacionais para as expressoes booleanas são:

 equal to ==

 not equal to >=

 less than <

 greater than >

 less than or equal to <=

 greater than or equal to >=
 
 Operadores Lógicos:
 
 Operadores && (and), || (or) e ! (not)
 
 ## If
 
Conhecida como declaração condicional, as instruções são executadas se a condição for verdadeira. Chaves não são necessárias se apenas uma afirmação estiver relacionada à condição.


```
if(nota>=9.0){
  System.out.println("A");
}
else if(nota>=8.0){
  System.out.println("B");
}
else
  System.out.println("C");
```
 Neste exemplo é possivel observar a utilização do else if e else, dessa forma, se a expressão booleana 1 for verdadeira, o bloco de código 1 será executado. Caso seja falsa, o bloco de código 1 será ignorado e será testada a expressão booleana 2. Se ela for verdadeira, o bloco de código 2 será executado. Caso contrário, o programa vai ignorar esse bloco de código e executar o bloco 3, declarado dentro do else.

Outra opção é o operador condicional "?",possui a mesma semântica da estrutura if-else, é o unico operador ternário da linguagem Java,o primeiro operando é uma expressão booleana retorna o segundo operando se a expressão condicional for true ou o terceiro operando se for false
```
System.out.println( (media >= 7) ? “Aprovado” : “Reprovado” );
int x = (y != 0) ? 50 : 500;
String titulo = (sex == 'f') ? "Sra." : "Sr.“ ;
```

**Seleção múltipla: switch**

Avalia uma expressão de
números inteiros e tenta
selecionar um rótulo (case):

Caso haja um case correspondente, transfere o controle para
a primeira instrução após o
rótulo

Caso contrário, o controle será
transferido para a primeira
instrução após o rótulo
default

break provoca a saída do
comando switch

![image](https://user-images.githubusercontent.com/58619307/139147940-a297415e-4f69-4706-98b0-328b049dacf8.png)

```
switch(expr1) {
  case expr2:
    instruções;
    break;
  case expr3:
    instruções;
    break;
  default:
    instruções;
}
```

Na instrução switch (expr1),
expr1 deve ser compatível com
atribuições do tipo int, sendo
permitidos os tipos de dados
short, int, byte ou char, pois
pode ser feita a coerção (cast)
para o tipo int, o que não é
possível com os tipos long ou de
ponto flutuante.

```
switch(letra) {
  case 'A' : System.out.println("A");
        break;
  case 'B' : System.out.println("B");
        break;
  default : System.out.println("?");
}
```

**Estrutura de repetição: while**

Especifica uma ação que será repetida enquanto
uma condição for verdadeira.

```
while (expressão booleana){
  instruções;
}
```

```
int x = 0;
while (x < 10) {
  System.out.println ("item " + x);
  x++;
}
```

**Estrutura de repetição: do-while**

![image](https://user-images.githubusercontent.com/58619307/139148705-9d640eb6-af54-4a54-bc1d-1fac138336de.png)


O loop será executado pelo menos uma vez, pois a
condição só é testada no final

```
do
{
  instruções;
} while (expressão booleana);
```

```
int x = 0;
do {
  System.out.println ("item " + x);
  x++;
} while (x < 10);
```

**Estrutura de repetição: for**

![image](https://user-images.githubusercontent.com/58619307/139148741-4bde8001-2bf6-49e1-9ef4-953c8285bb5a.png)


Repete um bloco de comandos um número prédeterminado de vezes. Normalmente está associada
a algum contador.

```
for(inicialização ; expressão booleana ; passo de repetição) {
  instruções
}
```

```
for ( int x = 0; x < 10; x++ ) {
  System.out.println ("item " + x);
}
```

**Comandos de desvio: break e continue**

break: interrompe a execução do bloco de repetição. Continua com a próxima instrução após o bloco.

continue: interrompe a iteração atual. Ignora as instruções restantes no bloco, testa a condição e reinicia com a próxima iteração.

```
public static void main( String args[] ) {
  int count;
  for ( count = 1; count <= 10; count++ ) {
    if ( count == 5 )
      break;
    System.out.print(count + “ “);
   } // fim for
  System.out.println(“\nValor de count: ” + count);
} // fim main
```
Saida: 

1 2 3 4

Valor de count: 5

```
public static void main( String args[] ) {
  final int SKIP = 5; // constante
  for (int count = 1; count <= 10; count++ ) {
    if ( count == SKIP )
      continue;
    System.out.print(count + " ");
  } // fim for
  System.out.println("\nNumero " + SKIP + " nao foi impresso");
} // fim main
```
Saida:

1 2 3 4 6 7 8 9 10

Numero 5 nao foi impresso

**Usando rótulos**

break e continue sempre atuam sobre o bloco de repetição
onde são chamados.

Em blocos de repetição contidos em outros blocos, pode-se usar
rótulos para fazer break e continue atuarem em blocos externos.

Os rótulos só podem ser usados antes de do, while e for

 As chamadas só podem ocorrer dentro de blocos de repetição
 
 ## Ecossistema
 
  ### Maturidade
  
  Por ser uma linguagem antiga e por causa da popularidade já foi muito testada e aperfeiçoada.
  
  ### Comunidade
  
  Java comnta com uma comunidade assídua sendo uma das linguagens de programação mais utilizadas.
  
  ### Governança
  
  Oracle Corporation
  
