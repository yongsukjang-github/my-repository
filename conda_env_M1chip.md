# M1에서 tensorflow 설치 시 주의사항

기존 환경구성은 anaconda 기반이었습니다.

하지만, M1에서 tensorflow를 설치하기 위해서는 현재는 miniforge 에서만 호환된다고 합니다.

저는 기존에 anaconda가 설치되어 있었고, 충돌이 생길 수 있어 anaconda를 지우고 miniforge를 설치했습니다.

1. anaconda uninstall

    ```terminal
    % cd
    % sudo rm -rf anaconda
    % sudo rm -rf .anaconda_backup
    % sudo rm -rf ~/.condarc ~/.conda ~/.continuum
    ```

    경로도 삭제해줍니다.

    ```terminal
    % open -e .bash_profile
    % open -e .zshrc
    ```

    마지막으로 anaconda가 설치되어있는 폴더도 삭제해줍니다.

    ```terminal
    % opt/anaconda3
    ```

2. miniforge 설치

    homebrew 없으면 설치해 줘야합니다.

    ```terminal
    % brew install miniforge
    ```

    terminal에서 init 해줍니다.

    ```terminal
    % conda init bash
    % conda init zsh
    ```

    bash_profile과 zshrc 파일에서 경로가 miniforge로 되어있는지 확인합니다.

    ```terminal
    % open -e .bash_profile
    % open -e .zshrc
    ```

3. conda env 생성

    ```terminal
    % conda info --envs
    % conda create -n "가상환경이름" python=3.8
    % conda activate 가상환경이름
    ```

4. tensorflow 설치

    ```terminal
    % conda install tensorflow
    ``
