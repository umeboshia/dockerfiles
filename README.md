# dockerfiles
my docker files

# how to use
to make docker image, do this commnand at directory where dokcerfile exists
`$ docker image build -t <account_name>/<image_name>:<tag> {path}`
and docker run to run new container
`$ docker run -it --name jamie_old --gpus all umeboshia/jamie_old:ver.1 bash`
