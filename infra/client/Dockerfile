FROM node:8

RUN useradd --user-group --create-home --shell /bin/false app

ENV HOME=/home/app
ENV APP=$HOME/client

COPY ./codebase/client $APP
RUN chown -R app:app $HOME/*

USER app
WORKDIR $APP

CMD ["npm", "start"]
