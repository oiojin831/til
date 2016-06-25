# Docker Basics
기본적인 Docker에서 많이 쓰이는 용어

## docker engine
**Server, docker daemon** <--> **REST API** <--> **Client, docker CLI**
- Docker daemon
  Docker daemon 은 Docker Host에서 실행되는데 사용자는 직접 daemon과
    통신하지는 않고 Docker client를 통해 상호작용을 한다.
- Docker client
  Docker(binery)로 docker daemon과 통신하는 primary UI로 사용된다.

![Alt text](https://docs.docker.com/engine/article-img/architecture.svg)

## Docker's internals
- Docker images
  read only template이라고 생각하면된다. 예를 들어 image는 우분투, 아파치와 web app이 설치를 포함하고있을 수있다. image는 container를 만드는데 사용된다.  Docker의 ```build``` component이다.

- Docker registries
  public, private으로 image를 저장하는 공간이다.
- Docker containers
  container는 directory랑 비슷하다. application이 실행되기 위한 모든게 담겨있다. Docker의 ```run``` component이다.

### Image and container
[image vs container](http://stackoverflow.com/questions/23735149/docker-image-vs-container)

# Docker Machine

Docker 자체를 설치하기위해 필요한 도구다. (Docker App이 생기면서 필요없이지게됨) Docker Engine을 virtual hosts에 설치하게 해주는 툴이다.  docker-machine 명령어로 호드트들을 관리하게 해준다.  Machine으로 어떤 머신에든 Docker hosts를 만들수있다.  Machine CLI로 동작하고 관리되고있는 host를 point 하면 docker 명령어를 사용할수있다

