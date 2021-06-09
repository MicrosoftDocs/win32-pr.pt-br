---
title: SV_GroupThreadID
description: Índices para os quais um thread individual dentro de um grupo de threads em que um sombreador de computação está sendo executado.
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
ms.openlocfilehash: d399008f1a9314ceb1fd4b1499b51340b499600b
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827025"
---
# <a name="sv_groupthreadid"></a><span data-ttu-id="e1cec-104">SV \_ GroupThreadID</span><span class="sxs-lookup"><span data-stu-id="e1cec-104">SV\_GroupThreadID</span></span>

<span data-ttu-id="e1cec-105">Índices para os quais um thread individual dentro de um grupo de threads em que um sombreador de computação está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="e1cec-105">Indices for which an individual thread within a thread group a compute shader is executing in.</span></span> <span data-ttu-id="e1cec-106">O SV GroupThreadID varia de acordo com o intervalo especificado para o \_ sombreador de computação no [atributo numthreads.](sm5-attributes-numthreads.md)</span><span class="sxs-lookup"><span data-stu-id="e1cec-106">SV\_GroupThreadID varies across the range specified for the compute shader in the [numthreads](sm5-attributes-numthreads.md) attribute.</span></span> <span data-ttu-id="e1cec-107">Por exemplo, se numthreads(3,2,1) tiver sido especificado valores possíveis para o valor de entrada GroupThreadID SV têm esse intervalo de valores \_ (0-2,0-1,0).</span><span class="sxs-lookup"><span data-stu-id="e1cec-107">For example if numthreads(3,2,1) was specified possible values for the SV\_GroupThreadID input value have this range of values (0-2,0-1,0).</span></span>

## <a name="type"></a><span data-ttu-id="e1cec-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="e1cec-108">Type</span></span>



| <span data-ttu-id="e1cec-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e1cec-109">Type</span></span>      |
|-------|
| <span data-ttu-id="e1cec-110">uint3</span><span class="sxs-lookup"><span data-stu-id="e1cec-110">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e1cec-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1cec-111">Remarks</span></span>

<span data-ttu-id="e1cec-112">Esse valor do sistema é opcional e está sempre dentro dos limites dos valores passados para o [atributo numthreads.](sm5-attributes-numthreads.md)</span><span class="sxs-lookup"><span data-stu-id="e1cec-112">This system value is optional, and is always within the bounds of the values passed into the [numthreads](sm5-attributes-numthreads.md) attribute.</span></span>

<span data-ttu-id="e1cec-113">A ilustração a seguir mostra a relação entre os parâmetros passados para [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), os valores especificados no [atributo numthreads,](sm5-attributes-numthreads.md) numthreads(10,8,3) e os valores que serão passados para o sombreador de computação para os valores do sistema relacionados ao thread ([SV \_ GroupIndex,](sv-groupindex.md)[SV \_ DispatchThreadID,](sv-dispatchthreadid.md)SV \_ GroupThreadID,[SV \_ GroupID](sv-groupid.md)).</span><span class="sxs-lookup"><span data-stu-id="e1cec-113">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),SV\_GroupThreadID,[SV\_GroupID](sv-groupid.md)).</span></span>

![ilustração da relação entre expedição, grupos de threads e threads](images/threadgroupids.png)

<span data-ttu-id="e1cec-115">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="e1cec-115">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="e1cec-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="e1cec-116">Vertex</span></span> | <span data-ttu-id="e1cec-117">Casco</span><span class="sxs-lookup"><span data-stu-id="e1cec-117">Hull</span></span> | <span data-ttu-id="e1cec-118">Domínio</span><span class="sxs-lookup"><span data-stu-id="e1cec-118">Domain</span></span> | <span data-ttu-id="e1cec-119">Geometry</span><span class="sxs-lookup"><span data-stu-id="e1cec-119">Geometry</span></span> | <span data-ttu-id="e1cec-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="e1cec-120">Pixel</span></span> | <span data-ttu-id="e1cec-121">Computação</span><span class="sxs-lookup"><span data-stu-id="e1cec-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="e1cec-122">x</span><span class="sxs-lookup"><span data-stu-id="e1cec-122">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e1cec-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1cec-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1cec-124">Semântica</span><span class="sxs-lookup"><span data-stu-id="e1cec-124">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="e1cec-125">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e1cec-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
