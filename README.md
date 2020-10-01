# Prime-Number-Solver
Simple C++ program to find whether an inputted number is prime
//
//  main.cpp
//  PrimeNumberFinderApp
//
//  Created by Duff Isberg in 2020.
//  Copyright (c) 2020 Duff Isberg. All rights reserved.
//

#include <iostream>
#include <cmath>
using namespace std;

bool primeNumberFunction(int primeNumberCheck)
{
    for(int i = 2;i<primeNumberCheck;i++)
    {
        if(primeNumberCheck%i == 0)
        {
            return 0;
            break;
        }
        if((primeNumberCheck - 1) == i)
        {
            return 1;
            break;
            
        }
    }
    return 0;
    
};


int main()
{
    int primeNumberCheck;
    char repeat = 'Y';
    while(repeat == 'Y')
    {
    cout<<"Enter the integer you wish to check is prime: "<<endl;
        bool function;
    
    cin>>primeNumberCheck;
        
        function = primeNumberFunction(primeNumberCheck);
    
    for(int i = 2;i<primeNumberCheck;i++)
    {
        if(primeNumberCheck%i == 0)
        {
            cout<<primeNumberCheck<<" is divisible by: "<<i<<", and therefore is not prime."<<endl;
            break;
        }
        if((primeNumberCheck - 1) == i)
        {
            cout<<primeNumberCheck<<" is a prime. It is only divisible by 1 and itself."<<endl;
        }
    }
        if(function == 1)
        {
            cout<<"yes"<<endl;
        }
    cout<<"Repeat? (Y/N)"<<endl;
        cin>>repeat;
        repeat = toupper(repeat);
    }
    cout<<"Goodbye!"<<endl;
    return 0;
}


