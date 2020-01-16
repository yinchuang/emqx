# =============================================================================
#
# CentOS-7 7.6.1810 x86_64
# 
# =============================================================================
FROM centos:centos7.6.1810

RUN \
    curl -o /etc/yum.repos.d/CentOS-Base.repo http://mirrors.aliyun.com/repo/Centos-7.repo && \
    curl -o /etc/yum.repos.d/epel.repo http://mirrors.aliyun.com/repo/epel-7.repo && \
    ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime

ADD docker-entrypoint.sh emqx-centos7-v3.2.7.tar.gz /opt/ 

WORKDIR /opt/emqx/

ENTRYPOINT ["/opt/docker-entrypoint.sh"]

CMD ["/opt/emqx/bin/emqx","foreground"]
