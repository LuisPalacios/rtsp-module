

[Movistar TV: Video bajo demanda con router Linux](http://www.luispa.com/?p=378)


Aquí tienes la versión del programa y el parche documentado en dicho artículo: 


#### ___DESCARGA___
    
    # mkdir /tmp/rtsp
    # cd /tmp/rtsp
    # wget http://mike.it-loops.com/rtsp/rtsp-module-3.7-v2.tar.gz
    : 
    # tar xvfz rtsp-module-3.7-v2.tar.gz
    # rm rtsp-module-3.7-v2.tar.gz

#### ___PATCH___
    Copia/Pega desde pastebin el parche: http://pastebin.com/4QZ2r7eV 
    Crea un fichero por ejempo en: /tmp/rtsp-3.7-v2.patch

    # patch < /tmp/rtsp-3.7-v2.patch

#### ___COMPILA___
    # make debug
    :

#### ___INSTALA MODULOS KERNEL___
    # make modules_install
    :
    # ls -al /lib/modules/3.17.0-gentoo/extra/
    total 36
    drwxr-xr-x 2 root root 4096 oct 18 16:37 .
    drwxr-xr-x 5 root root 4096 oct 18 16:41 ..
    -rw-r--r-- 1 root root 13305 oct 18 16:41 nf_conntrack_rtsp.ko
    -rw-r--r-- 1 root root 11369 oct 18 16:41 nf_nat_rtsp.ko
 
 
 
 