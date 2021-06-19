---
title: Intrínsecos de valor do sistema HLSL de raytracing do Direct3D 12
description: Exiba links para artigos que descrevem funções intrínsecas de valor do sistema HLSL (linguagem de sombreamento de alto nível) que dão suporte ao pipeline do Direct3D 12 raytracing.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2790cf5df42f64071db3ca51a35e58ee9afcd5
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396431"
---
# <a name="direct3d-12-raytracing-hlsl-system-value-intrinsics"></a><span data-ttu-id="886d1-103">Intrínsecos de valor do sistema HLSL de raytracing do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="886d1-103">Direct3D 12 raytracing HLSL system value intrinsics</span></span>

<span data-ttu-id="886d1-104">Os valores do sistema são recuperados usando funções intrínsecas especiais, em vez de incluir parâmetros com semântica especial na assinatura da função de sombreador.</span><span class="sxs-lookup"><span data-stu-id="886d1-104">System values are retrieved by using special intrinsic functions, rather than including parameters with special semantics in your shader function signature.</span></span> 

## <a name="in-this-section"></a><span data-ttu-id="886d1-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="886d1-105">In this section</span></span>

### <a name="ray-dispatch-system-values"></a><span data-ttu-id="886d1-106">Valores do sistema de expedição de Ray</span><span class="sxs-lookup"><span data-stu-id="886d1-106">Ray dispatch system values</span></span>

| <span data-ttu-id="886d1-107">Tópico</span><span class="sxs-lookup"><span data-stu-id="886d1-107">Topic</span></span> | <span data-ttu-id="886d1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="886d1-108">Description</span></span> |
|-|-|
| [<span data-ttu-id="886d1-109">**DispatchRaysIndex**</span><span class="sxs-lookup"><span data-stu-id="886d1-109">**DispatchRaysIndex**</span></span>](dispatchraysindex.md) | <span data-ttu-id="886d1-110">Obtém o local x e y atual dentro da largura e altura obtidas com o valor do sistema **DispatchRaysDimensions** intrínseco.</span><span class="sxs-lookup"><span data-stu-id="886d1-110">Gets the current x and y location within the width and height obtained with the **DispatchRaysDimensions** system value intrinsic.</span></span> |
| [<span data-ttu-id="886d1-111">**DispatchRaysDimensions**</span><span class="sxs-lookup"><span data-stu-id="886d1-111">**DispatchRaysDimensions**</span></span>](dispatchraysdimensions.md) | <span data-ttu-id="886d1-112">A largura, a altura e os valores de profundidade da estrutura desc de raios de expedição de D3D12 especificadas na chamada de **DispatchRays** de origem. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="886d1-112">The width, height and depth values from the **D3D12\_DISPATCH\_RAYS\_DESC** structure specified in the originating **DispatchRays** call.</span></span> |

### <a name="ray-system-values"></a><span data-ttu-id="886d1-113">Valores do sistema Ray</span><span class="sxs-lookup"><span data-stu-id="886d1-113">Ray system values</span></span>

| <span data-ttu-id="886d1-114">Tópico</span><span class="sxs-lookup"><span data-stu-id="886d1-114">Topic</span></span> | <span data-ttu-id="886d1-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="886d1-115">Description</span></span> |
|-|-|
| [<span data-ttu-id="886d1-116">**WorldRayOrigin**</span><span class="sxs-lookup"><span data-stu-id="886d1-116">**WorldRayOrigin**</span></span>](worldrayorigin.md) | <span data-ttu-id="886d1-117">A origem de espaço Mundial do raio atual.</span><span class="sxs-lookup"><span data-stu-id="886d1-117">The world-space origin of the current ray.</span></span> |
| [<span data-ttu-id="886d1-118">**WorldRayDirection**</span><span class="sxs-lookup"><span data-stu-id="886d1-118">**WorldRayDirection**</span></span>](worldraydirection.md) | <span data-ttu-id="886d1-119">A direção de espaço mundial para o raio atual.</span><span class="sxs-lookup"><span data-stu-id="886d1-119">The world-space direction for the current ray.</span></span> |
| [<span data-ttu-id="886d1-120">**RayTMin**</span><span class="sxs-lookup"><span data-stu-id="886d1-120">**RayTMin**</span></span>](raytmin.md) | <span data-ttu-id="886d1-121">Um float que representa o ponto de partida paramétrica atual para o raio.</span><span class="sxs-lookup"><span data-stu-id="886d1-121">A float representing the current parametric starting point for the ray.</span></span> |
| [<span data-ttu-id="886d1-122">**RayTCurrent**</span><span class="sxs-lookup"><span data-stu-id="886d1-122">**RayTCurrent**</span></span>](raytcurrent.md) | <span data-ttu-id="886d1-123">Um float que representa o ponto final paramétrica atual para o raio.</span><span class="sxs-lookup"><span data-stu-id="886d1-123">A float representing the current parametric ending point for the ray.</span></span>  |
| [<span data-ttu-id="886d1-124">**RayFlags**</span><span class="sxs-lookup"><span data-stu-id="886d1-124">**RayFlags**</span></span>](rayflags.md) | <span data-ttu-id="886d1-125">Um inteiro sem sinal contendo os sinalizadores de **ray_flag** atuais.</span><span class="sxs-lookup"><span data-stu-id="886d1-125">An unsigned integer containing the current **ray_flag** flags.</span></span> |

### <a name="primitiveobject-space-system-values"></a><span data-ttu-id="886d1-126">Valores do sistema de espaço primitivo/objeto</span><span class="sxs-lookup"><span data-stu-id="886d1-126">Primitive/object space system values</span></span>

