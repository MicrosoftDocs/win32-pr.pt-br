---
description: Você pode definir e atribuir escopos de entrada personalizados usando a sintaxe de expressão regular de manuscrito que é compreendida por alguns dos reconhecedores de manuscrito da Microsoft.
ms.assetid: e3afe735-eca8-4fda-bd5b-cc0ab0b6a872
title: Referência de sintaxe de expressão regular
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c0de50ff37795032719d9bc90ee81891324ba9
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104172421"
---
# <a name="regular-expression-syntax-reference"></a><span data-ttu-id="8486c-103">Referência de sintaxe de expressão regular</span><span class="sxs-lookup"><span data-stu-id="8486c-103">Regular Expression Syntax Reference</span></span>

<span data-ttu-id="8486c-104">Você pode definir e atribuir escopos de entrada personalizados usando a sintaxe de expressão regular de manuscrito que é compreendida por alguns dos reconhecedores de manuscrito da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8486c-104">You can define and assign custom input scopes using the handwriting regular expression syntax that is understood by some of the Microsoft handwriting recognizers.</span></span> <span data-ttu-id="8486c-105">A sintaxe é um subconjunto da [implementação da linguagem de expressão regular](/documentation/?url=%2flibrary%2fcpgenref%2fhtml%2fcpconRegularExpressionsLanguageElements.asp%3fframe%3dtrue) no .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="8486c-105">The syntax is a subset of the [Regular Expression Language Implementation](/documentation/?url=%2flibrary%2fcpgenref%2fhtml%2fcpconRegularExpressionsLanguageElements.asp%3fframe%3dtrue) in the .NET Framework.</span></span>

<span data-ttu-id="8486c-106">Há algumas diferenças na maneira como as expressões regulares manuscritas são usadas e a maneira como os outros tipos de expressões regulares são usados.</span><span class="sxs-lookup"><span data-stu-id="8486c-106">There are some differences in the way that handwriting regular expressions are used and the way the other types of regular expressions are used.</span></span> <span data-ttu-id="8486c-107">A sintaxe de manuscrito é usada para especificar uma cadeia de caracteres exata que será correspondida pelo mecanismo de reconhecimento e não por uma subcadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8486c-107">The handwriting syntax is used to specify an exact string that will be matched by the recognition engine and not a sub-string.</span></span> <span data-ttu-id="8486c-108">Por exemplo, a expressão regular s ( \[ a-z \] +) p retornaria correspondências para "sopa", "parar", "inetapa" e "esophagus".</span><span class="sxs-lookup"><span data-stu-id="8486c-108">For example, the regular expression s(\[a-z\]+)p would return matches for "soup", "stop", "instep", and "esophagus".</span></span> <span data-ttu-id="8486c-109">Enquanto que uma expressão regular de manuscrito equivalente, como s (! IS \_ ONECHAR) + p, corresponderia a "sopa" e "Stop", mas não "Instep" e "esophagus".</span><span class="sxs-lookup"><span data-stu-id="8486c-109">Whereas, an equivalent handwriting regular expression such as s(!IS\_ONECHAR)+p would match "soup" and "stop", but not "instep" and "esophagus".</span></span>

<span data-ttu-id="8486c-110">As expressões regulares manuscritas não dão suporte a espaços não separáveis em expressões regulares.</span><span class="sxs-lookup"><span data-stu-id="8486c-110">Handwriting regular expressions do not support non-breaking spaces within regular expressions.</span></span> <span data-ttu-id="8486c-111">Ou seja, você não pode usar a entidade "nbsp" em uma expressão regular de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="8486c-111">That is, you cannot use the "nbsp" entity within a handwriting regular expression.</span></span>

<span data-ttu-id="8486c-112">As seções a seguir descrevem a sintaxe em mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="8486c-112">The following sections describe the syntax in more detail.</span></span>

## <a name="valid-operators"></a><span data-ttu-id="8486c-113">Operadores válidos</span><span class="sxs-lookup"><span data-stu-id="8486c-113">Valid Operators</span></span>

<span data-ttu-id="8486c-114">Os operadores a seguir são válidos para a criação de expressões regulares para definir escopos de entrada para reconhecedores de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="8486c-114">The following operators are valid for creating regular expressions to define input scopes for handwriting recognizers.</span></span>



