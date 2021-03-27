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
ms.openlocfilehash: 12cfee533a71408a445d97a63bbd8b76b281236b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292843"
---
# <a name="pixel-shader-source-register-modifiers"></a><span data-ttu-id="4dea5-103">Modificadores de registro de origem do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="4dea5-103">Pixel Shader Source Register Modifiers</span></span>

<span data-ttu-id="4dea5-104">Use modificadores de registro de origem para alterar o valor lido de um registro antes de uma instrução ser executada.</span><span class="sxs-lookup"><span data-stu-id="4dea5-104">Use source register modifiers to change the value read from a register before an instruction runs.</span></span> <span data-ttu-id="4dea5-105">O conteúdo de um registro de origem permanece inalterado.</span><span class="sxs-lookup"><span data-stu-id="4dea5-105">The contents of a source register are left unchanged.</span></span> <span data-ttu-id="4dea5-106">Os modificadores são úteis para ajustar o intervalo de dados de registro em preparação para a instrução.</span><span class="sxs-lookup"><span data-stu-id="4dea5-106">Modifiers are useful for adjusting the range of register data in preparation for the instruction.</span></span> <span data-ttu-id="4dea5-107">Um conjunto de modificadores chamados seletores copia ou replica os dados de um único canal (r, g, b, a) para os outros canais.</span><span class="sxs-lookup"><span data-stu-id="4dea5-107">A set of modifiers called selectors copies or replicates the data from a single channel (r,g,b,a) into the other channels.</span></span>

## <a name="ps_1_1---ps_1_4"></a><span data-ttu-id="4dea5-108">PS \_ 1 \_ 1-PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="4dea5-108">ps\_1\_1 - ps\_1\_4</span></span>

<span data-ttu-id="4dea5-109">Esta tabela identifica as versões que oferecem suporte a cada modificador:</span><span class="sxs-lookup"><span data-stu-id="4dea5-109">This table identifies the versions that support each modifier:</span></span>



