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
<><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><>
**Call By Value**

#include<iostream>
using namespace std;

void swap(int a, int b){
    int temp;
    temp=a;
    a=b;
    b=temp;
}
int main(){
    int a=100, b=200;

    swap(a,b);
    cout<<" Value of a: "<< a<<endl;
    cout<<"Vale of b: "<< b;
    
    return 0;
}

<><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><>

**call by value**
#include<iostream>
using namespace std;

void swap( int x, int y){
    int t=x;
    x=y;
    y=t;
    cout<<"Inside function :x : "<< x<<" y: "<< y<< endl;
    cout<<"Inside function :x : "<< x<<" y: "<< y<< endl;
}
int main(){
    int a=3,b=5;
    cout<<"before Swap: a is: "<<a<<" b: "<<b<<endl;
    swap(a,b);
    cout<<"After Swap:a is : "<< a<<"b: "<<b<<endl;
    cout<<"After Swap:a is : "<< &a<<"b: "<<a<<endl;
    return 0;
}

<><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><>
**Swapping**
#include<iostream>
using namespace std;

void swap(int a, int b){
    int temp;
    temp=a;
    a=b;
    b=temp;
}
int main(){
    int a=100, b=200;
    swap(a,b);
    cout<<" Value of a: "<< a<<endl;
    cout<<"Vale of b: "<< b;
    
    return 0;
} 


<><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><>
**object to pointer**
#include <iostream>
using namespace std;
class ABC{
    public:
    int x=5;
    void display(){
        cout<<" x is : "<<x<<endl;
    }
};
int main(){
    ABC obj;
    ABC *p;
    p=&obj;
    p->display();
    (*p).display();
}

<><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><>
**dangling pointer**
#include<iostream>
using namespace std;

void createDanglingPointer(){
    int *ptr = new int(10);  // Dynamically allocate memory for an integer and assign it the value 10
    cout << "Value: " << *ptr << endl;  // Output the value of the dynamically allocated memory (10)
    delete ptr;  // Free the allocated memory, making the pointer dangling
}

int main(){
    createDanglingPointer();  // Correct function call with parentheses
    return 0;
}

<><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><>

