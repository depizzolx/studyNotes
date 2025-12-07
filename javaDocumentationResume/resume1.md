### INTRODUCTION
## RESUME
Java é uma linguagem de programação de uso geral. É baseada em *classes* e é *orientada a objetos*.
Java tem relação com C e C++, mas é organizada de uma forma diferente: Omite alguns aspectos de C e C++, e implementa aspectos de outras linguagens de programação. É uma linguagem de Produção, ou seja, é focada em estabilidade e escalabilidade.

## TYPED, STATICALLY, COMPILER-ERRORS & RUN-TIME-ERRORS
Java é uma linguagem fortemente e estaticamente tipada (estática). Isso nos diz que existem dois problemas possíveis para o código que estamos escrevendo: O erro alertado antes do programa rodar, quando o compilador do código reconhecerá erros da tipagem desse código, como variáveis não-declaradas, atribuição de um valor incompatível ao tipo da variável, erros de sintaxe (como falta de parenteses e erros na estrutura do código). Resumindo: O compilador apontará erros de variáveis, funções, sintaxes que foram escritas/formatados de maneira que o código não pode ser convertido para bytecode. E erros que aparecerão quando o programa já estiver rodando, como por exemplo: O código tentar acessar uma base de dados inexistente, um arquivo corrompido, dididir um número por zero e coisas assim.
A fase de *compilação* que falamos acima, no primeiro erro, é a fase em que o Java converte o código escrito para um código bytecode, que é uma forma de código intermediária utilizado pela *JVM*. A segunda fase é composta pelo código já transformado em bytecode.

### GRAMMARS
## LEXICAL GRAMMAR & LEXICAL STRUCTURE
A Gramática Léxica é uma "parte" do compilador que lê os caracteres que escrevemos em Unicode (um código númerico atribuído pelo compilador as letras escritas) e forma "palavras" (tokens). Exemplo:

    int idade = 25;

O compilador lê 'i' 'n' 't', que foi transformado em Unicode, e reconhece o tipo da variável;
O compilador descarta os espaços em branco entre a declaração da variável, o nome atribuído e etc;
O compilador lê o nome atribuído a variável e reconhece como um *Identificador*;
O compilador lê o sinal de igual (=) e reconhece como um *Operador*;
O compilador lê o número e reconhece como um *Literal*;
O compilador lê o ';' e reconhece como um *Separador*;

Se distoarmos do padrão léxico-gramatical estabelecido em Java, como, por exemplo, adicionando um caractere especial (*, @, !) para definir um nome de variável, um erro será apontado no código pelo compilador.

## SYNTATIC GRAMMAR
Após a gramática anterior alertar dos erros apontados pelo compilador e você corrigi-los, o código é convertido em "tokens" e é lido através de uma Gramática Sintética, para verificar se essas palavras formam "frases" que fazem sentido. Ela é responsavel pela *sintaxe* do código. Usando o exemplo anterior, se tivéssemos escrito-o assim:

    int = 25;

Não haveria erro pela leitura da gramática lexical, mas a sintaxe do código estaria incorreta, pois não foi declarado um nome para essa variável.
