---
title: 'Texture3D:: MIPS. Função Operator'
description: 'Retorna uma variável de recurso somente leitura. | Texture3D:: MIPS. Função Operator'
ms.assetid: d5f6cb3b-4163-44c2-8379-ac8a412b1aa6
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
ms.openlocfilehash: e8f7064459354ec4827ba6d96795e82ccab3800c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172677"
---
# <a name="texture3dmipsoperator----function"></a><span data-ttu-id="68364-105">Texture3D:: MIPS. Função Operator</span><span class="sxs-lookup"><span data-stu-id="68364-105">Texture3D::mips.Operator    function</span></span>

<span data-ttu-id="68364-106">Retorna uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="68364-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="68364-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="68364-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="68364-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="68364-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68364-109">*mipSlice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="68364-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68364-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="68364-110">Type: **uint**</span></span>

<span data-ttu-id="68364-111">O índice de fatia MIP.</span><span class="sxs-lookup"><span data-stu-id="68364-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="68364-112">*pos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="68364-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68364-113">Tipo: **uint3**</span><span class="sxs-lookup"><span data-stu-id="68364-113">Type: **uint3**</span></span>

<span data-ttu-id="68364-114">A posição do índice.</span><span class="sxs-lookup"><span data-stu-id="68364-114">The index position.</span></span> <span data-ttu-id="68364-115">Contém as coordenadas (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="68364-115">Contains the (x, y, z) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68364-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="68364-116">Return value</span></span>

<span data-ttu-id="68364-117">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="68364-117">Type: **R**</span></span>

<span data-ttu-id="68364-118">Uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="68364-118">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="68364-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="68364-119">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="68364-120">Exemplo de uso</span><span class="sxs-lookup"><span data-stu-id="68364-120">Usage Example</span></span>


```
Texture3D<float4> tex;
uint mip = 2;
uint3 pos_xyz = {123, 456, 789};
float4 f = tex.mips[mip][pos_xyz];
        
```



<span data-ttu-id="68364-121">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="68364-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="68364-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="68364-122">Vertex</span></span> | <span data-ttu-id="68364-123">Envoltória</span><span class="sxs-lookup"><span data-stu-id="68364-123">Hull</span></span> | <span data-ttu-id="68364-124">Domínio</span><span class="sxs-lookup"><span data-stu-id="68364-124">Domain</span></span> | <span data-ttu-id="68364-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="68364-125">Geometry</span></span> | <span data-ttu-id="68364-126">16x16</span><span class="sxs-lookup"><span data-stu-id="68364-126">Pixel</span></span> | <span data-ttu-id="68364-127">Computação</span><span class="sxs-lookup"><span data-stu-id="68364-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="68364-128">x</span><span class="sxs-lookup"><span data-stu-id="68364-128">x</span></span>      | <span data-ttu-id="68364-129">x</span><span class="sxs-lookup"><span data-stu-id="68364-129">x</span></span>    | <span data-ttu-id="68364-130">x</span><span class="sxs-lookup"><span data-stu-id="68364-130">x</span></span>      | <span data-ttu-id="68364-131">x</span><span class="sxs-lookup"><span data-stu-id="68364-131">x</span></span>        | <span data-ttu-id="68364-132">x</span><span class="sxs-lookup"><span data-stu-id="68364-132">x</span></span>     | <span data-ttu-id="68364-133">x</span><span class="sxs-lookup"><span data-stu-id="68364-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="68364-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="68364-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68364-135">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68364-135">Texture3D</span></span>](sm5-object-texture3d.md)
</dt> <dt>

[<span data-ttu-id="68364-136">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="68364-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




