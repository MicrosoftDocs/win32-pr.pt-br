---
title: Modificadores para ps_1_X
description: Os modificadores de instrução afetam o resultado da instrução antes de serem gravados no registro de destino. Saiba mais sobre modificadores para ps_1_X.
ms.assetid: 15b892da-b6fd-4bd5-8889-bc48035e7819
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9291d818252c95bc11fae72bd3311ec733a45fa
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129935"
---
# <a name="modifiers-for-ps_1_x"></a><span data-ttu-id="34cf2-104">Modificadores para PS \_ 1 \_ X</span><span class="sxs-lookup"><span data-stu-id="34cf2-104">Modifiers for ps\_1\_X</span></span>

<span data-ttu-id="34cf2-105">Os modificadores de instrução afetam o resultado da instrução antes de serem gravados no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="34cf2-105">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span> <span data-ttu-id="34cf2-106">Por exemplo, use-os para multiplicar ou dividir o resultado por um fator de dois ou para fixe o resultado entre zero e um.</span><span class="sxs-lookup"><span data-stu-id="34cf2-106">For instance, use them to multiply or divide the result by a factor of two, or to clamp the result between zero and one.</span></span> <span data-ttu-id="34cf2-107">Os modificadores de instrução são aplicados depois que a instrução é executada, mas antes de gravar o resultado no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="34cf2-107">Instruction modifiers are applied after the instruction runs but before writing the result to the destination register.</span></span>

<span data-ttu-id="34cf2-108">Uma lista dos modificadores é mostrada abaixo.</span><span class="sxs-lookup"><span data-stu-id="34cf2-108">A list of the modifiers is shown below.</span></span>



