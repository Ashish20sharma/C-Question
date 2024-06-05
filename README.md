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
leetcode Question 2273. Find Resultant Array After Removing Anagrams.
Ans:

    #include <bits/stdc++.h>
    using namespace std;
    bool anagram(string s1,string s2){
        sort(s1.begin(),s1.end());
        sort(s2.begin(),s2.end());
        return s1==s2;
    }
    int main()
    {
    vector<string>arr={"abba","baba","bbaa","cd","cd"};
    vector<string>res;
    res.push_back(arr[0]);
    for(int i=1;i<arr.size();i++){
        if(!anagram(arr[i-1],arr[i])){
            res.push_back(arr[i]);
        }
    }
    // for(auto it:res){
    //     cout<<it<<"\n";
    // }
    return res;
    return 0;
    }
--------------------------------------------------------------------------------------------
Q:11 input: {2,1,5,8,7}
     output: {9,3,6,13,15}
Ans:

    #include <bits/stdc++.h>
    using namespace std;

    int main()
    {
        vector<int>arr={2,1,5,8,7};
        vector<int>res;  //9 3 6 13 15
        for(int i=0;i<arr.size();i++){
            res.push_back(arr[i]+arr[arr.size()-1]);
            break;
        }
        for(int i=0;i<arr.size()-1;i++){
            res.push_back(arr[i]+arr[i+1]);
        }
        for(auto it:res){
            cout<<it<<" ";
        }
        return 0;
    }
----------------------------------------------------------------------------------------------
12.Given an array of integers, write a function that creates a frequency array to count the occurrences of each integer in the array.
Ans:

    #include <bits/stdc++.h>
    using namespace std;


    int main() {
    std::vector<int>arr={1,5,2,2,3,4,5,4,6,4,5} ;
    map<int,int>count;
    for(auto it:arr){
        count[it]++;
    }
    for(auto it:count){
        cout<<it.first<<" "<<it.second<<"\n";
    }
    return 0;
    }
---------------------------------------------------------------------------------------------
13. Write a function that takes an array of integers as input and returns the element that appears most frequently in the array. If there is a tie, return any of the most frequent elements.  
Ans:

        #include <bits/stdc++.h>
        using namespace std;


        int main() {
        std::vector<int>arr={1,5,2,2,3,4,5,4,6,4,4,4,5} ;
        map<int,int>count;
        for(auto it:arr){
            count[it]++;
        }
        int max=0;
        int maxfreq;
        for(auto it:count){
        if(it.second>max){
            max=it.second;
            maxfreq=it.first;
        }
        }
        cout<<maxfreq<<" "<<max;
        return 0;
        }
-------------------------------------------------------------------------------------------
14.Given an array of integers and a threshold value, write a function to find all elements whose frequency is above the given threshold.
Ans:

    #include <bits/stdc++.h>
    using namespace std;


    int main() {
    std::vector<int>arr={1,5,2,2,2,2,2,1,1,1,3,4,5,4,6,4,4,4,5} ;
    map<int,int>count;
    vector<int>newArr;
    int threshold=3;
    for(auto it:arr){
        count[it]++;
    }
    for(auto it:count){
    if(it.second>threshold){
       newArr.push_back(it.first);
    }
    }
    for(auto it:newArr){
        cout<<it<<" ";
    }
    return 0;
    }
------------------------------------------------------------------------------------------------
15.Write a function that takes a sentence as input and returns a frequency array (or dictionary) for the occurrences of each word in the sentence.
Ans:

    #include <bits/stdc++.h>
    using namespace std;


    int main() {
    vector<string>s={"hellow","hii","hellow"};
    map<string,int>count;
    for(auto it:s){
        count[it]++;
    }
    for(auto it:count){
        cout<<it.first<<" "<<it.second<<"\n";
    }
    return 0;
    }
------------------------------------------------------------------------------------------------















