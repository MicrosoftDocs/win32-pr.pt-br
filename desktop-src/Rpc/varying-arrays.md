---
title: Matrizes variáveis
description: No MIDL, matrizes variadas são fixas em tamanho. Eles permitem que os clientes passem diferentes partes de matrizes de clientes para servidores. O tamanho da parte da matriz pode variar de invocação para invocação. No entanto, o tamanho da matriz geral é fixo.
ms.assetid: 31c4bc63-de55-4937-832e-8dde9bcc47b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b2d79ee37f3e366bbf232b362306f78ca6ada4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454255"
---
# <a name="varying-arrays"></a>Matrizes variáveis

No MIDL, matrizes variadas são fixas em tamanho. Eles permitem que os clientes passem diferentes partes de matrizes de clientes para servidores. O tamanho da parte da matriz pode variar de invocação para invocação. No entanto, o tamanho da matriz geral é fixo.

Por exemplo, o exemplo a seguir mostra a definição de um procedimento remoto em uma interface em um arquivo MIDL. O tamanho da matriz que o cliente passa para o servidor é fixo pelo tamanho da matriz constante \_ . A interface especifica a parte da matriz que o cliente passa para o servidor nos parâmetros firstelement e chunkSize.

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    const long ARRAY_SIZE = 1000;

    MyRemoteProc(
        [in] long lFirstElement,
        [in] long lChunkSize,
        [in, first_is(lFirstElement), 
          length_is(lChunkSize)] char achArray[ARRAY_SIZE]
    );

    /* Other interface procedures are defined here. */
}
```

A definição de interface usa o atributo MIDL \[ [**primeiro \_ é**](/windows/desktop/Midl/first-is) \] especificar o número de índice do primeiro elemento na parte da matriz que o cliente passa para o servidor. O \[ [**tamanho \_ é**](/windows/desktop/Midl/length-is) \] atributo especifica o número total de elementos de matriz que o cliente passa. Para obter mais informações sobre esses atributos de MIDL, consulte [atributos de matriz](array-attributes.md).

O fragmento de código a seguir ilustra como um cliente pode invocar o procedimento remoto definido no arquivo MIDL anterior.


```C++
long lFirstArrayElementNumber = 20;
long lTotalElementsPassed = 100;
char achCharArray[ARRAY_SIZE];

// Code to store chars in the array goes here.

MyRemoteProc(
    lFirstArrayElementNumber ,
    lTotalElementsPassed , 
    achCharArray);

firstArrayElementNumber = 120;
totalElementsPassed = 200;

MyRemoteProc(
    lFirstArrayElementNumber ,
    lTotalElementsPassed , 
    achCharArray);
```



Esse fragmento chama o procedimento remoto MyRemoteProc duas vezes. Na primeira invocação, ele passa os elementos de matriz numerados 20 a 119, conforme indicado pelos valores nas variáveis firstArrayElementNumber e totalElementsPassed. Na segunda chamada, o cliente passa os elementos de matriz numerados de 120 a 319.

 

 