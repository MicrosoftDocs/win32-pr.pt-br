---
title: min
description: Seleciona o menor x e y.
ms.assetid: 4e10cfc2-d680-4d7f-81b2-fa52024f902d
keywords:
- HLSL mín.
topic_type:
- apiref
api_name:
- min
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 129c5cb641c2d69b6c1365d8221663e264060532
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454310"
---
# <a name="min"></a><span data-ttu-id="dd58b-104">min</span><span class="sxs-lookup"><span data-stu-id="dd58b-104">min</span></span>

<span data-ttu-id="dd58b-105">Seleciona o menor x e y.</span><span class="sxs-lookup"><span data-stu-id="dd58b-105">Selects the lesser of x and y.</span></span>



| <span data-ttu-id="dd58b-106">Ret. mín (x, y)</span><span class="sxs-lookup"><span data-stu-id="dd58b-106">ret min(x, y)</span></span> |
|---------------|



 

## <a name="parameters"></a><span data-ttu-id="dd58b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd58b-107">Parameters</span></span>



| <span data-ttu-id="dd58b-108">Item</span><span class="sxs-lookup"><span data-stu-id="dd58b-108">Item</span></span>                                                   | <span data-ttu-id="dd58b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="dd58b-109">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="dd58b-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="dd58b-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="dd58b-111">\[no \] valor de entrada x.</span><span class="sxs-lookup"><span data-stu-id="dd58b-111">\[in\] The x input value.</span></span><br/> |
| <span data-ttu-id="dd58b-112"><span id="y"></span><span id="Y"></span>*Iar*</span><span class="sxs-lookup"><span data-stu-id="dd58b-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="dd58b-113">\[no \] valor de entrada de y.</span><span class="sxs-lookup"><span data-stu-id="dd58b-113">\[in\] The y input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="dd58b-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="dd58b-114">Return Value</span></span>

<span data-ttu-id="dd58b-115">O parâmetro *x* ou *y* , o que for o menor valor.</span><span class="sxs-lookup"><span data-stu-id="dd58b-115">The *x* or *y* parameter, whichever is the smallest value.</span></span>


## <a name="remarks"></a><span data-ttu-id="dd58b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd58b-116">Remarks</span></span>

<span data-ttu-id="dd58b-117">Os desnormals são tratados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="dd58b-117">Denormals are handled as follows:</span></span>

| <span data-ttu-id="dd58b-118">src0 src1-></span><span class="sxs-lookup"><span data-stu-id="dd58b-118">src0 src1-></span></span> | <span data-ttu-id="dd58b-119">-inf</span><span class="sxs-lookup"><span data-stu-id="dd58b-119">-inf</span></span> | <span data-ttu-id="dd58b-120">F</span><span class="sxs-lookup"><span data-stu-id="dd58b-120">F</span></span>             | <span data-ttu-id="dd58b-121">+inf</span><span class="sxs-lookup"><span data-stu-id="dd58b-121">+inf</span></span> | <span data-ttu-id="dd58b-122">NAN</span><span class="sxs-lookup"><span data-stu-id="dd58b-122">NAN</span></span>  |
|-------------|------|---------------|------|------|
| <span data-ttu-id="dd58b-123">-inf</span><span class="sxs-lookup"><span data-stu-id="dd58b-123">-inf</span></span>        | <span data-ttu-id="dd58b-124">-inf</span><span class="sxs-lookup"><span data-stu-id="dd58b-124">-inf</span></span> | <span data-ttu-id="dd58b-125">-inf</span><span class="sxs-lookup"><span data-stu-id="dd58b-125">-inf</span></span>          | <span data-ttu-id="dd58b-126">-inf</span><span class="sxs-lookup"><span data-stu-id="dd58b-126">-inf</span></span> | <span data-ttu-id="dd58b-127">-inf</span><span class="sxs-lookup"><span data-stu-id="dd58b-127">-inf</span></span> |
| <span data-ttu-id="dd58b-128">F</span><span class="sxs-lookup"><span data-stu-id="dd58b-128">F</span></span>           | <span data-ttu-id="dd58b-129">-inf</span><span class="sxs-lookup"><span data-stu-id="dd58b-129">-inf</span></span> | <span data-ttu-id="dd58b-130">src0 ou src1</span><span class="sxs-lookup"><span data-stu-id="dd58b-130">src0 or src1</span></span>  | <span data-ttu-id="dd58b-131">src0</span><span class="sxs-lookup"><span data-stu-id="dd58b-131">src0</span></span> | <span data-ttu-id="dd58b-132">src0</span><span class="sxs-lookup"><span data-stu-id="dd58b-132">src0</span></span> |
| <span data-ttu-id="dd58b-133">+inf</span><span class="sxs-lookup"><span data-stu-id="dd58b-133">+inf</span></span>        | <span data-ttu-id="dd58b-134">-inf</span><span class="sxs-lookup"><span data-stu-id="dd58b-134">-inf</span></span> | <span data-ttu-id="dd58b-135">src1</span><span class="sxs-lookup"><span data-stu-id="dd58b-135">src1</span></span>          | <span data-ttu-id="dd58b-136">+inf</span><span class="sxs-lookup"><span data-stu-id="dd58b-136">+inf</span></span> | <span data-ttu-id="dd58b-137">+inf</span><span class="sxs-lookup"><span data-stu-id="dd58b-137">+inf</span></span> |
| <span data-ttu-id="dd58b-138">NaN</span><span class="sxs-lookup"><span data-stu-id="dd58b-138">NaN</span></span>         | <span data-ttu-id="dd58b-139">-inf</span><span class="sxs-lookup"><span data-stu-id="dd58b-139">-inf</span></span> | <span data-ttu-id="dd58b-140">src1</span><span class="sxs-lookup"><span data-stu-id="dd58b-140">src1</span></span>          | <span data-ttu-id="dd58b-141">+inf</span><span class="sxs-lookup"><span data-stu-id="dd58b-141">+inf</span></span> | <span data-ttu-id="dd58b-142">NaN</span><span class="sxs-lookup"><span data-stu-id="dd58b-142">NaN</span></span>  |

