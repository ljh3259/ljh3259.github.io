# vim에디터를 사용하기 쉽게 수정하라

## vim 에디터를 설정하려면 ?
- ~/.vimrc 파일을 수정하면된다
- 없으면 만들고 작성만 하면된다.

## 설정하다가 알게된 점
- set mouse=a 적용하면 마우스로 드래그하는 순간 visual 모드로 변환 된다.
- system clipboard 사용이 안된다.
- mouse 옵션을 제거했다.

```vim
  1 set number " 라인 넘버 보이도록
  2 
  3 " Syntax Highlighting
  4 if has("syntax")
  5     syntax on " 
  6 endif
  7 
  8 set autoindent
  9 set cindent
 10 
 11 set tabstop=4
 12 set shiftwidth=4
 13 
 14 set linebreak
 15 set showbreak=+++\ " 줄바꿈이 일어난 라인일경우 표기해준다
 16 
 17 set hlsearch " 검색결과에 강조표시를해준다
 18 set nocp " vi와의 호환여부 설정
 19 set ignorecase   " 검색시 대소문자 무시 (소문자로도 대문자 검색 가능)
 20 set smartcase    " 검색어에 대문자가 포함되어 있다면 대소문자를 무시하지 않는다
 21 
 22 set incsearch " 검색어를 한글자 입력할때마자 찾아준다
 23 set laststatus=2 " status 라인을 표기한다. 수정이 일어나면 [+] 로 변하네
```