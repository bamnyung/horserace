How to use AWS : EC2 ?
===============================

- 우리가 현재 사용하고 있는 AWS 스펙 : EC2
- AWS EC2 : memory 1GiB
- EC2에서 쓰는 운영체제 : Linux Redhat (apt-get >>yum)

# AWS 시작하기
1. key 압축 해제
2. ssh -i letsrunpark-id_rsa ec2-user@18.218.142.199
> /home/~
> /home/~/data : csv 파일 존재
> /tmp : 테스트 코드들 있음

## Mac Error
- sudo chmod 400 letsrunpark-id_rsa
- 비밀번호 : Local PC Password

-------------------------------

# 파일 이동 to cloud!
- scp -i letsrunpark-id_rsa <myfile> ec2-user@18.218.142.199:/tmp
> ex) scp -i letsrunpark-id_rsa temp_race_send.py ec2-user@18.218.142.199:/tmp

-------------------------------

# Git 사용법

- 원격 저장소에서 로컬 저장소로 불러오기
1. git clone <주소>

- 로컬 저장소에서 원격 저장소에 저장하기
1. git add .
2. git commit -m "무슨 내용 commit할 지 간단한 멘트"
3. git push origin master

-------------------------------


# 모듈 설치
- pip3 install modulename --user

# 코드 실행
- python3 /tmp/filename.py

-------------------------------

# Crontab 사용법

### crontab 내용 편집하기
- crontab -e
> crontab editor 실행하기

- i = 편집모드
- esc , :wq = 편집 종료 후 저장


- crontab -l
> crontab list 보기

- crontab -r
> crontab 내용 삭제

### crontab 문법

1. __minute hour day month yoil command__
2. __5 * * * * mkdir test-dir__
> __* 시 5분에 mkdir test-dir__

3. __*/2 * * * * rmdir test-dir__
> __2분마다 rmdir test-dir__

-------------------------------


# MySQL
- workbench 통해서 들어가기 & Query 작성
- hostname= 18.218.142.199 / port=3306 / pw=

> local에서 EC2로 파일 업로드할때 filezila 이용하면 편하다!

# mysql에 csv 파일 업로드할 때(현세가 알려준 명령어)
로그인할 때 : mysql --local-infile -uroot -p

-------------------------------
# 참고

[Colab YouTube](https://www.youtube.com/watch?v=XRBXMohjQos&t=)

[Colab 용량, 제약사항](https://colab.research.google.com/drive/151805XTDg--dgHb3-AXJCpnWaqRhop_2#scrollTo=gsqXZwauphVV)


[MarkDown 사용법](https://heropy.blog/2017/09/30/markdown/)
