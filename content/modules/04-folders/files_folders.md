# Arquivos e Pastas

Vamos entender como funcionam as estruturas de arquivos e pastas no Linux.

## Listar arquivos e pastas

Para listar os arquivos e pasta, podemos utilizar os comandos `ls` e `dir`.


!!! exercise text short
    Utilize os comandos `ls` e `dir`. O que acontece?

    <div class="termy">

    ```console
    $ ls
    $ dir
    ```

    </div>
    <br>

    Sua resposta abaixo:

    !!! answer
        Nada é listado, uma vez que ainda não criamos nenhum arquivo!

## Redirecionar saída: Criar arquivo de texto

Quando utilizamos o comando `echo` as mensagens são direcionadas para a **saída padrão** (tela, terminal, console). Podemos utilizar o sinal de maior "`>`" para que as informações sejam escritas em um arquivo ao invés de exibidas na tela. Tente fazer:

<div class="termy">

    ```console
    $ echo "Este é meu primeiro a arquivo!"
    ```

</div>
<br>

Por enquanto, com o comando acima a informação foi exibida na tela. Não é bem o que queremos!

Agora faça:

<div class="termy">

    ```console
    $ echo "Este é meu primeiro a arquivo!" > mensagem.txt
    ```

</div>
<br>

Perceba que a informação não é exibida. Vamos tentar listar os arquivos:

<div class="termy">

    ```console
    $ ls
    mensagem.txt
    ```

</div>
<br>

!!! tip
    Teste tanto `ls` quanto `dir`.

Para conferir o que há dentro deste arquivo, fazemos o uso do comando `cat`:

<div class="termy">

    ```console
    $ cat mensagem.txt
    Este é meu primeiro a arquivo!
    ```

</div>
<br>

!!! tip
    Caso crie um arquivo por enganho, você pode utilizar o comando `rm` para removê-lo.

    Vamos supor que o arquivo `cartao.txt` foi criado por engano:

    <div class="termy">

    ```console
    $ echo "123456" > cartao.txt
    $ cat cartao.txt
    ```

    </div>
    <br>

    Ele pode ser removido com:

    <div class="termy">

    ```console
    $ rm cartao.txt
    $ ls
    ```

    </div>
    <br>

    !!! danger "Atenção"
        Perceba que o arquivo `cartao.txt` não existe mais (conforme esperado)!

!!! exercise
    Tente executar novamente o `echo`, com outra mensagem, salvando no arquivo `info.txt`. Por exemplo:
    
    <div class="termy">

    ```console
    $ echo "Meu nome é Maciel, criado em 01-05-2024" > info.txt
    ```

    </div>
    <br>

    !!! tip
        Ao invés de copiar os comandos deste site, leia e digite-os no terminal!

!!! exercise
    Liste os arquivos. Então, exiba o conteúdo do novo arquivo `info.txt`.

    !!! answer
        <div class="termy">

        ```console
        $ ls
        info.txt  mensagem.txt
        $ cat info.txt
        Meu nome é Maciel, criado em 01-05-2024
        ```

        </div>
        <br>


!!! exercise text long
    Agora, execute novamente o comando para salvar uma mensagem em `info.txt`, mas com uma mensagem diferente. O que acontece?

    !!! tip
        Para entender, repita várias vezes os comandos de salvar mensagem, listas arquivos e exibir o conteúdo dos arquivos.

    !!! answer
        O arquivo é **sobrescrito**, a mensagem anterior é perdida e apenas a última mensagem é salva!


!!! exercise text long
    Execute múltiplas vezes o comando para salvar mensagens em `hello.txt` (com uma mensagem diferente a cada execução), mas utilizando `>>` ao invés de `>`:

    <div class="termy">

    ```console
    $ echo "teste 1" >> hello.txt
    $ echo "bom dia" >> hello.txt
    $ echo "ola mundo!" >> hello.txt
    ```

    </div>
    <br>
    
    O que acontece?

    !!! tip
        Para entender, repita várias vezes os comandos de salvar mensagem, listas arquivos e exibir o conteúdo dos arquivos.

    !!! tip
        Ao invés de copiar os comandos deste site, leia e digite-os no terminal!

    !!! answer
        As novas mensagens são  **acrescentadas** no final do arquivo, todas as mensagens são salvas!


        <div class="termy">

        ```console
        $ echo "teste 1" >> hello.txt
        $ echo "bom dia" >> hello.txt
        $ echo "ola mundo!" >> hello.txt
        $ ls
        hello.txt  info.txt  mensagem.txt
        $ cat hello.txt 
        teste 1
        bom dia
        ola mundo!
        ```

        </div>
        <br>

