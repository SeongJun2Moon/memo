- 타입체크 


    print(f'type {type(self.iris)}')
### error: (-215:Assertion failed) !empty() in function
> 원인
>>- haarcascade_fronface.xml이 프로젝트 파일에 없을 때
>>- 경로가 잘못됨

> 해결
>> 두 번째의 경우 *params 순서가 잘못됨(아래 코드로 확인) 
> 
    if param.size == 0:
    print("### param is null ### ")
    else :
    print(" ### param is not null ### ")

### 
> 원인
>>- df에 int와 str이 섞여서

> 해결
>>  regex 사용 <p> (self.seoul_crime[cols].str.replace(',', '')을 쓰는 방법도 있지만 불필요한 루프가 생겨서 효율x)
> 
    self.seoul_crime = pd.read_csv('./data/crime_in_seoul.csv')
    cols = ['절도 발생', '절도 검거', '폭력 발생', '폭력 검거']
    self.seoul_crime[cols] = self.seoul_crime[cols].replace(',', '', regex=True).astype(int)
참고한 내용 : <a href>https://acdongpgm.tistory.com/166

### MySQL 요구 버전 or later is required (found 현재 버전).
> 원인 
>> 버전 이슈

> 해결
>> - 지금 버전 지우고 요구 버전으로
>> - docker에서는 sql 백업 후 업데이트 

### django.db.utils.OperationalError: (2005, "Unknown server host 'mysql-container' (11001)")
> 원인
>> 호스트 명이 잘못됨

> 해결
>>  ATABASES = {
    "default": {
        "ENGINE": "django.db.backends.mysql",
        "NAME": "mydb",
        "USER": "root",
        "PASSWORD" : "root",
        "HOST": "localhost",
        "PORT": "3306"
    }
}<p>처럼 "HOST" : "호스트명"을 바꿔준다

### OMP: Error #15: Initializing libiomp5md.dll, but found libiomp5md.dll already initialized.
> 원인
>> 라이브러리 충돌

> 해결
>> libiomp5md.dll이 기실행중
>> 재부팅으로 중지되지 않으므로 model load하는 부분의 .py나 노트북 상단에 os를 통해 중복 실행 허용

    import os
    os.environ['KMP_DUPLICATE_LIB_OK']='True'

### 이미지 생성모델 미출력
> 원인 
>> 뭐겠어

> 해결
>> plt.show()를 안했다

### RuntimeError: Input type (torch.cuda.FloatTensor) and weight type (torch.FloatTensor) should be the same
> 원인
>> 디바이스 경로 에러

> 해결
> >>

### Python TypeError: 'int' object is not subscriptable
> 원인
>> 리액트-장고 연결된 상태에서 GET과 POST의 onClick 모양이 다른데 GET의 내용을 POST에도 그대로 적용해서 생긴 문제

> 해결1
>>  GET이 아래 모양이면</br>
    const onGetClick = e =>{
        e.preventDefault()
        getfashion(id)
        .then((res)=>{
            alert(`카테고리 : ${JSON.stringify(res.data.result)}`)
        })
        .catch((err)=>{
            console.log(err)
            alert('실패')
        })
    }
> 
> POST는 아래처럼 코드를 추가해준다
>
>>  const onPostClick = e =>{</br>
    e.preventDefault()</br>
    <a style=color:red>const request = {id} </br>
    postfashion(request) </a></br>
    .then((res)=>{
        alert(`카테고리 : ${JSON.stringify(res.data.result)}`)
    })
    .catch((err)=>{
        console.log(err)
        alert('실패')
    })
}

### Method Not Allowed: /shop/iris/iris
### ValueError: set_wakeup_fd only works in main thread of the main interpreter
