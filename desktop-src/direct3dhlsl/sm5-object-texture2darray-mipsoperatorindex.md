---
title: 'Texture2DArray:: MIPS. Função Operator'
description: 'Retorna uma variável de recurso somente leitura. | Texture2DArray:: MIPS. Função Operator'
ms.assetid: 66639bf6-74dd-4c69-9cc1-74cc9314de57
keywords:
- seqüencia. Função Operator HLSL
topic_type:
- apiref
api_name:
- mips.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17f24dd54768f3583f508527b7e03f72399bf98e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103663931"
---
# <a name="texture2darraymipsoperator----function"></a><span data-ttu-id="db83e-105">Texture2DArray:: MIPS. Função Operator</span><span class="sxs-lookup"><span data-stu-id="db83e-105">Texture2DArray::mips.Operator    function</span></span>

<span data-ttu-id="db83e-106">Retorna uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="db83e-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="db83e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db83e-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="db83e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db83e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db83e-109">*mipSlice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="db83e-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db83e-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="db83e-110">Type: **uint**</span></span>

<span data-ttu-id="db83e-111">O índice de fatia MIP.</span><span class="sxs-lookup"><span data-stu-id="db83e-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="db83e-112">*pos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="db83e-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db83e-113">Tipo: **uint3**</span><span class="sxs-lookup"><span data-stu-id="db83e-113">Type: **uint3**</span></span>

<span data-ttu-id="db83e-114">A posição do índice.</span><span class="sxs-lookup"><span data-stu-id="db83e-114">The index position.</span></span> <span data-ttu-id="db83e-115">O primeiro e o segundo componentes contêm as coordenadas (x, y).</span><span class="sxs-lookup"><span data-stu-id="db83e-115">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="db83e-116">O terceiro componente indica a fatia de matriz desejada.</span><span class="sxs-lookup"><span data-stu-id="db83e-116">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db83e-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="db83e-117">Return value</span></span>

<span data-ttu-id="db83e-118">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="db83e-118">Type: **R**</span></span>

<span data-ttu-id="db83e-119">Uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="db83e-119">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="db83e-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="db83e-120">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="db83e-121">Exemplo de uso</span><span class="sxs-lookup"><span data-stu-id="db83e-121">Usage Example</span></span>


```
Texture2DArray<float4> tex;
uint mip = 2;
uint2 pos_xy_and_array = {123, 456, 3};
float4 f = tex.mips[mip][pos_xy_and_array];
        
```



<span data-ttu-id="db83e-122">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="db83e-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="db83e-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="db83e-123">Vertex</span></span> | <span data-ttu-id="db83e-124">Envoltória</span><span class="sxs-lookup"><span data-stu-id="db83e-124">Hull</span></span> | <span data-ttu-id="db83e-125">Domínio</span><span class="sxs-lookup"><span data-stu-id="db83e-125">Domain</span></span> | <span data-ttu-id="db83e-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="db83e-126">Geometry</span></span> | <span data-ttu-id="db83e-127">16x16</span><span class="sxs-lookup"><span data-stu-id="db83e-127">Pixel</span></span> | <span data-ttu-id="db83e-128">Computação</span><span class="sxs-lookup"><span data-stu-id="db83e-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="db83e-129">x</span><span class="sxs-lookup"><span data-stu-id="db83e-129">x</span></span>      | <span data-ttu-id="db83e-130">x</span><span class="sxs-lookup"><span data-stu-id="db83e-130">x</span></span>    | <span data-ttu-id="db83e-131">x</span><span class="sxs-lookup"><span data-stu-id="db83e-131">x</span></span>      | <span data-ttu-id="db83e-132">x</span><span class="sxs-lookup"><span data-stu-id="db83e-132">x</span></span>        | <span data-ttu-id="db83e-133">x</span><span class="sxs-lookup"><span data-stu-id="db83e-133">x</span></span>     | <span data-ttu-id="db83e-134">x</span><span class="sxs-lookup"><span data-stu-id="db83e-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="db83e-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="db83e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db83e-136">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="db83e-136">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> <dt>

[<span data-ttu-id="db83e-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="db83e-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




