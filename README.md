# sianse
인공신경망 그래프 그리기

-------------------------------------------
%matplotlib
import numpy as np
import matplotlib.pyplot as plt
------------------------------------------------
# 이동걸와 금액 각각x,y라는 이름의 넘파일 배열로 만든다
x = np.array([1, 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 23, 25, 27, 29, 31, 33])
y = np.array([61, 63, 65, 67, 68, 70, 72, 74, 76, 78, 80, 82, 84, 86, 88, 90, 92])


x2 = np.arange(0,20)
y2= a* x2 + b

mx = np.mean(x)
my = np.mean(y)

print("x의 평균값: ", mx)
print("y의 평균값:", my)

-------------------------------------------------------

divisor = sum([(i - mx)**2 for i in x])

def top(x,mx ,y ,my):
  d = 0
  for i in range(len(x)):
      d += (x[i] - mx ) * (y[i] -my)
  return d
dividend = top(x,mx,y,my)

print("분모:",divisor)
print("분자:",dividend)

-------------------------------------------

a = dividend / divisor

b = my - (mx*a)

print("기울기 a = " , a)
print("y절편 b =",b)

--------------------------
import matplotlib.pyplot as plt
import numpy as np

# 예시 데이터 (입력된 데이터)
x = np.array([1, 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 23, 25, 27, 29, 31, 33])
y = np.array([61, 63, 65, 67, 68, 70, 72, 74, 76, 78, 80, 82, 84, 86, 88, 90, 92])

# 선형 회귀선 (예측)
m, b = np.polyfit(x, y, 1)
y_pred = m * x + b

# 그래프 그리기
plt.scatter(x, y, color='blue', label='입력된 데이터')  # 산점도
plt.plot(x, y_pred, color='red', label='예측')  # 선형 회귀선

# 레이블 추가
plt.xlabel('시간')
plt.ylabel('수치')
plt.title('산점도 예시')

# 레전드 추가
plt.legend()

# 그래프 출력
plt.show()
----------------------------------------------

