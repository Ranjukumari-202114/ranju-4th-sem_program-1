# ranju-4th-sem_program-1

/*Write the program to read a matrix from your keyboard and display 
the same by using functions.*/

#include <iostream>
using namespace std;

#define m 3                              //creating pre processor
#define n 3

class Matrix                             //creating class named Matrix
{
    int arr[m][n];                       
    public:
    void Mat(int,int);                   //declaring member function in class
    void print();                        //declaring member function in class
};
void Matrix::Mat(int row,int column)     //defining member function of matrix class outside
{
    cout<<"Enter your matrix :["<<m<<"]["<<n<<"]"<<endl;
    for (int i=0;i<m;i++) 
    {
        for(int j=0;j<n;j++)
        {   
            cout<<"Enter the element at position ["<<i<<", "<<j<<"]:";
            cin>>arr[i][j];
        }
    }
    cout<<endl;
}
void Matrix::print()                     //defining member function of matrix class outside
{
    cout<<"Matrix :\n";
      for (int i=0;i<m;i++) 
    {
        for(int j=0;j<n;j++)
        {
            cout<<arr[i][j]<<" ";
        }
        cout<<endl;
    }
}
int main()
{
    Matrix M1;                        //creating object of class matrix 
    M1.Mat(m,n);                      //function call
    M1.print();                       //function call

    return 0;
}
