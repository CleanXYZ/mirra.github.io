# [ 목차 ]
### 1. [컨셉](#1)
### 2. [관련 이미지와 동영상](#2)
### 3. [대표 이미지](#3)
### 4. [게임설명](#4)
### 5. [게임 시스템 디자인](#5)
### 6. [요구사항](#6)
### 7. [요구사항(N주차)](#7)

# Mirra

# [컨셉] <a name='1'></a>

## 메인컨셉 : 성장

- 플레이어는 미라를 조정하면서 적을 죽여 끝까지 살아남기

### 서브 컨셉 1 :다양한 공격 스킬

- 다양한 공격스킬로 적을 죽일 수 있음
<br><br>

# [관련 동영상] <a name='2'></a>

- 동영상
- [![예제](http://img.youtube.com/vi/KQWwXvCtyIs/0.jpg)](https://youtu.be/KQWwXvCtyIs) 

<br><br>

# [대표 이미지] <a name='3'></a>

![그림](/image/뱀서.png)

<br><br>

# [<게임제목> Mirra Survival] <a name='4'></a>

- 모든적을 죽이고 끝까지 살아남기
<br>

## 1. 이야기

[만들게 된 배경]  
최근 뱀파이어서바이벌을 하는것에 빠져서 하다가 이게임을 3D로 만들고 싶었다.

[카메라 관점]  
3D 탑뷰

<br>

## 2. 미적요소

[디자인][컬러]  
사막와 어울리는 색 1

[음향]  
사막와 어울리는 음악
<br>

## 3. 기술

Unity 사용

# [게임 시스템 디자인] <a name='5'></a>

1. 게임 오브젝트 분해 (구성 요소 분석)

|연번|오브젝트 이름|오브젝트 이미지|
|:----:|:----:|:----:|
|1|주인공|<img src="./image/미라.png" width="300" height="300">|
|2|적1|<img src="./image/슬라임.png" width="300" height="300">|
|3|적2|<img src="./image/거북이.png" width="300" height="300">|

2. 파라미터(속성) 뽑아 보기

1) 오브젝트 이름 : 주인공

|속성|영문명칭|설명|비고|
|:----:|:----:|:----:|:----:|
|이동속도|main_speed|주인공의 속도를 결정한다||
|체력|main_hp|주인공의 체력을 결정한다||
|점수|main_score|주인공이 적을 처치시 획득하는 점수||

2) 오브젝트 이름 : 적

|속성|영문명칭|설명|비고|
|:----:|:----:|:----:|:----:|
|이동속도|speed|적 물고기의 이동속도를 결정한다||
|체력|hp|적 물고기의 체력을 결정한다||

3. 행동 뽑아 보기

1) 오브젝트 이름 : 주인공

|행동|설명|
|:----:|:----:|
|이동|방향키로 이동한다|
|사망|hp가 0이 될 경우 게임이 종료된다|

2) 오브젝트 이름 : 적

|행동|설명|
|:----:|:----:|
|공격|주인공이 일정거리안으로 들어오면 공격한다|
|이동|주인공에게 이동한다|
|스폰|맵 상하좌우 스폰지점에서 스폰한다|
|소멸|hp가 0이 될 경우 점수가 증가한다|

4. 상태 뽑아 보기

1) 오브젝트 이름 : 주인공

|현상태|전이상태|전이조건|
|:----:|:----:|:----:|
|멈춤|이동|플레이어가 방향키를 누를때|

2) 오브젝트 이름 : 적

|현상태|전이상태|전이조건|
|:----:|:----:|:----:|
|X|생성|시간에따라 생성됨|
|생성|이동|생성된후 주인공에게 이동함|
|이동|소멸|hp가 0이 될 경우 점수가 증가한다|
|이동|공격|일정범위 안으로 들어오면 주인공을 공격함|

5. 게임의 규칙

1) 핵심 규칙
- 죽을때까지 주인공은 적에게서 도망쳐서 처치하고 살아남는다.

2) 보조 규칙

-적을 처치하면 점수를 얻는다.

-적은 일정범위안으로 들어가면 공격한다.

# [요구사항] <a name='6'></a>

미라 서바이벌의 요구사항

- 캐릭터가 방향키에 따라 이동한다.
- 캐릭터에게서 자동적으로 공격이 나간다.
- 적이 스폰지역에서 생성되어 캐릭터를 쫒는다.
- 캐릭터의 공격에 맞은적은 데미지를 출력하며 맞는 애니이션이 나온다
- 시작화면, 점수화면 게임화면 총 3개의 화면이 있다.
- 종료 클릭시 게임이 종료된다.
- 점수보기 클릭시 점수화면으로 이동한다.
- 게임종료시 종료팝업이 뜬다. 종료팝업에는 플레이시간, 점수, 다시하기, 메인메뉴 버튼이 있다.
- 적을 처치하면 점수를 얻는다.

# [요구사항 N주차] <a name='7'></a>
  -1주차
    캐릭터의 기본적인 움직임과 이동
  
  -2주차
    AI, 적의 움직임과 행동
  
  -3주차
    AI, 적의 움직임과 행동
  
  -4주차
    맵제작 및 시스템
   


