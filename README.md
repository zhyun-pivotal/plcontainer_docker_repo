Docker install repository 사용법

[Clone or download] 버튼 클릭하여 Centos 버전에 맞는 파일 다운로드
다운로드된 tar 또는 gz 파일 다운로드
해당 파일 압축 해제하여 server에서 local repository 설정
분할압축 수행 명령은 아래와 같음
[~]# tar cvzf - centos74_docker-ce-stable.tar | split -b 24m - centos74_docker-ce-stable.tar.gz
분할압축(tar.gz*) 해제 명령은 아래와 같음
[~]# cat centos74_docker-ce-stable.tar.gz* | tar -xzvpf -
yum 명령을 이용하여 docker install 
[~]# yum install -y yum-utils device-mapper-persistent-data lvm2
[~]# yum install -y docker-ce



Docker install repository on off-line server

Click the [Clone or download] button to download the file suitable for the Centos version.
Download downloaded tar or gz file
Unzip the file and set up a local repository on the server
The command to perform divided compression is as follows.
[~]# tar cvzf-centos74_docker-ce-stable.tar | split -b 24m-centos74_docker-ce-stable.tar.gz
The command to release split compression (tar.gz*) is as follows
[~]# cat centos74_docker-ce-stable.tar.gz* | tar -xzvpf-
docker install using yum command
[~]# yum install -y yum-utils device-mapper-persistent-data lvm2
[~]# yum install -y docker-ce
