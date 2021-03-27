---
title: 'Função OutputPatch:: Operator'
description: 'Retorna o enésimo ponto de controle no patch. | Função OutputPatch:: Operator'
ms.assetid: 3ac15fe8-8bab-46a2-8826-61ade927c99e
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
ms.openlocfilehash: 8194713dc4967151991fab95000fa70c40122f26
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298191"
---
# <a name="outputpatchoperator--function"></a><span data-ttu-id="d5e91-105">Função OutputPatch:: Operator</span><span class="sxs-lookup"><span data-stu-id="d5e91-105">OutputPatch::Operator  function</span></span>

<span data-ttu-id="d5e91-106">Retorna o *n*<sup>º</sup> do ponto de controle no patch.</span><span class="sxs-lookup"><span data-stu-id="d5e91-106">Returns the *n*<sup>th</sup> control point in the patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5e91-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5e91-107">Syntax</span></span>

``` syntax
T Operator[](
  in uint n
);
```

## <a name="parameters"></a><span data-ttu-id="d5e91-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5e91-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5e91-109">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="d5e91-109">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5e91-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="d5e91-110">Type: **uint**</span></span>

<span data-ttu-id="d5e91-111">O índice de entrada.</span><span class="sxs-lookup"><span data-stu-id="d5e91-111">The input index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5e91-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d5e91-112">Return value</span></span>

<span data-ttu-id="d5e91-113">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="d5e91-113">Type: **T**</span></span>

<span data-ttu-id="d5e91-114">O *n*<sup>º</sup> do ponto de controle.</span><span class="sxs-lookup"><span data-stu-id="d5e91-114">The *n*<sup>th</sup> control point.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5e91-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5e91-115">Remarks</span></span>

<span data-ttu-id="d5e91-116">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="d5e91-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d5e91-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="d5e91-117">Vertex</span></span> | <span data-ttu-id="d5e91-118">Envoltória</span><span class="sxs-lookup"><span data-stu-id="d5e91-118">Hull</span></span> | <span data-ttu-id="d5e91-119">Domínio</span><span class="sxs-lookup"><span data-stu-id="d5e91-119">Domain</span></span> | <span data-ttu-id="d5e91-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="d5e91-120">Geometry</span></span> | <span data-ttu-id="d5e91-121">16x16</span><span class="sxs-lookup"><span data-stu-id="d5e91-121">Pixel</span></span> | <span data-ttu-id="d5e91-122">Computação</span><span class="sxs-lookup"><span data-stu-id="d5e91-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="d5e91-123">x</span><span class="sxs-lookup"><span data-stu-id="d5e91-123">x</span></span>    | <span data-ttu-id="d5e91-124">x</span><span class="sxs-lookup"><span data-stu-id="d5e91-124">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="d5e91-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5e91-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5e91-126">OutputPatch</span><span class="sxs-lookup"><span data-stu-id="d5e91-126">OutputPatch</span></span>](sm5-object-outputpatch.md)
</dt> <dt>

[<span data-ttu-id="d5e91-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="d5e91-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




