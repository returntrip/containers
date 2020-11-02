FROM registry.fedoraproject.org/fedora:33

LABEL version="$VERSION"                                              \
      usage="This image is meant to be used with the toolbox command" \
      summary="Vagrant ready image"                                   \
      maintainer="Stefano Figura <stefano@figura.im>"

COPY extra-packages /
RUN dnf -y upgrade                                                                                                    \
    && dnf -y install $(<extra-packages)                                                                              \
    && rm /extra-packages                                                                                             \
    && dnf clean all
CMD [ "/bin/bash" ]
