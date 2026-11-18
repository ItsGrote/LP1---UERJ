## Questoes Slide 02

Disciplina: Linguagem de Programacao I - UERJ

## Questao 01

Feita em aula.

## Questao 02

'''c
#include <stdio.h>

int main(void){

float num_1, num_2;

scanf("%f %f", &num_1, &num_2);

if(num_1 > num_2){
	printf("%f\n", num_1);
} else {
	printf("%f\n", num_2);
}

return 0;
}
'''

## Questao 03

'''c
#include <stdio.h>

int main(void){
float limite, cotacao, valor_em_dolar, valor_em_real;
cotacao = 3.17;
limite = 1000.00;

scanf("%f", &valor_em_dolar);

valor_em_real = valor_em_dolar * cotacao;



if(valor_em_real <= limite){
printf("BOM NEGOCIO\n");
} 

return 0;
}
'''

## Questao 04

'''c
#include <stdio.h>

int main(void){
float limite_superior, limite_inferior, conversao, velocidade_atual, velocidade_atual_em_kph;

conversao = 1.6; //unidade: km/milha
limite_superior = 100.0; //km/h
limite_inferior = 80.0; //km/h

scanf("%f", &velocidade_atual);

velocidade_atual_em_kph = velocidade_atual * conversao;

if(velocidade_atual_em_kph > limite_superior){
	printf("DESACELERE\n");
	
} else if(velocidade_atual_em_kph < limite_inferior){
	printf("ACELERE\n");
	
} else {
	printf("MANTENHA\n");
}

return 0;
}
'''


## Questao 05

'''c
#include <stdio.h>

int main(void){

float soma, num;
soma = 0;

scanf("%f", &num);

while(num != 0){
	soma += num;
	scanf("%f", &num);
}

printf("%f\n", soma);

return 0;
}
'''

## Questao 	06

'''c
#include <stdio.h>

int main(void){

int limite_superior, soma;
soma = 0;

scanf("%d", &limite_superior);

for(int i = 1; i <= limite_superior; i++){
	soma += (i*i);	
}

printf("%d\n", soma);
return 0;
}
'''

## Questao 07

'''c
#include <stdio.h>

int main(void){
//vamos fazer o caso usando os identificadores numericos do time

int pontos_vitoria, pontos_empate, pontos_derrota, pontos_totais;
int id, numero_de_times;
int num_vitorias, num_empates, num_derrotas;

pontos_vitoria = 3;
pontos_empate = 1;
pontos_derrota = 0;
numero_de_times = 20;

int identificador_time[numero_de_times];
int pontos_time[numero_de_times];

for(int i = 0; i < numero_de_times; i++){
	pontos_totais = 0;
  
	scanf("%d", &identificador_time[i]);
	
	scanf("%d", &num_vitorias);
	scanf("%d", &num_empates);
	scanf("%d", &num_derrotas);
	
	pontos_totais += (pontos_vitoria * num_vitorias + pontos_empate * num_empates + pontos_derrota * num_derrotas);
	
	pontos_time[i] = pontos_totais;
}


int max_pontos, min_pontos;
int idx_max, idx_min;

max_pontos = pontos_time[0];
idx_max = 0;

min_pontos = pontos_time[0];
idx_min = 0;

for(int i = 0; i < numero_de_times; i++){
	if(max_pontos < pontos_time[i]){
		max_pontos = pontos_time[i];
		idx_max = i;
	}
	
	if(min_pontos > pontos_time[i]){
		min_pontos = pontos_time[i];
		idx_min = i;
	}
	
}

printf("%d\n", identificador_time[idx_max]);
printf("%d\n", identificador_time[idx_min]);

return 0;
}
'''

## Questao 08

1) Em Python:

'''python
num_1 = int(input())
num_2 = int(input())

if(num_1 > num_2):
	aux = num_1
	num_1 = n2
	num_2 = aux

for i in range(num_1 + 1, num_2):
	print(i)
'''
	
2) Em C:

'''c
#include<stdio.h>

int main(void){

int n1, n2, aux;

scanf("%d %d", &num_1, &num_2);

if(num_1 > num_2){
	aux = n1;
	n1 = n2;
	n2 = aux;
}

for(int i = num_1 + 1; i < num_2; i++ ){
	printf("%d\n", i);
}

return 0;
}
'''