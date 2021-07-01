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
ms.openlocfilehash: b77f1050beaee2b269d12e69704018e3c5abee6e
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129844"
---
# <a name="grammar"></a><span data-ttu-id="866c8-103">Gramática</span><span class="sxs-lookup"><span data-stu-id="866c8-103">Grammar</span></span>

<span data-ttu-id="866c8-104">As instruções HLSL são construídas usando as regras a seguir para gramática.</span><span class="sxs-lookup"><span data-stu-id="866c8-104">HLSL statements are constructed using the following rules for grammar.</span></span>

-   [<span data-ttu-id="866c8-105">Diferente</span><span class="sxs-lookup"><span data-stu-id="866c8-105">Whitespace</span></span>](#whitespace)
-   [<span data-ttu-id="866c8-106">Números de ponto flutuante</span><span class="sxs-lookup"><span data-stu-id="866c8-106">Floating point numbers</span></span>](#floating-point-numbers)
-   [<span data-ttu-id="866c8-107">Números inteiros</span><span class="sxs-lookup"><span data-stu-id="866c8-107">Integer numbers</span></span>](#integer-numbers)
-   [<span data-ttu-id="866c8-108">Characters</span><span class="sxs-lookup"><span data-stu-id="866c8-108">Characters</span></span>](#characters)
-   [<span data-ttu-id="866c8-109">Cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="866c8-109">Strings</span></span>](#strings)
-   [<span data-ttu-id="866c8-110">Identificadores</span><span class="sxs-lookup"><span data-stu-id="866c8-110">Identifiers</span></span>](#identifiers)
-   [<span data-ttu-id="866c8-111">Operadores</span><span class="sxs-lookup"><span data-stu-id="866c8-111">Operators</span></span>](#operators)
-   [<span data-ttu-id="866c8-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="866c8-112">Related topics</span></span>](#related-topics)

## <a name="whitespace"></a><span data-ttu-id="866c8-113">Espaço em branco</span><span class="sxs-lookup"><span data-stu-id="866c8-113">Whitespace</span></span>

<span data-ttu-id="866c8-114">Os caracteres a seguir são reconhecidos como espaços em branco.</span><span class="sxs-lookup"><span data-stu-id="866c8-114">The following characters are recognized as white space.</span></span>

- <span data-ttu-id="866c8-115">SPACE</span><span class="sxs-lookup"><span data-stu-id="866c8-115">SPACE</span></span>
- <span data-ttu-id="866c8-116">TAB</span><span class="sxs-lookup"><span data-stu-id="866c8-116">TAB</span></span>
- <span data-ttu-id="866c8-117">MERCADO</span><span class="sxs-lookup"><span data-stu-id="866c8-117">EOL</span></span>
- <span data-ttu-id="866c8-118">Comentários de estilo C (/ \* \* /)</span><span class="sxs-lookup"><span data-stu-id="866c8-118">C style comments (/\* \*/)</span></span>
- <span data-ttu-id="866c8-119">Comentários de estilo C++ (//)</span><span class="sxs-lookup"><span data-stu-id="866c8-119">C++ style comments (//)</span></span>

## <a name="floating-point-numbers"></a><span data-ttu-id="866c8-120">Números de ponto flutuante</span><span class="sxs-lookup"><span data-stu-id="866c8-120">Floating point numbers</span></span>

<span data-ttu-id="866c8-121">Os números de ponto flutuante são representados em HLSL da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="866c8-121">Floating point numbers are represented in HLSL as follows:</span></span>

-   <span data-ttu-id="866c8-122">fração fracionária-parte do expoente (opt) de sufixo flutuante (opcional)</span><span class="sxs-lookup"><span data-stu-id="866c8-122">fractional-constant exponent-part(opt) floating-suffix(opt)</span></span>

    <span data-ttu-id="866c8-123">expoente de sequência de dígitos – sufixo de parte flutuante (opt)</span><span class="sxs-lookup"><span data-stu-id="866c8-123">digit-sequence exponent-part floating-suffix(opt)</span></span>

-   <span data-ttu-id="866c8-124">fração fracionária:</span><span class="sxs-lookup"><span data-stu-id="866c8-124">fractional-constant :</span></span>

    <span data-ttu-id="866c8-125">sequência de dígitos (opt).</span><span class="sxs-lookup"><span data-stu-id="866c8-125">digit-sequence(opt) .</span></span> <span data-ttu-id="866c8-126">digit-sequence</span><span class="sxs-lookup"><span data-stu-id="866c8-126">digit-sequence</span></span>

    <span data-ttu-id="866c8-127">sequência de dígitos.</span><span class="sxs-lookup"><span data-stu-id="866c8-127">digit-sequence .</span></span>

-   <span data-ttu-id="866c8-128">expoente – parte:</span><span class="sxs-lookup"><span data-stu-id="866c8-128">exponent-part :</span></span>

    <span data-ttu-id="866c8-129">sequência de dígitos de sinal e (opt)</span><span class="sxs-lookup"><span data-stu-id="866c8-129">e sign(opt) digit-sequence</span></span>

    <span data-ttu-id="866c8-130">Sequência de dígitos de sinal E (opt)</span><span class="sxs-lookup"><span data-stu-id="866c8-130">E sign(opt) digit-sequence</span></span>

-   <span data-ttu-id="866c8-131">sign : one of</span><span class="sxs-lookup"><span data-stu-id="866c8-131">sign : one of</span></span>

    \+ -

-   <span data-ttu-id="866c8-132">sequência de dígitos:</span><span class="sxs-lookup"><span data-stu-id="866c8-132">digit-sequence :</span></span>

    <span data-ttu-id="866c8-133">{1&gt;digit&lt;1}</span><span class="sxs-lookup"><span data-stu-id="866c8-133">digit</span></span>

    <span data-ttu-id="866c8-134">digit-sequence digit</span><span class="sxs-lookup"><span data-stu-id="866c8-134">digit-sequence digit</span></span>

-   <span data-ttu-id="866c8-135">floating-suffix : one of</span><span class="sxs-lookup"><span data-stu-id="866c8-135">floating-suffix : one of</span></span>

    <span data-ttu-id="866c8-136">h H f F l</span><span class="sxs-lookup"><span data-stu-id="866c8-136">h H f F l L</span></span>

    <span data-ttu-id="866c8-137">Use o sufixo "L" para especificar um literal de ponto flutuante de precisão de 64 bits completo.</span><span class="sxs-lookup"><span data-stu-id="866c8-137">Use the “L” suffix to specify a full 64-bit precision floating-point literal.</span></span> <span data-ttu-id="866c8-138">Um literal de float de 32 bits é o padrão.</span><span class="sxs-lookup"><span data-stu-id="866c8-138">A 32-bit float literal is the default.</span></span>

    <span data-ttu-id="866c8-139">Por exemplo, o compilador reconhece o valor literal a seguir como um literal de ponto flutuante de precisão de 32 bits e ignora os bits inferiores:</span><span class="sxs-lookup"><span data-stu-id="866c8-139">For example, the compiler recognizes the following literal value as a 32-bit precision floating-point literal and ignores the lower bits:</span></span>

    ```
    double x = -0.6473313946860445;
    ```

    

    <span data-ttu-id="866c8-140">O compilador reconhece o seguinte valor literal como um literal de ponto flutuante de precisão de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="866c8-140">The compiler recognizes the following literal value as a 64-bit precision floating-point literal:</span></span>

    ```
    double x = -0.6473313946860445L;
    ```

    

## <a name="integer-numbers"></a><span data-ttu-id="866c8-141">Números inteiros</span><span class="sxs-lookup"><span data-stu-id="866c8-141">Integer numbers</span></span>

<span data-ttu-id="866c8-142">Os números inteiros são representados em HLSL da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="866c8-142">Integer numbers are represented in HLSL as follows:</span></span>

-   <span data-ttu-id="866c8-143">Integer-inteiro constante-sufixo (opt)</span><span class="sxs-lookup"><span data-stu-id="866c8-143">integer-constant integer-suffix(opt)</span></span>
-   <span data-ttu-id="866c8-144">inteiro-constante: uma das</span><span class="sxs-lookup"><span data-stu-id="866c8-144">integer-constant: one of</span></span>

    <span data-ttu-id="866c8-145">\# (número decimal)</span><span class="sxs-lookup"><span data-stu-id="866c8-145">\# (decimal number)</span></span>

    <span data-ttu-id="866c8-146">0 \# (número octal)</span><span class="sxs-lookup"><span data-stu-id="866c8-146">0\# (octal number)</span></span>

    <span data-ttu-id="866c8-147">0x \# (número hexadecimal)</span><span class="sxs-lookup"><span data-stu-id="866c8-147">0x\# (hex number)</span></span>

-   <span data-ttu-id="866c8-148">o sufixo inteiro pode ser qualquer um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="866c8-148">integer-suffix can be any one of these:</span></span>

    <span data-ttu-id="866c8-149">u U l l</span><span class="sxs-lookup"><span data-stu-id="866c8-149">u U l L</span></span>

## <a name="characters"></a><span data-ttu-id="866c8-150">Characters</span><span class="sxs-lookup"><span data-stu-id="866c8-150">Characters</span></span>

<span data-ttu-id="866c8-151">Os caracteres são representados em HLSL da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="866c8-151">Characters are represented in HLSL as follows:</span></span>



| <span data-ttu-id="866c8-152">Caractere</span><span class="sxs-lookup"><span data-stu-id="866c8-152">Character</span></span>                                          | <span data-ttu-id="866c8-153">Descrição</span><span class="sxs-lookup"><span data-stu-id="866c8-153">Description</span></span>                                                                |
|-------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="866c8-154">'c'</span><span class="sxs-lookup"><span data-stu-id="866c8-154">'c'</span></span>                                       | <span data-ttu-id="866c8-155">espaço</span><span class="sxs-lookup"><span data-stu-id="866c8-155">(character)</span></span>                                                     |
| <span data-ttu-id="866c8-156">' \\ a ' ' \\ b ' ' \\ f ' ' \\ b ' ' \\ r ' ' \\ t ' ' \\ v '</span><span class="sxs-lookup"><span data-stu-id="866c8-156">'\\a' '\\b' '\\f' '\\b' '\\r' '\\t' '\\v'</span></span> | <span data-ttu-id="866c8-157">ignora</span><span class="sxs-lookup"><span data-stu-id="866c8-157">(escapes)</span></span>                                                       |
| <span data-ttu-id="866c8-158">'\\\#\#\#'</span><span class="sxs-lookup"><span data-stu-id="866c8-158">'\\\#\#\#'</span></span>                                | <span data-ttu-id="866c8-159">(escape octal, cada \# um é um dígito octal)</span><span class="sxs-lookup"><span data-stu-id="866c8-159">(octal escape, each \# is an octal digit)</span></span>                       |
| <span data-ttu-id="866c8-160">' \\ x \# '</span><span class="sxs-lookup"><span data-stu-id="866c8-160">'\\x\#'</span></span>                                   | <span data-ttu-id="866c8-161">(escape Hex, \# é número hexadecimal, qualquer número de dígitos)</span><span class="sxs-lookup"><span data-stu-id="866c8-161">(hex escape, \# is hex number, any number of digits)</span></span>            |
| <span data-ttu-id="866c8-162">' \\ C'</span><span class="sxs-lookup"><span data-stu-id="866c8-162">'\\c'</span></span>                                     | <span data-ttu-id="866c8-163">(c é outro caractere, incluindo barra invertida e aspas)</span><span class="sxs-lookup"><span data-stu-id="866c8-163">(c is other character, including backslash and quotation marks)</span></span> |



 

<span data-ttu-id="866c8-164">Não há suporte para escapes em expressões de pré-processador.</span><span class="sxs-lookup"><span data-stu-id="866c8-164">Escapes are not supported in preprocessor expressions.</span></span>

## <a name="strings"></a><span data-ttu-id="866c8-165">Cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="866c8-165">Strings</span></span>

<span data-ttu-id="866c8-166">As cadeias de caracteres são representadas em HLSL da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="866c8-166">Strings are represented in HLSL as follows:</span></span>

<span data-ttu-id="866c8-167">"s" (s é qualquer cadeia de caracteres com escapes).</span><span class="sxs-lookup"><span data-stu-id="866c8-167">"s" (s is any string with escapes).</span></span>

## <a name="identifiers"></a><span data-ttu-id="866c8-168">Identificadores</span><span class="sxs-lookup"><span data-stu-id="866c8-168">Identifiers</span></span>

<span data-ttu-id="866c8-169">Os identificadores são representados em HLSL da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="866c8-169">Identifiers are represented in HLSL as follows:</span></span>


```
    [A-Za-z_][A-Za-z0-9_]*
```



## <a name="operators"></a><span data-ttu-id="866c8-170">Operadores</span><span class="sxs-lookup"><span data-stu-id="866c8-170">Operators</span></span>


```
##, #@, ++, --, &, &, &, ||, ==, ::, <<, <<=, >>, >>=, ..., 
<=, >=, !=, *=, /=, +=, -=, %=, &=, |=, ^=, ->
```



<span data-ttu-id="866c8-171">Também qualquer outro caractere único que não corresponde a outra regra.</span><span class="sxs-lookup"><span data-stu-id="866c8-171">Also any other single character that did not match another rule.</span></span>

## <a name="related-topics"></a><span data-ttu-id="866c8-172">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="866c8-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="866c8-173">Apêndice (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="866c8-173">Appendix (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




