# Answers

Nom: Grimault
Prénom: Théophile
NB: 6

## 1.3
command: sudo docker build .

## 1.4
answer: les ports sont fermés
command: sudo docker run -p 8080:8080 tp2

## 1.5
command: sudo docker run -e ENVIRONMENT=dev tp2

## 1.6
answer: elle ne peut pas être push car il lui faut un tag
command: sudo docker tag b56321cc8ffc kingsun21/tp2

## 1.7
answer: il faut mettre sudo docker run kingsun21/tp2 au lieu de juste tp2, car
	le dépôt n'existe plus localement, mais seulement sur le hub
command: sudo docker rmi -f $(docker images -q)
command: sudo docker run -p 8080:8080 -e ENVIRONMENT=dev kingsun21/tp2
command: sudo docker run -p 8080:8080 -e ENVIRONMENT=dev -d kingsun21/tp2

## 1.8
answer: le container démarre après avoir été relancé, une fois le terminal 
	relancé également
command: sudo docker ds
command: sudo docker rename musing_volhard dockername
	 sudo docker restart dockername

## 1.9
answer: l'OS du container est Debian
answer: PRETTY_NAME="Debian GNU/Linux 9 (stretch)"
	NAME="Debian GNU/Linux"
	VERSION_ID="9"
	VERSION="9 (stretch)"
	ID=debian
	HOME_URL="https://www.debian.org/"
	SUPPORT_URL="https://www.debian.org/support"
	BUG_REPORT_URL="https://bugs.debian.org/"

## 1.11
command: sudo docker run -p 8081:8081 -e APP_PORT=8081 -e WS_BACK_URL=172.17.0.1 -d fronttp2
answer: http://localhost:8081/theophile (With path : theophile)

## 2.1
command: sudo docker-compose run -p 8080:8080 -e ENVIRONMENT=dev service-back

## 2.6
command: sudo docker-compose up
command: sudo docker-compose logs

## 2.9
command: sudo docker-compose up -d --scale backtp2=2

