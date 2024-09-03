#include<iostream>
using namespace std;


class MazeSolver{
    public:
   static const int m =10;
   static const int n=5;

   int sol[m][n]={{0,0,0,0,0},{0,0,0,0,0},
   {0,0,0,0,0},{0,0,0,0,0},
   {0,0,0,0,0},{0,0,0,0,0},
   {0,0,0,0,0},{0,0,0,0,0},
   {0,0,0,0,0},{0,0,0,0,0},
   };

    bool move(int maze[m][n],int x,int y)
    {
        if(x>=0 && x<m && y>=0 && y<n &&maze[x][y] ==1)
        return true;
      return false;
    }

    bool solution(int maze[m][n],int x ,int y)
     {
        if(x == m-1 && y == n-1)
        {
           sol[x][y]=1;
           return true;
        }

      if(move(maze,x,y)== true)
      {
         sol[x][y]=1;

         if(solution(maze,x+1,y))
         {
            return true;
         }
         if(solution(maze,x,y+1))
         {
            return true;
         }

         sol[x][y]=0;
         return false;
      }

     
     return false;
     }
void printSolution()
{
   for(int i=0;i<m;i++)
   {
      for(int j=0;j<n;j++)
      {
         cout<<sol[i][j]<<"";
      }
      cout<<endl;
   }
}
};

int main()
{
   MazeSolver solver;
   int maze[MazeSolver::m]
   [MazeSolver::n]={{1,0,0,0,0},{1,1,1,1,0},{0,0,0,1,0},{1,1,1,1,0},{0,0,0,1,0},{0,0,0,1,0},
   {0,0,0,1,0},{0,0,0,1,0},{0,0,0,1,0},{0,0,0,1,1},};
   if(solver.solution(maze,0,0))
   {
      solver.printSolution();
   }
else
cout<< "No solution exits"<<endl;
return 0;
}
