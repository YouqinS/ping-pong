IMAGE_TAG=exercise_1.09
IMAGE_NAME_WITH_TAG=pingpong:$(IMAGE_TAG)

all: package  image  push-image

package:
	./mvnw clean package

image:
	sudo docker build . -t $(IMAGE_NAME_WITH_TAG)


push-image:
	sudo docker login
	sudo docker tag $(IMAGE_NAME_WITH_TAG) lnsth/$(IMAGE_NAME_WITH_TAG)
	sudo docker push lnsth/$(IMAGE_NAME_WITH_TAG)


run:
	./mvnw org.springframework.boot:spring-boot-maven-plugin:run
