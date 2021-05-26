FROM gblin/minivpl
LABEL maintainer="guillaume.blin@u-bordeaux.fr"
LABEL authors="Guillaume Blin and Corentin Abel Mercier"
RUN install_packages opam ocaml m4 aspcud
WORKDIR /tmp/
RUN opam init -y --root=/usr/local/opam && eval `opam config env --root=/usr/local/opam` && opam switch create 4.12.0 && opam switch 4.12.0 && opam install ocamlfind qtest qcheck oUnit
