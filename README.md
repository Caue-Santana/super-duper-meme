#include <stdio.h>
#include <stdlib.h>
#include <time.h>
#include <string.h>
#include <locale.h>
#include <conio.h>
#include <windows.h>
#include <math.h>

int main()
{
		
	int N = 0, M = 19, cont, cont0, cont1, cont2, Resp;
	int  contx = 0, conty = 0;
	FILE *Times, *Jogos;
	int *Comp, *AUX;
	int PI, T;
	char times[25];
	char T;
	
	//struct Dados T[20];
	//struct Dados	 
	//{
		char Escolha[20];
	//}T[20];

	char Escolha[20][20], Aux[1+1][20], Aux2[1+1][20];
	int Valid;


	
//	int *AUX1, AUX2;
	
	setlocale(LC_ALL, "Portuguese");
	Times = fopen ("Times.txt","r");
	Jogos = fopen ("Jogos.txt","w");
	
	do
	{		
		printf("Quantos times irão jogar? \n");
		scanf ("%d", &N);
		
		T = (N-1);
		
		if (N < 8 || N > 20)
		{
			printf("Quantidade inválida. Escolha um valor entre 8 e 20.\n\n");
		}
	}while(N < 8 || N >20);
	
	Comp = (int *)malloc(sizeof(int)*N);
	AUX = (int *)malloc(sizeof(int)*N);	
	
	printf("Jogarão %d times \n\n", N);
	
	printf("Times disponíveis: \n\n");
	
	while(fgets(times, 25, Times) != NULL)
	{
		printf("%s", times);
	}
	
	printf("\n");
	printf("--------------------------------------------------------------------\n\n");
	
	printf("Escolha os %d times digitando os números correspondentes de cada um.\n" , N);
		 //Dados A, B;
	do
	{
		for(cont = 0; cont<N; cont++)
		{
			do
			{
				do
				{
					PI = 0;
					printf("Time nº %d: ", cont+1);
					scanf("%d", &Comp[cont]);			
					
					if (Comp[cont] == 1)
					{
						Escolha[0][0] = 'P'; 
						Escolha[0][1] = 'a'; 
						Escolha[0][2] = 'l'; 
						Escolha[0][3] = 'm'; 
						Escolha[0][4] = 'e'; 
						Escolha[0][5] = 'i'; 
						Escolha[0][6] = 'r'; 
						Escolha[0][7] = 'a'; 
						Escolha[0][8] = 's'; 
						Escolha[0][9] = ' ';
						Escolha[0][10] = ' ';						
						Escolha[0][1] = ' ';
						Escolha[0][12] = ' ';						
						Escolha[0][13] = ' ';
						Escolha[0][14] = ' ';						
						Escolha[0][15] = ' ';
						Escolha[0][16] = ' ';
						Escolha[0][17] = ' ';
						Escolha[0][18] = ' ';
						Escolha[0][19] = ' ';

						for (cont1 = 0; cont1 < 1; cont1++)
						{
							for (cont2 = 0; cont2 < M; cont2++)
								printf("%c", Escolha[cont1][cont2]);
						}
						printf("\n");
					}											
					
					if (Comp[cont] == 2)
					{
						Escolha[1][0] = 'F'; 
						Escolha[1][1] = ' '; 
						Escolha[1][2] = 'a'; 
						Escolha[1][3] = 'm'; 
						Escolha[1][4] = 'e'; 
						Escolha[1][5] = 'n'; 
						Escolha[1][6] = 'g'; 
						Escolha[1][7] = 'o';
						Escolha[1][8] = ' ';
						Escolha[1][9] = ' ';
						Escolha[1][10] = ' ';						
						Escolha[1][11] = ' ';
						Escolha[1][12] = ' ';						
						Escolha[1][13] = ' ';
						Escolha[1][14] = ' ';						
						Escolha[1][15] = ' ';
						Escolha[1][16] = ' ';
						Escolha[1][17] = ' ';
						Escolha[1][18] = ' ';						
						Escolha[1][19] = ' ';
												
						for (cont1 = 1; cont1 < 2; cont1++)
						{
							for (cont2 = 0; cont2 < M; cont2++)
								printf("%c", Escolha[cont1][cont2]);
						
						}
						printf("\n");
					}
						
					if (Comp[cont] == 3)
					{
						Escolha[2][0] = 'A'; 
						Escolha[2][1] = 't'; 
						Escolha[2][2] = 'l'; 
						Escolha[2][3] = 'é'; 
						Escolha[2][4] = 't'; 
						Escolha[2][5] = 'i'; 
						Escolha[2][6] = 'c'; 
						Escolha[2][7] = 'o'; 
						Escolha[2][8] = ' ';
						Escolha[2][9] = 'M'; 
						Escolha[2][10] = 'i'; 
						Escolha[2][11] = 'n'; 
						Escolha[2][12] = 'e'; 
						Escolha[2][13] = 'i'; 
						Escolha[2][14] = 'r'; 
						Escolha[2][15] = 'o';
						Escolha[2][16] = ' ';
						Escolha[2][17] = ' ';
						Escolha[2][18] = ' ';  
						Escolha[2][19] = ' ';
												
						for (cont1 = 2; cont1 < 3; cont1++)
						{
							for (cont2 = 0; cont2 < M; cont2++)
								printf("%c", Escolha[cont1][cont2]);
						}
						printf("\n");
					}																																																											
					
					if (Comp[cont] == 4)
					{
						Escolha[3][0] = 'S'; 
						Escolha[3][1] = 'a'; 
						Escolha[3][2] = 'n'; 
						Escolha[3][3] = 't'; 
						Escolha[3][4] = 'o'; 
						Escolha[3][5] = 's';
						Escolha[3][6] = ' ';
						Escolha[3][7] = ' ';
						Escolha[3][8] = ' ';
						Escolha[3][9] = ' ';
						Escolha[3][10] = ' ';						
						Escolha[3][11] = ' ';
						Escolha[3][12] = ' ';						
						Escolha[3][13] = ' ';
						Escolha[3][14] = ' ';						
						Escolha[3][15] = ' ';
						Escolha[3][16] = ' ';
						Escolha[3][17] = ' ';
						Escolha[3][18] = ' ';		
						Escolha[3][19] = ' ';						
										
							for (cont1 = 3; cont1 < 4; cont1++)
							{
								for (cont2 = 0; cont2 < M; cont2++)
									printf("%c", Escolha[cont1][cont2]);
							}
							printf("\n");
					}					
					
					if (Comp[cont] == 5)
					{
						Escolha[4][0] = 'B'; 
						Escolha[4][1] = 'o'; 
						Escolha[4][2] = 't'; 
						Escolha[4][3] = 'a'; 
						Escolha[4][4] = 'f'; 
						Escolha[4][5] = 'o'; 
						Escolha[4][6] = 'g'; 
						Escolha[4][7] = 'o'; 
						Escolha[4][8] = ' ';
						Escolha[4][9] = ' ';
						Escolha[4][10] = ' ';						
						Escolha[4][11] = ' ';
						Escolha[4][12] = ' ';						
						Escolha[4][13] = ' ';
						Escolha[4][14] = ' ';						
						Escolha[4][15] = ' ';
						Escolha[4][16] = ' ';
						Escolha[4][17] = ' ';
						Escolha[4][18] = ' ';
						Escolha[4][19] = ' ';
																
							for (cont1 = 4; cont1 < 5; cont1++)
							{
								for (cont2 = 0; cont2 < M; cont2++)
									printf("%c", Escolha[cont1][cont2]);
							}
							printf("\n");
					}					
					
					if (Comp[cont] == 6)
					{
						Escolha[5][0] = 'C'; 
						Escolha[5][1] = 'o'; 
						Escolha[5][2] = 'r'; 
						Escolha[5][3] = 'i'; 
						Escolha[5][4] = 'n'; 
						Escolha[5][5] = 't'; 
						Escolha[5][6] = 'h'; 
						Escolha[5][7] = 'i'; 
						Escolha[5][8] = 'a';
						Escolha[5][9] = 'n';
						Escolha[5][10] = 's'; 						
						Escolha[5][11] = ' ';
						Escolha[5][12] = ' ';						
						Escolha[5][13] = ' ';
						Escolha[5][14] = ' ';						
						Escolha[5][15] = ' ';
						Escolha[5][16] = ' ';
						Escolha[5][17] = ' ';
						Escolha[5][18] = ' ';
						Escolha[5][19] = ' ';
								
							for (cont1 = 5; cont1 < 6; cont1++)
							{
								for (cont2 = 0; cont2 < M; cont2++)
									printf("%c", Escolha[cont1][cont2]);
							}
							printf("\n");
					}					
																															
					if (Comp[cont] == 7)
					{
						Escolha[6][0] = 'A'; 
						Escolha[6][1] = 't'; 
						Escolha[6][2] = 'l'; 
						Escolha[6][3] = 'é'; 
						Escolha[6][4] = 't'; 
						Escolha[6][5] = 'i'; 
						Escolha[6][6] = 'c'; 
						Escolha[6][7] = 'o'; 
						Escolha[6][8] = ' ';
						Escolha[6][9] = 'P';
						Escolha[6][10] = 'a';
						Escolha[6][11] = 'r';
						Escolha[6][12] = 'a';
						Escolha[6][13] = 'n';
						Escolha[6][14] = 'a';
						Escolha[6][15] = 'e';
						Escolha[6][16] = 'n';
						Escolha[6][17] = 's';
						Escolha[6][18] = 'e';
						Escolha[6][19] = ' ';
						
						
						for (cont1 = 6; cont1 < 7; cont1++)
						{
							for (cont2 = 0; cont2 < M; cont2++)
								printf("%c", Escolha[cont1][cont2]);
						}
						printf("\n");
					}											

					if (Comp[cont] == 8)
					{
						Escolha[7][0] = 'G'; 
						Escolha[7][1] = 'r'; 
						Escolha[7][2] = 'ê'; 
						Escolha[7][3] = 'm'; 
						Escolha[7][4] = 'i'; 
						Escolha[7][5] = 'o'; 
						Escolha[7][6] = ' ';
						Escolha[7][7] = ' ';
						Escolha[7][8] = ' '; 	
						Escolha[7][9] = ' ';
						Escolha[7][10] = ' ';						
						Escolha[7][11] = ' ';
						Escolha[7][12] = ' ';						
						Escolha[7][13] = ' ';
						Escolha[7][14] = ' ';						
						Escolha[7][15] = ' ';
						Escolha[7][16] = ' ';
						Escolha[7][17] = ' ';
						Escolha[7][18] = ' ';		
						Escolha[7][19] = ' ';
						
						for (cont1 = 7; cont1 < 8; cont1++)
						{
							for (cont2 = 0; cont2 < M; cont2++)
								printf("%c", Escolha[cont1][cont2]);
						}
						printf("\n");
					}											

					if (Comp[cont] == 9)
					{
						Escolha[8][0] = 'F'; 
						Escolha[8][1] = 'l'; 
						Escolha[8][2] = 'u'; 
						Escolha[8][3] = 'm'; 
						Escolha[8][4] = 'i'; 
						Escolha[8][5] = 'n'; 
						Escolha[8][6] = 'e'; 
						Escolha[8][7] = 'n'; 
						Escolha[8][8] = 's';
						Escolha[8][9] = 'e';
						Escolha[8][10] = ' ';						
						Escolha[8][11] = ' ';
						Escolha[8][12] = ' ';						
						Escolha[8][13] = ' ';
						Escolha[8][14] = ' ';						
						Escolha[8][15] = ' ';
						Escolha[8][16] = ' ';
						Escolha[8][17] = ' ';
						Escolha[8][18] = ' ';
						Escolha[8][19] = ' ';
						
						for (cont1 = 8; cont1 < 9; cont1++)
						{
							for (cont2 = 0; cont2 < M; cont2++)
								printf("%c", Escolha[cont1][cont2]);
						}
						printf("\n");
					}											

					if (Comp[cont] == 10)
					{
						Escolha[9][0] = 'P'; 
						Escolha[9][1] = 'o'; 
						Escolha[9][2] = 'n'; 
						Escolha[9][3] = 't'; 
						Escolha[9][4] = 'e'; 
						Escolha[9][5] = ' '; 
						Escolha[9][6] = 'P'; 
						Escolha[9][7] = 'r'; 
						Escolha[9][8] = 'e';
						Escolha[9][9] = 't';
						Escolha[9][10] = 'a';						
						Escolha[9][11] = ' ';
						Escolha[9][12] = ' ';						
						Escolha[9][13] = ' ';
						Escolha[9][14] = ' ';						
						Escolha[9][15] = ' ';
						Escolha[9][16] = ' ';
						Escolha[9][17] = ' ';
						Escolha[9][18] = ' ';
						Escolha[9][19] = ' ';
						
						for (cont1 = 9; cont1 < 10; cont1++)
						{
							for (cont2 = 0; cont2 < M; cont2++)
								printf("%c", Escolha[cont1][cont2]);
						}
						printf("\n");
					}											

					if (Comp[cont] == 11)
					{
						Escolha[10][0] = 'S'; 
						Escolha[10][1] = 'ã'; 
						Escolha[10][2] = 'o'; 
						Escolha[10][3] = ' '; 
						Escolha[10][4] = 'P'; 
						Escolha[10][5] = 'a'; 
						Escolha[10][6] = 'u'; 
						Escolha[10][7] = 'l'; 
						Escolha[10][8] = 'o';
						Escolha[10][9] = ' ';
						Escolha[10][10] = ' ';						
						Escolha[10][11] = ' ';
						Escolha[10][12] = ' ';						
						Escolha[10][13] = ' ';
						Escolha[10][14] = ' ';						
						Escolha[10][15] = ' ';
						Escolha[10][16] = ' ';
						Escolha[10][17] = ' ';
						Escolha[10][18] = ' ';
						Escolha[10][19] = ' '; 

						for (cont1 = 10; cont1 < 11; cont1++)
						{
							for (cont2 = 0; cont2 < M; cont2++)
								printf("%c", Escolha[cont1][cont2]);
						}
						printf("\n");
					}											

					if (Comp[cont] == 12)
					{
						Escolha[11][0] = 'C'; 
						Escolha[11][1] = 'h'; 
						Escolha[11][2] = 'a'; 
						Escolha[11][3] = 'p'; 
						Escolha[11][4] = 'e'; 
						Escolha[11][5] = 'c'; 
						Escolha[11][6] = 'e'; 
						Escolha[11][7] = 'n'; 
						Escolha[11][8] = 's';
						Escolha[11][9] = 'e';
						Escolha[11][10] = ' ';						
						Escolha[11][11] = ' ';
						Escolha[11][12] = ' ';						
						Escolha[11][13] = ' ';
						Escolha[11][14] = ' ';						
						Escolha[11][15] = ' ';
						Escolha[11][16] = ' ';
						Escolha[11][17] = ' ';
						Escolha[11][18] = ' ';
						Escolha[11][19] = ' ';
								
						for (cont1 = 11; cont1 < 12; cont1++)
						{
							for (cont2 = 0; cont2 < M; cont2++)
								printf("%c", Escolha[cont1][cont2]);
						}
						printf("\n");
					}											

					if (Comp[cont] == 13)
					{
						Escolha[12][0] = 'C'; 
						Escolha[12][1] = 'r'; 
						Escolha[12][2] = 'u'; 
						Escolha[12][3] = 'z'; 
						Escolha[12][4] = 'e'; 
						Escolha[12][5] = 'i'; 
						Escolha[12][6] = 'r'; 
						Escolha[12][7] = 'o';
						Escolha[12][8] = ' ';
						Escolha[12][9] = ' ';
						Escolha[12][10] = ' ';						
						Escolha[12][11] = ' ';
						Escolha[12][12] = ' ';						
						Escolha[12][13] = ' ';
						Escolha[12][14] = ' ';						
						Escolha[12][15] = ' ';
						Escolha[12][16] = ' ';
						Escolha[12][17] = ' ';
						Escolha[12][18] = ' '; 
						Escolha[12][19] = ' ';
								
						for (cont1 = 12; cont1 < 13; cont1++)
						{
							for (cont2 = 0; cont2 < M; cont2++)
								printf("%c", Escolha[cont1][cont2]);
						}
						printf("\n");
					}											

					if (Comp[cont] == 14)
					{
						Escolha[13][0] = 'S'; 
						Escolha[13][1] = 'p'; 
						Escolha[13][2] = 'o'; 
						Escolha[13][3] = 'r'; 
						Escolha[13][4] = 't';
						Escolha[13][5] = ' ';						
						Escolha[13][6] = ' ';
						Escolha[13][7] = ' ';						
						Escolha[13][8] = ' ';
						Escolha[13][9] = ' ';
						Escolha[13][10] = ' ';						
						Escolha[13][11] = ' ';
						Escolha[13][12] = ' ';						
						Escolha[13][13] = ' ';
						Escolha[13][14] = ' ';						
						Escolha[13][15] = ' ';
						Escolha[13][16] = ' ';
						Escolha[13][17] = ' ';
						Escolha[13][18] = ' ';
						Escolha[13][19] = ' ';
									
						for (cont1 = 13; cont1 < 14; cont1++)
						{
							for (cont2 = 0; cont2 < M; cont2++)
								printf("%c", Escolha[cont1][cont2]);
						}
						printf("\n");
					}											
					
					if (Comp[cont] == 15)
					{
						Escolha[14][0] = 'C'; 
						Escolha[14][1] = 'o'; 
						Escolha[14][2] = 'r'; 
						Escolha[14][3] = 'i'; 
						Escolha[14][4] = 't'; 
						Escolha[14][5] = 'i'; 
						Escolha[14][6] = 'b'; 
						Escolha[14][7] = 'a'; 					
						Escolha[14][8] = ' ';
						Escolha[14][9] = ' ';
						Escolha[14][10] = ' ';						
						Escolha[14][11] = ' ';
						Escolha[14][12] = ' ';						
						Escolha[14][13] = ' ';
						Escolha[14][14] = ' ';						
						Escolha[14][15] = ' ';
						Escolha[14][16] = ' ';
						Escolha[14][17] = ' ';
						Escolha[14][18] = ' ';
						Escolha[14][19] = ' ';

						for (cont1 = 14; cont1 < 15; cont1++)
						{
							for (cont2 = 0; cont2 < 8; cont2++)
								printf("%c", Escolha[cont1][cont2]);
						}
						printf("\n");
					}											

					if (Comp[cont] == 16)
					{
						Escolha[15][0] = 'I'; 
						Escolha[15][1] = 'n'; 
						Escolha[15][2] = 't'; 
						Escolha[15][3] = 'e'; 
						Escolha[15][4] = 'r'; 
						Escolha[15][5] = 'n'; 
						Escolha[15][6] = 'a'; 
						Escolha[15][7] = 'c'; 
						Escolha[15][8] = 'i';
						Escolha[15][9] = 'o';
						Escolha[15][10] = 'n';
						Escolha[15][11] = 'a';
						Escolha[15][12] = 'l';							
						Escolha[15][13] = ' ';
						Escolha[15][14] = ' ';						
						Escolha[15][15] = ' ';
						Escolha[15][16] = ' ';
						Escolha[15][17] = ' ';
						Escolha[15][18] = ' ';	
						Escolha[15][19] = ' ';		
						
						for (cont1 = 15; cont1 < 16; cont1++)
						{
							for (cont2 = 0; cont2 < M; cont2++)
								printf("%c", Escolha[cont1][cont2]);
						}
						printf("\n");
					}											

					if (Comp[cont] == 17)
					{
						Escolha[16][0] = 'V'; 
						Escolha[16][1] = 'i'; 
						Escolha[16][2] = 't'; 
						Escolha[16][3] = 'ó'; 
						Escolha[16][4] = 'r'; 
						Escolha[16][5] = 'i'; 
						Escolha[16][6] = 'a'; 
						Escolha[16][7] = ' ';						
						Escolha[16][8] = ' ';
						Escolha[16][9] = ' ';
						Escolha[16][10] = ' ';						
						Escolha[16][11] = ' ';
						Escolha[16][12] = ' ';						
						Escolha[16][13] = ' ';
						Escolha[16][14] = ' ';						
						Escolha[16][15] = ' ';
						Escolha[16][16] = ' ';
						Escolha[16][17] = ' ';
						Escolha[16][18] = ' ';
						Escolha[16][19] = ' ';
										
						for (cont1 = 16; cont1 < 17; cont1++)
						{
							for (cont2 = 0; cont2 < M; cont2++)
								printf("%c", Escolha[cont1][cont2]);
						}
						printf("\n");
					}											

					if (Comp[cont] == 18)
					{
						Escolha[17][0] = 'F'; 
						Escolha[17][1] = 'i'; 
						Escolha[17][2] = 'g'; 
						Escolha[17][3] = 'u'; 
						Escolha[17][4] = 'g'; 
						Escolha[17][5] = 'u'; 
						Escolha[17][6] = 'e'; 
						Escolha[17][7] = 'i'; 
						Escolha[17][8] = 'r';
						Escolha[17][9] = 'e';
						Escolha[17][10] = 'n';
						Escolha[17][11] = 's';
						Escolha[17][12] = 'e';					
						Escolha[17][13] = ' ';
						Escolha[17][14] = ' ';						
						Escolha[17][15] = ' ';
						Escolha[17][16] = ' ';
						Escolha[17][17] = ' ';
						Escolha[17][18] = ' ';		
						Escolha[17][19] = ' ';			
						
						for (cont1 = 17; cont1 < 18; cont1++)
						{
							for (cont2 = 0; cont2 < M; cont2++)
								printf("%c", Escolha[cont1][cont2]);
						}
						printf("\n");
					}											

					if (Comp[cont] == 19)
					{
						Escolha[18][0] = 'A'; 
						Escolha[18][1] = 'm'; 
						Escolha[18][2] = 'é'; 
						Escolha[18][3] = 'r'; 
						Escolha[18][4] = 'i'; 
						Escolha[18][5] = 'c'; 
						Escolha[18][6] = 'a'; 
						Escolha[18][7] = ' '; 
						Escolha[18][8] = 'M';
						Escolha[18][9] = 'i';
						Escolha[18][10] = 'n';
						Escolha[18][11] = 'e';
						Escolha[18][12] = 'i';
						Escolha[18][13] = 'r';
						Escolha[18][14] = 'o';						
						Escolha[18][15] = ' ';
						Escolha[18][16] = ' ';
						Escolha[18][17] = ' ';
						Escolha[18][18] = ' ';
						Escolha[18][19] = ' ';
						
						for (cont1 = 18; cont1 < 19; cont1++)
						{
							for (cont2 = 0; cont2 < M; cont2++)
								printf("%c", Escolha[cont1][cont2]);
						}
						printf("\n");
					}							
					
					if (Comp[cont] == 20)
					{ 
						Escolha[19][0] = 'S'; 
						Escolha[19][1] = 'a'; 
						Escolha[19][2] = 'n'; 
						Escolha[19][3] = 't'; 
						Escolha[19][4] = 'a'; 
						Escolha[19][5] = ' '; 
						Escolha[19][6] = 'C'; 
						Escolha[19][7] = 'r'; 
						Escolha[19][8] = 'u';
						Escolha[19][9] = 'z';
						Escolha[19][10] = ' ';						
						Escolha[19][11] = ' ';
						Escolha[19][12] = ' ';						
						Escolha[19][13] = ' ';
						Escolha[19][14] = ' ';						
						Escolha[19][15] = ' ';
						Escolha[19][16] = ' ';
						Escolha[19][17] = ' ';
						Escolha[19][18] = ' ';
						Escolha[19][19] = ' ';
	
						for (cont1 = 19; cont1 < 20; cont1++)
						{
							for (cont2 = 0; cont2 < M; cont2++)
								printf("%c", Escolha[cont1][cont2]);
						}
						printf("\n");
					}							
					
					printf("\n");
					AUX[cont1] = Comp[cont]; 
					
				//	printf("AUX = %d\n\n", AUX[cont1]);
					//AUX[cont1] = Comp[cont1];
					
				}while (Comp[cont] < 1 || Comp[cont] > 20);
				
				for(cont0 = 0; cont0<cont; cont0++)
				{
					if (Comp[cont] == Comp[cont0])
					{
						PI = 69;
						break;
					}
				}
			
			}while (PI == 69);
			
		}
			
			
		printf("Digite 1 para confirmar: ");
		scanf("%d", &Resp);
		printf("\n\n");
					
	}while (Resp != 1);	
	
	for(cont1 = 0; cont1 < N; cont1++)
	{
		for(cont2 = 0; cont2 < 20; cont2++)
		{
			printf("%c", Escolha[cont1][cont2]);
		}
		printf("\n");
	}
	
	for (cont = 0; cont < N; cont++)
	{
		printf("%d \t", Comp[cont]);
	}
	printf("\n\n");
	
	if (N % 2 == 0)	
	{			
		if(N == 8)		
		{
			contx = 1;
			do
			{			
				
				
				fprintf(Jogos, "\nRodada %d (Ida)\n\n", contx);
//==================================================================================================			
				for(cont1 = 0; cont1 < 1; cont1++)
				{
					for(cont2 = 0; cont2 <M; cont2++)
						fprintf(Jogos, "%c", Escolha[cont1][cont2]);
				}
				fprintf(Jogos, "X \t");
				
				for(cont1 = 7; cont1 < 8; cont1++)
				{
					for(cont2 = 0; cont2 < M; cont2++)
						fprintf(Jogos, "%c", Escolha[cont1][cont2]);
				}
				fprintf(Jogos, "\n");
//==================================================================================================				
				for(cont1 = 1; cont1 < 2; cont1++)
				{
					for(cont2 = 0; cont2<M; cont2++)
						fprintf(Jogos, "%c", Escolha[cont1][cont2]);
				}
				fprintf(Jogos, "X \t");
				
				for(cont1 = 6; cont1 <7; cont1++)
				{
					for(cont2 = 0; cont2<M; cont2++)
						fprintf(Jogos,"%c", Escolha[cont1][cont2]);
				}
				fprintf(Jogos, "\n");
//==================================================================================================				
				for(cont1 = 2; cont1 < 3; cont1++)
				{
					for(cont2 = 0; cont2<M; cont2++)
						fprintf(Jogos, "%c", Escolha[cont1][cont2]);
				}
				fprintf(Jogos, "X \t");
				
				for(cont1 = 5; cont1 <6; cont1++)
				{
					for(cont2 = 0; cont2<M; cont2++)
						fprintf(Jogos, "%c", Escolha[cont1][cont2]);
				}
				fprintf(Jogos, "\n");
//==================================================================================================
				for(cont1 = 3; cont1 < 4; cont1++)
				{
					for(cont2 = 0; cont2<M; cont2++)
						fprintf(Jogos, "%c", Escolha[3][cont2]);
				}
				fprintf(Jogos, "X \t");
				
				for(cont1 = 4; cont1 <5; cont1++)
				{
					for(cont2 = 0; cont2<M; cont2++)
						fprintf(Jogos, "%c", Escolha[cont1][cont2]);
				}
				fprintf(Jogos, "\n");
//==================================================================================================
				for(cont1 = 1; cont1 < 2; cont1++)
				{
					for(cont2 = 0; cont2 <M; cont2++)
					{
						Aux[1][cont2] = Escolha[7][cont2];
						Escolha[1][cont2] = Escolha[7][cont2]; 
						Escolha[7][cont2] = Escolha[6][cont2];
						Escolha[6][cont2] = Escolha[5][cont2];
						Escolha[5][cont2] = Escolha[4][cont2];
						Escolha[4][cont2] = Escolha[3][cont2];
						Escolha[3][cont2] = Escolha[2][cont2];
						Escolha[2][cont2] = Aux[1][cont2];
					}
				}
				
				contx++;
				conty = contx;
				//Valid++;
				
			}while(contx < 8);
		}
	}
	
	else
	{
		//printf("IMPAR");
		//for (cont1 = 0; cont1<N; cont1++)
		//{
		//	printf("%d \t", Comp[cont1]);
			
			
		//}
	}
	
	fclose (Times);
	fclose (Jogos);
}
