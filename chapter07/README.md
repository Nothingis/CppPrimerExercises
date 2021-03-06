# Chapter 7 

## Exercise 7.1
> 1.6절에 있는 거래 내용 처리 프로그램을 2.6.1절 연습문제에서 정의한 Sales_data 클래스를 사용해 만든다.

코드는 [여기](ex7_01.cc)

## Exercise 7.2
> 2.6.2절 연습문제에서 만든 Sales_data 클래스에 combine과 isbn 멤버를 추가한다.

코드는 [여기](ex7_02.h)

## Exercise 7.3
> 7.1.1절에서 본 거래 내용 처리 프로그램에서 이 멤버를 사용하도록 고친다.

코드는 [여기](ex7_03.cc)

## Exercise 7.4
> 개인의 이름과 주소를 나타내는 Person 객체를 만들고 각 요소는 string을 사용해 담는다. 이후 연습문제에서는 이 클래스에 기능을 차례로 정차 추가한다.

코드는 [여기](ex7_04.h)

## Exercise 7.5
> Person 클래스에 이름과 주소를 반환하는 연산을 추가한다. 이 함수는 const여야 하는가? 선택에 대해 설명한다.

코드는 [여기](ex7_05.h)

## Exercise 7.6
> add, read, print 함수를 직접 정의한다.

코드는 [여기](ex7_06.h)

## Exercise 7.7
> 7.1.2절 연습문제에서 만든 거래 내용 처리 프로그램을 고쳐 방금 만든 새로운 함수를 쓰도록 한다.

코드는 [여기](ex7_07.cc)

## Exercise 7.8
> Sales_data 매개변수를 read에서는 보통의 참조자로, print에서는 const에 대한 참조자로 정의한 이유를 설명한다.

read에서는 매개변수를 변경할 여지가 있지만, print에서는 변경할 여지가 없다.

## Exercise 7.9
> 7.1.2절 연습문제에서 만든 코드에 Person 객체를 읽어 출력하는 연산을 추가한다.

코드는 [여기](ex7_09.h)

## Exercise 7.10
> 다음 if 조건에서 하는 일이 무엇인지 설명한다.
```cpp
if (read(read(cin, data1), data2))
```

두 번의 data를 입력 받아야 true이다.

## Exercise 7.11
> 직접 만든 Sales_data 클래스에 생성자를 추가하고 각 생성자를 사용하는 프로그램을 만든다.

[ex7_11.h](ex7_11.h)

[ex7_11.cc](ex7_11.cc)

## Exercise 7.12
> istream을 취하는 Sales_data 생성자 정의를 Sales_data클래스 본체로 옮긴다.

코드는 [여기](ex7_12.h)

## Exercise 7.13
> 299쪽에 있는 프로그램을 다시 만들어 istream 생성자를 사용하도록 한다.

코드는 [여기](ex7_13.cc)

## Exercise 7.14
> 클래스 내 초기 값으로 지정한 값을 사용해 해당 멤버를 명시적으로 초기화하는 기본 생성자를 만든다.

```cpp
Sales_data() : bookNo(""), units_sold(0), revenue(0){ }
```

## Exercise 7.15
> Person 클래스에 적절한 생성자를 추가한다.

코드는 [여기](ex7_15.h)

## Exercise 7.16
> 클래스 정의에서 접근 지정자를 쓸 수 있는 위치와 얼마나 많이 쓸 수 있는지에 대한 제약이 있다면 설명한다. public 지정자와 private 다음에는 어떤 멤버를 정의해야 하는지 각각 설명한다.

클래스에서는 접근 지정자를 사용하지 않거나 하나 이상 사용할 수 있으며 얼마나 많이 쓸 수 있는지에 대한 제한도 없다. 각 접근 지정자에서는 다음에 오는 멤버에 대한 접근 수준을 지정한다. 접근 수준을 지정하면 다음 접근 지정자를 만나거나 클래스 본체를 빠져나갈 때까지 그대로 유지한다.


public에는 해당 클래스 인터페이스를 정의하고,

private는 구현에 속하는 데이터 멤버와 함수를 정의한다.

## Exercise 7.17
> class나 struct를 사용하는 것에 차이가 있다면 무엇인지 설명한다.

struct와 class 사이의 유일한 차이는 기본 접근 수준이다.

