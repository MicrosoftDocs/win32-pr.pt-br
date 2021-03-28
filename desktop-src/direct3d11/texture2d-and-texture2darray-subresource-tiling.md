---
title: Sub-recursos lado a lado de Texture2D e Texture2DArray
description: Estas tabelas mostram como sub-recursos Texture2D e Texture2DArray são agrupados lado a lado.
ms.assetid: 3CFA384D-2C49-4BB2-9A92-FC45B1A499B5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a7ded22fcb7e7e476a701c7db3063dfae33fda
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366341"
---
# <a name="texture2d-and-texture2darray-subresource-tiling"></a><span data-ttu-id="c8409-103">Sub-recursos lado a lado de Texture2D e Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="c8409-103">Texture2D and Texture2DArray subresource tiling</span></span>

<span data-ttu-id="c8409-104">Essas tabelas mostram como os subrecursos [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) são colocados ao lado.</span><span class="sxs-lookup"><span data-stu-id="c8409-104">These tables show how [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) subresources are tiled.</span></span> <span data-ttu-id="c8409-105">Os valores nestas tabelas não contam a compactação MIP final.</span><span class="sxs-lookup"><span data-stu-id="c8409-105">The values in these tables don't count tail mip packing.</span></span>

<span data-ttu-id="c8409-106">Esta tabela mostra como os sub-recursos [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) com contagens multisample de 1 são agrupados lado a lado.</span><span class="sxs-lookup"><span data-stu-id="c8409-106">This table shows how [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) subresources with multisample counts of 1 are tiled.</span></span>



| <span data-ttu-id="c8409-107">Bits/Pixel (1 amostra/pixel)</span><span class="sxs-lookup"><span data-stu-id="c8409-107">Bits/Pixel (1 sample/pixel)</span></span> | <span data-ttu-id="c8409-108">Dimensões do bloco (Pixels, LxA)</span><span class="sxs-lookup"><span data-stu-id="c8409-108">Tile Dimensions (Pixels, WxH)</span></span> |
|-----------------------------|-------------------------------|
| <span data-ttu-id="c8409-109">8</span><span class="sxs-lookup"><span data-stu-id="c8409-109">8</span></span>                           | <span data-ttu-id="c8409-110">256x256</span><span class="sxs-lookup"><span data-stu-id="c8409-110">256x256</span></span>                       |
| <span data-ttu-id="c8409-111">16</span><span class="sxs-lookup"><span data-stu-id="c8409-111">16</span></span>                          | <span data-ttu-id="c8409-112">256x128</span><span class="sxs-lookup"><span data-stu-id="c8409-112">256x128</span></span>                       |
| <span data-ttu-id="c8409-113">32</span><span class="sxs-lookup"><span data-stu-id="c8409-113">32</span></span>                          | <span data-ttu-id="c8409-114">128x128</span><span class="sxs-lookup"><span data-stu-id="c8409-114">128x128</span></span>                       |
| <span data-ttu-id="c8409-115">64</span><span class="sxs-lookup"><span data-stu-id="c8409-115">64</span></span>                          | <span data-ttu-id="c8409-116">128x64</span><span class="sxs-lookup"><span data-stu-id="c8409-116">128x64</span></span>                        |
| <span data-ttu-id="c8409-117">128</span><span class="sxs-lookup"><span data-stu-id="c8409-117">128</span></span>                         | <span data-ttu-id="c8409-118">64x64</span><span class="sxs-lookup"><span data-stu-id="c8409-118">64x64</span></span>                         |
| <span data-ttu-id="c8409-119">BC1,4</span><span class="sxs-lookup"><span data-stu-id="c8409-119">BC1,4</span></span>                       | <span data-ttu-id="c8409-120">512x256</span><span class="sxs-lookup"><span data-stu-id="c8409-120">512x256</span></span>                       |
| <span data-ttu-id="c8409-121">BC2,3,5,6,7</span><span class="sxs-lookup"><span data-stu-id="c8409-121">BC2,3,5,6,7</span></span>                 | <span data-ttu-id="c8409-122">256x256</span><span class="sxs-lookup"><span data-stu-id="c8409-122">256x256</span></span>                       |



 

