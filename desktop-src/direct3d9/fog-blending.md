---
description: A fusão de neblina refere-se à aplicação do fator de neblina às cores de neblina e objeto para produzir a cor final que aparece em uma cena, conforme discutido em fórmulas de neblina (Direct3D 9).
ms.assetid: b5b43f12-bbed-4464-aebc-02ad6dab1951
title: Fusão de neblina (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa918715a7bbe37b200568a0a9098135c5558b0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087216"
---
# <a name="fog-blending-direct3d-9"></a><span data-ttu-id="fd73b-103">Fusão de neblina (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fd73b-103">Fog Blending (Direct3D 9)</span></span>

<span data-ttu-id="fd73b-104">A fusão de neblina refere-se à aplicação do fator de neblina às cores de neblina e objeto para produzir a cor final que aparece em uma cena, conforme discutido em [fórmulas de neblina (Direct3D 9)](fog-formulas.md).</span><span class="sxs-lookup"><span data-stu-id="fd73b-104">Fog blending refers to the application of the fog factor to the fog and object colors to produce the final color that appears in a scene, as discussed in [Fog Formulas (Direct3D 9)](fog-formulas.md).</span></span> <span data-ttu-id="fd73b-105">A combinação de D3DRS \_ FOGENABLE renderizar controles de estado de neblina.</span><span class="sxs-lookup"><span data-stu-id="fd73b-105">The D3DRS\_FOGENABLE render state controls fog blending.</span></span> <span data-ttu-id="fd73b-106">Defina esse estado de renderização como **true** para habilitar a mesclagem de neblina, conforme mostrado no código de exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="fd73b-106">Set this render state to **TRUE** to enable fog blending as shown in the following example code.</span></span> <span data-ttu-id="fd73b-107">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="fd73b-107">The default is **FALSE**.</span></span>


```
// For this example, g_pDevice is a valid pointer
// to an IDirect3DDevice9 interface.
HRESULT hr;
hr = g_pDevice->SetRenderState(
                    D3DRS_FOGENABLE,
                    TRUE);
if FAILED(hr)
    return hr;
```



<span data-ttu-id="fd73b-108">Você deve habilitar a mesclagem de neblina para sombra de pixel e sombra de vértice.</span><span class="sxs-lookup"><span data-stu-id="fd73b-108">You must enable fog blending for both pixel fog and vertex fog.</span></span> <span data-ttu-id="fd73b-109">Para obter informações sobre como usar esses tipos de neblina, consulte [sombra de pixel (Direct3D 9)](pixel-fog.md) e [neblina de vértice (Direct3D 9)](vertex-fog.md).</span><span class="sxs-lookup"><span data-stu-id="fd73b-109">For information about using these types of fog, see [Pixel Fog (Direct3D 9)](pixel-fog.md) and [Vertex Fog (Direct3D 9)](vertex-fog.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd73b-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fd73b-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd73b-111">Tipos de neblina</span><span class="sxs-lookup"><span data-stu-id="fd73b-111">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 



