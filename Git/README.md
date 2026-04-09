# Guia de Sobrevivência: Git & GitHub

Este repositório contém um tutorial prático para configurar e utilizar o Git em sistemas Windows e Linux.

# O que é o Git?
O Git é o motor. Ele é um sistema de controle de versão que você instala no seu computador.

Sempre que você termina uma parte importante do seu código, você tira uma "foto" (chamada de commit) daquele momento. Se você fizer uma besteira no código no dia seguinte, o Git permite que você "viaje no tempo" e volte exatamente para como o projeto estava na foto anterior. Ele funciona offline e é responsável por organizar o histórico de tudo o que foi feito.

# O que é o GitHub?
Ele é uma plataforma online que hospeda os seus projetos que usam o Git. Além disso, é uma espécie de Rede Social dos Nerds. A plataforma conta com:

* Follow & Star: Você pode seguir desenvolvedores que admira e dar uma "estrela" (como um like) em projetos que achou interessantes ou úteis.

* Pull Requests: É como se você visse o projeto de alguém, fizesse uma melhoria e dissesse: "Ei, gostei do seu código, aqui está uma sugestão de melhoria, aceita?".

* Issues: Um espaço para discussão onde usuários relatam erros (bugs) ou sugerem novas funções, funcionando quase como um fórum do projeto.

* Fork: Você pode "copiar" um projeto inteiro de outra pessoa para a sua conta com um clique, para modificá-lo como quiser sem alterar o original.

## Instalação

### Windows

1.  Baixe o instalador oficial em [git-scm.com](https://git-scm.com/install/windows).
2.  Execute o `.exe` e siga as instruções (o padrão recomendado é manter as opções selecionadas pelo instalador).
3.  Ao final, você terá o **Git Bash**, um terminal que simula o ambiente Linux, facilitando o uso dos comandos.

### Linux (Debian/Ubuntu)

Abra o terminal e execute:

```bash
sudo apt update
sudo apt install git
```

Para verificar se a instalação foi bem-sucedida em qualquer sistema, digite:

```bash
git --version
```

-----

## Configuração Inicial

Antes de começar a criar seus commits, você precisa se identificar. Isso é importante para que o GitHub saiba quem é o autor das alterações.

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@exemplo.com"
```

-----

## Fluxo de Trabalho

O ciclo de vida de um arquivo no Git passa por três estados principais: **Working Directory**, **Staging Area** e **Repository**.

### 1\. Iniciando ou Clonando

  * **Para começar um projeto do zero:**
    ```bash
    git init
    ```
  * **Para baixar um projeto existente do GitHub:**
    ```bash
    git clone https://github.com/usuario/repositorio.git
    ```

### 2\. Ciclo de Alterações

Sempre que editar, criar ou deletar arquivos, siga estes passos:

1.  **Verificar o status:** Veja o que foi alterado.
    ```bash
    git status
    ```
2.  **Adicionar ao "palco" (Staging):** Prepare os arquivos para o commit.
    ```bash
    git add nome-do-arquivo.txt  # Para um arquivo específico
    git add .                   # Para todos os arquivos alterados
    ```
3.  **Criar um ponto na história (Commit):** Salve as alterações com uma mensagem descritiva.
    ```bash
    git commit -m "Explique o que você fez aqui"
    ```

### 3\. Sincronizando com o GitHub

  * **Enviar para o servidor:**
    ```bash
    git push origin main
    ```
  * **Trazer atualizações do servidor:**
    ```bash
    git pull origin main
    ```

-----

## Dicas Úteis

  * **Log de atividades:** Veja o histórico de commits com `git log --oneline`.
  * **Ramificações (Branches):** Use branches para testar novas funcionalidades sem quebrar o código principal:
    ```bash
    git checkout -b nome-da-nova-branch
    ```
  * **.gitignore:** Crie um arquivo chamado `.gitignore` na raiz do projeto para listar arquivos ou pastas que o Git deve ignorar (como senhas, pastas de dependências como `node_modules` ou arquivos temporários).

-----

*Tutorial criado para fins educacionais. Sinta-se à vontade para contribuir\!*
