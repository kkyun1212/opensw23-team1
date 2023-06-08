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



### <python 가상환경 구동 방법>

+ 프로젝트 진행 및 관리를 위하여 기존 python 환경과 격리된 가상환경을 venv를 활용하여 생성
+ Python 3.5 버전 이후부터는 venv가 python 표준 라이브러리에 내장되어 있기 때문에 따로 설치할 필요 없음

1. cmd에서 다음과 같이 가상환경을 생성한
![image](https://github.com/kkyun1212/opensw23-team1/assets/81912226/03f2d937-f6c2-4f84-b405-f4e77850180e)
+ 위 코드가 제대로 실행되었다면 생성한 가상환경 이름으로 폴더가 생성되었을 것이다 (본 프로젝트에서는 myenv로 설정)

2. 가상환경 활성화를 위해 다음과 같이 입력한다
![image](https://github.com/kkyun1212/opensw23-team1/assets/81912226/108b20bd-8bcd-4705-9690-aa80c560a727)
+ (본 프로젝트에서는 C:\venv>myenv\Scripts\activate로 설정)
+ deactivate 명령으로 가상환경 비활성화 가능

### <가상환경 내에서 오픈소스 실행>

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


### <파이썬 코드로 실행 process>

![image](https://github.com/kkyun1212/opensw23-team1/assets/81912226/04ab3ec0-50b0-43b6-ae86-1eadcb33a827)

1. 먼저 위의 실행 방법을 통해 demo_toolbox.py 코드를 실행하면 사진과 같이 python 프로그램이 실행된다.
이때 Browse는 파일을 불러오는 버튼이고, Record는 마이크로 직접 녹음하는 버튼, Play와 Stop은 불러온
파일이나 녹음된 파일을 재생하고 중지하는 버튼이다. 또한 Export 버튼은 Voice-Cloning을 통해 생성된
파일을 저장하는 버튼이다.
    
또한 Synthesize and vocode는 파이썬 소스코드를 실행하여 불러온 녹음 파일을 clone된 목소리로 변환하고    text를 읽게 하는 버튼이다. 이때 text의 길이나 언어는 자유롭게 설정할 수 있으나, 본 프로젝트에서는 accuracy를 높이기 위하여 English로 실행하였다. Synthesize only와 Vocode only 버튼을 이용하여 Synthesize와 vocode중 하나만 실행할 수도 있다.

    
![image](https://github.com/kkyun1212/opensw23-team1/assets/81912226/cb285272-4ae3-4d4a-9f98-cc990dd5cfe8)

2. Browse를 클릭하여 파일에서 음성 녹음 파일을 선택한 후 Play를 클릭하여 해당 파일을 실행해보고 올바른 파일을 불러왔는지 확인한다. 이후 Synthesize and vocode를 클릭하여 파이썬 프로그램을 실행한다.
    
![image](https://github.com/kkyun1212/opensw23-team1/assets/81912226/ca30ccba-7faf-4407-846a-0bddddc419eb)
(실행 중인 사진)
    
3. 실행이 완료되면 clone된 목소리로 text를 읽는 음성파일이 생성된다. Export 버튼을 클릭하여 파일에 Voice-Cloning된 녹음 파일을 저장한다.
    
![image](https://github.com/kkyun1212/opensw23-team1/assets/81912226/ed1fa141-b22a-4b25-a874-2806ebe7e44f)

4개 이상의 dataset이 생성되면 다음과 같이 왼쪽에 Sample과 Voice-Cloning된 녹음 파일의 정확도를 나타내는 graph가 생긴다. 프로그램이 잘 실행되었다면 시행을 계속할 수록 Cluster가 한 점으로 모이게 된다.
    
    
(참고: Real-Time Voice Cloning Toolbox - YouTube https://www.youtube.com/watch?v=-O_hYhToKoA)
    
------------

## Results


저희 팀이 생성한 dataset 파일입니다. 두 명의 목소리를 sample file로 녹음하였습니다.


첫 번째 dataset input file은 다음 6개의 파일입니다.



https://github.com/kkyun1212/opensw23-team1/assets/81912226/0448c587-61ee-4c19-a120-f9fa360ce8ae



https://github.com/kkyun1212/opensw23-team1/assets/81912226/300e2623-e267-4f21-aabe-d5043227eb56



https://github.com/kkyun1212/opensw23-team1/assets/81912226/814ba6ca-d7a8-4990-a579-039a1846139c



https://github.com/kkyun1212/opensw23-team1/assets/81912226/59b250d3-e561-4027-b803-a6d99067013a



https://github.com/kkyun1212/opensw23-team1/assets/81912226/23a03a6c-9d45-4ec9-a53e-420a23423be3



https://github.com/kkyun1212/opensw23-team1/assets/81912226/e3f6b70f-cba8-4e40-a9d7-7afa96208922




첫 번째 dataset에 대한 output 파일입니다.



https://github.com/kkyun1212/opensw23-team1/assets/81912226/ee00b359-5aeb-424b-a3d4-86775de2b38a





두 번째 dataset input file은 다음과 같습니다.


https://github.com/kkyun1212/opensw23-team1/assets/81912226/3b09249a-0257-4c15-8ec8-e1a4125aab66



https://github.com/kkyun1212/opensw23-team1/assets/81912226/96354cc1-32b5-453e-8715-3deccf64cd67



https://github.com/kkyun1212/opensw23-team1/assets/81912226/5ba569ed-6bb5-4ad4-935d-cec9d19b3ab8



https://github.com/kkyun1212/opensw23-team1/assets/81912226/c0d079be-a19e-4a1a-afdd-c058b4cd2cec



https://github.com/kkyun1212/opensw23-team1/assets/81912226/b0cd746a-df77-4649-b9b1-b805c64e6b9c



https://github.com/kkyun1212/opensw23-team1/assets/81912226/6ec4cfde-816b-405f-8b87-5c0f84530676




두 번째 dataset에 대한 output 파일입니다.



https://github.com/kkyun1212/opensw23-team1/assets/81912226/6807e3b6-8e03-457a-ba52-70153a1d8c71






------------

## Analysis/Visualization

### mel-spectrogram 에 대한 간단한 설명

가로축은 시간, 세로축은 주파수, 색상은 데시벨을 나타냄

→ 목소리와 오디오 파일을 분석하는데 이용

첫 번째 dataset input file에 대한 mel-spectrogram 입니다

![image](https://github.com/kkyun1212/opensw23-team1/assets/127182516/947d1815-7e9a-461f-bc11-8d8cd2715d5e)

![image](https://github.com/kkyun1212/opensw23-team1/assets/127182516/3a58a8b6-784a-4ab6-ad65-a2311db23e86)

![image](https://github.com/kkyun1212/opensw23-team1/assets/127182516/d1bf474f-ce5d-4995-aad3-6432323385a6)

![image](https://github.com/kkyun1212/opensw23-team1/assets/127182516/82e24100-757c-433a-b006-e8149caa9d22)

![image](https://github.com/kkyun1212/opensw23-team1/assets/127182516/093474d7-6d30-4583-b705-2e7ce9d3af2b)

![image](https://github.com/kkyun1212/opensw23-team1/assets/127182516/7665fd1d-51ca-4690-a469-2c2b3f46008f)

    
두 dataset을 synthesis한 결과 graph입니다.

![image](https://github.com/kkyun1212/opensw23-team1/assets/81912226/6c8c0bf7-ce4a-4578-b338-090446314d24)

원은 input을 x는 output을 나타냅니다.
같은 목소리가 각각 모여있고 output도 dataset 주변에 생성됨을 볼 수 있습니다.

------------


# Presentation

[Presentation 자료](https://curly-motorcycle-5f2.notion.site/Real-Time-Voice-Cloning-095f7b8d07b841a199ebc1cfab69a1a4?pvs=4)

[Presentation Video Link](https://youtu.be/e6nONIABYGA)
