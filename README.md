# oj 6-1 초기코드
#include <stdio.h>


char max_char(char char01, char char02) {
	if (char01 > char02) {
	return char01;
	}
	else {
		return char02;
	}
}

int max_int(int int01, int int02) {
	if (int01 > int02) {
		return int01;
	}
	else {
		return int02;
	}
}

float max_float(float float01, float float02) {
	if (float01 > float02) {
		return float01;
	}
	else {
		return float02;
	}
}




int main() {
	char a, b;
	int i, j;
	float f1, f2;

	scanf("%c %c", &a, &b);
	scanf("%d %d", &i, &j);
	scanf("%f %f", &f1, &f2);
	char char_result =  max_char(a, b);
	int int_result = max_int(i, j);
	float float_result = max_float(f1, f2);

	printf("max char is %c\n", char_result);
	printf("max int is %d\n", int_result);
	printf("max float is %f\n", float_result);
	
	return 0;
}

-----------------------------------------------------------
#헤성 코드
#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>

char max_1(char a, char b)
{
	if (a < b)
	{
		return b;
	}
	else
	{
		return a;
	}
}
int max_2(int i, int j)
{
	if (i < j)
	{
		return j;
	}
	else
	{
		return i;
	}
}
float max_3(float f1, float f2)
{
	if (f1 < f2)
		return f2;
	else
		return f1;
}
void max_a(int i, float f1)
{
	if (i < f1)
	{
		printf("max is %f\n",f1);
	}
	else
	{
		printf("max is %d\n", i);
	}
}
void max_b(char b, int j)
{
	if (b < j)
	{
		printf("max is %d\n",j);
	}
	else
	{
		printf("max is %c\n",b);
	}
}


int main(void) {
	char a, b;
	int i, j;
	float f1, f2;
	printf("char: ");
	scanf("%c %c", &a, &b);
	printf("int: ");
	scanf("%d %d", &i, &j);
	printf("float: ");
	scanf("%f %f", &f1, &f2);
	

	//아래 출력 코드를 보고 함수를 정의하라.
	printf("max char is %c\n", max_1(a, b));
	printf("max int is %d\n", max_2(i, j));
	printf("max float is %f\n", max_3(f1, f2));
	max_a(i, f1); //함수안에서 출력
	max_b(b, j);  //함수안에서 출력
	return 0;
}
---------------------------------------------------------

#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
int idx_1(int i, int j)
{
    return i*3 + j;
}
void print2x3(int mat[6])
{
    for (int i = 0; i < 2; i++)
    {
        for (int j = 0; j < 3; j++)
        {
            printf("%d ", mat[i * 3 + j]);
        }
        printf("\n");
    }
}
void idx_2(int i)
{
    int x, y;
    x = i / 3;
    y = i % 3;

    printf("(%d, %d)", x, y);
}
int main(void) {
    int matrix[6];
    //matrix값 입력
    scanf("%d %d %d", matrix + 0, matrix + 1, matrix + 2);
    scanf("%d %d %d", matrix + 3, matrix + 4, matrix + 5);

    printf("\nprint idx_1\n");
    for (int i = 0; i < 2; i++) {
        for (int j = 0; j < 3; j++) {
            printf("%d ", matrix[idx_1(i, j)]);
        }
    }
    printf("\n");

    printf("\nprint2x3\n");
    print2x3(matrix);

    printf("\nprint idx_2\n");
    for (int i = 0; i < 6; i++) {
        idx_2(i);
        printf(" ");
    }
    printf("\n");

    return 0;
}
-----------------------------------------------------------------
#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>

void scan_matrix(int mat[512], int r, int c)
{
	for (int i = 0; i < r; i++)
	{
		for (int j = 0; j < c; j++)
		{
			scanf("%d", &mat[i * c + j]);
		}
	}
}
void print_matrix(int mat[512], int r, int c)
{
	for (int i = 0; i < r; i++)
	{
		for (int j = 0; j < c; j++)
		{
			printf("%d ", mat[i * c + j]);
		}
		printf("\n");
	}
}
void find_2D(int mat[512], int r, int c, int mat1)
{
	printf("value %d is found at ", mat1);
	for (int i = 0; i < r; i++)
	{
		for (int j = 0; j < c; j++)
		{
			if (mat1 == mat[i * c + j])
			{
				printf("(%d, %d) ",i,j);
			}
		}
	}
}
int main(void) {
	int r, c;
	int matrix[512]; //matrix 아닌 다른 배열은 사용하지 못한다.
	printf("matrix shape: ");
	scanf("%d %d", &r, &c);

	scan_matrix(matrix, r, c);// matrix 요소 값을 입력 받는 함수.

	printf("----------\n");

	print_matrix(matrix, r, c);

	printf("----------\n");
	find_2D(matrix, r, c, matrix[1]);//matrix[i] 요소 값을 가진 모든 요소의 2차원 index 출력.
	return 0;
}
--------------------------------------------------------------
#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>

int odd(int v)
{
    static count = 0;
    if (v % 2 == 1)
    {
        count++;
    }
    return count;
}

int main(void) {
    int s;
    printf("입력할 수: ");
    scanf("%d", &s);
    int v, odd_numbers;
    for (int i = 0; i < s; i++) {
        scanf("%d", &v);
        odd_numbers = odd(v);
    }
    printf("입력한 홀수의 수는 %d\n", odd_numbers);
    return 0;
}

--------------------------------------------------
