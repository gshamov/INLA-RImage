Bootstrap: docker
From:  rocker/r-ver:latest

%post
        apt-get update
        apt-get install -y libssl-dev libsasl2-dev jags
        apt-get install -y curl  httpie libudunits2-dev
        #apt-get install -y gdal-bin gdal-data libgdal-dev libgdal-grass libgdal-java

        R -e "install.packages('ggplot')"
        R -e "install.packages('jsonlite')"
        R -e "install.packages('dplyr')"
        R -e "install.packages('ggplot2')"
        R -e "install.packages('igraph')"
        R -e "install.packages('Matrix')"
        R -e "install.packages('shiny')"
        R -e "install.packages('rjags')"
        R -e "install.packages('dclone')"
        R -e "install.packages('sp')"
        R -e "install.packages('lme4')"
        R -e "install.packages('MASS')"
        R -e "install.packages('psych')"

       #echo "DONE with dependencies?"
       #sleep 10

        R -e 'install.packages("INLA", repos="https://inla.r-inla-download.org/R/stable")'
        R -e 'update.packages("INLA", dep=TRUE)'
        mkdir /global
        mkdir /global/scratch
        mkdir /scratch
        mkdir /project

%runscript
        R --version
        
