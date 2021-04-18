---
description: O predicado LIKE executa a comparação de correspondência de padrões na coluna especificada.
ms.assetid: d4bcf406-1253-4e56-b770-79edd4a98205
title: Predicado LIKE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba042fb2fe3005e062e7961a048a81a64c0c144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814581"
---
# <a name="like-predicate"></a><span data-ttu-id="76785-103">Predicado LIKE</span><span class="sxs-lookup"><span data-stu-id="76785-103">LIKE Predicate</span></span>

<span data-ttu-id="76785-104">O predicado LIKE executa a comparação de correspondência de padrões na coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="76785-104">The LIKE predicate performs pattern-matching comparison on the specified column.</span></span> <span data-ttu-id="76785-105">Ela usa a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="76785-105">It uses the following syntax:</span></span>


```
...WHERE <column> LIKE '<wildcard_literal>'
```



<span data-ttu-id="76785-106">O <column> pode ser um [identificador](-search-sql-identifiers.md)regular ou delimitado.</span><span class="sxs-lookup"><span data-stu-id="76785-106">The <column> can be a regular or delimited [identifier](-search-sql-identifiers.md).</span></span> <span data-ttu-id="76785-107">A coluna é limitada às propriedades no repositório de propriedades.</span><span class="sxs-lookup"><span data-stu-id="76785-107">The column is limited to the properties in the property store.</span></span>

<span data-ttu-id="76785-108">O literal de curinga <\_> é um literal de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="76785-108">The <wildcard\_literal> is a string literal.</span></span> <span data-ttu-id="76785-109">Ele é colocado entre aspas e, opcionalmente, pode conter caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="76785-109">It is enclosed in quotation marks and optionally can contain wildcard characters.</span></span> <span data-ttu-id="76785-110">A cadeia de caracteres de correspondência pode conter vários caracteres curinga, se necessário.</span><span class="sxs-lookup"><span data-stu-id="76785-110">The match string can contain multiple wildcard characters if needed.</span></span> <span data-ttu-id="76785-111">A tabela a seguir descreve os caracteres curinga que o predicado LIKE reconhece.</span><span class="sxs-lookup"><span data-stu-id="76785-111">The following table describes the wildcard characters that the LIKE predicate recognizes.</span></span>