| <span data-ttu-id="4dea5-110">Modificadores de registro de origem</span><span class="sxs-lookup"><span data-stu-id="4dea5-110">Source register modifiers</span></span>                                                                                    | <span data-ttu-id="4dea5-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="4dea5-111">Syntax</span></span>         | <span data-ttu-id="4dea5-112">Versão</span><span class="sxs-lookup"><span data-stu-id="4dea5-112">Version</span></span> |      |      |      |     |     |
|--------------------------------------------------------------------------------------------------------------|----------------|---------|------|------|------|-----|-----|
|                                                                                                              |                | <span data-ttu-id="4dea5-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="4dea5-113">1\_1</span></span>    | <span data-ttu-id="4dea5-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="4dea5-114">1\_2</span></span> | <span data-ttu-id="4dea5-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="4dea5-115">1\_3</span></span> | <span data-ttu-id="4dea5-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="4dea5-116">1\_4</span></span> |     |     |
| [<span data-ttu-id="4dea5-117">Bias</span><span class="sxs-lookup"><span data-stu-id="4dea5-117">bias</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-bias.md)                                           | <span data-ttu-id="4dea5-118">registrar \_ diferença</span><span class="sxs-lookup"><span data-stu-id="4dea5-118">register\_bias</span></span> | <span data-ttu-id="4dea5-119">X</span><span class="sxs-lookup"><span data-stu-id="4dea5-119">X</span></span>       | <span data-ttu-id="4dea5-120">X</span><span class="sxs-lookup"><span data-stu-id="4dea5-120">X</span></span>    | <span data-ttu-id="4dea5-121">X</span><span class="sxs-lookup"><span data-stu-id="4dea5-121">X</span></span>    | <span data-ttu-id="4dea5-122">X</span><span class="sxs-lookup"><span data-stu-id="4dea5-122">X</span></span>    |     |     |
| [<span data-ttu-id="4dea5-123">minúsculo</span><span class="sxs-lookup"><span data-stu-id="4dea5-123">invert</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)                                       | <span data-ttu-id="4dea5-124">1-registrar</span><span class="sxs-lookup"><span data-stu-id="4dea5-124">1 - register</span></span>   | <span data-ttu-id="4dea5-125">X</span><span class="sxs-lookup"><span data-stu-id="4dea5-125">X</span></span>       | <span data-ttu-id="4dea5-126">X</span><span class="sxs-lookup"><span data-stu-id="4dea5-126">X</span></span>    | <span data-ttu-id="4dea5-127">X</span><span class="sxs-lookup"><span data-stu-id="4dea5-127">X</span></span>    | <span data-ttu-id="4dea5-128">X</span><span class="sxs-lookup"><span data-stu-id="4dea5-128">X</span></span>    |     |     |
| [<span data-ttu-id="4dea5-129">negate</span><span class="sxs-lookup"><span data-stu-id="4dea5-129">negate</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-negate.md)                                       | <span data-ttu-id="4dea5-130">\- Registr</span><span class="sxs-lookup"><span data-stu-id="4dea5-130">\- register</span></span>    | <span data-ttu-id="4dea5-131">X</span><span class="sxs-lookup"><span data-stu-id="4dea5-131">X</span></span>       | <span data-ttu-id="4dea5-132">X</span><span class="sxs-lookup"><span data-stu-id="4dea5-132">X</span></span>    | <span data-ttu-id="4dea5-133">X</span><span class="sxs-lookup"><span data-stu-id="4dea5-133">X</span></span>    | <span data-ttu-id="4dea5-134">X</span><span class="sxs-lookup"><span data-stu-id="4dea5-134">X</span></span>    |     |     |
| [<span data-ttu-id="4dea5-135">escala por 2</span><span class="sxs-lookup"><span data-stu-id="4dea5-135">scale by 2</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md)                                 | <span data-ttu-id="4dea5-136">registrar \_ X2</span><span class="sxs-lookup"><span data-stu-id="4dea5-136">register\_x2</span></span>   |         |      |      | <span data-ttu-id="4dea5-137">X</span><span class="sxs-lookup"><span data-stu-id="4dea5-137">X</span></span>    |     |     |
| [<span data-ttu-id="4dea5-138">dimensionamento assinado</span><span class="sxs-lookup"><span data-stu-id="4dea5-138">signed scaling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md)                         | <span data-ttu-id="4dea5-139">registrar \_ BX2</span><span class="sxs-lookup"><span data-stu-id="4dea5-139">register\_bx2</span></span>  | <span data-ttu-id="4dea5-140">X</span><span class="sxs-lookup"><span data-stu-id="4dea5-140">X</span></span>       | <span data-ttu-id="4dea5-141">X</span><span class="sxs-lookup"><span data-stu-id="4dea5-141">X</span></span>    | <span data-ttu-id="4dea5-142">X</span><span class="sxs-lookup"><span data-stu-id="4dea5-142">X</span></span>    | <span data-ttu-id="4dea5-143">X</span><span class="sxs-lookup"><span data-stu-id="4dea5-143">X</span></span>    |     |     |
| [<span data-ttu-id="4dea5-144">modificadores texld e texcrd</span><span class="sxs-lookup"><span data-stu-id="4dea5-144">texld and texcrd modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-ps-1-4.md)                   | <span data-ttu-id="4dea5-145">registrar \_ d\*</span><span class="sxs-lookup"><span data-stu-id="4dea5-145">register\_d\*</span></span>  | <span data-ttu-id="4dea5-146">X</span><span class="sxs-lookup"><span data-stu-id="4dea5-146">X</span></span>       | <span data-ttu-id="4dea5-147">X</span><span class="sxs-lookup"><span data-stu-id="4dea5-147">X</span></span>    | <span data-ttu-id="4dea5-148">X</span><span class="sxs-lookup"><span data-stu-id="4dea5-148">X</span></span>    | <span data-ttu-id="4dea5-149">X</span><span class="sxs-lookup"><span data-stu-id="4dea5-149">X</span></span>    |     |     |
| [<span data-ttu-id="4dea5-150">swizzling de registro de origem</span><span class="sxs-lookup"><span data-stu-id="4dea5-150">source register swizzling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) | <span data-ttu-id="4dea5-151">registrar. xyzw</span><span class="sxs-lookup"><span data-stu-id="4dea5-151">register.xyzw</span></span>  | <span data-ttu-id="4dea5-152">X</span><span class="sxs-lookup"><span data-stu-id="4dea5-152">X</span></span>       | <span data-ttu-id="4dea5-153">X</span><span class="sxs-lookup"><span data-stu-id="4dea5-153">X</span></span>    | <span data-ttu-id="4dea5-154">X</span><span class="sxs-lookup"><span data-stu-id="4dea5-154">X</span></span>    | <span data-ttu-id="4dea5-155">X</span><span class="sxs-lookup"><span data-stu-id="4dea5-155">X</span></span>    |     |     |



 