!!! exercise
    Apenas para relembrar o comando, limpe o terminal!

    !!! answer
        <div class="termy">

        ```console
        $ clear
        ```

        </div>
        <br>


## Estrutura de arquivos e pastas

No Linux, um **arquivo** é uma unidade básica de armazenamento de dados que pode conter informações de texto, código-fonte, imagens, áudio, vídeo ou qualquer outro tipo de dado. Ele é identificado por um nome único e pode ser acessado, modificado ou executado por meio de comandos ou aplicativos.

!!! tip
    Os arquivos no Linux podem ter extensões que indicam seu tipo, embora a extensão não seja estritamente necessária para determinar o conteúdo do arquivo.

    Exemplos de alguns nomes de arquivos:

    - `mensagem.txt`: o `.txt` indica que o arquivo provavelmente contém **texto**.
    - `exemplo.py`: o `.py` indica que o arquivo provavelmente contém **código-fonte** de programação em **Python**.
    - `paisagem.jpg`: o `.jpg` indica que o arquivo provavelmente é uma **imagem**.
    - `icone.png`: o `.png` indica que o arquivo provavelmente é uma **imagem**.
    - `fallout.mp4`: o `.mp4` indica que o arquivo provavelmente é um **vídeo**.
    - `index.html`: o `.html` indica que o arquivo provavelmente é **página Web**.

Já as **pastas**, também conhecidas como **diretórios**, são estruturas de armazenamento usadas para organizar e agrupar arquivos em uma hierarquia de diretórios. Elas permitem que os usuários criem uma estrutura lógica e ordenada para armazenar e acessar seus arquivos de forma eficiente.

!!! info
    As pastas podem conter tanto arquivos quanto outras pastas, formando uma árvore de diretórios que começa no **diretório raiz** (`/`) e se expande para diretórios filhos e subdiretórios.
    
    Essa estrutura hierárquica facilita a organização, localização e gerenciamento dos arquivos no sistema Linux.

### Diretório atual

Para listar o diretório atual do terminal, podemos utilizar o comando `pwd`.

O comando `pwd` no Linux é uma abreviação de *"print working directory"*. Ele exibe o caminho completo do diretório atual em que o usuário está trabalhando. Ao executar o comando `pwd` no terminal, será mostrado o caminho absoluto do diretório atual, a partir do diretório raiz (`/`).


!!! info
    O `pwd` é útil para verificar em qual diretório você está localizado no momento!