| <span data-ttu-id="76785-112">Curinga</span><span class="sxs-lookup"><span data-stu-id="76785-112">Wildcard</span></span>                | <span data-ttu-id="76785-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="76785-113">Description</span></span>                                                                                                                                                                                     | <span data-ttu-id="76785-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="76785-114">Example</span></span>                                                                                                                                                                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76785-115">% (porcentagem)</span><span class="sxs-lookup"><span data-stu-id="76785-115">% (percent)</span></span>             | <span data-ttu-id="76785-116">Corresponde a zero ou mais caracteres.</span><span class="sxs-lookup"><span data-stu-id="76785-116">Matches zero or more of any characters.</span></span>                                                                                                                                                         | <span data-ttu-id="76785-117">' comp% r ' corresponde a ' comp ' seguido de zero ou mais caracteres, terminando em um r.</span><span class="sxs-lookup"><span data-stu-id="76785-117">'comp%r' matches 'comp' followed by zero or more of any characters, ending in an r.</span></span>                                                                                                                                  |
| <span data-ttu-id="76785-118">\_ sublinhado</span><span class="sxs-lookup"><span data-stu-id="76785-118">\_ (underscore)</span></span>         | <span data-ttu-id="76785-119">Corresponde a qualquer caractere único.</span><span class="sxs-lookup"><span data-stu-id="76785-119">Matches any single character.</span></span>                                                                                                                                                                   | <span data-ttu-id="76785-120">' compse \_ ' corresponde a ' comp ' seguido de exatamente um de qualquer caractere, seguido de ' los '.</span><span class="sxs-lookup"><span data-stu-id="76785-120">'comp\_ter' matches 'comp' followed by exactly one of any character, followed by 'ter'.</span></span>                                                                                                                              |
| <span data-ttu-id="76785-121">\[\](colchetes)</span><span class="sxs-lookup"><span data-stu-id="76785-121">\[ \] (square brackets)</span></span> | <span data-ttu-id="76785-122">Corresponde a qualquer caractere único dentro do intervalo ou conjunto especificado.</span><span class="sxs-lookup"><span data-stu-id="76785-122">Matches any single character within the specified range or set.</span></span> <span data-ttu-id="76785-123">Por exemplo, \[ a-z \] especifica um intervalo; \[ aeiou \] especifica o conjunto de vogais.</span><span class="sxs-lookup"><span data-stu-id="76785-123">For example, \[a-z\] specifies a range; \[aeiou\] specifies the set of vowels.</span></span>                                                  | <span data-ttu-id="76785-124">' comp \[ a-z \] re ' corresponde a ' comp ' seguido de um único caractere no intervalo de a até z, seguido de is '.</span><span class="sxs-lookup"><span data-stu-id="76785-124">'comp\[a-z\]re' matches 'comp' followed by a single character in the range of a through z, followed by 're'.</span></span> <span data-ttu-id="76785-125">' comp \[ ' \] corresponde a ' comp ' seguido de um único caractere que deve ser um ou um.</span><span class="sxs-lookup"><span data-stu-id="76785-125">'comp\[ao\]' matches 'comp' followed by a single character that must be either an a or an o.</span></span><br/> |
| <span data-ttu-id="76785-126">\[^ \] acento</span><span class="sxs-lookup"><span data-stu-id="76785-126">\[^ \] (caret)</span></span>          | <span data-ttu-id="76785-127">Corresponde a qualquer caractere único que não esteja dentro do intervalo ou conjunto especificado.</span><span class="sxs-lookup"><span data-stu-id="76785-127">Matches any single character that is not within the specified range or set.</span></span> <span data-ttu-id="76785-128">Por exemplo, \[ ^ a-z \] especifica um intervalo que exclui de a a z; \[ ^ aeiou \] especifica um conjunto que exclui as vogais.</span><span class="sxs-lookup"><span data-stu-id="76785-128">For example, \[^a-z\] specifies a range that excludes a through z; \[^aeiou\] specifies a set that excludes vowels.</span></span> | <span data-ttu-id="76785-129">' comp \[ ^ u \] ' corresponde a ' comp ' seguido de qualquer caractere único que não seja um u.</span><span class="sxs-lookup"><span data-stu-id="76785-129">'comp\[^u\]' matches 'comp' followed by any single character that is not a u.</span></span>                                                                                                                                        |



 

<span data-ttu-id="76785-130">Se você criar predicados com vários intervalos, os intervalos deverão estar em ordem.</span><span class="sxs-lookup"><span data-stu-id="76785-130">If you create predicates with multiple ranges, the ranges must be in order.</span></span>

> [!Note]  
> <span data-ttu-id="76785-131">Para corresponder os caracteres curinga como caracteres literais para correspondência e não como caracteres curinga, coloque o caractere dentro de colchetes.</span><span class="sxs-lookup"><span data-stu-id="76785-131">To match the wildcard characters as literal characters for matching and not as wildcard characters, place the character inside square brackets.</span></span> <span data-ttu-id="76785-132">Por exemplo, para corresponder ao sinal de porcentagem, use ' \[ % \] '</span><span class="sxs-lookup"><span data-stu-id="76785-132">For example, to match the percent sign, use '\[%\]'</span></span>

 

## <a name="examples"></a><span data-ttu-id="76785-133">Exemplos</span><span class="sxs-lookup"><span data-stu-id="76785-133">Examples</span></span>


```
...WHERE System.ItemNameDisplay LIKE 'financ%'
```



## <a name="related-topics"></a><span data-ttu-id="76785-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="76785-134">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="76785-135">**Referência**</span><span class="sxs-lookup"><span data-stu-id="76785-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="76785-136">Comparação de valor literal</span><span class="sxs-lookup"><span data-stu-id="76785-136">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="76785-137">Comparações de vários valores (matriz)</span><span class="sxs-lookup"><span data-stu-id="76785-137">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

[<span data-ttu-id="76785-138">Predicado nulo</span><span class="sxs-lookup"><span data-stu-id="76785-138">NULL Predicate</span></span>](-search-sql-null.md)
</dt> <dt>

<span data-ttu-id="76785-139">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="76785-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="76785-140">Predicados de texto completo</span><span class="sxs-lookup"><span data-stu-id="76785-140">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="76785-141">Predicados de texto não completo</span><span class="sxs-lookup"><span data-stu-id="76785-141">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 