| <span data-ttu-id="8486c-115">Operador</span><span class="sxs-lookup"><span data-stu-id="8486c-115">Operator</span></span>      | <span data-ttu-id="8486c-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="8486c-116">Description</span></span>                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| \*<br/> | <span data-ttu-id="8486c-117">Operador unário de sufixo que significa zero ou mais ocorrências do operando.</span><span class="sxs-lookup"><span data-stu-id="8486c-117">Postfix unary operator signifying zero or more occurrences of the operand.</span></span><br/> |
| +<br/>  | <span data-ttu-id="8486c-118">Operador unário de sufixo que representa uma ou mais ocorrências do operando.</span><span class="sxs-lookup"><span data-stu-id="8486c-118">Postfix unary operator signifying one or more occurrences of the operand.</span></span><br/>  |
| <span data-ttu-id="8486c-119">?</span><span class="sxs-lookup"><span data-stu-id="8486c-119">?</span></span><br/>  | <span data-ttu-id="8486c-120">Operador unário de sufixo que significa zero ou uma ocorrência do operando.</span><span class="sxs-lookup"><span data-stu-id="8486c-120">Postfix unary operator signifying zero or one occurrence of the operand.</span></span><br/>   |
| \|<br/> | <span data-ttu-id="8486c-121">Operador de infixos binários que significa "ou".</span><span class="sxs-lookup"><span data-stu-id="8486c-121">Binary infix operator meaning "or".</span></span><br/>                                        |
| <span data-ttu-id="8486c-122">()</span><span class="sxs-lookup"><span data-stu-id="8486c-122">()</span></span><br/> | <span data-ttu-id="8486c-123">Usado para agrupar itens.</span><span class="sxs-lookup"><span data-stu-id="8486c-123">Used to group items.</span></span><br/>                                                       |



 

<span data-ttu-id="8486c-124">A implementação da Microsoft de expressões regulares para reconhecedores de manuscrito permite aplicativos repetidos de operadores unários de sufixo.</span><span class="sxs-lookup"><span data-stu-id="8486c-124">The Microsoft implementation of regular expressions for handwriting recognizers allows repeated applications of postfix unary operators.</span></span> <span data-ttu-id="8486c-125">Por exemplo, a \* \* = (a \* ) \* = a \* , b??</span><span class="sxs-lookup"><span data-stu-id="8486c-125">For example, a\*\* = (a\*)\* = a\*, b??</span></span> <span data-ttu-id="8486c-126">= (b?)?</span><span class="sxs-lookup"><span data-stu-id="8486c-126">= (b?)?</span></span> <span data-ttu-id="8486c-127">= b?.</span><span class="sxs-lookup"><span data-stu-id="8486c-127">= b?.</span></span> <span data-ttu-id="8486c-128">Eles também permitem repetições não consecutivas, por exemplo: a \* ? \* = ((a \* )?) \* = (a \* ) \* = a \* .</span><span class="sxs-lookup"><span data-stu-id="8486c-128">They also allow non-consecutive repetitions, for example: a\*?\* = ((a\*)?)\* = (a\*)\* = a\*.</span></span> <span data-ttu-id="8486c-129">Isso é diferente de .NET Framework expressões regulares, que permitem apenas o?</span><span class="sxs-lookup"><span data-stu-id="8486c-129">This is different from .NET Framework regular expressions, which only allow the ?</span></span> <span data-ttu-id="8486c-130">operador a ser repetido.</span><span class="sxs-lookup"><span data-stu-id="8486c-130">operator to be repeated.</span></span>

<span data-ttu-id="8486c-131">Outra diferença de .NET Framework expressões regulares é que as expressões regulares manuscritas não dão suporte a uma expressão vazia designada com um par de parênteses vazio, ().</span><span class="sxs-lookup"><span data-stu-id="8486c-131">Another difference from .NET Framework regular expressions is that handwriting regular expressions do not support an empty expression designated with an empty pair of parentheses, ().</span></span>

> [!Note]  
> <span data-ttu-id="8486c-132">Somente caracteres na página de código 1252 têm suporte para expressões regulares de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="8486c-132">Only characters in the 1252 codepage are supported for handwriting regular expressions.</span></span>

 

## <a name="using-input-scopes"></a><span data-ttu-id="8486c-133">Usando escopos de entrada</span><span class="sxs-lookup"><span data-stu-id="8486c-133">Using Input Scopes</span></span>

