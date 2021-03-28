---
title: SV_GroupID
description: Índices para os quais o grupo de threads um sombreador de computação está sendo executado.
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
ms.openlocfilehash: a2588474a4c6f2cfc6d616cdb70940277389fd1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084617"
---
# <a name="sv_groupid"></a><span data-ttu-id="d9fe0-104">\_GroupId da VA</span><span class="sxs-lookup"><span data-stu-id="d9fe0-104">SV\_GroupID</span></span>

<span data-ttu-id="d9fe0-105">Índices para os quais o grupo de threads um sombreador de computação está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="d9fe0-105">Indices for which thread group a compute shader is executing in.</span></span> <span data-ttu-id="d9fe0-106">Os índices são para o grupo inteiro e não para um thread individual.</span><span class="sxs-lookup"><span data-stu-id="d9fe0-106">The indices are to the whole group and not an individual thread.</span></span> <span data-ttu-id="d9fe0-107">Os valores possíveis variam entre o intervalo passado como parâmetros para [**expedição**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch).</span><span class="sxs-lookup"><span data-stu-id="d9fe0-107">Possible values vary across the range passed as parameters to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch).</span></span> <span data-ttu-id="d9fe0-108">Por exemplo, chamar dispatch (2, 1, 1) resulta em valores possíveis de 0, 0, 0 e 1, 0, 0.</span><span class="sxs-lookup"><span data-stu-id="d9fe0-108">For example calling Dispatch(2,1,1) results in possible values of 0,0,0 and 1,0,0.</span></span>

<span data-ttu-id="d9fe0-109">Define o deslocamento do grupo dentro de uma chamada de [**expedição**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) , por dimensão da chamada de expedição.</span><span class="sxs-lookup"><span data-stu-id="d9fe0-109">Defines the group offset within a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) call, per dimension of the dispatch call.</span></span>

## <a name="type"></a><span data-ttu-id="d9fe0-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="d9fe0-110">Type</span></span>



|       |
|-------|
| <span data-ttu-id="d9fe0-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="d9fe0-111">Type</span></span>  |
| <span data-ttu-id="d9fe0-112">uint3</span><span class="sxs-lookup"><span data-stu-id="d9fe0-112">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d9fe0-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9fe0-113">Remarks</span></span>

<span data-ttu-id="d9fe0-114">Esse valor de sistema é opcional.</span><span class="sxs-lookup"><span data-stu-id="d9fe0-114">This system value is optional.</span></span>

<span data-ttu-id="d9fe0-115">A ilustração a seguir mostra a relação entre os parâmetros passados para [**expedição**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), expedição (5, 3, 2), os valores especificados no atributo [numthreads](sm5-attributes-numthreads.md) , numthreads (10, 8, 3) e valores que serão passados para o sombreador de computação para os valores do sistema relacionados ao thread ([VA \_ GroupIndex](sv-groupindex.md),[VA \_ DispatchThreadID](sv-dispatchthreadid.md),[VA \_ GroupThreadID](sv-groupthreadid.md), SV \_ GroupId).</span><span class="sxs-lookup"><span data-stu-id="d9fe0-115">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),[SV\_GroupThreadID](sv-groupthreadid.md),SV\_GroupID).</span></span>

![ilustração da relação entre expedição, grupos de threads e threads](images/threadgroupids.png)

<span data-ttu-id="d9fe0-117">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="d9fe0-117">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d9fe0-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="d9fe0-118">Vertex</span></span> | <span data-ttu-id="d9fe0-119">Envoltória</span><span class="sxs-lookup"><span data-stu-id="d9fe0-119">Hull</span></span> | <span data-ttu-id="d9fe0-120">Domínio</span><span class="sxs-lookup"><span data-stu-id="d9fe0-120">Domain</span></span> | <span data-ttu-id="d9fe0-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="d9fe0-121">Geometry</span></span> | <span data-ttu-id="d9fe0-122">16x16</span><span class="sxs-lookup"><span data-stu-id="d9fe0-122">Pixel</span></span> | <span data-ttu-id="d9fe0-123">Computação</span><span class="sxs-lookup"><span data-stu-id="d9fe0-123">Compute</span></span> |
|        |      |        |          |       | <span data-ttu-id="d9fe0-124">x</span><span class="sxs-lookup"><span data-stu-id="d9fe0-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d9fe0-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9fe0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9fe0-126">Semântica</span><span class="sxs-lookup"><span data-stu-id="d9fe0-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="d9fe0-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="d9fe0-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 