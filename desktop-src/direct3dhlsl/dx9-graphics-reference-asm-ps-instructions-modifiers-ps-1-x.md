---
title: Modificadores para ps_1_X
description: Os modificadores de instrução afetam o resultado da instrução antes de serem gravados no registro de destino.
ms.assetid: 15b892da-b6fd-4bd5-8889-bc48035e7819
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bbc8a9b13f7ffc29cf84bc839409f29bea6c8c8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823039"
---
# <a name="modifiers-for-ps_1_x"></a><span data-ttu-id="ce822-103">Modificadores para PS \_ 1 \_ X</span><span class="sxs-lookup"><span data-stu-id="ce822-103">Modifiers for ps\_1\_X</span></span>

<span data-ttu-id="ce822-104">Os modificadores de instrução afetam o resultado da instrução antes de serem gravados no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="ce822-104">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span> <span data-ttu-id="ce822-105">Por exemplo, use-os para multiplicar ou dividir o resultado por um fator de dois ou para fixe o resultado entre zero e um.</span><span class="sxs-lookup"><span data-stu-id="ce822-105">For instance, use them to multiply or divide the result by a factor of two, or to clamp the result between zero and one.</span></span> <span data-ttu-id="ce822-106">Os modificadores de instrução são aplicados depois que a instrução é executada, mas antes de gravar o resultado no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="ce822-106">Instruction modifiers are applied after the instruction runs but before writing the result to the destination register.</span></span>

<span data-ttu-id="ce822-107">Uma lista dos modificadores é mostrada abaixo.</span><span class="sxs-lookup"><span data-stu-id="ce822-107">A list of the modifiers is shown below.</span></span>



