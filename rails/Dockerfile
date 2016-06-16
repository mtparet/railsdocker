FROM ruby:2.3.1

RUN apt-get update && apt-get upgrade -y
RUN apt-get update && apt-get install -y nodejs --no-install-recommends && rm -rf /var/lib/apt/lists/*
RUN apt-get update && apt-get install -y mysql-client postgresql-client sqlite3 --no-install-recommends && rm -rf /var/lib/apt/lists/*

ENV GEM_HOME /ruby_gems/2.3/ruby/gems
ENV GEM_PATH $GEM_HOME:/lib/ruby/gems/2.3.1
ENV GEM_CACHE $GEM_HOME/cache
ENV PATH $PATH:/ruby_gems/2.3/ruby/gems/bin


ENV HOME  /usr/src/app
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

EXPOSE 3000
