---
description: Uma função de agregação executa um cálculo em um conjunto de valores e retorna um valor. Isso torna possível gerar estatísticas de resumo para grupos de vários níveis com pouca sobrecarga.
ms.assetid: 82a93f57-8273-45bf-81d7-50a673845ae1
title: Funções de Agregação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da68ad1104c93e8ae04f7ec37cbbde5020109336
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555294"
---
# <a name="aggregate-functions"></a><span data-ttu-id="7daa8-104">Funções de Agregação</span><span class="sxs-lookup"><span data-stu-id="7daa8-104">Aggregate Functions</span></span>

<span data-ttu-id="7daa8-105">Uma função de agregação executa um cálculo em um conjunto de valores e retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7daa8-105">An aggregate function performs a calculation on a set of values and returns a value.</span></span> <span data-ttu-id="7daa8-106">Isso torna possível gerar estatísticas de resumo para grupos de vários níveis com pouca sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="7daa8-106">Doing so makes it possible to generate summary statistics for multi-level groups with little overhead.</span></span>

## <a name="about-aggregate-functions"></a><span data-ttu-id="7daa8-107">Sobre funções de agregação</span><span class="sxs-lookup"><span data-stu-id="7daa8-107">About Aggregate Functions</span></span>

<span data-ttu-id="7daa8-108">As funções de agregação no Windows Search linguagem SQL (SQL) têm a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="7daa8-108">Aggregate functions in Windows Search Structured Query Language (SQL) have the following syntax:</span></span>


```
AGGREGATE <function> [AS <label>] [,<function> [AS <label>]]*
```



<span data-ttu-id="7daa8-109">A parte da função pode incluir qualquer uma das seguintes funções e sintaxe:</span><span class="sxs-lookup"><span data-stu-id="7daa8-109">The function portion can include any of the following functions and syntax:</span></span>



