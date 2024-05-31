# Homework7
#include <iostream> 
#include <vector> 
using namespace std;


int multiply(int x, int y) { 

if (x == 0 || y == 0) { 
return 0; 
} 
if (y < 0) { 
return - multiply(x, -y); 
} 
return x + multiply(x, y - 1); 
} 
int sumOfDigits(int n) { 
if (n < 10) { 
return n; 
} 
number 
return n % 10 + sumOfDigits(n / 10); 
} 
void decimalToBinary(int n) { 
if (n == 0) { 
return; 
} 

decimalToBinary(n / 2); 

cout << n % 2; 
} 
vector<int> calculateRowSum(const vector<vector<int>>& arr) { 
vector<int> rowSums; 
for (const auto& row : arr) { 
int sum = 0; 
for (int num : row) { 
sum += num; 
} 
rowSums.push_back(sum); 
} 
return rowSums; 
} 
vector<vector<int>> matrixSum(const vector>vector<int>>& A, const 
vector<vector<int>>& { 
int m = A.size(); 
int n = A[0].size(); 
vector<vector<int>> result(m, vector<int>(n)); 
for (int i = 0; i < m; ++i) { 
for (int j = 0; j < n; ++j) { 
result[i][j] = A[i][j] + B[i][j]; 
} 
} 
return result; 
} 
int main() { 
cout<<"Problem_1"<<endl; 
int x, y; 

cout << "Enter two numbers: "; 
cin >> x >> y; 

cout << "Result: " << multiply(x, y) << endl;
cout<<"Problem_2"<<endl; 
int n_2; 

cout << "Enter a number: "; 
cin >> n_2; 
  
cout << "Sum of digits: " << sumOfDigits(n_2) << endl; 
cout<<"Problem_3"<<endl; 
int n_3; 
  
cout << "Enter a decimal number: "; 
cin >> n_3; 

cout << "Binary representation: "; 
decimalToBinary(n_3); 
cout << endl; 
cout<<"Problem_4"<<endl; 
int m, n; 
cout << "Enter the number of rows: "; 
cin >> m; 
cout << "Enter the number of columns: "; 
cin >> n; 
vector<vector<int>> matrix(m, vector<int>(n)); 
cout << "Enter the elements of the matrix:" << endl; 
for (int i = 0; i < m; ++i) { 
for (int j = 0; j < n; ++j) { 
cin >> matrix[i][j]; 
} 
} 
vector<int> rowSums = calculateRowSum(matrix); 
cout << "Row-wise sum:" << endl; 
for (int sum : rowSums) { 
cout << sum << " "; 
} 
cout << endl; 
cout<<"Problem_5"<< endl; 
int m_5, n_5; 
cout << "Enter the number of rows: "; 
cin >> m_5; 
cout << "Enter the number of columns: "; 
cin >> n_5; 
cout << "Enter the elements of matrix A:" << endl; 
vector<vector<int>> A(m_5, vector<int>(n_5)); 
for (int i = 0; i < m_5; ++i) { 
for (int j = 0; j < n_5; ++j) { 
cin >> A[i][j]; 
} 
} 
cout << "Enter the elements of matrix B:" << endl; 
vector<vector<int>> B(m_5, vector<int>(n_5));
for (int i = 0; i < m_5; ++i) { 
for (int j = 0; j < n_5; ++j) { 
cin >> B[i][j]; 
} 
} 
vector<vector<int>> result = matrixSum(A, B); 
cout << "Sum of matrices A and B:" << endl; 
for (int i = 0; i < m_5; ++i) { 
for (int j = 0; j < n; ++j) { 
cout << result[i][j] << " "; 
} 
cout << endl; 
} 
return 0; 
}
