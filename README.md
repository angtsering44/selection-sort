# selection-sort
#include <stdio.h>

int main() {
    int list[100], size, temp;

    printf("Enter number of elements: ");
    scanf("%d", &size);

    printf("Enter %d numbers:\n", size);
    for(int i = 0; i < size; i++) {
        scanf("%d", &list[i]);
    }

   
    for(int i = 0; i < size; i++) {
        for(int j = i + 1; j < size; j++) {
            if(list[i] > list[j]) {
                temp = list[i];
                list[i] = list[j];
                list[j] = temp;
            }
        }
    }

    printf("Sorted numbers:\n");
    for(int i = 0; i < size; i++) {
        printf("%d ", list[i]);
    }

    return 0;
}