<span data-ttu-id="4dea5-156">Modificadores de registro de origem só podem ser usados em instruções aritméticas.</span><span class="sxs-lookup"><span data-stu-id="4dea5-156">Source register modifiers can be used only on arithmetic instructions.</span></span> <span data-ttu-id="4dea5-157">Eles não podem ser usados em instruções de endereço de textura.</span><span class="sxs-lookup"><span data-stu-id="4dea5-157">They cannot be used on texture address instructions.</span></span> <span data-ttu-id="4dea5-158">A exceção a isso é o modificador de [escala por 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) .</span><span class="sxs-lookup"><span data-stu-id="4dea5-158">The exception to this is the [scale by 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) modifier.</span></span> <span data-ttu-id="4dea5-159">Para a versão 1 \_ 1, a escala assinada pode ser usada no argumento de origem de qualquer \* instrução texm.</span><span class="sxs-lookup"><span data-stu-id="4dea5-159">For version 1\_1, signed scale can be used on the source argument of any texm\* instruction.</span></span> <span data-ttu-id="4dea5-160">Para a versão 1 \_ 2 ou 1 \_ 3, a escala assinada pode ser usada no argumento de origem de qualquer instrução de endereço de textura.</span><span class="sxs-lookup"><span data-stu-id="4dea5-160">For version 1\_2 or 1\_3, signed scale can be used on the source argument of any texture address instruction.</span></span>

<span data-ttu-id="4dea5-161">Algumas restrições específicas de modificador:</span><span class="sxs-lookup"><span data-stu-id="4dea5-161">Some modifier specific restrictions:</span></span>

-   <span data-ttu-id="4dea5-162">O negar pode ser combinado com o modificador de tendência, dimensionamento assinado ou scalex2.</span><span class="sxs-lookup"><span data-stu-id="4dea5-162">Negate can be combined with either the bias, signed scaling, or scalex2 modifier.</span></span> <span data-ttu-id="4dea5-163">Quando combinado, negar é executado por último.</span><span class="sxs-lookup"><span data-stu-id="4dea5-163">When combined, negate is run last.</span></span>
-   <span data-ttu-id="4dea5-164">Invert não pode ser combinado com nenhum outro modificador.</span><span class="sxs-lookup"><span data-stu-id="4dea5-164">Invert cannot be combined with any other modifier.</span></span>
-   <span data-ttu-id="4dea5-165">Invert, negação, tendência, dimensionamento assinado e scalex2 podem ser combinados com qualquer um dos seletores.</span><span class="sxs-lookup"><span data-stu-id="4dea5-165">Invert, negate, bias, signed scaling, and scalex2 can be combined with any of the selectors.</span></span>
-   <span data-ttu-id="4dea5-166">Os modificadores de registro de origem não devem ser usados em registros constantes porque eles causarão resultados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="4dea5-166">Source register modifiers should not be used on constant registers because they will cause undefined results.</span></span> <span data-ttu-id="4dea5-167">Para a versão 1 \_ 4, os modificadores em constantes não são permitidos e ocorrerão falha na validação.</span><span class="sxs-lookup"><span data-stu-id="4dea5-167">For version 1\_4, modifiers on constants are not allowed and will fail validation.</span></span>

## <a name="ps_2_0-and-above"></a><span data-ttu-id="4dea5-168">PS \_ 2 \_ 0 e superior</span><span class="sxs-lookup"><span data-stu-id="4dea5-168">ps\_2\_0 and Above</span></span>

<span data-ttu-id="4dea5-169">Para a versão PS \_ 2 \_ 0 e superior, o número de modificadores foi simplificado.</span><span class="sxs-lookup"><span data-stu-id="4dea5-169">For version ps\_2\_0 and up, the number of modifiers has been simplified.</span></span>

### <a name="negate"></a><span data-ttu-id="4dea5-170">Negar</span><span class="sxs-lookup"><span data-stu-id="4dea5-170">Negate</span></span>

<span data-ttu-id="4dea5-171">Negar o conteúdo do registro de origem.</span><span class="sxs-lookup"><span data-stu-id="4dea5-171">Negate the contents of the source register.</span></span>



