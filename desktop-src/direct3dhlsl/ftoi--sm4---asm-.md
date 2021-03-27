---
title: 'ftoi (sm4 – asm) '
description: Ponto flutuante para conversão de inteiro assinado.
ms.assetid: 580AB4A6-0C1C-409B-B2B9-BA1D37772F46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02ce1b506d112a59d3087f59d219557575b8def
ms.sourcegitcommit: 8c658e9872a2173e3dcec94195f9067fbcd85d3d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/17/2020
ms.locfileid: "104294571"
---
# <a name="ftoi-sm4---asm"></a><span data-ttu-id="c753d-103">ftoi (sm4 – asm) </span><span class="sxs-lookup"><span data-stu-id="c753d-103">ftoi (sm4 - asm)</span></span>

<span data-ttu-id="c753d-104">Ponto flutuante para conversão de inteiro assinado.</span><span class="sxs-lookup"><span data-stu-id="c753d-104">Floating point to signed integer conversion.</span></span>

| <span data-ttu-id="c753d-105">ftoi dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="c753d-105">ftoi dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-|

| <span data-ttu-id="c753d-106">Item</span><span class="sxs-lookup"><span data-stu-id="c753d-106">Item</span></span> | <span data-ttu-id="c753d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c753d-107">Description</span></span> |
|-|-|
| <span data-ttu-id="c753d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="c753d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="c753d-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="c753d-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="c753d-110">*dest*  =  [arredondar \_ z](round-z--sm4---asm-.md)(*src0*)</span><span class="sxs-lookup"><span data-stu-id="c753d-110">*dest* = [round\_z](round-z--sm4---asm-.md)(*src0*)</span></span><br/> |
| <span data-ttu-id="c753d-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c753d-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="c753d-112">\[no \] componente a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="c753d-112">\[in\] The component to convert.</span></span><br/> |

## <a name="remarks"></a><span data-ttu-id="c753d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c753d-113">Remarks</span></span>

<span data-ttu-id="c753d-114">A conversão é executada por componente.</span><span class="sxs-lookup"><span data-stu-id="c753d-114">The conversion is performed per component.</span></span> <span data-ttu-id="c753d-115">O arredondamento é sempre executado em direção a zero, seguindo a Convenção C para conversões de float para int. Os aplicativos que exigem uma semântica de arredondamento diferente podem invocar as instruções de **arredondamento** antes da conversão para o número inteiro.</span><span class="sxs-lookup"><span data-stu-id="c753d-115">Rounding is always performed towards zero, following the C convention for casts from float to int. Applications that require different rounding semantics can invoke the **round** instructions before casting to integer.</span></span>

<span data-ttu-id="c753d-116">As entradas são clamped para o intervalo \[ -2147483648.999 f... 2147483647.999 f \] antes da conversão, e os valores Nan de entrada produzem um resultado zero.</span><span class="sxs-lookup"><span data-stu-id="c753d-116">Inputs are clamped to the range \[-2147483648.999f ... 2147483647.999f\] prior to conversion, and input NaN values produce a zero result.</span></span>

<span data-ttu-id="c753d-117">Os modificadores de valor negado e absoluto opcionais são aplicados aos valores de origem antes da conversão.</span><span class="sxs-lookup"><span data-stu-id="c753d-117">Optional negate and absolute value modifiers are applied to the source values before conversion.</span></span>

<span data-ttu-id="c753d-118">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="c753d-118">This instruction applies to the following shader stages:</span></span>

| <span data-ttu-id="c753d-119">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="c753d-119">Vertex Shader</span></span> | <span data-ttu-id="c753d-120">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="c753d-120">Geometry Shader</span></span> | <span data-ttu-id="c753d-121">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="c753d-121">Pixel Shader</span></span> |
|-|-|-|
| <span data-ttu-id="c753d-122">x</span><span class="sxs-lookup"><span data-stu-id="c753d-122">x</span></span> | <span data-ttu-id="c753d-123">x</span><span class="sxs-lookup"><span data-stu-id="c753d-123">x</span></span> | <span data-ttu-id="c753d-124">x</span><span class="sxs-lookup"><span data-stu-id="c753d-124">x</span></span> |

## <a name="minimum-shader-model"></a><span data-ttu-id="c753d-125">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="c753d-125">Minimum Shader Model</span></span>

<span data-ttu-id="c753d-126">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c753d-126">This function is supported in the following shader models.</span></span>

| <span data-ttu-id="c753d-127">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="c753d-127">Shader Model</span></span> | <span data-ttu-id="c753d-128">Com suporte</span><span class="sxs-lookup"><span data-stu-id="c753d-128">Supported</span></span> |
|-|-|
| [<span data-ttu-id="c753d-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c753d-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="c753d-130">sim</span><span class="sxs-lookup"><span data-stu-id="c753d-130">yes</span></span> |
| [<span data-ttu-id="c753d-131">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="c753d-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md) | <span data-ttu-id="c753d-132">sim</span><span class="sxs-lookup"><span data-stu-id="c753d-132">yes</span></span> |
| [<span data-ttu-id="c753d-133">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="c753d-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md) | <span data-ttu-id="c753d-134">sim</span><span class="sxs-lookup"><span data-stu-id="c753d-134">yes</span></span> |
| [<span data-ttu-id="c753d-135">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c753d-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c753d-136">não</span><span class="sxs-lookup"><span data-stu-id="c753d-136">no</span></span> |
| [<span data-ttu-id="c753d-137">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c753d-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c753d-138">não</span><span class="sxs-lookup"><span data-stu-id="c753d-138">no</span></span> |
| [<span data-ttu-id="c753d-139">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c753d-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c753d-140">não</span><span class="sxs-lookup"><span data-stu-id="c753d-140">no</span></span> |

## <a name="related-topics"></a><span data-ttu-id="c753d-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c753d-141">Related topics</span></span>

[<span data-ttu-id="c753d-142">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c753d-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