struct 키워드를 사용하면 첫 번째 접근 지정자 이전에 정의한 멤버는 public이고 class를 사용하면 그 멤버는 private이다.

## Exercise 7.18
> 캡슐화는 무엇인지, 왜 유용한지 설명한다.

캡슐화는 인터페이스와 구현의 분리입니다. 캡슐화는 타입에 따른 상세한 구현을 숨깁니다. 

캡슐화에는 두 가지 중요한 장점이 있다.
- * 사용자 코드에서는 캡슐화한 객체 상태를 무심코 망가뜨릴 수 없다.
- * 시간이 흘러도 사용자 수준 코드를 변셩하지 않고 캡슐화한 클래스의 구현 내용을 변경할 수 있다.

## Exercise 7.19
> Person 클래스 멤버 중 public과 private으로 선언해야 하는 것은 각각 무엇인지 나타내고 이유를 설명한다.

public: 생성자, getName(), getAddress().

private: name, address.

인터페이스는 public으로 생성해야하고 데이터는 private로 해야한다.

## Exercise 7.20
> 프렌드가 유용할 때는 언제인가? 프렌드를 사용할 때 장단점을 논의한다.

장점:

- * 모든 non-public 멤버에게 모두 접근할 수 있다.

단점:

- * 캡슐화를 줄이고 유지보수를 어렵게 한다.

## Exercise 7.21
> 직접 만든 Sales_data 클래스를 갱신해 구현을 숨기도록 한다. Sales_data 연산을 사용하도록 만든 프로그램은 여전히 잘 작동해야 한다. 새 클래스 정의를 사용하는 프로그램을 재컴파일 하고 여전히 잘 작동하는지 검증한다.

코드는 [여기](ex7_21.h)


## Exercise 7.22
> Person 클래스를 갱신해 구현 내용을 숨기도록 한다.

코드는 [여기](ex7_22.h)

## Exercise 7.23
> Screen 클래스를 직접 만든다.

코드는 [여기](ex7_23.h)

## Exercise 7.24
> 직접 만든 Screen 클래스에 세 가지 생성자, 즉 기본 생성자, 높이와 폭에 대한 값을 취하고 지정한 수의 공백 문자로 내용을 초기화하는 생성자, 높이와 폭에 대한 값과 화면 내용으로 사용할 문자를 취하는 생성자를 추가한다.

코드는 [여기](ex7_24.h)
## Exercise 7.25
> Screen에서 복사와 대입에 대해 기본 버전에 의존해도 안전할지, 그렇지 않을지 이유와 함께 설명한다.

책에서...


"게다가 복사, 대입, 소멸에 대한 합성 버전은 vector나 string을 멤버로 하는 클래스에 대해서는 올바로 작동한다."


따라서 기본 버전에 의존해도 안전하다.

## Exercise 7.26
> Sales_data::avg_price를 inline 함수로 정의한다.

[ex7_26.h](ex7_26.h)

[ex7_26.cc](ex7_26.cc)

## Exercise 7.27
> 직접 만든 Screen에 move, set, display 연산을 추가하고 다음 코드를 실행해 클래스를 시험한다.

```cpp
Screen myScreen(5, 5, 'X');
myScreen.move(4, 0).set('#').display(cout);
cout << "\n";
myScreen.display(cout);
cout << "\n";
```

코드는 [여기](ex7_27.h)

## Exercise 7.28
> move, set, display에서 Screen& 대신 Screen을 반환하면 앞 연습문제에서 어떤 일이 생길지 설명한다.

set이 일시적인 복사 값을 변경하기 때문에 객체가 set의 결과를 가지고 있지 않다. 

따라서, 두 번째 display는 다르게 출력된다.

## Exercise 7.29
> 직접 만든 Screen을 고쳐 move, set, display 함수에서 Screen을 반환하도록 하고 앞 연습문제에서 한 예상이 맞는지 확인한다.

```cpp
//&일 때
XXXXXXXXXXXXXXXXXXXX#XXXX
XXXXXXXXXXXXXXXXXXXX#XXXX
                   ^^^
//아닐 때
XXXXXXXXXXXXXXXXXXXX#XXXX
XXXXXXXXXXXXXXXXXXXXXXXXX
                   ^^^
```

