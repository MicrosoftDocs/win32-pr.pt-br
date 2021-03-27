---
title: modf (Corecrt \_ Math. h)
description: Divide o valor x em partes fracionárias e de inteiros, cada qual com o mesmo sinal de x.
ms.assetid: 0cac1cf3-f0da-4b0a-ba30-4af5d65b04b2
keywords:
- modf HLSL
topic_type:
- apiref
api_name:
- modf
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5079549e70414f8237fd33a5e263dd8f17dcb9e3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930637"
---
# <a name="modf"></a><span data-ttu-id="7f1cc-104">modf</span><span class="sxs-lookup"><span data-stu-id="7f1cc-104">modf</span></span>

<span data-ttu-id="7f1cc-105">Divide o valor x em partes fracionárias e de inteiros, cada qual com o mesmo sinal de x.</span><span class="sxs-lookup"><span data-stu-id="7f1cc-105">Splits the value x into fractional and integer parts, each of which has the same sign as x.</span></span>



| <span data-ttu-id="7f1cc-106">RET modf (x, out IP)</span><span class="sxs-lookup"><span data-stu-id="7f1cc-106">ret modf(x, out ip)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="7f1cc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f1cc-107">Parameters</span></span>



| <span data-ttu-id="7f1cc-108">Item</span><span class="sxs-lookup"><span data-stu-id="7f1cc-108">Item</span></span>                                                      | <span data-ttu-id="7f1cc-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f1cc-109">Description</span></span>                                    |
|-----------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="7f1cc-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="7f1cc-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/>    | <span data-ttu-id="7f1cc-111">\[no \] valor de entrada x.</span><span class="sxs-lookup"><span data-stu-id="7f1cc-111">\[in\] The x input value.</span></span><br/>           |
| <span data-ttu-id="7f1cc-112"><span id="ip"></span><span id="IP"></span>*IP*</span><span class="sxs-lookup"><span data-stu-id="7f1cc-112"><span id="ip"></span><span id="IP"></span>*ip*</span></span><br/> | <span data-ttu-id="7f1cc-113">\[\]a parte inteira de *x*.</span><span class="sxs-lookup"><span data-stu-id="7f1cc-113">\[out\] The integer portion of *x*.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="7f1cc-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="7f1cc-114">Return Value</span></span>

<span data-ttu-id="7f1cc-115">A porção fracionária de x.</span><span class="sxs-lookup"><span data-stu-id="7f1cc-115">The signed-fractional portion of x.</span></span>

## <a name="type-description"></a><span data-ttu-id="7f1cc-116">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="7f1cc-116">Type Description</span></span>



| <span data-ttu-id="7f1cc-117">Name</span><span class="sxs-lookup"><span data-stu-id="7f1cc-117">Name</span></span> | <span data-ttu-id="7f1cc-118">Entrada/saída</span><span class="sxs-lookup"><span data-stu-id="7f1cc-118">In/Out</span></span> | [<span data-ttu-id="7f1cc-119">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="7f1cc-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="7f1cc-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="7f1cc-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="7f1cc-121">Tamanho</span><span class="sxs-lookup"><span data-stu-id="7f1cc-121">Size</span></span>                         |
|------|--------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="7f1cc-122">x</span><span class="sxs-lookup"><span data-stu-id="7f1cc-122">x</span></span>    | <span data-ttu-id="7f1cc-123">in</span><span class="sxs-lookup"><span data-stu-id="7f1cc-123">in</span></span>     | <span data-ttu-id="7f1cc-124">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="7f1cc-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="7f1cc-125">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="7f1cc-125">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="7f1cc-126">any</span><span class="sxs-lookup"><span data-stu-id="7f1cc-126">any</span></span>                          |
| <span data-ttu-id="7f1cc-127">IP</span><span class="sxs-lookup"><span data-stu-id="7f1cc-127">ip</span></span>   | <span data-ttu-id="7f1cc-128">out</span><span class="sxs-lookup"><span data-stu-id="7f1cc-128">out</span></span>    | <span data-ttu-id="7f1cc-129">igual ao x de entrada</span><span class="sxs-lookup"><span data-stu-id="7f1cc-129">same as input x</span></span>                                                                                                | <span data-ttu-id="7f1cc-130">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="7f1cc-130">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="7f1cc-131">mesmas dimensões como entrada x</span><span class="sxs-lookup"><span data-stu-id="7f1cc-131">same dimension(s) as input x</span></span> |
| <span data-ttu-id="7f1cc-132">RET</span><span class="sxs-lookup"><span data-stu-id="7f1cc-132">ret</span></span>  | <span data-ttu-id="7f1cc-133">out</span><span class="sxs-lookup"><span data-stu-id="7f1cc-133">out</span></span>    | <span data-ttu-id="7f1cc-134">igual ao x de entrada</span><span class="sxs-lookup"><span data-stu-id="7f1cc-134">same as input x</span></span>                                                                                                | <span data-ttu-id="7f1cc-135">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="7f1cc-135">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="7f1cc-136">mesmas dimensões como entrada x</span><span class="sxs-lookup"><span data-stu-id="7f1cc-136">same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7f1cc-137">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="7f1cc-137">Minimum Shader Model</span></span>

<span data-ttu-id="7f1cc-138">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7f1cc-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7f1cc-139">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="7f1cc-139">Shader Model</span></span>                                                                       | <span data-ttu-id="7f1cc-140">Com suporte</span><span class="sxs-lookup"><span data-stu-id="7f1cc-140">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="7f1cc-141">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="7f1cc-141">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="7f1cc-142">sim</span><span class="sxs-lookup"><span data-stu-id="7f1cc-142">yes</span></span>                 |
| [<span data-ttu-id="7f1cc-143">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7f1cc-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="7f1cc-144">Sim ( \_ apenas vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="7f1cc-144">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="7f1cc-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f1cc-145">Requirements</span></span>



| <span data-ttu-id="7f1cc-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f1cc-146">Requirement</span></span> | <span data-ttu-id="7f1cc-147">Valor</span><span class="sxs-lookup"><span data-stu-id="7f1cc-147">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f1cc-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7f1cc-148">Header</span></span><br/> | <dl> <span data-ttu-id="7f1cc-149"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f1cc-149"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f1cc-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f1cc-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f1cc-151">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="7f1cc-151">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

