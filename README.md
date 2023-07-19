# dockerfiles
my docker files

# how to use
to make docker image, do this commnand at directory where dokcerfile exists

`$ docker image build -t <account_name>/<image_name>:<tag> {path}`

and docker run to run new container

`$ docker run -it --name <container_name> --gpus all <account_name>/<image_name>:<tag> bash`
