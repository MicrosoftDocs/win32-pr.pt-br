---
title: sinal
description: Retorna o sinal de x.
ms.assetid: 3e2e04e8-0ffc-4721-a5d8-1ccfa6ca2a1a
keywords:
- assinar HLSL
topic_type:
- apiref
api_name:
- sign
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fc177e72e116394ffd6241e0616b84c9066a68a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988704"
---
# <a name="sign"></a><span data-ttu-id="b727d-104">sinal</span><span class="sxs-lookup"><span data-stu-id="b727d-104">sign</span></span>

<span data-ttu-id="b727d-105">Retorna o sinal de *x*.</span><span class="sxs-lookup"><span data-stu-id="b727d-105">Returns the sign of *x*.</span></span>



| <span data-ttu-id="b727d-106">sinal de *RET* (*x*)</span><span class="sxs-lookup"><span data-stu-id="b727d-106">*ret* sign(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="b727d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b727d-107">Parameters</span></span>



| <span data-ttu-id="b727d-108">Item</span><span class="sxs-lookup"><span data-stu-id="b727d-108">Item</span></span>                                                   | <span data-ttu-id="b727d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="b727d-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="b727d-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="b727d-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="b727d-111">\[no \] valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="b727d-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="b727d-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b727d-112">Return Value</span></span>

<span data-ttu-id="b727d-113">Retornará-1 se *x* for menor que zero; 0 se *x* for igual a zero; e 1 se *x* for maior que zero.</span><span class="sxs-lookup"><span data-stu-id="b727d-113">Returns -1 if *x* is less than zero; 0 if *x* equals zero; and 1 if *x* is greater than zero.</span></span>

## <a name="type-description"></a><span data-ttu-id="b727d-114">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="b727d-114">Type Description</span></span>



| <span data-ttu-id="b727d-115">Name</span><span class="sxs-lookup"><span data-stu-id="b727d-115">Name</span></span>  | [<span data-ttu-id="b727d-116">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="b727d-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="b727d-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="b727d-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="b727d-118">Tamanho</span><span class="sxs-lookup"><span data-stu-id="b727d-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="b727d-119">*x*</span><span class="sxs-lookup"><span data-stu-id="b727d-119">*x*</span></span>   | <span data-ttu-id="b727d-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="b727d-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="b727d-121">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="b727d-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="b727d-122">any</span><span class="sxs-lookup"><span data-stu-id="b727d-122">any</span></span>                            |
| <span data-ttu-id="b727d-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="b727d-123">*ret*</span></span> | <span data-ttu-id="b727d-124">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="b727d-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="b727d-125">**int**</span><span class="sxs-lookup"><span data-stu-id="b727d-125">**int**</span></span>](/windows/desktop/WinProg/windows-data-types)                                          | <span data-ttu-id="b727d-126">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="b727d-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b727d-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="b727d-127">Minimum Shader Model</span></span>

<span data-ttu-id="b727d-128">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b727d-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b727d-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="b727d-129">Shader Model</span></span>                                                                       | <span data-ttu-id="b727d-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="b727d-130">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="b727d-131">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="b727d-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="b727d-132">sim</span><span class="sxs-lookup"><span data-stu-id="b727d-132">yes</span></span>                         |
| [<span data-ttu-id="b727d-133">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b727d-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="b727d-134">Sim (vs \_ 1 \_ 1 e PS \_ 1 \_ 4)</span><span class="sxs-lookup"><span data-stu-id="b727d-134">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="b727d-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="b727d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b727d-136">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="b727d-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

