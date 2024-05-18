# C++ -Question

# C-Questions
Q:1 Write a C++ program that prints the first 10 numbers of a sequence where each number is the double of its predecessor, starting from 1, using a for loop.
Ans:

#include <bits/stdc++.h>

using namespace std;

void printNumber(double num){

    for(int i=1;i<11;i++){
        cout<<num<<" ";
        num*=2;
    }
}

int main()

{

    double num=1;
    
    printNumber(num);
    
    return 0;
}
------------------------------------------------------------------------------------------------------------------------------------------------------------
Q:2 Write a C++ program that generates and prints the first 15 terms of the sequence defined by: an​=2an−1​+1 with a1​=1 using a for loop. consider n is the nth term
Ans:

#include <bits/stdc++.h>

using namespace std;

int main() {

     int numTerms = 15;
    int a = 1;
    cout << "a1 = " << a << endl;
    for (int n = 2; n <= numTerms; ++n) {
        a = 2 * a + 1; 
        cout << "a" << n << " = " << a << endl;
    }
    return 0;
}

-----------------------------------------------------------------------------------------------------------------------------------------------------------
Q:3 Write a C++ program that sums all odd numbers between 1 and 50 but stops the summation when the sum exceeds 100 using a while loop.
Ans:

#include <bits/stdc++.h>

using namespace std;

int main() {

    int sum=0;
    int num=1;
     while(num<=50){
         if(num%2!=0){
         sum+=num;
         if(sum>100){
             break;
         }
     }
         num++;
     }
     cout<<sum;
    return 0;
}
------------------------------------------------------------------------------------------------------------------------------------------------------------
Q:4 Write a C++ program that iterates through the numbers from 1 to 100 and prints the number and its factorial but skips the factorial computation for prime numbers using a for loop.
Ans:

#include <bits/stdc++.h>

using namespace std;

bool isPrime(int num){

     if (num <= 1) {
        return false;
    }
    for(int j=2;j<num;j++){
        if(num%j==0){
            return false;
        }
    }
    return true;
}

int factorial(int number){

    if (number == 0 || number == 1) {
        return 1;
    }
    int fact=1;
    for(int k=1;k<=number;k++){
        fact=fact*k;
    }
    return fact;
}

int main() {

    for(int i=1;i<=100;i++){
        if(!isPrime(i)){
            int value=factorial(i);
            cout<<i<<" "<<value<<"\n";
        }else{
            cout<<"skips " << i<<" factorial for prime number"<<"\n";
        }
    }
    // cout<< factorial<<"\n";
    return 0;
}
----------------------------------------------------------------------------------------------------------------------------------------------------------


