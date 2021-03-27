---
title: Função EvaluateAttributeAtSample
description: Avalia no local de exemplo indexado.
ms.assetid: b5886004-5960-461d-a0d2-f4c3b0d09d94
keywords:
- HLSL da função EvaluateAttributeAtSample
topic_type:
- apiref
api_name:
- EvaluateAttributeAtSample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b183f86599d08a6892e33c169b938dc09a2b55de
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638449"
---
# <a name="evaluateattributeatsample-function"></a><span data-ttu-id="83b57-104">Função EvaluateAttributeAtSample</span><span class="sxs-lookup"><span data-stu-id="83b57-104">EvaluateAttributeAtSample function</span></span>

<span data-ttu-id="83b57-105">Avalia no local de exemplo indexado.</span><span class="sxs-lookup"><span data-stu-id="83b57-105">Evaluates at the indexed sample location.</span></span>

## <a name="syntax"></a><span data-ttu-id="83b57-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83b57-106">Syntax</span></span>

``` syntax
numeric EvaluateAttributeAtSample(
  in attrib numeric value,
  in uint sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="83b57-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83b57-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83b57-108">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="83b57-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83b57-109">Tipo: **Atrib. numérico**</span><span class="sxs-lookup"><span data-stu-id="83b57-109">Type: **attrib numeric**</span></span>

<span data-ttu-id="83b57-110">O valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="83b57-110">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="83b57-111">*sampleindex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="83b57-111">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83b57-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="83b57-112">Type: **uint**</span></span>

<span data-ttu-id="83b57-113">O local de exemplo.</span><span class="sxs-lookup"><span data-stu-id="83b57-113">The sample location.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83b57-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="83b57-114">Remarks</span></span>

<span data-ttu-id="83b57-115">O modo de interpolação pode ser **linear** ou **linear \_ sem nenhuma \_ perspectiva** na variável.</span><span class="sxs-lookup"><span data-stu-id="83b57-115">Interpolation mode can be **linear** or **linear\_no\_perspective** on the variable.</span></span> <span data-ttu-id="83b57-116">O uso de **centróide** ou de **exemplo** é ignorado.</span><span class="sxs-lookup"><span data-stu-id="83b57-116">Use of **centroid** or **sample** is ignored.</span></span> <span data-ttu-id="83b57-117">Atributos com interpolação de constante também são permitidos; nesse caso, o índice de exemplo é ignorado.</span><span class="sxs-lookup"><span data-stu-id="83b57-117">Attributes with constant interpolation are also allowed, in which case the sample index is ignored.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="83b57-118">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="83b57-118">Minimum Shader Model</span></span>

<span data-ttu-id="83b57-119">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="83b57-119">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="83b57-120">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="83b57-120">Shader Model</span></span>                                                                | <span data-ttu-id="83b57-121">Com suporte</span><span class="sxs-lookup"><span data-stu-id="83b57-121">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="83b57-122">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="83b57-122">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="83b57-123">sim</span><span class="sxs-lookup"><span data-stu-id="83b57-123">yes</span></span>       |



 

<span data-ttu-id="83b57-124">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="83b57-124">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="83b57-125">Vértice</span><span class="sxs-lookup"><span data-stu-id="83b57-125">Vertex</span></span> | <span data-ttu-id="83b57-126">Envoltória</span><span class="sxs-lookup"><span data-stu-id="83b57-126">Hull</span></span> | <span data-ttu-id="83b57-127">Domínio</span><span class="sxs-lookup"><span data-stu-id="83b57-127">Domain</span></span> | <span data-ttu-id="83b57-128">Geometria</span><span class="sxs-lookup"><span data-stu-id="83b57-128">Geometry</span></span> | <span data-ttu-id="83b57-129">16x16</span><span class="sxs-lookup"><span data-stu-id="83b57-129">Pixel</span></span> | <span data-ttu-id="83b57-130">Computação</span><span class="sxs-lookup"><span data-stu-id="83b57-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="83b57-131">x</span><span class="sxs-lookup"><span data-stu-id="83b57-131">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="83b57-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="83b57-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83b57-133">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="83b57-133">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="83b57-134">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="83b57-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




