# maximum-occurence-of-character-in-string-in-cpp

**PROBLEM STATEMENT**
you are given a string ,find the occurence of character which appears maximum in the input string.

if there are more characters ofsame frequency in  string ,print 0 else print maximum occurence of character

**INPUT:**
ABSDGCA

**OUTPUT:**
2

**INPUT:**
ABAPRCKB

**OUTPUT:**
0

  **CODE**
```

#include<bits/stdc++.h>
using namespace std;

int main()
{
    string s;
    cin>>s;
    unordered_map<char,int>mp;
     for(int i=0;i<s.size();i++)
     {
         mp[s[i]]++;
     }
     int mx=-1;
     for(auto i:mp)
     {
         if(i.second>mx)
         {
             mx=i.second;
         }
     }
     int cnt=0;
     for(auto i:mp)
     {
         if(mx==i.second)
         {
             cnt++;
         }
     }
     if(cnt==1)
     {
         cout<<mx<<endl;
     }
     else
     {
         cout<<0<<endl;
     }
     
}



