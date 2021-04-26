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
ms.openlocfilehash: cb9265734663881981f1626db6e23c6b7dd9415a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996503"
---
# <a name="sv_domainlocation"></a><span data-ttu-id="17061-104">\_DOMAINLOCATION VA</span><span class="sxs-lookup"><span data-stu-id="17061-104">SV\_DomainLocation</span></span>

<span data-ttu-id="17061-105">Define o local no envoltória do ponto de domínio atual que está sendo avaliado.</span><span class="sxs-lookup"><span data-stu-id="17061-105">Defines the location on the hull of the current domain point being evaluated.</span></span>

## <a name="type"></a><span data-ttu-id="17061-106">Digite</span><span class="sxs-lookup"><span data-stu-id="17061-106">Type</span></span>



|        |                |
|--------|----------------|
| <span data-ttu-id="17061-107">Digite</span><span class="sxs-lookup"><span data-stu-id="17061-107">Type</span></span>   | <span data-ttu-id="17061-108">Topologia de entrada</span><span class="sxs-lookup"><span data-stu-id="17061-108">Input Topology</span></span> |
| <span data-ttu-id="17061-109">float2</span><span class="sxs-lookup"><span data-stu-id="17061-109">float2</span></span> | <span data-ttu-id="17061-110">patch quádruplo</span><span class="sxs-lookup"><span data-stu-id="17061-110">quad patch</span></span>     |
| <span data-ttu-id="17061-111">float3</span><span class="sxs-lookup"><span data-stu-id="17061-111">float3</span></span> | <span data-ttu-id="17061-112">Tri patch</span><span class="sxs-lookup"><span data-stu-id="17061-112">tri patch</span></span>      |
| <span data-ttu-id="17061-113">float2</span><span class="sxs-lookup"><span data-stu-id="17061-113">float2</span></span> | <span data-ttu-id="17061-114">isoline</span><span class="sxs-lookup"><span data-stu-id="17061-114">isoline</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="17061-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="17061-115">Remarks</span></span>

<span data-ttu-id="17061-116">Esse valor do sistema é necessário.</span><span class="sxs-lookup"><span data-stu-id="17061-116">This system value is required.</span></span>

<span data-ttu-id="17061-117">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="17061-117">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="17061-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="17061-118">Vertex</span></span> | <span data-ttu-id="17061-119">Envoltória</span><span class="sxs-lookup"><span data-stu-id="17061-119">Hull</span></span> | <span data-ttu-id="17061-120">Domain</span><span class="sxs-lookup"><span data-stu-id="17061-120">Domain</span></span> | <span data-ttu-id="17061-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="17061-121">Geometry</span></span> | <span data-ttu-id="17061-122">16x16</span><span class="sxs-lookup"><span data-stu-id="17061-122">Pixel</span></span> | <span data-ttu-id="17061-123">Computação</span><span class="sxs-lookup"><span data-stu-id="17061-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      | <span data-ttu-id="17061-124">x</span><span class="sxs-lookup"><span data-stu-id="17061-124">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="17061-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="17061-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17061-126">Semântica</span><span class="sxs-lookup"><span data-stu-id="17061-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="17061-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="17061-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




