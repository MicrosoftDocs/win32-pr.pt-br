---
title: max
description: Seleciona o maior x e y.
ms.assetid: 08e17a0c-6d44-49ea-b613-bd262534522c
keywords:
- HLSL máx.
topic_type:
- apiref
api_name:
- max
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a40ccb32bb2c2fcd7ca7342b9d7d4d143688102
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366453"
---
# <a name="max"></a><span data-ttu-id="403ae-104">max</span><span class="sxs-lookup"><span data-stu-id="403ae-104">max</span></span>

<span data-ttu-id="403ae-105">Seleciona o maior x e y.</span><span class="sxs-lookup"><span data-stu-id="403ae-105">Selects the greater of x and y.</span></span>



| <span data-ttu-id="403ae-106">RET máx. (x, y)</span><span class="sxs-lookup"><span data-stu-id="403ae-106">ret max(x, y)</span></span> |
|---------------|



 

## <a name="parameters"></a><span data-ttu-id="403ae-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="403ae-107">Parameters</span></span>



| <span data-ttu-id="403ae-108">Item</span><span class="sxs-lookup"><span data-stu-id="403ae-108">Item</span></span>                                                   | <span data-ttu-id="403ae-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="403ae-109">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="403ae-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="403ae-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="403ae-111">\[no \] valor de entrada x.</span><span class="sxs-lookup"><span data-stu-id="403ae-111">\[in\] The x input value.</span></span><br/> |
| <span data-ttu-id="403ae-112"><span id="y"></span><span id="Y"></span>*Iar*</span><span class="sxs-lookup"><span data-stu-id="403ae-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="403ae-113">\[no \] valor de entrada de y.</span><span class="sxs-lookup"><span data-stu-id="403ae-113">\[in\] The y input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="403ae-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="403ae-114">Return Value</span></span>

<span data-ttu-id="403ae-115">O parâmetro *x* ou *y* , o que for o maior valor.</span><span class="sxs-lookup"><span data-stu-id="403ae-115">The *x* or *y* parameter, whichever is the largest value.</span></span>


## <a name="remarks"></a><span data-ttu-id="403ae-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="403ae-116">Remarks</span></span>

<span data-ttu-id="403ae-117">Os desnormals são tratados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="403ae-117">Denormals are handled as follows:</span></span>

| <span data-ttu-id="403ae-118">src0 src1-></span><span class="sxs-lookup"><span data-stu-id="403ae-118">src0 src1-></span></span> | <span data-ttu-id="403ae-119">-inf</span><span class="sxs-lookup"><span data-stu-id="403ae-119">-inf</span></span> | <span data-ttu-id="403ae-120">F</span><span class="sxs-lookup"><span data-stu-id="403ae-120">F</span></span>             | <span data-ttu-id="403ae-121">+inf</span><span class="sxs-lookup"><span data-stu-id="403ae-121">+inf</span></span> | <span data-ttu-id="403ae-122">NAN</span><span class="sxs-lookup"><span data-stu-id="403ae-122">NAN</span></span>  |
|-------------|------|---------------|------|------|
| <span data-ttu-id="403ae-123">-inf</span><span class="sxs-lookup"><span data-stu-id="403ae-123">-inf</span></span>        | <span data-ttu-id="403ae-124">-inf</span><span class="sxs-lookup"><span data-stu-id="403ae-124">-inf</span></span> | <span data-ttu-id="403ae-125">src1</span><span class="sxs-lookup"><span data-stu-id="403ae-125">src1</span></span>          | <span data-ttu-id="403ae-126">+inf</span><span class="sxs-lookup"><span data-stu-id="403ae-126">+inf</span></span> | <span data-ttu-id="403ae-127">-inf</span><span class="sxs-lookup"><span data-stu-id="403ae-127">-inf</span></span> |
| <span data-ttu-id="403ae-128">F</span><span class="sxs-lookup"><span data-stu-id="403ae-128">F</span></span>           | <span data-ttu-id="403ae-129">src0</span><span class="sxs-lookup"><span data-stu-id="403ae-129">src0</span></span> | <span data-ttu-id="403ae-130">src0 ou src1</span><span class="sxs-lookup"><span data-stu-id="403ae-130">src0 or src1</span></span>  | <span data-ttu-id="403ae-131">+inf</span><span class="sxs-lookup"><span data-stu-id="403ae-131">+inf</span></span> | <span data-ttu-id="403ae-132">src0</span><span class="sxs-lookup"><span data-stu-id="403ae-132">src0</span></span> |
| <span data-ttu-id="403ae-133">+inf</span><span class="sxs-lookup"><span data-stu-id="403ae-133">+inf</span></span>        | <span data-ttu-id="403ae-134">+inf</span><span class="sxs-lookup"><span data-stu-id="403ae-134">+inf</span></span> | <span data-ttu-id="403ae-135">+inf</span><span class="sxs-lookup"><span data-stu-id="403ae-135">+inf</span></span>          | <span data-ttu-id="403ae-136">+inf</span><span class="sxs-lookup"><span data-stu-id="403ae-136">+inf</span></span> | <span data-ttu-id="403ae-137">+inf</span><span class="sxs-lookup"><span data-stu-id="403ae-137">+inf</span></span> |
| <span data-ttu-id="403ae-138">NaN</span><span class="sxs-lookup"><span data-stu-id="403ae-138">NaN</span></span>         | <span data-ttu-id="403ae-139">-inf</span><span class="sxs-lookup"><span data-stu-id="403ae-139">-inf</span></span> | <span data-ttu-id="403ae-140">src1</span><span class="sxs-lookup"><span data-stu-id="403ae-140">src1</span></span>          | <span data-ttu-id="403ae-141">+inf</span><span class="sxs-lookup"><span data-stu-id="403ae-141">+inf</span></span> | <span data-ttu-id="403ae-142">NaN</span><span class="sxs-lookup"><span data-stu-id="403ae-142">NaN</span></span>  |