| <span data-ttu-id="4dea5-172">Modificador de componente</span><span class="sxs-lookup"><span data-stu-id="4dea5-172">Component modifier</span></span> | <span data-ttu-id="4dea5-173">Description</span><span class="sxs-lookup"><span data-stu-id="4dea5-173">Description</span></span>     |
|--------------------|-----------------|
| <span data-ttu-id="4dea5-174">\- d</span><span class="sxs-lookup"><span data-stu-id="4dea5-174">\- r</span></span>               | <span data-ttu-id="4dea5-175">Negação de origem</span><span class="sxs-lookup"><span data-stu-id="4dea5-175">Source negation</span></span> |



 

<span data-ttu-id="4dea5-176">O modificador de negação não pode ser usado no segundo registro de origem dessas instruções: [M3X2-PS](m3x2---ps.md), [m3x3-PS](m3x3---ps.md), [M3x4-PS](m3x4---ps.md), [m4x3-PS](m4x3---ps.md)e [m4x4-PS](m4x4---ps.md).</span><span class="sxs-lookup"><span data-stu-id="4dea5-176">The negate modifier cannot be used on second source register of these instructions: [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md), and [m4x4 - ps](m4x4---ps.md).</span></span>



| <span data-ttu-id="4dea5-177">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="4dea5-177">Pixel shader versions</span></span> | <span data-ttu-id="4dea5-178">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4dea5-178">2\_0</span></span> | <span data-ttu-id="4dea5-179">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4dea5-179">2\_x</span></span> | <span data-ttu-id="4dea5-180">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4dea5-180">2\_sw</span></span> | <span data-ttu-id="4dea5-181">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4dea5-181">3\_0</span></span> | <span data-ttu-id="4dea5-182">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4dea5-182">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| \-                    | <span data-ttu-id="4dea5-183">x</span><span class="sxs-lookup"><span data-stu-id="4dea5-183">x</span></span>    | <span data-ttu-id="4dea5-184">x</span><span class="sxs-lookup"><span data-stu-id="4dea5-184">x</span></span>    | <span data-ttu-id="4dea5-185">x</span><span class="sxs-lookup"><span data-stu-id="4dea5-185">x</span></span>     | <span data-ttu-id="4dea5-186">x</span><span class="sxs-lookup"><span data-stu-id="4dea5-186">x</span></span>    | <span data-ttu-id="4dea5-187">x</span><span class="sxs-lookup"><span data-stu-id="4dea5-187">x</span></span>     |



 

### <a name="absolute-value"></a><span data-ttu-id="4dea5-188">Valor absoluto</span><span class="sxs-lookup"><span data-stu-id="4dea5-188">Absolute Value</span></span>

<span data-ttu-id="4dea5-189">Pegue o valor absoluto do registro.</span><span class="sxs-lookup"><span data-stu-id="4dea5-189">Take the absolute value of the register.</span></span>



| <span data-ttu-id="4dea5-190">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="4dea5-190">Pixel shader versions</span></span> | <span data-ttu-id="4dea5-191">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4dea5-191">2\_0</span></span> | <span data-ttu-id="4dea5-192">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4dea5-192">2\_x</span></span> | <span data-ttu-id="4dea5-193">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4dea5-193">2\_sw</span></span> | <span data-ttu-id="4dea5-194">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4dea5-194">3\_0</span></span> | <span data-ttu-id="4dea5-195">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4dea5-195">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| <span data-ttu-id="4dea5-196">abs</span><span class="sxs-lookup"><span data-stu-id="4dea5-196">abs</span></span>                   |      |      |       | <span data-ttu-id="4dea5-197">x</span><span class="sxs-lookup"><span data-stu-id="4dea5-197">x</span></span>    | <span data-ttu-id="4dea5-198">x</span><span class="sxs-lookup"><span data-stu-id="4dea5-198">x</span></span>     |



 

<span data-ttu-id="4dea5-199">Se qualquer sombreador da versão 3 ler um ou mais registros de flutuação constante (c \# ), um dos seguintes deve ser verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="4dea5-199">If any version 3 shader reads from one or more constant float registers (c\#), one of the following must be true.</span></span>

-   <span data-ttu-id="4dea5-200">Todos os registros constantes de ponto flutuante devem usar o modificador ABS.</span><span class="sxs-lookup"><span data-stu-id="4dea5-200">All of the constant floating-point registers must use the abs modifier.</span></span>
-   <span data-ttu-id="4dea5-201">Nenhum dos registros constantes de ponto flutuante pode usar o modificador ABS.</span><span class="sxs-lookup"><span data-stu-id="4dea5-201">None of the constant floating-point registers can use the abs modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4dea5-202">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4dea5-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dea5-203">Modificadores de registro do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="4dea5-203">Pixel Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




