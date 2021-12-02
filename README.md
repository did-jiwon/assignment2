# assignment2(20203187 컴퓨터공학과 양지원)

## vimgolf(1)
---
`GWi"<End>"<Esc>ZZ` `9번`
1) `G` : 맨 밑으로 이동
2) `W` : 오른쪽 한 단어의 끝 부분으로 커서 이동
3) `i` : 입력모드로 변환
4) `""` 입력
5) `ESC` : 일반 모드로 변환
6) `ZZ` : 저장하고 나가기
---

## vimgolf(2)
---
`:%s/sublime\|emacs/vim/g<CR>ZZ` `27번`
1) `:%s/sublime\|emacs/vim/g`
    * `sublime`과 `emacs` 둘 다 `vim`으로 치환하는 것이기 때문에 `|(파이프)`를 사용하여 동시에 명령어 처리가 될 수 있다.
    * `g` -> 전체에 적용
3) `ZZ` : 저장하고 나가기
---

## vimgolf(3)
---
`4GYPi// <Esc>WWCTODO<Esc>6GYPi// <Esc>WWCTODO<Esc>ZZ` `36번`
1) `4G` : 4번째 줄로 이동
2) `Y` : 현재 커서가 위치한 줄을 임시 버퍼에 복사
3) `P` : 현재 커서의 앞에 임시 버퍼에 복사된 내용 붙이기
4) `i` : 입력모드로 변환
5) `//` : 주석 직접 입력(:norm :i//보다 입력수가 적기 때문에)
6) `<Esc>` : 일반모드로 변환
7) `W` : 오른쪽 한 단어의 끝 부분으로 커서 이동
8) `C' : 현 커서에서 줄의 끝까지를 임의의 다른 내용으로 바꿈
9) `TODO` : TODO 직접 입력
10) `6G` : 6번째 줄로 이동
11) 위와 똑같이 실행
12) `ZZ` : 저장하고 나가기
---

## vimgolf(4)
---
`:%s/y1/abs(y1)/g<CR>/1<CR>r4<Up>r3<Up>r2<C-V><Down><Down>yn<C-V><Down><Down>p<C-V><Down><Down>yn<C-V><C-><Down><Down>p?k<CR>rb<Down>rr<Down>rgZZ` `60번`
![image](https://user-images.githubusercontent.com/66530743/144385868-758d197f-0522-4270-9fcd-8022cdb288fa.png)

***많은 시도를 했지만 60번에 최대였습니다....***

---
