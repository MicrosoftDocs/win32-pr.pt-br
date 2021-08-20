---
description: Define um GUID que pode ser usado em outros modelos.
ms.assetid: dbfdd307-310f-4c80-b4aa-f16a81a9a372
title: GUID (DirectX 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57869992cc080be77cde5f065a895698c7983989f6268df09e0aa2714930f059
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094713"
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

Em que os parâmetros juntos formam o formato de armazenamento binário para um GUID:

-   data1 – valor de dados inteiro sem sinal de 32 bits
-   data2 – valor de dados inteiro sem sinal de 16 bits
-   data3 – valor de dados inteiro sem sinal de 16 bits
-   data4 – uma matriz de caracteres não assinados

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



