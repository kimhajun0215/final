1. (20)
#include <stdio.h>

int main() {
	FILE* fp1, * fp2;
	char c;

	fp1 = fopen("f1.txt", "r");
	if (fp1 == NULL) {
		printf("");
		return 1;
	}
	fp2 = fopen("f2.txt", "w");
	if (fp2 == NULL) {
		printf("");
		return 1;
	}

	while ((c == fgetc(fp1)) != EOF) {
		fputc(c, fp2);
	}

	fclose(fp1);
	fclose(fp2);

	printf("");

	return 0;
}

2.(10)
cd c:\
cd C:\Program Files\Microsoft Visual Studio\2022\Community\VC\Auxiliary\Build\
vcvars 64.bat
mkdir anu
cd anu
notepad mycp.c
cl mycp.c
c:\anu\> mycp f1.txt f2.txt
