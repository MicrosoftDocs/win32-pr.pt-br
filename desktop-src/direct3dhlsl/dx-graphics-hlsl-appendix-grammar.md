---
title: Gramática
description: As instruções HLSL são construídas usando as regras a seguir para gramática.
ms.assetid: 683248e9-6fc7-451a-906b-6e0aab1b0c8c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d2346e1ca2302f80c796558b4aa2bbdce016d494
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104498954"
---
# <a name="grammar"></a><span data-ttu-id="53440-103">Gramática</span><span class="sxs-lookup"><span data-stu-id="53440-103">Grammar</span></span>

<span data-ttu-id="53440-104">As instruções HLSL são construídas usando as regras a seguir para gramática.</span><span class="sxs-lookup"><span data-stu-id="53440-104">HLSL statements are constructed using the following rules for grammar.</span></span>

-   [<span data-ttu-id="53440-105">Espaço em branco</span><span class="sxs-lookup"><span data-stu-id="53440-105">Whitespace</span></span>](#whitespace)
-   [<span data-ttu-id="53440-106">Números de ponto flutuante</span><span class="sxs-lookup"><span data-stu-id="53440-106">Floating point numbers</span></span>](#floating-point-numbers)
-   [<span data-ttu-id="53440-107">Números inteiros</span><span class="sxs-lookup"><span data-stu-id="53440-107">Integer numbers</span></span>](#integer-numbers)
-   [<span data-ttu-id="53440-108">Characters</span><span class="sxs-lookup"><span data-stu-id="53440-108">Characters</span></span>](#characters)
-   [<span data-ttu-id="53440-109">Cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="53440-109">Strings</span></span>](#strings)
-   [<span data-ttu-id="53440-110">Identificadores</span><span class="sxs-lookup"><span data-stu-id="53440-110">Identifiers</span></span>](#identifiers)
-   [<span data-ttu-id="53440-111">Operadores</span><span class="sxs-lookup"><span data-stu-id="53440-111">Operators</span></span>](#operators)
-   [<span data-ttu-id="53440-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="53440-112">Related topics</span></span>](#related-topics)

## <a name="whitespace"></a><span data-ttu-id="53440-113">Espaço em branco</span><span class="sxs-lookup"><span data-stu-id="53440-113">Whitespace</span></span>

<span data-ttu-id="53440-114">Os caracteres a seguir são reconhecidos como espaços em branco.</span><span class="sxs-lookup"><span data-stu-id="53440-114">The following characters are recognized as white space.</span></span>



|                            |
|----------------------------|
| <span data-ttu-id="53440-115">SPACE</span><span class="sxs-lookup"><span data-stu-id="53440-115">SPACE</span></span>                      |
| <span data-ttu-id="53440-116">TAB</span><span class="sxs-lookup"><span data-stu-id="53440-116">TAB</span></span>                        |
| <span data-ttu-id="53440-117">MERCADO</span><span class="sxs-lookup"><span data-stu-id="53440-117">EOL</span></span>                        |
| <span data-ttu-id="53440-118">Comentários de estilo C (/ \* \* /)</span><span class="sxs-lookup"><span data-stu-id="53440-118">C style comments (/\* \*/)</span></span> |
| <span data-ttu-id="53440-119">Comentários de estilo C++ (//)</span><span class="sxs-lookup"><span data-stu-id="53440-119">C++ style comments (//)</span></span>    |



 

## <a name="floating-point-numbers"></a><span data-ttu-id="53440-120">Números de ponto flutuante</span><span class="sxs-lookup"><span data-stu-id="53440-120">Floating point numbers</span></span>

<span data-ttu-id="53440-121">Os números de ponto flutuante são representados em HLSL da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="53440-121">Floating point numbers are represented in HLSL as follows:</span></span>

-   <span data-ttu-id="53440-122">fração fracionária-parte do expoente (opt) de sufixo flutuante (opcional)</span><span class="sxs-lookup"><span data-stu-id="53440-122">fractional-constant exponent-part(opt) floating-suffix(opt)</span></span>

    <span data-ttu-id="53440-123">expoente de sequência de dígitos – sufixo de parte flutuante (opt)</span><span class="sxs-lookup"><span data-stu-id="53440-123">digit-sequence exponent-part floating-suffix(opt)</span></span>

-   <span data-ttu-id="53440-124">fração fracionária:</span><span class="sxs-lookup"><span data-stu-id="53440-124">fractional-constant :</span></span>

    <span data-ttu-id="53440-125">sequência de dígitos (opt).</span><span class="sxs-lookup"><span data-stu-id="53440-125">digit-sequence(opt) .</span></span> <span data-ttu-id="53440-126">digit-sequence</span><span class="sxs-lookup"><span data-stu-id="53440-126">digit-sequence</span></span>

    <span data-ttu-id="53440-127">sequência de dígitos.</span><span class="sxs-lookup"><span data-stu-id="53440-127">digit-sequence .</span></span>

-   <span data-ttu-id="53440-128">expoente – parte:</span><span class="sxs-lookup"><span data-stu-id="53440-128">exponent-part :</span></span>

    <span data-ttu-id="53440-129">sequência de dígitos de sinal e (opt)</span><span class="sxs-lookup"><span data-stu-id="53440-129">e sign(opt) digit-sequence</span></span>

    <span data-ttu-id="53440-130">Sequência de dígitos de sinal E (opt)</span><span class="sxs-lookup"><span data-stu-id="53440-130">E sign(opt) digit-sequence</span></span>

-   <span data-ttu-id="53440-131">sign : one of</span><span class="sxs-lookup"><span data-stu-id="53440-131">sign : one of</span></span>

    \+ -

-   <span data-ttu-id="53440-132">sequência de dígitos:</span><span class="sxs-lookup"><span data-stu-id="53440-132">digit-sequence :</span></span>

    <span data-ttu-id="53440-133">{1&gt;digit&lt;1}</span><span class="sxs-lookup"><span data-stu-id="53440-133">digit</span></span>

    <span data-ttu-id="53440-134">digit-sequence digit</span><span class="sxs-lookup"><span data-stu-id="53440-134">digit-sequence digit</span></span>

-   <span data-ttu-id="53440-135">floating-suffix : one of</span><span class="sxs-lookup"><span data-stu-id="53440-135">floating-suffix : one of</span></span>

    <span data-ttu-id="53440-136">h H f F l</span><span class="sxs-lookup"><span data-stu-id="53440-136">h H f F l L</span></span>

    <span data-ttu-id="53440-137">Use o sufixo "L" para especificar um literal de ponto flutuante de precisão de 64 bits completo.</span><span class="sxs-lookup"><span data-stu-id="53440-137">Use the “L” suffix to specify a full 64-bit precision floating-point literal.</span></span> <span data-ttu-id="53440-138">Um literal de float de 32 bits é o padrão.</span><span class="sxs-lookup"><span data-stu-id="53440-138">A 32-bit float literal is the default.</span></span>

    <span data-ttu-id="53440-139">Por exemplo, o compilador reconhece o valor literal a seguir como um literal de ponto flutuante de precisão de 32 bits e ignora os bits inferiores:</span><span class="sxs-lookup"><span data-stu-id="53440-139">For example, the compiler recognizes the following literal value as a 32-bit precision floating-point literal and ignores the lower bits:</span></span>

    ```
    double x = -0.6473313946860445;
    ```

    

    <span data-ttu-id="53440-140">O compilador reconhece o seguinte valor literal como um literal de ponto flutuante de precisão de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="53440-140">The compiler recognizes the following literal value as a 64-bit precision floating-point literal:</span></span>

    ```
    double x = -0.6473313946860445L;
    ```

    

## <a name="integer-numbers"></a><span data-ttu-id="53440-141">Números inteiros</span><span class="sxs-lookup"><span data-stu-id="53440-141">Integer numbers</span></span>

<span data-ttu-id="53440-142">Os números inteiros são representados em HLSL da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="53440-142">Integer numbers are represented in HLSL as follows:</span></span>

-   <span data-ttu-id="53440-143">Integer-inteiro constante-sufixo (opt)</span><span class="sxs-lookup"><span data-stu-id="53440-143">integer-constant integer-suffix(opt)</span></span>
-   <span data-ttu-id="53440-144">inteiro-constante: uma das</span><span class="sxs-lookup"><span data-stu-id="53440-144">integer-constant: one of</span></span>

    <span data-ttu-id="53440-145">\# (número decimal)</span><span class="sxs-lookup"><span data-stu-id="53440-145">\# (decimal number)</span></span>

    <span data-ttu-id="53440-146">0 \# (número octal)</span><span class="sxs-lookup"><span data-stu-id="53440-146">0\# (octal number)</span></span>

    <span data-ttu-id="53440-147">0x \# (número hexadecimal)</span><span class="sxs-lookup"><span data-stu-id="53440-147">0x\# (hex number)</span></span>

-   <span data-ttu-id="53440-148">o sufixo inteiro pode ser qualquer um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="53440-148">integer-suffix can be any one of these:</span></span>

    <span data-ttu-id="53440-149">u U l l</span><span class="sxs-lookup"><span data-stu-id="53440-149">u U l L</span></span>

## <a name="characters"></a><span data-ttu-id="53440-150">Characters</span><span class="sxs-lookup"><span data-stu-id="53440-150">Characters</span></span>

<span data-ttu-id="53440-151">Os caracteres são representados em HLSL da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="53440-151">Characters are represented in HLSL as follows:</span></span>



|                                           |                                                                 |
|-------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="53440-152">&</span><span class="sxs-lookup"><span data-stu-id="53440-152">'c'</span></span>                                       | <span data-ttu-id="53440-153">espaço</span><span class="sxs-lookup"><span data-stu-id="53440-153">(character)</span></span>                                                     |
| <span data-ttu-id="53440-154">' \\ a ' ' \\ b ' ' \\ f ' ' \\ b ' ' \\ r ' ' \\ t ' ' \\ v '</span><span class="sxs-lookup"><span data-stu-id="53440-154">'\\a' '\\b' '\\f' '\\b' '\\r' '\\t' '\\v'</span></span> | <span data-ttu-id="53440-155">ignora</span><span class="sxs-lookup"><span data-stu-id="53440-155">(escapes)</span></span>                                                       |
| <span data-ttu-id="53440-156">'\\\#\#\#'</span><span class="sxs-lookup"><span data-stu-id="53440-156">'\\\#\#\#'</span></span>                                | <span data-ttu-id="53440-157">(escape octal, cada \# um é um dígito octal)</span><span class="sxs-lookup"><span data-stu-id="53440-157">(octal escape, each \# is an octal digit)</span></span>                       |
| <span data-ttu-id="53440-158">' \\ x \# '</span><span class="sxs-lookup"><span data-stu-id="53440-158">'\\x\#'</span></span>                                   | <span data-ttu-id="53440-159">(escape Hex, \# é número hexadecimal, qualquer número de dígitos)</span><span class="sxs-lookup"><span data-stu-id="53440-159">(hex escape, \# is hex number, any number of digits)</span></span>            |
| <span data-ttu-id="53440-160">' \\ C'</span><span class="sxs-lookup"><span data-stu-id="53440-160">'\\c'</span></span>                                     | <span data-ttu-id="53440-161">(c é outro caractere, incluindo barra invertida e aspas)</span><span class="sxs-lookup"><span data-stu-id="53440-161">(c is other character, including backslash and quotation marks)</span></span> |



 

<span data-ttu-id="53440-162">Não há suporte para escapes em expressões de pré-processador.</span><span class="sxs-lookup"><span data-stu-id="53440-162">Escapes are not supported in preprocessor expressions.</span></span>

## <a name="strings"></a><span data-ttu-id="53440-163">Cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="53440-163">Strings</span></span>

<span data-ttu-id="53440-164">As cadeias de caracteres são representadas em HLSL da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="53440-164">Strings are represented in HLSL as follows:</span></span>

<span data-ttu-id="53440-165">"s" (s é qualquer cadeia de caracteres com escapes).</span><span class="sxs-lookup"><span data-stu-id="53440-165">"s" (s is any string with escapes).</span></span>

## <a name="identifiers"></a><span data-ttu-id="53440-166">Identificadores</span><span class="sxs-lookup"><span data-stu-id="53440-166">Identifiers</span></span>

<span data-ttu-id="53440-167">Os identificadores são representados em HLSL da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="53440-167">Identifiers are represented in HLSL as follows:</span></span>


```
    [A-Za-z_][A-Za-z0-9_]*
```



## <a name="operators"></a><span data-ttu-id="53440-168">Operadores</span><span class="sxs-lookup"><span data-stu-id="53440-168">Operators</span></span>


```
##, #@, ++, --, &, &, &, ||, ==, ::, <<, <<=, >>, >>=, ..., 
<=, >=, !=, *=, /=, +=, -=, %=, &=, |=, ^=, ->
```



<span data-ttu-id="53440-169">Também qualquer outro caractere único que não corresponde a outra regra.</span><span class="sxs-lookup"><span data-stu-id="53440-169">Also any other single character that did not match another rule.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53440-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="53440-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53440-171">Apêndice (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="53440-171">Appendix (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




