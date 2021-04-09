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
# <a name="vertexelement"></a><span data-ttu-id="14380-103">Vérticeelement</span><span class="sxs-lookup"><span data-stu-id="14380-103">VertexElement</span></span>

<span data-ttu-id="14380-104">Descreve um elemento Vertex individual em uma declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="14380-104">Describes an individual vertex element in a vertex declaration.</span></span>

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

<span data-ttu-id="14380-105">Em que:</span><span class="sxs-lookup"><span data-stu-id="14380-105">Where:</span></span>

-   <span data-ttu-id="14380-106">Tipo de dados de vértice de tipo.</span><span class="sxs-lookup"><span data-stu-id="14380-106">Type - Vertex data type.</span></span> <span data-ttu-id="14380-107">Consulte [**D3DDECLTYPE**](./d3ddecltype.md).</span><span class="sxs-lookup"><span data-stu-id="14380-107">See [**D3DDECLTYPE**](./d3ddecltype.md).</span></span>
-   <span data-ttu-id="14380-108">Método-método de processamento Tessellator.</span><span class="sxs-lookup"><span data-stu-id="14380-108">Method - Tessellator processing method.</span></span> <span data-ttu-id="14380-109">Consulte [**D3DDECLMETHOD**](./d3ddeclmethod.md).</span><span class="sxs-lookup"><span data-stu-id="14380-109">See [**D3DDECLMETHOD**](./d3ddeclmethod.md).</span></span>
-   <span data-ttu-id="14380-110">Uso pretendido pelo uso dos dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="14380-110">Usage - Intended use of the vertex data.</span></span> <span data-ttu-id="14380-111">Consulte [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="14380-111">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>
-   <span data-ttu-id="14380-112">UsageIndex – modifica os dados de uso.</span><span class="sxs-lookup"><span data-stu-id="14380-112">UsageIndex - Modifies the usage data.</span></span> <span data-ttu-id="14380-113">Consulte [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="14380-113">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="14380-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="14380-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14380-115">Modelos</span><span class="sxs-lookup"><span data-stu-id="14380-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> <dt>

[<span data-ttu-id="14380-116">**D3DVERTEXELEMENT9**</span><span class="sxs-lookup"><span data-stu-id="14380-116">**D3DVERTEXELEMENT9**</span></span>](d3dvertexelement9.md)
</dt> </dl>

 

 
