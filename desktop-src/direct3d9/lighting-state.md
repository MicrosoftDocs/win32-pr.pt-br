---
description: Se você não acender com um sombreador de vértice ou um sombreador de pixel, poderá optar por usar o mecanismo de iluminação no tempo de execução.
ms.assetid: vs|directx_sdk|~\lighting_state.htm
title: Estado de iluminação (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74f0e7b7ec4a8bcf0ee27c9bc1e643536819d8fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105793277"
---
# <a name="lighting-state-direct3d-9"></a><span data-ttu-id="5bf45-103">Estado de iluminação (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5bf45-103">Lighting State (Direct3D 9)</span></span>

<span data-ttu-id="5bf45-104">Se você não acender com um sombreador de vértice ou um sombreador de pixel, poderá optar por usar o mecanismo de iluminação no tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="5bf45-104">If you do not light with a vertex shader or a pixel shader, you may choose to use the lighting engine in the runtime.</span></span> <span data-ttu-id="5bf45-105">O mecanismo de iluminação requer que os dados de vértice contenham normalidades por vértice; os vértices sem dados normais gerarão um produto de ponto zero em todos os cálculos de iluminação.</span><span class="sxs-lookup"><span data-stu-id="5bf45-105">The lighting engine requires that the vertex data contains per-vertex normals; vertices without normal data will generate a dot product of zero in all lighting computations.</span></span> <span data-ttu-id="5bf45-106">Os cálculos de iluminação são abordados em mais detalhes na [matemática de iluminação (Direct3D 9)](mathematics-of-lighting.md).</span><span class="sxs-lookup"><span data-stu-id="5bf45-106">The lighting calculations are covered in more detail in [Mathematics of Lighting (Direct3D 9)](mathematics-of-lighting.md).</span></span>

<span data-ttu-id="5bf45-107">Para habilitar o mecanismo de iluminação, use:</span><span class="sxs-lookup"><span data-stu-id="5bf45-107">To enable the lighting engine, use:</span></span>


```
SetRenderState(D3DRS_LIGHTING, TRUE); 
```



## <a name="related-topics"></a><span data-ttu-id="5bf45-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5bf45-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bf45-109">Processar Estados</span><span class="sxs-lookup"><span data-stu-id="5bf45-109">Render States</span></span>](render-states.md)
</dt> </dl>

 

 



