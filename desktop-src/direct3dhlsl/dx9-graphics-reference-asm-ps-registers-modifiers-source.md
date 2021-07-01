---
title: Modificadores de registro de origem do sombreador de pixel
description: Use modificadores de registro de origem para alterar o valor lido de um registro antes de uma instrução ser executada.
ms.assetid: b45d0919-7878-4184-ad4a-5623aae9d1f1
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a9dd4476dd7a1a885edb2e62a29b5127f5ff0a14
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129673"
---
# <a name="pixel-shader-source-register-modifiers"></a><span data-ttu-id="3f4a9-103">Modificadores de registro de origem do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="3f4a9-103">Pixel Shader Source Register Modifiers</span></span>

<span data-ttu-id="3f4a9-104">Use modificadores de registro de origem para alterar o valor lido de um registro antes de uma instrução ser executada.</span><span class="sxs-lookup"><span data-stu-id="3f4a9-104">Use source register modifiers to change the value read from a register before an instruction runs.</span></span> <span data-ttu-id="3f4a9-105">O conteúdo de um registro de origem permanece inalterado.</span><span class="sxs-lookup"><span data-stu-id="3f4a9-105">The contents of a source register are left unchanged.</span></span> <span data-ttu-id="3f4a9-106">Os modificadores são úteis para ajustar o intervalo de dados de registro em preparação para a instrução.</span><span class="sxs-lookup"><span data-stu-id="3f4a9-106">Modifiers are useful for adjusting the range of register data in preparation for the instruction.</span></span> <span data-ttu-id="3f4a9-107">Um conjunto de modificadores chamados seletores copia ou replica os dados de um único canal (r, g, b, a) para os outros canais.</span><span class="sxs-lookup"><span data-stu-id="3f4a9-107">A set of modifiers called selectors copies or replicates the data from a single channel (r,g,b,a) into the other channels.</span></span>

## <a name="ps_1_1---ps_1_4"></a><span data-ttu-id="3f4a9-108">PS \_ 1 \_ 1-PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="3f4a9-108">ps\_1\_1 - ps\_1\_4</span></span>

<span data-ttu-id="3f4a9-109">Esta tabela identifica as versões que oferecem suporte a cada modificador:</span><span class="sxs-lookup"><span data-stu-id="3f4a9-109">This table identifies the versions that support each modifier:</span></span>



