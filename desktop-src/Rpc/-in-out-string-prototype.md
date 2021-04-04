---
title: " dentro, fora do protótipo de cadeia de caracteres"
description: O protótipo de função a seguir usa um único parâmetro \ in, out, String \ para as cadeias de caracteres de entrada e saída.
ms.assetid: 5a652b79-11ca-4780-aac1-60a22f96b4af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed8ed47c02ea3e08672d529bf7ce9f627925518
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917409"
---
# <a name="in-out-string-prototype"></a>\[dentro, fora do protótipo de cadeia de caracteres \]

O protótipo de função a seguir usa um único \[ parâmetro [**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl), [**String**](/windows/desktop/Midl/string) \] para as cadeias de caracteres de entrada e saída. A cadeia de caracteres contém primeiro a entrada de paciente e, em seguida, é substituída pela resposta médica, conforme mostrado:

``` syntax
void Analyze([in, out, string, size_is(STRSIZE)] char  achInOut[]);
```

Este exemplo é semelhante ao que empregava uma cadeia de caracteres de conta única para entrada e saída. Assim como no exemplo, o \[ [**tamanho \_ é**](/windows/desktop/Midl/size-is) \] atributo determina o número de elementos alocados no servidor. O \[ [](/windows/desktop/Midl/string) \] atributo String direciona o stub para chamar **strlen** para determinar o número de elementos transmitidos.

O cliente aloca toda a memória antes da chamada como:

``` syntax
/* client */
char achInOut[STRSIZE];
...
gets_s(achInOut, STRSIZE);            // get patient input
Analyze(achInOut);
printf("%s\n", achInOut);  // display doctor response
```

Observe que a função de análise não deve mais calcular o comprimento da cadeia de caracteres de retorno como fazia no exemplo de cadeia de caracteres contado, em que o atributo de **\[ cadeia de caracteres \]** não foi usado. Agora, os stubs calculam o comprimento conforme mostrado:

``` syntax
/* server */
void Analyze(char *pchInOut)
{
   ...
   Respond(response, pchInOut); // don't need to call strlen
   return;                      // stubs handle size
}
```

 

 