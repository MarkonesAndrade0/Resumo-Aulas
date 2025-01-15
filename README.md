<h1>
    <a href="https://www.dio.me/">
     <img align="center" width="40px" src="https://hermes.digitalinnovation.one/assets/diome/logo-minimized.png"></a>
    <span> DIO | Resumos Git e GitHub</span>
</h1>

Repositorio para armazenar resumos Git e Github do curso Versionamento de Código com Git e Github da [Inteligência Artificial Aplicada a Dados com Copilot](https://web.dio.me/track/coding-the-future-heineken-ia-para-analise-de-dados).

## 📒**Documentação**

<h1>
    <a href="https://git-scm.com/doc">
        <img align="center" width="80px" src="https://img.shields.io/badge/Git-000?style=for-the-badge&logo=git&logoColor=E94D5F"></a>
    <span> Documentaçao Git</span>
</h1>

<h1>
    <a href="https://docs.github.com/">
        <img align="center" width="80px" src="https://img.shields.io/badge/GitHub-000?style=for-the-badge&logo=github&logoColor=32A3DC"></a>
    <span> Documentação GitHub</span>
</h1>

## 🖥️ **Resumo das Aulas**

## 🔧 **Visão Geral do Curso e Ferramentas**

#### **O que é Versionamento de Código?**

- *`O versionamento de código é uma prática essencial no desenvolvimento de software que permite acompanhar as alterações feitas no código ao longo do tempo. Ele utiliza sistemas de controle de versão, como o Git, para registrar modificações, criar históricos detalhados, colaborar com outras pessoas de forma eficiente e reverter alterações, se necessário. Com o versionamento, é possível gerenciar diferentes versões de um projeto, trabalhar em equipe sem conflitos e garantir a integridade do código.`* 

#### **O que é Git?**

- *`O Git é uma ferramenta de controle de versão que permite registrar e gerenciar alterações em projetos de software. Ele facilita o trabalho em equipe, mantendo um histórico completo de mudanças, permitindo criar ramificações para novas funcionalidades e combinar alterações. É rápido, distribuído e amplamente usado com plataformas como GitHub e GitLab para colaboração.`*

#### **O que é GitHub?**

- *`O GitHub é uma plataforma online para hospedagem de repositórios Git. Ele permite que desenvolvedores colaborem em projetos, compartilhem código, rastreiem alterações e gerenciem versões. Além disso, oferece recursos como pull requests, issues e integração com ferramentas de desenvolvimento, sendo amplamente utilizado para projetos open source e privados.`*

## ⚙️ **Instalação, Configuração e Autenticação**

#### **Instalando o Git no Windows**

**`1° Baixar o instalador: Acesse o site oficial do`** [![Git](https://img.shields.io/badge/Git-black?style=flat)](https://git-scm.com/downloads) **`e baixe a versão para Windows.`**

**`2° Executar o instalador: Clique no arquivo baixado para iniciar a instalação.`**

**`3° Configurar a instalação:`**
- *`Escolha as opções padrão para a maioria dos casos.`*
- *`Selecione o editor padrão (como Vim ou outro de sua escolha).`*
- *`Configure como o Git será usado no terminal (recomenda-se "Git Bash").`*

**`4° Concluir a instalação: Finalize o processo e abra o Git Bash para começar a usar o Git.`**

#### **Configurando o Git**

- *`Abra o Git Bash e configure seu nome, e-mail e o nome padrão da branch:`*

     ```
    git config --global user.name "Seu Nome"
    git config --global user.email "seuemail@example.com"
    git config --global init.defaultBranch main
    ```
- *`Agora, toda vez que você inicializar um repositório com git init, a branch principal será chamada main em vez de master (o padrão antigo).`*

#### ✅ **Autenticando via Token**

**`1°Gerar o Token de Acesso:`**

- *`Acesse sua conta no GitHub e vá para Settings (Configurações).`* 

- *`Navegue até Developer Settings > Personal Access Tokens > Tokens (classic) > Generate new token.`*

- *`Preencha as informações:`*

- *`Nome do token.`*

- *`Validade (expiração).`*

- *`Selecione as permissões necessárias, como acesso a repositórios públicos e privados.`*

- *`Clique em Generate token e copie o token gerado (ele será exibido apenas uma vez).`*

**`2° Configurar o Token no Git:`**

- *`No terminal, ao executar um comando que requer autenticação, como git push ou git clone, o Git solicitará suas credenciais.`*

- *`No campo de usuário, insira seu nome de usuário do GitHub.`*

- *`No campo de senha, insira o token gerado.`*

**`3° Salvar o Token:`**

- *`Para evitar digitar o token em toda operação, configure o Git para armazenar as credenciais:`*

    ```
    git config --global credential.helper store
    ```
- *`Após isso, insira o token na próxima autenticação, e ele será salvo localmente.`*

#### ✅ **Autenticando via Chave SSH**

**`1° Gerar uma chave SSH`**
- *`Abra o terminal ou Git Bash.`*
- *`Execute o comando para gerar a chave:`*
    
    ```
    ssh-keygen -t ed25519 -C "seuemail@example.com"
    ```
- *`Quando solicitado: Pressione Enter para aceitar o local padrão (~/.ssh/id_ed25519).`*

- *`Digite uma senha para proteger a chave e pressione Enter.`*

**`2° Iniciar o agente SSH`**
- *`No terminal, inicie o agente SSH`*
    
    ```
    eval "$(ssh-agent -s)"
    ```
- *`Adicione sua chave ao agente:`*
    
    ```
    ssh-add ~/.ssh/id_ed25519
    ```
**`3° Adicionar a chave SSH ao GitHub`**

- *`Copie a chave pública para a área de transferência`*
    
    ```
    cat ~/.ssh/id_ed25519.pub
    ```
- *`Acesse o GitHub e vá para Settings (Configurações).`*

- *`Clique em SSH and GPG keys > New SSH key.`*

- *`Cole a chave pública copiada no campo "Key".`*

- *`Dê um nome à chave (ex.: "Meu PC") no campo "Title".`*

- *`Clique em Add SSH Key.`*

**`4° Testar a conexão com o GitHub`**

- *`No terminal, clone o repositório usando a URL SSH:`*

    ```
    git clone git@github.com:seu-usuario/seu-repositorio.git
    ```
- *`Digite sua senha se for solicitado ou confirme com o token SSH.`*

## **Primeiros Passos com** ![Static Badge](https://img.shields.io/badge/git-000?style=for-the-badge&logo=github&logoColor=E94D5F&logoSize=100) ![Static Badge](https://img.shields.io/badge/GIThub-000?style=for-the-badge&logo=github&logoColor=32A3DC&logoSize=100)

#### **Criando e Clonando Repositórios com Git e GitHub**
**`Trabalhar com repositórios no Git e GitHub envolve criar um espaço para versionamento de projetos e clonar repositórios para trabalhar localmente. Aqui está um guia detalhado:`**

**`1° Criando Repositórios`**

- *`Criando no GitHub`*

    - *`Acesse o [GitHub](https://github.com/login) e faça login.`*
    - *`Clique em "New" ou no botão de criar repositório.`*
    - *`Preencha as informações:`*
        - *`Nome do repositório: O identificador principal.`*
        - *`Descrição (opcional): Um resumo do projeto.`*
        - *`Visibilidade: Escolha entre:`*
        - *`Público: Qualquer pessoa pode ver.`*
        - *`Privado: Apenas pessoas autorizadas têm acesso.`*

    - *`Opções adicionais`*

        - *`README.md: Arquivo inicial com informações do projeto.`*
        - *`.gitignore: Define arquivos que o Git deve ignorar.`*
        - *`Licença: Define como o código pode ser usado.`*

    - *`Clique em "Create Repository".`*

- **`Criando Localmente`**

    - *`No terminal, crie um diretório:`*
            
        ```
        mkdir meu-projeto
        cd meu-projeto
        ```
    - *`Inicialize o repositório:`*
        
        ```
        git init
        ```
    - *`Crie arquivos e faça o primeiro commit:`*
       
        ```
        echo "# Meu Projeto" > README.md
        git add .
        git commit -m "Primeiro commit"
        ```
    - *`Conecte ao GitHub:`*
        
        ```
        git remote add origin <URL_DO_REPOSITÓRIO>
        git branch -M main
        git push -u origin main
        ```

**`2° Clonando Repositórios`**

- *`O que é Clonar?`*
    
    *`A clonagem copia um repositório remoto para sua máquina, criando uma versão local para edição e controle.`*

- *`Como Clonar?`*
    - *`No GitHub, vá ao repositório desejado.`*
    - *`Clique em "Code" e copie a URL (HTTPS, SSH).`*
    - *`No terminal, execute:`*
    
    ```
    git clone <URL_DO_REPOSITÓRIO>
    ```
    - *`A pasta do repositório será criada no diretório local.`*

**`3° Principais Comandos Utilizados`**

- *`Comandos de Criação`*
    - **`git init`**: *`Inicializa um repositório local.`*
    - **`git remote add origin <URL>`**: *`Conecta o repositório local ao GitHub.`*
    - **`git push -u origin main`**: *`Envia o repositório local para o GitHub.`*

- *`Comandos de Clonagem`*
    - **`git clone <URL>`**: *`Copia um repositório remoto para a máquina local.`*

- *`Outros Comandos Úteis`*
    - **`git status`**: *`Mostra o estado do repositório.`*
    - **`git pull`**: *`Atualiza o repositório local com alterações do remoto.`*
    - **`git log`**: *`Exibe o histórico de commits.`*

#### **Salvando Alterações no Repositório Local com Git e GitHub**

*`Salvar alterações no repositório local é uma etapa fundamental no uso do Git para versionamento. Aqui está um guia detalhado e especificado para garantir o correto salvamento e envio ao repositório remoto no GitHub.`*

**`1° Salvando Alterações Localmente`**

- *`Modificar os Arquivos`*
    - *`Realize alterações no código ou adicione novos arquivos no diretório do repositório local.`*

- *`Verificar o Estado do Repositório`*
    - *`Execute o comando:`*
    
    ```
    git status
    ```
    - **`Arquivos modificados`**: *`Listados em vermelho (não adicionados ao stage).`*
    - **`Novos arquivos`**: *`Exibidos como "Untracked files".`*

- *`Adicionar Arquivos ao Stage`*
    - *`Adicionar um arquivo específico:`*
    
    ```
    git add <nome_do_arquivo>
    ```
    - *`Adicionar todos os arquivos modificados:`*
    
    ```
    git add .
    ```
    - *`Estado após adicionar: Os arquivos aparecem em verde ao executar`* **`git status.`**

- *`Criar um Commit`*
    - *`Registre as alterações de forma permanente no repositório local:`*
    
    ```
    git commit -m "Descrição clara e objetiva das alterações realizadas"
    ```
    - *`Mensagem de commit ideal:`*
        -  *`Curta (menos de 50 caracteres).`*
        - *`Descreva o que foi feito, como "Corrigido bug na função X" ou   "Adicionado arquivo README".`*

**`2° Enviando Alterações para o Repositório Remoto (GitHub)`**

- *`Garantir Conexão com o Repositório Remoto`*
    - *`Verifique se o repositório local está conectado ao remoto:`*
    
    ```
    git remote -v
    ```
    - *`Se não estiver, conecte-o:`*
    
    ```
    git remote add origin <URL_DO_REPOSITÓRIO>
    ```

- *`Enviar os Commits`*
    - *`Suba as alterações para o GitHub usando:`*
    
    ```
    git push origin <branch>
    ```
    - *`Exemplo: Enviar para a branch principal`* (**`main`**)
    
    ```
    git push origin main
    ```

- *`Sincronizar Antes de Novas Alterações`*
    - *`Sempre sincronize sua branch local com o repositório remoto para evitar conflitos:`*
    
    ```
    git pull origin main
    ```

#### **Desfazendo Alterações no Repositório Local com Git e GitHub**

*`Desfazer alterações em um repositório local com Git e GitHub é uma tarefa comum e útil para corrigir erros ou retornar a um estado anterior do código. Aqui estão as principais abordagens para lidar com diferentes situações`*

- *`Desfazer alterações não confirmadas:`*
    - *`Arquivos modificados mas não adicionados ao staging (`* **`Git add`** *`não usado):`* 
       
        ```
        git restore <arquivo>
        ```
    - *`Para desfazer alterações em todos os arquivos:`*

        ```
        git restore .
        ```
    -  *`Excluir novos arquivos não ratreados: Se você criou novos arquivos que não foram adcionados ao Git:`*
        ```
        git clean -f
        ```

- *`Desfazer alterações antes do commit:`*
    - *`Se você usou o`* **`git add`**, *`mas ainda não realizou o commit, pode desfazer o staging:`*
       
        ```
        git restore --staged <arquivo>
        ```
    - *`Isso romeve o arquivo da área de staging, mas mantém as modificação no disco.`*

- *`Desfazer o último commit:`*
    - *`Manter as alterções no diretório de trabalho:`*
      
        ```
        git reset --soft HEAD~1
        ```
    - *`Isso reverte o commit, mas preserva as alterações para que você possa corrigir e fazer um novo commit.`*

    - *`Descartar completamente o commit e as alterações:`*
      
      ```
        git reset --hard HEAD~1
        ```

- *`Reverter commits mais antigos`*
    - *`Para cirar um commit que desfaz alterações de um commit específico:`*
        
        ```
        git revert <hash-do-commit>
        ```
        - *`Isso preserva o histórico de commits.`*

- *`Sincronizar com repositório remoto:`*
    - *`Forçar um reset para alinhar com o repositório remoto:`*
        ```
        git fetch origin
        git reset --hard origin/<branch>
        ```
    - *`Isso sincroniza sua branch local com o estado mais recente do repositório remoto.`*

    - *`Desfazer alterações já enviadas para o **GitHub**: Se você já fez um push e precisa corrigir, use:`*
        ```
        git push --force
        ```
    -  **Atenção** *`o uso de`* **`--force`** *`pode sobrescrever o trabalho de outros, então use com cuidado`*

*`Essas técnicas ajudam a corrigir erros e mantes o histórico do projeto organizado, mas é importante utilizá-las com responsabilidade, especialmente em ambientes colaborativos.`*

#### Enviando e Baixando Alterações com Repositórios Remotos (Git e GitHub)

- *`1° Clonar um Repositório Remoto`*

- *`Para obter uma cópia local de um repositório hospedado no`* **`GitHub`**, *`use comando:`*
    ```
    git clone <url-do-repositório>
    ````
- *`Exemplo:`*
    ```
    git clone https://github.com/usuario/repo.git
    ```
- *`Isso cria uma cópia do repositório remoto no seu computado.`*

-  *`2° Sincronizar Alterações`*
    - **`git fetch`**
        - *`Baixa as alterações do repositório remoto para o local sem integrá-la á sua branch atual`*
           
            ```
            git fetch origin
            ```
    - **`git pull`**
        - *`Combina`* **`fetch`** *`e`* **`merge,`** *` baixando e integrando as alterações remotas á branch local automaticamente.`**
            
            ```
            git pull origin  <branch>
            ```
        - *`Exemplo para baixar da branch principal:`*
           
            ```
            git pull origin main
            ```

- *`Enviar Alterações (Push):`*
    - *`Enviar commits locais para o repostório remoto:`*
        
        ```
        git push origin <branch>
        ```
    - *`Exemplo para enviar para a branch principal:`*
       
        ```
        git push origin main
        ```
    - *`Caso o repositório remoto tenha restrições (como revisão de pull requests), talvez seja necessário cirar uma branch separada:`*
        ```
        git checkou -b minha-branch
        git push origin minha-branch
        ```

- *`3° Resolver Conflitos`*
    - *`Conflitos podem surgir ao fazer`* **`git pull`** *`ou`* **`gti push.`**
    - *`Para resolver:`*
        - *`Edite os arquivos conflitantes manualmente`*
        - *`Marque os conflitos como reslvidos`*
            
            ```
            git add <arquivo>
            ```
        - *`Finalize o processo com um commit`*
            
            ```
            git commit
            ```

-  *`4° Configurar o Repositório Remoto`*
    - *`Adicionar um repositório a um projeto local:`*
        
        ```
        git remote add origin <url-do-repositório>
        ```
    - *`Verificar os repositorios remotos configurados:`*
        
        ```
        git remote -v
        ```
    
- *`5° Fluxo de Trabakho Comum`*
    - *`Faça alteração no código.`*
    - *`Use`* **`git add`** *´para preparar as alterações.`*
        
        ```
        git add .
        ```
    - *`Realize um commit para salvar as alterações localmente:`*
        ```
        git commit -m "Descrição do que foi alterado"
        ```
    - *`Envie para o repositório remoto:`*
        ```
        git push origin <branch>
        ```
    - *`Para integrar mudanças do remoto ao local use:`*
        ```
        git pull origin <branch>
        ```
    
#### Trabalhando com Branches no Git e GitHub

-  *`1° Criando Branches`*
    - *`Criar uma nova branch`*
        
        ```
        git branch <nome-da-branch>
        ```
    - *`Criar e mudar par nova branch:`*
        
        ```
        git checkout -b <nome-da-branch>
        ```
    - *`Listar branches`*
        
        ```
        git branch
        ```
        - *`A branch atual será indicado por um asterisco (*)`*
    
    - *`Enviar a branch para o repositótio remoto`* 
        ```
        git push -u origin <nome-da-branch>
        ```
    
- *`2° Alternando Entre Branches`*
    - *`Trocar para outra branch:`*
        
        ```
        git checkout <nome-da-branch>
        ```

    - *`No Git moderno, o comando alternativo é:`*

        ```
        git switch  <nome-da-branch>
        ```

- *`3° Mesclando Branches`*
    
    - *`Mesclar alterações de uma branch para outra:`*
    
        - *`Mude para a branch de destino (ex: main):`*
       
        ```
        git checkout main
        ```
        - *`Mescle a branch:`*
            
            ```
            git merge <nome-da-branch>
            ```
    - *`Mesclagem sem criar um commit adicional (fast-forward):`*
        
        - *`Essa abordagem é usada quando não ha divergências:`*
           
            ```
            git merge --ff-only <nome-da-branch>
            ```

- *`4° Deletando Branches`*
    - *`Deletar uma branch local`*
        
        ```
        git branch -d <nome-da-branch>
        ```
        - *`Forçar a exclusão de uma branch (não totalemnte mesclada):`*
            
            ```
            git branch -D  <nome-da-branch>
            ```
    - *`Deletar uma branch remota`*
       
         ```
        git push origin --delete  <nome-da-branch>
        ```

- *`5° Tratando Conflitos Durante a Mesclagem`*
    
    - *`Conlfitos ocorrem quando alterações em um mesma parte do códgio são feitar em diferentes branches.`*
    
    - *`Passos para reovler conflitos:`* 
       
        - *`O git marcará os arquivos com conflitos.`*
       
       - *`Abra os aqruivos e procure marcar de conflito  (<<<<<<<, =======,>>>>>>>).`*

       - *`Edite os arquivos para resolver os conflitos manualmente.`*

       - *`Marque o conflito como resolvido.`*
            
            ```
            git add <arquivo>
            ```
        - *`Finalize a mesclagem com um commit:`*

- *`6° FLuxo de Trabalho Comum com Branches`*
    - *`Crie uma ova branch para cada funcionalidade ou correção:`*
    
           git checkout -b minha-funcionalidade
        
    - *`Faça as alterações e confime os commits:`*

            git add . 
            git commit -m "Descrição das mudanças"
    
    - *`Envie a branch para o repositório remoto:`*
    
          git push oring minha-funcionalidade

    - *`Abra um Pull Request no GitHub para revisar e mesclar.`*

    - *`Meslce as alterções na branch principal após aprovação.`*

# **Códigos Utilizados**
|*Código*|*Explicação*|*Exemplos*|*Links*|
|---------|-------------|--------|-------|
|`Config`| Sistema de configuração usado para gerenciar as opções e preferências do Git| `git config --global user.name <Seu Nome>` */* `git config --global user.email <Seu Email>` */* `git help`|[![Config](https://img.shields.io/badge/Config-black?style=flat)](https://git-scm.com/docs/git-config)|
|`Mkdir`| Usado para criar uma nova pasta no sistema de arquivos |`mkdir <nome>`| [![Mkdir](https://img.shields.io/badge/Mkdir-black?style=flat)](https://learn.microsoft.com/pt-br/windows-server/administration/windows-commands/mkdir)|
|`Cd`| Navega entre pastas no terminal|`cd ..` */* `cd ~` */* `cd /`|[![Cd](https://img.shields.io/badge/Cd-black?style=flat)](https://graphite.dev/guides/change-directories-git-bash-windows) |
|`Ls`| Lista arquivos e pastas| `ls`|[![Ls](https://img.shields.io/badge/Ls-black?style=flat)](https://git-scm.com/docs/git-ls-files)|
|`Rm`| Remove arquivos do repositório| `git rm`|[![Rm](https://img.shields.io/badge/Rm-black?style=flat)](https://git-scm.com/docs/git-rm)|
|`Cat`| Exibe o conteúdo de arquivos no terminal| `cat <nome do arquivo>`|[![Cat](https://img.shields.io/badge/Cat-black?style=flat)](https://git-scm.com/docs/git-cat-file/pt_BR)|
|`Init`| Inicializa um novo repositório Git| `git init`|[![Init](https://img.shields.io/badge/Init-black?style=flat)](https://git-scm.com/docs/git-init/pt_BR)|
|`Branch`| Trabalha em branches| `git branch <nova-funcionalidade>`| [![Branch](https://img.shields.io/badge/Branch-black?style=flat)](https://git-scm.com/book/pt-br/v2/Branches-no-Git-Branches-em-poucas-palavras)|
|`Clone`| Copia um repositório existente| `git clone <URL-do-repositório>`|[![Clone](https://img.shields.io/badge/Clone-black?style=flat)](https://git-scm.com/docs/git-clone)|
|`Remote`| Gerencia conexões entre o repositório local e remotos| `git remote add <nome> <url>` */* `git remote ls` */* `git remote rm <nome>`|[![Remote](https://img.shields.io/badge/Remote-black?style=flat)](https://git-scm.com/docs/git-remote)|
|`Add`| Prepara alterações para commit| `git add <arquivo>` */* `git add .`|[![Add](https://img.shields.io/badge/Add-black?style=flat)](https://git-scm.com/docs/git-add/pt_BR)|
|`Commit`| Registra alterações no histórico do repositório| `git commit -m "Mensagem do commit"`|[![Commit](https://img.shields.io/badge/Commit-black?style=flat)](https://git-scm.com/docs/git-commit)|
|`Push`| Envia commits para um repositório remoto| `git push <nome remoto> <branch>`|[![Push](https://img.shields.io/badge/Push-black?style=flat)](https://git-scm.com/docs/git-push)|
|`Pull`| Atualiza branch local com alterações do repositório remoto| `git pull <nome remoto> <branch>`|[![Pull](https://img.shields.io/badge/Pull-black?style=flat)](https://git-scm.com/docs/git-pull)|
|`Status`| Mostra o estado do repositório| `git status`|[![Status](https://img.shields.io/badge/Status-black?style=flat)](https://git-scm.com/docs/git-status)|
|`Log`| Exibi histórico de commits| `git log`|[![Log](https://img.shields.io/badge/Log-black?style=flat)](https://git-scm.com/docs/git-log)|
|`Reset`| Desfaze alterações em commits| `git reset [<--soft/--mixed/--hard>] <commit>`|[![Reset](https://img.shields.io/badge/Reset-black?style=flat)](https://git-scm.com/docs/git-reset)|
|`Restore`| Desfaze alterações em um repositório local| `git restore <arquivo>` */* `git restore .`|[![Restore](https://img.shields.io/badge/Restore-black?style=flat)](https://git-scm.com/docs/git-restore)|
|`Clean`| Exclui arquivos não rastreados| `git clean -f`|[![Clean](https://img.shields.io/badge/Clean-black?style=flat)](https://git-scm.com/docs/git-clean)|
|`Revert`| Cria um commit que desfaz alterações de outro commit| `git revert <commit>`|[![Revert](https://img.shields.io/badge/Revert-black?style=flat)](https://git-scm.com/docs/git-revert)|
|`Checkout/Switch`| Alterna entre branches| `git checkout <branch>` */* `git switch <branch>`|[![Checkout/Switch](https://img.shields.io/badge/Checkout%2FSwitch-black?style=flat)](https://git-scm.com/docs/git-checkout)|
|`Fetch`| Baixa as alterações do repositório remoto, mas não as integra à sua branch local.|`git fetch origin`|[![Fetch](https://img.shields.io/badge/Fetch-black?style=flat)](https://git-scm.com/docs/git-fetch)|
