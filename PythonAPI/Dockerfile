FROM ubuntu:20.04

ENV TZ="Asia/Seoul"
# 환경 설정 (질의응답 뜨지 않게 함)
ENV DEBIAN_FRONTEND=noninteractive

# 파이썬 설치와 함께 pip도 설치
RUN apt-get update -y && \
    apt-get install -y python3.10 python3-pip

# pandas와 pymysql 패키지 설치
RUN pip install pandas pymysql requests

# 지금은 자동 업로드 하면 안된다.
CMD ["/bin/python3", "/code/api.py"]


# 도커 명령어
# sudo docker build .
# docker tag 0dd35d6c2c89 python:api
# sudo docker run -v /media/sunjin:/Drive -v /home/sunjin/AICCTV_DB/code:/code -d --name AICCTV_API --restart=always --log-driver=json-file --log-opt max-size=1m python:api

#AICCTV_Raw_To_DB: 

    # 첫번째 컨테이너에서만 이미지를 빌드한다
    #############################
#    build:
#      context: ./PythonImage
#      dockerfile: Dockerfile
#    image: "python3.10:db"
    #############################

#    logging:
#      driver: "json-file"
#      options:
#        max-size: "1m"
#        max-file: "3"