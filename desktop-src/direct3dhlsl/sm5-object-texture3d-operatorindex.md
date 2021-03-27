---
title: 'Função Texture3D:: Operator'
description: 'Retorna uma variável de recurso somente leitura. | Função Texture3D:: Operator'
ms.assetid: d7e27778-6a96-47f8-a58a-1966452adf04
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
ms.openlocfilehash: 5c3bb3718094ee859d1e33a046fde7016973a0aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103663897"
---
# <a name="texture3doperator--function"></a><span data-ttu-id="c3125-105">Função Texture3D:: Operator</span><span class="sxs-lookup"><span data-stu-id="c3125-105">Texture3D::Operator  function</span></span>

<span data-ttu-id="c3125-106">Retorna uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c3125-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3125-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3125-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="c3125-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3125-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3125-109">*pos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c3125-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3125-110">Tipo: **uint3**</span><span class="sxs-lookup"><span data-stu-id="c3125-110">Type: **uint3**</span></span>

<span data-ttu-id="c3125-111">A posição do índice.</span><span class="sxs-lookup"><span data-stu-id="c3125-111">The index position.</span></span> <span data-ttu-id="c3125-112">Contém as coordenadas (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="c3125-112">Contains the (x, y, z) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3125-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c3125-113">Return value</span></span>

<span data-ttu-id="c3125-114">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="c3125-114">Type: **R**</span></span>

<span data-ttu-id="c3125-115">Uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c3125-115">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3125-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3125-116">Remarks</span></span>

<span data-ttu-id="c3125-117">Esse método sempre acessa o primeiro nível de MIP.</span><span class="sxs-lookup"><span data-stu-id="c3125-117">This method always accesses the first mip level.</span></span> <span data-ttu-id="c3125-118">Para especificar outros níveis de MIP, use o [**MIP \[ \] \[ \] . Operator**](sm5-object-texture3d-mipsoperatorindex.md) .</span><span class="sxs-lookup"><span data-stu-id="c3125-118">To specify other mip levels use the [**mip.operator\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md) instead.</span></span>

<span data-ttu-id="c3125-119">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="c3125-119">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c3125-120">Vértice</span><span class="sxs-lookup"><span data-stu-id="c3125-120">Vertex</span></span> | <span data-ttu-id="c3125-121">Envoltória</span><span class="sxs-lookup"><span data-stu-id="c3125-121">Hull</span></span> | <span data-ttu-id="c3125-122">Domínio</span><span class="sxs-lookup"><span data-stu-id="c3125-122">Domain</span></span> | <span data-ttu-id="c3125-123">Geometria</span><span class="sxs-lookup"><span data-stu-id="c3125-123">Geometry</span></span> | <span data-ttu-id="c3125-124">16x16</span><span class="sxs-lookup"><span data-stu-id="c3125-124">Pixel</span></span> | <span data-ttu-id="c3125-125">Computação</span><span class="sxs-lookup"><span data-stu-id="c3125-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c3125-126">x</span><span class="sxs-lookup"><span data-stu-id="c3125-126">x</span></span>      | <span data-ttu-id="c3125-127">x</span><span class="sxs-lookup"><span data-stu-id="c3125-127">x</span></span>    | <span data-ttu-id="c3125-128">x</span><span class="sxs-lookup"><span data-stu-id="c3125-128">x</span></span>      | <span data-ttu-id="c3125-129">x</span><span class="sxs-lookup"><span data-stu-id="c3125-129">x</span></span>        | <span data-ttu-id="c3125-130">x</span><span class="sxs-lookup"><span data-stu-id="c3125-130">x</span></span>     | <span data-ttu-id="c3125-131">x</span><span class="sxs-lookup"><span data-stu-id="c3125-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c3125-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3125-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3125-133">Texture3D</span><span class="sxs-lookup"><span data-stu-id="c3125-133">Texture3D</span></span>](sm5-object-texture3d.md)
</dt> <dt>

[<span data-ttu-id="c3125-134">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c3125-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




