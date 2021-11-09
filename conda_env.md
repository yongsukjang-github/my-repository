콘다 가상환경 만들기

아나콘다를 가상환경을 만들기 위해 폴더를 생성해 준다.
만든 폴더를 vsc 시작할 때 open_folder에서 열어준다.

1. 아나콘다 버전 확인
conda -V

2. 아나콘다 가상환경 생성
conda create -n 가상환경 이름 python=3.7 anaconda

3. 아나콘다 가상환경 리스트
conda info --envs 

4. 가상환경 활성화
activate 가상환경 이름

5. 스크립트 생성
vsc 화면에서
command + shift + p
-. python : command + shift + p > python: select interpreter > enter > 해당 가상환경 > enter
-. 스크립트 : command + shift + p > jupyter: create new blank notebook > enter

5. 가상환경 종료(비활성화)
conda.bat deactivate

6. 만들어 놓은 가상환경 완전 삭제
conda remove -n 가상환경 이름 -all

7. 라이브러리 설치
-. 라이브러리 리스트 확인
conda list

-. 가상환경에 라이브러리 설치
해당 가상환경이 activate 되어있어야함.(4번 참고)
conda install 라이브러리명

-. 라이브러리 설치 안될 때
conda install -c conda-forge 라이브러리명

8. 가상환경 복사하기
conda create -n 복사된_가상환경이름 --clone 복사할_가상환경이름


