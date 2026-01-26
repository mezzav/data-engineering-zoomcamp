## Question 1
What is the version of `pip` in the image?

Using the [Dockerfile](Dockerfile) in the repository, I built the image with the command `docker build -t hw1:q1 .`. After the image was successfully built, I started a container using `docker run -it hw1:q1,` which opened an interactive shell inside the container. From there, I ran `pip --version` and received the output `pip 25.3`.

## Question 2

Since these services are defined in a Docker Compose file, Docker Compose creates an internal network that allows the services to communicate with each other. As a result, pgAdmin should use the service name `db` as the hostname and connect on port `5432`, which is the port exposed by the Postgres container.


Note: I did the data analysis for questions 3 - 6 in pandas

## Question 3

8007

## Question 4

88.03 miles

## Question 5

East Harlem North

## Question 6

Yorkville West

## Question 7

```
terraform init
terraform apply -auto-approve 
terraform destroy
```