---
title: asuint
description: Interpreta o padrão de bit de x como um inteiro sem sinal.
ms.assetid: 8401001d-f9ee-43da-9756-f311e9f2bb20
keywords:
- HLSL asuint
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1a2d351eb36c6910790e2dceb94e3a97951ad850
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967212"
---
# <a name="asuint"></a><span data-ttu-id="07abc-104">asuint</span><span class="sxs-lookup"><span data-stu-id="07abc-104">asuint</span></span>

<span data-ttu-id="07abc-105">Interpreta o padrão de bit de *x* como um inteiro sem sinal.</span><span class="sxs-lookup"><span data-stu-id="07abc-105">Interprets the bit pattern of *x* as an unsigned integer.</span></span>



| <span data-ttu-id="07abc-106">RET asuint (*x*)</span><span class="sxs-lookup"><span data-stu-id="07abc-106">ret asuint(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="07abc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07abc-107">Parameters</span></span>



| <span data-ttu-id="07abc-108">Item</span><span class="sxs-lookup"><span data-stu-id="07abc-108">Item</span></span>                                                   | <span data-ttu-id="07abc-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="07abc-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="07abc-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="07abc-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="07abc-111">\[no \] valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="07abc-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="07abc-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="07abc-112">Return Value</span></span>

<span data-ttu-id="07abc-113">A entrada interpretada como um inteiro não assinado.</span><span class="sxs-lookup"><span data-stu-id="07abc-113">The input interpreted as an unsigned integer.</span></span>

## <a name="type-description"></a><span data-ttu-id="07abc-114">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="07abc-114">Type Description</span></span>



| <span data-ttu-id="07abc-115">Name</span><span class="sxs-lookup"><span data-stu-id="07abc-115">Name</span></span>  | [<span data-ttu-id="07abc-116">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="07abc-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="07abc-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="07abc-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="07abc-118">Tamanho</span><span class="sxs-lookup"><span data-stu-id="07abc-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="07abc-119">*x*</span><span class="sxs-lookup"><span data-stu-id="07abc-119">*x*</span></span>   | <span data-ttu-id="07abc-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="07abc-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="07abc-121">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="07abc-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="07abc-122">any</span><span class="sxs-lookup"><span data-stu-id="07abc-122">any</span></span>                            |
| <span data-ttu-id="07abc-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="07abc-123">*ret*</span></span> | <span data-ttu-id="07abc-124">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="07abc-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="07abc-125">**uint**</span><span class="sxs-lookup"><span data-stu-id="07abc-125">**uint**</span></span>](/windows/desktop/WinProg/windows-data-types)                                         | <span data-ttu-id="07abc-126">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="07abc-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="07abc-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="07abc-127">Minimum Shader Model</span></span>

<span data-ttu-id="07abc-128">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="07abc-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="07abc-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="07abc-129">Shader Model</span></span>                                                        | <span data-ttu-id="07abc-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="07abc-130">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="07abc-131">[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="07abc-131">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="07abc-132">sim</span><span class="sxs-lookup"><span data-stu-id="07abc-132">yes</span></span>       |
| [<span data-ttu-id="07abc-133">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="07abc-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="07abc-134">não</span><span class="sxs-lookup"><span data-stu-id="07abc-134">no</span></span>        |
| [<span data-ttu-id="07abc-135">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="07abc-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="07abc-136">não</span><span class="sxs-lookup"><span data-stu-id="07abc-136">no</span></span>        |
| [<span data-ttu-id="07abc-137">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="07abc-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="07abc-138">não</span><span class="sxs-lookup"><span data-stu-id="07abc-138">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="07abc-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="07abc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07abc-140">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="07abc-140">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

