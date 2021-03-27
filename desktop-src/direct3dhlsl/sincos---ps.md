---
title: Sincos-PS
description: Computa seno e cosseno em radianos. | Sincos-PS
ms.assetid: 639237ea-1b7a-4959-9093-78f134c11863
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1e7ccdca91af206862384ae14cf25a85d0817814
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989198"
---
# <a name="sincos---ps"></a><span data-ttu-id="19853-104">Sincos-PS</span><span class="sxs-lookup"><span data-stu-id="19853-104">sincos - ps</span></span>

<span data-ttu-id="19853-105">Computa seno e cosseno em radianos.</span><span class="sxs-lookup"><span data-stu-id="19853-105">Computes sine and cosine, in radians.</span></span>

## <a name="syntax"></a><span data-ttu-id="19853-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="19853-106">Syntax</span></span>

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="19853-107">PS \_ 2 \_ 0 e PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="19853-107">ps\_2\_0 and ps\_2\_x</span></span>



| <span data-ttu-id="19853-108">Sincos DST. w.x.y.</span><span class="sxs-lookup"><span data-stu-id="19853-108">sincos dst.{x\</span></span>|<span data-ttu-id="19853-109">Iar</span><span class="sxs-lookup"><span data-stu-id="19853-109">y\</span></span>|<span data-ttu-id="19853-110">XY}, src0. w.x.y.</span><span class="sxs-lookup"><span data-stu-id="19853-110">xy}, src0.{x\</span></span>|<span data-ttu-id="19853-111">Iar</span><span class="sxs-lookup"><span data-stu-id="19853-111">y\</span></span>|<span data-ttu-id="19853-112">z</span><span class="sxs-lookup"><span data-stu-id="19853-112">z\</span></span>|<span data-ttu-id="19853-113">w}, src1, src2</span><span class="sxs-lookup"><span data-stu-id="19853-113">w}, src1, src2</span></span> |
|------------------------------------------------------|



 

<span data-ttu-id="19853-114">Em que:</span><span class="sxs-lookup"><span data-stu-id="19853-114">Where:</span></span>

-   <span data-ttu-id="19853-115">o DST é o registro de destino e precisa ser um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="19853-115">dst is the destination register and has to be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span> <span data-ttu-id="19853-116">O registro de destino deve ter exatamente uma das três seguintes máscaras:. x \| . y \| . XY.</span><span class="sxs-lookup"><span data-stu-id="19853-116">The destination register must have exactly one of the following three masks: .x \| .y \| .xy.</span></span>
-   <span data-ttu-id="19853-117">src0 é um registro de origem que fornece o ângulo de entrada, que deve estar dentro \[ de-PI, + PI \] .</span><span class="sxs-lookup"><span data-stu-id="19853-117">src0 is a source register that provides the input angle, which must be within \[-pi, +pi\].</span></span> <span data-ttu-id="19853-118">{x \| y \| z \| w} é o swizzle de replicação necessário.</span><span class="sxs-lookup"><span data-stu-id="19853-118">{x\|y\|z\|w} is the required replicate swizzle.</span></span>
-   <span data-ttu-id="19853-119">src1 e src2 são registros de origem e devem ser dois s de [registro float de constante](dx9-graphics-reference-asm-ps-registers-constant-float.md)diferente (c \# ).</span><span class="sxs-lookup"><span data-stu-id="19853-119">src1 and src2 are source registers and must be two different [Constant Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)s (c\#).</span></span> <span data-ttu-id="19853-120">Os valores de src1 e src2 devem ser das macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) e [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="19853-120">The values of src1 and src2 must be that of the macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) and [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) respectively.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="19853-121">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="19853-121">ps\_3\_0</span></span>



| <span data-ttu-id="19853-122">Sincos DST. w.x.y.</span><span class="sxs-lookup"><span data-stu-id="19853-122">sincos dst.{x\</span></span>|<span data-ttu-id="19853-123">Iar</span><span class="sxs-lookup"><span data-stu-id="19853-123">y\</span></span>|<span data-ttu-id="19853-124">XY}, src0. w.x.y.</span><span class="sxs-lookup"><span data-stu-id="19853-124">xy}, src0.{x\</span></span>|<span data-ttu-id="19853-125">Iar</span><span class="sxs-lookup"><span data-stu-id="19853-125">y\</span></span>|<span data-ttu-id="19853-126">z</span><span class="sxs-lookup"><span data-stu-id="19853-126">z\</span></span>|<span data-ttu-id="19853-127">Mostrar</span><span class="sxs-lookup"><span data-stu-id="19853-127">w}</span></span> |
|------------------------------------------|



 

<span data-ttu-id="19853-128">Em que:</span><span class="sxs-lookup"><span data-stu-id="19853-128">Where:</span></span>

-   <span data-ttu-id="19853-129">o DST é um registro de destino e precisa ser um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="19853-129">dst is a destination register and has to be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span> <span data-ttu-id="19853-130">O registro de destino deve ter exatamente uma das três seguintes máscaras:. x \| . y \| . XY.</span><span class="sxs-lookup"><span data-stu-id="19853-130">The destination register must have exactly one of the following three masks: .x \| .y \| .xy.</span></span>
-   <span data-ttu-id="19853-131">src0 é um registro de origem que fornece o ângulo de entrada, que deve estar dentro \[ de-PI, + PI \] .</span><span class="sxs-lookup"><span data-stu-id="19853-131">src0 is a source register that provides the input angle, which must be within \[-pi, +pi\].</span></span> <span data-ttu-id="19853-132">{x \| y \| z \| w} é o swizzle de replicação necessário.</span><span class="sxs-lookup"><span data-stu-id="19853-132">{x\|y\|z\|w} is the required replicate swizzle.</span></span>

