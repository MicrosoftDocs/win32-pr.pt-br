---
title: " Protótipo de entrada, saída size_is"
description: '\ in, out, Size \_ is \ Prototype usa uma matriz de caracteres de conta única que é passada do cliente para o servidor e do servidor para o cliente.'
ms.assetid: bce9a36f-9f7c-4438-9b5a-15b8877f74c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37829ce0d5a4bb44fefa038e9ce71773f9c4c9bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294139"
---
# <a name="in-out-size_is-prototype"></a>\[in, out, o tamanho \_ é \] protótipo

O protótipo de função a seguir usa uma matriz de caracteres de conta única que é passada de ambas as maneiras: do cliente para o servidor e do servidor para o cliente:

``` syntax
#define STRSIZE 500 //maximum string length

void Analyze(
    [in, out, length_is(*pcbSize), size_is(STRSIZE)] char  achInOut[],
    [in, out]  long *pcbSize);
```

Como um \[ parâmetro [**in**](/windows/desktop/Midl/in) \] , *achInOut* deve apontar para um armazenamento válido no lado do cliente. O desenvolvedor aloca memória associada à matriz no lado do cliente antes de fazer a chamada de procedimento remoto.

Os stubs usam \[ [**o \_**](/windows/desktop/Midl/size-is) \] parâmetro *strsize* para alocar memória no servidor e, em seguida, usar o \[ [**comprimento \_ é**](/windows/desktop/Midl/length-is) o \] parâmetro *pcbSize* para transmitir os elementos da matriz para essa memória. O desenvolvedor deve garantir que o código do cliente defina o **\[ comprimento \_ \]** como variável antes de chamar o procedimento remoto.

Em algumas situações, o uso de parâmetros separados em vez de uma única cadeia de caracteres para a entrada e saída é mais eficiente e fornece flexibilidade. Isso é demonstrado no exemplo a seguir:

``` syntax
/* client */ 
char achInOut[STRSIZE];
long cbSize;
...
gets_s(achInOut, STRSIZE);       // get patient input
cbSize = strlen(achInOut) + 1;   // transmit '\0' too
Analyze(achInOut, &cbSize);
```

No exemplo anterior, a matriz de caracteres achInOut também é usada como um \[ parâmetro [**out**](/windows/desktop/Midl/out-idl) \] . Em C, o nome da matriz é equivalente ao uso de um ponteiro. Por padrão, todos os ponteiros de nível superior são ponteiros de referência — eles não são alterados em valor e apontam para a mesma área de memória no cliente antes e depois da chamada. Toda a memória que o procedimento remoto acessa deve se ajustar ao tamanho que o cliente especifica antes da chamada, ou os stubs gerarão uma exceção.

Antes de retornar, a função Analyze no servidor deve redefinir o parâmetro *pcbSize* para indicar o número de elementos que o servidor transmitirá para o cliente, conforme mostrado a seguir:

``` syntax
/* server */ 
Analyze(char * str, long * pcbSize)
{
   ...
   *pcbSize = strlen(str) + 1; // transmit '\0' too
   return;
}
```

 

 