## Exercise 7.30
> this 포인터를 통해 멤버를 참조하는 것은 적법하지만 불필요하다. 명시적으로 this 포인터를 사용해 멤버에 접근하는 것에 대한 장단점을 논의한다.

### 장점
- * 직관적
- * scope에 대해 이해가 쉽다
- * 멤버 함수의 변수 이름을 멤버 이름과 같게 할 수 있다.

### 단점
- * 길어 진다??

## Exercise 7.31
> X와 Y 클래스 쌍을 정의하는데 X에는 Y에 대한 포인터가 있고 Y에는 X 타입 객체가 있도록 한다.

코드는 [여기](ex7_31.h)

## Exercise 7.32
> screen과 window-mgr을 직접 정의한다. 이때 clear는 window-mgr의 멤버이며 screen의 프렌드이다.

코드는 [여기](ex7_32.h)

## Exercise 7.33
> Screen에 다음처럼 정의한 size 멤버를 추가하면 어떻게 될지 설명하고 문제가 있으면 고친다.
```cpp
pos Screen:size() const
{
	return height * width;
}
```

unknown type name 'pos' 에러 발생

다음과 같이 고친다.

```cpp
Screen::pos Screen::size() const
{
	return height*width;
}
```

## Exercise 7.34
> 337쪽에 있는 Screen 클래스 마지막에 pos의 typedef를 둔다면 어떻게 될지 설명한다.

```cpp
dummy_fcn(pos height)
           ^
Unknown type name 'pos'
```

## Exercise 7.35
> Type과 initVal을 사용하는 곳에서 각각 어떤 정의를 사용하는지 나타내고 다음 코드를 설명한다. 또한 오류를 어떻게 수정할 수 있을지 설명한다.
```cpp
typedef string Type;
Type initVal(); /* string */
class Exercise {
	public:
		typedef double Type;
		Type setVal(Type); /* double */
		Type initVal(); /* double */
	private:
		int val;
};
Type Exercise::setVal(Type parm) { // 처음에는 string, 두 번째는 double
	val = parm + initVal(); // Exercise::initVal()
	return val;
}
```

Type Exercise를 Exercise::Type Exercise로 고친다.

## Exercise 7.36
> 다음 초기화식은 오류이다. 문제를 찾고 고친다.
```cpp
struct X {
	X (int i, int j): base(i), rem(base % j) { }
	int rem, base;
};
```

rem(base % j)를 rem(i % j)로 고친다.

## Exercise 7.37
> 이 절에 있는 Sales_data 버전을 사용해 다음 각 변수를 초기화하는 데 어느 생성자를 사용하는지 결정하고 각 객체의 데이터 멤버 값을 나열한다.
```cpp
Sales_data first_item(cin);

int main()
{
	Sales_data next; 
	Sales_data last("9-999-99999-9"); 
}
```

첫 번째 Sales_data(std::istream &is) 사용
두 번째 Sales_data(std::string s = "") 사용, bookNo = "", cnt = 0, revenue = 0.0
세 번째 Sales_data(std::string s = "") 사용, bookNo = "9-999-99999-9", cnt = 0, revenue = 0.0 

## Exercise 7.38
> istream&를 취하는 생성자에 cin을 기본 인자로 지정하길 바랄 수도 있다. cin을 기본 인자로 사용하는 생성자 선언을 만든다.

```cpp
Sales_data(std::istream &is = std::cin) { read(is, *this); }
```

## Exercise 7.39
> string을 취하는 생성자와 istream&를 취하는 것 둘 모두 기본 인자를 지정하는 것이 적법한지 설명한다. 아니라면 왜 그런지 설명한다.

위법. Sales_data() 생성자 호출을 모호?하게 만든다.

## Exercise 7.40
> 다음 추상 객체 중 하나를 선택한다. (또는 직접 만든다.) 그 클래스에서 필요한 데이터 멤버가 무엇인지 결정하고 적절한 생성자 집합을 추가한다. 결정한 내용에 대해 설명한다.

- (a) Book
- (b) Date
- (c) Employee
- (d) Vehicle
- (e) Object
- (f) Tree

```cpp
#include <iostream>
#include <string>

class Book 
{
public:
    Book(unsigned isbn, std::string const& name, std::string const& author, std::string const& pubdate)
        :isbn_(isbn), name_(name), author_(author), pubdate_(pubdate)
    { }

    explicit Book(std::istream &in) 
    { 
        in >> isbn_ >> name_ >> author_ >> pubdate_;
    }

private:
    unsigned isbn_;
    std::string name_;
    std::string author_;
    std::string pubdate_;
};
```

