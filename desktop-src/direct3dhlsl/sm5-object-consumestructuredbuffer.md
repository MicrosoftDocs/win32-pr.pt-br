---
title: ConsumeStructuredBuffer
description: Um buffer de entrada que aparece como um fluxo do qual o sombreador pode receber valores. Somente os buffers estruturados podem usar tipos T que são estruturas.
ms.assetid: 373bdd97-6186-4bce-99bf-738a153234f6
keywords:
- ConsumeStructuredBuffer HLSL
topic_type:
- apiref
api_name:
- ConsumeStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af7a670713dc5b63839702a04a632dda61ebfa43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988712"
---
# <a name="consumestructuredbuffer"></a><span data-ttu-id="9214c-105">ConsumeStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="9214c-105">ConsumeStructuredBuffer</span></span>

<span data-ttu-id="9214c-106">Um buffer de entrada que aparece como um fluxo do qual o sombreador pode receber valores.</span><span class="sxs-lookup"><span data-stu-id="9214c-106">An input buffer that appears as a stream the shader may pull values from.</span></span> <span data-ttu-id="9214c-107">Somente os buffers estruturados podem usar tipos T que são estruturas.</span><span class="sxs-lookup"><span data-stu-id="9214c-107">Only structured buffers can take T types that are structures.</span></span>



| <span data-ttu-id="9214c-108">Método</span><span class="sxs-lookup"><span data-stu-id="9214c-108">Method</span></span>                                                                    | <span data-ttu-id="9214c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="9214c-109">Description</span></span>                                 |
|---------------------------------------------------------------------------|---------------------------------------------|
| [<span data-ttu-id="9214c-110">**Consumir**</span><span class="sxs-lookup"><span data-stu-id="9214c-110">**Consume**</span></span>](sm5-object-consumestructuredbuffer-consume.md)             | <span data-ttu-id="9214c-111">Remove um valor do final do buffer.</span><span class="sxs-lookup"><span data-stu-id="9214c-111">Removes a value from the end of the buffer.</span></span> |
| [<span data-ttu-id="9214c-112">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="9214c-112">**GetDimensions**</span></span>](sm5-object-consumestructuredbuffer-getdimensions.md) | <span data-ttu-id="9214c-113">Obtém as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="9214c-113">Gets the resource dimensions.</span></span>               |



 

<span data-ttu-id="9214c-114">O formato UAV associado a esse recurso precisa ser criado com o formato \_ desconhecido de formato dxgi \_ .</span><span class="sxs-lookup"><span data-stu-id="9214c-114">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="9214c-115">O UAV associado a esse recurso deve ter sido criado com o [**D3D11 \_ buffer \_ UAV \_ sinalizador \_ Append**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span><span class="sxs-lookup"><span data-stu-id="9214c-115">The UAV bound to this resource must have been created with [**D3D11\_BUFFER\_UAV\_FLAG\_APPEND**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span></span>

<span data-ttu-id="9214c-116">Para obter mais informações sobre o consumo de buffers estruturados, consulte as duas seções: [acrescentar e consumir](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) buffer e [buffer estruturado](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span><span class="sxs-lookup"><span data-stu-id="9214c-116">For more info about consume structured buffers, see both sections: [append and consume buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) and [structured buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="9214c-117">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="9214c-117">Minimum Shader Model</span></span>

<span data-ttu-id="9214c-118">Esse objeto tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="9214c-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="9214c-119">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="9214c-119">Shader Model</span></span>                                                                | <span data-ttu-id="9214c-120">Com suporte</span><span class="sxs-lookup"><span data-stu-id="9214c-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="9214c-121">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="9214c-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="9214c-122">sim</span><span class="sxs-lookup"><span data-stu-id="9214c-122">yes</span></span>       |



 

<span data-ttu-id="9214c-123">Este objeto tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="9214c-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9214c-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="9214c-124">Vertex</span></span> | <span data-ttu-id="9214c-125">Envoltória</span><span class="sxs-lookup"><span data-stu-id="9214c-125">Hull</span></span> | <span data-ttu-id="9214c-126">Domínio</span><span class="sxs-lookup"><span data-stu-id="9214c-126">Domain</span></span> | <span data-ttu-id="9214c-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="9214c-127">Geometry</span></span> | <span data-ttu-id="9214c-128">16x16</span><span class="sxs-lookup"><span data-stu-id="9214c-128">Pixel</span></span> | <span data-ttu-id="9214c-129">Computação</span><span class="sxs-lookup"><span data-stu-id="9214c-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="9214c-130">x</span><span class="sxs-lookup"><span data-stu-id="9214c-130">x</span></span>     | <span data-ttu-id="9214c-131">x</span><span class="sxs-lookup"><span data-stu-id="9214c-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9214c-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="9214c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9214c-133">Objetos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="9214c-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 