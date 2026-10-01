#include<bits/stdc++.h>

using namespace std;

int main(){

    int n,m;
    
    cin>>n>>m;
    
    vector<string>a(n);
    for(auto&x:a)cin>>x;
    int r1=n,r2=-1,c1=m,c2=-1;
    for(int i=0;i<n;i++)
        for(int j=0;j<m;j++)
            if(a[i][j]=='*'){
                r1=min(r1,i);
                r2=max(r2,i);
                c1=min(c1,j);
                c2=max(c2,j);
            }
    for(int i=r1;i<=r2;i++){
        for(int j=c1;j<=c2;j++)
            cout<<a[i][j];
        cout<<'\n';
    }
}

