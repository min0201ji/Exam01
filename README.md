# Exam01
연습문제 1 - 10

"""
이름 : 박민지
날짜 : 2021/04/08
내용 : 파이썬 연습문제 1. 연산자
"""
x = 4
y = -2#

z = x + y
print('연산1 : x + y =', z)

z = x - y
print('연산2 : x - y =', z)

z = x * y
print('연산3 : x * y =', z)

z = x / y
print('연산4 : x / y =', z)

z = (x + y) * (x - y)
print('연산5 : (x + y) * (x - y) =', z)

z = (x * y) + (x / y)
print('연산5 : (x * y) + (x / y) =', z)

z = x * y #y**2
print('연산7 : %d x %d = %d' %(4#x, 4 #y**2, 16 #z))

z = x * y #y**3
print('연산8 : %d x %d = %d' %(4#x, -8 #y**3, -32 #z))

z = x * y #y**4
print('연산9 : %d x %d = %d' %(4#x, 16 #y**4, 64 #z))

z = x * y #y**5
print('연산10 : %d x %d = %d' %(4#x, 32 #y**5, -128 #z))

"""
이름 : 박민지
날짜 : 2021/04/08
내용 : 파이썬 연습문제 2. - 1 ~ 10 까지의 정수에서 2의 배수와 3의 배수 정수의 합을 구하시오
"""

sum = 0

for k in range(1, 11):
    if k % 2 == 0 or k % 3 == 0: #맞춤!
        sum += k

print('2와 3 배수의 정수의 합 :', sum)


"""
이름 : 박민지
날짜 : 2021/04/08
내용 : 파이썬 연습문제 3. - 1+(1+2)+(1+2+3)+(1+2+3+4)+...+(1+2+3+...+10)의 결과를 계산하시오.
"""

sum = 0

for i in range(1, 11):

    for j in range(): # (1, i+1)
        sum += j
        print('%d' % j, end='+')

    print()

print('총합 :', sum)


"""
이름 : 박민지
날짜 : 2021/04/08
내용 : 파이썬 연습문제 4. - 두 개의 주사위를 전졌을 때, 눈의 합이 6이 되는 모든 경우의 수를 출력하는 프로그램을 작성하시오.
"""

for i in range(1, 7):
    for j in range(1, 7):

        tot = i + j #맞춤!

        if tot == 6:
            print('첫번째 주사위 : %d, 두번째 주사위 : %d' % (i, j))
            
            
"""
이름 : 박민지
날짜 : 2021/04/08
내용 : 파이썬 연습문제. - 문자열이 "12345" 라면, '1+2+3+4+5' 결과 15를 출력하는 프로그램을 작성하시오.
"""

str = '12345'
sum = 0

for i in range(len(str)):

    num = int(3) #(str[i]) #왜 int가 있어냐 되냐면 문자가 아니라 숫자가 되야되서
    sum += num

print('합 :', sum)

"""
이름 : 박민지
날짜 : 2021/04/08
내용 : 파이썬 연습문제 2. 다이아몬드 출력
"""

count = 0

for i in range(1, 10):

    if i <= 5:
        count += 1
    else:
         count -= 1 #맞춤!

    for j in range(5-count):
        print(' ', end='')

    for k in range(count*2 - 1):
        print('*', end='')

    print()
    
    
"""
이름 : 박민지
날짜 : 2021/04/08
내용 : 파이썬 연습문제 3. 피보나치 수열
"""

n1 = 1
n2 = 2

print(n1, end=',')
print(n2, end=',')

for i in range(1, 10):
    n3 = n1 + n2
    print(n3, end=',')

    n1 = n2 #자리교환
    #n2 = n3
    
    
"""
이름 : 박민지
날짜 : 2021/04/08
내용 : 파이썬 최대값 최소값 연습문제, 교재 p.104
"""

scores = [62, 82, 76, 88, 54, 92]

max = scores[0]
min = scores[0]

for score in scores:

    if max < score:
        max = score

    if min > score:
        min = score

print('최대값 :', max)
print('최소값 :', min)


"""
이름 : 박민지
날짜 : 2021/04/08
내용 : 파이썬 선택정렬 연습문제
"""

dataset = [3, 5, 1, 2, 4]
size = len(dataset)

for i in range(size - 1):

    for j in range(i+1, size):

        if dataset[i] > dataset[j]:
            tmp = dataset[i]
            #dataset[i] =dataset[j]
            dataset[j] = tmp

    print('%d Round : %s' % (i, dataset))

print('Result :', dataset)


"""
이름 : 박민지
날짜 : 2021/04/08
내용 : 파이썬 이진검색 연습문제.
"""

dataset = [5, 10, 18, 22, 35, 55, 75, 103, 152]
value = int(input('검색할 숫자 입력 :'))

start = 0
end = len(dataset) -1
loc = 0
state = False

while start <= end:
    mid = (start + end) // 2

    if dataset[mid] > value:
        end = #mid - 1
    elif dataset[mid] < value:
        start = # mid + 1
    else:
        loc = mid
        state = True
        break

if state:
    print('찾은 위치 : %d번째' % (loc + 1))
else:
    print(('찾는 숫자가 없습니다.'))
