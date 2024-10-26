# Git 

<br>

**Git** é uma solução de Source Control Management (SCM), que nos permite versionar o código em desenvolvimento.


## Iniciando um repositório

<br>

Criando um diretório para o repositório

```shell
mkdir project
cd project
```

<br>

Dentro do diretório `project` executar o seguite comando para iniciar o repositório:
```shell
git init
```

<br>

Será criado um subdiretório `.git` contendo os seguintes subdiretórios:

- **braches**: Diretório não mais utilizado
- **config**: Contém as opções de configuração específicas do projeto
- **description**: Arquivo de descrição do repositório
- **HEAD**: Aponta para o branch que você fez check-out atualmente
- **hooks**: Diretório contém seus scripts de hooks do lado do cliente ou do servidor
- **index**: Arquivo onde o Git armazena as informações da sua área de staging.
- **info**: Mantém um arquivo de exclusão global para padrões ignorados que você não deseja rastrear em um arquivo .gitignore.
- **objects**: Armazena todo o conteúdo do seu banco de dados
- **refs**: Armazena ponteiros para objetos de commit de *objects* (ramificações, tags, controles remotos e mais),

<br>

## Configuração do repositório

<br>

Antes de começar a utilizar o repositório, o usuário tem que ser identificado com o *usuário* e *email*. Dessa forma, quando realizar o commit o autor poderá ser identificado.

```shell
git config --global user.name "Nome do Usuario"
git config --global user.email "email_usuario@exemplo.dev"
```
O comando `git config` tem a possibilidade de gravar a configuração de acordo com o parâmetro passado:  
- `--global`: Gravado no arquivo `~/.gitconfig`
- `--system`: Gravado no arquivo `/etc/gitconfig`
- `--local`: Gravado no arquivo `~/.git/config` do próprio repositório

<br>

### Visualiza as configurações aplicadas

<br>

```shell
git config --list
```
<br>

## O ciclo de vida do status dos arquivos no ambiente Git

<br>

![The lifecycle of the status of your files](lifecycle.png)

- **Tracked**: São arquivos que estavam no último snapshot, bem como quaisquer arquivos *staged*; eles podem ser *unmodified*, *modified* ou *staged*. Resumindo, arquivos *tracked* são arquivos que o Git conhece.
- **Untracked**: São quaisquer arquivos em seu diretório de trabalho que não estavam em seu último snapshot e não estão em sua área de *staging*.
- **Unmodified**: Arquivo já adicionado e commitado e dentro do ambiente do Git.
- **Modified**: Arquivo já presente no ambiente do Git e que possui uma modificação.
- **Staged**: Quando é adicionado um arquivo novo ou modificado ao ambiente do Git.

<br>

### Visualizando o status do Git

<br>

Comando para visualizar o status do Git

<br>

```shell
git status
```

<br>

## Realizando um *Commit*

<br>

Para este exemplo, vamos criar um arquivo dentro do diretório `project`, onde foi iniciado o repositório, anteriormente.

```shell
touch test.txt
``` 

<br>

Adiciona o arquivo `teste.txt` ao ambiente do git. 

```shell
git add test.txt
``` 

<br>

Faz o *commit* do arquivo e adiciona uma mensagem a este *commit*

```shell
git commit -m "Adicionando arquivo"
``` 

<br>



