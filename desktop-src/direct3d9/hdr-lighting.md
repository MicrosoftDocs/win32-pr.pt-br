---
description: A iluminação no mundo real contém um HDR (intervalo dinâmico) muito alto de valores de luminância.
ms.assetid: 537700e2-802d-4fd1-b026-142d6f4f0559
title: Iluminação HDR (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f397ccef2b1fa315e64861453b13f0f6fddfe77
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163678"
---
# <a name="hdr-lighting-direct3d-9"></a><span data-ttu-id="0f6af-103">Iluminação HDR (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0f6af-103">HDR Lighting (Direct3D 9)</span></span>

<span data-ttu-id="0f6af-104">A iluminação no mundo real contém um HDR (intervalo dinâmico) muito alto de valores de luminância.</span><span class="sxs-lookup"><span data-stu-id="0f6af-104">Lighting in the real world contains a very high dynamic range (HDR) of luminance values.</span></span> <span data-ttu-id="0f6af-105">O mundo real tem cerca de 10 pedidos de DR (intervalo dinâmico) para valores de luminância espalhados pelo espectro de escurecimento até o brilho.</span><span class="sxs-lookup"><span data-stu-id="0f6af-105">The real world has about 10 orders of dynamic range (DR) for luminance values spread across the spectrum of darkness to brightness.</span></span> <span data-ttu-id="0f6af-106">Por outro lado, uma tela de computador tem uma gama de monitores muito limitada (ou um intervalo de valores de luminância): aproximadamente duas ordens de intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="0f6af-106">On the other hand, a computer screen has a very limited display gamut (or range of luminance values): approximately two orders of dynamic range.</span></span> <span data-ttu-id="0f6af-107">O desafio de produzir imagens do HDR renderizadas é mapear os valores HDR do mundo real para a gama limitada de uma tela de computador.</span><span class="sxs-lookup"><span data-stu-id="0f6af-107">The challenge to producing HDR rendered images is to map the real world HDR values into the limited gamut of a computer screen.</span></span>

<span data-ttu-id="0f6af-108">O mapeamento de Tom é a técnica usada pelo DirectX para mapear informações HDR em um intervalo mais limitado.</span><span class="sxs-lookup"><span data-stu-id="0f6af-108">Tone mapping is the technique used by DirectX for mapping HDR information into a more limited range.</span></span> <span data-ttu-id="0f6af-109">O mapeamento de Tom aplicado à renderização CGI pode melhorar drasticamente a quantidade de detalhes de iluminação renderizados, permitindo que os detalhes nas áreas mais escuras sejam vistos e fornecendo contraste em áreas que são tão brilhantes, eles aparecem gravados.</span><span class="sxs-lookup"><span data-stu-id="0f6af-109">Tone mapping applied to CGI rendering can dramatically improve the amount of lighting detail rendered, allowing details in the darkest areas to be seen, and providing contrast in areas that are so bright, they appear burned.</span></span> <span data-ttu-id="0f6af-110">As cenas resultantes são renderizadas com detalhes de iluminação muito mais visíveis.</span><span class="sxs-lookup"><span data-stu-id="0f6af-110">The resulting scenes render with far more visible lighting detail.</span></span>

<span data-ttu-id="0f6af-111">[HDRLighting exemplo](https://msdn.microsoft.com/library/Ee417769(v=VS.85).aspx) é um exemplo de SDK que demonstra a iluminação HDR.</span><span class="sxs-lookup"><span data-stu-id="0f6af-111">[HDRLighting Sample](https://msdn.microsoft.com/library/Ee417769(v=VS.85).aspx) is a SDK sample that demonstrates HDR lighting.</span></span>

## <a name="tone-mapping"></a><span data-ttu-id="0f6af-112">Mapeamento de Tom</span><span class="sxs-lookup"><span data-stu-id="0f6af-112">Tone Mapping</span></span>

<span data-ttu-id="0f6af-113">O mapeamento de Tom geralmente simula fenômenos ópticos que não podem ser causados pelo DR do monitor.</span><span class="sxs-lookup"><span data-stu-id="0f6af-113">Tone mapping generally simulates optical phenomena that cannot be caused by the DR of the monitor.</span></span> <span data-ttu-id="0f6af-114">Os exemplos disso são os flares ou a cair (que são basicamente Propriedades de lentes), a mudança azul que ocorre no olho humano em condições de pouca luz e outras adaptações que são resultado da bioquímica do olho.</span><span class="sxs-lookup"><span data-stu-id="0f6af-114">Examples of this are flares or blooming (which are mostly properties of lenses), the blue shift that happens in the human eye in low light conditions, and other adaptations that are a result of the biochemistry of the eye.</span></span> <span data-ttu-id="0f6af-115">Se a DR da exibição fosse grande o suficiente, o mapeamento de Tom não seria tão necessário, exceto para fornecer efeitos artísticos ou algumas das propriedades de uma lente da câmera ou um dispositivo acoplado de encargo (CCD).</span><span class="sxs-lookup"><span data-stu-id="0f6af-115">If the DR of the display were large enough, tone mapping would not be as neccessary, except for providing artistic effects or some of the properties of a camera lens or a charge coupled device (CCD).</span></span>

<span data-ttu-id="0f6af-116">O mapeamento de Tom divide o intervalo de valores de luminância em uma cena em um conjunto de zonas.</span><span class="sxs-lookup"><span data-stu-id="0f6af-116">Tone mapping divides the range of luminance values in a scene into a set of zones.</span></span> <span data-ttu-id="0f6af-117">Cada zona abrange um intervalo de valores de luminância.</span><span class="sxs-lookup"><span data-stu-id="0f6af-117">Each zone encompasses a range of luminance values.</span></span>

<span data-ttu-id="0f6af-118">O HDR usa os seguintes termos:</span><span class="sxs-lookup"><span data-stu-id="0f6af-118">HDR uses the following terms:</span></span>

-   <span data-ttu-id="0f6af-119">Intervalo de zona de valores de luminância</span><span class="sxs-lookup"><span data-stu-id="0f6af-119">Zone - range of luminance values</span></span>
-   <span data-ttu-id="0f6af-120">Cinza intermediária-região de brilho central da cena</span><span class="sxs-lookup"><span data-stu-id="0f6af-120">Middle gray - middle brightness region of the scene</span></span>
-   <span data-ttu-id="0f6af-121">Taxa de intervalo dinâmica da luminância de cena mais alta para a luminância de cena mais baixa</span><span class="sxs-lookup"><span data-stu-id="0f6af-121">Dynamic range - ratio of the highest scene luminance to the lowest scene luminance</span></span>
-   <span data-ttu-id="0f6af-122">Medição subjetiva de chave da iluminação de cena: isso varia de claro para moderado a escuro</span><span class="sxs-lookup"><span data-stu-id="0f6af-122">Key - subjective measurement of scene lighting: this varies from light to moderate to dark</span></span>

<span data-ttu-id="0f6af-123">Para calcular a luminância a partir de valores RGB, use:</span><span class="sxs-lookup"><span data-stu-id="0f6af-123">To calculate luminance from RGB values, use this:</span></span>


```
L = 0.27R + 0.67G + 0.06B;
```



<span data-ttu-id="0f6af-124">A luminância de média de log é uma aproximação útil para a chave de uma cena.</span><span class="sxs-lookup"><span data-stu-id="0f6af-124">The log-average luminance is a useful approximation for the key of a scene.</span></span> <span data-ttu-id="0f6af-125">Uma equação geral tem esta aparência:</span><span class="sxs-lookup"><span data-stu-id="0f6af-125">A general equation looks like this:</span></span>

<span data-ttu-id="0f6af-126">L<sub>w</sub> = exp \[ 1/N ( \[ log Sum (Delta + L<sub>w</sub>(x, y) \] ) \]</span><span class="sxs-lookup"><span data-stu-id="0f6af-126">L<sub>w</sub> = exp\[ 1 / N( sum\[ log( delta + L<sub>w</sub>( x, y ) ) \] ) \]</span></span>

<span data-ttu-id="0f6af-127">Em que:</span><span class="sxs-lookup"><span data-stu-id="0f6af-127">Where:</span></span>

-   <span data-ttu-id="0f6af-128">L<sub>w</sub> -log-luminância de média</span><span class="sxs-lookup"><span data-stu-id="0f6af-128">L<sub>w</sub> - log-average luminance</span></span>
-   <span data-ttu-id="0f6af-129">N-número de pixels na imagem</span><span class="sxs-lookup"><span data-stu-id="0f6af-129">N - number of pixels in the image</span></span>
-   <span data-ttu-id="0f6af-130">Delta-um pequeno fator para evitar problemas com pixels pretos</span><span class="sxs-lookup"><span data-stu-id="0f6af-130">delta - a small factor to avoid problems with black pixels</span></span>
-   <span data-ttu-id="0f6af-131">L<sub>w</sub>(x, y)-a luminância de espaço mundial para pixel (x, y)</span><span class="sxs-lookup"><span data-stu-id="0f6af-131">L<sub>w</sub>( x, y ) - the world space luminance for pixel ( x, y )</span></span>

<span data-ttu-id="0f6af-132">Para mapear isso para um valor de cinza médio, aqui está um operador de dimensionamento de luminescência:</span><span class="sxs-lookup"><span data-stu-id="0f6af-132">To map this to a middle-gray value, here is a luminance scaling operator:</span></span>

<span data-ttu-id="0f6af-133">L (x, y) = a \* L<sub>w</sub>(x, y)/L<sub>w</sub></span><span class="sxs-lookup"><span data-stu-id="0f6af-133">L( x, y ) = a \* L<sub>w</sub>( x, y ) / L<sub>w</sub></span></span>

<span data-ttu-id="0f6af-134">Em que:</span><span class="sxs-lookup"><span data-stu-id="0f6af-134">Where:</span></span>

-   <span data-ttu-id="0f6af-135">L (x, y)-luminância em escala para pixel (x, y)</span><span class="sxs-lookup"><span data-stu-id="0f6af-135">L( x, y ) - scaled luminance for pixel ( x, y )</span></span>
-   <span data-ttu-id="0f6af-136">um valor de chave de imagem depois de aplicar o dimensionamento</span><span class="sxs-lookup"><span data-stu-id="0f6af-136">a - image key value after applying the scaling</span></span>

<span data-ttu-id="0f6af-137">E, finalmente, aqui está um operador de mapeamento de Tom simples para compactar as altas luminosidades:</span><span class="sxs-lookup"><span data-stu-id="0f6af-137">And finally, here is a simple tone mapping operator for compressing the high luminances:</span></span>

<span data-ttu-id="0f6af-138">L<sub>d</sub>(x, y) = l (x, y)/(1 + L (x, y))</span><span class="sxs-lookup"><span data-stu-id="0f6af-138">L<sub>d</sub>( x, y ) = L( x, y ) / ( 1 + L( x, y ) )</span></span>

<span data-ttu-id="0f6af-139">Em que:</span><span class="sxs-lookup"><span data-stu-id="0f6af-139">Where:</span></span>

-   <span data-ttu-id="0f6af-140">L<sub>d</sub>(x, y)-luminância compactada e dimensionada para pixel (x, y)</span><span class="sxs-lookup"><span data-stu-id="0f6af-140">L<sub>d</sub>( x, y ) - compressed and scaled luminance for pixel ( x, y )</span></span>
-   <span data-ttu-id="0f6af-141">um valor de chave de imagem depois de aplicar o dimensionamento</span><span class="sxs-lookup"><span data-stu-id="0f6af-141">a - image key value after applying the scaling</span></span>

<span data-ttu-id="0f6af-142">Esse operador dimensiona altas luminâncias de 1/L e baixa luminância em 1.</span><span class="sxs-lookup"><span data-stu-id="0f6af-142">This operator scales high luminances by 1/L and low luminances by 1.</span></span> <span data-ttu-id="0f6af-143">Para obter mais detalhes, consulte o documento a seguir.</span><span class="sxs-lookup"><span data-stu-id="0f6af-143">For more details, see the following paper.</span></span>

<span data-ttu-id="0f6af-144">Reinhard, Erik, Mike Stark, Peter Shirley e James Ferwerda.</span><span class="sxs-lookup"><span data-stu-id="0f6af-144">Reinhard, Erik, Mike Stark, Peter Shirley, and James Ferwerda.</span></span> <span data-ttu-id="0f6af-145">["Reprodução de tons fotográficos para imagens digitais"](https://www.cs.utah.edu/~reinhard/cdrom/tonemap.pdf).</span><span class="sxs-lookup"><span data-stu-id="0f6af-145">["Photographic Tone Reproduction for Digital Images"](https://www.cs.utah.edu/~reinhard/cdrom/tonemap.pdf).</span></span> <span data-ttu-id="0f6af-146">Transações de ACM sobre gráficos (TOG), procedimentos de conferência anual de 29 em inglês (SIGGRAPH), pp. 267-276.</span><span class="sxs-lookup"><span data-stu-id="0f6af-146">ACM Transactions on Graphics (TOG), Proceedings of the 29th Annual Conference on Computer Graphics and Interactive Techniques (SIGGRAPH), pp. 267-276.</span></span> <span data-ttu-id="0f6af-147">Nova York, NY: ACM Press, 2002.</span><span class="sxs-lookup"><span data-stu-id="0f6af-147">New York, NY: ACM Press, 2002.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f6af-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f6af-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f6af-149">Tópicos avançados</span><span class="sxs-lookup"><span data-stu-id="0f6af-149">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 



