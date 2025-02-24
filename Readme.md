# 자바 중급 공부

<br>

# Chapter 1

<br>

## java.lang
자바가 기본으로 제공하는 라이브러리 중에 가장 기본이 되는 것이 `java.lang` 패키지다  
자바 언어를 이루는 가장 기본이 되는 클래스들을 보관

<br>

### java.lang 패키지의 대표적인 클래스들
- `Object`: 모든 자바 객체의 부모 클래스
- `String`: 문자열
- `Integer`, `Long`, `Double`: 래퍼 타입, 기본형 데이터 타입을 객체로 만든 것
- `Class`: 클래스 메타 정보
- `System`: 시스템과 관련된 기본 기능들을 제공

<br>

> `java.lang` 패키지는 모든 자바 애플리케이션에 자동으로 임포트된다. 따라서 임포트 구문을 사용하지 않아도 됨

<br>

## Object 클래스
- 자바에서 **모든 클래스의 최상위 부모 클래스**
  - 공통기능 제공
    - toString(), equals(), getClass() 등등...
  - 다형성의 기본 구현
    - 모든 클래스의 부모 클래스이다. 따라서 모든 객체를 참조할 수 있다
- 클래스에 상속받을 부모 클래스가 없으면 묵시적으로 `Object` 클래스를 상속받는다

<br>
묵시적: 개발자가 코드에 직접 기술하지 않아도 시스템 또는 컴파일러에 의해 자동으로 수행<br>
명시적: 개발자가 코드에 직접 기술해서 작동하는 것

### Object 다형성의 한계 
- object로 객체를 받았을때, object는 최상위 부모이므로 자식을 불러낼 수 없다
- 그럴때 다음과 같이 다운캐스팅을 해야한다
```
        if (obj instanceof Dog dog) {
            dog.sound();
        } 
```

### Object 활용
- 모든 객체를 받을 수 있는 메서드, 배열을 만들 수 있다