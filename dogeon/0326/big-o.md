## 시간 복잡도

- 빅오 표기법의 특징을 말하시오

1. 시간 복잡도의 점근적 상한을 나타낸다.
2. 시간 복잡도 다항식의 최고차항만을 계수없이 사용한다.

   - 상수항은 무시
   - 상대적으로 영향이 작은 항은 무시




- T(n) = T(n-1) + n, T(0) = 1 의 시간복잡도를 구하시오

n = n-1, T(n-1) = T(n-2) + n - 1

​			=> T(n) = T(n-2) + n - 1 + n



n = n-2, T(n-2) = T(n-3) + n - 2

​        	=> T(n) = T(n-3) + n - 2 + n - 1 + n



n = n-3, T(n-3) = T(n-4) + n -3

​			=> T(n) = T(n-4) + n - 3 + n -2 + n - 1 + n

​						=> T(n-k) + k*n - (k-1) - (k-2) - ... -1



n = k, T(n) = T(0) + n^2 - (1+2+3+...+(n-1))

​				=> T(0) + n^2 - ((n-1)n)/2

​				=> T(0) + n^2 - (1/2)n^2 - (1/2)n

​				=> T(0) + (1/2)n^2 - (1/2)n

따라서, 시간복잡도는 O(n^2) 이다.