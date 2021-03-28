---
title: 'Texture2D:: MIPS. Função Operator'
description: 'Retorna uma variável de recurso somente leitura. | Texture2D:: MIPS. Função Operator'
ms.assetid: 201996a7-741f-4457-ab77-9cd653f3682b
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
ms.openlocfilehash: 994ede49563b1d4e568769be48a0e60592fe3dde
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968305"
---
# <a name="texture2dmipsoperator----function"></a><span data-ttu-id="df0a8-105">Texture2D:: MIPS. Função Operator</span><span class="sxs-lookup"><span data-stu-id="df0a8-105">Texture2D::mips.Operator    function</span></span>

<span data-ttu-id="df0a8-106">Retorna uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="df0a8-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="df0a8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df0a8-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="df0a8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df0a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df0a8-109">*mipSlice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df0a8-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df0a8-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="df0a8-110">Type: **uint**</span></span>

<span data-ttu-id="df0a8-111">O índice de fatia MIP.</span><span class="sxs-lookup"><span data-stu-id="df0a8-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="df0a8-112">*pos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df0a8-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df0a8-113">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="df0a8-113">Type: **uint2**</span></span>

<span data-ttu-id="df0a8-114">A posição do índice.</span><span class="sxs-lookup"><span data-stu-id="df0a8-114">The index position.</span></span> <span data-ttu-id="df0a8-115">Contém as coordenadas (x, y).</span><span class="sxs-lookup"><span data-stu-id="df0a8-115">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df0a8-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="df0a8-116">Return value</span></span>

<span data-ttu-id="df0a8-117">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="df0a8-117">Type: **R**</span></span>

<span data-ttu-id="df0a8-118">Uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="df0a8-118">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="df0a8-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="df0a8-119">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="df0a8-120">Exemplo de uso</span><span class="sxs-lookup"><span data-stu-id="df0a8-120">Usage Example</span></span>


```
Texture2D<float4> tex;
uint mip = 2;
uint2 pos_xy = {123, 456};
float4 f = tex.mips[mip][pos_xy];
        
```



<span data-ttu-id="df0a8-121">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="df0a8-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="df0a8-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="df0a8-122">Vertex</span></span> | <span data-ttu-id="df0a8-123">Envoltória</span><span class="sxs-lookup"><span data-stu-id="df0a8-123">Hull</span></span> | <span data-ttu-id="df0a8-124">Domínio</span><span class="sxs-lookup"><span data-stu-id="df0a8-124">Domain</span></span> | <span data-ttu-id="df0a8-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="df0a8-125">Geometry</span></span> | <span data-ttu-id="df0a8-126">16x16</span><span class="sxs-lookup"><span data-stu-id="df0a8-126">Pixel</span></span> | <span data-ttu-id="df0a8-127">Computação</span><span class="sxs-lookup"><span data-stu-id="df0a8-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="df0a8-128">x</span><span class="sxs-lookup"><span data-stu-id="df0a8-128">x</span></span>      | <span data-ttu-id="df0a8-129">x</span><span class="sxs-lookup"><span data-stu-id="df0a8-129">x</span></span>    | <span data-ttu-id="df0a8-130">x</span><span class="sxs-lookup"><span data-stu-id="df0a8-130">x</span></span>      | <span data-ttu-id="df0a8-131">x</span><span class="sxs-lookup"><span data-stu-id="df0a8-131">x</span></span>        | <span data-ttu-id="df0a8-132">x</span><span class="sxs-lookup"><span data-stu-id="df0a8-132">x</span></span>     | <span data-ttu-id="df0a8-133">x</span><span class="sxs-lookup"><span data-stu-id="df0a8-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="df0a8-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="df0a8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df0a8-135">Texture2D</span><span class="sxs-lookup"><span data-stu-id="df0a8-135">Texture2D</span></span>](sm5-object-texture2d.md)
</dt> <dt>

[<span data-ttu-id="df0a8-136">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="df0a8-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




