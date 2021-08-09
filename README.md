#include<bits/stdc++.h>
#include<string>
using namespace std;
int main()
{
	int n;
	while(cin>>n)
	{
		getchar();
		int a[2018]={0};
		string t,s[2018];
		for(int i=0;i<n;i++)
		{
			int x=0;
			getline(cin,t);
			for(int i=t.length()-4;i<t.length();i++)
			{
				x=10*x+t[i]-'0';
			}
			t.erase(t.length()-4,4);
			a[x]=1;
			s[x]=t;
		}
		for(int i=0;i<2018;i++)
		{
			if(a[i])
			{
				cout<<i<<' '<<s[i]<<endl;
			}
		}
	}
	return 0;
}
