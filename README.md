# ISit-2
#include <iostream>
#include <cmath>

using namespace std;


int main()
{
  int row, columnMatrix, sizeMatrix, count, matrix[5][5];
  float summ;
  count = 0;
  summ = 0;
  
  cout << "Введите размер матрицы" << endl;
  cin >> sizeMatrix;
  
  cout << "Введите элеметы матрицы" << endl;
  
  for (row = 0; row < sizeMatrix; ++ row) {
    for (columnMatrix = 0; columnMatrix < sizeMatrix; ++ columnMatrix) {
      cin >> matrix[row][columnMatrix];    
    }
  }
  
  cout << "Матрица" << endl;
  
  for (row = 0; row < sizeMatrix; ++ row) {
    for (columnMatrix = 0; columnMatrix < sizeMatrix; ++ columnMatrix) {
      cout << matrix[row][columnMatrix] << "\t";
    }
    cout << endl;
  }
  
  cout << "Элементы под главной диагональю" << endl;
  
  for (row = 0; row < sizeMatrix; ++ row) {
    for (columnMatrix = 0; columnMatrix < sizeMatrix; ++ columnMatrix) {
      if (row > columnMatrix) {
        cout << matrix[row][columnMatrix] << endl;
        count += 1;
        summ += matrix[row][columnMatrix];
      }
    }
  }
   
   cout << "Количество элементов" << endl;
   cout << count << endl;
   cout << "Сумма" << endl;
   cout << summ << endl;
   
}