| <span data-ttu-id="3f4a9-110">Modificadores de registro de origem</span><span class="sxs-lookup"><span data-stu-id="3f4a9-110">Source register modifiers</span></span>                                                                                    | <span data-ttu-id="3f4a9-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f4a9-111">Syntax</span></span>         | <span data-ttu-id="3f4a9-112">Versão 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="3f4a9-112">Version 1\_1</span></span> | <span data-ttu-id="3f4a9-113">Versão 1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="3f4a9-113">Version 1\_2</span></span>     | <span data-ttu-id="3f4a9-114">Versão 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3f4a9-114">Version 1\_3</span></span>     | <span data-ttu-id="3f4a9-115">Versão 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="3f4a9-115">Version 1\_4</span></span>     |
|--------------------------------------------------------------------------------------------------------------|----------------|---------|------|------|------|
| [<span data-ttu-id="3f4a9-116">Bias</span><span class="sxs-lookup"><span data-stu-id="3f4a9-116">bias</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-bias.md)                                           | <span data-ttu-id="3f4a9-117">registrar \_ diferença</span><span class="sxs-lookup"><span data-stu-id="3f4a9-117">register\_bias</span></span> | <span data-ttu-id="3f4a9-118">X</span><span class="sxs-lookup"><span data-stu-id="3f4a9-118">X</span></span>       | <span data-ttu-id="3f4a9-119">X</span><span class="sxs-lookup"><span data-stu-id="3f4a9-119">X</span></span>    | <span data-ttu-id="3f4a9-120">X</span><span class="sxs-lookup"><span data-stu-id="3f4a9-120">X</span></span>    | <span data-ttu-id="3f4a9-121">X</span><span class="sxs-lookup"><span data-stu-id="3f4a9-121">X</span></span>    |
| [<span data-ttu-id="3f4a9-122">minúsculo</span><span class="sxs-lookup"><span data-stu-id="3f4a9-122">invert</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)                                       | <span data-ttu-id="3f4a9-123">1-registrar</span><span class="sxs-lookup"><span data-stu-id="3f4a9-123">1 - register</span></span>   | <span data-ttu-id="3f4a9-124">X</span><span class="sxs-lookup"><span data-stu-id="3f4a9-124">X</span></span>       | <span data-ttu-id="3f4a9-125">X</span><span class="sxs-lookup"><span data-stu-id="3f4a9-125">X</span></span>    | <span data-ttu-id="3f4a9-126">X</span><span class="sxs-lookup"><span data-stu-id="3f4a9-126">X</span></span>    | <span data-ttu-id="3f4a9-127">X</span><span class="sxs-lookup"><span data-stu-id="3f4a9-127">X</span></span>    |
| [<span data-ttu-id="3f4a9-128">negate</span><span class="sxs-lookup"><span data-stu-id="3f4a9-128">negate</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-negate.md)                                       | <span data-ttu-id="3f4a9-129">\- Registr</span><span class="sxs-lookup"><span data-stu-id="3f4a9-129">\- register</span></span>    | <span data-ttu-id="3f4a9-130">X</span><span class="sxs-lookup"><span data-stu-id="3f4a9-130">X</span></span>       | <span data-ttu-id="3f4a9-131">X</span><span class="sxs-lookup"><span data-stu-id="3f4a9-131">X</span></span>    | <span data-ttu-id="3f4a9-132">X</span><span class="sxs-lookup"><span data-stu-id="3f4a9-132">X</span></span>    | <span data-ttu-id="3f4a9-133">X</span><span class="sxs-lookup"><span data-stu-id="3f4a9-133">X</span></span>    |
| [<span data-ttu-id="3f4a9-134">escala por 2</span><span class="sxs-lookup"><span data-stu-id="3f4a9-134">scale by 2</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md)                                 | <span data-ttu-id="3f4a9-135">registrar \_ X2</span><span class="sxs-lookup"><span data-stu-id="3f4a9-135">register\_x2</span></span>   |         |      |      | <span data-ttu-id="3f4a9-136">X</span><span class="sxs-lookup"><span data-stu-id="3f4a9-136">X</span></span>    |
| [<span data-ttu-id="3f4a9-137">dimensionamento assinado</span><span class="sxs-lookup"><span data-stu-id="3f4a9-137">signed scaling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md)                         | <span data-ttu-id="3f4a9-138">registrar \_ BX2</span><span class="sxs-lookup"><span data-stu-id="3f4a9-138">register\_bx2</span></span>  | <span data-ttu-id="3f4a9-139">X</span><span class="sxs-lookup"><span data-stu-id="3f4a9-139">X</span></span>       | <span data-ttu-id="3f4a9-140">X</span><span class="sxs-lookup"><span data-stu-id="3f4a9-140">X</span></span>    | <span data-ttu-id="3f4a9-141">X</span><span class="sxs-lookup"><span data-stu-id="3f4a9-141">X</span></span>    | <span data-ttu-id="3f4a9-142">X</span><span class="sxs-lookup"><span data-stu-id="3f4a9-142">X</span></span>    |
| [<span data-ttu-id="3f4a9-143">modificadores texld e texcrd</span><span class="sxs-lookup"><span data-stu-id="3f4a9-143">texld and texcrd modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-ps-1-4.md)                   | <span data-ttu-id="3f4a9-144">registrar \_ d\*</span><span class="sxs-lookup"><span data-stu-id="3f4a9-144">register\_d\*</span></span>  | <span data-ttu-id="3f4a9-145">X</span><span class="sxs-lookup"><span data-stu-id="3f4a9-145">X</span></span>       | <span data-ttu-id="3f4a9-146">X</span><span class="sxs-lookup"><span data-stu-id="3f4a9-146">X</span></span>    | <span data-ttu-id="3f4a9-147">X</span><span class="sxs-lookup"><span data-stu-id="3f4a9-147">X</span></span>    | <span data-ttu-id="3f4a9-148">X</span><span class="sxs-lookup"><span data-stu-id="3f4a9-148">X</span></span>    |
| [<span data-ttu-id="3f4a9-149">swizzling de registro de origem</span><span class="sxs-lookup"><span data-stu-id="3f4a9-149">source register swizzling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) | <span data-ttu-id="3f4a9-150">registrar. xyzw</span><span class="sxs-lookup"><span data-stu-id="3f4a9-150">register.xyzw</span></span>  | <span data-ttu-id="3f4a9-151">X</span><span class="sxs-lookup"><span data-stu-id="3f4a9-151">X</span></span>       | <span data-ttu-id="3f4a9-152">X</span><span class="sxs-lookup"><span data-stu-id="3f4a9-152">X</span></span>    | <span data-ttu-id="3f4a9-153">X</span><span class="sxs-lookup"><span data-stu-id="3f4a9-153">X</span></span>    | <span data-ttu-id="3f4a9-154">X</span><span class="sxs-lookup"><span data-stu-id="3f4a9-154">X</span></span>    |



 

