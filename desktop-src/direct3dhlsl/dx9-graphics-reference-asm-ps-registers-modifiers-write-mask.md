---
title: Máscara de gravação do registro de destino
description: Uma máscara de gravação controla quais componentes de um registro de destino são gravados depois que uma instrução é concluída.
ms.assetid: 376a28c8-8a88-4807-a8ab-f59448d965e8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 80f649770b84174dbb716967e9d941034c3966f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916641"
---
# <a name="destination-register-write-mask"></a><span data-ttu-id="f9442-103">Máscara de gravação do registro de destino</span><span class="sxs-lookup"><span data-stu-id="f9442-103">Destination Register Write Mask</span></span>

<span data-ttu-id="f9442-104">Uma máscara de gravação controla quais componentes de um registro de destino são gravados depois que uma instrução é concluída.</span><span class="sxs-lookup"><span data-stu-id="f9442-104">A write mask controls which components of a destination register are written after an instruction is completed.</span></span> <span data-ttu-id="f9442-105">Uma máscara de gravação de saída é permitida, desde que os componentes estejam na ordem de. RGBA ou. xyzw.</span><span class="sxs-lookup"><span data-stu-id="f9442-105">An output write mask is allowed as long as the components are in the order of .rgba or .xyzw.</span></span> <span data-ttu-id="f9442-106">Ou seja,. RBA e. XW são máscaras válidas.</span><span class="sxs-lookup"><span data-stu-id="f9442-106">That is, .rba and .xw are valid masks.</span></span> <span data-ttu-id="f9442-107">Os registros de textura têm um conjunto de regras e os registros que não são de textura têm outro conjunto de regras.</span><span class="sxs-lookup"><span data-stu-id="f9442-107">Texture registers have one set of rules and non-texture registers have another set of rules.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9442-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9442-108">Syntax</span></span>



| <span data-ttu-id="f9442-109">DST. writemask</span><span class="sxs-lookup"><span data-stu-id="f9442-109">dst.writemask</span></span> |
|---------------|



 

<span data-ttu-id="f9442-110">onde</span><span class="sxs-lookup"><span data-stu-id="f9442-110">where</span></span>

-   <span data-ttu-id="f9442-111">o DST é um registro de destino.</span><span class="sxs-lookup"><span data-stu-id="f9442-111">dst is a destination register.</span></span>
-   <span data-ttu-id="f9442-112">writemask é uma sequência de máscaras de um dos conjuntos: (x, y, z, w) ou (vermelho, verde, azul, alfa).</span><span class="sxs-lookup"><span data-stu-id="f9442-112">writemask is a sequence of masks from either set: (x,y,z,w) or (red, green, blue, alpha).</span></span>

## <a name="remarks"></a><span data-ttu-id="f9442-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9442-113">Remarks</span></span>

<span data-ttu-id="f9442-114">As seguintes máscaras de gravação de destino estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f9442-114">The following destination write masks are available.</span></span>



