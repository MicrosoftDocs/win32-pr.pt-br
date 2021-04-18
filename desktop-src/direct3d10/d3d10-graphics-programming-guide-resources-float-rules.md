---
description: O Direct3D 10 dá suporte a várias representações de ponto flutuante diferentes. Todos os cálculos de ponto flutuante funcionam em um subconjunto definido do comportamento de ponto flutuante de precisão única de IEEE 754 32 bits.
ms.assetid: 57221d13-8993-4db3-b1a0-88bdcf6f0167
title: Regras de ponto de FFloating (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6909d037b11f9098bb3e0dbad0f1846b79b513e8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784561"
---
# <a name="floating-point-rules-direct3d-10"></a><span data-ttu-id="552e7-104">Regras de ponto flutuante (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="552e7-104">Floating-point rules (Direct3D 10)</span></span>

<span data-ttu-id="552e7-105">O Direct3D 10 dá suporte a várias representações de ponto flutuante diferentes.</span><span class="sxs-lookup"><span data-stu-id="552e7-105">Direct3D 10 supports several different floating-point representations.</span></span> <span data-ttu-id="552e7-106">Todos os cálculos de ponto flutuante funcionam em um subconjunto definido do comportamento de ponto flutuante de precisão única de IEEE 754 32 bits.</span><span class="sxs-lookup"><span data-stu-id="552e7-106">All floating-point computations operate under a defined subset of the IEEE 754 32-bit single precision floating-point behavior.</span></span>

-   [<span data-ttu-id="552e7-107">Regras de Floating-Point de 32 bits</span><span class="sxs-lookup"><span data-stu-id="552e7-107">32-bit Floating-Point Rules</span></span>](#32-bit-floating-point-rules)
    -   [<span data-ttu-id="552e7-108">Regras do IEEE-754 respeitadas</span><span class="sxs-lookup"><span data-stu-id="552e7-108">Honored IEEE-754 Rules</span></span>](#honored-ieee-754-rules)
    -   [<span data-ttu-id="552e7-109">Desvios ou requisitos adicionais das regras IEEE-754</span><span class="sxs-lookup"><span data-stu-id="552e7-109">Deviations or Additional Requirements from IEEE-754 Rules</span></span>](#deviations-or-additional-requirements-from-ieee-754-rules)
-   [<span data-ttu-id="552e7-110">Regras de Floating-Point de 16 bits</span><span class="sxs-lookup"><span data-stu-id="552e7-110">16-bit Floating-Point Rules</span></span>](#16-bit-floating-point-rules)
-   [<span data-ttu-id="552e7-111">Regras de Floating-Point de 11 e 10 bits</span><span class="sxs-lookup"><span data-stu-id="552e7-111">11-bit and 10-bit Floating-Point Rules</span></span>](#11-bit-and-10-bit-floating-point-rules)
-   [<span data-ttu-id="552e7-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="552e7-112">Related topics</span></span>](#related-topics)

## <a name="32-bit-floating-point-rules"></a><span data-ttu-id="552e7-113">Regras de Floating-Point de 32 bits</span><span class="sxs-lookup"><span data-stu-id="552e7-113">32-bit Floating-Point Rules</span></span>

<span data-ttu-id="552e7-114">Existem dois conjuntos de regras: aquele em conformidade com IEEE-754, e aquele que desvia do padrão.</span><span class="sxs-lookup"><span data-stu-id="552e7-114">There are two sets of rules: those that conform to IEEE-754, and those that deviate from the standard.</span></span>

### <a name="honored-ieee-754-rules"></a><span data-ttu-id="552e7-115">Regras do IEEE-754 respeitadas</span><span class="sxs-lookup"><span data-stu-id="552e7-115">Honored IEEE-754 Rules</span></span>

<span data-ttu-id="552e7-116">Algumas dessas regras são uma única opção onde a IEEE-754 oferece opções.</span><span class="sxs-lookup"><span data-stu-id="552e7-116">Some of these rules are a single option where IEEE-754 offers choices.</span></span>

-   <span data-ttu-id="552e7-117">Divisão por 0 produz + /-INF, exceto 0/0, o que resulta em NaN.</span><span class="sxs-lookup"><span data-stu-id="552e7-117">Divide by 0 produces +/- INF, except 0/0 which results in NaN.</span></span>
-   <span data-ttu-id="552e7-118">o log de (+/-) 0 produz -INF.</span><span class="sxs-lookup"><span data-stu-id="552e7-118">log of (+/-) 0 produces -INF.</span></span> <span data-ttu-id="552e7-119">o log de um valor negativo (diferente de -0) produz NaN.</span><span class="sxs-lookup"><span data-stu-id="552e7-119">log of a negative value (other than -0) produces NaN.</span></span>
-   <span data-ttu-id="552e7-120">A raiz quadrada recíproca (rsq) ou raiz quadrada (sqrt) de um número negativo produz NaN.</span><span class="sxs-lookup"><span data-stu-id="552e7-120">Reciprocal square root (rsq) or square root (sqrt) of a negative number produces NaN.</span></span> <span data-ttu-id="552e7-121">A exceção é - 0; sqrt(-0) produz - 0 e rsq(-0) produz -INF.</span><span class="sxs-lookup"><span data-stu-id="552e7-121">The exception is -0; sqrt(-0) produces -0, and rsq(-0) produces -INF.</span></span>
-   <span data-ttu-id="552e7-122">INF - INF = NaN</span><span class="sxs-lookup"><span data-stu-id="552e7-122">INF - INF = NaN</span></span>
-   <span data-ttu-id="552e7-123">(+/-)INF / (+/-)INF = NaN</span><span class="sxs-lookup"><span data-stu-id="552e7-123">(+/-)INF / (+/-)INF = NaN</span></span>
-   <span data-ttu-id="552e7-124">(+/-) INF \* 0 = Nan</span><span class="sxs-lookup"><span data-stu-id="552e7-124">(+/-)INF \* 0 = NaN</span></span>
-   <span data-ttu-id="552e7-125">Qualquer valor NaN (qualquer OP) = NaN</span><span class="sxs-lookup"><span data-stu-id="552e7-125">NaN (any OP) any-value = NaN</span></span>
-   <span data-ttu-id="552e7-126">As comparações EQ, GT, GE, LT e LE, quando um ou ambos operandos for NaN retornará **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="552e7-126">The comparisons EQ, GT, GE, LT, and LE, when either or both operands is NaN returns **FALSE**.</span></span>
-   <span data-ttu-id="552e7-127">As comparações ignoram o sinal de 0 (sendo assim, +0 igual -0).</span><span class="sxs-lookup"><span data-stu-id="552e7-127">Comparisons ignore the sign of 0 (so +0 equals -0).</span></span>
-   <span data-ttu-id="552e7-128">A comparação NE, quando um ou ambos operandos for NaN retornará **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="552e7-128">The comparison NE, when either or both operands is NaN returns **TRUE**.</span></span>
-   <span data-ttu-id="552e7-129">As comparações de qualquer valor não NaN com +/-INF retornam o resultado correto.</span><span class="sxs-lookup"><span data-stu-id="552e7-129">Comparisons of any non-NaN value against +/- INF return the correct result.</span></span>

### <a name="deviations-or-additional-requirements-from-ieee-754-rules"></a><span data-ttu-id="552e7-130">Desvios ou requisitos adicionais das regras IEEE-754</span><span class="sxs-lookup"><span data-stu-id="552e7-130">Deviations or Additional Requirements from IEEE-754 Rules</span></span>

-   <span data-ttu-id="552e7-131">O IEEE-754 exibe que as operações de ponto flutuante produzam um resultado que seja o valor representável mais próximo a um resultado infinitamente preciso, conhecido como valor arredondado para o número par mais próximo.</span><span class="sxs-lookup"><span data-stu-id="552e7-131">IEEE-754 requires floating-point operations to produce a result that is the nearest representable value to an infinitely-precise result, known as round-to-nearest-even.</span></span> <span data-ttu-id="552e7-132">No entanto, o Direct3D 10 define um requisito mais flexível: as operações de ponto flutuante de 32 bits produzem um resultado que está dentro de uma unidade-último local (1 ULP) do resultado infinitamente preciso.</span><span class="sxs-lookup"><span data-stu-id="552e7-132">Direct3D 10, however, defines a looser requirement: 32-bit floating-point operations produce a result that is within one unit-last-place (1 ULP) of the infinitely-precise result.</span></span> <span data-ttu-id="552e7-133">Isso significa que, por exemplo, o hardware tem permissão de truncar resultados em 32 bits, em vez de executar o arredondamento para o número par mais próximo, uma vez que isso resultaria em um erro de no máximo 1 ULP.</span><span class="sxs-lookup"><span data-stu-id="552e7-133">This means that, for example, hardware is allowed to truncate results to 32-bit rather than perform round-to-nearest-even, as that would result in error of at most one ULP.</span></span>
-   <span data-ttu-id="552e7-134">Não há nenhum suporte para exceções de ponto flutuante, bits de status ou interrupções.</span><span class="sxs-lookup"><span data-stu-id="552e7-134">There is no support for floating-point exceptions, status bits or traps.</span></span>
-   <span data-ttu-id="552e7-135">Denorms são liberadas para zero com sinal preservado na entrada e saída de qualquer operação matemática de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="552e7-135">Denorms are flushed to sign-preserved zero on input and output of any floating-point mathematical operation.</span></span> <span data-ttu-id="552e7-136">São feitas exceções para qualquer operação de movimentação de dados e e/s que não manipula os dados.</span><span class="sxs-lookup"><span data-stu-id="552e7-136">Exceptions are made for any I/O or data movement operation that does not manipulate the data.</span></span>
-   <span data-ttu-id="552e7-137">Os Estados que contêm valores de ponto flutuante, como visor MinDepth/MaxDepth, valores de BorderColor, etc., podem ser fornecidos como valores não normativos e podem ou não ser liberados antes de serem usados pelo hardware.</span><span class="sxs-lookup"><span data-stu-id="552e7-137">States that contain floating-point values, such as Viewport MinDepth/MaxDepth, BorderColor values etc., may be provided as denorm values and may or may not be flushed before use by the hardware.</span></span>
-   <span data-ttu-id="552e7-138">As operações de mínimo ou máximo liberam denorms para a comparação, mas o resultado pode ou não ser um denorm liberado.</span><span class="sxs-lookup"><span data-stu-id="552e7-138">Min or max operations flush denorms for comparison, but the result may or may not be denorm flushed.</span></span>
-   <span data-ttu-id="552e7-139">A entrada NaN para uma operação sempre produz NaN na saída, no entanto, o padrão de bit exato do NaN não é necessário para permanecer o mesmo (a menos que a operação seja uma instrução de movimentação bruta, o que não altera dados.)</span><span class="sxs-lookup"><span data-stu-id="552e7-139">NaN input to an operation always produces NaN on output, however the exact bit pattern of the NaN is not required to stay the same (unless the operation is a raw move instruction - which does not alter data at all.)</span></span>
-   <span data-ttu-id="552e7-140">As operações min ou Max para as quais apenas um operando é NaN retornam o outro operando como resultado (ao contrário das regras de comparação acima).</span><span class="sxs-lookup"><span data-stu-id="552e7-140">Min or max operations for which only one operand is NaN return the other operand as the result (contrary to comparison rules above).</span></span> <span data-ttu-id="552e7-141">Essa é uma nova regra IEEE (IEEE 754R), necessária no Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="552e7-141">This is a new IEEE rule (IEEE 754R), required in Direct3D 10.</span></span>
-   <span data-ttu-id="552e7-142">Outra nova regra IEEE 754R é que min (-0, + 0) = = min (+ 0,-0) = =-0 e Max (-0, + 0) = = Max (+ 0,-0) = = + 0, que respeitam o sinal, em contraste com as regras de comparação para zero assinado (declarado acima).</span><span class="sxs-lookup"><span data-stu-id="552e7-142">Another new IEEE 754R rule is that min(-0,+0) == min(+0,-0) == -0, and max(-0,+0) == max(+0,-0) == +0, which honor the sign, in contrast to the comparison rules for signed zero (stated above).</span></span> <span data-ttu-id="552e7-143">O Direct3D 10 recomenda o comportamento do IEEE 754R aqui, mas não será imposto; é permitido que o resultado da comparação de zeros seja dependente da ordem dos parâmetros, usando uma comparação que ignora os sinais.</span><span class="sxs-lookup"><span data-stu-id="552e7-143">Direct3D 10 recommends the IEEE 754R behavior here, but it will not be enforced; it is permissible for the result of comparing zeros to be dependent on the order of parameters, using a comparison that ignores the signs.</span></span>
-   <span data-ttu-id="552e7-144">x \* 1.0 f sempre resulta em x (exceto descarregamento desnormal).</span><span class="sxs-lookup"><span data-stu-id="552e7-144">x\*1.0f always results in x (except denorm flushed).</span></span>
-   <span data-ttu-id="552e7-145">x/1.0f sempre resulta em x (exceto denorm liberados).</span><span class="sxs-lookup"><span data-stu-id="552e7-145">x/1.0f always results in x (except denorm flushed).</span></span>
-   <span data-ttu-id="552e7-146">x +/- 0.0f sempre resulta em x (exceto denorm liberados).</span><span class="sxs-lookup"><span data-stu-id="552e7-146">x +/- 0.0f always results in x (except denorm flushed).</span></span> <span data-ttu-id="552e7-147">Mas -0 + 0 = +0.</span><span class="sxs-lookup"><span data-stu-id="552e7-147">But -0 + 0 = +0.</span></span>
-   <span data-ttu-id="552e7-148">As operações fundidas (como mad, dp3) produzem resultados que não são menos precisos do que a pior ordem serial possível da avaliação da expansão não fundida da operação.</span><span class="sxs-lookup"><span data-stu-id="552e7-148">Fused operations (such as mad, dp3) produce results that are no less accurate than the worst possible serial ordering of evaluation of the unfused expansion of the operation.</span></span> <span data-ttu-id="552e7-149">Observe que a definição da pior ordenação possível, para fins de tolerância, não é uma definição fixa para uma determinada operação com fusível; depende dos valores específicos das entradas.</span><span class="sxs-lookup"><span data-stu-id="552e7-149">Note that the definition of the worst possible ordering, for the purpose of tolerance, is not a fixed definition for a given fused operation; it depends on the particular values of the inputs.</span></span> <span data-ttu-id="552e7-150">As etapas individuais na expansão não-fundida são cada uma delas permitida 1 tolerância de ULP (ou para quaisquer instruções que o Direct3D 10 chama com uma tolerância mais inlax do que 1 ULP, a tolerância mais incerto é permitida).</span><span class="sxs-lookup"><span data-stu-id="552e7-150">The individual steps in the unfused expansion are each allowed 1 ULP tolerance (or for any instructions Direct3D 10 calls out with a more lax tolerance than 1 ULP, the more lax tolerance is allowed).</span></span>
-   <span data-ttu-id="552e7-151">As operações fundidas cumprem as mesmas regras NaN que as operações não fundidas.</span><span class="sxs-lookup"><span data-stu-id="552e7-151">Fused operations adhere to the same NaN rules as non-fused operations.</span></span>
-   <span data-ttu-id="552e7-152">Multiplicar e dividir cada operação no nível de precisão de ponto flutuante de 32 bits (precisão para 1 ULP).</span><span class="sxs-lookup"><span data-stu-id="552e7-152">Multiply and divide each operate at the 32-bit floating-point precision level (accuracy to 1 ULP).</span></span>

## <a name="16-bit-floating-point-rules"></a><span data-ttu-id="552e7-153">Regras de Floating-Point de 16 bits</span><span class="sxs-lookup"><span data-stu-id="552e7-153">16-bit Floating-Point Rules</span></span>

<span data-ttu-id="552e7-154">O Direct3D 10 também dá suporte a representações de 16 bits de números de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="552e7-154">Direct3D 10 also supports 16-bit representations of floating-point numbers.</span></span>

<span data-ttu-id="552e7-155">Formato:</span><span class="sxs-lookup"><span data-stu-id="552e7-155">Format:</span></span>

-   <span data-ttu-id="552e7-156">Sinal de 1 bit (s) na posição MSB bit</span><span class="sxs-lookup"><span data-stu-id="552e7-156">1 sign bit (s)in the MSB bit position</span></span>
-   <span data-ttu-id="552e7-157">5 bits de expoente ajustado (e)</span><span class="sxs-lookup"><span data-stu-id="552e7-157">5 bits of biased exponent (e)</span></span>
-   <span data-ttu-id="552e7-158">10 bits de fração (f), com um bit oculto adicional</span><span class="sxs-lookup"><span data-stu-id="552e7-158">10 bits of fraction (f), with an additional hidden bit</span></span>

<span data-ttu-id="552e7-159">Um valor de float16 (v) segue as seguintes regras:</span><span class="sxs-lookup"><span data-stu-id="552e7-159">A float16 value (v) follows the following rules:</span></span>

-   <span data-ttu-id="552e7-160">Se e == 31 e f != 0, então v é NaN independente de s</span><span class="sxs-lookup"><span data-stu-id="552e7-160">if e == 31 and f != 0, then v is NaN regardless of s</span></span>
-   <span data-ttu-id="552e7-161">se e = = 31 e f = = 0, então v = (-1) s \* Infinity (infinito assinado)</span><span class="sxs-lookup"><span data-stu-id="552e7-161">if e == 31 and f == 0, then v = (-1)s\*infinity (signed infinity)</span></span>
-   <span data-ttu-id="552e7-162">se e estiver entre 0 e 31, v = (-1) s \* 2 (e-15) \* (1. f)</span><span class="sxs-lookup"><span data-stu-id="552e7-162">if e is between 0 and 31, then v = (-1)s\*2(e-15)\*(1.f)</span></span>
-   <span data-ttu-id="552e7-163">se e = = 0 e f! = 0, v = (-1) s \* 2 (e-14) \* (0. f) (números desnormalizados)</span><span class="sxs-lookup"><span data-stu-id="552e7-163">if e == 0 and f != 0, then v = (-1)s\*2(e-14)\*(0.f) (denormalized numbers)</span></span>
-   <span data-ttu-id="552e7-164">se e = = 0 e f = = 0, então v = (-1) s \* 0 (assinado zero)</span><span class="sxs-lookup"><span data-stu-id="552e7-164">if e == 0 and f == 0, then v = (-1)s\*0 (signed zero)</span></span>

<span data-ttu-id="552e7-165">as regras de ponto flutuante de 32 bits também contêm números de ponto flutuante de 16 bits, ajustadas para o layout de bit descrito acima.</span><span class="sxs-lookup"><span data-stu-id="552e7-165">32-bit floating-point rules also hold for 16-bit floating-point numbers, adjusted for the bit layout described above.</span></span> <span data-ttu-id="552e7-166">Algumas exceções:</span><span class="sxs-lookup"><span data-stu-id="552e7-166">Exceptions to this include:</span></span>

-   <span data-ttu-id="552e7-167">Precisão: as operações não fundidas em números de ponto flutuante de 16 bits produzem um resultado que é o valor representável mais próximo de um resultado infinitamente preciso (arredondado para o número par mais próximo, de acordo com IEEE-754, aplicado aos valores de 16 bits).</span><span class="sxs-lookup"><span data-stu-id="552e7-167">Precision: Unfused operations on 16-bit floating-point numbers produce a result that is the nearest representable value to an infinitely-precise result (round to nearest even, per IEEE-754, applied to 16-bit values).</span></span> <span data-ttu-id="552e7-168">As regras de ponto flutuante de 32 bits aderem à tolerância de 1 ULP, as regras de ponto flutuante de 16 bits aderem a 0,5 ULP para as operações não fundidas e 0,6 ULP para operações fundidas.</span><span class="sxs-lookup"><span data-stu-id="552e7-168">32-bit floating-point rules adhere to 1 ULP tolerance, 16-bit floating-point rules adhere to 0.5 ULP for unfused operations, and 0.6 ULP for fused operations.</span></span>
-   <span data-ttu-id="552e7-169">Os números de ponto flutuante de 16 bits preservam denorms.</span><span class="sxs-lookup"><span data-stu-id="552e7-169">16-bit floating-point numbers preserve denorms.</span></span>

## <a name="11-bit-and-10-bit-floating-point-rules"></a><span data-ttu-id="552e7-170">Regras de Floating-Point de 11 e 10 bits</span><span class="sxs-lookup"><span data-stu-id="552e7-170">11-bit and 10-bit Floating-Point Rules</span></span>

<span data-ttu-id="552e7-171">O Direct3D 10 também dá suporte a formatos de ponto flutuante de 11 e 10 bits.</span><span class="sxs-lookup"><span data-stu-id="552e7-171">Direct3D 10 also supports 11-bit and 10-bit floating-point formats.</span></span>

<span data-ttu-id="552e7-172">Formato:</span><span class="sxs-lookup"><span data-stu-id="552e7-172">Format:</span></span>

-   <span data-ttu-id="552e7-173">Nenhum bit de sinal</span><span class="sxs-lookup"><span data-stu-id="552e7-173">No sign bit</span></span>
-   <span data-ttu-id="552e7-174">5 bits de expoente ajustado (e)</span><span class="sxs-lookup"><span data-stu-id="552e7-174">5 bits of biased exponent (e)</span></span>
-   <span data-ttu-id="552e7-175">6 bits de fração (f) para um formato de 11 bits, 5 bits de fração (f) para um formato de 10 bits, com um bit oculto adicional em ambos os casos.</span><span class="sxs-lookup"><span data-stu-id="552e7-175">6 bits of fraction (f) for an 11-bit format, 5 bits of fraction (f) for a 10-bit format, with an additional hidden bit in either case.</span></span>

<span data-ttu-id="552e7-176">Um valor de float11/float10 (v) segue as regras a seguir:</span><span class="sxs-lookup"><span data-stu-id="552e7-176">A float11/float10 value (v) follows the following rules:</span></span>

-   <span data-ttu-id="552e7-177">se e == 31 and f != 0, então v é NaN</span><span class="sxs-lookup"><span data-stu-id="552e7-177">if e == 31 and f != 0, then v is NaN</span></span>
-   <span data-ttu-id="552e7-178">se e == 31 e f == 0, então v = +infinito</span><span class="sxs-lookup"><span data-stu-id="552e7-178">if e == 31 and f == 0, then v = +infinity</span></span>
-   <span data-ttu-id="552e7-179">se e estiver entre 0 e 31, v = 2 (e-15) \* (1. f)</span><span class="sxs-lookup"><span data-stu-id="552e7-179">if e is between 0 and 31, then v = 2(e-15)\*(1.f)</span></span>
-   <span data-ttu-id="552e7-180">se e = = 0 e f! = 0, v = \* 2 (e-14) \* (0. f) (números desnormalizados)</span><span class="sxs-lookup"><span data-stu-id="552e7-180">if e == 0 and f != 0, then v = \*2(e-14)\*(0.f) (denormalized numbers)</span></span>
-   <span data-ttu-id="552e7-181">se e == 0 e f == 0, então v = 0 (zero)</span><span class="sxs-lookup"><span data-stu-id="552e7-181">if e == 0 and f == 0, then v = 0 (zero)</span></span>

<span data-ttu-id="552e7-182">as regras de ponto flutuante de 32 bits também contêm números de ponto flutuante de 11 e 10 bits, ajustados para o layout de bit descrito acima.</span><span class="sxs-lookup"><span data-stu-id="552e7-182">32-bit floating-point rules also hold for 11-bit and 10-bit floating-point numbers, adjusted for the bit layout described above.</span></span> <span data-ttu-id="552e7-183">As exceções incluem:</span><span class="sxs-lookup"><span data-stu-id="552e7-183">Exceptions include:</span></span>

-   <span data-ttu-id="552e7-184">Precisão: as regras de ponto flutuante de 32 bits aderem a 0,5 ULP.</span><span class="sxs-lookup"><span data-stu-id="552e7-184">Precision: 32-bit floating-point rules adhere to 0.5 ULP.</span></span>
-   <span data-ttu-id="552e7-185">Os números de ponto flutuante de 10/11 bits preservam denorms.</span><span class="sxs-lookup"><span data-stu-id="552e7-185">10/11-bit floating-point numbers preserve denorms.</span></span>
-   <span data-ttu-id="552e7-186">Qualquer operação que resultaria em um número menor que zero é clamped para zero.</span><span class="sxs-lookup"><span data-stu-id="552e7-186">Any operation that would result in a number less than zero, is clamped to zero.</span></span>

## <a name="related-topics"></a><span data-ttu-id="552e7-187">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="552e7-187">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="552e7-188">Recursos (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="552e7-188">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



