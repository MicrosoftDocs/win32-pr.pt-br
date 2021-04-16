---
description: Define um GUID que pode ser usado em outros modelos.
ms.assetid: dbfdd307-310f-4c80-b4aa-f16a81a9a372
title: GUID (DirectX 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e83e45d6e993153cf293a2ad55080c74f2e6049d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500395"
---
# <a name="guid-directx-9"></a>GUID (DirectX 9)

Define um GUID que pode ser usado em outros modelos.

``` syntax
template Guid
{
    < a42790e0-7810-11cf-8f52-0040333594a3 >
    DWORD data1;
    WORD data2;
    WORD data3;
    array UCHAR data4[8];
} 
```

Onde os parâmetros formam o formato de armazenamento binário para um GUID:

-   valor de dados inteiros sem sinal de data1-32-bit
-   o valor de dados inteiros sem sinal de data2 de 16 bits
-   data3-valor de dados inteiros sem sinal de 16 bits
-   data4-uma matriz de caracteres não assinados

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



