---
title: Mapear entre declarações D3D9 e D3D8
description: Esta tabela mapeia os membros de uma declaração D3DVERTEXELEMENT9 para uma declaração do Direct3D 8.
ms.assetid: da02b2cd-5221-4d37-97d5-840df91e39a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5c52bd804907f201916386ef5fa5776a32a046b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645662"
---
# <a name="map-between-d3d9-and-d3d8-declarations"></a><span data-ttu-id="eebdb-103">Mapear entre declarações D3D9 e D3D8</span><span class="sxs-lookup"><span data-stu-id="eebdb-103">Map between D3D9 and D3D8 declarations</span></span>

<span data-ttu-id="eebdb-104">Esta tabela mapeia os membros de uma declaração [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) para uma declaração do Direct3D 8.</span><span class="sxs-lookup"><span data-stu-id="eebdb-104">This table maps members of a [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) declaration to a Direct3D 8 declaration.</span></span>



| <span data-ttu-id="eebdb-105">Uso do Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="eebdb-105">Direct3D 9 Usage</span></span>           | <span data-ttu-id="eebdb-106">Índice de uso do Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="eebdb-106">Direct3D 9 Usage index</span></span> | <span data-ttu-id="eebdb-107">Direct3D 8</span><span class="sxs-lookup"><span data-stu-id="eebdb-107">Direct3D 8</span></span>            |
|----------------------------|------------------------|-----------------------|
| <span data-ttu-id="eebdb-108">\_Posição D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="eebdb-108">D3DDECLUSAGE\_POSITION</span></span>     | <span data-ttu-id="eebdb-109">0</span><span class="sxs-lookup"><span data-stu-id="eebdb-109">0</span></span>                      | <span data-ttu-id="eebdb-110">\_Posição D3DVSDE</span><span class="sxs-lookup"><span data-stu-id="eebdb-110">D3DVSDE\_POSITION</span></span>     |
| <span data-ttu-id="eebdb-111">\_Posição D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="eebdb-111">D3DDECLUSAGE\_POSITION</span></span>     | <span data-ttu-id="eebdb-112">1</span><span class="sxs-lookup"><span data-stu-id="eebdb-112">1</span></span>                      | <span data-ttu-id="eebdb-113">D3DVSDE \_ POSITION2</span><span class="sxs-lookup"><span data-stu-id="eebdb-113">D3DVSDE\_POSITION2</span></span>    |
| <span data-ttu-id="eebdb-114">D3DDECLUSAGE \_ normal</span><span class="sxs-lookup"><span data-stu-id="eebdb-114">D3DDECLUSAGE\_NORMAL</span></span>       | <span data-ttu-id="eebdb-115">0</span><span class="sxs-lookup"><span data-stu-id="eebdb-115">0</span></span>                      | <span data-ttu-id="eebdb-116">D3DVSDE \_ normal</span><span class="sxs-lookup"><span data-stu-id="eebdb-116">D3DVSDE\_NORMAL</span></span>       |
| <span data-ttu-id="eebdb-117">D3DDECLUSAGE \_ normal</span><span class="sxs-lookup"><span data-stu-id="eebdb-117">D3DDECLUSAGE\_NORMAL</span></span>       | <span data-ttu-id="eebdb-118">1</span><span class="sxs-lookup"><span data-stu-id="eebdb-118">1</span></span>                      | <span data-ttu-id="eebdb-119">D3DVSDE \_ NORMAL2</span><span class="sxs-lookup"><span data-stu-id="eebdb-119">D3DVSDE\_NORMAL2</span></span>      |
| <span data-ttu-id="eebdb-120">D3DDECLUSAGE \_ BLENDWEIGHT</span><span class="sxs-lookup"><span data-stu-id="eebdb-120">D3DDECLUSAGE\_BLENDWEIGHT</span></span>  | <span data-ttu-id="eebdb-121">0</span><span class="sxs-lookup"><span data-stu-id="eebdb-121">0</span></span>                      | <span data-ttu-id="eebdb-122">D3DVSDE \_ BLENDWEIGHT</span><span class="sxs-lookup"><span data-stu-id="eebdb-122">D3DVSDE\_BLENDWEIGHT</span></span>  |
| <span data-ttu-id="eebdb-123">D3DDECLUSAGE \_ BLENDINDICES</span><span class="sxs-lookup"><span data-stu-id="eebdb-123">D3DDECLUSAGE\_BLENDINDICES</span></span> | <span data-ttu-id="eebdb-124">0</span><span class="sxs-lookup"><span data-stu-id="eebdb-124">0</span></span>                      | <span data-ttu-id="eebdb-125">D3DVSDE \_ BLENDINDICES</span><span class="sxs-lookup"><span data-stu-id="eebdb-125">D3DVSDE\_BLENDINDICES</span></span> |
| <span data-ttu-id="eebdb-126">D3DDECLUSAGE \_ PSIZE</span><span class="sxs-lookup"><span data-stu-id="eebdb-126">D3DDECLUSAGE\_PSIZE</span></span>        | <span data-ttu-id="eebdb-127">0</span><span class="sxs-lookup"><span data-stu-id="eebdb-127">0</span></span>                      | <span data-ttu-id="eebdb-128">D3DVSDE \_ PSIZE</span><span class="sxs-lookup"><span data-stu-id="eebdb-128">D3DVSDE\_PSIZE</span></span>        |
| <span data-ttu-id="eebdb-129">\_Cor D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="eebdb-129">D3DDECLUSAGE\_COLOR</span></span>        | <span data-ttu-id="eebdb-130">0</span><span class="sxs-lookup"><span data-stu-id="eebdb-130">0</span></span>                      | <span data-ttu-id="eebdb-131">D3DVSDE \_ difuso</span><span class="sxs-lookup"><span data-stu-id="eebdb-131">D3DVSDE\_DIFFUSE</span></span>      |
| <span data-ttu-id="eebdb-132">\_Cor D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="eebdb-132">D3DDECLUSAGE\_COLOR</span></span>        | <span data-ttu-id="eebdb-133">1</span><span class="sxs-lookup"><span data-stu-id="eebdb-133">1</span></span>                      | <span data-ttu-id="eebdb-134">\_Especular D3DVSDE</span><span class="sxs-lookup"><span data-stu-id="eebdb-134">D3DVSDE\_SPECULAR</span></span>     |
| <span data-ttu-id="eebdb-135">D3DDECLUSAGE \_ TEXCOORD</span><span class="sxs-lookup"><span data-stu-id="eebdb-135">D3DDECLUSAGE\_TEXCOORD</span></span>     | <span data-ttu-id="eebdb-136">n</span><span class="sxs-lookup"><span data-stu-id="eebdb-136">n</span></span>                      | <span data-ttu-id="eebdb-137">D3DVSDE \_ TEXCOORDn</span><span class="sxs-lookup"><span data-stu-id="eebdb-137">D3DVSDE\_TEXCOORDn</span></span>    |



 

