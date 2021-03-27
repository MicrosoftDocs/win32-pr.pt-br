---
title: função asuint
description: Reinterpreta o padrão de bit de um valor de 64 bits como dois inteiros de 32 bits não assinados.
ms.assetid: 29671661-4fec-46e5-9b6f-56fba8e1d756
keywords:
- função asuint HLSL
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c54ed89e112482df4a54f35e24a04694e88fa490
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006696"
---
# <a name="asuint-function"></a><span data-ttu-id="e816a-104">função asuint</span><span class="sxs-lookup"><span data-stu-id="e816a-104">asuint function</span></span>

<span data-ttu-id="e816a-105">Reinterpreta o padrão de bit de um valor de 64 bits como dois inteiros de 32 bits não assinados.</span><span class="sxs-lookup"><span data-stu-id="e816a-105">Reinterprets the bit pattern of a 64-bit value as two unsigned 32-bit integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="e816a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e816a-106">Syntax</span></span>

``` syntax
void asuint(
  in  double value,
  out uint lowbits,
  out uint highbits
);
```

## <a name="parameters"></a><span data-ttu-id="e816a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e816a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e816a-108">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="e816a-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e816a-109">Tipo: **duplo**</span><span class="sxs-lookup"><span data-stu-id="e816a-109">Type: **double**</span></span>

<span data-ttu-id="e816a-110">O valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="e816a-110">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="e816a-111">*lowbits* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e816a-111">*lowbits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e816a-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="e816a-112">Type: **uint**</span></span>

<span data-ttu-id="e816a-113">O padrão de *valor* baixo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e816a-113">The low 32-bit pattern of *value*.</span></span>

</dd> <dt>

<span data-ttu-id="e816a-114">*highbits* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e816a-114">*highbits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e816a-115">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="e816a-115">Type: **uint**</span></span>

<span data-ttu-id="e816a-116">O padrão de *valor* alto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e816a-116">The high 32-bit pattern of *value*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e816a-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e816a-117">Return value</span></span>

<span data-ttu-id="e816a-118">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e816a-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e816a-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="e816a-119">Remarks</span></span>

<span data-ttu-id="e816a-120">Essa função é uma versão alternativa do [**asuint**](dx-graphics-hlsl-asuint.md) intrínseco que está disponível em modelos de sombreador anteriores e foi introduzida para o modelo de sombreador 5.</span><span class="sxs-lookup"><span data-stu-id="e816a-120">This function is an alternate version of the [**asuint**](dx-graphics-hlsl-asuint.md) intrinsic that has been available in earlier shader models, and was introduced for Shader Model 5.</span></span> <span data-ttu-id="e816a-121">A função original (reconhecida no compilador HLSL por sua assinatura diferente) permanece disponível para o modelo de sombreador 5.</span><span class="sxs-lookup"><span data-stu-id="e816a-121">The original function (recognized in the HLSL compiler by its different signature) remains available to Shader Model 5.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="e816a-122">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="e816a-122">Minimum Shader Model</span></span>

<span data-ttu-id="e816a-123">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e816a-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e816a-124">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="e816a-124">Shader Model</span></span>                                                                | <span data-ttu-id="e816a-125">Com suporte</span><span class="sxs-lookup"><span data-stu-id="e816a-125">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="e816a-126">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="e816a-126">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="e816a-127">sim</span><span class="sxs-lookup"><span data-stu-id="e816a-127">yes</span></span>       |



 

<span data-ttu-id="e816a-128">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="e816a-128">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="e816a-129">Vértice</span><span class="sxs-lookup"><span data-stu-id="e816a-129">Vertex</span></span> | <span data-ttu-id="e816a-130">Envoltória</span><span class="sxs-lookup"><span data-stu-id="e816a-130">Hull</span></span> | <span data-ttu-id="e816a-131">Domínio</span><span class="sxs-lookup"><span data-stu-id="e816a-131">Domain</span></span> | <span data-ttu-id="e816a-132">Geometria</span><span class="sxs-lookup"><span data-stu-id="e816a-132">Geometry</span></span> | <span data-ttu-id="e816a-133">16x16</span><span class="sxs-lookup"><span data-stu-id="e816a-133">Pixel</span></span> | <span data-ttu-id="e816a-134">Computação</span><span class="sxs-lookup"><span data-stu-id="e816a-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e816a-135">x</span><span class="sxs-lookup"><span data-stu-id="e816a-135">x</span></span>      | <span data-ttu-id="e816a-136">x</span><span class="sxs-lookup"><span data-stu-id="e816a-136">x</span></span>    | <span data-ttu-id="e816a-137">x</span><span class="sxs-lookup"><span data-stu-id="e816a-137">x</span></span>      | <span data-ttu-id="e816a-138">x</span><span class="sxs-lookup"><span data-stu-id="e816a-138">x</span></span>        | <span data-ttu-id="e816a-139">x</span><span class="sxs-lookup"><span data-stu-id="e816a-139">x</span></span>     | <span data-ttu-id="e816a-140">x</span><span class="sxs-lookup"><span data-stu-id="e816a-140">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e816a-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="e816a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e816a-142">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="e816a-142">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="e816a-143">**asuint (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="e816a-143">**asuint (DirectX HLSL)**</span></span>](dx-graphics-hlsl-asuint.md)
</dt> <dt>

[<span data-ttu-id="e816a-144">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e816a-144">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




