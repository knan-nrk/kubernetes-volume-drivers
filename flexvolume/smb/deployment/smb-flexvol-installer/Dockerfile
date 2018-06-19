FROM busybox

MAINTAINER erik.inge.bolso@nrk.no

ADD ./smb /bin/smb
ADD ./install.sh /bin/install_smb_flexvol.sh

ENTRYPOINT ["/bin/install_smb_flexvol.sh"]