<span data-ttu-id="eebdb-138">Quando uma declaração é usada com o processamento de vértice de hardware em um driver do Direct3D 7, o tempo de execução do Direct3D converte-o em um FVF com as seguintes regras:</span><span class="sxs-lookup"><span data-stu-id="eebdb-138">When a declaration is used with hardware vertex processing on a Direct3D 7 driver, the Direct3D runtime converts it to a FVF with the following rules:</span></span>

-   <span data-ttu-id="eebdb-139">Somente o fluxo 0 deve ser usado (evidente na MaxStreams Cap).</span><span class="sxs-lookup"><span data-stu-id="eebdb-139">Only stream 0 should be used (evident from the MaxStreams cap).</span></span>
-   <span data-ttu-id="eebdb-140">A ordem dos elementos de vértice deve ser a mesma que a ordem de bits FVF.</span><span class="sxs-lookup"><span data-stu-id="eebdb-140">The order of vertex elements should be the same as order of FVF bits.</span></span>
-   <span data-ttu-id="eebdb-141">As lacunas nas coordenadas de textura não são permitidas.</span><span class="sxs-lookup"><span data-stu-id="eebdb-141">Gaps in texture coordinates are not allowed.</span></span>
-   <span data-ttu-id="eebdb-142">Qualquer elemento Vertex não descrito na tabela não pode ser convertido em um FVF válido para todos os drivers anteriores ao DirectX 8 e, portanto, não pode ser usado nesses drivers.</span><span class="sxs-lookup"><span data-stu-id="eebdb-142">Any vertex element not described the table cannot be converted into a valid FVF for all pre-DirectX 8 drivers and, hence, cannot be used on those drivers.</span></span>
-   <span data-ttu-id="eebdb-143">Somente D3DDECLTYPE \_ FLOAT2 é permitido para elementos de vértice com D3DDECLUSAGE \_ TEXCOORD se o dispositivo não definir uma das D3DPTEXTURECAPS \_ PROJETADAs ou D3DPTEXTURECAPSs CUBEMAP \_ .</span><span class="sxs-lookup"><span data-stu-id="eebdb-143">Only D3DDECLTYPE\_FLOAT2 is allowed for vertex elements with D3DDECLUSAGE\_TEXCOORD if device does not set either of the D3DPTEXTURECAPS\_PROJECTED or D3DPTEXTURECAPS\_CUBEMAP caps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eebdb-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="eebdb-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eebdb-145">Declaração de vértice</span><span class="sxs-lookup"><span data-stu-id="eebdb-145">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 



