---
title: Indicadores de tipo
description: As propriedades reais seguem a tabela de valores do conjunto de propriedades de identificadores de propriedade/pares de deslocamento. Cada propriedade é armazenada como uma DWORD, seguida pelo valor do tipo de dados.
ms.assetid: 8523458b-8b1b-4e9f-8f96-d7601e57675c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e6372db4d3f1d7bfee9b6c9d2435f9c8d5a7be6d7cce123c5b8b2185ac092c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117959547"
---
# <a name="type-indicators"></a>Indicadores de tipo

As propriedades reais seguem a tabela de valores do conjunto de propriedades de identificadores de propriedade/pares de deslocamento. Cada propriedade é armazenada como uma **DWORD**, seguida pelo valor do tipo de dados.

Os indicadores de tipo e seus valores associados são descritos na estrutura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Todos os pares de tipo/valor devem começar em um limite de 32 bits. Assim, os valores podem ser seguidos com bytes nulos para alinhar o par subsequente em um limite de 32 bits.

O código de exemplo a seguir calcula quantos bytes são necessários para alinhar em um limite de 32 bits, dada uma contagem de bytes.


```C++
cbAdd = (((cbCurrent + 3) >> 2) << 2) - cbCurrent ;
```



Dentro de um vetor de valores, cada repetição de um valor escalar simples menor que 32 bits deve ser alinhada com seu alinhamento natural, e não com um alinhamento de 32 bits. Na prática, isso só é significativo para os **tipos \_ VT UI1**, **VT \_ UI2**, **VT \_ i2** e **VT \_ bool** (que têm alinhamento natural de um ou dois bytes). Todos os outros tipos têm alinhamento natural de quatro bytes. Alguns tipos, por exemplo, **a \_ R8 de VT**, na verdade têm um alinhamento natural de 8 bytes, mas são armazenados como se tivessem um alinhamento de quatro bytes.

Um valor de propriedade com o símbolo de tipo **VT \_ i2** \| **VT \_ vector** incluiria:

-   Uma contagem de elementos **DWORD** .
-   Uma sequência de inteiros de dois bytes empacotados sem nenhum preenchimento nulo entre eles.

> [!IMPORTANT]
> Quaisquer contagens de 32 bits ou tipos de propriedade que são armazenados como parte de um elemento de propriedade de vetor também devem ser alinhados em 32 bits.

 

Um valor de Propriedade do tipo identificador **VT \_ LPSTR** do \| **\_ vetor VT** incluiria:

-   Uma contagem de elementos **DWORD** (**DWORD** *cElems*).
-   Uma sequência de cadeias de caracteres (**Char** *rgch \[ \]*), cada uma precedida por um **DWORD** de contagem de comprimento e possivelmente seguida por um preenchimento nulo para arredondar para um limite de 32 bits.

 

 