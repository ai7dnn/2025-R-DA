
# R의 데이터 타입과 자료 구조

R 언어에서 데이터를 다룰 때는 데이터가 **어떤 유형(type)**이며 **어떤 구조(structure)**로 저장되어 있는지 이해하는 것이 중요합니다. 데이터 유형과 구조에 대한 이해가 부족하면 코드가 예상과 다르게 동작하거나 초보자가 혼란을 느끼기 쉽습니다. 여기서는 R의 기본 데이터 **유형**과 **자료 구조**를 초보자도 이해하기 쉽게 설명하고, 각 예시와 함께 `typeof()`, `class()`, `str()` 함수를 사용하여 객체의 타입을 확인하는 방법도 다루겠습니다.

**목차:**

1. 기본 데이터 유형 (원자형 데이터 타입)  
   - Numeric (숫자형)과 Integer (정수형)  
   - Character (문자형)  
   - Logical (논리형)  
   - Complex (복소수형)  
   - Raw (Raw 타입)  

2. 자료 구조 (데이터 구조)  
   - Vector (벡터)  
   - Factor (팩터)  
   - List (리스트)  
   - Matrix (행렬)  
   - Array (배열)  
   - Data Frame (데이터 프레임)  

3. 데이터 타입 확인: `typeof()`, `class()`, `str()` 함수 활용법  

각 섹션에서는 개념 설명과 함께 간단한 R 코드 예제를 제공합니다. 예제는 **이름 목록**, **온도 값 목록**, **참/거짓 플래그** 등 일상적인 시나리오를 사용하여 이해를 돕겠습니다. 또한 곳곳에 가벼운 해설과 초보자가 흔히 저지르는 실수를 피하는 팁도 포함하였습니다.

## 1. 기본 데이터 유형 (원자형 데이터 타입)

### Numeric (숫자형)과 Integer (정수형)

```r
x_num <- 5    # numeric
x_int <- 5L   # integer
typeof(x_num)  # "double"
typeof(x_int)  # "integer"
```

### Character (문자형)

```r
name <- "홍길동"
fruits <- c("Apple", "Banana", "Cherry")
typeof(name)     # "character"
length(fruits)   # 3
```

### Logical (논리형)

```r
is_raining <- FALSE
flags <- c(TRUE, TRUE, FALSE, TRUE)
typeof(is_raining)  # "logical"
```

### Complex (복소수형)

```r
z <- 2 + 3i
typeof(z)        # "complex"
Re(z); Im(z)
```

### Raw (Raw 타입)

```r
raw_vec <- charToRaw("ABC")
raw_vec        # 41 42 43
typeof(raw_vec) # "raw"
```

## 2. 자료 구조 (데이터 구조)

### Vector (벡터)

```r
nums <- c(10, 20, 30)
chars <- c("안녕", "Hello")
bools <- c(TRUE, FALSE, TRUE)
typeof(chars)
length(chars)
class(chars)
str(chars)
```

### Factor (팩터)

```r
survey <- factor(c("Good", "Bad", "Bad", "Good", "Ok"),
                 levels = c("Bad", "Ok", "Good"))
survey
typeof(survey)  # "integer"
class(survey)   # "factor"
str(survey)
```

### List (리스트)

```r
person <- list(
  name = "John Doe",
  age = 29,
  scores = c(90, 85, 92),
  passed = TRUE
)
str(person)
```

### Matrix (행렬)

```r
m1 <- matrix(1:6, nrow=2, ncol=3)
dim(m1)
class(m1)
typeof(m1)
m1[2, 3]
```

### Array (배열)

```r
arr <- array(1:8, dim = c(2, 2, 2))
arr
arr[2, 1, 2]
```

### Data Frame (데이터 프레임)

```r
names <- c("철수", "영희", "길동")
ages  <- c(25, 30, 19)
passed <- c(TRUE, TRUE, FALSE)
df <- data.frame(Name = names, Age = ages, Passed = passed)
print(df)
str(df)
```

## 3. 데이터 타입 확인 함수

### typeof()

객체의 **저수준 저장 형태**를 알려줍니다.

```r
typeof(3.14)        # "double"
typeof("hello")     # "character"
typeof(TRUE)        # "logical"
```

### class()

객체의 **클래스(고수준 유형)**을 알려줍니다.

```r
class(df)           # "data.frame"
class(m1)           # "matrix"
class(person)       # "list"
```

### str()

객체의 **구조 요약**을 보여주는 함수로, 데이터 구조 확인 및 디버깅에 매우 유용합니다.

```r
str(df)
str(arr)
str(person)
```

---

이 문서는 초보자가 R의 다양한 데이터 유형과 구조를 정확히 이해하고 실전 코드에서 혼란 없이 활용할 수 있도록 구성되었습니다. 모든 코드 예제는 복사하여 바로 R 콘솔이나 RStudio에서 실행해볼 수 있으며, `typeof()`, `class()`, `str()` 함수는 디버깅과 학습에 필수적인 도구로서 익숙해지면 많은 도움이 됩니다.
