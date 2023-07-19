# JaMIE
https://github.com/umeboshia/JaMIE
https://github.com/umeboshia/my_JaMIE

# OLD
なるべく互換性を保った環境．rootしかない．

`$ docker image build -t umeboshia/jamie_old:ver1 .`
`$ docker run -it --name jamie_old --gpus all umeboshia/jamie_old:ver1 bash`

# NEW
書き換えにより環境を整える意味で作った環境．ユーザーがいる．

`$ docker image build -t umeboshia/jamie_new:ver1 .`
`$ docker run -it --name jamie_new --gpus all umeboshia/jamie_new:ver1 bash`
