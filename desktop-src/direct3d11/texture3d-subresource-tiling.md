---
title: Sub-recursos lado a lado de Texture3D
description: Esta tabela mostra como os sub-recursos de Texture3D são colocados lado a lado.
ms.assetid: D0CDD652-AE8E-40A4-BA05-E743B0757AFA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7a668f499a2f6d3911716d5d7bad60df4cd9e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988714"
---
# <a name="texture3d-subresource-tiling"></a><span data-ttu-id="35d0a-103">Sub-recursos lado a lado de Texture3D</span><span class="sxs-lookup"><span data-stu-id="35d0a-103">Texture3D subresource tiling</span></span>

<span data-ttu-id="35d0a-104">Esta tabela mostra como os [**SubTexture3Ds**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) de subrecursos são enlados.</span><span class="sxs-lookup"><span data-stu-id="35d0a-104">This table shows how [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) subresources are tiled.</span></span> <span data-ttu-id="35d0a-105">Os valores nesta tabela não contam a compactação MIP final.</span><span class="sxs-lookup"><span data-stu-id="35d0a-105">The values in this table don't count tail mip packing.</span></span>

<span data-ttu-id="35d0a-106">Esta tabela pega o agrupamento lado a lado do [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e divide cada uma das dimensões x/y por 4 e adiciona 16 camadas de profundidade.</span><span class="sxs-lookup"><span data-stu-id="35d0a-106">This table takes the [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) tiling and divides the x/y dimensions by 4 each and adds 16 layers of depth.</span></span> <span data-ttu-id="35d0a-107">Todos os blocos do primeiro plano (plano 2D de blocos definindo as 16 primeiras camadas de profundidade) aparecem antes dos planos subsequentes.</span><span class="sxs-lookup"><span data-stu-id="35d0a-107">All the tiles for the first plane (2D plane of tiles defining the first 16 layers of depth) appear before the subsequent planes.</span></span>

> [!Note]  
> <span data-ttu-id="35d0a-108">O suporte do [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) em recursos de blocos gráficos não é exposto na implementação inicial dos recursos do lado do quadrado, mas as formas de bloco desejadas são listadas aqui porque o suporte pode ser considerado em uma versão futura.</span><span class="sxs-lookup"><span data-stu-id="35d0a-108">[**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) support in tiled resources isn't exposed in the initial implementation of tiled resources, but the desired tile shapes are listed here because support might be consideration in a future release.</span></span>

 



| <span data-ttu-id="35d0a-109">Bits/Pixel (1 amostra/pixel)</span><span class="sxs-lookup"><span data-stu-id="35d0a-109">Bits/Pixel (1 sample/pixel)</span></span> | <span data-ttu-id="35d0a-110">Dimensões do bloco (Pixels, LxAxP)</span><span class="sxs-lookup"><span data-stu-id="35d0a-110">Tile Dimensions (Pixels, WxHxD)</span></span> |
|-----------------------------|---------------------------------|
| <span data-ttu-id="35d0a-111">8</span><span class="sxs-lookup"><span data-stu-id="35d0a-111">8</span></span>                           | <span data-ttu-id="35d0a-112">64x32x32</span><span class="sxs-lookup"><span data-stu-id="35d0a-112">64x32x32</span></span>                        |
| <span data-ttu-id="35d0a-113">16</span><span class="sxs-lookup"><span data-stu-id="35d0a-113">16</span></span>                          | <span data-ttu-id="35d0a-114">32x32x32</span><span class="sxs-lookup"><span data-stu-id="35d0a-114">32x32x32</span></span>                        |
| <span data-ttu-id="35d0a-115">32</span><span class="sxs-lookup"><span data-stu-id="35d0a-115">32</span></span>                          | <span data-ttu-id="35d0a-116">32x32x16</span><span class="sxs-lookup"><span data-stu-id="35d0a-116">32x32x16</span></span>                        |
| <span data-ttu-id="35d0a-117">64</span><span class="sxs-lookup"><span data-stu-id="35d0a-117">64</span></span>                          | <span data-ttu-id="35d0a-118">32x16x16</span><span class="sxs-lookup"><span data-stu-id="35d0a-118">32x16x16</span></span>                        |
| <span data-ttu-id="35d0a-119">128</span><span class="sxs-lookup"><span data-stu-id="35d0a-119">128</span></span>                         | <span data-ttu-id="35d0a-120">16x16x16</span><span class="sxs-lookup"><span data-stu-id="35d0a-120">16x16x16</span></span>                        |
| <span data-ttu-id="35d0a-121">BC1,4</span><span class="sxs-lookup"><span data-stu-id="35d0a-121">BC1,4</span></span>                       | <span data-ttu-id="35d0a-122">128x64x16</span><span class="sxs-lookup"><span data-stu-id="35d0a-122">128x64x16</span></span>                       |
| <span data-ttu-id="35d0a-123">BC2,3,5,6,7</span><span class="sxs-lookup"><span data-stu-id="35d0a-123">BC2,3,5,6,7</span></span>                 | <span data-ttu-id="35d0a-124">64x64x16</span><span class="sxs-lookup"><span data-stu-id="35d0a-124">64x64x16</span></span>                        |



 

<span data-ttu-id="35d0a-125">As contagens de bits de formato não suportadas com os recursos do lado do suporte são formatos de 96 BPP, formatos de vídeo, \_ formato dxgi \_ \_ UNORM, \_ formato dxgi \_ R8G8 \_ B8G8 UNORM e \_ \_ formato dxgi \_ R8R8 \_ \_ G8B8 UNORM.</span><span class="sxs-lookup"><span data-stu-id="35d0a-125">Format bit counts not supported with tiled resources are 96 bpp formats, video formats, DXGI\_FORMAT\_R1\_UNORM, DXGI\_FORMAT\_R8G8\_B8G8\_UNORM, and DXGI\_FORMAT\_R8R8\_G8B8\_UNORM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="35d0a-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="35d0a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35d0a-127">Como a área de um recurso do lado do ladrilho é colocada</span><span class="sxs-lookup"><span data-stu-id="35d0a-127">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 