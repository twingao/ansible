# Ansible 2.9.6安装

CentOS系统版本。

    cat /etc/redhat-release
    CentOS Linux release 7.7.1908 (Core)

    uname -a
    Linux ansible 3.10.0-1062.18.1.el7.x86_64 #1 SMP Tue Mar 17 23:49:17 UTC 2020 x86_64 x86_64 x86_64 GNU/Linux

安装扩展源，并查找Ansible。

    yum -y install epel-release
    
    yum list ansible --showduplicates | sort -r
    已加载插件：fastestmirror
    可安装的软件包
     * updates: mirror.bit.edu.cn
    Loading mirror speeds from cached hostfile
     * extras: mirror.bit.edu.cn
     * epel: mirrors.tuna.tsinghua.edu.cn
     * base: mirror.bit.edu.cn
    ansible.noarch                       2.9.6-1.el7                          epel
    ansible.noarch                       2.4.2.0-2.el7                        extras

安装ansible。

    yum install -y ansible-2.9.6-1.el7
    ......
    已安装:
      ansible.noarch 0:2.9.6-1.el7
    
    作为依赖被安装:
      PyYAML.x86_64 0:3.10-11.el7                                            libyaml.x86_64 0:0.1.4-11.el7_0
      python-babel.noarch 0:0.9.6-8.el7                                      python-backports.x86_64 0:1.0-8.el7
      python-backports-ssl_match_hostname.noarch 0:3.5.0.1-1.el7             python-cffi.x86_64 0:1.6.0-5.el7
      python-enum34.noarch 0:1.0.4-1.el7                                     python-httplib2.noarch 0:0.9.2-1.el7
      python-idna.noarch 0:2.4-1.el7                                         python-ipaddress.noarch 0:1.0.16-2.el7
      python-jinja2.noarch 0:2.7.2-4.el7                                     python-markupsafe.x86_64 0:0.11-10.el7
      python-paramiko.noarch 0:2.1.1-9.el7                                   python-ply.noarch 0:3.4-11.el7
      python-pycparser.noarch 0:2.14-1.el7                                   python-setuptools.noarch 0:0.9.8-7.el7
      python-six.noarch 0:1.9.0-2.el7                                        python2-cryptography.x86_64 0:1.7.2-2.el7
      python2-jmespath.noarch 0:0.9.0-3.el7                                  python2-pyasn1.noarch 0:0.1.9-7.el7
      sshpass.x86_64 0:1.06-2.el7

查看版本。

    ansible --version
    ansible 2.9.6
      config file = /etc/ansible/ansible.cfg
      configured module search path = [u'/root/.ansible/plugins/modules', u'/usr/share/ansible/plugins/modules']
      ansible python module location = /usr/lib/python2.7/site-packages/ansible
      executable location = /usr/bin/ansible
      python version = 2.7.5 (default, Aug  7 2019, 00:51:29) [GCC 4.8.5 20150623 (Red Hat 4.8.5-39)]
