<span data-ttu-id="8486c-134">Você também pode usar o conjunto de escopos de entrada regulares que são definidos como parte da função [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) em suas expressões regulares.</span><span class="sxs-lookup"><span data-stu-id="8486c-134">You can also use the set of regular input scopes that are defined as part of the [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) function in your regular expressions.</span></span> <span data-ttu-id="8486c-135">Por exemplo, o valor de mês (numérico) é \_ Data \_ mês.</span><span class="sxs-lookup"><span data-stu-id="8486c-135">For example, the value for Month (numerical) is IS\_DATE\_MONTH.</span></span> <span data-ttu-id="8486c-136">A sintaxe para especificar um escopo de entrada como parte de uma expressão regular é preceder o valor enumerado do escopo de entrada com um parêntese de abertura e um ponto de exclamação, (!, e colocar um parêntese de fechamento,) no final.</span><span class="sxs-lookup"><span data-stu-id="8486c-136">The syntax for specifying an input scope as part of a regular expression is to prepend the input scope enumerated value with an open parenthesis and an exclamation point, (!, and place a closing parenthesis, ), on the end.</span></span> <span data-ttu-id="8486c-137">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="8486c-137">For example:</span></span>

<span data-ttu-id="8486c-138">(! É \_ Data \_ mês)</span><span class="sxs-lookup"><span data-stu-id="8486c-138">(!IS\_DATE\_MONTH)</span></span>

<span data-ttu-id="8486c-139">Se você combinar o \_ escopo de entrada padrão por Oring-lo com qualquer outro escopo de entrada, o efeito é que o reconhecedor pode retornar qualquer expressão única compatível com o modelo de idioma padrão (por exemplo, uma palavra do dicionário do sistema ou uma data) com ou sem pontuação, ou qualquer valor que atenda ao restante da expressão regular passada para o reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="8486c-139">If you combine the IS\_DEFAULT input scope by ORing it with any other input scope, the effect is that the recognizer can return either any single expression that the default language model supports (for example, one word from the system dictionary or a date) with or without punctuation, or any value that meets the rest of the regular expression passed in to the recognizer.</span></span>

> [!Note]  
> <span data-ttu-id="8486c-140">Os seguintes membros de [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) não têm suporte em expressões regulares: is \_ formulalist, is \_ REGULAREXPRESSION, é \_ SRGS, é \_ XML.</span><span class="sxs-lookup"><span data-stu-id="8486c-140">The following members of [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) are not supported in regular expressions: IS\_PHRASELIST, IS\_REGULAREXPRESSION, IS\_SRGS, IS\_XML.</span></span>

 

## <a name="unsupported-operators"></a><span data-ttu-id="8486c-141">Operadores sem suporte</span><span class="sxs-lookup"><span data-stu-id="8486c-141">Unsupported Operators</span></span>

<span data-ttu-id="8486c-142">Os operadores de expressão regular a seguir não têm suporte ao criar expressões regulares de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="8486c-142">The following regular expression operators are not supported when creating handwriting regular expressions.</span></span>