| <span data-ttu-id="34cf2-109">Modificador</span><span class="sxs-lookup"><span data-stu-id="34cf2-109">Modifier</span></span> | <span data-ttu-id="34cf2-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="34cf2-110">Description</span></span>                   | <span data-ttu-id="34cf2-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="34cf2-111">Syntax</span></span>           | <span data-ttu-id="34cf2-112">Versão 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="34cf2-112">Version 1\_1</span></span> | <span data-ttu-id="34cf2-113">Versão 1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="34cf2-113">Version 1\_2</span></span>     |<span data-ttu-id="34cf2-114">Versão 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="34cf2-114">Version  1\_3</span></span>    | <span data-ttu-id="34cf2-115">Versão 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="34cf2-115">Version 1\_4</span></span>    |
|----------|-------------------------------|------------------|---------|------|------|------|
| <span data-ttu-id="34cf2-116">\_X2</span><span class="sxs-lookup"><span data-stu-id="34cf2-116">\_x2</span></span>     | <span data-ttu-id="34cf2-117">Multiplicar por 2</span><span class="sxs-lookup"><span data-stu-id="34cf2-117">Multiply by 2</span></span>                 | <span data-ttu-id="34cf2-118">instrução \_ X2</span><span class="sxs-lookup"><span data-stu-id="34cf2-118">instruction\_x2</span></span>  | <span data-ttu-id="34cf2-119">X</span><span class="sxs-lookup"><span data-stu-id="34cf2-119">X</span></span>       | <span data-ttu-id="34cf2-120">X</span><span class="sxs-lookup"><span data-stu-id="34cf2-120">X</span></span>    | <span data-ttu-id="34cf2-121">X</span><span class="sxs-lookup"><span data-stu-id="34cf2-121">X</span></span>    | <span data-ttu-id="34cf2-122">X</span><span class="sxs-lookup"><span data-stu-id="34cf2-122">X</span></span>    |
| <span data-ttu-id="34cf2-123">\_X4</span><span class="sxs-lookup"><span data-stu-id="34cf2-123">\_x4</span></span>     | <span data-ttu-id="34cf2-124">Multiplicar por 4</span><span class="sxs-lookup"><span data-stu-id="34cf2-124">Multiply by 4</span></span>                 | <span data-ttu-id="34cf2-125">\_X4 instruções</span><span class="sxs-lookup"><span data-stu-id="34cf2-125">instruction\_x4</span></span>  | <span data-ttu-id="34cf2-126">X</span><span class="sxs-lookup"><span data-stu-id="34cf2-126">X</span></span>       | <span data-ttu-id="34cf2-127">X</span><span class="sxs-lookup"><span data-stu-id="34cf2-127">X</span></span>    | <span data-ttu-id="34cf2-128">X</span><span class="sxs-lookup"><span data-stu-id="34cf2-128">X</span></span>    | <span data-ttu-id="34cf2-129">X</span><span class="sxs-lookup"><span data-stu-id="34cf2-129">X</span></span>    |
| <span data-ttu-id="34cf2-130">\_x8</span><span class="sxs-lookup"><span data-stu-id="34cf2-130">\_x8</span></span>     | <span data-ttu-id="34cf2-131">Multiplicar por 8</span><span class="sxs-lookup"><span data-stu-id="34cf2-131">Multiply by 8</span></span>                 | <span data-ttu-id="34cf2-132">x8 de instruções \_</span><span class="sxs-lookup"><span data-stu-id="34cf2-132">instruction\_x8</span></span>  |         |      |      | <span data-ttu-id="34cf2-133">X</span><span class="sxs-lookup"><span data-stu-id="34cf2-133">X</span></span>    |
| <span data-ttu-id="34cf2-134">\_D2</span><span class="sxs-lookup"><span data-stu-id="34cf2-134">\_d2</span></span>     | <span data-ttu-id="34cf2-135">Dividir por 2</span><span class="sxs-lookup"><span data-stu-id="34cf2-135">Divide by 2</span></span>                   | <span data-ttu-id="34cf2-136">instrução \_ D2</span><span class="sxs-lookup"><span data-stu-id="34cf2-136">instruction\_d2</span></span>  | <span data-ttu-id="34cf2-137">X</span><span class="sxs-lookup"><span data-stu-id="34cf2-137">X</span></span>       | <span data-ttu-id="34cf2-138">X</span><span class="sxs-lookup"><span data-stu-id="34cf2-138">X</span></span>    | <span data-ttu-id="34cf2-139">X</span><span class="sxs-lookup"><span data-stu-id="34cf2-139">X</span></span>    | <span data-ttu-id="34cf2-140">X</span><span class="sxs-lookup"><span data-stu-id="34cf2-140">X</span></span>    |
| <span data-ttu-id="34cf2-141">\_D4</span><span class="sxs-lookup"><span data-stu-id="34cf2-141">\_d4</span></span>     | <span data-ttu-id="34cf2-142">Dividir por 4</span><span class="sxs-lookup"><span data-stu-id="34cf2-142">Divide by 4</span></span>                   | <span data-ttu-id="34cf2-143">instrução \_ D4</span><span class="sxs-lookup"><span data-stu-id="34cf2-143">instruction\_d4</span></span>  |         |      |      | <span data-ttu-id="34cf2-144">X</span><span class="sxs-lookup"><span data-stu-id="34cf2-144">X</span></span>    |
| <span data-ttu-id="34cf2-145">\_D8</span><span class="sxs-lookup"><span data-stu-id="34cf2-145">\_d8</span></span>     | <span data-ttu-id="34cf2-146">Dividir por 8</span><span class="sxs-lookup"><span data-stu-id="34cf2-146">Divide by 8</span></span>                   | <span data-ttu-id="34cf2-147">instrução \_ D8</span><span class="sxs-lookup"><span data-stu-id="34cf2-147">instruction\_d8</span></span>  |         |      |      | <span data-ttu-id="34cf2-148">X</span><span class="sxs-lookup"><span data-stu-id="34cf2-148">X</span></span>    |
| <span data-ttu-id="34cf2-149">\_saturação</span><span class="sxs-lookup"><span data-stu-id="34cf2-149">\_sat</span></span>    | <span data-ttu-id="34cf2-150">Saturação (fixe de 0 e 1)</span><span class="sxs-lookup"><span data-stu-id="34cf2-150">Saturate (clamp from 0 and 1)</span></span> | <span data-ttu-id="34cf2-151">instrução \_ SAT</span><span class="sxs-lookup"><span data-stu-id="34cf2-151">instruction\_sat</span></span> | <span data-ttu-id="34cf2-152">X</span><span class="sxs-lookup"><span data-stu-id="34cf2-152">X</span></span>       | <span data-ttu-id="34cf2-153">X</span><span class="sxs-lookup"><span data-stu-id="34cf2-153">X</span></span>    | <span data-ttu-id="34cf2-154">X</span><span class="sxs-lookup"><span data-stu-id="34cf2-154">X</span></span>    | <span data-ttu-id="34cf2-155">X</span><span class="sxs-lookup"><span data-stu-id="34cf2-155">X</span></span>    |



 

