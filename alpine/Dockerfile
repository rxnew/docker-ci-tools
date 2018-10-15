FROM alpine

RUN apk --no-cache update && \
    apk --no-cache add python py-pip py-setuptools ca-certificates curl less zip openssh-client git && \
    pip --no-cache-dir install --upgrade pip && \
    pip --no-cache-dir install awscli && \
    mkdir -p ~/.ssh && \
    chmod 700 ~/.ssh && \
    echo -e "Host *\n\tStrictHostKeyChecking no\n\n" > ~/.ssh/config && \
    git config --global http.sslVerify false
