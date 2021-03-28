---
title: Sincos-vs
description: Computa seno e cosseno em radianos. | Sincos-vs
ms.assetid: 733a3980-ceaf-43dc-a862-923c369e4a65
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ca70a319852346c6e75ba544489d033a861d4c3b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930476"
---
# <a name="sincos---vs"></a><span data-ttu-id="c1366-104">Sincos-vs</span><span class="sxs-lookup"><span data-stu-id="c1366-104">sincos - vs</span></span>

<span data-ttu-id="c1366-105">Computa seno e cosseno em radianos.</span><span class="sxs-lookup"><span data-stu-id="c1366-105">Computes sine and cosine, in radians.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1366-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1366-106">Syntax</span></span>

### <a name="vs_2_0-and-vs_2_x"></a><span data-ttu-id="c1366-107">vs \_ 2 \_ 0 e vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c1366-107">vs\_2\_0 and vs\_2\_x</span></span>



| <span data-ttu-id="c1366-108">Sincos DST. w.x.y.</span><span class="sxs-lookup"><span data-stu-id="c1366-108">sincos dst.{x\</span></span>|<span data-ttu-id="c1366-109">Iar</span><span class="sxs-lookup"><span data-stu-id="c1366-109">y\</span></span>|<span data-ttu-id="c1366-110">XY}, src0. w.x.y.</span><span class="sxs-lookup"><span data-stu-id="c1366-110">xy}, src0.{x\</span></span>|<span data-ttu-id="c1366-111">Iar</span><span class="sxs-lookup"><span data-stu-id="c1366-111">y\</span></span>|<span data-ttu-id="c1366-112">z</span><span class="sxs-lookup"><span data-stu-id="c1366-112">z\</span></span>|<span data-ttu-id="c1366-113">w}, src1, src2</span><span class="sxs-lookup"><span data-stu-id="c1366-113">w}, src1, src2</span></span> |
|------------------------------------------------------|



 

<span data-ttu-id="c1366-114">Em que:</span><span class="sxs-lookup"><span data-stu-id="c1366-114">Where:</span></span>

