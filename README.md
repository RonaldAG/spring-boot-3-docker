# Docker Basic

Para rodar esse projeto, siga os passos abaixo:

1. Baixar ou dar git clone
2. docker build -t <image_name:tag> .
3. docker run <image_name>

OQUE É O DOCKER?
- É um serviço de virtualização
- Contém todas as dependencias da aplicação em uma imagem docker
- Faz a separação de cada container dentro do mesmo computador de forma que nenhum enxerga o outro.
  Essa separação é obtida através de cgroups e namespaces, fazendo com que cada processo (container) pare de enxergar os demais processos, mentindo para essa aplicação como se ela fosse a unica na máquina.
- Cada container possui sua partição de memória e recursos da máquina e separação de rede.
- Utiliza o mesmo sistema operacional do hospedeiro. (Diferente de VM's que sobem novos sistemas operacionais para cada VM).

POR QUE UTILIZAR DOCKER?

Utilizando docker, estamos virtualizando o ambiente e salvando todas as configurações dentro desse container, possibilita que essa aplicação rota em diferentes ambientes.

DOCKERFILE

É um arquivo que contém as informações necessárias para gerar uma imagem docker.

IMAGEM

É o produto de um dockerfile.

CONTAINER

É uma imagem docker sendo executada.

COMANDOS
- docker ps: lista todas os container rodando.
- docker run <image_name>: combinação dos comandos docker create e docker start. Ou seja, esse comando cria um novo container com base na imagem e executa ele. Caso a imagem nao possua nenhum processo rodando, ele irá morrer.
- docker run -it ubuntu it: comando para interagir com o bash do ubuntu de um container
- docker stop <id_container>: para o container que está em execução.
- docker start <id_container>: comando para iniciar o container com o id.
- docker exec -iti <id_container> bash: comando utilizado para acessar o bash do container após ele estar rodando.
- docker build -t <image_name>: gera uma imagem docker com base no arquivo dockerfile.
- docker image ls: visualiza todas as imagens docker instaladas na máquina
- docker push <repository_name:tag> : adicionar a imagem em questão no repositório docker hub
