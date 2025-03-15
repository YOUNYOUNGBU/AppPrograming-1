# 1. 구구단 출력 코드

<pre>
<code>
void main() {
  for (int i = 2; i <= 9; i++) {
    print('$i단');
    for (int j = 1; j <= 9; j++) {
      print('$i x $j = ${i * j}');
    }
    print(''); 
  }
}
</code>
</pre>

# 결과 화면

![image](https://github.com/user-attachments/assets/03ab4c5e-a2a1-4408-ba20-5a6b0323cca1)
![image](https://github.com/user-attachments/assets/b8f735ff-5739-49d0-8219-70655b7c4aa9)
![image](https://github.com/user-attachments/assets/c13beb64-6196-40f1-833f-43c3e5ae9aed)

# 2. 정사각형의 길이를 입력하고 사각형을 출력하라
n = 10 일때

(1) 꽉찬 사각형 코드

<pre>
<code>
void main() {
   int size = 10;

  for (int i = 0; i < size; i++) {
    print('*' * size);
  }
}
</code>
</pre>

결과 화면

![image](https://github.com/user-attachments/assets/b3f2d7b0-1b0f-431e-913b-dfe6bd9ddbf8)

(2) 테두리 사각형 코드

<pre>
<code>
void main() {
  int size = 10;

  for (int i = 0; i < size; i++) {
    if (i == 0 || i == size - 1) {
 
      print('*' * size);
    } else {
    
      print('*' + ' ' * (size - 2) + '*');
    }
  }
}
</code>
</pre>

결과 화면

![image](https://github.com/user-attachments/assets/afe79b4c-455e-4738-85d7-66c450a67331)

(3) /표시 코드
<pre>
<code>
void main() {
  const int size = 10; 

  for (int i = 0; i < size; i++) {
    print(' ' * (size - i - 1) + '*');
  }
}
    </code>
</pre>

결과 화면

![image](https://github.com/user-attachments/assets/bf7fb28a-4481-49d1-8c62-92e4dfeeb34f)

(4) \표시 코드
<pre>
<code>
void main() {
  const int size = 10;

  for (int i = 0; i < size; i++) {
    print(' ' * i + '*'); 
  }
}
     </code>
</pre>

# 결과 화면

![image](https://github.com/user-attachments/assets/daa00fb3-f8c9-458d-b9b5-fe9553c82699)

(5) X표시 코드
<pre>
<code>
void main() {
   int size = 10; 

  for (int i = 0; i < size; i++) {
    String line = '';

    for (int j = 0; j < size; j++) {
      if (j == i) {
        line += '*';
      } else if (j == size - i - 1) {
        line += '*';
      } else {
        line += ' ';
      }
    }
    print(line);
  }
}
 </code>
</pre>

결과화면

![image](https://github.com/user-attachments/assets/6d865123-414e-48d2-9626-75908c428441)


# 3. 년/월/일을 입력하면 요일을 출력하는 코드
<pre>
<code>
void main() {

  var input = '2025-03-11';

  DateTime date = DateTime.parse(input);

  List<String> weekdays = ['월요일', '화요일', '수요일', '목요일', '금요일', '토요일', '일요일'];
  
  print('${weekdays[date.weekday - 1]}');
}
 </code>
</pre>

결과 화면

![image](https://github.com/user-attachments/assets/a343768d-045e-4017-9426-0e78a157b53e)