| <span data-ttu-id="f9442-115">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="f9442-115">Pixel shader versions</span></span> | <span data-ttu-id="f9442-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="f9442-116">1\_1</span></span> | <span data-ttu-id="f9442-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="f9442-117">1\_2</span></span> | <span data-ttu-id="f9442-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f9442-118">1\_3</span></span> | <span data-ttu-id="f9442-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="f9442-119">1\_4</span></span> | <span data-ttu-id="f9442-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f9442-120">2\_0</span></span> | <span data-ttu-id="f9442-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f9442-121">2\_x</span></span> | <span data-ttu-id="f9442-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f9442-122">2\_sw</span></span> | <span data-ttu-id="f9442-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f9442-123">3\_0</span></span> | <span data-ttu-id="f9442-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f9442-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="f9442-125">. xyzw (padrão)</span><span class="sxs-lookup"><span data-stu-id="f9442-125">.xyzw (default)</span></span>       | <span data-ttu-id="f9442-126">x</span><span class="sxs-lookup"><span data-stu-id="f9442-126">x</span></span>    | <span data-ttu-id="f9442-127">x</span><span class="sxs-lookup"><span data-stu-id="f9442-127">x</span></span>    | <span data-ttu-id="f9442-128">x</span><span class="sxs-lookup"><span data-stu-id="f9442-128">x</span></span>    | <span data-ttu-id="f9442-129">x</span><span class="sxs-lookup"><span data-stu-id="f9442-129">x</span></span>    | <span data-ttu-id="f9442-130">x</span><span class="sxs-lookup"><span data-stu-id="f9442-130">x</span></span>    | <span data-ttu-id="f9442-131">x</span><span class="sxs-lookup"><span data-stu-id="f9442-131">x</span></span>    | <span data-ttu-id="f9442-132">x</span><span class="sxs-lookup"><span data-stu-id="f9442-132">x</span></span>     | <span data-ttu-id="f9442-133">x</span><span class="sxs-lookup"><span data-stu-id="f9442-133">x</span></span>    | <span data-ttu-id="f9442-134">x</span><span class="sxs-lookup"><span data-stu-id="f9442-134">x</span></span>     |
| <span data-ttu-id="f9442-135">. xyz</span><span class="sxs-lookup"><span data-stu-id="f9442-135">.xyz</span></span>                  | <span data-ttu-id="f9442-136">x</span><span class="sxs-lookup"><span data-stu-id="f9442-136">x</span></span>    | <span data-ttu-id="f9442-137">x</span><span class="sxs-lookup"><span data-stu-id="f9442-137">x</span></span>    | <span data-ttu-id="f9442-138">x</span><span class="sxs-lookup"><span data-stu-id="f9442-138">x</span></span>    | <span data-ttu-id="f9442-139">x</span><span class="sxs-lookup"><span data-stu-id="f9442-139">x</span></span>    | <span data-ttu-id="f9442-140">x</span><span class="sxs-lookup"><span data-stu-id="f9442-140">x</span></span>    | <span data-ttu-id="f9442-141">x</span><span class="sxs-lookup"><span data-stu-id="f9442-141">x</span></span>    | <span data-ttu-id="f9442-142">x</span><span class="sxs-lookup"><span data-stu-id="f9442-142">x</span></span>     | <span data-ttu-id="f9442-143">x</span><span class="sxs-lookup"><span data-stu-id="f9442-143">x</span></span>    | <span data-ttu-id="f9442-144">x</span><span class="sxs-lookup"><span data-stu-id="f9442-144">x</span></span>     |
| <span data-ttu-id="f9442-145">. w</span><span class="sxs-lookup"><span data-stu-id="f9442-145">.w</span></span>                    | <span data-ttu-id="f9442-146">x</span><span class="sxs-lookup"><span data-stu-id="f9442-146">x</span></span>    | <span data-ttu-id="f9442-147">x</span><span class="sxs-lookup"><span data-stu-id="f9442-147">x</span></span>    | <span data-ttu-id="f9442-148">x</span><span class="sxs-lookup"><span data-stu-id="f9442-148">x</span></span>    | <span data-ttu-id="f9442-149">x</span><span class="sxs-lookup"><span data-stu-id="f9442-149">x</span></span>    | <span data-ttu-id="f9442-150">x</span><span class="sxs-lookup"><span data-stu-id="f9442-150">x</span></span>    | <span data-ttu-id="f9442-151">x</span><span class="sxs-lookup"><span data-stu-id="f9442-151">x</span></span>    | <span data-ttu-id="f9442-152">x</span><span class="sxs-lookup"><span data-stu-id="f9442-152">x</span></span>     | <span data-ttu-id="f9442-153">x</span><span class="sxs-lookup"><span data-stu-id="f9442-153">x</span></span>    | <span data-ttu-id="f9442-154">x</span><span class="sxs-lookup"><span data-stu-id="f9442-154">x</span></span>     |
| <span data-ttu-id="f9442-155">máscara arbitrária</span><span class="sxs-lookup"><span data-stu-id="f9442-155">arbitrary mask</span></span>        |      |      |      | <span data-ttu-id="f9442-156">x</span><span class="sxs-lookup"><span data-stu-id="f9442-156">x</span></span>    | <span data-ttu-id="f9442-157">x</span><span class="sxs-lookup"><span data-stu-id="f9442-157">x</span></span>    | <span data-ttu-id="f9442-158">x</span><span class="sxs-lookup"><span data-stu-id="f9442-158">x</span></span>    | <span data-ttu-id="f9442-159">x</span><span class="sxs-lookup"><span data-stu-id="f9442-159">x</span></span>     | <span data-ttu-id="f9442-160">x</span><span class="sxs-lookup"><span data-stu-id="f9442-160">x</span></span>    | <span data-ttu-id="f9442-161">x</span><span class="sxs-lookup"><span data-stu-id="f9442-161">x</span></span>     |



 

