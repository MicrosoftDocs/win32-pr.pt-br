---
title: O atributo de cadeia de caracteres em matrizes
description: Você pode usar o atributo \ String \ para matrizes de caracteres unidimensionais, matrizes de caracteres largos e matrizes de bytes que representam cadeias de texto.
ms.assetid: 96cebb84-6123-4bf8-b70b-a4f6d48cce52
keywords:
- string
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8bd2f7234b2713b6a7df05cfb5d6ae4c08b2d8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084725"
---
# <a name="the-string-attribute-in-arrays"></a>O \[ atributo de cadeia \] de caracteres em matrizes

Você pode usar o \[ [](/windows/desktop/Midl/string) \] atributo String para matrizes de caracteres unidimensionais, matrizes de caracteres largos e matrizes de bytes que representam cadeias de texto. Se você usar o atributo de **\[ cadeia de caracteres \]** , o stub do cliente usará as funções **strlen** ou **wstrlen** da biblioteca C para contar o número de caracteres na cadeia de caracteres. Para evitar possíveis inconsistências, MIDL não permite que você use o atributo de **\[ cadeia de caracteres \]** ao mesmo tempo que o \[ [primeiro \_ é](/windows/desktop/Midl/first-is), o \] \[ [último \_](/windows/desktop/Midl/last-is) \] , e o \[ [tamanho \_ são](/windows/desktop/Midl/size-is) \] atributos.

Com cadeias de caracteres terminadas em nulo em C, você deve permitir espaço para o caractere nulo no final da cadeia de caracteres. Por exemplo, ao declarar uma cadeia de caracteres que irá conter até 80 caracteres, aloque 81 caracteres. O arquivo IDL de exemplo a seguir demonstra como declarar matrizes com o atributo de **\[ cadeia de caracteres \]** .

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(8.0)
]
interface arraytest
{
  void fArray8([in, out, string] char achArray[]);
}
```

 

 