| <span data-ttu-id="ce822-108">Modificador</span><span class="sxs-lookup"><span data-stu-id="ce822-108">Modifier</span></span> | <span data-ttu-id="ce822-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce822-109">Description</span></span>                   | <span data-ttu-id="ce822-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce822-110">Syntax</span></span>           | <span data-ttu-id="ce822-111">Versão</span><span class="sxs-lookup"><span data-stu-id="ce822-111">Version</span></span> |      |      |      |
|----------|-------------------------------|------------------|---------|------|------|------|
|          |                               |                  | <span data-ttu-id="ce822-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="ce822-112">1\_1</span></span>    | <span data-ttu-id="ce822-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="ce822-113">1\_2</span></span> | <span data-ttu-id="ce822-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="ce822-114">1\_3</span></span> | <span data-ttu-id="ce822-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="ce822-115">1\_4</span></span> |
| <span data-ttu-id="ce822-116">\_X2</span><span class="sxs-lookup"><span data-stu-id="ce822-116">\_x2</span></span>     | <span data-ttu-id="ce822-117">Multiplicar por 2</span><span class="sxs-lookup"><span data-stu-id="ce822-117">Multiply by 2</span></span>                 | <span data-ttu-id="ce822-118">instrução \_ X2</span><span class="sxs-lookup"><span data-stu-id="ce822-118">instruction\_x2</span></span>  | <span data-ttu-id="ce822-119">X</span><span class="sxs-lookup"><span data-stu-id="ce822-119">X</span></span>       | <span data-ttu-id="ce822-120">X</span><span class="sxs-lookup"><span data-stu-id="ce822-120">X</span></span>    | <span data-ttu-id="ce822-121">X</span><span class="sxs-lookup"><span data-stu-id="ce822-121">X</span></span>    | <span data-ttu-id="ce822-122">X</span><span class="sxs-lookup"><span data-stu-id="ce822-122">X</span></span>    |
| <span data-ttu-id="ce822-123">\_X4</span><span class="sxs-lookup"><span data-stu-id="ce822-123">\_x4</span></span>     | <span data-ttu-id="ce822-124">Multiplicar por 4</span><span class="sxs-lookup"><span data-stu-id="ce822-124">Multiply by 4</span></span>                 | <span data-ttu-id="ce822-125">\_X4 instruções</span><span class="sxs-lookup"><span data-stu-id="ce822-125">instruction\_x4</span></span>  | <span data-ttu-id="ce822-126">X</span><span class="sxs-lookup"><span data-stu-id="ce822-126">X</span></span>       | <span data-ttu-id="ce822-127">X</span><span class="sxs-lookup"><span data-stu-id="ce822-127">X</span></span>    | <span data-ttu-id="ce822-128">X</span><span class="sxs-lookup"><span data-stu-id="ce822-128">X</span></span>    | <span data-ttu-id="ce822-129">X</span><span class="sxs-lookup"><span data-stu-id="ce822-129">X</span></span>    |
| <span data-ttu-id="ce822-130">\_x8</span><span class="sxs-lookup"><span data-stu-id="ce822-130">\_x8</span></span>     | <span data-ttu-id="ce822-131">Multiplicar por 8</span><span class="sxs-lookup"><span data-stu-id="ce822-131">Multiply by 8</span></span>                 | <span data-ttu-id="ce822-132">x8 de instruções \_</span><span class="sxs-lookup"><span data-stu-id="ce822-132">instruction\_x8</span></span>  |         |      |      | <span data-ttu-id="ce822-133">X</span><span class="sxs-lookup"><span data-stu-id="ce822-133">X</span></span>    |
| <span data-ttu-id="ce822-134">\_D2</span><span class="sxs-lookup"><span data-stu-id="ce822-134">\_d2</span></span>     | <span data-ttu-id="ce822-135">Dividir por 2</span><span class="sxs-lookup"><span data-stu-id="ce822-135">Divide by 2</span></span>                   | <span data-ttu-id="ce822-136">instrução \_ D2</span><span class="sxs-lookup"><span data-stu-id="ce822-136">instruction\_d2</span></span>  | <span data-ttu-id="ce822-137">X</span><span class="sxs-lookup"><span data-stu-id="ce822-137">X</span></span>       | <span data-ttu-id="ce822-138">X</span><span class="sxs-lookup"><span data-stu-id="ce822-138">X</span></span>    | <span data-ttu-id="ce822-139">X</span><span class="sxs-lookup"><span data-stu-id="ce822-139">X</span></span>    | <span data-ttu-id="ce822-140">X</span><span class="sxs-lookup"><span data-stu-id="ce822-140">X</span></span>    |
| <span data-ttu-id="ce822-141">\_D4</span><span class="sxs-lookup"><span data-stu-id="ce822-141">\_d4</span></span>     | <span data-ttu-id="ce822-142">Dividir por 4</span><span class="sxs-lookup"><span data-stu-id="ce822-142">Divide by 4</span></span>                   | <span data-ttu-id="ce822-143">instrução \_ D4</span><span class="sxs-lookup"><span data-stu-id="ce822-143">instruction\_d4</span></span>  |         |      |      | <span data-ttu-id="ce822-144">X</span><span class="sxs-lookup"><span data-stu-id="ce822-144">X</span></span>    |
| <span data-ttu-id="ce822-145">\_D8</span><span class="sxs-lookup"><span data-stu-id="ce822-145">\_d8</span></span>     | <span data-ttu-id="ce822-146">Dividir por 8</span><span class="sxs-lookup"><span data-stu-id="ce822-146">Divide by 8</span></span>                   | <span data-ttu-id="ce822-147">instrução \_ D8</span><span class="sxs-lookup"><span data-stu-id="ce822-147">instruction\_d8</span></span>  |         |      |      | <span data-ttu-id="ce822-148">X</span><span class="sxs-lookup"><span data-stu-id="ce822-148">X</span></span>    |
| <span data-ttu-id="ce822-149">\_saturação</span><span class="sxs-lookup"><span data-stu-id="ce822-149">\_sat</span></span>    | <span data-ttu-id="ce822-150">Saturação (fixe de 0 e 1)</span><span class="sxs-lookup"><span data-stu-id="ce822-150">Saturate (clamp from 0 and 1)</span></span> | <span data-ttu-id="ce822-151">instrução \_ SAT</span><span class="sxs-lookup"><span data-stu-id="ce822-151">instruction\_sat</span></span> | <span data-ttu-id="ce822-152">X</span><span class="sxs-lookup"><span data-stu-id="ce822-152">X</span></span>       | <span data-ttu-id="ce822-153">X</span><span class="sxs-lookup"><span data-stu-id="ce822-153">X</span></span>    | <span data-ttu-id="ce822-154">X</span><span class="sxs-lookup"><span data-stu-id="ce822-154">X</span></span>    | <span data-ttu-id="ce822-155">X</span><span class="sxs-lookup"><span data-stu-id="ce822-155">X</span></span>    |



 

-   <span data-ttu-id="ce822-156">O modificador de multiplicação multiplica os dados de registro por uma potência de dois após sua leitura.</span><span class="sxs-lookup"><span data-stu-id="ce822-156">The multiply modifier multiplies the register data by a power of two after it is read.</span></span> <span data-ttu-id="ce822-157">Isso é o mesmo que uma mudança à esquerda.</span><span class="sxs-lookup"><span data-stu-id="ce822-157">This is the same as a shift left.</span></span>
-   <span data-ttu-id="ce822-158">O modificador de divisão divide os dados de registro por uma potência de dois após sua leitura.</span><span class="sxs-lookup"><span data-stu-id="ce822-158">The divide modifier divides the register data by a power of two after it is read.</span></span> <span data-ttu-id="ce822-159">Isso é o mesmo que uma mudança à direita.</span><span class="sxs-lookup"><span data-stu-id="ce822-159">This is the same as a shift right.</span></span>
-   <span data-ttu-id="ce822-160">O modificador saturação coloca o intervalo de valores de registro de zero para um.</span><span class="sxs-lookup"><span data-stu-id="ce822-160">The saturate modifier clamps the range of register values from zero to one.</span></span>

<span data-ttu-id="ce822-161">Os modificadores de instrução podem ser usados em instruções aritméticas.</span><span class="sxs-lookup"><span data-stu-id="ce822-161">Instruction modifiers can be used on arithmetic instructions.</span></span> <span data-ttu-id="ce822-162">Eles não podem ser usados em instruções de endereço de textura.</span><span class="sxs-lookup"><span data-stu-id="ce822-162">They may not be used on texture address instructions.</span></span>

