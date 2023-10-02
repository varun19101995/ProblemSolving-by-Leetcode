Que.1 Set Matrix 0 (if an element is 0 then set its corresponding row & col as 0)
import java.util.* ;
import java.io.*; 
public class Solution {
    public static ArrayList<ArrayList<Integer>> zeroMatrix(ArrayList<ArrayList<Integer>> matrix, Integer n, Integer m) {
    	// Write your code here.
      if(n>1 && m>1)
      {
        for(int row=0;row<n;row++)
        {
            for(int col=0;col<m;col++)
            {
                if(matrix.get(row).get(col)==0)
                {
                    setRowColZero(matrix,n,m,row,col);
                }
            }
        }
       for(int i=0;i<n;i++)
        {
            for(int j=0;j<m;j++)
            {
                if(matrix.get(i).get(j)==-1)
                {
                    matrix.get(i).set(j, 0);
                }
            }
        }
      }
        return matrix;
    }
    public static void setRowColZero(ArrayList<ArrayList<Integer>> matrix, int n,int m,int row, int col)
    {
        for(int i=0;i<m;i++)
        {
            if(matrix.get(row).get(i)!=0)
            {
                matrix.get(row).set(i,-1);
            }
        }
          for(int i=0;i<n;i++)
        {
            if(matrix.get(i).get(col)!=0)
            {
                matrix.get(i).set(col,-1);
            }
        }

    }
    
}
