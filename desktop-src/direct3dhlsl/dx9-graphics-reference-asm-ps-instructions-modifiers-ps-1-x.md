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
ms.openlocfilehash: 6c97196040a8f5f9888cb2fb354dcc18ca3743c7
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988721"
---
# <a name="modifiers-for-ps_1_x"></a><span data-ttu-id="720e0-104">Modificadores para PS \_ 1 \_ X</span><span class="sxs-lookup"><span data-stu-id="720e0-104">Modifiers for ps\_1\_X</span></span>

<span data-ttu-id="720e0-105">Os modificadores de instrução afetam o resultado da instrução antes de serem gravados no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="720e0-105">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span> <span data-ttu-id="720e0-106">Por exemplo, use-os para multiplicar ou dividir o resultado por um fator de dois ou para fixe o resultado entre zero e um.</span><span class="sxs-lookup"><span data-stu-id="720e0-106">For instance, use them to multiply or divide the result by a factor of two, or to clamp the result between zero and one.</span></span> <span data-ttu-id="720e0-107">Os modificadores de instrução são aplicados depois que a instrução é executada, mas antes de gravar o resultado no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="720e0-107">Instruction modifiers are applied after the instruction runs but before writing the result to the destination register.</span></span>

<span data-ttu-id="720e0-108">Uma lista dos modificadores é mostrada abaixo.</span><span class="sxs-lookup"><span data-stu-id="720e0-108">A list of the modifiers is shown below.</span></span>



| <span data-ttu-id="720e0-109">Modificador</span><span class="sxs-lookup"><span data-stu-id="720e0-109">Modifier</span></span> | <span data-ttu-id="720e0-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="720e0-110">Description</span></span>                   | <span data-ttu-id="720e0-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="720e0-111">Syntax</span></span>           | <span data-ttu-id="720e0-112">Versão</span><span class="sxs-lookup"><span data-stu-id="720e0-112">Version</span></span> |      |      |      |
|----------|-------------------------------|------------------|---------|------|------|------|
|          |                               |                  | <span data-ttu-id="720e0-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="720e0-113">1\_1</span></span>    | <span data-ttu-id="720e0-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="720e0-114">1\_2</span></span> | <span data-ttu-id="720e0-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="720e0-115">1\_3</span></span> | <span data-ttu-id="720e0-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="720e0-116">1\_4</span></span> |
| <span data-ttu-id="720e0-117">\_X2</span><span class="sxs-lookup"><span data-stu-id="720e0-117">\_x2</span></span>     | <span data-ttu-id="720e0-118">Multiplicar por 2</span><span class="sxs-lookup"><span data-stu-id="720e0-118">Multiply by 2</span></span>                 | <span data-ttu-id="720e0-119">instrução \_ X2</span><span class="sxs-lookup"><span data-stu-id="720e0-119">instruction\_x2</span></span>  | <span data-ttu-id="720e0-120">X</span><span class="sxs-lookup"><span data-stu-id="720e0-120">X</span></span>       | <span data-ttu-id="720e0-121">X</span><span class="sxs-lookup"><span data-stu-id="720e0-121">X</span></span>    | <span data-ttu-id="720e0-122">X</span><span class="sxs-lookup"><span data-stu-id="720e0-122">X</span></span>    | <span data-ttu-id="720e0-123">X</span><span class="sxs-lookup"><span data-stu-id="720e0-123">X</span></span>    |
| <span data-ttu-id="720e0-124">\_X4</span><span class="sxs-lookup"><span data-stu-id="720e0-124">\_x4</span></span>     | <span data-ttu-id="720e0-125">Multiplicar por 4</span><span class="sxs-lookup"><span data-stu-id="720e0-125">Multiply by 4</span></span>                 | <span data-ttu-id="720e0-126">\_X4 instruções</span><span class="sxs-lookup"><span data-stu-id="720e0-126">instruction\_x4</span></span>  | <span data-ttu-id="720e0-127">X</span><span class="sxs-lookup"><span data-stu-id="720e0-127">X</span></span>       | <span data-ttu-id="720e0-128">X</span><span class="sxs-lookup"><span data-stu-id="720e0-128">X</span></span>    | <span data-ttu-id="720e0-129">X</span><span class="sxs-lookup"><span data-stu-id="720e0-129">X</span></span>    | <span data-ttu-id="720e0-130">X</span><span class="sxs-lookup"><span data-stu-id="720e0-130">X</span></span>    |
| <span data-ttu-id="720e0-131">\_x8</span><span class="sxs-lookup"><span data-stu-id="720e0-131">\_x8</span></span>     | <span data-ttu-id="720e0-132">Multiplicar por 8</span><span class="sxs-lookup"><span data-stu-id="720e0-132">Multiply by 8</span></span>                 | <span data-ttu-id="720e0-133">x8 de instruções \_</span><span class="sxs-lookup"><span data-stu-id="720e0-133">instruction\_x8</span></span>  |         |      |      | <span data-ttu-id="720e0-134">X</span><span class="sxs-lookup"><span data-stu-id="720e0-134">X</span></span>    |
| <span data-ttu-id="720e0-135">\_D2</span><span class="sxs-lookup"><span data-stu-id="720e0-135">\_d2</span></span>     | <span data-ttu-id="720e0-136">Dividir por 2</span><span class="sxs-lookup"><span data-stu-id="720e0-136">Divide by 2</span></span>                   | <span data-ttu-id="720e0-137">instrução \_ D2</span><span class="sxs-lookup"><span data-stu-id="720e0-137">instruction\_d2</span></span>  | <span data-ttu-id="720e0-138">X</span><span class="sxs-lookup"><span data-stu-id="720e0-138">X</span></span>       | <span data-ttu-id="720e0-139">X</span><span class="sxs-lookup"><span data-stu-id="720e0-139">X</span></span>    | <span data-ttu-id="720e0-140">X</span><span class="sxs-lookup"><span data-stu-id="720e0-140">X</span></span>    | <span data-ttu-id="720e0-141">X</span><span class="sxs-lookup"><span data-stu-id="720e0-141">X</span></span>    |
| <span data-ttu-id="720e0-142">\_D4</span><span class="sxs-lookup"><span data-stu-id="720e0-142">\_d4</span></span>     | <span data-ttu-id="720e0-143">Dividir por 4</span><span class="sxs-lookup"><span data-stu-id="720e0-143">Divide by 4</span></span>                   | <span data-ttu-id="720e0-144">instrução \_ D4</span><span class="sxs-lookup"><span data-stu-id="720e0-144">instruction\_d4</span></span>  |         |      |      | <span data-ttu-id="720e0-145">X</span><span class="sxs-lookup"><span data-stu-id="720e0-145">X</span></span>    |
| <span data-ttu-id="720e0-146">\_D8</span><span class="sxs-lookup"><span data-stu-id="720e0-146">\_d8</span></span>     | <span data-ttu-id="720e0-147">Dividir por 8</span><span class="sxs-lookup"><span data-stu-id="720e0-147">Divide by 8</span></span>                   | <span data-ttu-id="720e0-148">instrução \_ D8</span><span class="sxs-lookup"><span data-stu-id="720e0-148">instruction\_d8</span></span>  |         |      |      | <span data-ttu-id="720e0-149">X</span><span class="sxs-lookup"><span data-stu-id="720e0-149">X</span></span>    |
| <span data-ttu-id="720e0-150">\_saturação</span><span class="sxs-lookup"><span data-stu-id="720e0-150">\_sat</span></span>    | <span data-ttu-id="720e0-151">Saturação (fixe de 0 e 1)</span><span class="sxs-lookup"><span data-stu-id="720e0-151">Saturate (clamp from 0 and 1)</span></span> | <span data-ttu-id="720e0-152">instrução \_ SAT</span><span class="sxs-lookup"><span data-stu-id="720e0-152">instruction\_sat</span></span> | <span data-ttu-id="720e0-153">X</span><span class="sxs-lookup"><span data-stu-id="720e0-153">X</span></span>       | <span data-ttu-id="720e0-154">X</span><span class="sxs-lookup"><span data-stu-id="720e0-154">X</span></span>    | <span data-ttu-id="720e0-155">X</span><span class="sxs-lookup"><span data-stu-id="720e0-155">X</span></span>    | <span data-ttu-id="720e0-156">X</span><span class="sxs-lookup"><span data-stu-id="720e0-156">X</span></span>    |



 