<span data-ttu-id="3f4a9-155">Modificadores de registro de origem só podem ser usados em instruções aritméticas.</span><span class="sxs-lookup"><span data-stu-id="3f4a9-155">Source register modifiers can be used only on arithmetic instructions.</span></span> <span data-ttu-id="3f4a9-156">Eles não podem ser usados em instruções de endereço de textura.</span><span class="sxs-lookup"><span data-stu-id="3f4a9-156">They cannot be used on texture address instructions.</span></span> <span data-ttu-id="3f4a9-157">A exceção a isso é o modificador de [escala por 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) .</span><span class="sxs-lookup"><span data-stu-id="3f4a9-157">The exception to this is the [scale by 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) modifier.</span></span> <span data-ttu-id="3f4a9-158">Para a versão 1 \_ 1, a escala assinada pode ser usada no argumento de origem de qualquer \* instrução texm.</span><span class="sxs-lookup"><span data-stu-id="3f4a9-158">For version 1\_1, signed scale can be used on the source argument of any texm\* instruction.</span></span> <span data-ttu-id="3f4a9-159">Para a versão 1 \_ 2 ou 1 \_ 3, a escala assinada pode ser usada no argumento de origem de qualquer instrução de endereço de textura.</span><span class="sxs-lookup"><span data-stu-id="3f4a9-159">For version 1\_2 or 1\_3, signed scale can be used on the source argument of any texture address instruction.</span></span>

<span data-ttu-id="3f4a9-160">Algumas restrições específicas de modificador:</span><span class="sxs-lookup"><span data-stu-id="3f4a9-160">Some modifier specific restrictions:</span></span>

-   <span data-ttu-id="3f4a9-161">O negar pode ser combinado com o modificador de tendência, dimensionamento assinado ou scalex2.</span><span class="sxs-lookup"><span data-stu-id="3f4a9-161">Negate can be combined with either the bias, signed scaling, or scalex2 modifier.</span></span> <span data-ttu-id="3f4a9-162">Quando combinado, negar é executado por último.</span><span class="sxs-lookup"><span data-stu-id="3f4a9-162">When combined, negate is run last.</span></span>
-   <span data-ttu-id="3f4a9-163">Invert não pode ser combinado com nenhum outro modificador.</span><span class="sxs-lookup"><span data-stu-id="3f4a9-163">Invert cannot be combined with any other modifier.</span></span>
-   <span data-ttu-id="3f4a9-164">Invert, negação, tendência, dimensionamento assinado e scalex2 podem ser combinados com qualquer um dos seletores.</span><span class="sxs-lookup"><span data-stu-id="3f4a9-164">Invert, negate, bias, signed scaling, and scalex2 can be combined with any of the selectors.</span></span>
-   <span data-ttu-id="3f4a9-165">Os modificadores de registro de origem não devem ser usados em registros constantes porque eles causarão resultados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="3f4a9-165">Source register modifiers should not be used on constant registers because they will cause undefined results.</span></span> <span data-ttu-id="3f4a9-166">Para a versão 1 \_ 4, os modificadores em constantes não são permitidos e ocorrerão falha na validação.</span><span class="sxs-lookup"><span data-stu-id="3f4a9-166">For version 1\_4, modifiers on constants are not allowed and will fail validation.</span></span>

## <a name="ps_2_0-and-above"></a><span data-ttu-id="3f4a9-167">PS \_ 2 \_ 0 e superior</span><span class="sxs-lookup"><span data-stu-id="3f4a9-167">ps\_2\_0 and Above</span></span>

<span data-ttu-id="3f4a9-168">Para a versão PS \_ 2 \_ 0 e superior, o número de modificadores foi simplificado.</span><span class="sxs-lookup"><span data-stu-id="3f4a9-168">For version ps\_2\_0 and up, the number of modifiers has been simplified.</span></span>

### <a name="negate"></a><span data-ttu-id="3f4a9-169">Negar</span><span class="sxs-lookup"><span data-stu-id="3f4a9-169">Negate</span></span>

<span data-ttu-id="3f4a9-170">Negar o conteúdo do registro de origem.</span><span class="sxs-lookup"><span data-stu-id="3f4a9-170">Negate the contents of the source register.</span></span>



