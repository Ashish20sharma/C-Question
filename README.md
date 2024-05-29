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

Q:5 using proper logic:

print

a)

                       1 2 3 4
                       1 2 3
                       1 2
                       1
     
                        2 3 4
                        2 3
                        2
     
                        3 4
                        3
     
                        4
Ans:

    #include <iostream>

    using namespace std;

    int main()

    {

    for(int k=0;k<4;k++){
    for(int i=k;i<4;i++){
        for(int j=1;j<=4-i;j++){
            cout<<j+k<<" ";
        }
        cout<<"\n";
    }
    cout<<"\n";
    }

    return 0;
    
    }
--------------------------------------------------------------------------------------------------------
b)

                       4 3 2 1
                       4 3 2
                       4 3
                       4

                       3 2 1
                       3 2
                       3

                       2  1
                       2

                       1
Ans:

    #include <iostream>

    using namespace std;

    int main()

    {

    for(int k=0;k<4;k++){
    for(int i=k;i<4;i++){
        for(int j=4;j>i;j--){
            cout<<j-k<<" ";
        }
        cout<<"\n";
    }
    cout<<"\n";
    }

    return 0;
    
    }
--------------------------------------------------------------------------------------------------------
c)

    4
    4 3
    4 3 2
    4 3 2 1

Ans:

    #include <iostream>

    using namespace std;

    int main()

    {

    for(int i=4;i>=1;i--){
        for(int j=4;j>=i;j--){
            cout<<j<<" ";
        }
        cout<<"\n";
    }

    return 0;
    
    }
--------------------------------------------------------------------------------------------------------
d)

              1
              1 2
              1 2  3
              1 2 3 4

              2 
              2 3
              2 3 4

              3
              3 4

              4
Ans:

    #include <iostream>

    using namespace std;

    int main()

    {

    for(int k=0;k<4;k++){
        for(int i=0;i<4-k;i++){
            for(int j=1;j<=i+1;j++){
                cout<<j+k<<" ";
            }
            cout<<"\n";
        }
        cout<<"\n";
    }

    return 0;
    
    }
-------------------------------------------------------------------------------------------------------------------------------
6.Write a program to print all elements of an array.
Ans:

    #include <bits/stdc++.h>
    using namespace std;
    int main()
    {
    vector<int> numbers={1,2,3,4,5};
    for(int i=0;i<numbers.size();i++){
       cout<<numbers[i]<<"\n";
       }

    return 0;
    }
-----------------------------------------------------------------------------------
7. Write a program to find the sum of all elements in an array.
Ans:

       #include <bits/stdc++.h>
       using namespace std;

        int main() 
        {
        vector<int> numbers={1,2,3,4,5};
        int sum=0;
        for(int i=0;i<numbers.size();i++){
          sum+=numbers[i];
        }
        cout << sum ;
        return 0;
    }
-----------------------------------------------------------------------------------
8. Write a program to find the largest element in an array.
Ans:

        #include <bits/stdc++.h>
        using namespace std;

        int main() 
        {
        vector<int> arr={1,2,5,4,12,10};
        int largest=arr[0];
        for(int i=0;i<arr.size();i++){
          if(largest<arr[i]){
            largest=arr[i];
          }
        }
        cout <<largest;
        return 0;
    }
------------------------------------------------------------------------------------
9.Write a program to find the smallest element in an array.
Ans:

    #include <bits/stdc++.h>
    using namespace std;

    int main() 
    {
    vector<int> arr={1,2,5,4,12,10};
    int largest=arr[0];
    for(int i=0;i<arr.size();i++){
      if(largest>arr[i]){
        largest=arr[i];
      }
    }
    cout <<largest;
    return 0;
    }
------------------------------------------------------------------------------------
10. Write a program to find the average of elements in an array.

    
        #include <bits/stdc++.h>
        using namespace std;

        int main() 
        {
        vector<int> arr={1,2,5,4,12,10};
        double avg=0.0;
        for(int i=0;i<arr.size();i++){
          avg=avg+arr[i];
        }
        cout <<avg/arr.size();
        return 0;
    }
--------------------------------------------------------------------------------------
10. Write a program to count the number of even and odd elements in an array.

        #include <bits/stdc++.h>
        using namespace std;

        int main() 
        {
        vector<int> arr={1,2,4,3,5,6,7,8};
        int even=0;
        int odd=0;
        for(int i=0;i<arr.size();i++){
          if(arr[i]%2==0){
            even++;
          }else if(arr[i]%2!=0){
            odd++;
          }
        }
        cout<<"Even:"<<even<<" Odd:"<<odd;
        return 0;
    }
--------------------------------------------------------------------------------------
11. Reverse Integer.
Ans:

        #include <bits/stdc++.h>
        using namespace std;

        int main()
        {
           int num =12345;
           long r=0;
           int sum;
           while(num){
               r=num%10;
               sum=sum*10+r;
               num=num/10;
           }
            cout<<sum;
            return 0;
        }
-----------------------------------------------------------------------------------------
12. Check Anagram?
Ans:

    


















