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

![vimgolf_1__1](https://user-images.githubusercontent.com/66530743/144410213-a5f9e169-b4ac-4bcc-ab99-2478eb58df2c.gif)
---


## vimgolf(2)
---
`:%s/sublime\|emacs/vim/g<CR>ZZ` `27번`
1) `:%s/sublime\|emacs/vim/g`
    * `sublime`과 `emacs` 둘 다 `vim`으로 치환하는 것이기 때문에 `|(파이프)`를 사용하여 동시에 명령어 처리가 될 수 있다.
    * `g` -> 전체에 적용
3) `ZZ` : 저장하고 나가기

![vimgolf(2)](https://user-images.githubusercontent.com/66530743/144412594-0208e5a0-882a-4b52-9119-4d514b073e14.gif)

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
8) `C` : 현 커서에서 줄의 끝까지를 임의의 다른 내용으로 바꿈
9) `TODO` : TODO 직접 입력
10) `6G` : 6번째 줄로 이동
11) 위와 똑같이 실행
12) `ZZ` : 저장하고 나가기

![vimgolf_3_](https://user-images.githubusercontent.com/66530743/144411289-7c7a6dbb-27b5-4248-bbaa-e96c05230f07.gif)
---

## vimgolf(4)
---
`:%s/y1/abs(y1)/g<CR>/1<CR>r4<Up>r3<Up>r2<C-V><Down><Down>yn<C-V><Down><Down>p<C-V><Down><Down>yn<C-V><Down><Down>p?k<CR>rb<Down>rr<Down>rgZZ` `59번`

![image](https://user-images.githubusercontent.com/66530743/144385868-758d197f-0522-4270-9fcd-8022cdb288fa.png)

***많은 시도를 했지만 59번이 최대였습니다....***
1) `:%s/y1/abs(y1)/g` : y1을 abs(y1)으로 바꿈
2) `<CR>` : 엔터
3) `/1<CR>` : 앞에서부터 1찾기, <CR> -> x1으로 커서 이동
4) `r4` : 1을 4로 바꾸기(r->한글자 바꾸기)
5) `r3` : 1을 3로 바꾸기
6) `r2` : 1을 2로 바꾸기
7) `<C-V><Down><Down>` : 비주얼 블록모드로 열(2,3,4)를 선택
8) `y` : 열(2,3,4)복사
9) `n` : 1을 찾고있는 중이니 그 다음 1찾기, 3번째줄의 y1으로 커서 이동
10) `<C-V><Down><Down>p` : 비주얼 블록모드로 열(1,1,1)를 선택하여 붙여넣기
   11) `<C-V><Down><Down>y` : 열(2,3,4)를 선택하여 다시 복사
      * 다시 복사하지않고 #1로 가서 붙여넣으면 복사가 되지 않았음
   12) `n` : 다음 1로 이동(3번째줄의 #1으로 이동)
   13) `<C-V><<Down><Down>p` : 비주얼 블록모드로 선택 후 복사
   14) `?k` : 뒤에서부터 k탐색(/k로 하면 4번째줄의 k로 이동하지만 ?k로 하면 3번째줄의 k로 이동해서 커서움직임을 줄일 수 있음)
   15) `rb rr rg` : k를 b,r,g로 바꾸기
   16) `ZZ` : 저장하고 나가기

       ![vimgolf_4__1](https://user-images.githubusercontent.com/66530743/144410476-856cec29-60e5-42bf-bf1c-201eeaeabd3d.gif)
   
---

## vimgolf(5)
---
`5Gyw/"<CR>pa,name,age,score<Esc>ZZ` `27번`
   1) `5G` : 5번째 줄로 이동
   2) `yw` : 현재 커서가 위치에서 오른쪽으로 한 단어를 임시 버퍼에 복사(student_id 복사)
   3) `/" <CR>` : 앞에서부터 "을 찾고 그 위치로 이동
   4) `p` : 붙여넣기(student_id)
   5) `a` : 텍스트를 현재의 커서 위치 뒤에 추가(현재 커서 위치 : student_i**커서**d))
   6) `,name,age,score` : 이들은 복사해서 붙여넣는 것보다 직접 입력하는 것이 입력 횟수가 더 적음
   7) `<Esc>` : 일반 모드로 변경
   8) `ZZ` : 저장하고 나가기
   
   ![vimgolf_5_](https://user-images.githubusercontent.com/66530743/144410552-eb2aa412-4e44-4e80-8d83-1838005002c4.gif)
---
