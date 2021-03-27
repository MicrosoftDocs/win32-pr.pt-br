---
title: 'Texture1D:: MIPS. Função Operator'
description: Retorna uma variável de recurso somente leitura ou um Texture1D.
ms.assetid: 0b64f0d3-f9a1-474b-b229-d91d18922d5c
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
ms.openlocfilehash: 4713fe20fa52e948113a220969229c413c5dc4d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104294730"
---
# <a name="texture1dmipsoperator----function"></a><span data-ttu-id="e1ebf-104">Texture1D:: MIPS. Função Operator</span><span class="sxs-lookup"><span data-stu-id="e1ebf-104">Texture1D::mips.Operator    function</span></span>

<span data-ttu-id="e1ebf-105">Retorna uma variável de recurso somente leitura ou um [**Texture1D**](sm5-object-texture1d.md).</span><span class="sxs-lookup"><span data-stu-id="e1ebf-105">Returns a read-only resource variable or a [**Texture1D**](sm5-object-texture1d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e1ebf-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1ebf-106">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="e1ebf-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1ebf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1ebf-108">*mipSlice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e1ebf-108">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1ebf-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="e1ebf-109">Type: **uint**</span></span>

<span data-ttu-id="e1ebf-110">O índice de fatia MIP.</span><span class="sxs-lookup"><span data-stu-id="e1ebf-110">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="e1ebf-111">*pos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e1ebf-111">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1ebf-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="e1ebf-112">Type: **uint**</span></span>

<span data-ttu-id="e1ebf-113">A posição do índice.</span><span class="sxs-lookup"><span data-stu-id="e1ebf-113">The index position.</span></span> <span data-ttu-id="e1ebf-114">Contém a coordenada x.</span><span class="sxs-lookup"><span data-stu-id="e1ebf-114">Contains the x-coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1ebf-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e1ebf-115">Return value</span></span>

<span data-ttu-id="e1ebf-116">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="e1ebf-116">Type: **R**</span></span>

<span data-ttu-id="e1ebf-117">Uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="e1ebf-117">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1ebf-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1ebf-118">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="e1ebf-119">Exemplo de uso</span><span class="sxs-lookup"><span data-stu-id="e1ebf-119">Usage Example</span></span>


```
Texture1D<float4> tex;
uint mip = 2;
uint pos = 1234;
float4 f = tex.mips[mip][pos];
      
```



<span data-ttu-id="e1ebf-120">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="e1ebf-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e1ebf-121">Vértice</span><span class="sxs-lookup"><span data-stu-id="e1ebf-121">Vertex</span></span> | <span data-ttu-id="e1ebf-122">Envoltória</span><span class="sxs-lookup"><span data-stu-id="e1ebf-122">Hull</span></span> | <span data-ttu-id="e1ebf-123">Domínio</span><span class="sxs-lookup"><span data-stu-id="e1ebf-123">Domain</span></span> | <span data-ttu-id="e1ebf-124">Geometria</span><span class="sxs-lookup"><span data-stu-id="e1ebf-124">Geometry</span></span> | <span data-ttu-id="e1ebf-125">16x16</span><span class="sxs-lookup"><span data-stu-id="e1ebf-125">Pixel</span></span> | <span data-ttu-id="e1ebf-126">Computação</span><span class="sxs-lookup"><span data-stu-id="e1ebf-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e1ebf-127">x</span><span class="sxs-lookup"><span data-stu-id="e1ebf-127">x</span></span>      | <span data-ttu-id="e1ebf-128">x</span><span class="sxs-lookup"><span data-stu-id="e1ebf-128">x</span></span>    | <span data-ttu-id="e1ebf-129">x</span><span class="sxs-lookup"><span data-stu-id="e1ebf-129">x</span></span>      | <span data-ttu-id="e1ebf-130">x</span><span class="sxs-lookup"><span data-stu-id="e1ebf-130">x</span></span>        | <span data-ttu-id="e1ebf-131">x</span><span class="sxs-lookup"><span data-stu-id="e1ebf-131">x</span></span>     | <span data-ttu-id="e1ebf-132">x</span><span class="sxs-lookup"><span data-stu-id="e1ebf-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e1ebf-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1ebf-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1ebf-134">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1ebf-134">Texture1D</span></span>](sm5-object-texture1d.md)
</dt> <dt>

[<span data-ttu-id="e1ebf-135">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e1ebf-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




