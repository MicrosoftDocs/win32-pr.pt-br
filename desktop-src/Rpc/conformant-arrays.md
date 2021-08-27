---
title: Matrizes compatíveis
description: O tamanho de uma matriz compatível pode variar ou estar em conformidade sempre que o cliente a passar para um procedimento remoto no servidor.
ms.assetid: b4aaec77-b7ae-495d-8666-4702017e675f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19766b7b9552bcab08a4d194629892e51d5185ed39b0bedddbaef32f08cececf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073426"
---
# <a name="conformant-arrays"></a>Matrizes compatíveis

O tamanho de uma matriz compatível pode variar ou estar em conformidade sempre que o cliente a passar para um procedimento remoto no servidor. A definição de interface no arquivo MIDL do aplicativo permite que o cliente especifique o tamanho da matriz sempre que ele invocar o procedimento remoto. Use colchetes vazios ( ) ou um asterisco entre colchetes ( ) na definição da matriz para \[ \] indicar uma matriz \[ \* \] compatível.

O exemplo a seguir contém a definição de um procedimento remoto em uma interface em um arquivo MIDL. O cliente especifica o tamanho da matriz que ele passa para o servidor pelo parâmetro *arraySize*.

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

A definição da interface usa o tamanho do atributo MIDL para especificar o tamanho da matriz que o cliente passa para o \[ [**\_**](/windows/desktop/Midl/size-is) \] servidor. Se você preferir indicar o valor máximo dos números de índice da matriz, use o \[ [**atributo max \_ is.**](/windows/desktop/Midl/max-is) \] Para obter mais informações sobre esses atributos MIDL, consulte [Atributos de matriz](array-attributes.md).

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



Esse fragmento chama o procedimento remoto MyRemoteProc duas vezes. Na primeira invocação, ele passa uma matriz de 20 elementos. Na segunda chamada, o cliente passa uma matriz de 200 elementos.

 

 