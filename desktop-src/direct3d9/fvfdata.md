---
description: Especifica os dados de malha menos os dados de posição.
ms.assetid: 30a95ca3-84ab-475d-9654-a3853263056b
title: FVFData
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52af6096357c4855d2dc34442c6cd4814b6713b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087384"
---
# <a name="fvfdata"></a>FVFData

Especifica os dados de malha menos os dados de posição.

``` syntax
template FVFData
{
    < B6E70A0E-8EF9-4e83-94AD-ECC8B0C04897 >
    DWORD dwFVF;
    DWORD nDWords;
    array DWORD data[nDWords];
} 
```

Em que:

-   dwFVF-um código FVF.
-   nDWords-dados binários. O número de DWORDs.
-   Data \[ nDWords \] -matriz de DWORDs que contêm os dados em cada elemento Vertex.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



