## 소스 / 리소스
- 가공 전인 리소스를 가공 후인 소스로 바꿔주는 텍스트 파일이 소스코드
- src 내부의 파일은 소스(여기가 우리의 본진)
- 나머지는 리소스
---
## 도구, 시스템, 서버
- IDE(개발환경) : 도구+언어 
- 도구(또는 시스템) → 개발 환경을 구축하는 시스템, 언어에 의존해서 시스템을 개발(배포 후에는 사라진다)<div>
- 서버 → 클라이언트의 요청에 의해 서비스를 제공하는 시스템. 즉, 서버와 클라이언트는 상황에 따라 달라진다<div>
- 시스템 → 개발 환경을 통해 구축한 서버와 클라이언트 → 결국 서버와 클라이언트의 본질<div>

    > 서버인지 클라이언트인지는 결국 역할에 따라 달라진다

> 프로젝트를 진행한다 = 도구와 언어를 이용해 시스템을 만드는 것<p>

- request와 response는 본질은 같지만 방향만 다르다 (동시에 한 공간에 있을 수 없다)

---
## 라이브러리와 프레임워크의 차이
- 라이브러리
  - 모듈과 패키지의 집합
    - 패키지(컴파일언어) - (인터프리터 언어는 디렉토리 사용-> 프로젝트는 디렉토리를 사용)
      - 모듈들을 하나의 상위 폴더에 있다
      - 패키지 안에 여러가지 폴더가 있을 수 있다
    - 모듈 : 재사용이 가능한 클래스의 집합
- 프레임워크
  - 작업의 구조가 정해진 라이브러리 → 제어흐름을 갖는 시스템
  특정 문제 해결을 위해 상호 협력하는 클래스와 인터페이스의 집합으로 프로그래머의 작업이 필요
> 차이점
> - 코드의 <a style=color:rgb(178,102,255)>제어 흐름</a>
>   - 흐름이 사용자에게 있으면 라이브러리, 시스템에게 있으면 프레임워크
>   - 라이브러리는 사용자가 객체나 함수를 <a style=color:red>직접 호출</a>
>   - 프레임워크는 프레임워크에 의해 메서드가 호출<p>
>>  제어흐름 : 프로그램에서 실행되는 함수가 <a style=color:rgb(178,102,255)> 호출되는 순서</a>

> 둘의 구분은 개발자의 손을 탔는지가 아니라 

명칭 그대로 도서관에서 필요한 파일(패키지)과 문서(모듈)를 꺼내서 다른 곳에 옮겨적는 것처럼 사용자에게 제어 흐름이 있고
프레임워크는 건축의 뼈대처럼 정해진 틀 안에서 작업을 수행해야하기 때문에 프레임워크에게 제어 흐름이 있다?

## prefix(접두사) / postfix

## 인조키
- 시퀀스
- uuid

---
## 이미지 / 컨테이너
## 상태(state)값과 설정(context)값(-it)
- 상태 : 변하냐 변하지 않냐의 차이
  - 변하는 상태는 상태값, 변하지 않는 상태는 설정값
  - 파라미터와 아규먼트는 각각 설정값과 상태값 중 뭘 가지나?
- 파이썬 입장에서 이미지는 class, 컨테이너는 인스턴스, 도커는 파일, 디렉토리는 설정값, 패키지는 상태값
- 설정값 오류가 났을 때는 rm 후 도커파일의 설정값을 다시 설정한다. 
- 메인영역의 메타데이터는 변경이 없지만 서브 영역은 상태가 변한다
> ※ 설정값은 상수가 아님을 기억해라

---

## Ayomic Pattern
- Atom → Molecule → Organism → Template → Page
    > 기본적으로 하위 개념은 상위 개념의 컴포넌트고 상위 개념은 하위 개념의 컨테이너
    >> 여기서는 원자, 분자, 유기체를 컴포넌트, 템플릿을 컨테이너로
    
#### Atom
- 가장 작은 단위의 컴포넌트
- 어떤 설정값이 주어져도 생성되어야해서 다양한 상태값을 가지고 있어야한다
- 마진이나 위치값을 가지지 않는다
 
---
## work, job, task

---
## 관계
#### 연관 관계

#### 상관 관계

#### 의존 관계