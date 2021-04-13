---
description: O mecanismo de iluminação Direct3D pode usar dados de cor por vértice ao executar a iluminação se você informar ao tempo de execução que os dados estão presentes.
ms.assetid: acb43921-f0d4-4151-9371-1b99e5d30c0e
title: Estado de cor de Per-Vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0104b427753fa3d7b7cf5a0a5a10cfeb5d10f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370051"
---
# <a name="per-vertex-color-state-direct3d-9"></a><span data-ttu-id="d3505-103">Estado de cor de Per-Vertex (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d3505-103">Per-Vertex Color State (Direct3D 9)</span></span>

<span data-ttu-id="d3505-104">O mecanismo de iluminação Direct3D pode usar dados de cor por vértice ao executar a iluminação se você informar ao tempo de execução que os dados estão presentes.</span><span class="sxs-lookup"><span data-stu-id="d3505-104">The Direct3D lighting engine can use per-vertex color data when performing lighting if you tell the runtime the data is present.</span></span> <span data-ttu-id="d3505-105">Isso é feito ativando o seguinte estado de renderização:</span><span class="sxs-lookup"><span data-stu-id="d3505-105">This is done by turning on the following render state:</span></span>


```
// disable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, FALSE);

// enable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, TRUE);
```



<span data-ttu-id="d3505-106">Se a cor por vértice estiver habilitada, os aplicativos poderão configurar a origem da qual o sistema recupera informações de cores para um vértice.</span><span class="sxs-lookup"><span data-stu-id="d3505-106">If per-vertex color is enabled, applications can configure the source from which the system retrieves color information for a vertex.</span></span> <span data-ttu-id="d3505-107">Os \_ Estados de RENDERIZAÇÃO D3DRS AMBIENTMATERIALSOURCE, D3DRS \_ DiffuseMaterialSource, D3DRS \_ EMISSIVEMATERIALSOURCE e D3DRS \_ SPECULARMATERIALSOURCE controlam as fontes de componente de cor ambiente, difuso, emissiva e especular, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d3505-107">The D3DRS\_AMBIENTMATERIALSOURCE, D3DRS\_DIFFUSEMATERIALSOURCE, D3DRS\_EMISSIVEMATERIALSOURCE, and D3DRS\_SPECULARMATERIALSOURCE render states control the ambient, diffuse, emissive, and specular color component sources, respectively.</span></span> <span data-ttu-id="d3505-108">Cada Estado pode ser definido como membros do tipo enumerado [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) , que define constantes que instruem o sistema a usar o material atual, a cor difusa ou a cor especular como a origem do componente de cor especificado.</span><span class="sxs-lookup"><span data-stu-id="d3505-108">Each state can be set to members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type, which defines constants that instruct the system to use the current material, diffuse color, or specular color as the source for the specified color component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3505-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d3505-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3505-110">Processar Estados</span><span class="sxs-lookup"><span data-stu-id="d3505-110">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
