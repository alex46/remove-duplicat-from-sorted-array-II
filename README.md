remove-duplicat-from-sorted-array-II
====================================
public class Solution {
    public int removeDuplicates(int[] A) {
        // Start typing your Java solution below
        // DO NOT write main() function
     if(A.length==0) return 0;
     if(A.length <= 2) return A.length;
     
     int j = 0;
     int count = 1;
     
     for(int i = 1; i < A.length; i++){
         if(A[i] == A[j]){
             if(count < 2){
                 A[++j] = A[i];
               
                 count++;
             }
         }
         else{
             A[++j] = A[i];
          
             count = 1;
         }
         
     }
     return j+1;
        
    }
}
