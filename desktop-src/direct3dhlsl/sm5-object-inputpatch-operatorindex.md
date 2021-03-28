---
title: 'Função InputPatch:: Operator'
description: 'Retorna o enésimo ponto de controle no patch. | Função InputPatch:: Operator'
ms.assetid: 2c1eda6b-a9c1-40d3-be91-7a2e8f1da9fc
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
ms.openlocfilehash: 5d95cb8adae6e7a91629614e0ae10b4161dbac3f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172706"
---
# <a name="inputpatchoperator--function"></a><span data-ttu-id="0d344-105">Função InputPatch:: Operator</span><span class="sxs-lookup"><span data-stu-id="0d344-105">InputPatch::Operator  function</span></span>

<span data-ttu-id="0d344-106">Retorna o *n*<sup>º</sup> do ponto de controle no patch.</span><span class="sxs-lookup"><span data-stu-id="0d344-106">Returns the *n*<sup>th</sup> control point in the patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d344-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d344-107">Syntax</span></span>

``` syntax
T Operator[](
  in uint n
);
```

## <a name="parameters"></a><span data-ttu-id="0d344-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d344-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d344-109">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="0d344-109">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d344-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="0d344-110">Type: **uint**</span></span>

<span data-ttu-id="0d344-111">O índice de entrada.</span><span class="sxs-lookup"><span data-stu-id="0d344-111">The input index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d344-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0d344-112">Return value</span></span>

<span data-ttu-id="0d344-113">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="0d344-113">Type: **T**</span></span>

<span data-ttu-id="0d344-114">O *n*<sup>º</sup> do ponto de controle.</span><span class="sxs-lookup"><span data-stu-id="0d344-114">The *n*<sup>th</sup> control point.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d344-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d344-115">Remarks</span></span>

<span data-ttu-id="0d344-116">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="0d344-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="0d344-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="0d344-117">Vertex</span></span> | <span data-ttu-id="0d344-118">Envoltória</span><span class="sxs-lookup"><span data-stu-id="0d344-118">Hull</span></span> | <span data-ttu-id="0d344-119">Domínio</span><span class="sxs-lookup"><span data-stu-id="0d344-119">Domain</span></span> | <span data-ttu-id="0d344-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="0d344-120">Geometry</span></span> | <span data-ttu-id="0d344-121">16x16</span><span class="sxs-lookup"><span data-stu-id="0d344-121">Pixel</span></span> | <span data-ttu-id="0d344-122">Computação</span><span class="sxs-lookup"><span data-stu-id="0d344-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="0d344-123">x</span><span class="sxs-lookup"><span data-stu-id="0d344-123">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="0d344-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d344-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d344-125">InputPatch</span><span class="sxs-lookup"><span data-stu-id="0d344-125">InputPatch</span></span>](sm5-object-inputpatch.md)
</dt> <dt>

[<span data-ttu-id="0d344-126">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="0d344-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




