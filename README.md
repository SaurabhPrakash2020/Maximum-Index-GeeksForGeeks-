# Maximum-Index-GeeksForGeeks-
Maximum Index is a medium level problem of GeeksForGeeks asked in several companies like Amazon,Microsoft,MakeMyTrip.I solved this problem using 3 pointers which is having time complexity of 0(N).
https://practice.geeksforgeeks.org/problems/maximum-index-1587115620/1?page=1&difficulty[]=1&status[]=unsolved&category[]=Arrays&sortBy=submissions

class Solution{
    static int maxIndexDiff(int A[], int N) { 
        int i=0;
        int j=N-1;
        int k=N-1;
        int maxAns=0;
        while(i<=j)
        {
            int ans=0;
            if(A[i]<=A[k])
            {
                ans=k-i;
                i++;
                k=j;
              if(ans>maxAns)
              {
                  maxAns=ans;
              }
            }
            else if(A[i]>A[k]){
                k--;
            }
            if(k==i)
            {
                k=j;
                i++;
            }
        }
        return maxAns;
    }
}

