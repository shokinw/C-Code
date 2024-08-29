About function Overloading

#include<iostream>
using namespace std;

int add( int a, int b){
    return a+b;
}
int add(int a,int b,int c){
    return a+b+c;
}
int main(){
    int sum1=add(6,7);
    int sum2=add(2,3,4);
    cout<< endl << "Sum1 : "<< sum1;
    cout<< endl << "Sum2 : "<< sum2;
    
    return 0;
}
