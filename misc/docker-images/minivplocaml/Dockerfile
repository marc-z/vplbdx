FROM gblin/minivpl
LABEL maintainer="guillaume.blin@u-bordeaux.fr"
LABEL authors="Guillaume Blin and Corentin Abel Mercier"
RUN install_packages opam ocaml m4 aspcud
WORKDIR /tmp/
RUN opam init -y --root=/usr/local/opam && eval `opam config env --root=/usr/local/opam` && opam install qtest ocamlfind qcheck ounit2 utop | tr "\n" " "` -y
