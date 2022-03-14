FROM ubuntu:22.04

RUN apt update && \
   apt-get install -y ruby-full build-essential zlib1g-dev

RUN echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc && \
   echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc && \
   echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc && \
   . ~/.bashrc && \
   gem install jekyll bundler
VOLUME site
WORKDIR site
EXPOSE 4000/tcp
