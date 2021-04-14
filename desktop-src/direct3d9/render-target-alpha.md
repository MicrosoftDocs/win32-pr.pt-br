---
description: O misturador de buffer de quadro agora pode misturar canais alfa independentemente da mistura de canal de cor em destinos de renderização. Esse controle é habilitado com um novo estado de renderização, D3DRS \_ SEPARATEALPHABLENDENABLE.
ms.assetid: 6d30b13e-f4c6-4bc4-8735-15c398c099f1
title: Processamento alfa de destino (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b70f395406559782172448b5555daff056ffd54c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500156"
---
# <a name="render-target-alpha-direct3d-9"></a><span data-ttu-id="7e30a-104">Processamento alfa de destino (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7e30a-104">Render Target Alpha (Direct3D 9)</span></span>

<span data-ttu-id="7e30a-105">O misturador de buffer de quadro agora pode misturar canais alfa independentemente da mistura de canal de cor em destinos de renderização.</span><span class="sxs-lookup"><span data-stu-id="7e30a-105">The frame buffer blender can now blend alpha channels independent from color-channel blending on render targets.</span></span> <span data-ttu-id="7e30a-106">Esse controle é habilitado com um novo estado de renderização, D3DRS \_ SEPARATEALPHABLENDENABLE.</span><span class="sxs-lookup"><span data-stu-id="7e30a-106">This control is enabled with a new render state, D3DRS\_SEPARATEALPHABLENDENABLE.</span></span>

<span data-ttu-id="7e30a-107">Quando D3DRS \_ SEPARATEALPHABLENDENABLE é definido como **false** (que é a condição padrão), os fatores de mesclagem de destino de renderização e as operações aplicadas a Alpha são iguais às definidas para mesclagem de canais de cores.</span><span class="sxs-lookup"><span data-stu-id="7e30a-107">When D3DRS\_SEPARATEALPHABLENDENABLE is set to **FALSE** (which is the default condition), the render-target blending factors and operations applied to alpha are the same as those defined for blending color channels.</span></span> <span data-ttu-id="7e30a-108">Um driver precisa definir o limite de D3DPMISCCAPS \_ SEPARATEALPHABLEND para indicar que ele pode dar suporte à mesclagem alfa de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="7e30a-108">A driver needs to set the D3DPMISCCAPS\_SEPARATEALPHABLEND cap to indicate that it can support render-target alpha blending.</span></span> <span data-ttu-id="7e30a-109">Certifique-se de habilitar D3DRS \_ ALPHABLEND para informar ao pipeline que a mistura alfa é necessária.</span><span class="sxs-lookup"><span data-stu-id="7e30a-109">Be sure to enable D3DRS\_ALPHABLEND to tell the pipeline that alpha blending is needed.</span></span>

<span data-ttu-id="7e30a-110">Para controlar os fatores no canal alfa dos misturadores de destino de renderização, dois novos Estados de renderização são definidos da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7e30a-110">To control the factors in the alpha channel of the render-target blenders, two new render states are defined as follows:</span></span>


```
D3DRS_SRCBLENDALPHA 
D3DRS_DESTBLENDALPHA 
```



<span data-ttu-id="7e30a-111">Como o D3DRS \_ SRCBLEND e D3DRS \_ DESTBLEND, eles podem ser definidos como um dos valores na enumeração [**D3DBLEND**](./d3dblend.md) .</span><span class="sxs-lookup"><span data-stu-id="7e30a-111">Like the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND, these can be set to one of the values in the [**D3DBLEND**](./d3dblend.md) enumeration.</span></span> <span data-ttu-id="7e30a-112">As configurações de mesclagem de origem e destino podem ser combinadas de várias maneiras, dependendo das configurações nos membros SrcBlendCaps e DestBlendCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="7e30a-112">The source and destination blend settings can be combined in several ways, depending on the settings in the SrcBlendCaps and DestBlendCaps members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

<span data-ttu-id="7e30a-113">A combinação alfa é feita da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7e30a-113">The alpha blending is done as follows:</span></span>

<span data-ttu-id="7e30a-114">renderTargetAlpha = (Alpha<sub>em</sub> \* srcBlendOp) BlendOp (Alpha<sub>RT</sub> \* destBlendOp)</span><span class="sxs-lookup"><span data-stu-id="7e30a-114">renderTargetAlpha = (alpha<sub>in</sub> \* srcBlendOp) BlendOp (alpha<sub>rt</sub> \* destBlendOp)</span></span>

<span data-ttu-id="7e30a-115">Em que:</span><span class="sxs-lookup"><span data-stu-id="7e30a-115">Where:</span></span>

-   <span data-ttu-id="7e30a-116">Alfa<sub>in</sub> é o valor alfa de entrada.</span><span class="sxs-lookup"><span data-stu-id="7e30a-116">alpha<sub>in</sub> is the input alpha value.</span></span>
-   <span data-ttu-id="7e30a-117">srcBlendOp é um dos fatores de mistura em [**D3DBLEND**](./d3dblend.md).</span><span class="sxs-lookup"><span data-stu-id="7e30a-117">srcBlendOp is one of the blend factors in [**D3DBLEND**](./d3dblend.md).</span></span>
-   <span data-ttu-id="7e30a-118">BlendOp é um dos fatores de mistura em [**D3DBLENDOP**](./d3dblendop.md).</span><span class="sxs-lookup"><span data-stu-id="7e30a-118">BlendOp is one of the blend factors in [**D3DBLENDOP**](./d3dblendop.md).</span></span>
-   <span data-ttu-id="7e30a-119">o Alpha<sub>RT</sub> é o valor alfa do destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="7e30a-119">alpha<sub>rt</sub> is the render-target alpha value.</span></span>
-   <span data-ttu-id="7e30a-120">destBlendOp é um dos fatores de mistura em [**D3DBLEND**](./d3dblend.md).</span><span class="sxs-lookup"><span data-stu-id="7e30a-120">destBlendOp is one of the blend factors in [**D3DBLEND**](./d3dblend.md).</span></span>
-   <span data-ttu-id="7e30a-121">renderTargetAlpha é o valor alfa combinado final.</span><span class="sxs-lookup"><span data-stu-id="7e30a-121">renderTargetAlpha is the final blended alpha value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e30a-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7e30a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e30a-123">Mesclagem alfa</span><span class="sxs-lookup"><span data-stu-id="7e30a-123">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 
