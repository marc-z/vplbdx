FROM gblin/minivpl
LABEL maintainer="guillaume.blin@u-bordeaux.fr"
LABEL authors="Guillaume Blin and Corentin Abel Mercier"
RUN install_packages opam ocaml m4 aspcud git rsync mercurial darcs bubblewrap
WORKDIR /tmp/
ENV OPAMROOT=/usr/local/opam
RUN curl -sL https://raw.githubusercontent.com/ocaml/opam/master/shell/install.sh | /bin/bash
RUN mkdir /usr/local/opam && export OPAMROOT=/usr/local/opam && \
    opam init --disable-sandboxing --no-setup && \
    eval $(opam env) && \
    opam switch create 4.12.0 && \
    eval $(opam env) && \
    opam switch set 4.12.0 && \
    eval $(opam env)
ENV OPAMSWITCH=4.12.0
RUN opam install --yes ocamlfind qtest qcheck oUnit
RUN eval $(opam env)
