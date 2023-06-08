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

<python 가상환경 구동 방법>

+ 프로젝트 진행 및 관리를 위하여 기존 python 환경과 격리된 가상환경을 venv를 활용하여 생성
+ Python 3.5 버전 이후부터는 venv가 python 표준 라이브러리에 내장되어 있기 때문에 따로 설치할 필요 없음

1. cmd에서 다음과 같이 가상환경을 생성한
![image](https://github.com/kkyun1212/opensw23-team1/assets/81912226/03f2d937-f6c2-4f84-b405-f4e77850180e)
+ 위 코드가 제대로 실행되었다면 생성한 가상환경 이름으로 폴더가 생성되었을 것이다 (본 프로젝트에서는 myenv로 설정)

2. 가상환경 활성화를 위해 다음과 같이 입력한다
![image](https://github.com/kkyun1212/opensw23-team1/assets/81912226/108b20bd-8bcd-4705-9690-aa80c560a727)
+ (본 프로젝트에서는 C:\venv>myenv\Scripts\activate로 설정)
+ deactivate 명령으로 가상환경 비활성화 가능

<가상환경 내에서 오픈소스 실행>

![image](https://github.com/kkyun1212/opensw23-team1/assets/127182516/9972fc9c-9e0f-4180-b138-ffe231bf30fd)

1. C드라이브에 파이썬 가상환경을 requirement.txt에 맞는 3.7 이상 version으로 구동(venv 사용)

2. github에서 git clone으로 가상환경 안에 Open Source Software 불러오기

3. Window 환경에 맞는 FFMPEG 설치 사이트 [ffmpeg 설치 사이 링크](https://www.gyan.dev/ffmpeg/builds/)

->FFMPEG 파일 [ffmpeg설치](https://www.gyan.dev/ffmpeg/builds/ffmpeg-release-essentials.7z) C드라이브에 압축 풀고 설치

시스템 환경 변수 편집-> 환경 변수 -> Path에서 새로 C:\ffnpng\bin 경로 추가(이건 압축 파일 풀때 실수로 ffnpng로 저장함. ffnpng는 파일 이름임 헷갈리지 마세요)

![image](https://github.com/kkyun1212/opensw23-team1/assets/127182516/90758f70-1fc8-4566-ad0d-fd635c6e9503)

![image](https://github.com/kkyun1212/opensw23-team1/assets/127182516/48a3cc98-9b3d-44a2-b4b4-cae5a86786d4)

4.파이썬 가상환경에서 ffmpeg 실행.(안될 시 재부팅 후 재확인 필요, 파일 없을 시 재설치)

![image](https://github.com/kkyun1212/opensw23-team1/assets/127182516/74fcf070-fbb3-415e-a546-2a604273826e)

![image](https://github.com/kkyun1212/opensw23-team1/assets/127182516/3a8ca668-d9e9-4bee-97ec-0bd3ab2d9eb0)

위와 같이 python 가상환경으로 이동할 수 있다.

5.PyTorch 사이트 [Pytorch 사이트 링크](https://pytorch.org/get-started/locally/)에서 Pytorch 최신 버전 Command 복사하여 가상환경에 설치

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


저희 팀이 생성한 dataset 파일입니다. 두 명의 목소리를 sample file로 녹음하였습니다.


첫 번째 dataset input file은 다음 5개의 파일입니다.


https://github.com/kkyun1212/opensw23-team1/assets/81912226/4d575307-634f-4f97-b1c6-04c366e7dcdc



https://github.com/kkyun1212/opensw23-team1/assets/81912226/0a8087ee-2c05-409f-85ee-c3bb4ac1e110



https://github.com/kkyun1212/opensw23-team1/assets/81912226/a610462e-23d9-453c-908c-a2b20f15b9cc



https://github.com/kkyun1212/opensw23-team1/assets/81912226/53c7f974-05e2-4ed9-b480-29f57cca9886



https://github.com/kkyun1212/opensw23-team1/assets/81912226/2a38110f-1f95-44a5-8b65-207211220b43



https://github.com/kkyun1212/opensw23-team1/assets/81912226/e64522ae-7d16-4630-9654-b36342b38268


첫 번째 dataset에 대한 output 파일입니다.


https://github.com/kkyun1212/opensw23-team1/assets/81912226/ee2b2d52-41c0-4fa6-b8ef-3cef85d109bf




두 번째 dataset input file은 다음과 같습니다.


https://github.com/kkyun1212/opensw23-team1/assets/81912226/a9d12dad-16e9-4856-880e-f22200272db7



https://github.com/kkyun1212/opensw23-team1/assets/81912226/64e6fedb-4f69-44fe-bfa6-160ab10b1c11



https://github.com/kkyun1212/opensw23-team1/assets/81912226/5362b006-b00c-4e7c-b4cb-cf6342c0fc74



https://github.com/kkyun1212/opensw23-team1/assets/81912226/c57b543c-91ce-4ce4-ab09-d6b37c00cc05



https://github.com/kkyun1212/opensw23-team1/assets/81912226/9bac91cd-02e4-4f5b-8e00-5a2eeb481909



https://github.com/kkyun1212/opensw23-team1/assets/81912226/0269e901-63ea-4773-98b1-63570550a462


두 번째 dataset에 대한 output 파일입니다.


https://github.com/kkyun1212/opensw23-team1/assets/81912226/4cf8cd77-6d3c-4257-9f97-27102a0080cb




두 목소리를 synthesis한 결과 graph입니다.

![image](https://github.com/kkyun1212/opensw23-team1/assets/81912226/6c8c0bf7-ce4a-4578-b338-090446314d24)


------------

## Analysis/Visualization

------------


# Presentation
[Real-TIme-Voice-Cloning_Presentation.pdf](https://github.com/kkyun1212/opensw23-team1/files/11684700/Real-TIme-Voice-Cloning_Presentation.pdf)
