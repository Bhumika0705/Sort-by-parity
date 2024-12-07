# Sort-by-parity
Sorting by parity
public class sortbyparity {
    public static int[] sortByParity(int[] a){
        int i =0;
        int j = a.length-1;
        while (i<j){
            if (a[i]%2==1&& a[j]%2==0){
                int temp = a[i];
                a[i]=a[j];
                a[j]=temp;
                i++;
                j--;
            }
            if (a[i]%2==0)i++;
            if (a[j]%2==1)j--;

        }
        return a;
    }

    public static void main(String[] args) {
        int[] a = { 2,7,4,9,6};
        int[] ans = sortByParity(a);
        for (int element : ans){
            System.out.println(element + " ");
        }
    }
}
