FROM python:3.8-buster

# ssh サーバーをインストールして、
# sshd を起動するのに必要な sshd ディレクトリを作成
RUN apt-get update -y \
    && apt-get install -y openssh-server \
    && mkdir /var/run/sshd \
    && mkdir ~/.ssh \
    && chmod 700 ~/.ssh \
    && touch ~/.ssh/authorized_keys \
    && chmod 600 ~/.ssh/authorized_keys 
EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]