| <span data-ttu-id="3f4a9-171">Modificador de componente</span><span class="sxs-lookup"><span data-stu-id="3f4a9-171">Component modifier</span></span> | <span data-ttu-id="3f4a9-172">Descrição</span><span class="sxs-lookup"><span data-stu-id="3f4a9-172">Description</span></span>     |
|--------------------|-----------------|
| <span data-ttu-id="3f4a9-173">\- d</span><span class="sxs-lookup"><span data-stu-id="3f4a9-173">\- r</span></span>               | <span data-ttu-id="3f4a9-174">Negação de origem</span><span class="sxs-lookup"><span data-stu-id="3f4a9-174">Source negation</span></span> |



 

<span data-ttu-id="3f4a9-175">O modificador de negação não pode ser usado no segundo registro de origem dessas instruções: [M3X2-PS](m3x2---ps.md), [m3x3-PS](m3x3---ps.md), [M3x4-PS](m3x4---ps.md), [m4x3-PS](m4x3---ps.md)e [m4x4-PS](m4x4---ps.md).</span><span class="sxs-lookup"><span data-stu-id="3f4a9-175">The negate modifier cannot be used on second source register of these instructions: [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md), and [m4x4 - ps](m4x4---ps.md).</span></span>



| <span data-ttu-id="3f4a9-176">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="3f4a9-176">Pixel shader versions</span></span> | <span data-ttu-id="3f4a9-177">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3f4a9-177">2\_0</span></span> | <span data-ttu-id="3f4a9-178">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3f4a9-178">2\_x</span></span> | <span data-ttu-id="3f4a9-179">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3f4a9-179">2\_sw</span></span> | <span data-ttu-id="3f4a9-180">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3f4a9-180">3\_0</span></span> | <span data-ttu-id="3f4a9-181">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3f4a9-181">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| \-                    | <span data-ttu-id="3f4a9-182">x</span><span class="sxs-lookup"><span data-stu-id="3f4a9-182">x</span></span>    | <span data-ttu-id="3f4a9-183">x</span><span class="sxs-lookup"><span data-stu-id="3f4a9-183">x</span></span>    | <span data-ttu-id="3f4a9-184">x</span><span class="sxs-lookup"><span data-stu-id="3f4a9-184">x</span></span>     | <span data-ttu-id="3f4a9-185">x</span><span class="sxs-lookup"><span data-stu-id="3f4a9-185">x</span></span>    | <span data-ttu-id="3f4a9-186">x</span><span class="sxs-lookup"><span data-stu-id="3f4a9-186">x</span></span>     |



 

### <a name="absolute-value"></a><span data-ttu-id="3f4a9-187">Valor absoluto</span><span class="sxs-lookup"><span data-stu-id="3f4a9-187">Absolute Value</span></span>

<span data-ttu-id="3f4a9-188">Pegue o valor absoluto do registro.</span><span class="sxs-lookup"><span data-stu-id="3f4a9-188">Take the absolute value of the register.</span></span>



| <span data-ttu-id="3f4a9-189">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="3f4a9-189">Pixel shader versions</span></span> | <span data-ttu-id="3f4a9-190">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3f4a9-190">2\_0</span></span> | <span data-ttu-id="3f4a9-191">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3f4a9-191">2\_x</span></span> | <span data-ttu-id="3f4a9-192">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3f4a9-192">2\_sw</span></span> | <span data-ttu-id="3f4a9-193">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3f4a9-193">3\_0</span></span> | <span data-ttu-id="3f4a9-194">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3f4a9-194">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| <span data-ttu-id="3f4a9-195">abs</span><span class="sxs-lookup"><span data-stu-id="3f4a9-195">abs</span></span>                   |      |      |       | <span data-ttu-id="3f4a9-196">x</span><span class="sxs-lookup"><span data-stu-id="3f4a9-196">x</span></span>    | <span data-ttu-id="3f4a9-197">x</span><span class="sxs-lookup"><span data-stu-id="3f4a9-197">x</span></span>     |



 

<span data-ttu-id="3f4a9-198">Se qualquer sombreador da versão 3 ler um ou mais registros de flutuação constante (c \# ), um dos seguintes deve ser verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="3f4a9-198">If any version 3 shader reads from one or more constant float registers (c\#), one of the following must be true.</span></span>

-   <span data-ttu-id="3f4a9-199">Todos os registros constantes de ponto flutuante devem usar o modificador ABS.</span><span class="sxs-lookup"><span data-stu-id="3f4a9-199">All of the constant floating-point registers must use the abs modifier.</span></span>
-   <span data-ttu-id="3f4a9-200">Nenhum dos registros constantes de ponto flutuante pode usar o modificador ABS.</span><span class="sxs-lookup"><span data-stu-id="3f4a9-200">None of the constant floating-point registers can use the abs modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f4a9-201">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3f4a9-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f4a9-202">Modificadores de registro do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="3f4a9-202">Pixel Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




