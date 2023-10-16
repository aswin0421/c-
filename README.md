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
