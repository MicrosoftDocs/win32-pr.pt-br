---
description: A interpolação de vértices combina duas posições fornecidas pelo usuário (ou normais).
ms.assetid: vs|directx_sdk|~\vertex_tweening.htm
title: Interpolação de vértice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7a5458e384fa69b91b1eab1623fb526d514591f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163802"
---
# <a name="vertex-tweening-direct3d-9"></a><span data-ttu-id="40ec5-103">Interpolação de vértice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="40ec5-103">Vertex Tweening (Direct3D 9)</span></span>

<span data-ttu-id="40ec5-104">A interpolação de vértices combina duas posições fornecidas pelo usuário (ou normais).</span><span class="sxs-lookup"><span data-stu-id="40ec5-104">Vertex tweening blends two user-provided positions (or normals).</span></span> <span data-ttu-id="40ec5-105">A interpolação é mutuamente exclusiva da mistura de vértices com pesos.</span><span class="sxs-lookup"><span data-stu-id="40ec5-105">Tweening is mutually exclusive from vertex blending with weights.</span></span> <span data-ttu-id="40ec5-106">A interpolação é executada antes da iluminação e do recorte e é habilitada pela configuração de D3DRS \_ VERTEXBLEND para D3DVBF \_ interpolação.</span><span class="sxs-lookup"><span data-stu-id="40ec5-106">Tweening is performed before lighting and clipping, and is enabled by setting D3DRS\_VERTEXBLEND to D3DVBF\_TWEENING.</span></span> <span data-ttu-id="40ec5-107">A posição do vértice resultante é computada por:</span><span class="sxs-lookup"><span data-stu-id="40ec5-107">The resulting vertex position is computed by:</span></span>


```
POSITION = POSITION1 * (1.0 - TWEENFACTOR) + POSITION2 * TWEENFACTOR
```



<span data-ttu-id="40ec5-108">A mesma abordagem é usada para calcular Normals.</span><span class="sxs-lookup"><span data-stu-id="40ec5-108">The same approach is used for calculating normals.</span></span> <span data-ttu-id="40ec5-109">Para obter mais informações, consulte [usando a interpolação de vértices (Direct3D 9)](using-vertex-tweening.md).</span><span class="sxs-lookup"><span data-stu-id="40ec5-109">For more information, see [Using Vertex Tweening (Direct3D 9)](using-vertex-tweening.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="40ec5-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="40ec5-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40ec5-111">Mesclagem de geometria</span><span class="sxs-lookup"><span data-stu-id="40ec5-111">Geometry Blending</span></span>](geometry-blending.md)
</dt> </dl>

 

 



