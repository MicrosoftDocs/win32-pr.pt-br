---
title: Matrizes de conformidade
description: O tamanho de uma matriz compatível pode variar ou obedecer cada vez que o cliente a transmite para um procedimento remoto no servidor.
ms.assetid: b4aaec77-b7ae-495d-8666-4702017e675f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6f1491354f9cd26ef6100ab8d21f2ace3133f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007999"
---
# <a name="conformant-arrays"></a>Matrizes de conformidade

O tamanho de uma matriz compatível pode variar ou obedecer cada vez que o cliente a transmite para um procedimento remoto no servidor. A definição de interface no arquivo MIDL do aplicativo permite que o cliente especifique o tamanho da matriz cada vez que invoca o procedimento remoto. Use colchetes vazios ( \[ \] ) ou um asterisco entre colchetes ( \[ \* \] ) na definição da matriz para indicar uma matriz compatível.

O exemplo a seguir contém a definição de um procedimento remoto em uma interface em um arquivo MIDL. O cliente especifica o tamanho da matriz que passa para o servidor pelo parâmetro *arrayize*.

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    MyRemoteProc(
         long lArraySize,
         [size_is(lArraySize)] char achArray[*]
    );

    /* Other interface procedures are defined here. */
}
```

A definição de interface usa o tamanho do atributo MIDL \[ [**\_ é**](/windows/desktop/Midl/size-is) \] especificar o tamanho da matriz que o cliente passa para o servidor. Se você preferir indicar o valor máximo dos números de índice da matriz, use o atributo \[ [**Max \_**](/windows/desktop/Midl/max-is) \] em vez disso. Para obter mais informações sobre esses atributos de MIDL, consulte [atributos de matriz](array-attributes.md).

O fragmento de código a seguir ilustra como um cliente pode invocar o procedimento remoto definido no arquivo MIDL anterior.


```C++
long lArrayLength = 20;
char achCharArray[20], achAnotherCharArray[200];

// Code to store 20 chars in achCharArray goes here.

MyRemoteProc(
    lArrayLength ,
    achCharArray);

lArrayLength = 200;

// Code to store 200 chars in achAnotherCharArray goes here.

MyRemoteProc(
    lArrayLength ,
    achAnotherCharArray);
```



Esse fragmento chama o procedimento remoto MyRemoteProc duas vezes. Na primeira invocação, ele passa uma matriz de 20 elementos. Na segunda chamada, o cliente passa uma matriz de elementos 200.

 

 