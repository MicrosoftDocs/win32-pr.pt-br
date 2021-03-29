---
title: 'Função Texture2D:: Operator'
description: 'Retorna uma variável de recurso somente leitura. | Função Texture2D:: Operator'
ms.assetid: 72ba3fc8-04c3-479a-b307-525020898bac
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
ms.openlocfilehash: 2c397b1b80836f48cb856d03ccdf52ad2c95ce48
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968438"
---
# <a name="texture2doperator--function"></a><span data-ttu-id="d9af2-105">Função Texture2D:: Operator</span><span class="sxs-lookup"><span data-stu-id="d9af2-105">Texture2D::Operator  function</span></span>

<span data-ttu-id="d9af2-106">Retorna uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d9af2-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9af2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d9af2-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="d9af2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9af2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9af2-109">*pos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d9af2-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9af2-110">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="d9af2-110">Type: **uint2**</span></span>

<span data-ttu-id="d9af2-111">A posição do índice.</span><span class="sxs-lookup"><span data-stu-id="d9af2-111">The index position.</span></span> <span data-ttu-id="d9af2-112">Contém as coordenadas (x, y).</span><span class="sxs-lookup"><span data-stu-id="d9af2-112">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9af2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d9af2-113">Return value</span></span>

<span data-ttu-id="d9af2-114">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="d9af2-114">Type: **R**</span></span>

<span data-ttu-id="d9af2-115">Uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d9af2-115">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9af2-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9af2-116">Remarks</span></span>

<span data-ttu-id="d9af2-117">Esse método sempre acessa o primeiro nível de MIP.</span><span class="sxs-lookup"><span data-stu-id="d9af2-117">This method always accesses the first mip level.</span></span> <span data-ttu-id="d9af2-118">Para especificar outros níveis de MIP, use o método [**MIP \[ \] \[ \] . Operator**](sm5-object-texture2d-mipsoperatorindex.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="d9af2-118">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture2d-mipsoperatorindex.md) method instead.</span></span>

<span data-ttu-id="d9af2-119">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="d9af2-119">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="d9af2-120">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="d9af2-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d9af2-121">Vértice</span><span class="sxs-lookup"><span data-stu-id="d9af2-121">Vertex</span></span> | <span data-ttu-id="d9af2-122">Envoltória</span><span class="sxs-lookup"><span data-stu-id="d9af2-122">Hull</span></span> | <span data-ttu-id="d9af2-123">Domínio</span><span class="sxs-lookup"><span data-stu-id="d9af2-123">Domain</span></span> | <span data-ttu-id="d9af2-124">Geometria</span><span class="sxs-lookup"><span data-stu-id="d9af2-124">Geometry</span></span> | <span data-ttu-id="d9af2-125">16x16</span><span class="sxs-lookup"><span data-stu-id="d9af2-125">Pixel</span></span> | <span data-ttu-id="d9af2-126">Computação</span><span class="sxs-lookup"><span data-stu-id="d9af2-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d9af2-127">x</span><span class="sxs-lookup"><span data-stu-id="d9af2-127">x</span></span>      | <span data-ttu-id="d9af2-128">x</span><span class="sxs-lookup"><span data-stu-id="d9af2-128">x</span></span>    | <span data-ttu-id="d9af2-129">x</span><span class="sxs-lookup"><span data-stu-id="d9af2-129">x</span></span>      | <span data-ttu-id="d9af2-130">x</span><span class="sxs-lookup"><span data-stu-id="d9af2-130">x</span></span>        | <span data-ttu-id="d9af2-131">x</span><span class="sxs-lookup"><span data-stu-id="d9af2-131">x</span></span>     | <span data-ttu-id="d9af2-132">x</span><span class="sxs-lookup"><span data-stu-id="d9af2-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d9af2-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9af2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9af2-134">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d9af2-134">Texture2D</span></span>](sm5-object-texture2d.md)
</dt> <dt>

[<span data-ttu-id="d9af2-135">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="d9af2-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




