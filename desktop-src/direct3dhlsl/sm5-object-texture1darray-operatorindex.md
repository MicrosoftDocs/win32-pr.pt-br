---
title: 'Função Texture1DArray:: Operator'
description: 'Retorna uma variável de recurso somente leitura. | Função Texture1DArray:: Operator'
ms.assetid: 05ec9652-b5dd-41cf-8bef-730c507c5ba4
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
ms.openlocfilehash: 578d778cd1e0e064c435c19fb094feb66f651e05
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968420"
---
# <a name="texture1darrayoperator--function"></a><span data-ttu-id="11eec-105">Função Texture1DArray:: Operator</span><span class="sxs-lookup"><span data-stu-id="11eec-105">Texture1DArray::Operator  function</span></span>

<span data-ttu-id="11eec-106">Retorna uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="11eec-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="11eec-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11eec-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="11eec-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11eec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11eec-109">*pos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="11eec-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11eec-110">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="11eec-110">Type: **uint2**</span></span>

<span data-ttu-id="11eec-111">A posição do índice.</span><span class="sxs-lookup"><span data-stu-id="11eec-111">The index position.</span></span> <span data-ttu-id="11eec-112">O primeiro componente contém a coordenada x.</span><span class="sxs-lookup"><span data-stu-id="11eec-112">The first component contains the x-coordinate.</span></span> <span data-ttu-id="11eec-113">O segundo componente indica a fatia de matriz desejada.</span><span class="sxs-lookup"><span data-stu-id="11eec-113">The second component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11eec-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="11eec-114">Return value</span></span>

<span data-ttu-id="11eec-115">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="11eec-115">Type: **R**</span></span>

<span data-ttu-id="11eec-116">Uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="11eec-116">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="11eec-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="11eec-117">Remarks</span></span>

<span data-ttu-id="11eec-118">Esse método sempre acessa o primeiro nível de MIP.</span><span class="sxs-lookup"><span data-stu-id="11eec-118">This method always accesses the first mip level.</span></span> <span data-ttu-id="11eec-119">Para especificar outros níveis de MIP, use o método [**MIP \[ \] \[ \] . Operator**](sm5-object-texture1darray-mipsoperatorindex.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="11eec-119">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md) method instead.</span></span>

<span data-ttu-id="11eec-120">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="11eec-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="11eec-121">Vértice</span><span class="sxs-lookup"><span data-stu-id="11eec-121">Vertex</span></span> | <span data-ttu-id="11eec-122">Envoltória</span><span class="sxs-lookup"><span data-stu-id="11eec-122">Hull</span></span> | <span data-ttu-id="11eec-123">Domínio</span><span class="sxs-lookup"><span data-stu-id="11eec-123">Domain</span></span> | <span data-ttu-id="11eec-124">Geometria</span><span class="sxs-lookup"><span data-stu-id="11eec-124">Geometry</span></span> | <span data-ttu-id="11eec-125">16x16</span><span class="sxs-lookup"><span data-stu-id="11eec-125">Pixel</span></span> | <span data-ttu-id="11eec-126">Computação</span><span class="sxs-lookup"><span data-stu-id="11eec-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="11eec-127">x</span><span class="sxs-lookup"><span data-stu-id="11eec-127">x</span></span>      | <span data-ttu-id="11eec-128">x</span><span class="sxs-lookup"><span data-stu-id="11eec-128">x</span></span>    | <span data-ttu-id="11eec-129">x</span><span class="sxs-lookup"><span data-stu-id="11eec-129">x</span></span>      | <span data-ttu-id="11eec-130">x</span><span class="sxs-lookup"><span data-stu-id="11eec-130">x</span></span>        | <span data-ttu-id="11eec-131">x</span><span class="sxs-lookup"><span data-stu-id="11eec-131">x</span></span>     | <span data-ttu-id="11eec-132">x</span><span class="sxs-lookup"><span data-stu-id="11eec-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="11eec-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="11eec-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11eec-134">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="11eec-134">Texture1DArray</span></span>](sm5-object-texture1darray.md)
</dt> <dt>

[<span data-ttu-id="11eec-135">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="11eec-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