## Exercise 7.41
> 직접 만든 Sales_data 클래스에서 위임 생정자를 사용하도록 다시 만든다. 각 생성자 본체에 문장을 추가해 실행할 때마다 메시지를 출력하도록 한다. 가능한 모든 방법으로 Sales_data 객체를 생성하도록 여러 선언을 만든다. 위임 생성자 사이에 실행 순서를 확실히 이해할 때까지 출력 내용을 학습한다.

[ex7_41.h](ex7_41.h)

[ex7_41.cc](ex7_41.cc)

## Exercise 7.42
> 7.5.1절 연습문제 7.40에서 만든 클래스에 대해 어느 생성자에서 위임을 사용할 수 있을지 결정한다. 사용할 수 있으면 클래스에 위임 생성자를 만들고 그렇지 않다면 추상 객체 목록에서 위임 생성자를 사용할 수 있을 것으로 생각하는 것을 선택한다. 해당 추상 객체에 대한 클래스 정의를 만든다.

```cpp
class Book {
 public:
  Book(unsigned isbn, std::string const& name,
      std::string const& author, std::string const& pubdate)
      :isbn_(isbn), name_(name), author_(author), pubdate_(pubdate) {}

  Book(std::string const &name, std::string const &author,
      std::string const &pubdate) : Book(0, name, author, pubdate) {}

    explicit Book(std::istream &in) {
        in >> isbn_ >> name_ >> author_ >> pubdate_;
    }

 private:
  unsigned isbn_;
  std::string name_;
  std::string author_;
  std::string pubdate_;
};
```

## Exercise 7.43
> int를 취하는 생성자는 있지만 기본 생성자는 없는 NoDefault 클래스가 있다고 하자. NoDefault 타입인 멤버가 있는 클래스 C를 정의하고 C에 대한 기본 생성자를 정의한다.

코드는 [여기](ex7_43.cc)


## Exercise 7.44
> 다음 선언이 옳은지 설명한다. 옳지 않다면 왜 그런지 설명한다.
```cpp
vector<Nodefault> vec(10);
```

옳지 않다. 각각은 default로 초기화 되어야 하지만 NoDefault는 default 생성자가 없다.

## Exercise 7.45
> 앞 연습문제의 vector에서 C 타입 객체를 담도록 정의하면 어떻게 될지 설명한다.

C는 기본 생성자가 있기 때문에 문제되지 않는다.

## Exercise 7.46
> 다음 문장 중 거짓이 있다면 어느 것인지, 왜 그런지 설명한다.

- (a) 클래스에서는 반드시 적어도 생성자 하나는 있어야 한다.

거짓. 기본 생성자가 자동으로 생긴다.

- (b) 기본 생성자는 매개변수 목록이 비어 있는 생성자이다.

거짓. 기본 생성자는 초기화 식 없이 호출되는 생성자이다. 기본 인자를 사용해 매겨변수 목록이 있어도 기본 생성자가 될 수 있다.

- (c) 클래스에 대한 의미 있는 기본 값이 없으면 해당 클래스에는 기본 생성자가 없어야 한다.

거짓. 클래스는 기본 생성자가 있어야 한다.

- (d) 클래스에서 기본 생성자를 정의하지 않으면 컴파일러에서 각 데이터 멤버와 연관된 타입의 기본 값으로 해당 멤버를 초기화하는 생성자를 만든다.

거짓. 기본 생성자는 클래스에 어떠한 생성자도 없을 때 만들어 진다.

## Exercise 7.47
> string을 취하는 Sales_data 생성자가 explicit여야 하는지 설명한다. 이 생성자를 explicit로 할 때 장단점은 무엇일지 설명한다.

### 장점
- * 암시적 변환이 필요한 생성자를 사용하지 못 하도록 막는다.
- * 직접 초기화하는 형식의 생성자를 정의할 수 있다.

### 단점
- * 하나의 인자를 가진 생성자가 호출될 때만 의미 있다.

