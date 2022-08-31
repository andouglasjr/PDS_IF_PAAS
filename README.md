# PDS_IF_PAAS
Material para as disciplinas de Introdução a Eng Software para os alunos do curso de Informática do IFRN/PAAS.

## Arquitetura Cliente Servidor

### Enviroment

Antes de iniciar, vamos criar um ambiente de densevolvimento. Isso facilita salvar bibliotecas específicas para cada projeto sem alterar o ambiente global.

1 - Criando um novo ambiente

```
    > python3 -m venv ArquiteturaClienteServidor
```

2 - Acessando o ambiente criado

No windows executa:

```
    > ArquiteturaClienteServidor\Scripts\activate.bat
```

No ubuntu executa:

```
    > souce ArquiteturaClienteServidor/bin/activate
```

Pronto. Agora todo novo pacote que você instalar dentro desse ambiente só será acessado pelos códigos do próprio ambiente.

### Instalando o Flask

O Flask é uma pequeno Framework escrito em Python que permite a criação de sistemas webs de forma simples, baseado em roteamento. O núcleo é bem simples, porém extensível. Não possui camada de abstração de banco de dados, validação de formulário ou quaisquer outros componentes onde bibliotecas de terceiros pré-existentes fornecem funções comuns. No entanto, o Flask oferece suporte a extensões que podem adicionar recursos do aplicativo como se fossem implementados no próprio Flask. Existem extensões para mapeadores objeto-relacional, validação de formulário, manipulação de upload, várias tecnologias de autenticação aberta e várias ferramentas comuns relacionadas ao framework.

Para instalar o flask basta executar o comando a seguir. OBS.: Lembre de verificar se está no ambiente criado acima.

```
    > pip install Flask
```


Testando alteração de conta.