-   <span data-ttu-id="c1366-115">o DST é o registro de destino e precisa ser um [registro temporário](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="c1366-115">dst is the destination register and has to be a [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r\#).</span></span> <span data-ttu-id="c1366-116">O registro de destino deve ter exatamente uma das três seguintes máscaras:. x \| . y \| . XY.</span><span class="sxs-lookup"><span data-stu-id="c1366-116">The destination register must have exactly one of the following three masks: .x \| .y \| .xy.</span></span>
-   <span data-ttu-id="c1366-117">src0 é um registro de origem que fornece o ângulo de entrada, que deve estar dentro \[ de-PI, + PI \] .</span><span class="sxs-lookup"><span data-stu-id="c1366-117">src0 is a source register that provides the input angle, which must be within \[-pi, +pi\].</span></span> <span data-ttu-id="c1366-118">{x \| y \| z \| w} é o swizzle de replicação necessário.</span><span class="sxs-lookup"><span data-stu-id="c1366-118">{x\|y\|z\|w} is the required replicate swizzle.</span></span>
-   <span data-ttu-id="c1366-119">src1 e src2 são registradores de origem e devem ser dois registros de [flutuação de constante](dx9-graphics-reference-asm-vs-registers-constant-float.md) diferente (c \# ).</span><span class="sxs-lookup"><span data-stu-id="c1366-119">src1 and src2 are source registers and must be two different [Constant Float Register](dx9-graphics-reference-asm-vs-registers-constant-float.md) (c\#).</span></span> <span data-ttu-id="c1366-120">Os valores de src1 e src2 devem ser das macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) e [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c1366-120">The values of src1 and src2 must be that of the macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) and [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) respectively.</span></span>

### <a name="vs_3_0"></a><span data-ttu-id="c1366-121">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c1366-121">vs\_3\_0</span></span>



| <span data-ttu-id="c1366-122">Sincos DST. w.x.y.</span><span class="sxs-lookup"><span data-stu-id="c1366-122">sincos dst.{x\</span></span>|<span data-ttu-id="c1366-123">Iar</span><span class="sxs-lookup"><span data-stu-id="c1366-123">y\</span></span>|<span data-ttu-id="c1366-124">XY}, src0. w.x.y.</span><span class="sxs-lookup"><span data-stu-id="c1366-124">xy}, src0.{x\</span></span>|<span data-ttu-id="c1366-125">Iar</span><span class="sxs-lookup"><span data-stu-id="c1366-125">y\</span></span>|<span data-ttu-id="c1366-126">z</span><span class="sxs-lookup"><span data-stu-id="c1366-126">z\</span></span>|<span data-ttu-id="c1366-127">Mostrar</span><span class="sxs-lookup"><span data-stu-id="c1366-127">w}</span></span> |
|------------------------------------------|



 

<span data-ttu-id="c1366-128">Em que:</span><span class="sxs-lookup"><span data-stu-id="c1366-128">Where:</span></span>

-   <span data-ttu-id="c1366-129">o DST é um registro de destino e precisa ser um [registro temporário](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="c1366-129">dst is a destination register and has to be a [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r\#).</span></span> <span data-ttu-id="c1366-130">O registro de destino deve ter exatamente uma das três seguintes máscaras:. x \| . y \| . XY.</span><span class="sxs-lookup"><span data-stu-id="c1366-130">The destination register must have exactly one of the following three masks: .x \| .y \| .xy.</span></span>
-   <span data-ttu-id="c1366-131">src0 é um registro de origem que fornece o ângulo de entrada, que deve estar dentro \[ de-PI, + PI \] .</span><span class="sxs-lookup"><span data-stu-id="c1366-131">src0 is a source register that provides the input angle, which must be within \[-pi, +pi\].</span></span> <span data-ttu-id="c1366-132">{x \| y \| z \| w} é o swizzle de replicação necessário.</span><span class="sxs-lookup"><span data-stu-id="c1366-132">{x\|y\|z\|w} is the required replicate swizzle.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1366-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1366-133">Remarks</span></span>



| <span data-ttu-id="c1366-134">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="c1366-134">Vertex shader versions</span></span> | <span data-ttu-id="c1366-135">1\_1</span><span class="sxs-lookup"><span data-stu-id="c1366-135">1\_1</span></span> | <span data-ttu-id="c1366-136">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c1366-136">2\_0</span></span> | <span data-ttu-id="c1366-137">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c1366-137">2\_x</span></span> | <span data-ttu-id="c1366-138">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c1366-138">2\_sw</span></span> | <span data-ttu-id="c1366-139">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c1366-139">3\_0</span></span> | <span data-ttu-id="c1366-140">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c1366-140">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="c1366-141">sincos</span><span class="sxs-lookup"><span data-stu-id="c1366-141">sincos</span></span>                 |      | <span data-ttu-id="c1366-142">x</span><span class="sxs-lookup"><span data-stu-id="c1366-142">x</span></span>    | <span data-ttu-id="c1366-143">x</span><span class="sxs-lookup"><span data-stu-id="c1366-143">x</span></span>    | <span data-ttu-id="c1366-144">x</span><span class="sxs-lookup"><span data-stu-id="c1366-144">x</span></span>     | <span data-ttu-id="c1366-145">x</span><span class="sxs-lookup"><span data-stu-id="c1366-145">x</span></span>    | <span data-ttu-id="c1366-146">x</span><span class="sxs-lookup"><span data-stu-id="c1366-146">x</span></span>     |



 

### <a name="vs_2_0-and-vs_2_x-remarks"></a><span data-ttu-id="c1366-147">Comentários sobre o vs \_ 2 \_ e o vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c1366-147">vs\_2\_0 and vs\_2\_x Remarks</span></span>

<span data-ttu-id="c1366-148">Para vs \_ 2 \_ 0 e vs \_ 2 \_ x, Sincos pode ser usado com predicação, mas com uma restrição para o swizzle do [registro de predicado](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0): somente replicar swizzle (. x. \| y \| . z \| . w) é permitido.</span><span class="sxs-lookup"><span data-stu-id="c1366-148">For vs\_2\_0 and vs\_2\_x, sincos can be used with predication, but with one restriction to the swizzle of the [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0): only replicate swizzle (.x \| .y \| .z \| .w) is allowed.</span></span>

<span data-ttu-id="c1366-149">Para vs \_ 2 \_ 0 e vs \_ 2 \_ x, a instrução opera da seguinte maneira: (V = o valor escalar de src0 com um swizzle replicate):</span><span class="sxs-lookup"><span data-stu-id="c1366-149">For vs\_2\_0 and vs\_2\_x, the instruction operates as follows: (V = the scalar value from src0 with a replicate swizzle):</span></span>

-   <span data-ttu-id="c1366-150">Se a máscara de gravação for. x:</span><span class="sxs-lookup"><span data-stu-id="c1366-150">If the write mask is .x:</span></span>
    ```
    dest.x = cos( V )
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="c1366-151">Se a máscara de gravação for. y:</span><span class="sxs-lookup"><span data-stu-id="c1366-151">If the write mask is .y:</span></span>
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin( V )
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="c1366-152">Se a máscara de gravação for. XY:</span><span class="sxs-lookup"><span data-stu-id="c1366-152">If the write mask is .xy:</span></span>
    ```
    dest.x = cos( V )
    dest.y = sin( V )
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="vs_3_0-remarks"></a><span data-ttu-id="c1366-153">vs \_ 3 \_ 0 comentários</span><span class="sxs-lookup"><span data-stu-id="c1366-153">vs\_3\_0 Remarks</span></span>

<span data-ttu-id="c1366-154">Para o vs \_ 3 \_ 0, Sincos pode ser usado com predicação sem nenhuma restrição.</span><span class="sxs-lookup"><span data-stu-id="c1366-154">For vs\_3\_0, sincos can be used with predication without any restriction.</span></span> <span data-ttu-id="c1366-155">Consulte [registro de predicado](dx9-graphics-reference-asm-vs-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="c1366-155">See [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>

<span data-ttu-id="c1366-156">Para \_ o vs 3 \_ 0, a instrução opera da seguinte maneira: (V = o valor escalar de src0 com um swizzle de replicação)</span><span class="sxs-lookup"><span data-stu-id="c1366-156">For vs\_3\_0, the instruction operates as follows: (V = the scalar value from src0 with a replicate swizzle)</span></span>

-   <span data-ttu-id="c1366-157">Se a máscara de gravação for. x:</span><span class="sxs-lookup"><span data-stu-id="c1366-157">If the write mask is .x:</span></span>
    ```
    dest.x = cos( V )
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="c1366-158">Se a máscara de gravação for. y:</span><span class="sxs-lookup"><span data-stu-id="c1366-158">If the write mask is .y:</span></span>
    ```
    dest.x is not touched by the instruction
    dest.y = sin( V )
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="c1366-159">Se a máscara de gravação for. XY:</span><span class="sxs-lookup"><span data-stu-id="c1366-159">If the write mask is .xy:</span></span>
    ```
    dest.x = cos( V )
    dest.y = sin( V )
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

<span data-ttu-id="c1366-160">O aplicativo pode mapear um ângulo arbitrário (em radianos) para o intervalo \[ -PI, + PI \] usando o pseudocódigo de sombreador a seguir:</span><span class="sxs-lookup"><span data-stu-id="c1366-160">The application can map an arbitrary angle (in radians) to the range \[-pi, +pi\] using the following shader pseudocode:</span></span>


```
def c0, pi, 0.5, 2*pi, 1/(2*pi)
mad r0.x, input_angle, c0.w, c0.y
frc r0.x, r0.x
mad r0.x, r0.x, c0.z, -c0.x
```



## <a name="related-topics"></a><span data-ttu-id="c1366-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c1366-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1366-162">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="c1366-162">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
