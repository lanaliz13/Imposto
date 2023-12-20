#include<stdio.h>


  float IN( float salario){
  	
  	float INSS;
  	
  	if(salario<=1320){
  		INSS = salario*0.075;
	}else if(salario>=1320&&salario<=2571.29){
		INSS = salario*0.09;
	}else if(salario>=2571.30&&salario<=3856.94){
		INSS = salario*0.012;
	}else if(salario>=3856.95&&salario<=7507.49){
		INSS = salario*0.014;
	}

	return INSS;
  }
  
  int dep(int D ){
  	
  	int Tdependentes = D*189.50;
  	
  	return Tdependentes;
  	
  }
  

  
  int main(){
  	float salario, deducao, INSS, imposto;
  	int dependentes;
  	
  	printf("Digite o salario: \n");
  	scanf("%f", &salario);
  	
  	printf("Digite a quantidade de dependentes:\n");
  	scanf("%d", &dependentes);

  	
    deducao = dep(dependentes)+IN(salario);
    
    printf("O valor do INSS e igual a: %.2f", IN(salario));
    printf("O valor dos dependentes e igual a : %d", dep(dependentes));
    printf("A deducao e igual a: %.2f", deducao);
  	
  	return 0;
  }
  
