# study

출처: https://jusung.gitbook.io/the-swift-language-guide/

//  *  문자열과 문자 *

// 빈 문자열 초기화
var emptyString = ""
var anotherEmptyString = String()

if emptyString.isEmpty{
    print("아무것도 없습니다")
}


// 문자열 수정
var variableString = "aaa"
variableString += "bbb"
variableString = "ccc"

for abc in "ABC"{
    print(abc)
}

let a : [Character] = ["A","B","C"]
let aString = String(a)
print(aString)

// 문자열과 문자의 결합
let string1 = "yu"
var string2 = "jhong"
var strign3 = string1+string2

var string4 = "hi"
string4 += " "+string2

let exp : Character = "!"
string2.append(exp)

print(string2)

// 문자열 삽입
let multipler = 5
let message = "\(multipler)곱하기 3.5은 \(Double(multipler)*3.5)"


// 문자열 인덱스
let greeting = "Guten Tag!"
greeting[greeting.startIndex]
// greeting[greeting.endIndex] 에러-> .endIndex는 마지막 인덱스+1
greeting[greeting.index(before: greeting.endIndex)]
greeting[greeting.index(after: greeting.startIndex)]

// 떨어진 위치 offsetBy
let dddd = greeting.index(greeting.startIndex, offsetBy: 0)
greeting[dddd]

// 개별 문자 접근 indices
for index in greeting.indices{
    print("\(greeting[index]) ", terminator: "")
}

// 문자의 삽입과 삭제
var welcome = "hello"
welcome.insert("!", at: welcome.endIndex)
welcome.insert(contentsOf: " jhong", at: welcome.index(before: welcome.endIndex))

welcome.remove(at: welcome.index(before: welcome.endIndex)) // 질문**********
let range = welcome.index(welcome.endIndex, offsetBy: -6)..<welcome.endIndex
welcome.removeSubrange(range)


// 부분 문자열
let greeting = "Hello , Jhong!"
let index = greeting.firstIndex(of: ",") ?? greeting.endIndex
let beginning = greeting[..<index]

// 이렇게 구해진 beginning은 String 타입이 아니라 Substring 타입이다.
// Substring은 자신의 원본 문자열을 저장하는 메모리를 그대로 사용한다.
// 즉, 원본 메모리의 인스턴스를 참조한다.
// 따라서 단순 참조만 이루어 질 경우에는 성능 최적화를 위해 Substring 그대로 사용하는 것이 좋고,
// Substring을 변형하는 등 기타 활용해야 할 경우, String으로 형변환 하여 사용하는 것이 좋다.

// substring인 beginning을 String으로 변환
let newString = String(beginning)

// 접두사 hasPreFix 접미사 hasSuffix
let memo = [
    "hi a ",
    "hi b bye",
    "hi c bye"
]
var cnt = 0

for hi in memo{
    if hi.hasPrefix("hi"){
        cnt += 1
    }
}

for bye in memo{
    if bye.hasSuffix("bye"){
        cnt += 1
    }
}

