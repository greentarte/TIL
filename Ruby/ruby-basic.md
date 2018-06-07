# Ruby

#### 0. 개요

1. 루비는 순수객체 지향 언어이다.
2. 루비는 모든 것이 객체
3. Ruby on Rails 프레임워크로 유명해짐



#### 1. puts vs print

```Ruby
3.times {print "hello"} #=> hellohellohello
3.times {puts "hello"} #=> hello
                       #   hello
                       #   hello
```

> puts는 개행문자 포함

> cloud9 에서 터미널에서 ruby코드 사용할 시 irb 실행 exit 종료
>
> 비슷한 방법 pry 설치 후 사용 (gem install pry) pry로 실행 exit 종료
>
> pry가 색인이 들어가서 사용하기 더 편함

#### 2. puts vs p

```ruby
string = "hello"
puts string # hello => nil
p string # "hello" => "hello"
```



#### 3. naming conventions

- 변수
  - snake_case
- 상수
  - CONSTANT
- 클래스
  - CamelCase



#### 4. pry

- 설치

  - `gem install pry`

- 실행

  - `pry`

    > '내용'으로 하면 작성가능



#### 5. inline statment

```ruby
# if 문
puts "a=0" if a == 0  # "a = 0"
puts "a=0" if a == 1  #  출력안됨

# while 문
c = 0
result = c += 2 while c < 50 
puts result # 50
    
puts "hi" if 0 # hi
# 0은 true!!!!!!!!!
    
```



#### 6. case

```ruby
name = "chang2"
case name
when "chang2" then puts "hi chang2"  
when "tak" then puts "hi tak"  
else puts "hi"  
end  
# hi chang2
```



#### 7. method

- 대부분의 언어

  - 클래스 밖 :  function
  - 클래스 안 :  method

- 루비에서는 모든 function은 method

- ```ruby
  # 루비에서의 method 선언
  def simple
  puts "simple!!"
  end  
  
  # 루비에서의 method는 괄호를 명시적으로 적어줄 수 있습니다.
  def asdf()
      	puts "asdf"
  end
  ```

- ```ruby
  # 루비에서는 return이 없을때는 마지막 연산 값을 return 합니다.
  def add2(a,b)
  	a+b
  end  
  
  add2(1,2) #=> 3
  
  # return을 선택적으로 사용할 수 있습니다.
  def divide(a,b)
      return "I don't think so" if b == 0
      a/b
  end
  ```



- 기본 매개변수

- ```ruby
  def factorial(n)
      n == 0 ? 1 : n * factorial(n-1)
  end
  
  factorial 
  #ArgumentError: wrong number of arguments (given 0, expected 1)
  
  def factorial_d(n=5)
      n == 0 ? 1 : n * factorial_d(n-1)
  end
  ```



#### 8. block

```ruby
3.times { puts "hello"}
3.times do |asdf|
	puts asdf # 요부분이 block 입니다.
end  
# 0 1 2
```

```ruby
def hihi
return "No block" unless block_given?  
yield  
end  

hihi # => "No block"
hihi { puts "hihi"} #hihi	
```



#### 10. String

```ruby
a= "안녕하세요 \n 멋사입니다."
puts a
# => 안녕하세요  
#    멋사입니다.

b = ' 안녕하세요 \n 멋사입니다.'
puts b
# => 안녕하세요 \n 멋사입니다.

name = "Sochang2"
a = "#{name}님 안녕하세요"
=> "Sochang2님 안녕하세요"
puts a # => Sochang2님 안녕하세요
b = '#{name}님 안녕하세요'
puts b # => #{name}님 안녕하세요
```







