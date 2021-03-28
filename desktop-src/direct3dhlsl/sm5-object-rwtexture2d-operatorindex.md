---
title: 'Função RWTexture2D:: Operator'
description: 'Retorna uma variável de recurso. | Função RWTexture2D:: Operator'
ms.assetid: 339dba7d-b0c6-4112-ae40-555661577a3e
keywords:
- Função Operator HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c1ff25cdf4a0f33d041500f6a81220261f216c4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968421"
---
# <a name="rwtexture2doperator--function"></a><span data-ttu-id="e0fa4-105">Função RWTexture2D:: Operator</span><span class="sxs-lookup"><span data-stu-id="e0fa4-105">RWTexture2D::Operator  function</span></span>

<span data-ttu-id="e0fa4-106">Retorna uma variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="e0fa4-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0fa4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0fa4-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="e0fa4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0fa4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0fa4-109">*pos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e0fa4-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0fa4-110">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="e0fa4-110">Type: **uint2**</span></span>

<span data-ttu-id="e0fa4-111">A posição do índice.</span><span class="sxs-lookup"><span data-stu-id="e0fa4-111">The index position.</span></span> <span data-ttu-id="e0fa4-112">Contém as coordenadas (x, y).</span><span class="sxs-lookup"><span data-stu-id="e0fa4-112">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0fa4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e0fa4-113">Return value</span></span>

<span data-ttu-id="e0fa4-114">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="e0fa4-114">Type: **R**</span></span>

<span data-ttu-id="e0fa4-115">Uma variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="e0fa4-115">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0fa4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0fa4-116">Remarks</span></span>

<span data-ttu-id="e0fa4-117">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="e0fa4-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e0fa4-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="e0fa4-118">Vertex</span></span> | <span data-ttu-id="e0fa4-119">Envoltória</span><span class="sxs-lookup"><span data-stu-id="e0fa4-119">Hull</span></span> | <span data-ttu-id="e0fa4-120">Domínio</span><span class="sxs-lookup"><span data-stu-id="e0fa4-120">Domain</span></span> | <span data-ttu-id="e0fa4-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="e0fa4-121">Geometry</span></span> | <span data-ttu-id="e0fa4-122">16x16</span><span class="sxs-lookup"><span data-stu-id="e0fa4-122">Pixel</span></span> | <span data-ttu-id="e0fa4-123">Computação</span><span class="sxs-lookup"><span data-stu-id="e0fa4-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="e0fa4-124">x</span><span class="sxs-lookup"><span data-stu-id="e0fa4-124">x</span></span>     | <span data-ttu-id="e0fa4-125">x</span><span class="sxs-lookup"><span data-stu-id="e0fa4-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e0fa4-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0fa4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0fa4-127">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="e0fa4-127">RWTexture2D</span></span>](sm5-object-rwtexture2d.md)
</dt> <dt>

[<span data-ttu-id="e0fa4-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e0fa4-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




