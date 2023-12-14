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
4. Inclua o usuário '`jenkins` no grupo `docker`. Isso permitirá que o `jenkins` execute comandos Docker sem necessidade de `sudo`:
```
sudo usermod -aG docker jenkins
```
5. Verifique se o usuário `jenkins` foi corretamente adicionado ao grupo `docker`:
```
grep docker /etc/group
```

# Configuração da Pipeline:

1. Faça login no Jenkins.
2. Clique em `+ Novo Tarefa`.
3. Nomeie a sua pipeline.
4. Escolha `pipeline` nas opções e selecione `Tudo certo`.
5. Adicione uma descrição se precisar.
6. Navegue até a seção `Pipeline`.
7. Em 'Definição', clique em 'Pipeline script' e selecione 'Pipeline script from SCM'.
8. Em 'SCM', escolha 'git'.
9. No campo 'Repository URL', insira a URL do projeto: 

`https://github.com/laisribeiroo/pipeline-jenkins.git` 

10. Em `Branch Specifier`, insira o nome da branch que você quer.

11. Clique em `Salvar` para concluir.

Com esses passoas feitos, a pipeline estará configrada.

# Implemetando a Pipeline

Para executar a pipeline:

1. Após criar a pipeline, no lado direito, localize e clique em `Construir agora`.

2. Em seguida, clique em `Open Blue Ocean`  para gerenciar a pipeline com uma interface gráfica mais intuitiva.

3. E Pronto!
