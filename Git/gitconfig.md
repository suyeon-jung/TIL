# Git Config
- `git config` 도구로 설정 내용을 확인하고 변경할 수 있다. 
- Git은 설정에 따라 동작한다. 
- 사용하는 설정 파일은 3가지가 있다. 

## 설정 파일의 종류
1. `/etc/gitconfig` 파일 
    - 시스템의 <span style="color:#0052cc">모든 사용자</span>와 <span style="color:#0052cc">모든 저장소</span>에 적용되는 설정이다. 
    - `git config --system` 옵션으로 이 파일을 읽고 쓸 수 있다. 
    - 시스템 전체 설정 파일이기 때문에 수정하려면 시스템의 관리자 권한이 필요하다. 
2. `~/.gitconfig`, `~/.config/git/config` 파일
    - 특정 <span style="color:#0052cc">사용자</span>(현재 사용자)에게만 적용되는 설정이다. 
    - `git config --global` 옵션으로 이 파일을 읽고 쓸 수 있다. 
    - 특정 사용자의 모든 저장소 설정에 적용된다. 
3. `.git/config` 
    - <span style="color:#0052cc">현재 작업 중인 프로젝트(특정 저장소)</span>에만 적용된다. 
    - 현재 작업 중인 프로젝트 내 Git 디렉토리에 있는 설정 파일이다. 
    - `--local` 옵션을 사용하면 이 파일을 사용하도록 지정할 수 있다. 
    - 기본적으로 이 옵션이 적용되어 있다. 

## 설정의 우선순위
> `.git/config` > `~/.gitconfig`, `~/.config/git/config` > `/etc/gitconfig`
- 각 설정 파일에 중복된 설정이 있으면 위 순서대로 우선순위가 부여된다. 
- 즉, `.git/config` 와 `~/.gitconfig`에 같은 설정이 있다면 `.git/config`에 있는 설정이 적용된다. 
