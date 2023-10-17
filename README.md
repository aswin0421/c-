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
