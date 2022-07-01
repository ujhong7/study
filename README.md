
//import UIKit
//
//var greeting = "Hello, playground"
//
//
//
//
//let b = 10
//var a = 5
//
//// a = b
//a
//a == b
//
//let (x,y) = (1,2)
//x
//y
//
//"hello" + " world"
//
//
//let One = 1
//let mOne = -One
//let pOne = -mOne
//
//
//let mTwo = -2
//let mmTow = +mTwo
//
//var d = 1
//d += 2
//d = d+2
//
//let name = "hooong"
//if name == "hong"{
//    print("hello jhong")
//}else{
//    print("who are you")
//}
//
// (1, "h" ) < (2, "g")
//"hong" < "jun"
//"h" < "g"
//
//let a = 1
//let b = false
//let c = a + ( b ? 2 : 3)
//c
//
//let a = "red"
//var b = "blue"
//var c = b ?? a
//
//for index in 1...5{
//    print("\(index)")
//}
//
//
// let name = ["a","b","c","d"]
//let cnt = name.count
//for i in 0..<cnt{
//    print("\(i+1) is \(name[i])")
//}
//
//for i in name[...2]{
//    print(i)
//}
//
//let a = true
//if !a{
//    print("hahaha")
//}else{
//    print("what")
//}
//
////  2 문자열과 문자
//
//// 빈 문자열 초기화
//var emptyString = ""
//var anotherEmptyString = String()
//
//if emptyString.isEmpty{
//    print("아무것도 없습니다")
//}
//
//
//// 문자열 수정
//var variableString = "aaa"
//variableString += "bbb"
//variableString = "ccc"
//
//for abc in "ABC"{
//    print(abc)
//}
//
//let a : [Character] = ["A","B","C"]
//let aString = String(a)
//print(aString)
//
//// 문자열과 문자의 결합
//let string1 = "yu"
//var string2 = "jhong"
//var strign3 = string1+string2
//
//var string4 = "hi"
//string4 += " "+string2
//
//let exp : Character = "!"
//string2.append(exp)
//
//print(string2)
//
//// 문자열 삽입
//let multipler = 5
//let message = "\(multipler)곱하기 3.5은 \(Double(multipler)*3.5)"
//
//
//// 문자열 인덱스
//let greeting = "Guten Tag!"
//greeting[greeting.startIndex]
//// greeting[greeting.endIndex] 에러-> .endIndex는 마지막 인덱스+1
//greeting[greeting.index(before: greeting.endIndex)]
//greeting[greeting.index(after: greeting.startIndex)]
//
//// 떨어진 위치 offsetBy
//let dddd = greeting.index(greeting.startIndex, offsetBy: 0)
//greeting[dddd]
//
//// 개별 문자 접근 indices
//for index in greeting.indices{
//    print("\(greeting[index]) ", terminator: "")
//}
//
// 문자의 삽입과 삭제
//var welcome = "hello"
//welcome.insert("!", at: welcome.endIndex)
//welcome.insert(contentsOf: " jhong", at: welcome.index(before: welcome.endIndex))
//
//welcome.remove(at: welcome.index(before: welcome.endIndex)) // 마지막 문자를 삭제하고 삭제한 문자를 리턴
//welcome
//let range = welcome.index(welcome.endIndex, offsetBy: -6)..<welcome.endIndex
//welcome.removeSubrange(range)
//
//
//// 부분 문자열
//let greeting = "Hello , Jhong!"
//let index = greeting.firstIndex(of: ",") ?? greeting.endIndex
//let beginning = greeting[..<index]
//
//// 이렇게 구해진 beginning은 String 타입이 아니라 Substring 타입이다.
//// Substring은 자신의 원본 문자열을 저장하는 메모리를 그대로 사용한다.
//// 즉, 원본 메모리의 인스턴스를 참조한다.
//// 따라서 단순 참조만 이루어 질 경우에는 성능 최적화를 위해 Substring 그대로 사용하는 것이 좋고,
//// Substring을 변형하는 등 기타 활용해야 할 경우, String으로 형변환 하여 사용하는 것이 좋다.
//
//// substring인 beginning을 String으로 변환
//let newString = String(beginning)
//
//// 접두사 hasPreFix 접미사 hasSuffix
//let memo = [
//    "hi a ",
//    "hi b bye",
//    "hi c bye"
//]
//var cnt = 0
//
//for hi in memo{
//    if hi.hasPrefix("hi"){
//        cnt += 1
//    }
//}
//
//for bye in memo{
//    if bye.hasSuffix("bye"){
//        cnt += 1
//    }
//}
//
//
//
////---------------------
//
////  빈 배열
//var someInts = [Int]()
//print("\(someInts.count)")
//
//someInts.append(3)
//print("\(someInts)")
//someInts = []
//print("\(someInts)")
//
//// 기본 값으로 빈 배열 생성
//var threeDoubles = Array(repeating: 0.0, count: 3)
//// 다른 배열을 추가한 배열
//var anotherThreeDoubles = Array(repeating: 2.5, count: 3)
//var sixDoubles = threeDoubles + anotherThreeDoubles
//
//
//// 리터럴을 이용한 배열의 생성
//var fruitList: [String] = ["Apple","Banana","Peach"]
//var friutList = ["Apple","Banana","Peach"]
//
//// 배열의 원소 개수 확인
//friutList.count
//
//// 배열이 비어있는지 확인
//if friutList.isEmpty{
//    print("empty")
//}else{
//    print("not empty")
//}
//
//// 배열 원소 추가
//friutList.append("melon")
//fruitList.count // 질문*************
//
//fruitList += ["melon"]
//fruitList.count
//
//// 배열의 특정 위치의 원소 접근
//var firstItem = fruitList[0]
//fruitList[2...3]=["a","b"]
//
//fruitList.insert("Pear", at: 4)
//fruitList.remove(at: 4)
//fruitList.removeLast() // 마지막 문자를 삭제하고 삭제한 문자를 리턴

// 배열의 순회
for item in fruitList{
    print(item)
}




