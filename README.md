# opensw23-team1


## Team Introduction


+ 202211326 윤서진 - 발표


+ 202111367 정서현 - 깃허브


+ 202211374 정현민 - 조장


+ 202211362 장익준 - 코더

------------

## Topic Introduction
### Real-Time Voice Cloning

이 repository는 real-time으로 작동하는 vocoder를 사용하여 speaker verification을 통해 multispeaker TTS(text-to-speech) synthesis로 transferring하는 작업을 구현한 것입니다.


<img width="639" alt="image" src="https://github.com/kkyun1212/opensw23-team1/assets/81912226/ff660655-ce46-4892-aee6-3bf00fa51d5a">

Input으로 any voice file과 원하는 text를 입력하면

Ouput으로는 input으로 입력된 voice file과 동일한 voice로 입력한 text를 speech하는 audio file이 출력됩니다.

------------

## Installation

<Window 10 환경에서 Python 3.9.13 버전으로 구동>

<python pip version: 22. 0. 4>

![image](https://github.com/kkyun1212/opensw23-team1/assets/127182516/9972fc9c-9e0f-4180-b138-ffe231bf30fd)

1. C드라이브에 파이썬 가상환경을 requirement.txt에 맞는 3.7 이상 version으로 구동(venv 사용)

2. github에서 git clone으로 가상환경 안에 Open Source Software 불러오기

3. Window 환경에 맞는 FFMPEG 설치 사이트(https://www.gyan.dev/ffmpeg/builds/)

->FFMPEG 파일(https://www.gyan.dev/ffmpeg/builds/ffmpeg-release-essentials.7z) C드라이브에 압축 풀고 설치

시스템 환경 변수 편집-> 환경 변수 -> Path에서 새로 C:\ffnpng\bin 경로 추가(이건 압축 파일 풀때 실수로 ffnpng로 저장함. ffnpng는 파일 이름임 헷갈리지 마세요)

![image](https://github.com/kkyun1212/opensw23-team1/assets/127182516/90758f70-1fc8-4566-ad0d-fd635c6e9503)

![image](https://github.com/kkyun1212/opensw23-team1/assets/127182516/48a3cc98-9b3d-44a2-b4b4-cae5a86786d4)

4.파이썬 가상환경에서 ffmpeg 실행.(안될 시 재부팅 후 재확인 필요, 파일 없을 시 재설치)

![image](https://github.com/kkyun1212/opensw23-team1/assets/127182516/74fcf070-fbb3-415e-a546-2a604273826e)

![image](https://github.com/kkyun1212/opensw23-team1/assets/127182516/3a8ca668-d9e9-4bee-97ec-0bd3ab2d9eb0)

위와 같이 python 가상환경으로 이동할 수 있다.

5.PyTorch 사이트(https://pytorch.org/get-started/locally/)에서 Pytorch 최신 버전 Command 복사하여 가상환경에 설치

![image](https://github.com/kkyun1212/opensw23-team1/assets/127182516/ab3b595d-a48e-46da-9d83-11c7cd27f413)

6.clone한 파일로 가서 pip install -r requirements.txt 실행 (오류 발생 시 wheel 패키지 설치되지 않았을 확률 높음. pip install wheel로 오류 해결필요)
    
![image](https://github.com/kkyun1212/opensw23-team1/assets/127182516/97fc40f6-7a1c-4153-9aed-e89c0eb1626a)

![image](https://github.com/kkyun1212/opensw23-team1/assets/127182516/c1d993e3-4722-418c-ad51-779c463641f4)

실행 후 pip list로 설치되었는지 확인.

![image](https://github.com/kkyun1212/opensw23-team1/assets/127182516/5939c368-580a-4dca-a5ce-92b9d65c370c)

(설치 중에 추가로 필요한 패키지는 별도 설치 필요.)

7.명령 프롬포트에 python demo_cli.py 입력하여 python 프로그램이 잘 작동되는지 확인.

![image](https://github.com/kkyun1212/opensw23-team1/assets/127182516/3a2d8b07-58b3-4856-b8a8-a97587f65b9c)

8.명령 프롬포트에 python demo_toolbox.py 입력하여 프로그램 실행.

![image](https://github.com/kkyun1212/opensw23-team1/assets/127182516/59c13512-7305-494d-ae5d-ec4cf4d17a33)

![image](https://github.com/kkyun1212/opensw23-team1/assets/127182516/9832d2b5-f97e-4258-9b55-021d8968ffe6)

(사용 방법: 유튜브 영상참고 [Real-Time Voice Cloning Toolbox - YouTube](https://www.youtube.com/watch?v=-O_hYhToKoA))



------------

## Results

input voice file입니다.

https://github.com/kkyun1212/opensw23-team1/assets/127182516/805f22e7-9524-451f-ab4f-040ec8450fb9


input에 대한 output voice file입니다.

https://github.com/kkyun1212/opensw23-team1/assets/127182516/67c4df93-4670-45c3-9d5f-6222f2672e4d

------------

## Analysis/Visualization

------------


# Presentation
