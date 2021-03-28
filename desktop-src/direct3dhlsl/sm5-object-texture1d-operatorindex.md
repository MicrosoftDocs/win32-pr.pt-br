---
title: 'Função Texture1D:: Operator'
description: Retorna uma variável de recurso somente leitura para um Texture1D.
ms.assetid: df54097d-4d1b-496a-a17d-6e9a10cfb996
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
ms.openlocfilehash: 44e5b502c7ae8b766363956920d7922858b4d771
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085081"
---
# <a name="texture1doperator--function"></a><span data-ttu-id="3444d-104">Função Texture1D:: Operator</span><span class="sxs-lookup"><span data-stu-id="3444d-104">Texture1D::Operator  function</span></span>

<span data-ttu-id="3444d-105">Retorna uma variável de recurso somente leitura para um [**Texture1D**](sm5-object-texture1d.md).</span><span class="sxs-lookup"><span data-stu-id="3444d-105">Returns a read-only resource variable for a [**Texture1D**](sm5-object-texture1d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3444d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3444d-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="3444d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3444d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3444d-108">*pos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3444d-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3444d-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="3444d-109">Type: **uint**</span></span>

<span data-ttu-id="3444d-110">A posição do índice.</span><span class="sxs-lookup"><span data-stu-id="3444d-110">The index position.</span></span> <span data-ttu-id="3444d-111">Contém a coordenada x.</span><span class="sxs-lookup"><span data-stu-id="3444d-111">Contains the x-coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3444d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3444d-112">Return value</span></span>

<span data-ttu-id="3444d-113">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="3444d-113">Type: **R**</span></span>

<span data-ttu-id="3444d-114">Uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3444d-114">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="3444d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="3444d-115">Remarks</span></span>

<span data-ttu-id="3444d-116">Esse método sempre acessa o primeiro nível de MIP.</span><span class="sxs-lookup"><span data-stu-id="3444d-116">This method always accesses the first mip level.</span></span> <span data-ttu-id="3444d-117">Para especificar outros níveis de MIP, use o [**MIP. \[ \] \[ \] Operator**](sm5-object-texture1d-mipsoperatorindex.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="3444d-117">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md) instead.</span></span>

<span data-ttu-id="3444d-118">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="3444d-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3444d-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="3444d-119">Vertex</span></span> | <span data-ttu-id="3444d-120">Envoltória</span><span class="sxs-lookup"><span data-stu-id="3444d-120">Hull</span></span> | <span data-ttu-id="3444d-121">Domínio</span><span class="sxs-lookup"><span data-stu-id="3444d-121">Domain</span></span> | <span data-ttu-id="3444d-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="3444d-122">Geometry</span></span> | <span data-ttu-id="3444d-123">16x16</span><span class="sxs-lookup"><span data-stu-id="3444d-123">Pixel</span></span> | <span data-ttu-id="3444d-124">Computação</span><span class="sxs-lookup"><span data-stu-id="3444d-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3444d-125">x</span><span class="sxs-lookup"><span data-stu-id="3444d-125">x</span></span>      | <span data-ttu-id="3444d-126">x</span><span class="sxs-lookup"><span data-stu-id="3444d-126">x</span></span>    | <span data-ttu-id="3444d-127">x</span><span class="sxs-lookup"><span data-stu-id="3444d-127">x</span></span>      | <span data-ttu-id="3444d-128">x</span><span class="sxs-lookup"><span data-stu-id="3444d-128">x</span></span>        | <span data-ttu-id="3444d-129">x</span><span class="sxs-lookup"><span data-stu-id="3444d-129">x</span></span>     | <span data-ttu-id="3444d-130">x</span><span class="sxs-lookup"><span data-stu-id="3444d-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3444d-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="3444d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3444d-132">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3444d-132">Texture1D</span></span>](sm5-object-texture1d.md)
</dt> <dt>

[<span data-ttu-id="3444d-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="3444d-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