!!! exercise text long
    Você conseguiria explicar o que significa **"diretório raiz"**?

    !!! answer
        No sistema de arquivos do Linux, o diretório raiz é o ponto de partida e o diretório mais alto na hierarquia de diretórios.
        
        Ele é representado pelo caractere `"/"` e contém todos os outros diretórios, subdiretórios e arquivos do sistema.

        !!! info
            O diretório raiz tem um papel semelhante ao `C:\` do Windows!

!!! exercise text long
    Utilize o comando `pwd`. O que é exibido? Explique.

    !!! answer
        `/home/boss`

        Ou seja, a partir do diretório raiz, temos uma pasta `home` e dentro dela temos uma pasta `boss`.

        !!! tip
            `/home/boss` é a pasta criada para armazenar os arquivos do usuário `boss`!

### Criar pastas

Já sabemos como criar e exibir o conteúdo de arquivos, mas ainda não criamos pastas.

Para criar uma pasta, utilizamos o comando `mkdir`.

Vamos criar uma pasta chamada `documentos`:

<div class="termy">

```console
$ mkdir documentos
```

</div>
<br>

!!! exercise
    Liste os arquivos e pastas!

    !!! answer
        <div class="termy">

        ```console
        $ ls
        documentos  hello.txt  info.txt  mensagem.txt
        ```

        </div>
        <br>

        !!! info
            Dependendo de qual terminal está utilizando, a pasta `documentos` pode ser exibida com cor diferente!

!!! tip
    Você pode utilizar o comando `rm -r nome_pasta` para **remover** uma pasta:
    <div class="termy">

    ```console
    $ mkdir uma_pasta_qualquer
    $ rm -rf uma_pasta_qualquer
    ```

    </div>
    <br>

    Para arquivos, você pode remover sem utilizar o `-r` no comando.

!!! tip
    Você pode utilizar o comando `mv nome_antigo novo_nome` para **renomear** arquivos e pastas:
    <div class="termy">

    ```console
    $ mkdir uma_pasta_qualquer
    $ mv uma_pasta_qualquer minha_pasta_favorita
    $ ls
    ```

    </div>
    <br>

    !!! info
        O comando `mv` também pode ser utilizado para **mover** arquivos e pastas.

Vamos listar de forma diferente, utilizando o comando `ls -l`:

<div class="termy">

```console
$ ls -l
total 16
drwxrwxr-x 2 boss boss 4096 May  1 16:12 documentos
-rw-rw-r-- 1 boss boss   27 May  1 15:38 hello.txt
-rw-rw-r-- 1 boss boss   41 May  1 15:27 info.txt
-rw-rw-r-- 1 boss boss   32 May  1 15:21 mensagem.txt
```

</div>
<br>

Perceba que a linha da pasta documentos inicia com `"d"`. Isto indica que ela é um diretório.

Note as duas colunas contendo `boss boss`. As colunas `"boss boss"` se referem ao **proprietário** e ao **grupo** proprietário dos arquivos e diretórios listados.

### Acessar pastas

No terminal, podemos navegar entre pastas, pois os comandos são executados em relação a pasta atual, e pode ser de interesse do usuário executar comandos em outras pastas.

Para entrar na recém criada pasta `documentos`, fazemos uso do comando `cd`:

<div class="termy">

```console
$ cd documentos
```

</div>
<br>

O `cd` é uma abreviação de *"change directory"*. Ele permite que você navegue pela estrutura de diretórios do sistema e altere o diretório atual para um diretório específico.

Ao dar um `ls`, note que nada é retornado, pois a pasta acabou de ser criada e está vazia:

<div class="termy">

```console
$ ls
```

</div>
<br>

!!! exercise text short
    Com qual comando posso garantir que estou na pasta correta?

    !!! answer
        <div class="termy">

        ```console
        $ pwd
        /home/boss/documentos
        ```

        </div>
        <br>

Agora tente utilizar:

<div class="termy">

```console
$ cd ..
```

</div>
<br>

Com `cd ..` podemos subir um nível na hierarquia de diretórios. Ou seja, estando em `/home/boss/documentos`, ao fazer `cd ..` voltamos para o diretório `boss`.

!!! exercise text short
    O que acontece se realizarmos novamente `cd ..`?

    !!! answer
        Vamos para `/home`:

        <div class="termy">

        ```console
        $ pwd
        /home/boss
        $ cd ..
        $ pwd
        /home
        ```

        </div>
        <br>

Com o `cd`, também podemos passar mais de uma pasta, navegando mais de um nível em apenas um comando. Por exemplo:

!!! exercise text short
    Confira que está em `/home`:

    <div class="termy">

    ```console
    $ pwd
    /home
    ```

    </div>
    <br>

    Então, faça:

    <div class="termy">

    ```console
    $ cd boss/documentos
    $ pwd
    /home/boss/documentos
    ```

    </div>
    <br>

    Note que navegamos direto para pasta documentos!

Também podemos fazer a navegação passando o caminho completo, a partir da raiz:

<div class="termy">

    ```console
    $ pwd
    /home/boss/documentos
    $ cd /home
    $ pwd
    /home
    ```

</div>
<br>

Perceba que com `cd /home` fomos direto para esta pasta.

### Exercícios

#### Documentos

!!! exercise text short
    Volte para `/home/boss/documentos` utilizando `cd` com o caminho completo.

    !!! answer

        <div class="termy">

        ```console
        $ pwd
        /home
        $ cd /home/boss/documentos
        $ pwd
        /home/boss/documentos
        ```

        </div>
        <br>

!!! exercise text long
    Em `/home/boss/documentos` (ou seja, dentro da pasta de documentos), crie um arquivo chamado `livros.txt`. Escreva nele nome de alguns livros que você gostaria de ler!

    !!! tip
        Se você quiser, pode listar aqui os comandos! Eles ficarão salvos e no futuro você pode acessar a página deste curso e ver suas respostas!

    !!! answer

        <div class="termy">

        ```console
        $ pwd
        /home/boss/documentos
        $ echo "O guia do mochileiro das galáxias" > livros.txt
        $ echo "Alice no país das maravilhas" >> livros.txt
        $ echo "Duna" >> livros.txt
        ```

        </div>
        <br>


!!! exercise text short
    Exiba o conteúdo do arquivo `livros.txt`!

    !!! answer
        <div class="termy">

        ```console
        $ pwd
        /home/boss/documentos
        $ ls
        livros.txt
        $ cat livros.txt
        O guia do mochileiro das galáxias
        Alice no país das maravilhas
        Duna
        ```

        </div>
        <br>

!!! exercise
    Garanta que o diretório atual continua sendo `/home/boss/documentos`. Crie um arquivo `compras.txt` e escreva nele alguns itens que estão em falta em sua casa e que gostaria de comprar!

#### Downloads

!!! exercise
    Limpe a tela!

!!! exercise
    Volte para `/home/boss`.

!!! exercise
    Dentro de `/home/boss`, crie uma pasta chamada `downloads`.

!!! exercise
    Acesse a pasta `downloads`, cujo caminho completo deve ser `/home/boss/downloads`.

Agora, vamos aprender como fazer download de arquivos. Para isto, podemos utilizar o comando `wget`.

!!! info
    O comando `wget` é uma ferramenta de linha de comando no Linux que permite baixar arquivos e conteúdos da Web!

Estando em `/home/boss/downloads`, execute o comando:

<div class="termy">

    ```console
    $ pwd
    /home/boss/downloads
    $ wget https://atd-insper.s3.us-east-2.amazonaws.com/aula04/alice_wonderland.txt
    ```

</div>
<br>


!!! tip
    Caso o `pwd` retorne algo diferente de `/home/boss/downloads`, ou seja, se você não estiver na pasta correta, execute o comando `cd /home/boss/downloads`:

    <div class="termy">

    ```console
    $ cd /home/boss/downloads
    $ pwd
    /home/boss/downloads
    $ wget https://atd-insper.s3.us-east-2.amazonaws.com/aula04/alice_wonderland.txt
    ```

    </div>
    <br>

Liste os arquivos existentes, você verá que um novo arquivo foi criado!

<div class="termy">

    ```console
    $ ls
    alice_wonderland.txt
    ```

</div>
<br>

!!! exercise
    Exiba o conteúdo de `alice_wonderland.txt`.

!!! exercise
    Estando em `/home/boss/downloads`, utilize `wget` para fazer o download da calculadora, que está na URL *https://universo-linux.s3.us-east-2.amazonaws.com/calculadora*

    !!! info
        Você precisa fazer o download na **máquina virtual**. Não é para clicar na URL, o que faz um download na sua máquina.
        
        Copie a URL e cole no terminal após o comando `wget`.

Vamos tentar executar a **calculadora**. Para isto, basta executar o comando `./calculadora` no terminal:

!!! tip
    Perceba o uso de `./` antes do nome `calculadora`

<div class="termy">

    ```console
    $ ./calculadora
    -bash: ./calculadora: Permission denied
    ```

</div>
<br>

Isto não irá funcionar! Será necessário **permitir** que a calculadora possa **ser executada**. Podemos fazer isto com o comando `chmod`:

<div class="termy">

    ```console
    $ pwd
    /home/boss/downloads
    $ chmod +x calculadora
    ```

</div>
<br>

!!! tip
    Utilizamos `chmod +x` para dar permissão de execução

    Utilizamos `chmod -x` para remover permissão de execução

Tente novamente executar a calculadora:

<div class="termy">

    ```console
    $ ./calculadora
    ```

</div>
<br>

Agora somos informado da necessidade de passar dois números após o comando! Vamos fazer:

<div class="termy">

    ```console
    $ ./calculadora 10 20
    ```

</div>
<br>

Confira o resultado!

!!! exercise
    Teste a calculadora com outros números!