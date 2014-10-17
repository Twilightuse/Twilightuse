#include<stdlib.h>
#include<string.h>
#include<algorithm>
#include<stdio.h>
#define MAX 509
#define LL long long int
using namespace std;
LL num[MAX];
int main() {
    int N,i;
    while(~scanf("%d",&N)) {
        for(i=0; i<N; i++) {
            scanf("%I64d",&num[i]);
        }
        sort(num,num+N);
        double ans=num[0];
        for(i=1; i<N; i++) {
            num[i]+=num[i-1];
            ans+=num[i];
        }
        printf("%.2lf\n",ans/N);
    }
    return 0;
}
/***
10
56 12 1 99 1000 234 33 55 99 812
***/
