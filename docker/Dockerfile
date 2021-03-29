FROM centos:centos7
LABEL maintainer="Ghassen Sghaier <medghassen.sghaier@iit.ens.tn>"

RUN yum -y update

RUN yum install -y epel-release && \ 
    yum install -y \
        nginx && \
    yum clean all	
COPY ./index.html /usr/share/nginx/html/
RUN current_time=$(date "+%Y.%m.%d-%H.%M.%S") && \
echo "<html><body><h1>Hello FivePoints </h1><div>$current_time</div></body></html>" > /usr/share/nginx/html/index.html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
