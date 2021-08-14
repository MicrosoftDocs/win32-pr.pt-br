---
title: Combinando atributos de matriz
description: Os atributos de campo podem ser fornecidos em várias combinações, desde que o stub possa usar as informações para determinar o tamanho da matriz e o número de bytes a serem transmitidos para o servidor.
ms.assetid: ff4f971f-9e46-4454-9d57-d8ebdf70b261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd440251a658dd5b888df7275f578369419d4b8b2d4f920b263bc5095c4bd948
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931749"
---
# <a name="combining-array-attributes"></a>Combinando atributos de matriz

Os atributos de campo podem ser fornecidos em várias combinações, desde que o stub possa usar as informações para determinar o tamanho da matriz e o número de bytes a serem transmitidos para o servidor. As relações entre os atributos são definidas usando as seguintes fórmulas:

``` syntax
size_is = max_is + 1;
length_is = last_is - first_is + 1;
```

Os valores associados aos atributos devem obedecer a várias regras de bom senso com base nessas fórmulas. Essas regras são:

-   Não especifique um \[ [**primeiro é o \_ valor**](/windows/desktop/Midl/first-is) \] de índice menor que zero ou um último \[ [**\_ valor**](/windows/desktop/Midl/last-is) \] é maior que max \[ [**\_ é**](/windows/desktop/Midl/max-is) \] .
-   Não especifique um tamanho negativo para uma matriz. Defina o primeiro e o último elementos para que eles resultem em um valor de comprimento de zero ou maior. Defina \[ [**o valor max \_ é**](/windows/desktop/Midl/max-is) \] para que o tamanho seja zero ou maior. Se MIDL foi invocado com a opção de verificação [**/error**](/windows/desktop/Midl/-error) bounds, o stub gera uma exceção quando o tamanho é menor que zero ou o comprimento transmitido é menor \_ que zero.
-   Não use o comprimento é e o último é atributos ao mesmo tempo, nem o tamanho e o último são \[ [**\_**](/windows/desktop/Midl/length-is) \] atributos ao mesmo \[ [**\_**](/windows/desktop/Midl/last-is) \] \[ **\_** \] \[ **\_** \] tempo.

Devido à relação próxima em C entre matrizes e ponteiros, o MIDL também permite declarar matrizes em listas de parâmetros usando a notação de ponteiro. MIDL trata um parâmetro que é um ponteiro para um tipo como uma matriz desse tipo se o parâmetro tiver qualquer um dos atributos comumente associados a matrizes.

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45)
  version(6.0) 
]
interface arraytest
{
  void fArray6([in] short sSize, 
               [in, out, size_is(sSize)] char * p1);
  void fArray7([in] short sSize, 
               [in, out, size_is(sSize)] char achArray[]);
}
```

No exemplo anterior, os parâmetros de matriz e ponteiro nas funções fArray6 e fArray7 são equivalentes.

 

 