---
title: ByteAddressBuffer
description: ByteAddressBuffer
ms.assetid: 809b5ee8-0a25-402e-8cf2-f5e7a8094ec6
keywords:
- ByteAddressBuffer HLSL
topic_type:
- apiref
api_name:
- ByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 03e89f56522d941db4447b33b55cbedc7c73303f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967219"
---
# <a name="byteaddressbuffer"></a><span data-ttu-id="9c546-104">ByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="9c546-104">ByteAddressBuffer</span></span>

<span data-ttu-id="9c546-105">Um buffer somente leitura que é indexado em bytes.</span><span class="sxs-lookup"><span data-stu-id="9c546-105">A read-only buffer that is indexed in bytes.</span></span>



| <span data-ttu-id="9c546-106">Método</span><span class="sxs-lookup"><span data-stu-id="9c546-106">Method</span></span>                                                              | <span data-ttu-id="9c546-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9c546-107">Description</span></span>                   |
|---------------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="9c546-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="9c546-108">**GetDimensions**</span></span>](sm5-object-byteaddressbuffer-getdimensions.md) | <span data-ttu-id="9c546-109">Obtém as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="9c546-109">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="9c546-110">**Carregamento**</span><span class="sxs-lookup"><span data-stu-id="9c546-110">**Load**</span></span>](byteaddressbuffer-load.md)                              | <span data-ttu-id="9c546-111">Obtém um valor.</span><span class="sxs-lookup"><span data-stu-id="9c546-111">Gets one value.</span></span>               |
| [<span data-ttu-id="9c546-112">**Load2**</span><span class="sxs-lookup"><span data-stu-id="9c546-112">**Load2**</span></span>](byteaddressbuffer-load2.md)                            | <span data-ttu-id="9c546-113">Obtém dois valores.</span><span class="sxs-lookup"><span data-stu-id="9c546-113">Gets two values.</span></span>              |
| [<span data-ttu-id="9c546-114">**Load3**</span><span class="sxs-lookup"><span data-stu-id="9c546-114">**Load3**</span></span>](byteaddressbuffer-load3.md)                            | <span data-ttu-id="9c546-115">Obtém três valores.</span><span class="sxs-lookup"><span data-stu-id="9c546-115">Gets three values.</span></span>            |
| [<span data-ttu-id="9c546-116">**Load4**</span><span class="sxs-lookup"><span data-stu-id="9c546-116">**Load4**</span></span>](byteaddressbuffer-load4.md)                            | <span data-ttu-id="9c546-117">Obtém quatro valores.</span><span class="sxs-lookup"><span data-stu-id="9c546-117">Gets four values.</span></span>             |



 

<span data-ttu-id="9c546-118">Você pode usar o tipo de objeto **ByteAddressBuffer** ao trabalhar com buffers brutos.</span><span class="sxs-lookup"><span data-stu-id="9c546-118">You can use the **ByteAddressBuffer** object type when you work with raw buffers.</span></span> <span data-ttu-id="9c546-119">Para obter mais informações sobre a exibição bruta de buffers, consulte [exibições brutas de buffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).</span><span class="sxs-lookup"><span data-stu-id="9c546-119">For more info about raw viewing of buffers, see [Raw Views of Buffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="9c546-120">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="9c546-120">Minimum Shader Model</span></span>

<span data-ttu-id="9c546-121">Esse objeto tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="9c546-121">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="9c546-122">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="9c546-122">Shader Model</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="9c546-123">Com suporte</span><span class="sxs-lookup"><span data-stu-id="9c546-123">Supported</span></span> |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="9c546-124">O [Shader Model 5](d3d11-graphics-reference-sm5.md) e os modelos de sombreador superiores modelo de sombreador [4](dx-graphics-hlsl-sm4.md) (disponível por meio da API do Direct3D 11 usando o nível de recurso 10,0 ou 10,1 ([**\_ \_ nível**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)de recurso do D3D \_ 10 \_ X) em dispositivos que dão suporte a sombreadores de computação.</span><span class="sxs-lookup"><span data-stu-id="9c546-124">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available through the Direct3D 11 API by using 10.0 or 10.1 feature level ([**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)\_10\_X) on devices that support compute shaders.</span></span> <span data-ttu-id="9c546-125">Para obter mais informações sobre o suporte de sombreador de computação em hardware de nível inferior, consulte [sombreadores de computação em hardware de nível inferior](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span><span class="sxs-lookup"><span data-stu-id="9c546-125">For more info about compute shader support on downlevel hardware, see [Compute Shaders on Downlevel Hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span></span><br/> | <span data-ttu-id="9c546-126">sim</span><span class="sxs-lookup"><span data-stu-id="9c546-126">yes</span></span>       |



 

<span data-ttu-id="9c546-127">Este objeto tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="9c546-127">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9c546-128">Vértice</span><span class="sxs-lookup"><span data-stu-id="9c546-128">Vertex</span></span> | <span data-ttu-id="9c546-129">Envoltória</span><span class="sxs-lookup"><span data-stu-id="9c546-129">Hull</span></span> | <span data-ttu-id="9c546-130">Domínio</span><span class="sxs-lookup"><span data-stu-id="9c546-130">Domain</span></span> | <span data-ttu-id="9c546-131">Geometria</span><span class="sxs-lookup"><span data-stu-id="9c546-131">Geometry</span></span> | <span data-ttu-id="9c546-132">16x16</span><span class="sxs-lookup"><span data-stu-id="9c546-132">Pixel</span></span> | <span data-ttu-id="9c546-133">Computação</span><span class="sxs-lookup"><span data-stu-id="9c546-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9c546-134">x</span><span class="sxs-lookup"><span data-stu-id="9c546-134">x</span></span>      | <span data-ttu-id="9c546-135">x</span><span class="sxs-lookup"><span data-stu-id="9c546-135">x</span></span>    | <span data-ttu-id="9c546-136">x</span><span class="sxs-lookup"><span data-stu-id="9c546-136">x</span></span>      | <span data-ttu-id="9c546-137">x</span><span class="sxs-lookup"><span data-stu-id="9c546-137">x</span></span>        | <span data-ttu-id="9c546-138">x</span><span class="sxs-lookup"><span data-stu-id="9c546-138">x</span></span>     | <span data-ttu-id="9c546-139">x</span><span class="sxs-lookup"><span data-stu-id="9c546-139">x</span></span>       |



 

<span data-ttu-id="9c546-140">Para obter mais informações sobre um buffer de endereço de byte, consulte o [tipo de recurso de byte endereçável](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span><span class="sxs-lookup"><span data-stu-id="9c546-140">For more info about a byte address buffer, see the [byte addressable resource type](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span></span>

<span data-ttu-id="9c546-141">O Shader Model 5 também implementa um [buffer de endereço de byte de leitura/gravação](sm5-object-rwbyteaddressbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="9c546-141">Shader Model 5 also implements a [read-write byte address buffer](sm5-object-rwbyteaddressbuffer.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9c546-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c546-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c546-143">Objetos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="9c546-143">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

