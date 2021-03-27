---
title: 'Função RWTexture2DArray:: Operator'
description: 'Retorna uma variável de recurso. | Função RWTexture2DArray:: Operator'
ms.assetid: ae3d0697-ea0a-450d-bdfe-7bc5d8faf11a
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
ms.openlocfilehash: faf49c48fbf5042ce2765005cd8daea4d1227255
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104011989"
---
# <a name="rwtexture2darrayoperator--function"></a><span data-ttu-id="a56be-105">Função RWTexture2DArray:: Operator</span><span class="sxs-lookup"><span data-stu-id="a56be-105">RWTexture2DArray::Operator  function</span></span>

<span data-ttu-id="a56be-106">Retorna uma variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="a56be-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="a56be-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a56be-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="a56be-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a56be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a56be-109">*pos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a56be-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a56be-110">Tipo: **uint3**</span><span class="sxs-lookup"><span data-stu-id="a56be-110">Type: **uint3**</span></span>

<span data-ttu-id="a56be-111">A posição do índice.</span><span class="sxs-lookup"><span data-stu-id="a56be-111">The index position.</span></span> <span data-ttu-id="a56be-112">O primeiro e o segundo componentes contêm as coordenadas (x, y).</span><span class="sxs-lookup"><span data-stu-id="a56be-112">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="a56be-113">O terceiro componente indica a fatia de matriz desejada.</span><span class="sxs-lookup"><span data-stu-id="a56be-113">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a56be-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a56be-114">Return value</span></span>

<span data-ttu-id="a56be-115">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="a56be-115">Type: **R**</span></span>

<span data-ttu-id="a56be-116">Uma variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="a56be-116">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="a56be-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a56be-117">Remarks</span></span>

<span data-ttu-id="a56be-118">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="a56be-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a56be-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="a56be-119">Vertex</span></span> | <span data-ttu-id="a56be-120">Envoltória</span><span class="sxs-lookup"><span data-stu-id="a56be-120">Hull</span></span> | <span data-ttu-id="a56be-121">Domínio</span><span class="sxs-lookup"><span data-stu-id="a56be-121">Domain</span></span> | <span data-ttu-id="a56be-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="a56be-122">Geometry</span></span> | <span data-ttu-id="a56be-123">16x16</span><span class="sxs-lookup"><span data-stu-id="a56be-123">Pixel</span></span> | <span data-ttu-id="a56be-124">Computação</span><span class="sxs-lookup"><span data-stu-id="a56be-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="a56be-125">x</span><span class="sxs-lookup"><span data-stu-id="a56be-125">x</span></span>     | <span data-ttu-id="a56be-126">x</span><span class="sxs-lookup"><span data-stu-id="a56be-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a56be-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="a56be-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a56be-128">RWTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="a56be-128">RWTexture2DArray</span></span>](sm5-object-rwtexture2darray.md)
</dt> <dt>

[<span data-ttu-id="a56be-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a56be-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




