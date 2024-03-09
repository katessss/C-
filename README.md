//ФИБОНАЧИ
/*
#include <climits>
int main() {
  int n=0, x = 0, y = 1, z = 0, MAX;
  long int s=0;
  //std::cout << "введите MAX: ";
  //std::cin >> MAX;
  MAX=INT_MAX;
  while (s+y < MAX) {    
    s = s + y;
    n=n+1;
    //std::cout << n << "\t" << y << "\n";
    z = x + y;
    x = y;
    y = z;    
  }
  std::cout << "количество: " << n << ", ";
  std::cout << "сумма: " << s;
}
*/

//ФУНКЦИЯ
/*
#include <cmath>  
int main() {
  double dx, x, x1, x10, f;
  std::cout << "введите начало диапозона: ";
  std::cin >> x1;
  std::cout << "введите конец диапозона: ";
  std::cin >> x10;
  
  if (x1<0 || x1==0.0  || x10>4 || x1>x10 || x1==x10) {
    std::cout << "Error";
    return 0;
  }

  dx=(x10-x1)/9.0;
  x=x1;
  while (x<x10+dx) {
    f=sin(x)/x;
    x=x+dx;
    std::cout << f << '\n';
  }
}
*/


//МАССИВЫ

//1
/*
int main()
{
    int Arr[10]; 
    for (int i = 0; i < 10; i++)
    
    { Arr[i] = i*i;
    }
    for (int i = 0; i < 10; i++) // вывод на экран
    {
        std::cout << Arr[i] << "\t";
    }
}
*/

//2
/*
int main()
{
  int Arr[10];
  int *b = Arr;
  int *a = Arr;
  for (int i = 0; i < 10; a++, i++)
  {
    *a = i*i;
  }


  for (int i = 0; i < 10; b++, i++)
    {
      std::cout << *b << "\t"; 
    }
}
*/


//3
/*
int main()
{
    int *Arr;
    Arr = new int[10];
    for (int i = 0; i < 10; i++)
    {
        Arr[i] = i*i;
    }
    for (int i = 0; i < 10; i++)
    {
        std::cout << Arr[i] << "\t";
    }
    delete[]Arr; 
}
*/

//4
/*
int main()
{
  int *Arr;
  Arr = new int[10];
  int *b = Arr;
  int *a = Arr;
  for (int i = 0; i < 10; i++, a++)
  {
    *a = i*i;
  }
    for (int i = 0; i < 10; i++, b++)
    {
        std::cout << *b << "\t";
    }
    delete[]Arr; 
}
*/


//МАССИВЫ СТРОК (lab 9)
/*
#include <cstring>
int main()
{
  std::cout << "количсетво слов: ";
  int n, len=10;
  std::cin >> n;
  if (n > 20) {
    std::cout << "В массиве должно быть не более 20 слов";
    return 0;
  }
  
  char Arr[n][len+1]; 
  
  for (int i = 0; i < n; i++)
    {
      std::cin >> Arr[i]; 
      if (strlen(Arr[i]) > len) {
        std::cout << "В слове должно быть не более 10 символов ";
        return 0;
      }
    }

  std::cout << "вывод: ";
  for (int i = 1; i < n; i=i+2)
  {
    std::cout << Arr[i] << "\t";
  }
}
*/

//lab 10.2 (гармошка)
//подпрваить надо (прочитай задание)
/*
int main()
{
  int n, k, i;
  std::cout << "количество: ";
  std::cin >> n;
  int *Arr;
  Arr = new int[n];

  std::cin >> Arr[0];

  i = 1; 
  while (i < n) 
  {
    std::cin >> k;
    if (k >= Arr[i-1])
    {
      Arr[i] = k;
      //std::cout << Arr[0] << "\t";
      //std::cout << Arr[i] << "\t";
      i = i + 1;
    }   
  }
  
//упаковывает 
  int Cnt[17];
  i = 0;
  for (int j = 0; j <= 17; j++)
    {
      Cnt[j] = 0; 
      while (Arr[i] == j) 
        {
          Cnt[j] = Cnt[j] + 1;
          i = i + 1;
        }
    }
  delete[]Arr; 

//распаковывает
  for (int j=0; j<=17; j++)
    {
      while (Cnt[j] > 0)
        {
          std::cout << "\n" << j;
          Cnt[j] = Cnt[j] - 1;
        }   
    }
  
  
}
*/


//lab 10.1(объяснение)
/*
#include <cstring>
int abc(char *s)
{
  s++;
  return strlen(s);
}

int main()
{
 int i;
  //char *s = nullptr;
  int a[5];
  char *s = strdup("qwer");
  for (i=0; i<5; i++)
    {
      a[i]=abc(s);
      std::cout << a[i] << "\t";
    }
}


#include <cstring>
int abc(char **s)
{
  (*s)++;
  return strlen(*s);
}

int main()
{
 int i;
  //char *s = nullptr;
  int a[5];
  char *s = strdup("qweretui");
  for (i=0; i<5; i++)
    {
      a[i]=abc(&s);
      std::cout << a[i] << "\t";
    }
}
*/

  
}