| <span data-ttu-id="7daa8-110">Função</span><span class="sxs-lookup"><span data-stu-id="7daa8-110">Function</span></span>                                                              | <span data-ttu-id="7daa8-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="7daa8-111">Description</span></span>                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7daa8-112">Méd ( <column> )</span><span class="sxs-lookup"><span data-stu-id="7daa8-112">AVG(<column>)</span></span>                                                   | <span data-ttu-id="7daa8-113">Retorna a média dos valores em um grupo.</span><span class="sxs-lookup"><span data-stu-id="7daa8-113">Returns the average of the values in a group.</span></span> <span data-ttu-id="7daa8-114">Aplica-se somente a números.</span><span class="sxs-lookup"><span data-stu-id="7daa8-114">Applies only to numbers.</span></span>                                                                                                                                      |
| <span data-ttu-id="7daa8-115">BYFREQUENCY ( <column> , <N> )</span><span class="sxs-lookup"><span data-stu-id="7daa8-115">BYFREQUENCY(<column>, <N>)</span></span>                                | <span data-ttu-id="7daa8-116">Retorna os valores de N colunas mais frequentes dos resultados no grupo.</span><span class="sxs-lookup"><span data-stu-id="7daa8-116">Returns the most frequent N column values from the results in the group.</span></span> <span data-ttu-id="7daa8-117">Também inclui uma contagem de quantas vezes cada valor ocorreu e os identificadores de documento para resultados que contêm cada valor retornado.</span><span class="sxs-lookup"><span data-stu-id="7daa8-117">Also includes a count of how many times each value occurred and document identifiers for results that contain each returned value.</span></span> |
| <span data-ttu-id="7daa8-118">CHILDCOUNT ()</span><span class="sxs-lookup"><span data-stu-id="7daa8-118">CHILDCOUNT()</span></span>                                                          | <span data-ttu-id="7daa8-119">Retorna o número de itens em um grupo (excluindo subgrupos).</span><span class="sxs-lookup"><span data-stu-id="7daa8-119">Returns the number of items in a group (excluding subgroups).</span></span> <span data-ttu-id="7daa8-120">Se houver vários níveis de agrupamento, isso retornará o número de grupos filho imediatos.</span><span class="sxs-lookup"><span data-stu-id="7daa8-120">If there are multiple levels of grouping, this returns the number of immediate child groups.</span></span>                                                  |
| <span data-ttu-id="7daa8-121">CONTAGEM ()</span><span class="sxs-lookup"><span data-stu-id="7daa8-121">COUNT()</span></span>                                                               | <span data-ttu-id="7daa8-122">Retorna o número de itens em um grupo e todos os subgrupos.</span><span class="sxs-lookup"><span data-stu-id="7daa8-122">Returns the number of items in a group and all subgroups.</span></span>                                                                                                                                                   |
| <span data-ttu-id="7daa8-123">DATERANGE ( <column> )</span><span class="sxs-lookup"><span data-stu-id="7daa8-123">DATERANGE(<column>)</span></span>                                             | <span data-ttu-id="7daa8-124">Retorna os limites inferior e superior dos valores de coluna encontrados no grupo de resultados de grupo.</span><span class="sxs-lookup"><span data-stu-id="7daa8-124">Returns the lower and upper bounds of the column values found in the group results group.</span></span> <span data-ttu-id="7daa8-125">Válido somente para propriedades FILETIME.</span><span class="sxs-lookup"><span data-stu-id="7daa8-125">Valid only for filetime properties.</span></span>                                                                               |
| <span data-ttu-id="7daa8-126">PRIMEIRO ( <column> , <N> )</span><span class="sxs-lookup"><span data-stu-id="7daa8-126">FIRST(<column>, <N>)</span></span>                                      | <span data-ttu-id="7daa8-127">Retorna os primeiros N valores de coluna dos resultados folha encontrados em um grupo.</span><span class="sxs-lookup"><span data-stu-id="7daa8-127">Returns the first N column values from leaf results found in a group.</span></span>                                                                                                                                       |
| <span data-ttu-id="7daa8-128">MÁX. ( <column> )</span><span class="sxs-lookup"><span data-stu-id="7daa8-128">MAX(<column>)</span></span>                                                   | <span data-ttu-id="7daa8-129">Retorna o valor máximo na expressão.</span><span class="sxs-lookup"><span data-stu-id="7daa8-129">Returns the maximum value in the expression.</span></span> <span data-ttu-id="7daa8-130">Aplica-se somente a números ou datas.</span><span class="sxs-lookup"><span data-stu-id="7daa8-130">Applies only to numbers or dates.</span></span>                                                                                                                              |
| <span data-ttu-id="7daa8-131">MIN ( <column> )</span><span class="sxs-lookup"><span data-stu-id="7daa8-131">MIN(<column>)</span></span>                                                   | <span data-ttu-id="7daa8-132">Retorna o valor mínimo na expressão.</span><span class="sxs-lookup"><span data-stu-id="7daa8-132">Returns the minimum value in the expression.</span></span> <span data-ttu-id="7daa8-133">Aplica-se somente a números ou datas.</span><span class="sxs-lookup"><span data-stu-id="7daa8-133">Applies only to numbers or dates.</span></span>                                                                                                                              |
| <span data-ttu-id="7daa8-134">REPRESENTATIVEOF ( <column> , <idRepresentative> , <N> )</span><span class="sxs-lookup"><span data-stu-id="7daa8-134">REPRESENTATIVEOF(<column>, <idRepresentative>, <N>)</span></span> | <span data-ttu-id="7daa8-135">Retorna N valores idRepresentative, cada um deles selecionado de um dos subconjuntos de resultados que tem um valor de coluna exclusivo.</span><span class="sxs-lookup"><span data-stu-id="7daa8-135">Returns N idRepresentative values, each selected from one of the result subsets that has a unique column value.</span></span> <span data-ttu-id="7daa8-136">Cada valor também é retornado com um identificador de documento que tem o valor idRepresentative.</span><span class="sxs-lookup"><span data-stu-id="7daa8-136">Each value is also returned with a document identifier that has the idRepresentative value.</span></span> |
| <span data-ttu-id="7daa8-137">SUM ( <column> )</span><span class="sxs-lookup"><span data-stu-id="7daa8-137">SUM(<column>)</span></span>                                                   | <span data-ttu-id="7daa8-138">Retorna a soma dos valores em um grupo.</span><span class="sxs-lookup"><span data-stu-id="7daa8-138">Returns the sum of the values in a group.</span></span> <span data-ttu-id="7daa8-139">Aplica-se somente a números.</span><span class="sxs-lookup"><span data-stu-id="7daa8-139">Applies only to numbers.</span></span>                                                                                                                                          |



 

 

> [!Note]  
> <span data-ttu-id="7daa8-140">As agregações são retornadas como colunas individuais.</span><span class="sxs-lookup"><span data-stu-id="7daa8-140">Aggregates are returned as individual columns.</span></span> <span data-ttu-id="7daa8-141">Eles são, na maioria das vezes, tipos simples, exceto ByFrequency, First, DateRange e RepresentativeOf, que são retornados como tipos compostos.</span><span class="sxs-lookup"><span data-stu-id="7daa8-141">They are mostly simple types except for ByFrequency, First, DateRange, and RepresentativeOf which are returned as compound types.</span></span>

 

<span data-ttu-id="7daa8-142">Você pode usar qualquer coluna numérica ou de data para agregações, e não apenas aquelas que estão na cláusula SELECT.</span><span class="sxs-lookup"><span data-stu-id="7daa8-142">You can use any numeric or date column for aggregations, and not only those that are in the SELECT clause.</span></span> <span data-ttu-id="7daa8-143">No entanto, você não pode agrupar em agregações.</span><span class="sxs-lookup"><span data-stu-id="7daa8-143">However, you cannot group on aggregates.</span></span> <span data-ttu-id="7daa8-144">Um erro de sintaxe será retornado se o argumento de coluna passado não for um tipo numérico ou de data.</span><span class="sxs-lookup"><span data-stu-id="7daa8-144">A syntax error is returned if the column argument passed in is not either a numeric or date type.</span></span>

