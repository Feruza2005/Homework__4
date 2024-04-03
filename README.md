# Homework__4
#include <iostream>
#include <math.h>
using std::cout;
using std::cin;
using std::endl;


 int main(){
     
    cout<<"PROBLEM 1\n";
    int N, prime, counter;
    prime =0;
    counter = 1;
    cout<<"Enter a number: ";
    cin>>N;
    
    
    for (prime = 1; prime < N; prime++){
        if (N%prime==0){
            counter= counter + 1 ;
        }
    }
    cout<<counter<<endl;
    
    cout << "PROBLEM 2\n";
    int Number, i, r, k,l ; 
    
    
    cout <<"Enter a digit: ";
    cin>> Number;
    if (Number>=1 && Number<=9){
        for (int i = Number; i >= 1; --i) {
        for (int r = 1; r <= i; ++r) {
            cout << r;
        }
        for (int k = 0; k < 2 * (Number - i); ++k) {
            cout << " ";
        }
        for (int l = i; l >= 1; --l) {
            cout << l;
        }
       cout << endl;
    }

    cout <<endl;
    
    cout<<"PROBLEM 3\n";
    int a, Counter, Sum, first, second, third;
    Counter = 2;
    cout<<"Enter a number: ";
    cin>>a;
    
    first = 0;
    second = first+1;
    third = first + second;
    
    while (a>Counter){
        Sum = first + second + third;
        Counter ++;
        first = second;
        second = third;
        third = Sum;
    }
    cout << third<<endl;
    
    if (a==0){
        cout<<"0"<<endl;
    }
    if (a ==1 || a == 2){
        cout<<"1"<<endl;
    }
    
    cout<<"PROBLEM 4\n";
    int number, x, y, z;
    cout<<"Enter a number: ";
    cin>>number;
    
    for (x = -10; x <= 10; ++x){
        for (y = -3 ; y <=3 ; ++y){
            for (z = 2; z<=6; ++z){
                if (x*y*z < number && pow(x,2)+pow(y,2)+pow(z,2)> 8 ){
                    4*x - 2*y + 3*z == 20;
                    cout <<"Solution: "<<x<<" "<<y<<" "<<z<<" "<< endl;
                    
                }
            }
        }
    }
    cout <<endl;
    
    cout<<"PROBLEM 5\n";
    int rounds, shift_factor, d, temp;
    char Char, ans;
    cout<<"Enter a Char, shift factor and rounds: ";
    cin>>Char>>shift_factor>>rounds;
    
    temp = (int)Char;
    
    for (d = 1 ; d<=rounds; ++d ){
        temp = shift_factor + (int)temp;
        ans = (char)temp;
    }
    cout << ans << endl;
    
 }
 }
