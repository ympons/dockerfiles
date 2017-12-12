FROM circleci/ruby
LABEL maintainer="Yaismel Miranda <yaismel.miranda@gmail.com>" 

RUN wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | \ 
    sudo apt-key add - && \
    sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt/ trusty-pgdg main" >> /etc/apt/sources.list.d/postgresql.list' && \
    sudo apt-get update && sudo apt-get install -y postgresql-client-9.6