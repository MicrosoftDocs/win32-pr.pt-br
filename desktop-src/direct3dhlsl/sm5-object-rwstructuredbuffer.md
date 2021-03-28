---
title: RWStructuredBuffer
description: Um buffer de leitura/gravação que pode usar um tipo T que é uma estrutura.
ms.assetid: 8dd93b81-135d-4f28-898f-38510dc39af1
keywords:
- RWStructuredBuffer HLSL
topic_type:
- apiref
api_name:
- RWStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f921ca795e761522828de14ede61894defe44f6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366194"
---
# <a name="rwstructuredbuffer"></a><span data-ttu-id="3a236-104">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="3a236-104">RWStructuredBuffer</span></span>

<span data-ttu-id="3a236-105">Um buffer de leitura/gravação que pode usar um tipo T que é uma estrutura.</span><span class="sxs-lookup"><span data-stu-id="3a236-105">A read/write buffer that can take a T type that is a structure.</span></span>



| <span data-ttu-id="3a236-106">Método</span><span class="sxs-lookup"><span data-stu-id="3a236-106">Method</span></span>                                                                     | <span data-ttu-id="3a236-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3a236-107">Description</span></span>                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="3a236-108">**DecrementCounter**</span><span class="sxs-lookup"><span data-stu-id="3a236-108">**DecrementCounter**</span></span>](sm5-object-rwstructuredbuffer-decrementcounter.md) | <span data-ttu-id="3a236-109">Decrementa o contador oculto do objeto.</span><span class="sxs-lookup"><span data-stu-id="3a236-109">Decrements the object's hidden counter.</span></span> |
| [<span data-ttu-id="3a236-110">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="3a236-110">**GetDimensions**</span></span>](sm5-object-rwstructuredbuffer-getdimensions.md)       | <span data-ttu-id="3a236-111">Obtém as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="3a236-111">Gets the resource dimensions.</span></span>           |
| [<span data-ttu-id="3a236-112">**IncrementCounter**</span><span class="sxs-lookup"><span data-stu-id="3a236-112">**IncrementCounter**</span></span>](sm5-object-rwstructuredbuffer-incrementcounter.md) | <span data-ttu-id="3a236-113">Incrementa o contador oculto do objeto.</span><span class="sxs-lookup"><span data-stu-id="3a236-113">Increments the object's hidden counter.</span></span> |
| [<span data-ttu-id="3a236-114">**Carregamento**</span><span class="sxs-lookup"><span data-stu-id="3a236-114">**Load**</span></span>](rwstructuredbuffer-load.md)                                    | <span data-ttu-id="3a236-115">Lê dados de buffer.</span><span class="sxs-lookup"><span data-stu-id="3a236-115">Reads buffer data.</span></span>                      |
| <span data-ttu-id="3a236-116">[**Operador\[\]**](sm5-object-rwstructuredbuffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="3a236-116">[**Operator\[\]**](sm5-object-rwstructuredbuffer-operatorindex.md)</span></span>        | <span data-ttu-id="3a236-117">Retorna uma variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="3a236-117">Returns a resource variable.</span></span>            |



 

<span data-ttu-id="3a236-118">Uma variável de recurso também pode ser passada para qualquer operação não ordenada ou interbloqueada.</span><span class="sxs-lookup"><span data-stu-id="3a236-118">A resource variable can also be passed into any unordered or interlocked operation.</span></span>

<span data-ttu-id="3a236-119">Os objetos RWStructuredBuffer podem ser prefixados com a classe de armazenamento **globallycoherent**.</span><span class="sxs-lookup"><span data-stu-id="3a236-119">RWStructuredBuffer objects can be prefixed with the storage class **globallycoherent**.</span></span> <span data-ttu-id="3a236-120">Essa classe de armazenamento causa barreiras de memória e sincronizações para liberar dados em toda a GPU, de modo que outros grupos possam ver gravações.</span><span class="sxs-lookup"><span data-stu-id="3a236-120">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="3a236-121">Sem esse especificador, uma barreira de memória ou sincronização só liberará um UAV dentro do grupo atual.</span><span class="sxs-lookup"><span data-stu-id="3a236-121">Without this specifier, a memory barrier or sync will only flush a UAV within the current group.</span></span>

<span data-ttu-id="3a236-122">O formato UAV associado a esse recurso precisa ser criado com o formato \_ desconhecido de formato dxgi \_ .</span><span class="sxs-lookup"><span data-stu-id="3a236-122">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="3a236-123">Para saber mais sobre [buffers estruturados](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), consulte o material de visão geral.</span><span class="sxs-lookup"><span data-stu-id="3a236-123">To find out more about [structured buffers](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), see the overview material.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="3a236-124">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="3a236-124">Minimum Shader Model</span></span>

<span data-ttu-id="3a236-125">Esse objeto tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="3a236-125">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="3a236-126">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="3a236-126">Shader Model</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="3a236-127">Com suporte</span><span class="sxs-lookup"><span data-stu-id="3a236-127">Supported</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="3a236-128">O [Shader Model 5](d3d11-graphics-reference-sm5.md) e os modelos de sombreador superiores modelo de sombreador [4](dx-graphics-hlsl-sm4.md) (disponível por meio da API do Direct3D 11 usando o nível de recurso 10,0 ou 10,1 ([**\_ \_ nível**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)de recurso do D3D \_ 10 \_ X) em dispositivos que dão suporte a sombreadores de computação.</span><span class="sxs-lookup"><span data-stu-id="3a236-128">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available through the Direct3D 11 API by using 10.0 or 10.1 feature level ([**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)\_10\_X) on devices that support compute shaders.</span></span> <span data-ttu-id="3a236-129">Para obter mais informações sobre o suporte de sombreador de computação em hardware de nível inferior, consulte [sombreadores de computação em hardware de nível inferior](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span><span class="sxs-lookup"><span data-stu-id="3a236-129">For more information about compute shader support on downlevel hardware, see [Compute Shaders on Downlevel Hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span></span><br/> | <span data-ttu-id="3a236-130">sim</span><span class="sxs-lookup"><span data-stu-id="3a236-130">yes</span></span>       |



 

<span data-ttu-id="3a236-131">Este objeto tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="3a236-131">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3a236-132">Vértice</span><span class="sxs-lookup"><span data-stu-id="3a236-132">Vertex</span></span> | <span data-ttu-id="3a236-133">Envoltória</span><span class="sxs-lookup"><span data-stu-id="3a236-133">Hull</span></span> | <span data-ttu-id="3a236-134">Domínio</span><span class="sxs-lookup"><span data-stu-id="3a236-134">Domain</span></span> | <span data-ttu-id="3a236-135">Geometria</span><span class="sxs-lookup"><span data-stu-id="3a236-135">Geometry</span></span> | <span data-ttu-id="3a236-136">16x16</span><span class="sxs-lookup"><span data-stu-id="3a236-136">Pixel</span></span> | <span data-ttu-id="3a236-137">Computação</span><span class="sxs-lookup"><span data-stu-id="3a236-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="3a236-138">x</span><span class="sxs-lookup"><span data-stu-id="3a236-138">x</span></span>     | <span data-ttu-id="3a236-139">x</span><span class="sxs-lookup"><span data-stu-id="3a236-139">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3a236-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a236-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a236-141">Objetos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="3a236-141">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

