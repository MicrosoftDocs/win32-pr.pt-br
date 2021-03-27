---
title: AppendStructuredBuffer
description: Buffer de saída que aparece como um fluxo ao qual o sombreador pode acrescentar. Somente os buffers estruturados podem usar tipos T que são estruturas.
ms.assetid: 377b0358-0f9d-4021-9140-19c3d1bfed38
keywords:
- AppendStructuredBuffer HLSL
topic_type:
- apiref
api_name:
- AppendStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c140052c861c8da3df6378fc3bc49816998c130
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641321"
---
# <a name="appendstructuredbuffer"></a><span data-ttu-id="e691d-105">AppendStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="e691d-105">AppendStructuredBuffer</span></span>

<span data-ttu-id="e691d-106">Buffer de saída que aparece como um fluxo ao qual o sombreador pode acrescentar.</span><span class="sxs-lookup"><span data-stu-id="e691d-106">Output buffer that appears as a stream the shader may append to.</span></span> <span data-ttu-id="e691d-107">Somente os buffers estruturados podem usar tipos T que são estruturas.</span><span class="sxs-lookup"><span data-stu-id="e691d-107">Only structured buffers can take T types that are structures.</span></span>



| <span data-ttu-id="e691d-108">Método</span><span class="sxs-lookup"><span data-stu-id="e691d-108">Method</span></span>                                                                   | <span data-ttu-id="e691d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e691d-109">Description</span></span>                               |
|--------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="e691d-110">**Acrescentar**</span><span class="sxs-lookup"><span data-stu-id="e691d-110">**Append**</span></span>](sm5-object-appendstructuredbuffer-append.md)               | <span data-ttu-id="e691d-111">Anexa um valor ao final do buffer.</span><span class="sxs-lookup"><span data-stu-id="e691d-111">Appends a value to the end of the buffer.</span></span> |
| [<span data-ttu-id="e691d-112">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="e691d-112">**GetDimensions**</span></span>](sm5-object-appendstructuredbuffer-getdimensions.md) | <span data-ttu-id="e691d-113">Obtém as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="e691d-113">Gets the resource dimensions.</span></span>             |



 

<span data-ttu-id="e691d-114">O formato UAV associado a esse recurso precisa ser criado com o formato \_ desconhecido de formato dxgi \_ .</span><span class="sxs-lookup"><span data-stu-id="e691d-114">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="e691d-115">O UAV associado a esse recurso deve ter sido criado com o [**D3D11 \_ buffer \_ UAV \_ sinalizador \_ Append**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span><span class="sxs-lookup"><span data-stu-id="e691d-115">The UAV bound to this resource must have been created with [**D3D11\_BUFFER\_UAV\_FLAG\_APPEND**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span></span>

<span data-ttu-id="e691d-116">Para obter mais informações sobre um buffer estruturado de acréscimo, consulte as duas seções: [acrescentar e consumir](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) buffer e [buffer estruturado](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span><span class="sxs-lookup"><span data-stu-id="e691d-116">For more information about an append structured buffer, see both sections: [append and consume buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) and [structured buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="e691d-117">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="e691d-117">Minimum Shader Model</span></span>

<span data-ttu-id="e691d-118">Esse objeto tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e691d-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="e691d-119">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="e691d-119">Shader Model</span></span>                                                                | <span data-ttu-id="e691d-120">Com suporte</span><span class="sxs-lookup"><span data-stu-id="e691d-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="e691d-121">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="e691d-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="e691d-122">sim</span><span class="sxs-lookup"><span data-stu-id="e691d-122">yes</span></span>       |



 

<span data-ttu-id="e691d-123">Este objeto tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="e691d-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e691d-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="e691d-124">Vertex</span></span> | <span data-ttu-id="e691d-125">Envoltória</span><span class="sxs-lookup"><span data-stu-id="e691d-125">Hull</span></span> | <span data-ttu-id="e691d-126">Domínio</span><span class="sxs-lookup"><span data-stu-id="e691d-126">Domain</span></span> | <span data-ttu-id="e691d-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="e691d-127">Geometry</span></span> | <span data-ttu-id="e691d-128">16x16</span><span class="sxs-lookup"><span data-stu-id="e691d-128">Pixel</span></span> | <span data-ttu-id="e691d-129">Computação</span><span class="sxs-lookup"><span data-stu-id="e691d-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="e691d-130">x</span><span class="sxs-lookup"><span data-stu-id="e691d-130">x</span></span>     | <span data-ttu-id="e691d-131">x</span><span class="sxs-lookup"><span data-stu-id="e691d-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e691d-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="e691d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e691d-133">Objetos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="e691d-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 