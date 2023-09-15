# JaMIE
https://github.com/umeboshia/JaMIE

https://github.com/umeboshia/my_JaMIE

# OLD
なるべく互換性を保った環境．rootしかない．実行ディレクトリはdockerfileがあるファイルで．

`$ docker image build -t umeboshia/jamie_old:ver1 .`

`$ docker run -it --name jamie_old1 --gpus all umeboshia/jamie_old:ver1 bash`

# NEW
書き換えにより環境を整える意味で作った環境．ユーザーがいる．

`$ docker image build -t umeboshia/jamie_new:ver1 .`

`$ docker run -it -v /home/yoshimura.19094/projects/research2022:/workspace -v /data/yoshimura.19094:/data --name jamie_new1 --gpus all umeboshia/jamie_new:ver1 bash`

not in server:

`docker run -it --name jamie_new1 --gpus all umeboshia/jamie_new:ver1 bash`

---------------------------
<!-- 
`docker run -it --name devel6.1 -p 8080:3000 -v /home/yoshimura.19094/projects/research2022:/workspace -v /data/yoshimura.19094:/data -v ~/.ssh:/root/.ssh --gpus all umeboshia/research:ver5.6.1 bash`

`docker run -it -v /home/yoshimura.19094/projects/research2022:/workspace -v ~/.ssh:/home/yoshimura.19094/.ssh --name jamie_new1 --gpus all umeboshia/jamie_new:ver1 bash` -->
