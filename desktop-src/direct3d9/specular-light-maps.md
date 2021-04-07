---
description: Quando iluminado por uma fonte de luz, objetos brilhantes-aqueles que usam materiais altamente refletidos – recebem destaques especulares.
ms.assetid: cea53131-1e2e-4389-80fd-ef5a0d068703
title: Mapas de luz especulares (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d55b4bf34baae0e73c2d072d62470533fc99827a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825761"
---
# <a name="specular-light-maps-direct3d-9"></a><span data-ttu-id="a218f-103">Mapas de luz especulares (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a218f-103">Specular Light Maps (Direct3D 9)</span></span>

<span data-ttu-id="a218f-104">Quando iluminado por uma fonte de luz, objetos brilhantes-aqueles que usam materiais altamente refletidos – recebem destaques especulares.</span><span class="sxs-lookup"><span data-stu-id="a218f-104">When illuminated by a light source, shiny objects - those that use highly reflective materials - receive specular highlights.</span></span> <span data-ttu-id="a218f-105">Em alguns casos, os realces especulares produzidos pelo módulo iluminação não são precisos.</span><span class="sxs-lookup"><span data-stu-id="a218f-105">In some cases, the specular highlights produced by the lighting module is not accurate.</span></span> <span data-ttu-id="a218f-106">Para produzir um realce mais atraente, muitos aplicativos Direct3D aplicam mapas de luz especulares a primitivos.</span><span class="sxs-lookup"><span data-stu-id="a218f-106">To produce a more appealing highlight, many Direct3D applications apply specular light maps to primitives.</span></span>

<span data-ttu-id="a218f-107">Para executar o mapeamento de luz especular, adicione o mapa de luz especular à textura do primitivo e module (multiplique o resultado por) o mapa de luz RGB.</span><span class="sxs-lookup"><span data-stu-id="a218f-107">To perform specular light mapping, add the specular light map to the primitive's texture, then modulate (multiply the result by) the RGB light map.</span></span>

<span data-ttu-id="a218f-108">O exemplo de código a seguir ilustra esse processo em C++.</span><span class="sxs-lookup"><span data-stu-id="a218f-108">The following code example illustrates this process in C++.</span></span>


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface.
// lptexBaseTexture is a valid pointer to a texture.
// lptexSpecLightMap is a valid pointer to a texture that contains RGB
// specular light map data.
// lptexLightMap is a valid pointer to a texture that contains RGB
// light map data.

// Set the base texture.
d3dDevice->SetTexture(0, lptexBaseTexture );

// Set the base texture operation and arguments.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE );

// Set the specular light map.
d3dDevice->SetTexture(1, lptexSpecLightMap);

// Set the specular light map operation and args.
d3dDevice->SetTextureStageState(1, D3DTSS_COLOROP, D3DTOP_ADD );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(1, D3DTSS_COLORARG2, D3DTA_CURRENT );

// Set the RGB light map.
d3dDevice->SetTexture(2, lptexLightMap);

// Set the RGB light map operation and arguments.
d3dDevice->SetTextureStageState(2,D3DTSS_COLOROP, D3DTOP_MODULATE);
d3dDevice->SetTextureStageState(2,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState(2,D3DTSS_COLORARG2, D3DTA_CURRENT );
```



## <a name="related-topics"></a><span data-ttu-id="a218f-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a218f-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a218f-110">Mapeamento claro com texturas</span><span class="sxs-lookup"><span data-stu-id="a218f-110">Light Mapping with Textures</span></span>](light-mapping-with-textures.md)
</dt> </dl>

 

 



