---
title: Atributos de matriz
description: Há uma relação de fechamento entre as matrizes e os ponteiros na linguagem C.
ms.assetid: 0d65c993-63e4-42ae-ae24-6c19a71386a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ed669a2a81528afa84b41a1be25a0c84f70fbe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641633"
---
# <a name="array-attributes"></a>Atributos de matriz

Há uma relação de fechamento entre as matrizes e os ponteiros na linguagem C. Quando passado como um parâmetro para uma função, um nome de matriz é tratado como um ponteiro para o primeiro elemento da matriz, conforme mostrado no exemplo a seguir:


```C++
/* fragment */
extern void f1(char * p1);

void main(void)
{
    char chArray[MAXSIZE];

    fLocal1(chArray);
}
```



Em uma chamada local, você pode usar o parâmetro pointer para março por meio da memória e examinar o conteúdo de outros endereços:


```C++
/* dump memory (fragment) */
void fLocal1(char * pch1)
{
    int i;

    for (i = 0; i < MAXSIZE; i++)
       printf("%c ", *pch1++);
}
```



Quando um cliente passa um ponteiro para um procedimento remoto, o stub do cliente transmite o ponteiro e os dados para os quais ele aponta. A menos que o ponteiro seja restrito aos seus dados correspondentes, toda a memória do cliente deve ser transmitida a cada chamada remota. Ao impor uma tipagem forte na definição da interface, o MIDL limita o processamento do stub do cliente aos dados que corresponde ao ponteiro especificado.

O tamanho da matriz e o intervalo de elementos de matriz transmitidos para o computador remoto podem ser constantes ou variáveis. Quando esses valores são variáveis e, portanto, determinados em tempo de execução, você deve usar atributos no arquivo IDL para especificar quantos elementos de matriz devem ser transmitidos. Os seguintes atributos de MIDL dão suporte a limites de matriz.



| Atributo                             | Descrição                                             | Padrão |
|---------------------------------------|---------------------------------------------------------|---------|
| \[[ **primeiro \_ é**](/windows/desktop/Midl/first-is)\]   | Índice do primeiro elemento de matriz transmitido.           | 0       |
| \[[ **último \_ é**](/windows/desktop/Midl/last-is)\]     | Índice do último elemento de matriz transmitido.            | \-      |
| \[[ **comprimento \_ é**](/windows/desktop/Midl/length-is)\] | Número total de elementos de matriz transmitidos.             | \-      |
| \[[ **máximo \_ é**](/windows/desktop/Midl/max-is)\]       | Valor de índice de matriz mais alto válido.                        | \-      |
| \[[ **mín. \_ é**](/windows/desktop/Midl/min-is)\]       | Menor valor de índice de matriz válido.                         | 0       |
| \[o [ **tamanho \_ é**](/windows/desktop/Midl/size-is)\]     | Número total de elementos de matriz alocados para a matriz. | \-      |



 

> [!Note]  
> O atributo **min \_ is** não está implementado no RPC. O índice de matriz mínimo é sempre tratado como zero.

 

 

 