<span data-ttu-id="403ae-143">F significa número real finito.</span><span class="sxs-lookup"><span data-stu-id="403ae-143">F means finite-real number.</span></span>


## <a name="type-description"></a><span data-ttu-id="403ae-144">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="403ae-144">Type Description</span></span>

| <span data-ttu-id="403ae-145">Name</span><span class="sxs-lookup"><span data-stu-id="403ae-145">Name</span></span> | <span data-ttu-id="403ae-146">Entrada/saída</span><span class="sxs-lookup"><span data-stu-id="403ae-146">In/Out</span></span>      | [<span data-ttu-id="403ae-147">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="403ae-147">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="403ae-148">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="403ae-148">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="403ae-149">Tamanho</span><span class="sxs-lookup"><span data-stu-id="403ae-149">Size</span></span>                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="403ae-150">x</span><span class="sxs-lookup"><span data-stu-id="403ae-150">x</span></span>    | <span data-ttu-id="403ae-151">in</span><span class="sxs-lookup"><span data-stu-id="403ae-151">in</span></span>          | <span data-ttu-id="403ae-152">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="403ae-152">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="403ae-153">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="403ae-153">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="403ae-154">any</span><span class="sxs-lookup"><span data-stu-id="403ae-154">any</span></span>                          |
| <span data-ttu-id="403ae-155">a</span><span class="sxs-lookup"><span data-stu-id="403ae-155">y</span></span>    | <span data-ttu-id="403ae-156">in</span><span class="sxs-lookup"><span data-stu-id="403ae-156">in</span></span>          | <span data-ttu-id="403ae-157">igual ao x de entrada</span><span class="sxs-lookup"><span data-stu-id="403ae-157">same as input x</span></span>                                                                                                | <span data-ttu-id="403ae-158">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="403ae-158">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="403ae-159">mesmas dimensões como entrada x</span><span class="sxs-lookup"><span data-stu-id="403ae-159">same dimension(s) as input x</span></span> |
| <span data-ttu-id="403ae-160">RET</span><span class="sxs-lookup"><span data-stu-id="403ae-160">ret</span></span>  | <span data-ttu-id="403ae-161">tipo de retorno</span><span class="sxs-lookup"><span data-stu-id="403ae-161">return type</span></span> | <span data-ttu-id="403ae-162">igual ao x de entrada</span><span class="sxs-lookup"><span data-stu-id="403ae-162">same as input x</span></span>                                                                                                | <span data-ttu-id="403ae-163">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="403ae-163">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="403ae-164">mesmas dimensões como entrada x</span><span class="sxs-lookup"><span data-stu-id="403ae-164">same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="403ae-165">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="403ae-165">Minimum Shader Model</span></span>

<span data-ttu-id="403ae-166">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="403ae-166">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="403ae-167">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="403ae-167">Shader Model</span></span>                                                                       | <span data-ttu-id="403ae-168">Com suporte</span><span class="sxs-lookup"><span data-stu-id="403ae-168">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="403ae-169">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="403ae-169">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="403ae-170">sim</span><span class="sxs-lookup"><span data-stu-id="403ae-170">yes</span></span>                         |
| [<span data-ttu-id="403ae-171">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="403ae-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="403ae-172">Sim (vs \_ 1 \_ 1 e PS \_ 1 \_ 4)</span><span class="sxs-lookup"><span data-stu-id="403ae-172">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="403ae-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="403ae-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="403ae-174">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="403ae-174">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

[<span data-ttu-id="403ae-175">**Especificação funcional do DirectX**</span><span class="sxs-lookup"><span data-stu-id="403ae-175">**DirectX Functional Specification**</span></span>](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MAX) 
</dt> </dl>
 
