
package Array;

public class RoataedElementLeftBy2 {
    public static void Rotate2(int arr[]){

        // //this brute force approach time O(n) space complexity O(n)

        int n= arr.length;
        int k=3;
        int temp[] = new int[n];
        for(int i=0; i<n-k;i++){
            temp[i] = arr[i+(k+1)-1];
        }
        // temp[n-1] = arr[2];
        // temp[n-2] = arr[1];
        // temp[n-3] =arr[0];
        
        for(int i =n-k;i<n;i++){
            temp[i] = arr[i-(n-k)];
         
        }
       
        for(int i=0;i<n; i++){
            System.out.print(temp[i]+" ");
        }



// //this brute force approach O(n+d)+O(n-d +n)+O(n) =O(n) space complexity O(d)
//     int n= arr.length;
//         int d=3;
//         int temp[] = {1,2,3};
//         for(int i =d; i<n; i++){
//             arr[i-d] = arr[i];
//         }
//         for(int i =n-d; i<n; i++){
//             arr[i] = temp[i-(n-d)];
//         }
//         for(int i =0; i<n; i++){
//         System.out.print(arr[i]+" ");        }
        
     }
    public static void main(String[] args) {
        int arr[]={1,2,3,4,5};
        Rotate2(arr);
        
    }
}
