---
description: Envia um raio para uma pesquisa de ocorrências em uma estrutura de aceleração.
ms.assetid: ''
title: Função TraceRay
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TraceRay
api_type:
- NA
ms.openlocfilehash: faeed928b25acb4dac95e47a46a103daf87124e0
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "105768218"
---
# <a name="traceray-function"></a><span data-ttu-id="8890f-103">Função TraceRay</span><span class="sxs-lookup"><span data-stu-id="8890f-103">TraceRay function</span></span>

<span data-ttu-id="8890f-104">Envia um raio para uma pesquisa de ocorrências em uma estrutura de aceleração.</span><span class="sxs-lookup"><span data-stu-id="8890f-104">Sends a ray into a search for hits in an acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="8890f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8890f-105">Syntax</span></span>
<span data-ttu-id="8890f-106">Essa definição de função intrínseca é equivalente ao seguinte modelo de função:</span><span class="sxs-lookup"><span data-stu-id="8890f-106">This intrinsic function definition is equivalent to the following function template:</span></span>

```
Template<payload_t>
void TraceRay(RaytracingAccelerationStructure AccelerationStructure,
              uint RayFlags,
              uint InstanceInclusionMask,
              uint RayContributionToHitGroupIndex,
              uint MultiplierForGeometryContributionToHitGroupIndex,
              uint MissShaderIndex,
              RayDesc Ray,
              inout payload_t Payload);

```



## <a name="parameters"></a><span data-ttu-id="8890f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8890f-107">Parameters</span></span>

`AccelerationStructure`

<span data-ttu-id="8890f-108">A estrutura de aceleração de nível superior a ser usada.</span><span class="sxs-lookup"><span data-stu-id="8890f-108">The top-level acceleration structure to use.</span></span> <span data-ttu-id="8890f-109">A especificação de uma estrutura de aceleração nula força um erro.</span><span class="sxs-lookup"><span data-stu-id="8890f-109">Specifying a NULL acceleration structure forces a miss.</span></span>

`RayFlags`

<span data-ttu-id="8890f-110">Combinação válida de valores de [ray_flag](ray_flag.md) .</span><span class="sxs-lookup"><span data-stu-id="8890f-110">Valid combination of [ray_flag](ray_flag.md) values.</span></span> <span data-ttu-id="8890f-111">Somente os sinalizadores de Ray definidos são propagados pelo sistema, ou seja, são visíveis para o sombreador [RayFlags](rayflags.md) intrínseco.</span><span class="sxs-lookup"><span data-stu-id="8890f-111">Only defined ray flags are propagated by the system, i.e. are visible to the [RayFlags](rayflags.md) shader intrinsic.</span></span>

`InstanceInclusionMask`

<span data-ttu-id="8890f-112">Um inteiro sem sinal, os 8 bits inferiores que são usados para incluir ou rejeitar instâncias de geometria com base no InstanceMask em cada instância.</span><span class="sxs-lookup"><span data-stu-id="8890f-112">An unsigned integer, the bottom 8 bits of which are used to include or reject geometry instances based on the InstanceMask in each instance.</span></span> <span data-ttu-id="8890f-113">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="8890f-113">For example:</span></span>
```
if(!((InstanceInclusionMask & InstanceMask) & 0xff)) { //ignore intersection }
```

`RayContributionToHitGroupIndex`

<span data-ttu-id="8890f-114">Um inteiro não assinado que especifica o deslocamento a ser adicionado aos cálculos de endereçamento em tabelas de sombreamento para indexação de grupo de acesso.</span><span class="sxs-lookup"><span data-stu-id="8890f-114">An unsigned integer specifying the offset to add into addressing calculations within shader tables for hit group indexing.</span></span>  <span data-ttu-id="8890f-115">Somente os 4 últimos bits desse valor são usados.</span><span class="sxs-lookup"><span data-stu-id="8890f-115">Only the bottom 4 bits of this value are used.</span></span>

`MultiplierForGeometryContributionToHitGroupIndex`

<span data-ttu-id="8890f-116">Um inteiro não assinado que especifica o stride para multiplicar por *GeometryContributionToHitGroupIndex*, que é apenas o índice baseado em 0 que a geometria foi fornecida pelo aplicativo em sua estrutura de aceleração de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="8890f-116">An unsigned integer specifying the stride to multiply by *GeometryContributionToHitGroupIndex*, which is just the 0 based index the geometry was supplied by the app into its bottom-level acceleration structure.</span></span> <span data-ttu-id="8890f-117">Somente os 16 bits inferiores desse valor de multiplicador são usados.</span><span class="sxs-lookup"><span data-stu-id="8890f-117">Only the bottom 16 bits of this multiplier value are used.</span></span>

`MissShaderIndex`

<span data-ttu-id="8890f-118">Um inteiro sem sinal que especifica o índice do sombreador ausente dentro de uma tabela de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8890f-118">An unsigned integer specifying the index of the miss shader within a shader table.</span></span>

`Ray`

<span data-ttu-id="8890f-119">Um [**RayDesc**](raydesc.md) que representa o raio a ser rastreado.</span><span class="sxs-lookup"><span data-stu-id="8890f-119">A [**RayDesc**](raydesc.md) representing the ray to be traced.</span></span>

`Payload`

<span data-ttu-id="8890f-120">Uma carga Ray definida pelo usuário foi acessada tanto para entrada quanto para saída por sombreadores invocados durante raytracing.</span><span class="sxs-lookup"><span data-stu-id="8890f-120">A user defined ray payload accessed both for both input and output by shaders invoked during raytracing.</span></span>  <span data-ttu-id="8890f-121">Após a conclusão do [**TraceRay**](traceray-function.md) , o chamador também pode acessar a carga.</span><span class="sxs-lookup"><span data-stu-id="8890f-121">After [**TraceRay**](traceray-function.md) completes, the caller can access the payload as well.</span></span>

## <a name="return-value"></a><span data-ttu-id="8890f-122">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="8890f-122">Return Value</span></span>

<span data-ttu-id="8890f-123">**void**</span><span class="sxs-lookup"><span data-stu-id="8890f-123">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="8890f-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="8890f-124">Remarks</span></span>

<span data-ttu-id="8890f-125">Essa função pode ser chamada nos seguintes tipos de sombreador raytracing:</span><span class="sxs-lookup"><span data-stu-id="8890f-125">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="8890f-126">**Sombreador do clique mais próximo**</span><span class="sxs-lookup"><span data-stu-id="8890f-126">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="8890f-127">**Sombreador de resolução**</span><span class="sxs-lookup"><span data-stu-id="8890f-127">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="8890f-128">**Sombreador da geração de raio**</span><span class="sxs-lookup"><span data-stu-id="8890f-128">**Ray Generation Shader**</span></span>](ray-generation-shader.md)



## <a name="see-also"></a><span data-ttu-id="8890f-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="8890f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8890f-130">Referência HLSL de raytracing do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="8890f-130">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