| <span data-ttu-id="886d1-127">Tópico</span><span class="sxs-lookup"><span data-stu-id="886d1-127">Topic</span></span> | <span data-ttu-id="886d1-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="886d1-128">Description</span></span> |
|-|-|
| [<span data-ttu-id="886d1-129">**InstanceIndex**</span><span class="sxs-lookup"><span data-stu-id="886d1-129">**InstanceIndex**</span></span>](instanceindex.md) | <span data-ttu-id="886d1-130">O índice gerado automaticamente da instância atual na estrutura de aceleração raytracing de nível superior.</span><span class="sxs-lookup"><span data-stu-id="886d1-130">The autogenerated index of the current instance in the top-level raytracing acceleration structure.</span></span> |
| [<span data-ttu-id="886d1-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="886d1-131">**InstanceID**</span></span>](instanceid.md) | <span data-ttu-id="886d1-132">O identificador fornecido pelo usuário para a instância na instância da estrutura de aceleração de nível inferior dentro da estrutura de nível superior.</span><span class="sxs-lookup"><span data-stu-id="886d1-132">The user-provided identifier for the instance on the bottom-level acceleration structure instance within the top-level structure.</span></span> |
| [<span data-ttu-id="886d1-133">**PrimitiveIndex**</span><span class="sxs-lookup"><span data-stu-id="886d1-133">**PrimitiveIndex**</span></span>](primitiveindex.md) | <span data-ttu-id="886d1-134">O índice gerado automaticamente do primitivo dentro da geometria dentro da instância de estrutura de aceleração de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="886d1-134">The autogenerated index of the primitive within the geometry inside the bottom-level acceleration structure instance.</span></span> |
| [<span data-ttu-id="886d1-135">**ObjectRayOrigin**</span><span class="sxs-lookup"><span data-stu-id="886d1-135">**ObjectRayOrigin**</span></span>](objectrayorigin.md) | <span data-ttu-id="886d1-136">A origem do espaço de objeto para o raio atual.</span><span class="sxs-lookup"><span data-stu-id="886d1-136">The object-space origin for the current ray.</span></span> |
| [<span data-ttu-id="886d1-137">**ObjectRayDirection**</span><span class="sxs-lookup"><span data-stu-id="886d1-137">**ObjectRayDirection**</span></span>](objectraydirection.md) | <span data-ttu-id="886d1-138">A direção do espaço de objeto para o raio atual.</span><span class="sxs-lookup"><span data-stu-id="886d1-138">The object-space direction for the current ray.</span></span> |
| [<span data-ttu-id="886d1-139">**ObjectToWorld3x4**</span><span class="sxs-lookup"><span data-stu-id="886d1-139">**ObjectToWorld3x4**</span></span>](objecttoworld3x4.md) | <span data-ttu-id="886d1-140">Uma matriz para transformar de espaço de objeto em espaço mundial.</span><span class="sxs-lookup"><span data-stu-id="886d1-140">A matrix for transforming from object-space to world-space.</span></span> |
| [<span data-ttu-id="886d1-141">**ObjectToWorld4x3**</span><span class="sxs-lookup"><span data-stu-id="886d1-141">**ObjectToWorld4x3**</span></span>](objecttoworld4x3.md) | <span data-ttu-id="886d1-142">Uma matriz para transformar de espaço de objeto em espaço mundial.</span><span class="sxs-lookup"><span data-stu-id="886d1-142">A matrix for transforming from object-space to world-space.</span></span> |
| [<span data-ttu-id="886d1-143">**WorldToObject3x4**</span><span class="sxs-lookup"><span data-stu-id="886d1-143">**WorldToObject3x4**</span></span>](worldtoobject3x4.md) | <span data-ttu-id="886d1-144">Uma matriz para transformar de espaço mundial em espaço de objeto</span><span class="sxs-lookup"><span data-stu-id="886d1-144">A matrix for transforming from world-space to object-space</span></span> |
| [<span data-ttu-id="886d1-145">**WorldToObject4x3**</span><span class="sxs-lookup"><span data-stu-id="886d1-145">**WorldToObject4x3**</span></span>](worldtoobject4x3.md) | <span data-ttu-id="886d1-146">Uma matriz para transformar de espaço mundial em espaço de objeto</span><span class="sxs-lookup"><span data-stu-id="886d1-146">A matrix for transforming from world-space to object-space</span></span> |
### <a name="hit-specific-system-values"></a><span data-ttu-id="886d1-147">Valores de sistema específicos de um clique</span><span class="sxs-lookup"><span data-stu-id="886d1-147">Hit-specific system values</span></span>

| <span data-ttu-id="886d1-148">Tópico</span><span class="sxs-lookup"><span data-stu-id="886d1-148">Topic</span></span> | <span data-ttu-id="886d1-149">Descrição</span><span class="sxs-lookup"><span data-stu-id="886d1-149">Description</span></span> |
|-|-|
| [<span data-ttu-id="886d1-150">**HitKind**</span><span class="sxs-lookup"><span data-stu-id="886d1-150">**HitKind**</span></span>](hitkind.md) | <span data-ttu-id="886d1-151">Retorna o valor passado como o parâmetro **HitKind** para [**ReportHit**](reporthit-function.md).</span><span class="sxs-lookup"><span data-stu-id="886d1-151">Returns the value passed as the **HitKind** parameter to [**ReportHit**](reporthit-function.md).</span></span> |

## <a name="related-topics"></a><span data-ttu-id="886d1-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="886d1-152">Related topics</span></span>

* [<span data-ttu-id="886d1-153">Referência principal</span><span class="sxs-lookup"><span data-stu-id="886d1-153">Core Reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="886d1-154">Referência do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="886d1-154">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
