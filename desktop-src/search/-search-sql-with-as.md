---
description: Os aliases de grupo de colunas fornecem uma maneira de usar nomes mais curtos no lugar do nome de uma coluna ou de um grupo de colunas. O predicado de alias de grupo opcional faz parte da cláusula WHERE.
ms.assetid: 7782ac24-ea6c-4a97-b1b6-982f276fcefc
title: Como predicado de alias de grupo--AS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29218e11fbffe5f47128eeefba3a7fe847a5b21d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646866"
---
# <a name="with----as-group-alias-predicate"></a><span data-ttu-id="6c826-104">Como predicado de alias de grupo--AS</span><span class="sxs-lookup"><span data-stu-id="6c826-104">WITH -- AS Group Alias Predicate</span></span>

<span data-ttu-id="6c826-105">Os aliases de grupo de colunas fornecem uma maneira de usar nomes mais curtos no lugar do nome de uma coluna ou de um grupo de colunas.</span><span class="sxs-lookup"><span data-stu-id="6c826-105">Column group aliases provide a way to use shorter names in place of the name of a column or a group of columns.</span></span> <span data-ttu-id="6c826-106">O predicado de alias de grupo opcional faz parte da cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="6c826-106">The optional group alias predicate is part of the WHERE clause.</span></span> <span data-ttu-id="6c826-107">A sintaxe a seguir:</span><span class="sxs-lookup"><span data-stu-id="6c826-107">Its syntax follows:</span></span>


```
...WHERE[ WITH(<columns>) AS #<alias_name>]
[,WITH(<columns>) AS #<alias_name>]
```



<span data-ttu-id="6c826-108">Você pode especificar mais de um alias de grupo, separando o com... COMO predicados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="6c826-108">You can specify more than one group alias, separating the WITH...AS predicates by commas.</span></span>

<span data-ttu-id="6c826-109">Quando um alias de grupo é referenciado em um predicado de cláusula WHERE, a condição é aplicada a cada coluna no grupo.</span><span class="sxs-lookup"><span data-stu-id="6c826-109">When a group alias is referred to in a WHERE clause predicate, the condition is applied to each column in the group.</span></span> <span data-ttu-id="6c826-110">Os valores lógicos resultantes da correspondência de cada coluna são combinados usando o operador **or** lógico.</span><span class="sxs-lookup"><span data-stu-id="6c826-110">The logical values resulting from matching each column are combined by using the logical **OR** operator.</span></span>

<span data-ttu-id="6c826-111">Um alias deve ser definido antes que possa ser usado e pode ser usado somente dentro da cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="6c826-111">An alias must be defined before it can be used, and it can be used only within the WHERE clause.</span></span> <span data-ttu-id="6c826-112">O nome do alias deve ser um identificador regular precedido por um sinal de sustenido necessário ( \# ).</span><span class="sxs-lookup"><span data-stu-id="6c826-112">The alias name must be a regular identifier preceded by a required pound sign (\#).</span></span>

<span data-ttu-id="6c826-113">O especificador de coluna pode conter um ou mais especificadores de coluna, separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="6c826-113">The column specifier can contain one or more column specifiers, separated by commas.</span></span> <span data-ttu-id="6c826-114">A lista de colunas deve ser colocada entre parênteses e o peso pode ser atribuído a cada uma delas.</span><span class="sxs-lookup"><span data-stu-id="6c826-114">The list of columns must be enclosed in parentheses and weighting can be assigned to each.</span></span> <span data-ttu-id="6c826-115">Cada coluna tem a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="6c826-115">Each column has the following syntax:</span></span>


```
<column_identifier> [<weight_assignment>]
```



<span data-ttu-id="6c826-116">Para obter informações sobre como especificar pesos de coluna, consulte [predicado FREETEXT](-search-sql-freetext.md) e [contém predicado](-search-sql-contains.md).</span><span class="sxs-lookup"><span data-stu-id="6c826-116">For information on specifying column weights, see [FREETEXT Predicate](-search-sql-freetext.md) and [CONTAINS Predicate](-search-sql-contains.md).</span></span>

<span data-ttu-id="6c826-117">O identificador de coluna pode ser regular ou delimitado.</span><span class="sxs-lookup"><span data-stu-id="6c826-117">The column identifier can be regular or delimited.</span></span>

## <a name="examples"></a><span data-ttu-id="6c826-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6c826-118">Examples</span></span>

<span data-ttu-id="6c826-119">Os exemplos de cláusula WHERE a seguir demonstram quando e como você pode usar o predicado de alias de grupo.</span><span class="sxs-lookup"><span data-stu-id="6c826-119">The following WHERE clause examples demonstrate when and how you can use the group alias predicate.</span></span> <span data-ttu-id="6c826-120">O primeiro exemplo mostra uma cláusula WHERE mais repetitiva que não usa a alias de grupo.</span><span class="sxs-lookup"><span data-stu-id="6c826-120">The first example shows a more repetitive WHERE clause that does not use group aliasing.</span></span>


```
...WHERE
    FREETEXT("System.ItemNameDisplay",'"computer software"')
    OR
    FREETEXT("System.Title",'"computer software"')
    OR 
    FREETEXT("System.Keywords",'"computer software"')
```



<span data-ttu-id="6c826-121">O exemplo anterior pode ser simplificado usando um alias de grupo, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="6c826-121">The preceding example can be simplified by using a group alias, as shown in the following example.</span></span>


```
...WHERE
    WITH("System.ItemNameDisplay","System.Title","System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



<span data-ttu-id="6c826-122">Veja a seguir um exemplo de peso positivo em que a propriedade **title** recebe mais peso na determinação da classificação relativa.</span><span class="sxs-lookup"><span data-stu-id="6c826-122">The following is an example of positive weighting where the **Title** property is given more weight in determining the relative rank.</span></span>


```
...WHERE
    WITH("System.Title":0.8,*:0.5,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



<span data-ttu-id="6c826-123">Veja a seguir um exemplo de peso negativo em que a propriedade **title** com peso de 0 não é considerada.</span><span class="sxs-lookup"><span data-stu-id="6c826-123">The following is an example of negative weighting where the **Title** property with weight of 0 is not considered.</span></span>


```
...WHERE
    WITH("System.Title":0,*:1.0,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



## <a name="related-topics"></a><span data-ttu-id="6c826-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6c826-124">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6c826-125">**Referência**</span><span class="sxs-lookup"><span data-stu-id="6c826-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6c826-126">Predicado FREETEXT</span><span class="sxs-lookup"><span data-stu-id="6c826-126">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

<span data-ttu-id="6c826-127">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="6c826-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6c826-128">Predicados de texto completo</span><span class="sxs-lookup"><span data-stu-id="6c826-128">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="6c826-129">Predicados de texto não completo</span><span class="sxs-lookup"><span data-stu-id="6c826-129">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



