# pipeline-jenkins
Criação de uma pipeline de integração e entrega contínua no Jenkins para uma aplicação de serviço restful que utiliza o framework Flask-restful para a disciplina de Gerência e Configuração de Internet.

## A seguir um Guia Básico para execução dessa pipeline.


# Guia para Executar o Projeto 'Pipeline' com Jenkins.

## Configurações Iniciais

Para começar, certifique-se de ter as permissões corretas:

1. Navegue até o diretório essencial usando o comando:
```
cd /var/run
```
2. Garanta permissões para o docker.sock:
```
sudo chmod 777 docker.sock
```
3. Adicione um novo usuário denominado `jenkins`:
```
useradd jenkins
```
4. Inclua o usuário '`jenkins` no grupo `docker`.
```
sudo usermod -aG docker jenkins
```

# Configuração da Pipeline passo a passo:

1. Faça login no Jenkins e em seguida, clique em `+ Novo Tarefa`, e assim, nomeie a sua pipeline.
2. Escolha `pipeline` nas opções e selecione `Tudo certo`.
3. Navegue até a seção `Pipeline`.
4. Em 'Definição', clique em 'Pipeline script' e selecione a 'Pipeline script from SCM'.
5. Em 'SCM', escolha 'git'. Em seguida coloque no campo certo a URL desse projeto: 

`https://github.com/laisribeiroo/pipeline-jenkins.git` 

6. Já na `Branch Specifier`, insira o nome da branch que você quer e depois é só salvar, para concluir.

Com esses passos feitos, a pipeline estará configrada.

# Implemetando a Pipeline

Para executar a pipeline:

1. Após criar a pipeline, clique em `Construir agora`.

2. Em seguida, clique em `Open Blue Ocean`  para gerenciar a pipeline.

3. E Pronto!