-   <span data-ttu-id="34cf2-156">O modificador de multiplicação multiplica os dados de registro por uma potência de dois após sua leitura.</span><span class="sxs-lookup"><span data-stu-id="34cf2-156">The multiply modifier multiplies the register data by a power of two after it is read.</span></span> <span data-ttu-id="34cf2-157">Isso é o mesmo que uma mudança à esquerda.</span><span class="sxs-lookup"><span data-stu-id="34cf2-157">This is the same as a shift left.</span></span>
-   <span data-ttu-id="34cf2-158">O modificador de divisão divide os dados de registro por uma potência de dois após sua leitura.</span><span class="sxs-lookup"><span data-stu-id="34cf2-158">The divide modifier divides the register data by a power of two after it is read.</span></span> <span data-ttu-id="34cf2-159">Isso é o mesmo que uma mudança à direita.</span><span class="sxs-lookup"><span data-stu-id="34cf2-159">This is the same as a shift right.</span></span>
-   <span data-ttu-id="34cf2-160">O modificador saturação coloca o intervalo de valores de registro de zero para um.</span><span class="sxs-lookup"><span data-stu-id="34cf2-160">The saturate modifier clamps the range of register values from zero to one.</span></span>

<span data-ttu-id="34cf2-161">Os modificadores de instrução podem ser usados em instruções aritméticas.</span><span class="sxs-lookup"><span data-stu-id="34cf2-161">Instruction modifiers can be used on arithmetic instructions.</span></span> <span data-ttu-id="34cf2-162">Eles não podem ser usados em instruções de endereço de textura.</span><span class="sxs-lookup"><span data-stu-id="34cf2-162">They may not be used on texture address instructions.</span></span>

<span data-ttu-id="34cf2-163">Modificador de multiplicação</span><span class="sxs-lookup"><span data-stu-id="34cf2-163">Multiply modifier</span></span>

<span data-ttu-id="34cf2-164">Este exemplo carrega o registro de destino (dest) com a soma das duas cores nos operandos de origem (src0 e src1) e multiplica o resultado por dois.</span><span class="sxs-lookup"><span data-stu-id="34cf2-164">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and multiplies the result by two.</span></span>


```
add_x2 dest, src0, src1
```



<span data-ttu-id="34cf2-165">Este exemplo combina dois modificadores de instrução.</span><span class="sxs-lookup"><span data-stu-id="34cf2-165">This example combines two instruction modifiers.</span></span> <span data-ttu-id="34cf2-166">Primeiro, duas cores nos operandos de origem (src0 e src1) são adicionadas.</span><span class="sxs-lookup"><span data-stu-id="34cf2-166">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="34cf2-167">Em seguida, o resultado é multiplicado por dois e clamped entre 0,0 e 1,0 para cada componente.</span><span class="sxs-lookup"><span data-stu-id="34cf2-167">The result is then multiplied by two, and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="34cf2-168">O resultado é salvo no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="34cf2-168">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



