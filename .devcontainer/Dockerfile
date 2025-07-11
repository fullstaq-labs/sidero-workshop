FROM mcr.microsoft.com/devcontainers/base:debian

ADD --chmod=777 get-ip /usr/local/bin/get-ip
ADD --chmod=777 kubectl-oidc_login /usr/local/bin/kubectl-oidc_login

RUN sudo apt update && sudo apt install -y --no-install-recommends \
  entr git &&\
  echo "alias k=kubectl" >> /home/vscode/.bashrc &&\
  echo "complete -F __start_kubectl k" >> /home/vscode/.bashrc
