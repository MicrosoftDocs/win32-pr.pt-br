---
description: Seu aplicativo geralmente renderizará cenas 3D de forma mais realista se usar mapas de luz coloridos. Um mapa de luz colorido usa os dados RGB no mapa de luz para saber da iluminação.
ms.assetid: 47760884-7b9f-45de-9d4a-faf822da899f
title: Mapas de luz de cor (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 621c5056fe2cbb9e6446adfb5dcad3079c0d90bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456988"
---
# <a name="color-light-maps-direct3d-9"></a><span data-ttu-id="39470-104">Mapas de luz de cor (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="39470-104">Color Light Maps (Direct3D 9)</span></span>

<span data-ttu-id="39470-105">Seu aplicativo geralmente renderizará cenas 3D de forma mais realista se usar mapas de luz coloridos.</span><span class="sxs-lookup"><span data-stu-id="39470-105">Your application will usually render 3D scenes more realistically if it uses colored light maps.</span></span> <span data-ttu-id="39470-106">Um mapa de luz colorido usa os dados RGB no mapa de luz para saber da iluminação.</span><span class="sxs-lookup"><span data-stu-id="39470-106">A colored light map uses the RGB data in the light map for its lighting information.</span></span>

<span data-ttu-id="39470-107">O exemplo de código C++ a seguir demonstra o mapeamento claro com dados de cores RGB.</span><span class="sxs-lookup"><span data-stu-id="39470-107">The following C++ code example demonstrates light mapping with RGB color data.</span></span>


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface and that lptexLightMap is a valid
// pointer to a texture that contains RGB light map data.

// Set the light map texture as the first texture.
d3dDevice->SetTexture(0, lptexLightMap);

d3dDevice->SetTextureStageState( 0,D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState( 0,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 0,D3DTSS_COLORARG2, D3DTA_DIFFUSE );
```



<span data-ttu-id="39470-108">Este exemplo define o mapa claro como a primeira textura.</span><span class="sxs-lookup"><span data-stu-id="39470-108">This example sets the light map as the first texture.</span></span> <span data-ttu-id="39470-109">Em seguida, ele define o estado do primeiro estágio de mesclagem para modular os dados de textura de entrada.</span><span class="sxs-lookup"><span data-stu-id="39470-109">It then sets the state of the first blending stage to modulate the incoming texture data.</span></span> <span data-ttu-id="39470-110">Ele usa a primeira textura e a cor atual do primitivo como os argumentos para a operação modular.</span><span class="sxs-lookup"><span data-stu-id="39470-110">It uses the first texture and the current color of the primitive as the arguments to the modulate operation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39470-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="39470-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39470-112">Mapeamento claro com texturas</span><span class="sxs-lookup"><span data-stu-id="39470-112">Light Mapping with Textures</span></span>](light-mapping-with-textures.md)
</dt> </dl>

 

 



