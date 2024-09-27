

#include<stdio.h>

int main()
{
//structure
	struct s_lampe{
		char lettre[30];
		char type[30];
		int consommation;
		float prix;
		} LMP[30];

int N,i;
float budget;
	printf("Le nombre de lampes Ã  enregistre? :\t");
	scanf("%d",&N);
	if(N>200){
	printf("La dimension du rayon ne permets pas d'exposer plus de 200 lampes\n");
	printf("Veuillez introduire un autre nombre inferieur Ã  200 : \t");
	scanf("%d",&N);}
	
	for(i=1;i<=N;i++){
	printf("\nLa lampe %d :\n",i);
	printf("\nSaisir la lettre d'economie d'Ã©nergie :\t"); scanf("%s",LMP[i].lettre);
	printf("\nSaisir son type de culot :\t"); scanf("%s",LMP[i].type);
	printf("\nSaisir sa consommation :\t"); scanf("%d",&LMP[i].consommation);
	printf("\nSaisir son prix :\t"); scanf("%f",&LMP[i].prix);
	}
//affichage
	for(i=1;i<=N;i++){
	printf("\nLa lampe %d :\n",i);
	printf("\n Sa lettre d'Ã©conomie d'energie: %s\t Son type de culot: %s\t Sa consommation: %d W\t Son prix: %f e\t\n",LMP[i].lettre,LMP[i].type,LMP[i].consommation,LMP[i].prix);
	}

	printf("\nDonnez votre budget? :\t"); scanf("%f",&budget);
	printf("\nLes lampes dont le prix est inferieur Ã  votre budget sont :\n");
	for(i=1;i<=N;i++){
	if(LMP[i].prix<budget){
	printf("%s %s %d %f\n",LMP[i].lettre,LMP[i].type,LMP[i].consommation,LMP[i].prix);}
	}
	
return 0;
}

