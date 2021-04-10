---
description: Esta tabela mapeia os membros de uma declaração D3DVERTEXELEMENT9 para um código FVF.
ms.assetid: be4357b5-5b92-44ca-9100-ec9473930446
title: Mapeamento entre uma declaração de Direct3D e códigos de FVF (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4831af7b8c03ae4abd5ac2847351d2a6c921fb97
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087592"
---
# <a name="mapping-between-a-direct3d-declaration-and-fvf-codes-direct3d-9"></a><span data-ttu-id="bc334-103">Mapeamento entre uma declaração de Direct3D e códigos de FVF (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bc334-103">Mapping between a Direct3D Declaration and FVF Codes (Direct3D 9)</span></span>

<span data-ttu-id="bc334-104">Esta tabela mapeia os membros de uma declaração [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) para um código FVF.</span><span class="sxs-lookup"><span data-stu-id="bc334-104">This table maps members of a [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) declaration to a FVF code.</span></span>



| <span data-ttu-id="bc334-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="bc334-105">Data type</span></span>             | <span data-ttu-id="bc334-106">Uso</span><span class="sxs-lookup"><span data-stu-id="bc334-106">Usage</span></span>                      | <span data-ttu-id="bc334-107">Índice de uso</span><span class="sxs-lookup"><span data-stu-id="bc334-107">Usage index</span></span> | <span data-ttu-id="bc334-108">FVF</span><span class="sxs-lookup"><span data-stu-id="bc334-108">FVF</span></span>                       |
|-----------------------|----------------------------|-------------|---------------------------|
| <span data-ttu-id="bc334-109">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="bc334-109">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="bc334-110">\_Posição D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="bc334-110">D3DDECLUSAGE\_POSITION</span></span>     | <span data-ttu-id="bc334-111">0</span><span class="sxs-lookup"><span data-stu-id="bc334-111">0</span></span>           | <span data-ttu-id="bc334-112">D3DFVF \_ XYZ</span><span class="sxs-lookup"><span data-stu-id="bc334-112">D3DFVF\_XYZ</span></span>               |
| <span data-ttu-id="bc334-113">D3DDECLTYPE \_ FLOAT4</span><span class="sxs-lookup"><span data-stu-id="bc334-113">D3DDECLTYPE\_FLOAT4</span></span>   | <span data-ttu-id="bc334-114">Posição de D3DDECLUSAGE \_</span><span class="sxs-lookup"><span data-stu-id="bc334-114">D3DDECLUSAGE\_POSITIONT</span></span>    | <span data-ttu-id="bc334-115">0</span><span class="sxs-lookup"><span data-stu-id="bc334-115">0</span></span>           | <span data-ttu-id="bc334-116">D3DFVF \_ XYZRHW</span><span class="sxs-lookup"><span data-stu-id="bc334-116">D3DFVF\_XYZRHW</span></span>            |
| <span data-ttu-id="bc334-117">D3DDECLTYPE \_ floatn</span><span class="sxs-lookup"><span data-stu-id="bc334-117">D3DDECLTYPE\_FLOATn</span></span>   | <span data-ttu-id="bc334-118">D3DDECLUSAGE \_ BLENDWEIGHT</span><span class="sxs-lookup"><span data-stu-id="bc334-118">D3DDECLUSAGE\_BLENDWEIGHT</span></span>  | <span data-ttu-id="bc334-119">0</span><span class="sxs-lookup"><span data-stu-id="bc334-119">0</span></span>           | <span data-ttu-id="bc334-120">D3DFVF \_ XYZBn</span><span class="sxs-lookup"><span data-stu-id="bc334-120">D3DFVF\_XYZBn</span></span>             |
| <span data-ttu-id="bc334-121">D3DDECLTYPE \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="bc334-121">D3DDECLTYPE\_UBYTE4</span></span>   | <span data-ttu-id="bc334-122">D3DDECLUSAGE \_ BLENDINDICES</span><span class="sxs-lookup"><span data-stu-id="bc334-122">D3DDECLUSAGE\_BLENDINDICES</span></span> | <span data-ttu-id="bc334-123">0</span><span class="sxs-lookup"><span data-stu-id="bc334-123">0</span></span>           | <span data-ttu-id="bc334-124">D3DFVF \_ XYZB (nWeights + 1)</span><span class="sxs-lookup"><span data-stu-id="bc334-124">D3DFVF\_XYZB (nWeights+1)</span></span> |
| <span data-ttu-id="bc334-125">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="bc334-125">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="bc334-126">D3DDECLUSAGE \_ normal</span><span class="sxs-lookup"><span data-stu-id="bc334-126">D3DDECLUSAGE\_NORMAL</span></span>       | <span data-ttu-id="bc334-127">0</span><span class="sxs-lookup"><span data-stu-id="bc334-127">0</span></span>           | <span data-ttu-id="bc334-128">D3DFVF \_ normal</span><span class="sxs-lookup"><span data-stu-id="bc334-128">D3DFVF\_NORMAL</span></span>            |
| <span data-ttu-id="bc334-129">D3DDECLTYPE \_ FLOAT1</span><span class="sxs-lookup"><span data-stu-id="bc334-129">D3DDECLTYPE\_FLOAT1</span></span>   | <span data-ttu-id="bc334-130">D3DDECLUSAGE \_ PSIZE</span><span class="sxs-lookup"><span data-stu-id="bc334-130">D3DDECLUSAGE\_PSIZE</span></span>        | <span data-ttu-id="bc334-131">0</span><span class="sxs-lookup"><span data-stu-id="bc334-131">0</span></span>           | <span data-ttu-id="bc334-132">D3DFVF \_ PSIZE</span><span class="sxs-lookup"><span data-stu-id="bc334-132">D3DFVF\_PSIZE</span></span>             |
| <span data-ttu-id="bc334-133">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="bc334-133">D3DDECLTYPE\_D3DCOLOR</span></span> | <span data-ttu-id="bc334-134">\_Cor D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="bc334-134">D3DDECLUSAGE\_COLOR</span></span>        | <span data-ttu-id="bc334-135">0</span><span class="sxs-lookup"><span data-stu-id="bc334-135">0</span></span>           | <span data-ttu-id="bc334-136">D3DFVF \_ difuso</span><span class="sxs-lookup"><span data-stu-id="bc334-136">D3DFVF\_DIFFUSE</span></span>           |
| <span data-ttu-id="bc334-137">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="bc334-137">D3DDECLTYPE\_D3DCOLOR</span></span> | <span data-ttu-id="bc334-138">\_Cor D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="bc334-138">D3DDECLUSAGE\_COLOR</span></span>        | <span data-ttu-id="bc334-139">1</span><span class="sxs-lookup"><span data-stu-id="bc334-139">1</span></span>           | <span data-ttu-id="bc334-140">\_Especular D3DFVF</span><span class="sxs-lookup"><span data-stu-id="bc334-140">D3DFVF\_SPECULAR</span></span>          |
| <span data-ttu-id="bc334-141">D3DDECLTYPE \_ floatm</span><span class="sxs-lookup"><span data-stu-id="bc334-141">D3DDECLTYPE\_FLOATm</span></span>   | <span data-ttu-id="bc334-142">D3DDECLUSAGE \_ TEXCOORD</span><span class="sxs-lookup"><span data-stu-id="bc334-142">D3DDECLUSAGE\_TEXCOORD</span></span>     | <span data-ttu-id="bc334-143">n</span><span class="sxs-lookup"><span data-stu-id="bc334-143">n</span></span>           | <span data-ttu-id="bc334-144">D3DFVF \_ TEXCOORDSIZEm (n)</span><span class="sxs-lookup"><span data-stu-id="bc334-144">D3DFVF\_TEXCOORDSIZEm(n)</span></span>  |
| <span data-ttu-id="bc334-145">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="bc334-145">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="bc334-146">\_Posição D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="bc334-146">D3DDECLUSAGE\_POSITION</span></span>     | <span data-ttu-id="bc334-147">1</span><span class="sxs-lookup"><span data-stu-id="bc334-147">1</span></span>           | <span data-ttu-id="bc334-148">N/D</span><span class="sxs-lookup"><span data-stu-id="bc334-148">N/A</span></span>                       |
| <span data-ttu-id="bc334-149">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="bc334-149">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="bc334-150">D3DDECLUSAGE \_ normal</span><span class="sxs-lookup"><span data-stu-id="bc334-150">D3DDECLUSAGE\_NORMAL</span></span>       | <span data-ttu-id="bc334-151">1</span><span class="sxs-lookup"><span data-stu-id="bc334-151">1</span></span>           | <span data-ttu-id="bc334-152">N/D</span><span class="sxs-lookup"><span data-stu-id="bc334-152">N/A</span></span>                       |



 

## <a name="related-topics"></a><span data-ttu-id="bc334-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bc334-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc334-154">Declaração de vértice</span><span class="sxs-lookup"><span data-stu-id="bc334-154">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 



