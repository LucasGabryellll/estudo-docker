Estudo Docker:

# COMANDOS:
OBS: Por padrão as imagens são baixadas do Hub Docker.

 -> `docker run` `imagem`: *Executa um novo Container, descrito após o run, do Docker Docks*.
  Exemplo: docker run ubuntu -> Roda um Container com uma Imagem do Ubuntu.

 -> `docker ps`: *Lista todos os Containers que estão em execução no momento*.

 -> `docker ps -a`: *Lista todos os Containers que foram executados*.

 -> `docker run ubuntu bash`: *Após subir o container Ubuntu será executado o comando bash*.
  OBS: Caso queira executar algum comando após inicialização de um Container basta escrever dessa forma.

  -> `docker run -it ubuntu bash`: *Executa o docker no modo interativo no comando Bash trocando mensagens Bidirecionais*.
  OBS: -i: `Modo Interativo`, t: `Mensanges Bidirecionais`.

  -> `docker run -p 8080:80 nginx`: *Executa a imagem do nginx porém encaminhando a porta escolhida da minha máquina para a que a imagem está executando*.
  Ex: localhost:8080 sera encaminhando para localhost:80 da imagem executada.
  
  -> `crtl + d (sair do contêiner/bash)`
  
  -> `docker exec sisakjysa ls`: *Vai executar o comando escolhido em um Container em execução escolhido pelo seu name ou id*
  OBS: Vai executar o comando `ls` no container que tem esse id `sisakjysa`

  -> `docker run -p 8080:80 -v $(pwd)/html:/usr/share/nginx/html nginx`: *Especifica um volume que serve para não perder dados de um Container, Vai ser igual*.
   OBS: `$(pwd)=A Pasta atual que o terminal está sendo executado`,Porém pode ser qualquer pasta do PC.
   OBS2: *Então sempre que algo for alterado na pasta html do MEU PC será alterado na pasta com o caminho descrito apos os `:` nesse caso `/usr/share/nginx/html` a parta HTML do Container*.
   Ex: Todos os arquivos que tenho em uma pasta se forem alterados o container vai Atualizar tudo.

  -> `docker build -t lucasgabdev/criar-imagem:latest .`: *Cria uma imagem Apartir do arquivo Dockerfile*.
  OBS: Cria uma imagem com nome `criar-imagem` com o meu usuário do Docker Hub pegando o arquivo Dockerfile que está localizado na mesma pasta descrito com o `.`.

  -> `docker compose up`: *Cria um ambiente com tudo que for necessário, executando todos os comendos que contem no arquivo `docker-compose.yaml` -> Tudo que estiver nesse arquivo será executado*.

  -> `docker compose down`: *Para todos os Containers que estão no compose.yaml*.
