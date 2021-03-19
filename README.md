# setup the docker repository

off-line 서버에 docker repository 설정

1. [Clone or download] 버튼 클릭하여 Centos 버전에 맞는 파일 다운로드

2. 다운로드된 tar 또는 gz 파일 압축 해제하여 server에서 local repository 설정

2-1. 분할압축 수행 명령은 아래와 같음
[/]# tar cvzf - centos74_docker-ce-stable.tar | split -b 24m - centos74_docker-ce-stable.tar.gz

2-2. 분할압축(tar.gz*) 해제 명령은 아래와 같음
[/]# cat centos74_docker-ce-stable.tar.gz* | tar -xzvpf -

3. yum 명령을 이용하여 docker install 
[/]# yum install -y yum-utils device-mapper-persistent-data lvm2
[/]# yum install -y docker-ce

------------------------------------------------------------------------------------------
How to setup the docker repository on off-line server

1. Click the [Clone or download] button to download the file suitable for the Centos version.

2. Unzip the downloaded tar or gz file and set up a local repository on the server.

2-1. The command to perform divided compression is as follows.
[/]# tar cvzf-centos74_docker-ce-stable.tar | split -b 24m-centos74_docker-ce-stable.tar.gz

2-2. The command to release split compression (tar.gz*) is as follows
[/]# cat centos74_docker-ce-stable.tar.gz* | tar -xzvpf-

3. Use the yum command to install docker
[/]# yum install -y yum-utils device-mapper-persistent-data lvm2
[/]# yum install -y docker-ce
