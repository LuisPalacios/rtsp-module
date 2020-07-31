

[Movistar TV: Video bajo demanda con router Linux](http://www.luispa.com/?p=378)


Dejo aquí un fork de los ficheros descritos en dicho apunte: 


#### ___DESCARGA___

Descarga el fichero [rtsp-module-3.7-v2.tar.gz](https://raw.githubusercontent.com/LuisPalacios/rtsp-module/master/rtsp-module-3.7-v2.tar.gz)
    
    # mkdir /tmp/rtsp
    # cd /tmp/rtsp
    # wget https://raw.githubusercontent.com/LuisPalacios/rtsp-module/master/rtsp-module-3.7-v2.tar.gz
    : 
    # tar xvfz rtsp-module-3.7-v2.tar.gz
    # rm rtsp-module-3.7-v2.tar.gz

#### ___PATCH___ 

Descarga los ficheros .patch y aplícalos en orden... 

    # wget https://raw.githubusercontent.com/LuisPalacios/rtsp-module/master/rtsp-3.7-v2.patch
    # wget https://raw.githubusercontent.com/LuisPalacios/rtsp-module/master/rtsp-3.7-v2-range2.patch
    # wget https://raw.githubusercontent.com/LuisPalacios/rtsp-module/master/rtsp-3.7-v2-nuevo.patch
    # wget https://raw.githubusercontent.com/LuisPalacios/rtsp-module/master/rtsp-3.7-v2-nuevo2.patch

    # patch < /tmp/rtsp-3.7-v2.patch
    # patch < /tmp/rtsp-3.7-v2-range2.patch
    # patch < /tmp/rtsp-3.7-v2-nuevo.patch
    # patch < /tmp/rtsp-3.7-v2-nuevo2.patch


#### ___COMPILA___

    # make
    :

#### Opcional, si quieres hacer debug... 

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
 
 
 
 