-   <span data-ttu-id="720e0-157">O modificador de multiplicação multiplica os dados de registro por uma potência de dois após sua leitura.</span><span class="sxs-lookup"><span data-stu-id="720e0-157">The multiply modifier multiplies the register data by a power of two after it is read.</span></span> <span data-ttu-id="720e0-158">Isso é o mesmo que uma mudança à esquerda.</span><span class="sxs-lookup"><span data-stu-id="720e0-158">This is the same as a shift left.</span></span>
-   <span data-ttu-id="720e0-159">O modificador de divisão divide os dados de registro por uma potência de dois após sua leitura.</span><span class="sxs-lookup"><span data-stu-id="720e0-159">The divide modifier divides the register data by a power of two after it is read.</span></span> <span data-ttu-id="720e0-160">Isso é o mesmo que uma mudança à direita.</span><span class="sxs-lookup"><span data-stu-id="720e0-160">This is the same as a shift right.</span></span>
-   <span data-ttu-id="720e0-161">O modificador saturação coloca o intervalo de valores de registro de zero para um.</span><span class="sxs-lookup"><span data-stu-id="720e0-161">The saturate modifier clamps the range of register values from zero to one.</span></span>

<span data-ttu-id="720e0-162">Os modificadores de instrução podem ser usados em instruções aritméticas.</span><span class="sxs-lookup"><span data-stu-id="720e0-162">Instruction modifiers can be used on arithmetic instructions.</span></span> <span data-ttu-id="720e0-163">Eles não podem ser usados em instruções de endereço de textura.</span><span class="sxs-lookup"><span data-stu-id="720e0-163">They may not be used on texture address instructions.</span></span>

