---
title: 'Função RWTexture1DArray:: Operator'
description: 'Retorna uma variável de recurso. | Função RWTexture1DArray:: Operator'
ms.assetid: 7047e670-dd78-4b73-8d80-5575e458f27c
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
ms.openlocfilehash: 6f8623ab25b42f6865e401c5b263a1774206c752
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968440"
---
# <a name="rwtexture1darrayoperator--function"></a><span data-ttu-id="7b494-105">Função RWTexture1DArray:: Operator</span><span class="sxs-lookup"><span data-stu-id="7b494-105">RWTexture1DArray::Operator  function</span></span>

<span data-ttu-id="7b494-106">Retorna uma variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="7b494-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b494-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b494-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="7b494-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b494-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b494-109">*pos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b494-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b494-110">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="7b494-110">Type: **uint2**</span></span>

<span data-ttu-id="7b494-111">A posição do índice.</span><span class="sxs-lookup"><span data-stu-id="7b494-111">The index position.</span></span> <span data-ttu-id="7b494-112">O primeiro componente contém a coordenada x.</span><span class="sxs-lookup"><span data-stu-id="7b494-112">The first component contains the x coordinate.</span></span> <span data-ttu-id="7b494-113">O segundo componente indica a fatia de matriz desejada.</span><span class="sxs-lookup"><span data-stu-id="7b494-113">The second component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b494-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7b494-114">Return value</span></span>

<span data-ttu-id="7b494-115">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="7b494-115">Type: **R**</span></span>

<span data-ttu-id="7b494-116">Uma variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="7b494-116">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b494-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b494-117">Remarks</span></span>

<span data-ttu-id="7b494-118">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="7b494-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7b494-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="7b494-119">Vertex</span></span> | <span data-ttu-id="7b494-120">Envoltória</span><span class="sxs-lookup"><span data-stu-id="7b494-120">Hull</span></span> | <span data-ttu-id="7b494-121">Domínio</span><span class="sxs-lookup"><span data-stu-id="7b494-121">Domain</span></span> | <span data-ttu-id="7b494-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="7b494-122">Geometry</span></span> | <span data-ttu-id="7b494-123">16x16</span><span class="sxs-lookup"><span data-stu-id="7b494-123">Pixel</span></span> | <span data-ttu-id="7b494-124">Computação</span><span class="sxs-lookup"><span data-stu-id="7b494-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="7b494-125">x</span><span class="sxs-lookup"><span data-stu-id="7b494-125">x</span></span>     | <span data-ttu-id="7b494-126">x</span><span class="sxs-lookup"><span data-stu-id="7b494-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7b494-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b494-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b494-128">RWTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="7b494-128">RWTexture1DArray</span></span>](sm5-object-rwtexture1darray.md)
</dt> <dt>

[<span data-ttu-id="7b494-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="7b494-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




