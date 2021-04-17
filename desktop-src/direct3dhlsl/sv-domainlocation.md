---
title: SV_DomainLocation
description: Define o local no envoltória do ponto de domínio atual que está sendo avaliado.
ms.assetid: 907f568c-7c45-41e5-96c4-6e6b816a4a53
keywords:
- SV_DomainLocation HLSL
topic_type:
- apiref
api_name:
- SV_DomainLocation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c5195881df438c94cdaed7de8484d0df65e4d54
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104365027"
---
# <a name="sv_domainlocation"></a><span data-ttu-id="4685a-104">\_DOMAINLOCATION VA</span><span class="sxs-lookup"><span data-stu-id="4685a-104">SV\_DomainLocation</span></span>

<span data-ttu-id="4685a-105">Define o local no envoltória do ponto de domínio atual que está sendo avaliado.</span><span class="sxs-lookup"><span data-stu-id="4685a-105">Defines the location on the hull of the current domain point being evaluated.</span></span>

## <a name="type"></a><span data-ttu-id="4685a-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="4685a-106">Type</span></span>



|        |                |
|--------|----------------|
| <span data-ttu-id="4685a-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="4685a-107">Type</span></span>   | <span data-ttu-id="4685a-108">Topologia de entrada</span><span class="sxs-lookup"><span data-stu-id="4685a-108">Input Topology</span></span> |
| <span data-ttu-id="4685a-109">float2</span><span class="sxs-lookup"><span data-stu-id="4685a-109">float2</span></span> | <span data-ttu-id="4685a-110">patch quádruplo</span><span class="sxs-lookup"><span data-stu-id="4685a-110">quad patch</span></span>     |
| <span data-ttu-id="4685a-111">float3</span><span class="sxs-lookup"><span data-stu-id="4685a-111">float3</span></span> | <span data-ttu-id="4685a-112">Tri patch</span><span class="sxs-lookup"><span data-stu-id="4685a-112">tri patch</span></span>      |
| <span data-ttu-id="4685a-113">float2</span><span class="sxs-lookup"><span data-stu-id="4685a-113">float2</span></span> | <span data-ttu-id="4685a-114">isoline</span><span class="sxs-lookup"><span data-stu-id="4685a-114">isoline</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="4685a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4685a-115">Remarks</span></span>

<span data-ttu-id="4685a-116">Esse valor do sistema é necessário.</span><span class="sxs-lookup"><span data-stu-id="4685a-116">This system value is required.</span></span>

<span data-ttu-id="4685a-117">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="4685a-117">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4685a-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="4685a-118">Vertex</span></span> | <span data-ttu-id="4685a-119">Envoltória</span><span class="sxs-lookup"><span data-stu-id="4685a-119">Hull</span></span> | <span data-ttu-id="4685a-120">Domínio</span><span class="sxs-lookup"><span data-stu-id="4685a-120">Domain</span></span> | <span data-ttu-id="4685a-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="4685a-121">Geometry</span></span> | <span data-ttu-id="4685a-122">16x16</span><span class="sxs-lookup"><span data-stu-id="4685a-122">Pixel</span></span> | <span data-ttu-id="4685a-123">Computação</span><span class="sxs-lookup"><span data-stu-id="4685a-123">Compute</span></span> |
|        |      | <span data-ttu-id="4685a-124">x</span><span class="sxs-lookup"><span data-stu-id="4685a-124">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="4685a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="4685a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4685a-126">Semântica</span><span class="sxs-lookup"><span data-stu-id="4685a-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="4685a-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="4685a-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




