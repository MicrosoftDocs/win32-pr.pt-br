---
title: 'Função Texture2DArray:: Operator'
description: 'Retorna uma variável de recurso somente leitura. | Função Texture2DArray:: Operator'
ms.assetid: eb6ff496-c46f-405f-a172-ab747415a2f9
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
ms.openlocfilehash: 1b86aad839fbf28a4fc666b3a5fe5c5788b7b3ae
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104011988"
---
# <a name="texture2darrayoperator--function"></a><span data-ttu-id="e5b0f-105">Função Texture2DArray:: Operator</span><span class="sxs-lookup"><span data-stu-id="e5b0f-105">Texture2DArray::Operator  function</span></span>

<span data-ttu-id="e5b0f-106">Retorna uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="e5b0f-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5b0f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5b0f-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="e5b0f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5b0f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5b0f-109">*pos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5b0f-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5b0f-110">Tipo: **uint3**</span><span class="sxs-lookup"><span data-stu-id="e5b0f-110">Type: **uint3**</span></span>

<span data-ttu-id="e5b0f-111">A posição do índice.</span><span class="sxs-lookup"><span data-stu-id="e5b0f-111">The index position.</span></span> <span data-ttu-id="e5b0f-112">O primeiro e o segundo componentes contêm as coordenadas (x, y).</span><span class="sxs-lookup"><span data-stu-id="e5b0f-112">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="e5b0f-113">O terceiro componente indica a fatia de matriz desejada.</span><span class="sxs-lookup"><span data-stu-id="e5b0f-113">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5b0f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e5b0f-114">Return value</span></span>

<span data-ttu-id="e5b0f-115">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="e5b0f-115">Type: **R**</span></span>

<span data-ttu-id="e5b0f-116">Uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="e5b0f-116">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5b0f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5b0f-117">Remarks</span></span>

<span data-ttu-id="e5b0f-118">Esse método sempre acessa o primeiro nível de MIP.</span><span class="sxs-lookup"><span data-stu-id="e5b0f-118">This method always accesses the first mip level.</span></span> <span data-ttu-id="e5b0f-119">Para especificar outros níveis de MIP, use o método [**MIP \[ \] \[ \] . Operator**](sm5-object-texture2darray-mipsoperatorindex.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="e5b0f-119">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md) method instead.</span></span>

<span data-ttu-id="e5b0f-120">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="e5b0f-120">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="e5b0f-121">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="e5b0f-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e5b0f-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="e5b0f-122">Vertex</span></span> | <span data-ttu-id="e5b0f-123">Envoltória</span><span class="sxs-lookup"><span data-stu-id="e5b0f-123">Hull</span></span> | <span data-ttu-id="e5b0f-124">Domínio</span><span class="sxs-lookup"><span data-stu-id="e5b0f-124">Domain</span></span> | <span data-ttu-id="e5b0f-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="e5b0f-125">Geometry</span></span> | <span data-ttu-id="e5b0f-126">16x16</span><span class="sxs-lookup"><span data-stu-id="e5b0f-126">Pixel</span></span> | <span data-ttu-id="e5b0f-127">Computação</span><span class="sxs-lookup"><span data-stu-id="e5b0f-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e5b0f-128">x</span><span class="sxs-lookup"><span data-stu-id="e5b0f-128">x</span></span>      | <span data-ttu-id="e5b0f-129">x</span><span class="sxs-lookup"><span data-stu-id="e5b0f-129">x</span></span>    | <span data-ttu-id="e5b0f-130">x</span><span class="sxs-lookup"><span data-stu-id="e5b0f-130">x</span></span>      | <span data-ttu-id="e5b0f-131">x</span><span class="sxs-lookup"><span data-stu-id="e5b0f-131">x</span></span>        | <span data-ttu-id="e5b0f-132">x</span><span class="sxs-lookup"><span data-stu-id="e5b0f-132">x</span></span>     | <span data-ttu-id="e5b0f-133">x</span><span class="sxs-lookup"><span data-stu-id="e5b0f-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e5b0f-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5b0f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5b0f-135">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="e5b0f-135">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> <dt>

[<span data-ttu-id="e5b0f-136">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e5b0f-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




