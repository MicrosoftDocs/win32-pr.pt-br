---
title: abs
description: Retorna o valor absoluto do valor especificado.
ms.assetid: 8c4cfd8f-8aac-4db3-8247-ce2bbf501e80
keywords:
- HLSL de ABS
topic_type:
- apiref
api_name:
- abs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1acd1903e1a65a38f5af7549ab52577bc6cba51c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967211"
---
# <a name="abs"></a><span data-ttu-id="c0241-104">abs</span><span class="sxs-lookup"><span data-stu-id="c0241-104">abs</span></span>

<span data-ttu-id="c0241-105">Retorna o valor absoluto do valor especificado.</span><span class="sxs-lookup"><span data-stu-id="c0241-105">Returns the absolute value of the specified value.</span></span>



| <span data-ttu-id="c0241-106">ABS de RET (*x*)</span><span class="sxs-lookup"><span data-stu-id="c0241-106">ret abs(*x*)</span></span> |
|--------------|



 

## <a name="parameters"></a><span data-ttu-id="c0241-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0241-107">Parameters</span></span>



| <span data-ttu-id="c0241-108">Item</span><span class="sxs-lookup"><span data-stu-id="c0241-108">Item</span></span>                                                   | <span data-ttu-id="c0241-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c0241-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="c0241-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="c0241-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="c0241-111">\[no \] valor especificado.</span><span class="sxs-lookup"><span data-stu-id="c0241-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="c0241-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c0241-112">Return Value</span></span>

<span data-ttu-id="c0241-113">O valor absoluto do parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="c0241-113">The absolute value of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="c0241-114">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="c0241-114">Type Description</span></span>



| <span data-ttu-id="c0241-115">Name</span><span class="sxs-lookup"><span data-stu-id="c0241-115">Name</span></span>  | [<span data-ttu-id="c0241-116">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="c0241-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="c0241-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="c0241-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="c0241-118">Tamanho</span><span class="sxs-lookup"><span data-stu-id="c0241-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="c0241-119">*x*</span><span class="sxs-lookup"><span data-stu-id="c0241-119">*x*</span></span>   | <span data-ttu-id="c0241-120">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="c0241-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="c0241-121">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="c0241-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="c0241-122">any</span><span class="sxs-lookup"><span data-stu-id="c0241-122">any</span></span>                            |
| <span data-ttu-id="c0241-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="c0241-123">*ret*</span></span> | <span data-ttu-id="c0241-124">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="c0241-124">same as input *x*</span></span>                                                                                              | <span data-ttu-id="c0241-125">igual ao *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="c0241-125">same as input *x*</span></span>                                                              | <span data-ttu-id="c0241-126">mesmas dimensões como entrada *x*</span><span class="sxs-lookup"><span data-stu-id="c0241-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c0241-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="c0241-127">Minimum Shader Model</span></span>

<span data-ttu-id="c0241-128">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c0241-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c0241-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="c0241-129">Shader Model</span></span>                                                                       | <span data-ttu-id="c0241-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="c0241-130">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="c0241-131">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="c0241-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="c0241-132">sim</span><span class="sxs-lookup"><span data-stu-id="c0241-132">yes</span></span>                   |
| [<span data-ttu-id="c0241-133">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c0241-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="c0241-134">vs \_ 1 \_ 1 e PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="c0241-134">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="c0241-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0241-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0241-136">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="c0241-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

