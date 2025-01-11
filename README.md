<h1>
    <a href="https://www.dio.me/">
     <img align="center" width="40px" src="https://hermes.digitalinnovation.one/assets/diome/logo-minimized.png"></a>
    <span> DIO | Resumos Git e GitHub</span>
</h1>

Repositorio para armazenar resumos Git e Github do curso Versionamento de Código com Git e Github da [Inteligência Artificial Aplicada a Dados com Copilot](https://web.dio.me/track/coding-the-future-heineken-ia-para-analise-de-dados).

## 📒 Documentação

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

## 🖥️ Resumo das Aulas

## 🔧 Visão Geral do Curso e Ferramentas

#### O que é Versionamento de Código?

- *`O versionamento de código é uma prática essencial no desenvolvimento de software que permite acompanhar as alterações feitas no código ao longo do tempo. Ele utiliza sistemas de controle de versão, como o Git, para registrar modificações, criar históricos detalhados, colaborar com outras pessoas de forma eficiente e reverter alterações, se necessário. Com o versionamento, é possível gerenciar diferentes versões de um projeto, trabalhar em equipe sem conflitos e garantir a integridade do código.`* 

#### O que é Git?

- *`O Git é uma ferramenta de controle de versão que permite registrar e gerenciar alterações em projetos de software. Ele facilita o trabalho em equipe, mantendo um histórico completo de mudanças, permitindo criar ramificações para novas funcionalidades e combinar alterações. É rápido, distribuído e amplamente usado com plataformas como GitHub e GitLab para colaboração.`*

#### O que é GitHub?

- *`O GitHub é uma plataforma online para hospedagem de repositórios Git. Ele permite que desenvolvedores colaborem em projetos, compartilhem código, rastreiem alterações e gerenciem versões. Além disso, oferece recursos como pull requests, issues e integração com ferramentas de desenvolvimento, sendo amplamente utilizado para projetos open source e privados.`*

## ⚙️ Instalação, Configuração e Autenticação

#### Instalando o Git no Windows
<h1>
    <code style="font-weight: bold; font-size: 2px;">1° Baixar o instalador: Acesse o site oficial do</code>
    <a href="https://git-scm.com/doc">
        <img align="center" width="80px" src="https://img.shields.io/badge/Git-000?style=for-the-badge&logo=git&logoColor=E94D5F">
    </a>
    <code style="font-weight: bold; font-size: 2px;">e baixe a versão para Windows.</code>
</h1>


**`2° Executar o instalador: Clique no arquivo baixado para iniciar a instalação.`**

**`3° Configurar a instalação:`**
- *`Escolha as opções padrão para a maioria dos casos.`*
- *`Selecione o editor padrão (como Vim ou outro de sua escolha).`*
- *`Configure como o Git será usado no terminal (recomenda-se "Git Bash").`*

**`4° Concluir a instalação: Finalize o processo e abra o Git Bash para começar a usar o Git.`**

#### Configurando o Git

- *`Abra o Git Bash e configure seu nome, e-mail e o nome padrão da branch:`*
```
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@example.com"
git config --global init.defaultBranch main
```
- *`Agora, toda vez que você inicializar um repositório com git init, a branch principal será chamada main em vez de master (o padrão antigo).`*

#### ✅ Autenticando via Token

**`1°Gerar o Token de Acesso:`**

- *`Acesse sua conta no GitHub e vá para Settings (Configurações).`* [![Static Badge](https://img.shields.io/badge/GIThub-000?style=for-the-badge&logo=github&logoColor=32A3DC&logoSize=100)](https://github.com/settings/profile)


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

#### ✅ Autenticando via Chave SSH

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
- *`Acesse o GitHub e vá para Settings (Configurações).`*[![Static Badge](https://img.shields.io/badge/GIThub-000?style=for-the-badge&logo=github&logoColor=32A3DC&logoSize=100)](https://github.com/settings/profile)

- *`Clique em SSH and GPG keys > New SSH key.`*

- *`Cole a chave pública copiada no campo "Key".`*

- *`Dê um nome à chave (ex.: "Meu PC") no campo "Title".`*

- *`Clique em Add SSH Key.`*

**`4° Testar a conexão com o GitHub`**

*`No terminal, clone o repositório usando a URL SSH:`*
```
git clone git@github.com:seu-usuario/seu-repositorio.git
```
- *`Digite sua senha se for solicitado ou confirme com o token SSH.`*