<span data-ttu-id="f9442-162">A máscara arbitrária permite que qualquer conjunto de canais seja combinado para produzir uma máscara.</span><span class="sxs-lookup"><span data-stu-id="f9442-162">The arbitrary mask allows any set of channels to be combined to produce a mask.</span></span> <span data-ttu-id="f9442-163">Os canais devem estar listados na ordem r, g, b, a-por exemplo, Register. RBA, que atualiza os canais vermelho, azul e alfa do destino.</span><span class="sxs-lookup"><span data-stu-id="f9442-163">The channels must be listed in the order r, g, b, a - for example, register.rba, which updates the red, blue, and alpha channels of the destination.</span></span> <span data-ttu-id="f9442-164">A máscara arbitrária está disponível na versão 1 \_ 4 ou superior.</span><span class="sxs-lookup"><span data-stu-id="f9442-164">The arbitrary mask is available in version 1\_4 or higher.</span></span>

<span data-ttu-id="f9442-165">Se nenhuma máscara de gravação de destino for especificada, a máscara de gravação de destino padronizará para o caso RGBA.</span><span class="sxs-lookup"><span data-stu-id="f9442-165">If no destination write mask is specified, the destination write mask defaults to the rgba case.</span></span> <span data-ttu-id="f9442-166">Em outras palavras, todos os canais no registro de destino são atualizados.</span><span class="sxs-lookup"><span data-stu-id="f9442-166">In other words, all channels in the destination register are updated.</span></span>

<span data-ttu-id="f9442-167">Para as versões de 1 \_ a 1 \_ 3, a instrução aritmética de DP3 [DP3-PS](dp3---ps.md) pode usar apenas as máscaras de gravação de saída. RGB ou. RGBA.</span><span class="sxs-lookup"><span data-stu-id="f9442-167">For versions 1\_0 to 1\_3, the [dp3 - ps](dp3---ps.md) dp3 arithmetic instruction can use only the .rgb or .rgba output write masks.</span></span>

