# Ques1
int main() {
    int t;
    scanf("%d",&t);
    while(t){
        t=t-1;
        int a[100];int max;int min;int n;int d;
        scanf("%d %d",&n,&d);
        for(int i=0;i<n;i++){
            scanf("%d",&a[i]);
        }
        int count=1;
        int m=1;;
        for(int i=0;i<n;i++){
            if((a[i+1]-a[i])<=d && (a[i+1]-a[i]>0)){
                count++;
                m=count;
            }
            else if(a[i+1]-a[i]>d ){
                count=1;
            }
            a[i]=m;
            if(count==1 && i==n-2)
                a[i]=1;
            if(i>=3 && a[i-2]==a[i-1] && a[i]==a[i-1])
                a[i]=1;
            }
        max=a[0];
        min=a[0];
        for(int i=0;i<n-1;i++){
            if(a[i]<min)
                min=a[i];
            else if(a[i]>max)
                max=a[i];
        }
        if(max==n){
            printf("%d %d",max,max);
        }
        else
            printf("%d %d",min,max);
        printf("\n");
        }
    return 0;
}
