#include <bits/stdc++.h>
using namespace std;

void dfs(vector<vector<char>>&grid,int n,int m,int visited[][501],int i,int j)
    {
        if(i<0 or j<0 or i>=n or j>=m)return;
        if(grid[i][j]=='0')return;
        if(visited[i][j]==0)
        {
            visited[i][j]=1;
            dfs(grid,n,m,visited,i,j+1);
            dfs(grid,n,m,visited,i,j-1);
            dfs(grid,n,m,visited,i-1,j);
            dfs(grid,n,m,visited,i+1,j);
            dfs(grid,n,m,visited,i+1,j+1);
            dfs(grid,n,m,visited,i+1,j-1);
            dfs(grid,n,m,visited,i-1,j-1);
            dfs(grid,n,m,visited,i-1,j+1);
        }
    }
    

int numIslands(vector<vector<char>>& grid) 
    {
        
        int n=grid.size();
        int m = grid[0].size();
        int visited[501][501];
        for(int i=0;i<n;i++)
        {
            for(int j=0;j<m;j++)
            {
                visited[i][j]=0;
            }
        }
        int c=0;
        for(int i=0;i<n;i++)
        {
            for(int j=0;j<m;j++)
            {
                if(visited[i][j]==0 && grid[i][j]=='1')
                {
                    dfs(grid,n,m,visited,i,j);
                    c++;
                }
            }   
        }
        return c;
    }


int main()
{
    int n,m;
    cout<<"Enter dim: ";
    cin>>n>>m;
    vector<vector<char>> M(n);
    cout<<"Enter matrix:"<<endl;
    for (int i=0;i<n;i++){
        for(int j=0;j<m;j++)
        {
            char x;
            cin>>x;
            M[i].push_back(x);
        }
    }
    
    cout<<"Number of Island: "numIslands(M);
    
}