<span data-ttu-id="7daa8-145">A parte do rótulo é opcional e fornece um alias mais legível para o rótulo.</span><span class="sxs-lookup"><span data-stu-id="7daa8-145">The label portion is optional and provides a more readable alias for the label.</span></span> <span data-ttu-id="7daa8-146">Se você não incluir um rótulo de alias, o Windows Search transformará a função e o nome da coluna em um rótulo.</span><span class="sxs-lookup"><span data-stu-id="7daa8-146">If you do not include an alias label, then Windows Search transforms the function and column name into a label.</span></span> <span data-ttu-id="7daa8-147">Por exemplo, MAX (System.Document. WordCount) torna-se MAX \_ SystemDocumentWordCount.</span><span class="sxs-lookup"><span data-stu-id="7daa8-147">For example, MAX(System.Document.WordCount) becomes MAX\_SystemDocumentWordCount.</span></span>

## <a name="multi-level-groups-and-counting"></a><span data-ttu-id="7daa8-148">Grupos e contagens de vários níveis</span><span class="sxs-lookup"><span data-stu-id="7daa8-148">Multi-level Groups and Counting</span></span>

<span data-ttu-id="7daa8-149">As agregações são definidas em folhas e duplicadas.</span><span class="sxs-lookup"><span data-stu-id="7daa8-149">Aggregates are defined over leaves and are duplicated.</span></span> <span data-ttu-id="7daa8-150">Uma agregação usa como entrada as folhas do grupo que as define (documentos), em vez dos subgrupos de seus filhos.</span><span class="sxs-lookup"><span data-stu-id="7daa8-150">An aggregate takes as input the leaves of the group that defines it (documents), rather than the subgroups of its children.</span></span> <span data-ttu-id="7daa8-151">Essa funcionalidade é conhecida como agrupamento de vários níveis.</span><span class="sxs-lookup"><span data-stu-id="7daa8-151">This functionality is referred to as multi-level grouping.</span></span>

<span data-ttu-id="7daa8-152">Além de agregações sendo definidas em todas as folhas e duplicadas, elas são contadas apenas uma vez.</span><span class="sxs-lookup"><span data-stu-id="7daa8-152">In addition to aggregates being defined over leaves and duplicated, they are counted only once.</span></span> <span data-ttu-id="7daa8-153">Embora o mesmo documento possa ser representado várias vezes em um grupo, as agregações só o consideram uma vez.</span><span class="sxs-lookup"><span data-stu-id="7daa8-153">While the same document might be represented multiple times under one group, aggregates would only consider it once.</span></span> <span data-ttu-id="7daa8-154">O gráfico a seguir ilustra esse conceito.</span><span class="sxs-lookup"><span data-stu-id="7daa8-154">The following graphic illustrates this concept.</span></span>

![diagrama mostrando que as agregações são definidas em folhas e duplicadas, e são contadas apenas uma vez](images/aggregates.png)

## <a name="aggregate-examples"></a><span data-ttu-id="7daa8-156">Exemplos de agregação</span><span class="sxs-lookup"><span data-stu-id="7daa8-156">Aggregate Examples</span></span>

<span data-ttu-id="7daa8-157">Veja a seguir exemplos de funções de agregação dentro da cláusula GROUP ON:</span><span class="sxs-lookup"><span data-stu-id="7daa8-157">The following are examples of aggregate functions within the GROUP ON clause:</span></span>


```
GROUP ON System.Sender ['d','m','r'] 
    AGGREGATE COUNT() as 'Total',
              MAX(System.Size) as 'Max Size',
              MIN(System.Size) as 'Min Size'
    OVER (SELECT System.Subject FROM systemindex)
              
GROUP ON System.Sender ['d', 'm', 'r']
      AGGREGATE MAX(System.Search.Rank) as 'MaxRank', 
                MIN(System.Search.Rank) as 'MinRank'
      OVER (GROUP ON system.conversationID
                  OVER (SELECT workid, System.ItemUrl FROM systemindex
                        WHERE CONTAINS (*, 'sometext')
                        ORDER BY System.DateCreated))
               
GROUP ON System.FileName [before('a'),before('z')] 
      AGGREGATE MAX(System.Size) as 'maxsize', MIN(System.Size) as 'MinSize' 
      OVER (SELECT System.FileName FROM systemindex
            ORDER BY System.FileName)      
            
GROUP ON System.author 
      AGGREGATE MAX(System.size) as 'maxsize' 
      ORDER BY min(System.Size) 
      OVER (GROUP ON System.DateCreated 
                  AGGREGATE Count() 
                  ORDER BY MAX(System.size) 
                  OVER (SELECT filename, System.DateCreated, System.Size FROM systemindex
                        WHERE CONTAINS('text')))
```



## <a name="return-value"></a><span data-ttu-id="7daa8-158">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="7daa8-158">Return Value</span></span>

<span data-ttu-id="7daa8-159">O valor de retorno é uma variante encontrada no conjunto de linhas como uma propriedade personalizada, seja como os aliases especificados ou como "agregações" se nenhum rótulo de alias for especificado.</span><span class="sxs-lookup"><span data-stu-id="7daa8-159">The return value is a variant found on the rowset as a custom property, either as the specified aliases or as "Aggregates" if no alias label is specified.</span></span>

 

 