<span data-ttu-id="c8409-123">As contagens de bits de formato não suportadas com os recursos do lado do suporte são formatos de 96 BPP, formatos de vídeo, \_ formato dxgi \_ \_ UNORM, \_ formato dxgi \_ R8G8 \_ B8G8 UNORM e \_ \_ formato dxgi \_ R8R8 \_ \_ G8B8 UNORM.</span><span class="sxs-lookup"><span data-stu-id="c8409-123">Format bit counts not supported with tiled resources are 96 bpp formats, video formats, DXGI\_FORMAT\_R1\_UNORM, DXGI\_FORMAT\_R8G8\_B8G8\_UNORM, and DXGI\_FORMAT\_R8R8\_G8B8\_UNORM.</span></span>

<span data-ttu-id="c8409-124">Esta tabela mostra como os sub-recursos [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) com várias contagens multisample são agrupados lado a lado.</span><span class="sxs-lookup"><span data-stu-id="c8409-124">This table shows how [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) subresources with various multisample counts are tiled.</span></span>



| <span data-ttu-id="c8409-125">Contagem de multiamostras</span><span class="sxs-lookup"><span data-stu-id="c8409-125">Multisample Count</span></span>           | <span data-ttu-id="c8409-126">Dividir dimensões de bloco acima por (WxH)</span><span class="sxs-lookup"><span data-stu-id="c8409-126">Divide Tile Dimensions Above by (WxH)</span></span> |
|-----------------------------|-------------------------------|
| <span data-ttu-id="c8409-127">1</span><span class="sxs-lookup"><span data-stu-id="c8409-127">1</span></span>                           | <span data-ttu-id="c8409-128">1x1</span><span class="sxs-lookup"><span data-stu-id="c8409-128">1x1</span></span>                           |
| <span data-ttu-id="c8409-129">2</span><span class="sxs-lookup"><span data-stu-id="c8409-129">2</span></span>                           | <span data-ttu-id="c8409-130">2x1</span><span class="sxs-lookup"><span data-stu-id="c8409-130">2x1</span></span>                           |
| <span data-ttu-id="c8409-131">4</span><span class="sxs-lookup"><span data-stu-id="c8409-131">4</span></span>                           | <span data-ttu-id="c8409-132">2x2</span><span class="sxs-lookup"><span data-stu-id="c8409-132">2x2</span></span>                           |
| <span data-ttu-id="c8409-133">8</span><span class="sxs-lookup"><span data-stu-id="c8409-133">8</span></span>                           | <span data-ttu-id="c8409-134">4x2</span><span class="sxs-lookup"><span data-stu-id="c8409-134">4x2</span></span>                           |
| <span data-ttu-id="c8409-135">16</span><span class="sxs-lookup"><span data-stu-id="c8409-135">16</span></span>                          | <span data-ttu-id="c8409-136">4x4</span><span class="sxs-lookup"><span data-stu-id="c8409-136">4x4</span></span>                           |



 

<span data-ttu-id="c8409-137">Somente as contagens de exemplo 1 e 4 são necessárias (e permitidas) para serem suportadas com recursos de lado.</span><span class="sxs-lookup"><span data-stu-id="c8409-137">Only sample counts 1 and 4 are required (and allowed) to be supported with tiled resources.</span></span> <span data-ttu-id="c8409-138">No momento, os recursos de lado não dão suporte a 2, 8 e 16, embora sejam mostrados.</span><span class="sxs-lookup"><span data-stu-id="c8409-138">Tiled resources don't currently support 2, 8, and 16 even though they are shown.</span></span>

<span data-ttu-id="c8409-139">As implementações podem optar por oferecer suporte ao modo de 2, 8 e/ou 16 amostras de anti-aliasing multiamostrador (MSAA) para recursos que não são de lado do ladrilho, mesmo que o recurso de lado não ofereça suporte a eles.</span><span class="sxs-lookup"><span data-stu-id="c8409-139">Implementations can choose to support 2, 8, and/or 16 sample multisample antialiasing (MSAA) mode for non-tiled resources even though tiled resource don't support them.</span></span>

<span data-ttu-id="c8409-140">Os recursos com sublado com contagens de exemplo maiores que 1 não podem usar formatos de 128 BPP.</span><span class="sxs-lookup"><span data-stu-id="c8409-140">Tiled resources with sample counts larger than 1 can't use 128 bpp formats.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8409-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c8409-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8409-142">Como a área de um recurso do lado do ladrilho é colocada</span><span class="sxs-lookup"><span data-stu-id="c8409-142">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 