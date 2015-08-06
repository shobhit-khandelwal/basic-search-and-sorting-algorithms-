# basic-search-and-sorting-algorithms- actitvity selection
Implementation some algorithms in c++
#include<iostream.h>
#include<conio.h>
int a[15]={0,1,2,3,4,5,6,7,8,9,10,11,12,13,14};
/*ras(int s[],int f[],int i,int j)
{
int m;
m=i+1;
while(m<j && s[m]<f[i])
{
m++;
}
if(m<j)
{
cout<<" "<<a[m];
ras(s,f,m,j);
}
else
return 0;
}
void main()
{
  clrscr();
  int s[15],f[15],i,j,k,n,t;
  cout<<"\n Enter the number of activities (<15) ";
  cin>>n;
  for(i=0;i<n;i++)
  {
      cout<<"\n Enter the start time of activity number "<<i+1<<" : ";
      cin>>s[i];
      cout<<"\n Enter the finish time of activity number "<<i+1<<" : ";
      cin>>f[i];
  }
  for(i=0;i<n;i++)
  {
      for(j=i;j<n;j++)
      {
	 if(f[i]>f[j])
	 {
	    t=f[i];
	    f[i]=f[j];
	    f[j]=t;
	    t=s[i];
	    s[i]=s[j];
	    s[j]=t;
	 }
      }
  }
  for(i=0;i<n;i++)
  {
     cout<<" "<<i;
  }
  cout<<endl;
  for(i=0;i<n;i++)
  {

     cout<<" "<<s[i];
  }
  cout<<endl;
  for(i=0;i<n;i++)
  {
     cout<<" "<<f[i];
  }
  cout<<a[0];
  ras(s,f,0,n);




  getch();
} */
void main()
{
  clrscr();
  int s[15],f[15],i,j,n,m,t;
  cout<<"\n Enter the number of activities (<15) ";
  cin>>n;
  for(i=0;i<n;i++)
  {
      cout<<"\n Enter the start time of activity number "<<i+1<<" : ";
      cin>>s[i];
      cout<<"\n Enter the finish time of activity number "<<i+1<<" : ";
      cin>>f[i];
  }
  for(i=0;i<n;i++)
  {
      for(j=i;j<n;j++)
      {
	 if(f[i]>f[j])
	 {
	    t=f[i];
	    f[i]=f[j];
	    f[j]=t;
	    t=s[i];
	    s[i]=s[j];
	    s[j]=t;
	 }
      }
  }
  for(i=0;i<n;i++)
  {
     cout<<" "<<i;
  }
  cout<<endl;
  for(i=0;i<n;i++)
  {

     cout<<" "<<s[i];
  }
  cout<<endl;
  for(i=0;i<n;i++)
  {
     cout<<" "<<f[i];
  }

  cout<<" "a[0];
  i=0;
  for(m=1;m<n;m++)
  {
    if(s[m]>=f[i])
    {
      cout<<" "<<a[m];
      i=m;
    }
  }
  getch();
}
