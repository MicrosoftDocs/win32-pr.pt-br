---
title: SV_DispatchThreadID
description: Índices para os quais thread e grupo de threads combinados um sombreador de computação está sendo executado.
ms.assetid: bad697f6-26d9-47cd-93e5-127621a161e8
keywords:
- SV_DispatchThreadID HLSL
topic_type:
- apiref
api_name:
- SV_DispatchThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d55fcf7e291c561ecb51dd32dfac135c563974c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104566437"
---
# <a name="sv_dispatchthreadid"></a><span data-ttu-id="88650-104">\_DISPATCHTHREADID VA</span><span class="sxs-lookup"><span data-stu-id="88650-104">SV\_DispatchThreadID</span></span>

<span data-ttu-id="88650-105">Índices para os quais thread e grupo de threads combinados um sombreador de computação está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="88650-105">Indices for which combined thread and thread group a compute shader is executing in.</span></span> <span data-ttu-id="88650-106">\_DISPATCHTHREADID VA é a soma de VA \_ GroupId \* numthreads e GroupThreadID.</span><span class="sxs-lookup"><span data-stu-id="88650-106">SV\_DispatchThreadID is the sum of SV\_GroupID \* numthreads and GroupThreadID.</span></span> <span data-ttu-id="88650-107">Varia em todo o intervalo especificado em [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) e [numthreads](sm5-attributes-numthreads.md).</span><span class="sxs-lookup"><span data-stu-id="88650-107">It varies across the range specified in [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) and [numthreads](sm5-attributes-numthreads.md).</span></span> <span data-ttu-id="88650-108">Por exemplo, se a expedição (2, 2, 2) for chamada em um sombreador de computação com numthreads (3, 3, 3) \_ , DISPATCHTHREADID VA terá um intervalo de 0.. 5 para cada dimensão.</span><span class="sxs-lookup"><span data-stu-id="88650-108">For example if Dispatch(2,2,2) is called on a compute shader with numthreads(3,3,3) SV\_DispatchThreadID will have a range of 0..5 for each dimension.</span></span>

## <a name="type"></a><span data-ttu-id="88650-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="88650-109">Type</span></span>



|       |
|-------|
| <span data-ttu-id="88650-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="88650-110">Type</span></span>  |
| <span data-ttu-id="88650-111">uint3</span><span class="sxs-lookup"><span data-stu-id="88650-111">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="88650-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="88650-112">Remarks</span></span>

<span data-ttu-id="88650-113">Esse valor de sistema é opcional.</span><span class="sxs-lookup"><span data-stu-id="88650-113">This system value is optional.</span></span>

<span data-ttu-id="88650-114">A ilustração a seguir mostra a relação entre os parâmetros passados para [**expedição**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), expedição (5, 3, 2), os valores especificados no atributo [numthreads](sm5-attributes-numthreads.md) , numthreads (10, 8, 3) e valores que serão passados para o sombreador de computação para os valores do sistema relacionados ao thread ([VA \_ GroupIndex](sv-groupindex.md), VA \_ DispatchThreadID,[VA \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupId](sv-groupid.md)).</span><span class="sxs-lookup"><span data-stu-id="88650-114">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),SV\_DispatchThreadID,[SV\_GroupThreadID](sv-groupthreadid.md),[SV\_GroupID](sv-groupid.md)).</span></span>

![ilustração da relação entre expedição, grupos de threads e threads](images/threadgroupids.png)

<span data-ttu-id="88650-116">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="88650-116">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="88650-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="88650-117">Vertex</span></span> | <span data-ttu-id="88650-118">Envoltória</span><span class="sxs-lookup"><span data-stu-id="88650-118">Hull</span></span> | <span data-ttu-id="88650-119">Domínio</span><span class="sxs-lookup"><span data-stu-id="88650-119">Domain</span></span> | <span data-ttu-id="88650-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="88650-120">Geometry</span></span> | <span data-ttu-id="88650-121">16x16</span><span class="sxs-lookup"><span data-stu-id="88650-121">Pixel</span></span> | <span data-ttu-id="88650-122">Computação</span><span class="sxs-lookup"><span data-stu-id="88650-122">Compute</span></span> |
|        |      |        |          |       | <span data-ttu-id="88650-123">x</span><span class="sxs-lookup"><span data-stu-id="88650-123">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="88650-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="88650-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88650-125">Semântica</span><span class="sxs-lookup"><span data-stu-id="88650-125">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="88650-126">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="88650-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 