---
title: 'Texture1DArray:: MIPS. Função Operator'
description: 'Retorna uma variável de recurso somente leitura. | Texture1DArray:: MIPS. Função Operator'
ms.assetid: b8f2ef78-4b50-4051-a00f-5b81cd77d1e0
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
ms.openlocfilehash: cbe2d1116839cede8dda69f1b0b8cf9a049595e9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104012026"
---
# <a name="texture1darraymipsoperator----function"></a><span data-ttu-id="75b6a-105">Texture1DArray:: MIPS. Função Operator</span><span class="sxs-lookup"><span data-stu-id="75b6a-105">Texture1DArray::mips.Operator    function</span></span>

<span data-ttu-id="75b6a-106">Retorna uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="75b6a-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="75b6a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75b6a-107">Syntax</span></span>

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="75b6a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75b6a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75b6a-109">*mipSlice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75b6a-109">*mipSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75b6a-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="75b6a-110">Type: **uint**</span></span>

<span data-ttu-id="75b6a-111">O índice de fatia MIP.</span><span class="sxs-lookup"><span data-stu-id="75b6a-111">The mip slice index.</span></span>

</dd> <dt>

<span data-ttu-id="75b6a-112">*pos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75b6a-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75b6a-113">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="75b6a-113">Type: **uint2**</span></span>

<span data-ttu-id="75b6a-114">A posição do índice.</span><span class="sxs-lookup"><span data-stu-id="75b6a-114">The index position.</span></span> <span data-ttu-id="75b6a-115">O primeiro componente contém a coordenada x.</span><span class="sxs-lookup"><span data-stu-id="75b6a-115">The first component contains the x-coordinate.</span></span> <span data-ttu-id="75b6a-116">O segundo componente indica a fatia de matriz desejada.</span><span class="sxs-lookup"><span data-stu-id="75b6a-116">The second component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75b6a-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="75b6a-117">Return value</span></span>

<span data-ttu-id="75b6a-118">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="75b6a-118">Type: **R**</span></span>

<span data-ttu-id="75b6a-119">Uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="75b6a-119">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="75b6a-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="75b6a-120">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="75b6a-121">Exemplo de uso</span><span class="sxs-lookup"><span data-stu-id="75b6a-121">Usage Example</span></span>


```
Texture1DArray<float4> tex;
uint mip = 2;
uint2 pos_x_and_array = {1234, 3};
float4 f = tex.mips[mip][pos_x_and_array];        
        
```



<span data-ttu-id="75b6a-122">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="75b6a-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="75b6a-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="75b6a-123">Vertex</span></span> | <span data-ttu-id="75b6a-124">Envoltória</span><span class="sxs-lookup"><span data-stu-id="75b6a-124">Hull</span></span> | <span data-ttu-id="75b6a-125">Domínio</span><span class="sxs-lookup"><span data-stu-id="75b6a-125">Domain</span></span> | <span data-ttu-id="75b6a-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="75b6a-126">Geometry</span></span> | <span data-ttu-id="75b6a-127">16x16</span><span class="sxs-lookup"><span data-stu-id="75b6a-127">Pixel</span></span> | <span data-ttu-id="75b6a-128">Computação</span><span class="sxs-lookup"><span data-stu-id="75b6a-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="75b6a-129">x</span><span class="sxs-lookup"><span data-stu-id="75b6a-129">x</span></span>      | <span data-ttu-id="75b6a-130">x</span><span class="sxs-lookup"><span data-stu-id="75b6a-130">x</span></span>    | <span data-ttu-id="75b6a-131">x</span><span class="sxs-lookup"><span data-stu-id="75b6a-131">x</span></span>      | <span data-ttu-id="75b6a-132">x</span><span class="sxs-lookup"><span data-stu-id="75b6a-132">x</span></span>        | <span data-ttu-id="75b6a-133">x</span><span class="sxs-lookup"><span data-stu-id="75b6a-133">x</span></span>     | <span data-ttu-id="75b6a-134">x</span><span class="sxs-lookup"><span data-stu-id="75b6a-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="75b6a-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="75b6a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75b6a-136">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="75b6a-136">Texture1DArray</span></span>](sm5-object-texture1darray.md)
</dt> <dt>

[<span data-ttu-id="75b6a-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="75b6a-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




