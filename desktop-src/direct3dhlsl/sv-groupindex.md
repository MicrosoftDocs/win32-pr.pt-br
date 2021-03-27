---
title: SV_GroupIndex
description: O \ 0034; achatado \ 0034; índice de um thread de sombreador de computação dentro de um grupo de threads, que transforma a GroupThreadID de VA multidimensional \_ em um valor 1D. \_GROUPINDEX VA varia de 0 a (numthreadsX \ numthreadsY \ numThreadsZ) \ 8211; uma.
ms.assetid: e793be10-7c83-478c-859a-4b0a2c537570
keywords:
- SV_GroupIndex HLSL
topic_type:
- apiref
api_name:
- SV_GroupIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 952a94378a0570d5bb7bc4f08959074bc8a4da4d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641319"
---
# <a name="sv_groupindex"></a><span data-ttu-id="4309e-105">\_GROUPINDEX VA</span><span class="sxs-lookup"><span data-stu-id="4309e-105">SV\_GroupIndex</span></span>

<span data-ttu-id="4309e-106">O índice "achatado" de um thread de sombreador de computação em um grupo de threads, que transforma a GroupThreadID de VA multidimensional \_ em um valor 1D.</span><span class="sxs-lookup"><span data-stu-id="4309e-106">The "flattened" index of a compute shader thread within a thread group, which turns the multi-dimensional SV\_GroupThreadID into a 1D value.</span></span> <span data-ttu-id="4309e-107">\_A GroupIndex de VA varia de 0 a (numthreadsX \* numthreadsY \* numThreadsZ) – 1.</span><span class="sxs-lookup"><span data-stu-id="4309e-107">SV\_GroupIndex varies from 0 to (numthreadsX \* numthreadsY \* numThreadsZ) – 1.</span></span>

## <a name="type"></a><span data-ttu-id="4309e-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="4309e-108">Type</span></span>



| <span data-ttu-id="4309e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="4309e-109">Type</span></span> |
|------|
| <span data-ttu-id="4309e-110">uint</span><span class="sxs-lookup"><span data-stu-id="4309e-110">uint</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4309e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4309e-111">Remarks</span></span>


```
SV_GroupIndex = SV_GroupThreadID.z*dimx*dimy + 
                      SV_GroupThreadID.y*dimx + 
                      SV_GroupThreadID.x
```



<span data-ttu-id="4309e-112">em que Dimx e Dimy são as dimensões especificadas no atributo [numthreads](sm5-attributes-numthreads.md) para o ponto de entrada.</span><span class="sxs-lookup"><span data-stu-id="4309e-112">where dimx and dimy are the dimensions specified in the [numthreads](sm5-attributes-numthreads.md) attribute for the entry point.</span></span>

<span data-ttu-id="4309e-113">Esse valor de sistema é opcional.</span><span class="sxs-lookup"><span data-stu-id="4309e-113">This system value is optional.</span></span> <span data-ttu-id="4309e-114">No entanto, seu uso garante que um thread só grave em sua região atribuída de memória na variável groupshared.</span><span class="sxs-lookup"><span data-stu-id="4309e-114">However, its use ensures that a thread only writes to its assigned region of memory in the groupshared variable.</span></span>

<span data-ttu-id="4309e-115">A ilustração a seguir mostra a relação entre os parâmetros passados [**para ID3D11DeviceContext::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), expedição (5, 3, 2), os valores especificados no [atributo numthreads](sm5-attributes-numthreads.md) , numthreads (10, 8, 3) e valores que serão passados para o sombreador de computação para os valores do sistema relacionados ao thread (VA \_ GroupIndex,[VA \_ DispatchThreadID](sv-dispatchthreadid.md),[VA \_ GroupThreadID](sv-groupthreadid.md), a [ \_ DefaultGroupID](sv-groupid.md)).</span><span class="sxs-lookup"><span data-stu-id="4309e-115">The following illustration shows the relationship between the parameters passed to [**ID3D11DeviceContext::Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values (SV\_GroupIndex,[SV\_DispatchThreadID](sv-dispatchthreadid.md),[SV\_GroupThreadID](sv-groupthreadid.md),[SV\_GroupID](sv-groupid.md)).</span></span>

![ilustração da relação entre expedição, grupos de threads e threads](images/threadgroupids.png)

<span data-ttu-id="4309e-117">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="4309e-117">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="4309e-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="4309e-118">Vertex</span></span> | <span data-ttu-id="4309e-119">Envoltória</span><span class="sxs-lookup"><span data-stu-id="4309e-119">Hull</span></span> | <span data-ttu-id="4309e-120">Domínio</span><span class="sxs-lookup"><span data-stu-id="4309e-120">Domain</span></span> | <span data-ttu-id="4309e-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="4309e-121">Geometry</span></span> | <span data-ttu-id="4309e-122">16x16</span><span class="sxs-lookup"><span data-stu-id="4309e-122">Pixel</span></span> | <span data-ttu-id="4309e-123">Computação</span><span class="sxs-lookup"><span data-stu-id="4309e-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="4309e-124">x</span><span class="sxs-lookup"><span data-stu-id="4309e-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4309e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="4309e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4309e-126">Semântica</span><span class="sxs-lookup"><span data-stu-id="4309e-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="4309e-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="4309e-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 