---
title: " no, size_is e out, size_is protótipo"
description: O protótipo de função a seguir usa duas cadeias de caracteres contadas. O desenvolvedor deve escrever código no cliente e no servidor para manter o controle dos comprimentos da matriz de caracteres e passar parâmetros que informam aos stubs quantos elementos de matriz devem ser transmitidos.
ms.assetid: 334c5e0f-b1fb-41ca-8157-d92525e78b3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75075ccabe4a29ca1765a189c371c407c791cb868d2980386488879415e8f60d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073626"
---
# <a name="in-size_is-and-out-size_is-prototype"></a>\[em, tamanho \_ é \] e \[ out, o tamanho \_ é \] protótipo

O protótipo de função a seguir usa duas cadeias de caracteres contadas. O desenvolvedor deve escrever código no cliente e no servidor para manter o controle dos comprimentos da matriz de caracteres e passar parâmetros que informam aos stubs quantos elementos de matriz devem ser transmitidos.

``` syntax
void Analyze(
    [in,  length_is(cbIn), size_is(STRSIZE)]    char  achIn[],
    [in]                                        long  cbIn,
    [out, length_is(*pcbOut), size_is(STRSIZE)] char  achOut[],
    [out]                                       long *pcbOut);
```

Observe que os parâmetros que descrevem o tamanho da matriz são transmitidos na mesma direção que as matrizes: *cbIn* e *achIn* estão \[ [**em**](/windows/desktop/Midl/in) \] parâmetros, enquanto *pcbOut* e *achOut* são parâmetros de \[ [**saída**](/windows/desktop/Midl/out-idl) \] . Como um parâmetro **\[ \] out** , o parâmetro *PcbOut* deve seguir a Convenção C e ser declarado como um ponteiro.

O código do cliente conta o número de caracteres na cadeia de caracteres, incluindo o zero à direita, antes de chamar o procedimento remoto, conforme mostrado:

``` syntax
/* client */
char achIn[STRSIZE], achOut[STRSIZE];
long cbIn, cbOut;
...
gets_s(achIn, STRSIZE);                   // get patient input
cbIn = strlen(achIn) + 1;      // transmitted elements
Analyze(achIn, cbIn, achOut, &cbOut);
```

O procedimento remoto no servidor fornece o comprimento do buffer de retorno em *cbOut* , conforme mostrado:

``` syntax
/* server */
void Analyze(char *pchIn,
             long cbIn,
             char *pchOut,
             long *pcbOut)
{
   ...
   *pcbOut = strlen(pchOut) + 1; // transmitted elements
   return;
}
```

O \[ atributo de **cadeia de caracteres** \] pode ser utilizado quando um parâmetro é conhecido como uma cadeia de caracteres. Esse atributo direciona o stub para calcular o tamanho da cadeia de caracteres, eliminando assim a sobrecarga associada ao \[ [**comprimento**](/windows/desktop/Midl/size-is) dos \] parâmetros. Além disso, ele direcionará o stub para verificar se a cadeia de caracteres é terminada em **nulo** antes de passar o parâmetro para o aplicativo.

 

 