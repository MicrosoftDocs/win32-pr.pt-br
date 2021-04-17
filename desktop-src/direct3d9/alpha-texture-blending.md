---
description: O mecanismo de iluminação combina a cor do material, a cor do vértice e as informações de iluminação para gerar uma cor por vértice.
ms.assetid: 1e7c31cb-dc63-4f4a-9ddc-d1d1d0b69085
title: Mesclagem de textura alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad394b70b96e17b2ce858f871fb869afde0d122
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812868"
---
# <a name="alpha-texture-blending-direct3d-9"></a><span data-ttu-id="ec660-103">Mesclagem de textura alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ec660-103">Alpha Texture Blending (Direct3D 9)</span></span>

<span data-ttu-id="ec660-104">O mecanismo de iluminação combina a cor do material, a cor do vértice e as informações de iluminação para gerar uma cor por vértice.</span><span class="sxs-lookup"><span data-stu-id="ec660-104">The lighting engine combines material color, vertex color, and lighting information to generate a per-vertex color.</span></span> <span data-ttu-id="ec660-105">Depois de interpolado, isso gera uma cor por pixel que é gravada no buffer de quadro.</span><span class="sxs-lookup"><span data-stu-id="ec660-105">Once interpolated, this generates a per-pixel color that is written to the frame buffer.</span></span> <span data-ttu-id="ec660-106">Se um aplicativo habilitar a mesclagem de textura, a cor do pixel se tornará uma combinação do pixel atual no buffer do quadro e uma cor de textura.</span><span class="sxs-lookup"><span data-stu-id="ec660-106">If an application enables texture blending, the pixel color will become a combination of the current pixel in the frame buffer and a texture color.</span></span>

<span data-ttu-id="ec660-107">Esta fórmula determina a cor do pixel misturado final:</span><span class="sxs-lookup"><span data-stu-id="ec660-107">This formula determines the final blended pixel color:</span></span>


```
Color = TexelColor x SourceBlend + CurrentPixelColor x DestBlend
```



<span data-ttu-id="ec660-108">Em que:</span><span class="sxs-lookup"><span data-stu-id="ec660-108">Where:</span></span>

-   <span data-ttu-id="ec660-109">Color é a cor do pixel de saída.</span><span class="sxs-lookup"><span data-stu-id="ec660-109">Color is the output pixel color.</span></span>
-   <span data-ttu-id="ec660-110">TexelColor é a cor de entrada após a filtragem de textura.</span><span class="sxs-lookup"><span data-stu-id="ec660-110">TexelColor is the input color after texture filtering.</span></span>
-   <span data-ttu-id="ec660-111">SourceBlend é a porcentagem da cor de pixel final que é composta pela cor de Texel de origem.</span><span class="sxs-lookup"><span data-stu-id="ec660-111">SourceBlend is the percentage of the final pixel color that is made up of the source texel color.</span></span>
-   <span data-ttu-id="ec660-112">CurrentPixelColor é a cor do pixel atual.</span><span class="sxs-lookup"><span data-stu-id="ec660-112">CurrentPixelColor is the color of the current pixel.</span></span>
-   <span data-ttu-id="ec660-113">DestBlend é a porcentagem da cor final do pixel que é composta pela cor atual do pixel.</span><span class="sxs-lookup"><span data-stu-id="ec660-113">DestBlend is the percentage of the final pixel color that is made up of the current pixel color.</span></span>

<span data-ttu-id="ec660-114">A equação de mesclagem final é definida chamando [**IDirect3DDevice9:: Setrenderingstate**](/windows/desktop/api) e especificando o estado de renderização de Blend (D3DRS \_ BLENDXXX) com um fator de mistura correspondente ([**D3DBLEND**](./d3dblend.md)).</span><span class="sxs-lookup"><span data-stu-id="ec660-114">The final blending equation is set by calling [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) and specifying the blend render state (D3DRS\_BLENDXXX) with a corresponding blending factor ([**D3DBLEND**](./d3dblend.md)).</span></span> <span data-ttu-id="ec660-115">Os valores de SourceBlend e DestBlend variam de 0,0 (transparente) a 1,0 (opaco) inclusive.</span><span class="sxs-lookup"><span data-stu-id="ec660-115">The values of SourceBlend and DestBlend range from 0.0 (transparent) to 1.0 (opaque) inclusive.</span></span> <span data-ttu-id="ec660-116">Além disso, um aplicativo pode controlar a transparência de um pixel definindo o valor alfa em uma textura.</span><span class="sxs-lookup"><span data-stu-id="ec660-116">In addition, an application can control the transparency of a pixel by setting the alpha value in a texture.</span></span> <span data-ttu-id="ec660-117">Nesse caso, use o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ec660-117">In this case, use the following:</span></span>


```
SourceBlend = D3DBLEND_ZERO 
DestBlend = D3DBLEND_ONE
```



<span data-ttu-id="ec660-118">A equação de mesclagem fará com que o pixel renderizado seja transparente.</span><span class="sxs-lookup"><span data-stu-id="ec660-118">The blending equation will cause the rendered pixel to be transparent.</span></span> <span data-ttu-id="ec660-119">Os valores padrão são:</span><span class="sxs-lookup"><span data-stu-id="ec660-119">The default values are:</span></span>


```
SourceBlend = D3DBLEND_SRCALPHA 
DestBlend = D3DBLEND_INVSRCALPHA
```



## <a name="related-topics"></a><span data-ttu-id="ec660-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ec660-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec660-121">Mesclagem de textura</span><span class="sxs-lookup"><span data-stu-id="ec660-121">Texture Blending</span></span>](texture-blending.md)
</dt> <dt>

[<span data-ttu-id="ec660-122">Filtragem de textura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ec660-122">Texture Filtering (Direct3D 9)</span></span>](texture-filtering.md)
</dt> <dt>

[<span data-ttu-id="ec660-123">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="ec660-123">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
