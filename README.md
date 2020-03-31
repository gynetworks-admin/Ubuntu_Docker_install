# Ubuntu_Docker_install

## 필요 환경
Ubuntu\
Nvidia Driver\
CUDA

## 설치되는 항목
Docker\
Nvidia Docker

## 설치 방법
Ubuntu 터미널을 실행 시키고 위 shell script를 실행한다.
~~~
sudo bash Docker_install.sh
~~~

## 주의사항
 Nvidia Docker를 실행하기 위해서는 CUDA가 지원되는 Nvidia 그래픽 카드가 필요합니다. 그래픽 카드를 확인하고 그래픽 드라이버 설치를 확인 후 진행합니다.

## 설치 확인
~~~
sudo docker run --gpus all -it --rm tensorflow/tensorflow:1.13.2-gpu-py3  python -c "import tensorflow as tf; tf.Session();"
~~~
 Tensorflow가 자신의 그래픽 카드를 잡은 것이 확인되면 완료.
