#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>
//Complete the following function.


void calculate_the_maximum(int n, int k) {
    
    int maxAnd = 0;
    int maxOr = 0;
    int maxXor = 0;

    for (int i = 1; i < n; i++)
    {
        for (int j = i + 1; j < n + 1; j++)
        {
             int x = i & j;
             int y = i | j;
             int z = i ^ j;

             if (x > maxAnd && x < k) maxAnd = x;
             if (y > maxOr && y < k) maxOr = y;
             if (z > maxXor && z < k) maxXor = z;
        }
    }

    
    printf("%d\n", maxAnd);
    printf("%d\n", maxOr);
    printf("%d\n", maxXor);

}

int main() {
    int n, k;
  
    scanf("%d %d", &n, &k);
    calculate_the_maximum(n, k);
 
    return 0;
}
