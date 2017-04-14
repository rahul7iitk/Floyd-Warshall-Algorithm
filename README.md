# Floyd-Warshall-Algorithm
#include <bits/stdc++.h>
using namespace std;

int main() {
	int n;
	cin>>n;
	
	int table[n][n];
	
	for(int i=0;i<n;i++)
	{
	 for(int j=0;j<n;j++)
	 cin>>table[i][j];
	}
	
	int path[n][n];
	
	for(int i=0;i<n;i++)
	{
	 for(int j=0;j<n;j++)
	 {
	  if(table[i][j]<100000)
	  path[i][j]=i;
	  else
	  path[i][j]=-1;
	 }
	}
	for(int i=0;i<n;i++)
	path[i][i]=-1;
	
	for(int k=0;k<n;k++)
	{
	 for(int i=0;i<n;i++)
	 {
	  for(int j=0;j<n;j++)
	  {
	   if(table[i][j]>table[i][k]+table[k][j])
	   {
	       table[i][j]=table[i][k]+table[k][j];
	       path[i][j]=path[k][j];
	   }
	  }
	 }
	}
	
	for(int i=0;i<n;i++)
	{
	 for(int j=0;j<n;j++)
	 cout<<table[i][j]<<" ";
	 cout<<endl;
	}
	
	return 0;
}
	
	       
	       
	       
	       
	       
	       
	       
	       
	       
	       
	       
	       
	       
	  
	  
	 
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	 
	 
	
	
	
