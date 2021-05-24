---
description: Sistemas de coordenadas para Direct3D 10 são definidos para pixels e texels.
ms.assetid: c8c269e7-6e2a-4b5d-847c-6779e276b9af
title: Sistemas de coordenadas (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3da846ae4b989f6d8cb4741f9df8f7228e8970
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335460"
---
# <a name="coordinate-systems-direct3d-10"></a><span data-ttu-id="f769d-103">Sistemas de coordenadas (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="f769d-103">Coordinate Systems (Direct3D 10)</span></span>

<span data-ttu-id="f769d-104">Sistemas de coordenadas para Direct3D 10 são definidos para pixels e texels.</span><span class="sxs-lookup"><span data-stu-id="f769d-104">Coordinate systems for Direct3D 10 are defined for pixels and texels.</span></span>



<span data-ttu-id="f769d-105">Diferenças entre o Direct3D 9 e o Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="f769d-105">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="f769d-106">O Direct3D 10 define o canto superior esquerdo do pixel superior esquerdo como a origem de um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="f769d-106">Direct3D 10 defines the upper-left corner of the upper-left pixel as the origin of a render target.</span></span>
- <span data-ttu-id="f769d-107">O Direct3D 9 define o centro do pixel superior esquerdo como a origem de um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="f769d-107">Direct3D 9 defines the center of the upper-left pixel as the origin of a render target.</span></span>



 

[<span data-ttu-id="f769d-108">Sistema de coordenadas de pixel</span><span class="sxs-lookup"><span data-stu-id="f769d-108">Pixel Coordinate System</span></span>](#pixel-coordinate-system)
- [<span data-ttu-id="f769d-109">Sistema de coordenadas de pixel para Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="f769d-109">Pixel Coordinate System for Direct3D 9</span></span>](#pixel-coordinate-system-for-direct3d-9)

[<span data-ttu-id="f769d-110">Sistema de coordenadas Texel</span><span class="sxs-lookup"><span data-stu-id="f769d-110">Texel Coordinate System</span></span>](#texel-coordinate-system)
- [<span data-ttu-id="f769d-111">Sistema de coordenadas Texel</span><span class="sxs-lookup"><span data-stu-id="f769d-111">Texel Coordinate System</span></span>](#texel-coordinate-system)

[<span data-ttu-id="f769d-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f769d-112">Related topics</span></span>](#related-topics)

## <a name="pixel-coordinate-system"></a><span data-ttu-id="f769d-113">Sistema de coordenadas de pixels</span><span class="sxs-lookup"><span data-stu-id="f769d-113">Pixel Coordinate System</span></span>

<span data-ttu-id="f769d-114">O sistema de coordenadas de pixel no Direct3D 10 define a origem de um destino de renderização no canto superior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="f769d-114">The pixel coordinate system in Direct3D 10 defines the origin of a render target at the upper-left corner.</span></span> <span data-ttu-id="f769d-115">conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="f769d-115">as shown in the following diagram.</span></span> <span data-ttu-id="f769d-116">Os centros de pixels são separados por (0,5f;0,5f) de locais de números inteiros.</span><span class="sxs-lookup"><span data-stu-id="f769d-116">Pixel centers are offset by (0.5f,0.5f) from integer locations.</span></span>

![diagrama do sistema de coordenadas de pixels no direct3d 10](images/d3d10-coordspix10.png)

### <a name="pixel-coordinate-system-for-direct3d-9"></a><span data-ttu-id="f769d-118">Sistema de coordenadas de pixel para Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="f769d-118">Pixel Coordinate System for Direct3D 9</span></span>

<span data-ttu-id="f769d-119">Para referência, aqui está o sistema de coordenadas de pixel para Direct3D 9, que definiu a origem ou um destino de renderização como o centro do pixel superior esquerdo, (0,5,0,5) do canto superior esquerdo, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="f769d-119">For reference, here is the pixel coordinate system for Direct3D 9, which defined the origin or a render target as the center of the upper-left pixel, (0.5,0.5) away from the upper left corner, as shown in the following diagram.</span></span> <span data-ttu-id="f769d-120">No Direct3D 9, os centros de pixels estão em locais inteiros.</span><span class="sxs-lookup"><span data-stu-id="f769d-120">In Direct3D 9, pixel centers are at integer locations.</span></span>

![diagrama do sistema de coordenadas de pixel no Direct3d 9](images/d3d10-coordspix9.png)

## <a name="texel-coordinate-system"></a><span data-ttu-id="f769d-122">Sistema de coordenadas de texel</span><span class="sxs-lookup"><span data-stu-id="f769d-122">Texel Coordinate System</span></span>

<span data-ttu-id="f769d-123">O sistema de coordenadas de texel é originado no canto superior esquerdo da textura, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="f769d-123">The texel coordinate system has its origin at the top-left corner of the texture, as shown in the following diagram.</span></span> <span data-ttu-id="f769d-124">Isso torna a renderização de texturas alinhadas à tela trivial (no Direct3D 10), pois o sistema de coordenadas de pixel é alinhado com o sistema de coordenadas texel.</span><span class="sxs-lookup"><span data-stu-id="f769d-124">This makes rendering screen-aligned textures trivial (in Direct3D 10), as the pixel coordinate system is aligned with the texel coordinate system.</span></span>

![diagrama do sistema de coordenadas de texel](images/d3d10-coordstex10.png)

### <a name="texel-coordinate-system"></a><span data-ttu-id="f769d-126">Sistema de coordenadas de texel</span><span class="sxs-lookup"><span data-stu-id="f769d-126">Texel Coordinate System</span></span>

<span data-ttu-id="f769d-127">As coordenadas de textura são representadas por um número normalizado ou dimensionado; cada coordenada de textura é mapeada de acordo com um texel específico da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="f769d-127">Texture coordinates are represented with either a normalized or a scaled number; each texture coordinate is mapped to a specific texel as follows:</span></span>

<span data-ttu-id="f769d-128">Para uma coordenada normalizada:</span><span class="sxs-lookup"><span data-stu-id="f769d-128">For a normalized coordinate:</span></span>

-   <span data-ttu-id="f769d-129">Amostragem de ponto: Texel \# = floor(U \* Width)</span><span class="sxs-lookup"><span data-stu-id="f769d-129">Point sampling: Texel \# = floor(U \* Width)</span></span>
-   <span data-ttu-id="f769d-130">Amostragem linear: Left Texel \# = floor(U \* Width), Right Texel \# = Left Texel + \# 1</span><span class="sxs-lookup"><span data-stu-id="f769d-130">Linear sampling: Left Texel \# = floor(U \* Width), Right Texel \# = Left Texel \# + 1</span></span>

<span data-ttu-id="f769d-131">Para uma coordenada dimensionada:</span><span class="sxs-lookup"><span data-stu-id="f769d-131">For a scaled coordinate:</span></span>

-   <span data-ttu-id="f769d-132">Amostragem de ponto: Texel \# = Floor (U)</span><span class="sxs-lookup"><span data-stu-id="f769d-132">Point sampling: Texel \# = floor(U)</span></span>
-   <span data-ttu-id="f769d-133">Amostragem linear: esquerda Texel \# = Floor (U-0,5), direita Texel \# = Left Texel \# + 1</span><span class="sxs-lookup"><span data-stu-id="f769d-133">Linear sampling: Left Texel \# = floor(U - 0.5), Right Texel \# = Left Texel \# + 1</span></span>

<span data-ttu-id="f769d-134">Onde a largura é a largura da textura (em texels).</span><span class="sxs-lookup"><span data-stu-id="f769d-134">Where the width, is the width of the texture (in texels).</span></span>

<span data-ttu-id="f769d-135">O encapsulamento do endereço da textura ocorre após o cálculo da localização de texel.</span><span class="sxs-lookup"><span data-stu-id="f769d-135">Texture address wrapping occurs after the texel location is computed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f769d-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f769d-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f769d-137">Recursos (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="f769d-137">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