<span data-ttu-id="f9442-168">As máscaras de gravação de registro de destino têm suporte apenas para operações aritméticas.</span><span class="sxs-lookup"><span data-stu-id="f9442-168">Destination register write masks are supported for arithmetic operations only.</span></span> <span data-ttu-id="f9442-169">Eles não podem ser usados em instruções de endereçamento de textura, com exceção das instruções da versão 1 \_ 4, [texcrd-PS](texcrd---ps.md) e [texld-PS \_ 2 \_ 0 e up](texld---ps-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="f9442-169">They cannot be used on texture addressing instructions, with the exception of the version 1\_4 instructions, [texcrd - ps](texcrd---ps.md) and [texld - ps\_2\_0 and up](texld---ps-2-0.md).</span></span>

<span data-ttu-id="f9442-170">O padrão é gravar todos os quatro canais de cor.</span><span class="sxs-lookup"><span data-stu-id="f9442-170">The default is to write all four color channels.</span></span>


```
// All four color channels can be written by explicitly listing them.
mul r0.rgba, t0, v0

// Or, the default mask can be used to write all four channels.
mul r0, t0, v0
```



<span data-ttu-id="f9442-171">A máscara de gravação alfa também é conhecida como a máscara de gravação escalar, porque ela usa o pipeline escalar.</span><span class="sxs-lookup"><span data-stu-id="f9442-171">The alpha write mask is also referred to as the scalar write mask, because it uses the scalar pipeline.</span></span>


```
add r0.a, t1, v1
```



<span data-ttu-id="f9442-172">Portanto, essa instrução coloca efetivamente a soma do componente alfa do T1 e o componente alfa de v1 em r0. a.</span><span class="sxs-lookup"><span data-stu-id="f9442-172">So this instruction effectively puts the sum of the alpha component of t1 and the alpha component of v1 into r0.a.</span></span>

<span data-ttu-id="f9442-173">A máscara de gravação de cor é usada para controlar a gravação nos canais de cores.</span><span class="sxs-lookup"><span data-stu-id="f9442-173">The color write mask is used to control writing to the color channels.</span></span>


```
// The color write mask is also referred to as the vector write mask, 
//   because it uses the vector pipeline.
mul r0.rgb, t0, v0
```



<span data-ttu-id="f9442-174">Para a versão 1 \_ 4, as máscaras de gravação de destino podem ser usadas em qualquer combinação, desde que as máscaras sejam ordenadas como r, g, b, a.</span><span class="sxs-lookup"><span data-stu-id="f9442-174">For version 1\_4, destination write masks can be used in any combination as long as the masks are ordered r,g,b,a.</span></span>


```
// This example updates the red, blue, and alpha channels.
mov r0.rba, r1
```



<span data-ttu-id="f9442-175">Uma instrução coemitida permite que duas instruções potencialmente diferentes sejam emitidas simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="f9442-175">A co-issued instruction allows two potentially different instructions to be issued simultaneously.</span></span> <span data-ttu-id="f9442-176">Isso é feito executando as instruções no pipeline alfa e no pipeline RGB.</span><span class="sxs-lookup"><span data-stu-id="f9442-176">This is accomplished by executing the instructions in the alpha pipeline and the RGB pipeline.</span></span>


```
  mul r0.rgb, t0, v0
+ add r1.a,   t1, c1
```



<span data-ttu-id="f9442-177">A vantagem de emparelhar instruções dessa forma é que ela permite que operações diferentes sejam executadas no pipeline de vetor e escalar em paralelo.</span><span class="sxs-lookup"><span data-stu-id="f9442-177">The advantage of pairing instructions this way is that it allows different operations to be performed in the vector and scalar pipeline in parallel.</span></span>

<span data-ttu-id="f9442-178">Esses registros de saída do sombreador de vértice são restritos às seguintes máscaras de gravação:</span><span class="sxs-lookup"><span data-stu-id="f9442-178">These vertex shader output registers are restricted to the following write masks:</span></span>



| <span data-ttu-id="f9442-179">Tipo de registro</span><span class="sxs-lookup"><span data-stu-id="f9442-179">Register Type</span></span> | <span data-ttu-id="f9442-180">Máscara de gravação necessária</span><span class="sxs-lookup"><span data-stu-id="f9442-180">Required Write Mask</span></span>                                              |
|---------------|------------------------------------------------------------------|
| <span data-ttu-id="f9442-181">oFog</span><span class="sxs-lookup"><span data-stu-id="f9442-181">oFog</span></span>          | <span data-ttu-id="f9442-182">nenhuma máscara de gravação explícita é permitida neste registro escalar</span><span class="sxs-lookup"><span data-stu-id="f9442-182">no explicit write mask is allowed on this scalar register</span></span>        |
| <span data-ttu-id="f9442-183">oPts</span><span class="sxs-lookup"><span data-stu-id="f9442-183">oPts</span></span>          | <span data-ttu-id="f9442-184">nenhuma máscara de gravação explícita é permitida neste registro escalar</span><span class="sxs-lookup"><span data-stu-id="f9442-184">no explicit write mask is allowed on this scalar register</span></span>        |
| <span data-ttu-id="f9442-185">oPos</span><span class="sxs-lookup"><span data-stu-id="f9442-185">oPos</span></span>          | <span data-ttu-id="f9442-186">. xyzw (que é o padrão)</span><span class="sxs-lookup"><span data-stu-id="f9442-186">.xyzw(which is the default)</span></span>                                      |
| <span data-ttu-id="f9442-187">To\#</span><span class="sxs-lookup"><span data-stu-id="f9442-187">oT\#</span></span>          | <span data-ttu-id="f9442-188">máscara combinada:. x \| . XY \| . xyz \| . xyzw (que é o padrão)</span><span class="sxs-lookup"><span data-stu-id="f9442-188">combined mask: .x \| .xy \| .xyz \| .xyzw (which is the default)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f9442-189">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f9442-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9442-190">Modificadores de registro do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="f9442-190">Pixel Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




