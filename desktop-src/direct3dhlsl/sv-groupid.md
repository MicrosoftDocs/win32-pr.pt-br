---
title: SV_GroupID
description: Índices para os quais um sombreador de computação está sendo executado por um grupo de threads.
ms.assetid: 1b90ca74-a2b6-4a5f-aa4a-1ec879360593
keywords:
- SV_GroupID HLSL
topic_type:
- apiref
api_name:
- SV_GroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab94cef0a9a33f23947e11b93a5487c65eee3890
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827035"
---
# <a name="sv_groupid"></a><span data-ttu-id="ab2c8-104">GroupID de SV \_</span><span class="sxs-lookup"><span data-stu-id="ab2c8-104">SV\_GroupID</span></span>

<span data-ttu-id="ab2c8-105">Índices para os quais um sombreador de computação está sendo executado por um grupo de threads.</span><span class="sxs-lookup"><span data-stu-id="ab2c8-105">Indices for which thread group a compute shader is executing in.</span></span> <span data-ttu-id="ab2c8-106">Os índices são para todo o grupo e não para um thread individual.</span><span class="sxs-lookup"><span data-stu-id="ab2c8-106">The indices are to the whole group and not an individual thread.</span></span> <span data-ttu-id="ab2c8-107">Os valores possíveis variam entre o intervalo passado como parâmetros para [**Dispatch.**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)</span><span class="sxs-lookup"><span data-stu-id="ab2c8-107">Possible values vary across the range passed as parameters to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch).</span></span> <span data-ttu-id="ab2c8-108">Por exemplo, chamar Dispatch(2,1,1) resulta em valores possíveis de 0,0,0 e 1,0,0.</span><span class="sxs-lookup"><span data-stu-id="ab2c8-108">For example calling Dispatch(2,1,1) results in possible values of 0,0,0 and 1,0,0.</span></span>

<span data-ttu-id="ab2c8-109">Define o deslocamento de grupo dentro de uma [**chamada dispatch,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) por dimensão da chamada de expedição.</span><span class="sxs-lookup"><span data-stu-id="ab2c8-109">Defines the group offset within a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) call, per dimension of the dispatch call.</span></span>

## <a name="type"></a><span data-ttu-id="ab2c8-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab2c8-110">Type</span></span>



| <span data-ttu-id="ab2c8-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab2c8-111">Type</span></span>      |
|-------|
| <span data-ttu-id="ab2c8-112">uint3</span><span class="sxs-lookup"><span data-stu-id="ab2c8-112">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ab2c8-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab2c8-113">Remarks</span></span>

<span data-ttu-id="ab2c8-114">Esse valor do sistema é opcional.</span><span class="sxs-lookup"><span data-stu-id="ab2c8-114">This system value is optional.</span></span>

<span data-ttu-id="ab2c8-115">A ilustração a seguir mostra a relação entre os parâmetros passados para [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), os valores especificados no [atributo numthreads,](sm5-attributes-numthreads.md) numthreads(10,8,3) e os valores que serão passados para o sombreador de computação para os valores do sistema relacionados ao thread [(SV \_ GroupIndex,](sv-groupindex.md)[SV \_ DispatchThreadID,](sv-dispatchthreadid.md)[SV \_ GroupThreadID,](sv-groupthreadid.md)SV \_ GroupID).</span><span class="sxs-lookup"><span data-stu-id="ab2c8-115">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),[SV\_GroupThreadID](sv-groupthreadid.md),SV\_GroupID).</span></span>

![ilustração da relação entre expedição, grupos de threads e threads](images/threadgroupids.png)

<span data-ttu-id="ab2c8-117">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="ab2c8-117">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="ab2c8-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="ab2c8-118">Vertex</span></span> | <span data-ttu-id="ab2c8-119">Casco</span><span class="sxs-lookup"><span data-stu-id="ab2c8-119">Hull</span></span> | <span data-ttu-id="ab2c8-120">Domínio</span><span class="sxs-lookup"><span data-stu-id="ab2c8-120">Domain</span></span> | <span data-ttu-id="ab2c8-121">Geometry</span><span class="sxs-lookup"><span data-stu-id="ab2c8-121">Geometry</span></span> | <span data-ttu-id="ab2c8-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="ab2c8-122">Pixel</span></span> | <span data-ttu-id="ab2c8-123">Computação</span><span class="sxs-lookup"><span data-stu-id="ab2c8-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="ab2c8-124">x</span><span class="sxs-lookup"><span data-stu-id="ab2c8-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ab2c8-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab2c8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab2c8-126">Semântica</span><span class="sxs-lookup"><span data-stu-id="ab2c8-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="ab2c8-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="ab2c8-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
