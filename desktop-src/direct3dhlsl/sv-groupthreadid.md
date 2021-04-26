---
title: SV_GroupThreadID
description: Índices para os quais um thread individual em um grupo de threads em que um sombreador de computação está sendo executado.
ms.assetid: be944592-c4ea-43c9-88bc-98a9a190a437
keywords:
- SV_GroupThreadID HLSL
topic_type:
- apiref
api_name:
- SV_GroupThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d36e5639b017dfa94e0f3c9f84d6725f6b6a283
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996983"
---
# <a name="sv_groupthreadid"></a><span data-ttu-id="10579-104">\_GROUPTHREADID VA</span><span class="sxs-lookup"><span data-stu-id="10579-104">SV\_GroupThreadID</span></span>

<span data-ttu-id="10579-105">Índices para os quais um thread individual em um grupo de threads em que um sombreador de computação está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="10579-105">Indices for which an individual thread within a thread group a compute shader is executing in.</span></span> <span data-ttu-id="10579-106">A \_ GroupThreadID de VA varia entre o intervalo especificado para o sombreador de computação no atributo [numthreads](sm5-attributes-numthreads.md) .</span><span class="sxs-lookup"><span data-stu-id="10579-106">SV\_GroupThreadID varies across the range specified for the compute shader in the [numthreads](sm5-attributes-numthreads.md) attribute.</span></span> <span data-ttu-id="10579-107">Por exemplo, se numthreads (3, 2, 1) tiver sido especificado, os valores possíveis para o \_ valor de entrada GroupThreadID de VA terão esse intervalo de valores (0-2, 0-1, 0).</span><span class="sxs-lookup"><span data-stu-id="10579-107">For example if numthreads(3,2,1) was specified possible values for the SV\_GroupThreadID input value have this range of values (0-2,0-1,0).</span></span>

## <a name="type"></a><span data-ttu-id="10579-108">Digite</span><span class="sxs-lookup"><span data-stu-id="10579-108">Type</span></span>



|       |
|-------|
| <span data-ttu-id="10579-109">Digite</span><span class="sxs-lookup"><span data-stu-id="10579-109">Type</span></span>  |
| <span data-ttu-id="10579-110">uint3</span><span class="sxs-lookup"><span data-stu-id="10579-110">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="10579-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="10579-111">Remarks</span></span>

<span data-ttu-id="10579-112">Esse valor do sistema é opcional e está sempre dentro dos limites dos valores passados para o atributo [numthreads](sm5-attributes-numthreads.md) .</span><span class="sxs-lookup"><span data-stu-id="10579-112">This system value is optional, and is always within the bounds of the values passed into the [numthreads](sm5-attributes-numthreads.md) attribute.</span></span>

<span data-ttu-id="10579-113">A ilustração a seguir mostra a relação entre os parâmetros passados para [**expedição**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), expedição (5, 3, 2), os valores especificados no atributo [numthreads](sm5-attributes-numthreads.md) , numthreads (10, 8, 3) e valores que serão passados para o sombreador de computação para os valores do sistema relacionados ao thread ([VA \_ GroupIndex](sv-groupindex.md),[VA \_ DispatchThreadID](sv-dispatchthreadid.md), VA \_ GroupThreadID,[SV \_ GroupId](sv-groupid.md)).</span><span class="sxs-lookup"><span data-stu-id="10579-113">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),SV\_GroupThreadID,[SV\_GroupID](sv-groupid.md)).</span></span>

![ilustração da relação entre expedição, grupos de threads e threads](images/threadgroupids.png)

<span data-ttu-id="10579-115">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="10579-115">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="10579-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="10579-116">Vertex</span></span> | <span data-ttu-id="10579-117">Envoltória</span><span class="sxs-lookup"><span data-stu-id="10579-117">Hull</span></span> | <span data-ttu-id="10579-118">Domain</span><span class="sxs-lookup"><span data-stu-id="10579-118">Domain</span></span> | <span data-ttu-id="10579-119">Geometria</span><span class="sxs-lookup"><span data-stu-id="10579-119">Geometry</span></span> | <span data-ttu-id="10579-120">16x16</span><span class="sxs-lookup"><span data-stu-id="10579-120">Pixel</span></span> | <span data-ttu-id="10579-121">Computação</span><span class="sxs-lookup"><span data-stu-id="10579-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="10579-122">x</span><span class="sxs-lookup"><span data-stu-id="10579-122">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="10579-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="10579-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10579-124">Semântica</span><span class="sxs-lookup"><span data-stu-id="10579-124">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="10579-125">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="10579-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
