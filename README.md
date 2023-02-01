class Solve {
    Pair getFloorAndCeil(int[] arr, int n, int x) {
      int f=-1;
      int c=-1;
     int high=n-1;
     Arrays.sort(arr);

    int low=0;

    while(low<=high){

        int mid=(low+high)/2;

        if(arr[mid]==x){

            c=arr[mid];

            f=arr[mid];

            break;

        }else if(arr[mid]<x){

            f=arr[mid];

            low=mid+1;

        }else{

            c=arr[mid];

            high=mid-1;

        }

    }
    return new Pair(f,c);
    }
}
