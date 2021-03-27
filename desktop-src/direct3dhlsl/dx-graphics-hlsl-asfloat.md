---
title: asfloat
description: Interpreta o padrão de bit de x como um número de ponto flutuante.
ms.assetid: 48e1e0cb-8578-4e6d-8c46-2b8b201906c1
keywords:
- asfloat HLSL
topic_type:
- apiref
api_name:
- asfloat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a5701d959fb59519318dd7f2e91b6790f4c0b6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988696"
---
# <a name="asfloat"></a><span data-ttu-id="c72f9-104">asfloat</span><span class="sxs-lookup"><span data-stu-id="c72f9-104">asfloat</span></span>

<span data-ttu-id="c72f9-105">Interpreta o padrão de bit de *x* como um número de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="c72f9-105">Interprets the bit pattern of *x* as a floating-point number.</span></span>



| <span data-ttu-id="c72f9-106">RET asfloat (*x*)</span><span class="sxs-lookup"><span data-stu-id="c72f9-106">ret asfloat(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="c72f9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c72f9-107">Parameters</span></span>



| <span data-ttu-id="c72f9-108">Item</span><span class="sxs-lookup"><span data-stu-id="c72f9-108">Item</span></span>                                                   | <span data-ttu-id="c72f9-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c72f9-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="c72f9-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="c72f9-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="c72f9-111">\[no \] valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="c72f9-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="c72f9-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c72f9-112">Return Value</span></span>

<span data-ttu-id="c72f9-113">A entrada interpretada como um número de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="c72f9-113">The input interpreted as a floating-point number.</span></span>

## <a name="type-description"></a><span data-ttu-id="c72f9-114">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="c72f9-114">Type Description</span></span>



| <span data-ttu-id="c72f9-115">Name</span><span class="sxs-lookup"><span data-stu-id="c72f9-115">Name</span></span>  | [<span data-ttu-id="c72f9-116">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="c72f9-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="c72f9-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="c72f9-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                         | <span data-ttu-id="c72f9-118">Tamanho</span><span class="sxs-lookup"><span data-stu-id="c72f9-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="c72f9-119">*x*</span><span class="sxs-lookup"><span data-stu-id="c72f9-119">*x*</span></span>   | <span data-ttu-id="c72f9-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="c72f9-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="c72f9-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="c72f9-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="c72f9-122">any</span><span class="sxs-lookup"><span data-stu-id="c72f9-122">any</span></span>                            |
| <span data-ttu-id="c72f9-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="c72f9-123">*ret*</span></span> | <span data-ttu-id="c72f9-124">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="c72f9-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="c72f9-125">**barra**</span><span class="sxs-lookup"><span data-stu-id="c72f9-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                                                                                | <span data-ttu-id="c72f9-126">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="c72f9-126">same dimension(s) as input *x*</span></span> |



 

## <a name="function-overloads"></a><span data-ttu-id="c72f9-127">Sobrecargas de função</span><span class="sxs-lookup"><span data-stu-id="c72f9-127">Function Overloads</span></span>

<dl> <span data-ttu-id="c72f9-128">' float <x> asfloat ( <x> valor float); `  
` float <x> asfloat ( <x> valor int); `  
` float <x> asfloat ( <x> valor UINT); '</span><span class="sxs-lookup"><span data-stu-id="c72f9-128">`float<x> asfloat(float<x> value);`  
`float<x> asfloat(int<x> value);`  
`float<x> asfloat(uint<x> value);`</span></span>
</dl>

## <a name="minimum-shader-model"></a><span data-ttu-id="c72f9-129">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="c72f9-129">Minimum Shader Model</span></span>

<span data-ttu-id="c72f9-130">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c72f9-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c72f9-131">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="c72f9-131">Shader Model</span></span>                                                        | <span data-ttu-id="c72f9-132">Com suporte</span><span class="sxs-lookup"><span data-stu-id="c72f9-132">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="c72f9-133">[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="c72f9-133">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="c72f9-134">sim</span><span class="sxs-lookup"><span data-stu-id="c72f9-134">yes</span></span>       |
| [<span data-ttu-id="c72f9-135">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c72f9-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="c72f9-136">não</span><span class="sxs-lookup"><span data-stu-id="c72f9-136">no</span></span>        |
| [<span data-ttu-id="c72f9-137">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c72f9-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="c72f9-138">não</span><span class="sxs-lookup"><span data-stu-id="c72f9-138">no</span></span>        |
| [<span data-ttu-id="c72f9-139">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c72f9-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="c72f9-140">não</span><span class="sxs-lookup"><span data-stu-id="c72f9-140">no</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="c72f9-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="c72f9-141">Remarks</span></span>

<span data-ttu-id="c72f9-142">Os compiladores mais antigos são permitidos incorretamente `asfloat(bool)` , mas observe que não há suporte para entradas bool.</span><span class="sxs-lookup"><span data-stu-id="c72f9-142">Older compilers incorrectly allowed `asfloat(bool)`, but note that bool inputs are not supported.</span></span>

## <a name="see-also"></a><span data-ttu-id="c72f9-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="c72f9-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c72f9-144">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="c72f9-144">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

