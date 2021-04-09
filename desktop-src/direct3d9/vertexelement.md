---
description: Descreve um elemento Vertex individual em uma declaração de vértice.
ms.assetid: efe3e98b-938d-4d4c-b790-2b8c8aab0ded
title: Vérticeelement
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 049511c89b335c0da31a9f41344082c3b818fa0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087680"
---
# <a name="vertexelement"></a>Vérticeelement

Descreve um elemento Vertex individual em uma declaração de vértice.

``` syntax
template VertexElement 
{ 
    < F752461C-1E23-48f6-B9F8-8350850F336F > 
    DWORD Type; 
    DWORD Method; 
    DWORD Usage; 
    DWORD UsageIndex; 
} 
```

Em que:

-   Tipo de dados de vértice de tipo. Consulte [**D3DDECLTYPE**](./d3ddecltype.md).
-   Método-método de processamento Tessellator. Consulte [**D3DDECLMETHOD**](./d3ddeclmethod.md).
-   Uso pretendido pelo uso dos dados de vértice. Consulte [**D3DDECLUSAGE**](./d3ddeclusage.md).
-   UsageIndex – modifica os dados de uso. Consulte [**D3DDECLUSAGE**](./d3ddeclusage.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> <dt>

[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)
</dt> </dl>

 

 