| <span data-ttu-id="8486c-143">Operador</span><span class="sxs-lookup"><span data-stu-id="8486c-143">Operator</span></span>                                     | <span data-ttu-id="8486c-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="8486c-144">Description</span></span>                                                         |
|----------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8486c-145">.</span><span class="sxs-lookup"><span data-stu-id="8486c-145">.</span></span><br/>                                 | <span data-ttu-id="8486c-146">Caractere de período.</span><span class="sxs-lookup"><span data-stu-id="8486c-146">Period character.</span></span><br/>                                        |
| \[\]<br/>                              | <span data-ttu-id="8486c-147">Colchetes.</span><span class="sxs-lookup"><span data-stu-id="8486c-147">Square brackets.</span></span> <span data-ttu-id="8486c-148">Use parênteses para agrupar itens.</span><span class="sxs-lookup"><span data-stu-id="8486c-148">Use parenthesis for grouping items.</span></span><br/>     |
| {}<br/>                                | <span data-ttu-id="8486c-149">Chaves.</span><span class="sxs-lookup"><span data-stu-id="8486c-149">Curly brackets.</span></span><br/>                                          |
| <span data-ttu-id="8486c-150">(?\# Comentário) e \# \[ Comentário\]</span><span class="sxs-lookup"><span data-stu-id="8486c-150">(?\# comment) and \#\[ comment \]</span></span><br/> | <span data-ttu-id="8486c-151">Comentários.</span><span class="sxs-lookup"><span data-stu-id="8486c-151">Comments.</span></span><br/>                                                |
| $<br/>                                 | <span data-ttu-id="8486c-152">Caractere de cifrão.</span><span class="sxs-lookup"><span data-stu-id="8486c-152">Dollar sign character.</span></span><br/>                                   |
| ^<br/>                                 | <span data-ttu-id="8486c-153">Caractere de cursor.</span><span class="sxs-lookup"><span data-stu-id="8486c-153">Caret character.</span></span><br/>                                         |
| -<br/>                                 | <span data-ttu-id="8486c-154">Caractere de traço.</span><span class="sxs-lookup"><span data-stu-id="8486c-154">Dash character.</span></span> <span data-ttu-id="8486c-155">Deve ou ( \| ) reunir todos os conjuntos de itens.</span><span class="sxs-lookup"><span data-stu-id="8486c-155">Must OR (\|) together all sets of items.</span></span><br/> |



 

## <a name="escaping-characters"></a><span data-ttu-id="8486c-156">Substituindo caracteres</span><span class="sxs-lookup"><span data-stu-id="8486c-156">Escaping Characters</span></span>

<span data-ttu-id="8486c-157">Os caracteres comuns, além daqueles na tabela a seguir, correspondem a si mesmos.</span><span class="sxs-lookup"><span data-stu-id="8486c-157">Ordinary characters, other than the ones in the following table, match themselves.</span></span> <span data-ttu-id="8486c-158">Ou seja, um "a" em uma expressão regular especifica que a entrada deve corresponder a um "a".</span><span class="sxs-lookup"><span data-stu-id="8486c-158">That is, an "a" in a regular expression specifies that input should match an "a".</span></span>

<span data-ttu-id="8486c-159">Outra diferença significativa na escrita de expressões regulares de manuscrito é que você só pode escapar um conjunto limitado de caracteres dentro de uma expressão regular.</span><span class="sxs-lookup"><span data-stu-id="8486c-159">Another significant difference in writing handwriting regular expressions is that you can only escape a limited set of characters within a regular expression.</span></span> <span data-ttu-id="8486c-160">A tabela a seguir descreve o conjunto de caracteres permitido que pode ter escape.</span><span class="sxs-lookup"><span data-stu-id="8486c-160">The following table outlines the allowed set of characters that can be escaped.</span></span> <span data-ttu-id="8486c-161">Qualquer outra tentativa de escapar de um caractere resultará em um erro sendo gerado pelo reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="8486c-161">Any other attempt to escape a character will result in an error being thrown by the recognizer.</span></span>



| <span data-ttu-id="8486c-162">Caractere</span><span class="sxs-lookup"><span data-stu-id="8486c-162">Character</span></span>       |
|-----------------|
| \\\*<br/> |
| \\+<br/>  |
| <span data-ttu-id="8486c-163">\\?</span><span class="sxs-lookup"><span data-stu-id="8486c-163">\\?</span></span><br/>  |
| <span data-ttu-id="8486c-164">\\(</span><span class="sxs-lookup"><span data-stu-id="8486c-164">\\(</span></span><br/>  |
| <span data-ttu-id="8486c-165">\\)</span><span class="sxs-lookup"><span data-stu-id="8486c-165">\\)</span></span><br/>  |
| \\\|<br/> |
| \\\\<br/> |
| <span data-ttu-id="8486c-166">\\!</span><span class="sxs-lookup"><span data-stu-id="8486c-166">\\!</span></span><br/>  |
| <span data-ttu-id="8486c-167">\\.</span><span class="sxs-lookup"><span data-stu-id="8486c-167">\\.</span></span><br/>  |
| \\\[<br/> |
| \\\]<br/> |
| \\^<br/>  |
| <span data-ttu-id="8486c-168">\\{</span><span class="sxs-lookup"><span data-stu-id="8486c-168">\\{</span></span><br/>  |
| <span data-ttu-id="8486c-169">\\}</span><span class="sxs-lookup"><span data-stu-id="8486c-169">\\}</span></span><br/>  |
| \\$<br/>  |
| \\\#<br/> |



 

 

 