<span data-ttu-id="720e0-164">Modificador de multiplicação</span><span class="sxs-lookup"><span data-stu-id="720e0-164">Multiply modifier</span></span>

<span data-ttu-id="720e0-165">Este exemplo carrega o registro de destino (dest) com a soma das duas cores nos operandos de origem (src0 e src1) e multiplica o resultado por dois.</span><span class="sxs-lookup"><span data-stu-id="720e0-165">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and multiplies the result by two.</span></span>


```
add_x2 dest, src0, src1
```



<span data-ttu-id="720e0-166">Este exemplo combina dois modificadores de instrução.</span><span class="sxs-lookup"><span data-stu-id="720e0-166">This example combines two instruction modifiers.</span></span> <span data-ttu-id="720e0-167">Primeiro, duas cores nos operandos de origem (src0 e src1) são adicionadas.</span><span class="sxs-lookup"><span data-stu-id="720e0-167">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="720e0-168">Em seguida, o resultado é multiplicado por dois e clamped entre 0,0 e 1,0 para cada componente.</span><span class="sxs-lookup"><span data-stu-id="720e0-168">The result is then multiplied by two, and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="720e0-169">O resultado é salvo no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="720e0-169">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



<span data-ttu-id="720e0-170">Modificador de divisão</span><span class="sxs-lookup"><span data-stu-id="720e0-170">Divide modifier</span></span>

<span data-ttu-id="720e0-171">Este exemplo carrega o registro de destino (dest) com a soma das duas cores nos operandos de origem (src0 e src1) e divide o resultado por dois.</span><span class="sxs-lookup"><span data-stu-id="720e0-171">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and divides the result by two.</span></span>


```
add_d2 dest, src0, src1
```



<span data-ttu-id="720e0-172">Modificador saturado</span><span class="sxs-lookup"><span data-stu-id="720e0-172">Saturate modifier</span></span>

<span data-ttu-id="720e0-173">Para obter instruções aritméticas, o modificador de saturação coloca o resultado dessa instrução no intervalo de 0,0 a 1,0 para cada componente.</span><span class="sxs-lookup"><span data-stu-id="720e0-173">For arithmetic instructions, the saturation modifier clamps the result of this instruction into the range 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="720e0-174">O exemplo a seguir mostra como usar esse modificador de instrução.</span><span class="sxs-lookup"><span data-stu-id="720e0-174">The following example shows how to use this instruction modifier.</span></span>


```
dp3_sat r0, t0_bx2, v0_bx2    ; t0 is bump, v0 is light direction
```



<span data-ttu-id="720e0-175">Essa operação ocorre depois de qualquer modificador de instrução de multiplicação ou de divisão.</span><span class="sxs-lookup"><span data-stu-id="720e0-175">This operation occurs after any multiply or divide instruction modifier.</span></span> <span data-ttu-id="720e0-176">\_SAT é usado com mais frequência para fixe pontos de produtos.</span><span class="sxs-lookup"><span data-stu-id="720e0-176">\_sat is most often used to clamp dot product results.</span></span> <span data-ttu-id="720e0-177">No entanto, ele também habilita a emulação consistente de métodos de várias passagens, em que o buffer de quadro está sempre no intervalo de 0 a 1 e da sintaxe multitextura DirectX 6 e 7,0, na qual a saturação é definida para ocorrer em cada estágio.</span><span class="sxs-lookup"><span data-stu-id="720e0-177">However, it also enables consistent emulation of multipass methods where the frame buffer is always in the range 0 to 1, and of DirectX 6 and 7.0 multitexture syntax, in which saturation is defined to occur at every stage.</span></span>

<span data-ttu-id="720e0-178">Este exemplo carrega o registro de destino (dest) com a soma das duas cores nos operandos de origem (src0 e src1) e coloca o resultado no intervalo de 0,0 a 1,0 para cada componente.</span><span class="sxs-lookup"><span data-stu-id="720e0-178">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1), and clamps the result into the range 0.0 to 1.0 for each component.</span></span>


```
add_sat dest, src0, src1
```



<span data-ttu-id="720e0-179">Este exemplo combina dois modificadores de instrução.</span><span class="sxs-lookup"><span data-stu-id="720e0-179">This example combines two instruction modifiers.</span></span> <span data-ttu-id="720e0-180">Primeiro, duas cores nos operandos de origem (src0 e src1) são adicionadas.</span><span class="sxs-lookup"><span data-stu-id="720e0-180">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="720e0-181">O resultado é multiplicado por dois e clamped entre 0,0 e 1,0 para cada componente.</span><span class="sxs-lookup"><span data-stu-id="720e0-181">The result is multiplied by two and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="720e0-182">O resultado é salvo no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="720e0-182">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



## <a name="related-topics"></a><span data-ttu-id="720e0-183">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="720e0-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="720e0-184">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="720e0-184">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




