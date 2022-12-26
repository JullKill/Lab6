#include <stdio.h>
#include <stdlib.h>
#include <math.h>
int non(float fact) {
    float p = 1;
    for (int i = 1; i<=fact; i++){
        p*=i;
    }
        return p;
    }
    int main(){
        float x, eps, n = 0, sum = 0;
        printf("Input x =\n");
        scanf("%f", &x);
        printf("Input eps =\n");
        scanf("%f", &eps);
        if (eps>= 1 || eps <=0){
            printf("Input other eps =\n");
            scanf("%f", &eps);
        }
        else{
                while (((powf(x, 2*n))/(powf(2,n)*(non(n))))>eps){
                        if (x!=0){
                        sum = sum + ((powf(x, 2*n))/(powf(2,n)*(non(n))));
                        n++;}
                        else {
                        printf("Input other x =\n");
                        scanf("%f", &x);
            }
        }
    }
        
printf("sum = %f\n", sum);
return 0;
}
