# Java_0927  
  
  
  
### 해쉬맵  
  
리스트와 배열은 순서가 있다 (인덱스가 있다)  
맵은 순서가 없다. 경품권 상자에 들어있는 이름표같은 느낌  
키와 값으로 저장한다.  
  
객체를 저장하는 구조를 가지고 있는 자료구조  
여기서 키와 값은 모두 객체  
값은 중복 저장 가능,키는 중복저장 불가능. 만약 기존에 저장된 키와 동일한 키로 값을 저장하면  
기존의 값은 없어지고 새로운 값으로 대치된다.  
  
  
![image](https://user-images.githubusercontent.com/80766275/192416345-59de0150-6c0f-4041-a1e3-42cbc1efff3e.png)
  
해쉬맵은 내부에 키와 값을 저장하는 자료 구조를 가지고 있다. 해쉬맵은 해시 함수를 통해 키와 값이 저장되는 위치를 결정.  
사용자는 그 위치를 알 수 없고 삽입되는 순서와 들어있는 위치또한 관계 없음..!
  
  
  
  
![image](https://user-images.githubusercontent.com/80766275/192418523-bdac9eac-bfb2-43a4-9dcf-5d0997334e7d.png)
  
해시맵을 생성 - 키타입과 값 타입을 파라미터로 주고 기본 생성자를 호출.  
해시맵은 저장공간에 값이 추가로 들어오면 list처럼 저장공간을 추가로 늘리는데 list처럼 한 칸씩 늘리는것x 약 두배로 늘린다  
그래서 저장할 데이터 개수를 알고있다면 Map의 초기 용량을 지정해주는것이 좋다.  
  
  
  
  
![image](https://user-images.githubusercontent.com/80766275/192418911-790bae99-9274-4ef6-ae83-e486a2480c7b.png)
  
값 추가 - put(key,value) 메소드 사용. 선언시 해시맵에 설정해준 타입과 같은 타입의 키,밸류값을 넣어야 하며  
만약 입력되는 키값이 해시맵 내부에 존재한다면 기존의 값은 새로 입력되는 값으로 대체됨  
  
  
  
  
  
![image](https://user-images.githubusercontent.com/80766275/192419162-e6b12884-4e08-46f5-bdd9-a386efaa9808.png)
  
값 제거- remove(key)메소드 사용 .오직 키값으로만 Map요소 삭제 가능.  
모든 값 제거시 clear()  
  
  
  
  
  

![image](https://user-images.githubusercontent.com/80766275/192419449-89616c06-9aac-4ccd-9020-4f772cf17bd5.png)
  
값 출력 -  
1. print 시 : {}로 묶어 Map의 전체 키값,밸류값 출력
2. get(key) : 특정 키값 가져오고 싶을때  
3. 전체값 출력 : entrySet() , keySet() 메소드 사용.Map의 객체를 반환받은 후 출력  
entrySet() - 키와 밸류 모두 필요한 경우 사용  
keySet() - 키값만 필요할 경우 사용,그런데 키값만 받아서 get(key)를 사용하여 밸류도 출력 가능함  
so 어떤 메소드를 선택하던지 간에 큰 상관이 없어 대부분 keySet()활용. 많은 양의 데이터를 가져올때는 entrySet()이 좋다.  
  
  
  
  
  
![image](https://user-images.githubusercontent.com/80766275/192421047-f0e3984f-8714-4ff1-bff0-1a3a1c256ae2.png)
  
전체출력 - 반복문을 사용하지 않고 iterater를 사용하여도 된다.

  
  
  
![image](https://user-images.githubusercontent.com/80766275/192415624-efca74c6-7be0-4ae5-8bfe-9ae887450c8e.png)
  
  
  