<span data-ttu-id="dd58b-143">F significa número real finito.</span><span class="sxs-lookup"><span data-stu-id="dd58b-143">F means finite-real number.</span></span>


## <a name="type-description"></a><span data-ttu-id="dd58b-144">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="dd58b-144">Type Description</span></span>

| <span data-ttu-id="dd58b-145">Name</span><span class="sxs-lookup"><span data-stu-id="dd58b-145">Name</span></span> | <span data-ttu-id="dd58b-146">Entrada/saída</span><span class="sxs-lookup"><span data-stu-id="dd58b-146">In/Out</span></span>      | [<span data-ttu-id="dd58b-147">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="dd58b-147">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="dd58b-148">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="dd58b-148">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="dd58b-149">Tamanho</span><span class="sxs-lookup"><span data-stu-id="dd58b-149">Size</span></span>                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="dd58b-150">x</span><span class="sxs-lookup"><span data-stu-id="dd58b-150">x</span></span>    | <span data-ttu-id="dd58b-151">in</span><span class="sxs-lookup"><span data-stu-id="dd58b-151">in</span></span>          | <span data-ttu-id="dd58b-152">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="dd58b-152">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="dd58b-153">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="dd58b-153">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="dd58b-154">any</span><span class="sxs-lookup"><span data-stu-id="dd58b-154">any</span></span>                          |
| <span data-ttu-id="dd58b-155">a</span><span class="sxs-lookup"><span data-stu-id="dd58b-155">y</span></span>    | <span data-ttu-id="dd58b-156">in</span><span class="sxs-lookup"><span data-stu-id="dd58b-156">in</span></span>          | <span data-ttu-id="dd58b-157">igual ao x de entrada</span><span class="sxs-lookup"><span data-stu-id="dd58b-157">same as input x</span></span>                                                                                                | <span data-ttu-id="dd58b-158">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="dd58b-158">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="dd58b-159">mesmas dimensões como entrada x</span><span class="sxs-lookup"><span data-stu-id="dd58b-159">same dimension(s) as input x</span></span> |
| <span data-ttu-id="dd58b-160">RET</span><span class="sxs-lookup"><span data-stu-id="dd58b-160">ret</span></span>  | <span data-ttu-id="dd58b-161">tipo de retorno</span><span class="sxs-lookup"><span data-stu-id="dd58b-161">return type</span></span> | <span data-ttu-id="dd58b-162">igual ao x de entrada</span><span class="sxs-lookup"><span data-stu-id="dd58b-162">same as input x</span></span>                                                                                                | <span data-ttu-id="dd58b-163">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="dd58b-163">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="dd58b-164">mesmas dimensões como entrada x</span><span class="sxs-lookup"><span data-stu-id="dd58b-164">same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="dd58b-165">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="dd58b-165">Minimum Shader Model</span></span>

<span data-ttu-id="dd58b-166">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="dd58b-166">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="dd58b-167">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="dd58b-167">Shader Model</span></span>                                                                       | <span data-ttu-id="dd58b-168">Com suporte</span><span class="sxs-lookup"><span data-stu-id="dd58b-168">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="dd58b-169">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="dd58b-169">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="dd58b-170">sim</span><span class="sxs-lookup"><span data-stu-id="dd58b-170">yes</span></span>                         |
| [<span data-ttu-id="dd58b-171">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dd58b-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="dd58b-172">Sim (vs \_ 1 \_ 1 e PS \_ 1 \_ 4)</span><span class="sxs-lookup"><span data-stu-id="dd58b-172">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="dd58b-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd58b-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd58b-174">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="dd58b-174">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

[<span data-ttu-id="dd58b-175">**Especificação funcional do DirectX**</span><span class="sxs-lookup"><span data-stu-id="dd58b-175">**DirectX Functional Specification**</span></span>](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MIN)