# Árvore de diretórios

Vamos verificar como exibir, no terminal, quais pastas e arquivos estão dentro de quais pastas, construindo uma árvore.

O comando `tree` pode nos ajudar nesta tarefa. Entretanto, ao tentar executá-lo:

<div class="termy">

    ```console
    $ tree
    Command 'tree' not found...
    ```

</div>
<br>

## Update do sistema

Será necessário instalar o `tree`. Mas antes, precisamos descobrir os pacotes disponíveis para instalação.

O comando `sudo apt update` é usado no sistema operacional **Ubuntu** (e outras distribuições baseadas no Debian) para atualizar a lista de pacotes disponíveis nos repositórios configurados no sistema. Ele verifica se há atualizações disponíveis para os pacotes instalados e sincroniza as informações locais com os servidores de repositórios, garantindo que você tenha acesso às versões mais recentes dos pacotes.

!!! info
    `sudo` no Linux permite que um usuário execute um comando com privilégios de **superusuário** (`root`), fornecendo a autorização necessária para realizar **tarefas administrativas** e acessar arquivos ou comandos restritos ao usuário `root`.

    Ou seja, nosso usuário `boss` vai usar `sudo` quando precisar, por exemplo, instalar novos programas no Linux!

Faça `sudo apt update`:

<div class="termy">

    ```console
    $ sudo apt update
    ```

</div>
<br>

## Upgrade do sistema

Vamos fazer também o `upgrade`, garantindo que todos os pacotes atualmente instalados sejam atualizados:

!!! info
    Execute o comando abaixo e aperte **ENTER** (ou digite **Y e ENTER**) ao ser questionado se deseja continuar.

<div class="termy">

    ```console
    $ sudo apt upgrade
    ```

</div>
<br>

## Instalação

Agora podemos fazer a instalação do `tree`:

!!! info
    Pode confirmar com **ENTER** ou **Y + ENTER** caso receba pedido de confirmação da instalação!

<div class="termy">

    ```console
    $ sudo apt install tree
    ```

</div>
<br>

## Uso do `tree`

Volte para pasta de usuário em `/home/boss`. Você pode fazer isto de três maneiras:


=== "Alternativa 1"

    Como já fizemos.

    <div class="termy">

    ```console
    $ cd /home/boss
    ```

    </div>

=== "Alternativa 2"
    Utilizando "`~`". O "`~`" representa a pasta do usuário!

    Então, ao fazer:

    <div class="termy">

    ```console
    $ cd ~
    ```

    </div>

    conseguimos navegar para `/home/boss`.

    !!! tip
        Note que, ao fazer **SSH**, o terminal contém `boss@ip-172-31-9-133:~$` onde:

        - `boss` representa o usuário.
        - `@ip-172-31-9-133` representa "at host", então `ip-172-31-9-133` é o nome da máquina.
        - `~` representa a pasta atual (`/home/boss`). Ou seja, `~` representa a pasta do usuário atualmente logado / conectado.

=== "Alternativa 3"
    Utilizando apenas `cd`. O comando `cd`, sem nenhum argumento, vai para a pasta do usuário!

    Então, ao fazer:

    <div class="termy">

    ```console
    $ cd
    ```

    </div>

    conseguimos navegar para `/home/boss`.

Então, faça a exibição da árvore de diretórios:

<div class="termy">

    ```console
    $ pwd
    /home/boss
    $ tree
    ```

</div>
<br>

Você deve ver algo como:

```console
.
├── documentos
│   ├── compras.txt
│   └── livros.txt
├── downloads
│   ├── alice_wonderland.txt
│   └── calculadora
├── hello.txt
├── info.txt
└── mensagem.txt

2 directories, 7 files
```

Ou seja, dentro de `/home/boss`, temos a pasta `documentos`. Dentro da pasta documentos, temos dois arquivos: `compras.txt` e `livros.txt`.

Observe que `documentos` e `downloads` estão no mesmo nível da árvore. Seguindo o caminho, vemos que ambas estão dentro da mesma pasta.

!!! exercise choice
    Os arquivos `hello.txt`, `info.txt` e `mensagem.txt` estão dentro da mesma pasta que `documentos` e `downloads`.

    - [X] Verdadeiro
    - [ ] Falso

    !!! answer "Answer"
        Sim! Tudo isto está em `/home/boss`.

!!! exercise choice
    O caminho completo para o arquivo `livros.txt` é `/home/boss/livros.txt`.

    - [ ] Verdadeiro
    - [X] Falso

    !!! answer "Answer"
        Não! Faltou a pasta `documentos`. O correto é `/home/boss/documentos/livros.txt`.



!!! exercise text short
    Qual o caminho completo para o arquivo `hello.txt`?

    !!! answer "Answer"
        `/home/boss/hello.txt`

!!! exercise text short
    Estando em `/home/boss/documentos`, como posso exibir o conteúdo de `info.txt`?

    !!! info
        Note que `info.txt` não está em `documentos`!

    !!! answer "Answer"
        Duas alternativas de resposta são:

        === "Alternativa 1"

            Utilizar caminho completo do arquivo:

            <div class="termy">

            ```console
            $ cd /home/boss/documentos
            $ pwd
            /home/boss/documentos
            $ cat /home/boss/info.txt
            ```

            </div>

        === "Alternativa 2"
            Utilizar caminho relativo, fazendo uso do `..` para acessar a pasta anterior.

            Então, ao fazer:

            <div class="termy">

            ```console
            $ cd /home/boss/documentos
            $ pwd
            /home/boss/documentos
            $ cat ../info.txt
            ```

            </div>