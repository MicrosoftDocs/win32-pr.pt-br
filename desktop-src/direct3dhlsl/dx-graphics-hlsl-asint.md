---
title: asent
description: Interpreta o padrão de bit de x como um inteiro.
ms.assetid: e17e0a11-ef52-4b23-94b8-5db0b18aff4d
keywords:
- HLSL de Asen
topic_type:
- apiref
api_name:
- asint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce1b0ca7e1c7b3716be1a3029c5478f96e261ce5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007938"
---
# <a name="asint"></a><span data-ttu-id="2217d-104">asent</span><span class="sxs-lookup"><span data-stu-id="2217d-104">asint</span></span>

<span data-ttu-id="2217d-105">Interpreta o padrão de bit de *x* como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="2217d-105">Interprets the bit pattern of *x* as an integer.</span></span>



| <span data-ttu-id="2217d-106">RET asent (*x*)</span><span class="sxs-lookup"><span data-stu-id="2217d-106">ret asint(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="2217d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2217d-107">Parameters</span></span>



| <span data-ttu-id="2217d-108">Item</span><span class="sxs-lookup"><span data-stu-id="2217d-108">Item</span></span>                                                   | <span data-ttu-id="2217d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="2217d-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="2217d-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="2217d-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="2217d-111">\[no \] valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="2217d-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="2217d-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="2217d-112">Return Value</span></span>

<span data-ttu-id="2217d-113">A entrada interpretada como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="2217d-113">The input interpreted as an integer.</span></span>

## <a name="type-description"></a><span data-ttu-id="2217d-114">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="2217d-114">Type Description</span></span>



| <span data-ttu-id="2217d-115">Name</span><span class="sxs-lookup"><span data-stu-id="2217d-115">Name</span></span>  | [<span data-ttu-id="2217d-116">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="2217d-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="2217d-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="2217d-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                  | <span data-ttu-id="2217d-118">Tamanho</span><span class="sxs-lookup"><span data-stu-id="2217d-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="2217d-119">*x*</span><span class="sxs-lookup"><span data-stu-id="2217d-119">*x*</span></span>   | <span data-ttu-id="2217d-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="2217d-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="2217d-121">[**float**](/windows/desktop/WinProg/windows-data-types), [ **uint**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="2217d-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="2217d-122">any</span><span class="sxs-lookup"><span data-stu-id="2217d-122">any</span></span>                            |
| <span data-ttu-id="2217d-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="2217d-123">*ret*</span></span> | <span data-ttu-id="2217d-124">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="2217d-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="2217d-125">**int**</span><span class="sxs-lookup"><span data-stu-id="2217d-125">**int**</span></span>](/windows/desktop/WinProg/windows-data-types)                                           | <span data-ttu-id="2217d-126">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="2217d-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2217d-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="2217d-127">Minimum Shader Model</span></span>

<span data-ttu-id="2217d-128">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="2217d-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2217d-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="2217d-129">Shader Model</span></span>                                                        | <span data-ttu-id="2217d-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="2217d-130">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="2217d-131">[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="2217d-131">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="2217d-132">sim</span><span class="sxs-lookup"><span data-stu-id="2217d-132">yes</span></span>       |
| [<span data-ttu-id="2217d-133">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2217d-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="2217d-134">não</span><span class="sxs-lookup"><span data-stu-id="2217d-134">no</span></span>        |
| [<span data-ttu-id="2217d-135">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2217d-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="2217d-136">não</span><span class="sxs-lookup"><span data-stu-id="2217d-136">no</span></span>        |
| [<span data-ttu-id="2217d-137">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2217d-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="2217d-138">não</span><span class="sxs-lookup"><span data-stu-id="2217d-138">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="2217d-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="2217d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2217d-140">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="2217d-140">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