## <a name="remarks"></a><span data-ttu-id="19853-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="19853-133">Remarks</span></span>



| <span data-ttu-id="19853-134">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="19853-134">Pixel shader versions</span></span> | <span data-ttu-id="19853-135">1\_1</span><span class="sxs-lookup"><span data-stu-id="19853-135">1\_1</span></span> | <span data-ttu-id="19853-136">1\_2</span><span class="sxs-lookup"><span data-stu-id="19853-136">1\_2</span></span> | <span data-ttu-id="19853-137">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="19853-137">1\_3</span></span> | <span data-ttu-id="19853-138">1\_4</span><span class="sxs-lookup"><span data-stu-id="19853-138">1\_4</span></span> | <span data-ttu-id="19853-139">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="19853-139">2\_0</span></span> | <span data-ttu-id="19853-140">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="19853-140">2\_x</span></span> | <span data-ttu-id="19853-141">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="19853-141">2\_sw</span></span> | <span data-ttu-id="19853-142">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="19853-142">3\_0</span></span> | <span data-ttu-id="19853-143">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="19853-143">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="19853-144">sincos</span><span class="sxs-lookup"><span data-stu-id="19853-144">sincos</span></span>                |      |      |      |      | <span data-ttu-id="19853-145">x</span><span class="sxs-lookup"><span data-stu-id="19853-145">x</span></span>    | <span data-ttu-id="19853-146">x</span><span class="sxs-lookup"><span data-stu-id="19853-146">x</span></span>    | <span data-ttu-id="19853-147">x</span><span class="sxs-lookup"><span data-stu-id="19853-147">x</span></span>     | <span data-ttu-id="19853-148">x</span><span class="sxs-lookup"><span data-stu-id="19853-148">x</span></span>    | <span data-ttu-id="19853-149">x</span><span class="sxs-lookup"><span data-stu-id="19853-149">x</span></span>     |



 

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="19853-150">PS \_ 2 \_ 0 e PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="19853-150">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="19853-151">Para \_ o PS 2 \_ 0 e o PS \_ 2 \_ x, Sincos pode ser usado com predicação, mas com uma restrição para o swizzle do [registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md) (p0): somente replicar swizzle (. x. \| y \| . z \| . w) é permitido.</span><span class="sxs-lookup"><span data-stu-id="19853-151">For ps\_2\_0 and ps\_2\_x, sincos can be used with predication, but with one restriction to the swizzle of the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md) (p0): only replicate swizzle (.x \| .y \| .z \| .w) is allowed.</span></span>

<span data-ttu-id="19853-152">Para \_ o PS 2 \_ 0 e \_ o PS 2 \_ x, a instrução funciona da seguinte maneira (V = o valor escalar de src0 com um swizzle replicate):</span><span class="sxs-lookup"><span data-stu-id="19853-152">For ps\_2\_0 and ps\_2\_x, the instruction operates as follows (V = the scalar value from src0 with a replicate swizzle):</span></span>

-   <span data-ttu-id="19853-153">Se a máscara de gravação for. x:</span><span class="sxs-lookup"><span data-stu-id="19853-153">If the write mask is .x:</span></span>
    ```
    dest.x = cos(V)
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="19853-154">Se a máscara de gravação for. y:</span><span class="sxs-lookup"><span data-stu-id="19853-154">If the write mask is .y:</span></span>
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="19853-155">Se a máscara de gravação for. XY:</span><span class="sxs-lookup"><span data-stu-id="19853-155">If the write mask is .xy:</span></span>
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="ps_3_0"></a><span data-ttu-id="19853-156">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="19853-156">ps\_3\_0</span></span>

<span data-ttu-id="19853-157">Para o PS \_ 3 \_ 0, Sincos pode ser usado com predicação sem nenhuma restrição.</span><span class="sxs-lookup"><span data-stu-id="19853-157">For ps\_3\_0, sincos can be used with predication without any restriction.</span></span> <span data-ttu-id="19853-158">Consulte [registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="19853-158">See [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>

<span data-ttu-id="19853-159">Para \_ o PS 3 \_ 0, a instrução funciona da seguinte maneira (V = o valor escalar de src0 com um swizzle de replicação):</span><span class="sxs-lookup"><span data-stu-id="19853-159">For ps\_3\_0, the instruction operates as follows (V = the scalar value from src0 with a replicate swizzle):</span></span>

-   <span data-ttu-id="19853-160">Se a máscara de gravação for. x:</span><span class="sxs-lookup"><span data-stu-id="19853-160">If the write mask is .x:</span></span>
    ```
    dest.x = cos(V)
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="19853-161">Se a máscara de gravação for. y:</span><span class="sxs-lookup"><span data-stu-id="19853-161">If the write mask is .y:</span></span>
    ```
    dest.x is not touched by the instruction
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="19853-162">Se a máscara de gravação for. XY:</span><span class="sxs-lookup"><span data-stu-id="19853-162">If the write mask is .xy:</span></span>
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

<span data-ttu-id="19853-163">O aplicativo pode mapear um ângulo arbitrário (em radianos) para o intervalo \[ -PI, + PI \] usando o pseudocódigo de sombreador a seguir:</span><span class="sxs-lookup"><span data-stu-id="19853-163">The application can map an arbitrary angle (in radians) to the range \[-pi, +pi\] using the following shader pseudocode:</span></span>


```
def c0, pi, 0.5, 2*pi, 1/(2*pi)
mad r0.x, input_angle, c0.w, c0.y
frc r0.x, r0.x
mad r0.x, r0.x, c0.z, -c0.x
```



## <a name="related-topics"></a><span data-ttu-id="19853-164">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="19853-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19853-165">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="19853-165">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