## Exercise 7.48
> Sales_data 생성자가 explicit가 아니라면 다음 정의에서 어떤 일이 생길지 설명한다.
```cpp
string null_isbn("9-999-99999-9");
Sales_data item1(null_isbn);
Sales_data item2("9-999-99999-9");
```
> Sales_data 생성자가 explicit라면 어떻게 될지 설명한다.

Sales_data에 대해 생성자를 모두 정의했으므로 내부적으로 같은 동작이다.

## Exercise 7.49
> 다음 세 가지 combine 선언 각각에 대해, i는 Sales_data이고 s는 string일 때 i.combine(s)를 호출하면 어떻게 될지 설명한다.

- (a) Sales_data &combine(Sales_data);

적합.

- (b) Sales_data &combine(Sales_data&);

오류. s에 대한 임시 객체를 non-const 인자로 줄 수 없다.

- (c) Sales_data &combine(const Sales_data&) const;

부적절. 마지막 const가 데이터 멤버에 대한 변형을 막기 때문에 const가 있을 수 없다.

## Exercise 7.50
> Person 클래스 생성자 중 어느 것을 explicit로 지정해야 하는지 결정한다

```cpp
explicit Person(std::istream &is) { read(is, *this); }
```

## Exercise 7.51
> vector에서는 단일 인자 생성자를 explicit로 정의하지만 string에서는 그렇게 하지 않은 이유가 무엇일지 설명한다.

vector는 생성자를 불렀을 때 그 형태가 매우 혼동된다.

ex> Person(30);


하지만 string은 매우 자연스럽다

ex> Person("jh");

## Exercise 7.52
> 2.6.1절에 있는 Sales_data의 첫 버전을 사용해 다음 초기화를 설명한다. 문제가 있으면 찾아 수정한다.
```cpp
Sales_data item = {"978-0590353403", 25, 15.99};
```

클래스내 초기 값이 없어야 한다.

```cpp
 struct Sales_data {
    std::string bookNo;
    unsigned units_sold;
    double revenue;
};
```

## Exercise 7.53
> Debug를 직접 정의한다.

코드는 [여기](ex7_53.h)

## Exercise 7.54
> Debug에서 set_으로 시작하는 멤버를 constexpr로 선언해야 할지 설명한다. 만약 아니라면 왜 그런지 설명한다.

set_으로 시작하는 멤버는 데이터를 수정하는 함수지만 constexpr로 선언하면 데이터를 수정할 수 없다.

## Exercise 7.55
> 7.5.5절에 있는 Data 클래스는 상수 클래스인가? 맞다면 그 이유를, 아니라면 아닌 이유를 설명한다.

아니다.

std::string은 리터럴 타입이 아니다.

## Exercise 7.56
> static 클래스 멤버가 무엇이고 장단점은 무엇인지, 보통의 멤버와 어떻게 다른지 설명한다.

static 클래스 멤버는 각각이 고유한 객체가 아니라 클래스 자체와 연관된 멤버이다.

클래스에 대한 모든 객체가 하나의 공통된 데이터를 가지는 장점이자 단점이 있다.

static 멤버는 불완전한 타입을 가질 수 있다.

## Exercise 7.57
> Account 클래스를 직접 만든다.

코드는 [여기](ex7_57.h)

## Exercise 7.58
> 다음 static 데이터 멤버 선언과 정의 중 오류가 있다면 어느 것인지 찾고 이유를 설명한다.

```cpp
// example.h
class Example {
	public:
		static double rate = 6.5;
		static const int vecSize = 20;
		static vector<double> vec(vecSize);
};
// example.C
#include "example.h"
double Example::rate;
vector<double> Example::vec;
```

다음과 같은 오류가 발생한다.

(일반적으로 클래스 static 멤버는 클래스 본체 안에서 초기화할 수 없다. 하지만 const 정수 타입인 static 멤버에는 클래스 내 초기 값을 지정할 수 있으며~)


```cpp
static double rate = 6.5;
                ^
            rate should be a constant expression.

static vector<double> vec(vecSize);
                            ^
            we may not specify an in-class initializer inside parentheses.
```

다음과 같이 고친다.

```cpp
// example.h
class Example {
public:
    static constexpr double rate = 6.5;
    static const int vecSize = 20;
    static vector<double> vec;
};

// example.C
#include "example.h"
constexpr double Example::rate;
vector<double> Example::vec(Example::vecSize);
```