<span data-ttu-id="34cf2-169">Modificador de divisão</span><span class="sxs-lookup"><span data-stu-id="34cf2-169">Divide modifier</span></span>

<span data-ttu-id="34cf2-170">Este exemplo carrega o registro de destino (dest) com a soma das duas cores nos operandos de origem (src0 e src1) e divide o resultado por dois.</span><span class="sxs-lookup"><span data-stu-id="34cf2-170">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and divides the result by two.</span></span>


```
add_d2 dest, src0, src1
```



<span data-ttu-id="34cf2-171">Modificador saturado</span><span class="sxs-lookup"><span data-stu-id="34cf2-171">Saturate modifier</span></span>

<span data-ttu-id="34cf2-172">Para obter instruções aritméticas, o modificador de saturação coloca o resultado dessa instrução no intervalo de 0,0 a 1,0 para cada componente.</span><span class="sxs-lookup"><span data-stu-id="34cf2-172">For arithmetic instructions, the saturation modifier clamps the result of this instruction into the range 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="34cf2-173">O exemplo a seguir mostra como usar esse modificador de instrução.</span><span class="sxs-lookup"><span data-stu-id="34cf2-173">The following example shows how to use this instruction modifier.</span></span>


```
dp3_sat r0, t0_bx2, v0_bx2    ; t0 is bump, v0 is light direction
```



<span data-ttu-id="34cf2-174">Essa operação ocorre depois de qualquer modificador de instrução de multiplicação ou de divisão.</span><span class="sxs-lookup"><span data-stu-id="34cf2-174">This operation occurs after any multiply or divide instruction modifier.</span></span> <span data-ttu-id="34cf2-175">\_SAT é usado com mais frequência para fixe pontos de produtos.</span><span class="sxs-lookup"><span data-stu-id="34cf2-175">\_sat is most often used to clamp dot product results.</span></span> <span data-ttu-id="34cf2-176">No entanto, ele também habilita a emulação consistente de métodos de várias passagens, em que o buffer de quadro está sempre no intervalo de 0 a 1 e da sintaxe multitextura DirectX 6 e 7,0, na qual a saturação é definida para ocorrer em cada estágio.</span><span class="sxs-lookup"><span data-stu-id="34cf2-176">However, it also enables consistent emulation of multipass methods where the frame buffer is always in the range 0 to 1, and of DirectX 6 and 7.0 multitexture syntax, in which saturation is defined to occur at every stage.</span></span>

<span data-ttu-id="34cf2-177">Este exemplo carrega o registro de destino (dest) com a soma das duas cores nos operandos de origem (src0 e src1) e coloca o resultado no intervalo de 0,0 a 1,0 para cada componente.</span><span class="sxs-lookup"><span data-stu-id="34cf2-177">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1), and clamps the result into the range 0.0 to 1.0 for each component.</span></span>


```
add_sat dest, src0, src1
```



<span data-ttu-id="34cf2-178">Este exemplo combina dois modificadores de instrução.</span><span class="sxs-lookup"><span data-stu-id="34cf2-178">This example combines two instruction modifiers.</span></span> <span data-ttu-id="34cf2-179">Primeiro, duas cores nos operandos de origem (src0 e src1) são adicionadas.</span><span class="sxs-lookup"><span data-stu-id="34cf2-179">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="34cf2-180">O resultado é multiplicado por dois e clamped entre 0,0 e 1,0 para cada componente.</span><span class="sxs-lookup"><span data-stu-id="34cf2-180">The result is multiplied by two and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="34cf2-181">O resultado é salvo no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="34cf2-181">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



## <a name="related-topics"></a><span data-ttu-id="34cf2-182">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="34cf2-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34cf2-183">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="34cf2-183">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




