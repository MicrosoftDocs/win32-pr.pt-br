---
title: Função EvaluateAttributeAtCentroid
description: Avalia no pixel centróide.
ms.assetid: 6735b3f4-765f-4cd9-9f38-326a52709021
keywords:
- HLSL da função EvaluateAttributeAtCentroid
topic_type:
- apiref
api_name:
- EvaluateAttributeAtCentroid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ee95c7f2f202dfd0065e5e9c30003cc46fd29281
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364872"
---
# <a name="evaluateattributeatcentroid-function"></a><span data-ttu-id="ec9b4-104">Função EvaluateAttributeAtCentroid</span><span class="sxs-lookup"><span data-stu-id="ec9b4-104">EvaluateAttributeAtCentroid function</span></span>

<span data-ttu-id="ec9b4-105">Avalia no pixel centróide.</span><span class="sxs-lookup"><span data-stu-id="ec9b4-105">Evaluates at the pixel centroid.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec9b4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec9b4-106">Syntax</span></span>

``` syntax
numeric EvaluateAttributeAtCentroid(
  in attrib numeric value
);
```

## <a name="parameters"></a><span data-ttu-id="ec9b4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec9b4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec9b4-108">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="ec9b4-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec9b4-109">Tipo: **Atrib. numérico**</span><span class="sxs-lookup"><span data-stu-id="ec9b4-109">Type: **attrib numeric**</span></span>

<span data-ttu-id="ec9b4-110">O valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="ec9b4-110">The input value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec9b4-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec9b4-111">Remarks</span></span>

<span data-ttu-id="ec9b4-112">O modo de interpolação pode ser **linear** ou **linear \_ sem nenhuma \_ perspectiva** na variável.</span><span class="sxs-lookup"><span data-stu-id="ec9b4-112">Interpolation mode can be **linear** or **linear\_no\_perspective** on the variable.</span></span> <span data-ttu-id="ec9b4-113">O uso de **centróide** ou de **exemplo** é ignorado.</span><span class="sxs-lookup"><span data-stu-id="ec9b4-113">Use of **centroid** or **sample** is ignored.</span></span> <span data-ttu-id="ec9b4-114">Atributos com interpolação de constante também são permitidos; nesse caso, o índice de exemplo é ignorado.</span><span class="sxs-lookup"><span data-stu-id="ec9b4-114">Attributes with constant interpolation are also allowed, in which case the sample index is ignored.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="ec9b4-115">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="ec9b4-115">Minimum Shader Model</span></span>

<span data-ttu-id="ec9b4-116">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ec9b4-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ec9b4-117">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="ec9b4-117">Shader Model</span></span>                                                                | <span data-ttu-id="ec9b4-118">Com suporte</span><span class="sxs-lookup"><span data-stu-id="ec9b4-118">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="ec9b4-119">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="ec9b4-119">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="ec9b4-120">sim</span><span class="sxs-lookup"><span data-stu-id="ec9b4-120">yes</span></span>       |



 

<span data-ttu-id="ec9b4-121">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="ec9b4-121">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="ec9b4-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="ec9b4-122">Vertex</span></span> | <span data-ttu-id="ec9b4-123">Envoltória</span><span class="sxs-lookup"><span data-stu-id="ec9b4-123">Hull</span></span> | <span data-ttu-id="ec9b4-124">Domínio</span><span class="sxs-lookup"><span data-stu-id="ec9b4-124">Domain</span></span> | <span data-ttu-id="ec9b4-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="ec9b4-125">Geometry</span></span> | <span data-ttu-id="ec9b4-126">16x16</span><span class="sxs-lookup"><span data-stu-id="ec9b4-126">Pixel</span></span> | <span data-ttu-id="ec9b4-127">Computação</span><span class="sxs-lookup"><span data-stu-id="ec9b4-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="ec9b4-128">x</span><span class="sxs-lookup"><span data-stu-id="ec9b4-128">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="ec9b4-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec9b4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec9b4-130">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="ec9b4-130">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="ec9b4-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="ec9b4-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