<span data-ttu-id="ce822-163">Modificador de multiplicação</span><span class="sxs-lookup"><span data-stu-id="ce822-163">Multiply modifier</span></span>

<span data-ttu-id="ce822-164">Este exemplo carrega o registro de destino (dest) com a soma das duas cores nos operandos de origem (src0 e src1) e multiplica o resultado por dois.</span><span class="sxs-lookup"><span data-stu-id="ce822-164">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and multiplies the result by two.</span></span>


```
add_x2 dest, src0, src1
```



<span data-ttu-id="ce822-165">Este exemplo combina dois modificadores de instrução.</span><span class="sxs-lookup"><span data-stu-id="ce822-165">This example combines two instruction modifiers.</span></span> <span data-ttu-id="ce822-166">Primeiro, duas cores nos operandos de origem (src0 e src1) são adicionadas.</span><span class="sxs-lookup"><span data-stu-id="ce822-166">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="ce822-167">Em seguida, o resultado é multiplicado por dois e clamped entre 0,0 e 1,0 para cada componente.</span><span class="sxs-lookup"><span data-stu-id="ce822-167">The result is then multiplied by two, and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="ce822-168">O resultado é salvo no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="ce822-168">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



<span data-ttu-id="ce822-169">Modificador de divisão</span><span class="sxs-lookup"><span data-stu-id="ce822-169">Divide modifier</span></span>

<span data-ttu-id="ce822-170">Este exemplo carrega o registro de destino (dest) com a soma das duas cores nos operandos de origem (src0 e src1) e divide o resultado por dois.</span><span class="sxs-lookup"><span data-stu-id="ce822-170">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and divides the result by two.</span></span>


```
add_d2 dest, src0, src1
```



<span data-ttu-id="ce822-171">Modificador saturado</span><span class="sxs-lookup"><span data-stu-id="ce822-171">Saturate modifier</span></span>

<span data-ttu-id="ce822-172">Para obter instruções aritméticas, o modificador de saturação coloca o resultado dessa instrução no intervalo de 0,0 a 1,0 para cada componente.</span><span class="sxs-lookup"><span data-stu-id="ce822-172">For arithmetic instructions, the saturation modifier clamps the result of this instruction into the range 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="ce822-173">O exemplo a seguir mostra como usar esse modificador de instrução.</span><span class="sxs-lookup"><span data-stu-id="ce822-173">The following example shows how to use this instruction modifier.</span></span>


```
dp3_sat r0, t0_bx2, v0_bx2    ; t0 is bump, v0 is light direction
```



<span data-ttu-id="ce822-174">Essa operação ocorre depois de qualquer modificador de instrução de multiplicação ou de divisão.</span><span class="sxs-lookup"><span data-stu-id="ce822-174">This operation occurs after any multiply or divide instruction modifier.</span></span> <span data-ttu-id="ce822-175">\_SAT é usado com mais frequência para fixe pontos de produtos.</span><span class="sxs-lookup"><span data-stu-id="ce822-175">\_sat is most often used to clamp dot product results.</span></span> <span data-ttu-id="ce822-176">No entanto, ele também habilita a emulação consistente de métodos de várias passagens, em que o buffer de quadro está sempre no intervalo de 0 a 1 e da sintaxe multitextura DirectX 6 e 7,0, na qual a saturação é definida para ocorrer em cada estágio.</span><span class="sxs-lookup"><span data-stu-id="ce822-176">However, it also enables consistent emulation of multipass methods where the frame buffer is always in the range 0 to 1, and of DirectX 6 and 7.0 multitexture syntax, in which saturation is defined to occur at every stage.</span></span>

<span data-ttu-id="ce822-177">Este exemplo carrega o registro de destino (dest) com a soma das duas cores nos operandos de origem (src0 e src1) e coloca o resultado no intervalo de 0,0 a 1,0 para cada componente.</span><span class="sxs-lookup"><span data-stu-id="ce822-177">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1), and clamps the result into the range 0.0 to 1.0 for each component.</span></span>


```
add_sat dest, src0, src1
```



<span data-ttu-id="ce822-178">Este exemplo combina dois modificadores de instrução.</span><span class="sxs-lookup"><span data-stu-id="ce822-178">This example combines two instruction modifiers.</span></span> <span data-ttu-id="ce822-179">Primeiro, duas cores nos operandos de origem (src0 e src1) são adicionadas.</span><span class="sxs-lookup"><span data-stu-id="ce822-179">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="ce822-180">O resultado é multiplicado por dois e clamped entre 0,0 e 1,0 para cada componente.</span><span class="sxs-lookup"><span data-stu-id="ce822-180">The result is multiplied by two and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="ce822-181">O resultado é salvo no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="ce822-181">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



## <a name="related-topics"></a><span data-ttu-id="ce822-182">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ce822-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce822-183">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="ce822-183">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




