FROM docker:dind

RUN apk add curl
RUN curl https://raw.githubusercontent.com/nektos/act/master/install.sh | sh

COPY .actrc /
RUN mv /.actrc ~/.actrc

WORKDIR /REPO

CMD /bin/sh -c "act -n > /logs/dry-run.log; act > /logs/run.log"
