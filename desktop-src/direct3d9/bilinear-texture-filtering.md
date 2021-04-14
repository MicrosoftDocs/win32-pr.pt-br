---
description: As texturas são sempre endereçadas linearmente de (0,0, 0,0) no canto superior esquerdo para (1,0, 1,0) no canto inferior direito, conforme mostrado na ilustração a seguir.
ms.assetid: 16fb04b9-4476-4dbe-a24f-51c0813a7917
title: Filtragem de textura bilinear (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51213e5187c775963de2fa740847d55084c5be2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370484"
---
# <a name="bilinear-texture-filtering-direct3d-9"></a><span data-ttu-id="00c0a-103">Filtragem de textura bilinear (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="00c0a-103">Bilinear Texture Filtering (Direct3D 9)</span></span>

<span data-ttu-id="00c0a-104">As texturas são sempre endereçadas linearmente de (0,0, 0,0) no canto superior esquerdo para (1,0, 1,0) no canto inferior direito, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="00c0a-104">Textures are always linearly addressed from (0.0, 0.0) at the top-left corner to (1.0, 1.0) at the bottom-right corner, as shown in the following illustration.</span></span>

![ilustração de textura 4 x 4 com blocos sólidas de cor](images/bilinear-fig7a.png)

<span data-ttu-id="00c0a-106">As texturas geralmente são representadas como se fossem compostas de blocos sólidos de cor, mas é mais correto pensar nas texturas da mesma maneira que você pensaria na exibição de rasterização: cada texel é definido no centro exato de uma célula de grade, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="00c0a-106">Textures are usually represented as if they were composed of solid blocks of color, but it's actually more correct to think of textures the same way you should think of the raster display: Each texel is defined at the exact center of a grid cell, as shown in the following illustration.</span></span>

![ilustração de textura 4 x 4 com texels definidos no centro das células de grade](images/bilinear-fig7b.png)

<span data-ttu-id="00c0a-108">Se você solicitar a amostra de textura para a cor dessa textura nas coordenadas UV (0,375, 0,375), você receberá vermelho sólido (255, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="00c0a-108">If you ask the texture sampler for this texture's color at UV coordinates (0.375, 0.375) you'll get solid red (255, 0, 0).</span></span> <span data-ttu-id="00c0a-109">Isso faz sentido perfeito porque o centro exato da célula vermelha Texel está na UV (0,375, 0,375).</span><span class="sxs-lookup"><span data-stu-id="00c0a-109">That makes perfect sense because the exact center of the red texel cell is at UV (0.375, 0.375).</span></span> <span data-ttu-id="00c0a-110">E se você pedir a amostra de cor da textura UV (0,25, 0,25)?</span><span class="sxs-lookup"><span data-stu-id="00c0a-110">What if you ask the sampler for the texture's color at UV (0.25, 0.25)?</span></span> <span data-ttu-id="00c0a-111">Isso não é tão fácil, porque o ponto na UV (0,25, 0,25) está no canto exato de 4 texels.</span><span class="sxs-lookup"><span data-stu-id="00c0a-111">That's not quite as easy, because the point at UV (0.25, 0.25) lies at the exact corner of 4 texels.</span></span>

<span data-ttu-id="00c0a-112">O esquema mais simples é simplesmente fazer com que a amostra retorne a cor do Texel mais próximo; Isso é chamado de filtragem de ponto (consulte a [amostragem de ponto mais próximo (Direct3D 9)](nearest-point-sampling.md)) e geralmente é indesejável devido a resultados granulares ou de blocos.</span><span class="sxs-lookup"><span data-stu-id="00c0a-112">The simplest scheme is simply to have the sampler return the color of the closest texel; this is called Point filtering (see [Nearest-Point Sampling (Direct3D 9)](nearest-point-sampling.md)), and is usually undesirable due to grainy or blocky results.</span></span> <span data-ttu-id="00c0a-113">A amostragem de pontos de nossa textura em UV (0,25, 0,25) mostra outro problema sutil com filtragem por ponto mais próximo: há quatro texels equidistantes do ponto de amostra, por isso não há um único texel mais próximo.</span><span class="sxs-lookup"><span data-stu-id="00c0a-113">Point-sampling our texture at UV (0.25, 0.25) shows another subtle problem with nearest-point filtering: there are four texels equidistant from the sampling point, so there's no single nearest texel.</span></span> <span data-ttu-id="00c0a-114">Um desses quatro texels será escolhido como a cor retornada, mas a seleção depende de como a coordenada é arredondada, o que pode introduzir artefatos que causam danos (consulte o artigo sobre amostragem por ponto mais próximo no SDK).</span><span class="sxs-lookup"><span data-stu-id="00c0a-114">One of those four texels will be chosen as the returned color, but the selection depends on how the coordinate is rounded, which may introduce tearing artifacts (see the Nearest-Point Sampling article in the SDK).</span></span>

<span data-ttu-id="00c0a-115">Um esquema de filtragem um pouco mais preciso e mais comum é calcular a média ponderada do 4 texels mais próximo ao ponto de amostragem; Isso é chamado de filtragem bilinear, e o custo computacional extra geralmente é insignificante porque essa rotina é implementada em hardware de gráficos moderno.</span><span class="sxs-lookup"><span data-stu-id="00c0a-115">A slightly more accurate and more common filtering scheme is to calculate the weighted average of the 4 texels closest to the sampling point; this is called Bilinear filtering, and the extra computational cost is usually negligible because this routine is implemented in modern graphics hardware.</span></span> <span data-ttu-id="00c0a-116">Veja as cores que obtemos em alguns pontos de amostragem diferentes usando a filtragem bilinear:</span><span class="sxs-lookup"><span data-stu-id="00c0a-116">Here are the colors we get at a few different sample points using bilinear filtering:</span></span>


```
UV: (0.5, 0.5)
```



<span data-ttu-id="00c0a-117">Esse ponto fica localizado na borda exata entre os texels vermelhos, verdes, azuis e brancos.</span><span class="sxs-lookup"><span data-stu-id="00c0a-117">This point is at the exact border between red, green, blue, and white texels.</span></span> <span data-ttu-id="00c0a-118">A cor retornada pela amostragem é cinza:</span><span class="sxs-lookup"><span data-stu-id="00c0a-118">The color the sampler returns is gray:</span></span>


```
  0.25 * (255, 0, 0)
  0.25 * (0, 255, 0) 
  0.25 * (0, 0, 255) 
## + 0.25 * (255, 255, 255) 
------------------------
= (128, 128, 128)
```




```
UV: (0.5, 0.375)
```



<span data-ttu-id="00c0a-119">Esse ponto fica localizado no ponto intermediário da borda entre os texels vermelhos e verdes.</span><span class="sxs-lookup"><span data-stu-id="00c0a-119">This point is at the midpoint of the border between red and green texels.</span></span> <span data-ttu-id="00c0a-120">A cor retornada pela amostragem é amarelo-cinza (observe que as contribuições de texels azuis e brancos são dimensionadas como 0):</span><span class="sxs-lookup"><span data-stu-id="00c0a-120">The color the sampler returns is yellow-gray (note that the contributions of the blue and white texels are scaled to 0):</span></span>


```
  0.5 * (255, 0, 0)
  0.5 * (0, 255, 0) 
  0.0 * (0, 0, 255) 
## + 0.0 * (255, 255, 255) 
------------------------
= (128, 128, 0)
```




```
UV: (0.375, 0.375)
```



<span data-ttu-id="00c0a-121">Esse é o endereço do texel vermelho, que é a cor retornada (todos os outros texels do cálculo de filtragem são ponderados para 0):</span><span class="sxs-lookup"><span data-stu-id="00c0a-121">This is the address of the red texel, which is the returned color (all other texels in the filtering calculation are weighted to 0):</span></span>


```
  1.0 * (255, 0, 0)
  0.0 * (0, 255, 0) 
  0.0 * (0, 0, 255) 
## + 0.0 * (255, 255, 255) 
------------------------
= (255, 0, 0)
```



<span data-ttu-id="00c0a-122">Compare esses cálculos com a ilustração a seguir, que mostra o que acontece se o cálculo de filtragem bilinear for executado em cada endereço de textura na textura de 4 x 4.</span><span class="sxs-lookup"><span data-stu-id="00c0a-122">Compare these calculations against the following illustration, which shows what happens if the bilinear filtering calculation is performed at every texture address across the 4x4 texture.</span></span>

![Ilustração de textura 4 x 4 com filtragem bilinear realizada em todos os endereços de textura](images/bilinear-fig7c.jpg)

## <a name="related-topics"></a><span data-ttu-id="00c0a-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="00c0a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00c0a-125">Filtragem de textura</span><span class="sxs-lookup"><span data-stu-id="00c0a-125">Texture Filtering</span></span>](texture-filtering.md)
</dt> </dl>

 

 



