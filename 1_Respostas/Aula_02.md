1.Quais as diferenças entre os barramentos de dados e de endereços?

Barramento de dados é da quantidade de bits transmitidos paralelamente em uma via de comunição entre CPU e periféricos, já o barramento de endereço é a quantidade de bits transmitidos para identificar o endereço a ser lido/escrito em uma memória, este tende a ser unidimensional de maneira que o endereço seja sempre enviado à memória para acesso à informação.

2.Quais são as diferenças entre as memórias RAM e ROM?

RAM é uma memória mais rápida, de acesso aleatório (não sequencial), e volátil (dados são perdidos ao retirar a alimentação). A ROM é mais lenta, sequencial e não-volátil (mantém os dados após retirar a alimentação).

3.Considere o código abaixo:

```C
#include <stdio.h>
int main(void)
{
	int i;
	printf("Insira um número inteiro: ");
	scanf("%d", &i);
	if(i%2)
		printf("%d eh impar.\n");
	else
		printf("%d eh par.\n");
	return 0;
}
```

Para este código, responda:
(a) A variável i é armazenada na memória RAM ou ROM? Por quê?

A variável i é armazenada na memória RAM, pois, por se tratar de um programa executável, ao execiutar a parte onde é declarada uma variável, é alocada memória suficiente para comportar os dados dessa variável. O espaço depende do tipo de variável e, em alguns casos, do compilador utilizado.

(b) O programa compilado a partir deste código é armazenado na memória RAM ou ROM? Por quê?

O programa é armazenado na memória ROM, pois, por se tratar de um programa compilado, este é salvo na memória ROM, para que permanessa salvo após a alimentação ser cessada.

4.Quais são as diferenças, vantagens e desvantagens das arquiteturas Harvard e Von Neumann?

A arquitetura Harvard constitui em dois blocos separados de memória, um para memória de dados (RAM), outro para memória de instruções (ROM), onde o programa é guardado para ser lido, isso possibilita a ultilização simultânea das duas memórias por parte da CPU, podendo ler instruções e processar dados ao mesmo tempo, portanto, necessita-se apenas de um clock. Porém, é mais lento e seu design é mais complexo.

A arquitetura de Von-Neumann utiliza apenas uma memória para instruções e para dados, logo, o processador necessita ler instruções e processar dados em diferentes ciclos de clock, então são necessários dois ciclos de clock. Porém, este é mais rápido e de design mais simples.

5.Considere a variável inteira i, armazenando o valor 0x8051ABCD. Se i é armazenada na memória a partir do endereço 0x0200, como ficam este byte e os seguintes, considerando que a memória é:

(a) Little-endian;
 No byte 0x0200, fica o CD. No byte 0x0201, fica o AB. No byte 0x0202, fica o 51. No byte 0x0203, fica o 80.

(b) Big-endian.
 No byte 0x0200, fica o CD. No byte 0x01FF, fica o AB. No byte 0x01FE, fica o 51. No byte 0x01FD, fica o 80.

6.Sabendo que o processador do MSP430 tem registradores de 16 bits, como ele soma duas variáveis de 32 bits?

É possível efetuar essa soma por meio da concatenação de dois registradores para cada variável, conectando-os para a soma com o Carry, caso haja necessidade quando a soma for executada.
