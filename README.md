# longest-susbstring-without-repeatations
GIVEN A STRING TO FIND THE LENGTH OF LONGEST SUBSTRING WHITHOUT REPEATATIONS in C++
#
#
#include<bits/stdc++.h>

using namespace std;

int main()

{

 string s;
 
 cin>>s;
 
 vector<int> count(128);
	
  int left=0,right=0,res = 0;
	
        while (right < s.length()) 
																	
        {
																	
            count[s[right]]++;
																	
            while (count[s[right]] > 1) 
	
           {
	
                count[s[left]]--;
	
                left++;
	
            }

            res = max(res, right - left + 1);

            right++;
	
        }

        cout<<res;
	
  }

