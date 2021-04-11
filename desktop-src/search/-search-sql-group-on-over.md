---
description: O grupo em...
ms.assetid: 37f027c1-c2af-4d62-8b5f-918499fc2d7c
title: AGRUPAR EM... SOBRE... Privacidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d7087305f0a5a86f0288ed92ec4bda5b8c882c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090067"
---
# <a name="group-on--over--statement"></a><span data-ttu-id="d64d9-103">AGRUPAR EM... SOBRE... Privacidade</span><span class="sxs-lookup"><span data-stu-id="d64d9-103">GROUP ON ... OVER ... Statement</span></span>

<span data-ttu-id="d64d9-104">O grupo em... SOBRE... a instrução retorna um conjunto de linhas hierárquico no qual os resultados da pesquisa são divididos em grupos com base em uma coluna especificada e intervalos de agrupamento opcionais.</span><span class="sxs-lookup"><span data-stu-id="d64d9-104">The GROUP ON... OVER... statement returns a hierarchical rowset in which search results are divided into groups based on a specified column and optional grouping ranges.</span></span> <span data-ttu-id="d64d9-105">Se você agrupar na coluna [System. Kind](../properties/props-system-kind.md) , o conjunto de resultados será dividido em vários grupos: um para documentos, um para comunicações e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d64d9-105">If you group on the [System.Kind](../properties/props-system-kind.md) column, the result set is divided into multiple groups: one for documents, one for communications, and so on.</span></span> <span data-ttu-id="d64d9-106">Se você agrupar em [System. Size](../properties/props-system-size.md) e no intervalo de grupo 100 KB, o conjunto de resultados será dividido em três grupos: itens de tamanho < 100 KB, itens de tamanho >= 100 KB e itens sem valor de tamanho.</span><span class="sxs-lookup"><span data-stu-id="d64d9-106">If you group on [System.Size](../properties/props-system-size.md) and group range 100 KB, the result set is divided into three groups: items of size < 100 KB, items of size >= 100 KB, and items with no size value.</span></span> <span data-ttu-id="d64d9-107">Você também pode agregar agrupamentos com funções.</span><span class="sxs-lookup"><span data-stu-id="d64d9-107">You can also aggregate groupings with functions.</span></span>

<span data-ttu-id="d64d9-108">Este tópico aborda os seguintes assuntos:</span><span class="sxs-lookup"><span data-stu-id="d64d9-108">This topic covers the following subjects:</span></span>

-   [<span data-ttu-id="d64d9-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d64d9-109">Syntax</span></span>](#syntax)
-   [<span data-ttu-id="d64d9-110">Intervalos de grupo</span><span class="sxs-lookup"><span data-stu-id="d64d9-110">Group Ranges</span></span>](#group-ranges)
-   [<span data-ttu-id="d64d9-111">Rotulando grupos</span><span class="sxs-lookup"><span data-stu-id="d64d9-111">Labeling Groups</span></span>](#labeling-groups)
-   [<span data-ttu-id="d64d9-112">Grupos de pedidos</span><span class="sxs-lookup"><span data-stu-id="d64d9-112">Ordering Groups</span></span>](#ordering-groups)
-   [<span data-ttu-id="d64d9-113">Aninhando grupos</span><span class="sxs-lookup"><span data-stu-id="d64d9-113">Nesting Groups</span></span>](#nesting-groups)
-   [<span data-ttu-id="d64d9-114">Agrupamento em Propriedades de vetor</span><span class="sxs-lookup"><span data-stu-id="d64d9-114">Grouping on Vector Properties</span></span>](#grouping-on-vector-properties)
-   [<span data-ttu-id="d64d9-115">Mais exemplos</span><span class="sxs-lookup"><span data-stu-id="d64d9-115">More Examples</span></span>](#more-examples)
-   [<span data-ttu-id="d64d9-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d64d9-116">Related topics</span></span>](#related-topics)

## <a name="syntax"></a><span data-ttu-id="d64d9-117">Syntax</span><span class="sxs-lookup"><span data-stu-id="d64d9-117">Syntax</span></span>

<span data-ttu-id="d64d9-118">O grupo em... SOBRE... a instrução tem a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="d64d9-118">The GROUP ON ... OVER ... statement has the following syntax:</span></span>


```
GROUP ON <column> ['['<group ranges>']']] 
[AGGREGATE <aggregate_function>] 
[ORDER BY <column> [<direction>]] | [ORDER IN GROUP '<group name>' BY <column> [<direction>]]
    OVER (GROUP ON... | SELECT... ] )
```



<span data-ttu-id="d64d9-119">onde os intervalos de agrupamento são definidos da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d64d9-119">where grouping ranges are defined as follows:</span></span>


```
<group ranges> := <range limit> [/'<label>'] | <range limit> [/'<label>'], <group ranges>
<range limit> := (<number> | <date> | '<string>' | BEFORE('<string>') | AFTER('<string>')) 
```



<span data-ttu-id="d64d9-120">O grupo em <column> pode ser um [identificador](-search-sql-identifiers.md) regular ou delimitado para uma propriedade no repositório de propriedades.</span><span class="sxs-lookup"><span data-stu-id="d64d9-120">The GROUP ON <column> can be a regular or delimited [identifier](-search-sql-identifiers.md) for a property in the property store.</span></span>

<span data-ttu-id="d64d9-121">O opcional <group ranges> é uma lista de um ou mais valores (número, data ou cadeia de caracteres) usados para dividir os resultados em grupos.</span><span class="sxs-lookup"><span data-stu-id="d64d9-121">The optional <group ranges> is a list of one or more values (number, date, or string) used for dividing the results into groups.</span></span> <span data-ttu-id="d64d9-122">O <range limit> identifica um ponto de divisão no conjunto de resultados retornado e <label> identifica um rótulo amigável para um grupo.</span><span class="sxs-lookup"><span data-stu-id="d64d9-122">The <range limit> identifies a division point in the returned result set, and the <label> identifies a user-friendly label for a group.</span></span> <span data-ttu-id="d64d9-123">Você pode dividir o conjunto de resultados em quantos grupos forem necessários.</span><span class="sxs-lookup"><span data-stu-id="d64d9-123">You can divide the result set into as many groups as you need.</span></span>

<span data-ttu-id="d64d9-124">O primeiro grupo de resultados inclui itens com o valor mínimo possível para a propriedade especificada até, mas não incluindo o primeiro limite de intervalo.</span><span class="sxs-lookup"><span data-stu-id="d64d9-124">The first group of results includes items with the minimum possible value for the specified property up to but not including the first range limit.</span></span> <span data-ttu-id="d64d9-125">Esse grupo pode ser referenciado com a palavra-chave MINVALUE.</span><span class="sxs-lookup"><span data-stu-id="d64d9-125">This group can be referred to with the MINVALUE keyword.</span></span> <span data-ttu-id="d64d9-126">O segundo grupo pode ser referenciado com o especificador de limite de intervalo em si e inclui itens cujo valor da propriedade especificada é igual ou maior que o limite de intervalo.</span><span class="sxs-lookup"><span data-stu-id="d64d9-126">The second group can be referred to with the range limit specifier itself and includes items whose value for the specified property is equal to or greater than the range limit.</span></span> <span data-ttu-id="d64d9-127">Todos os itens que não têm um valor para a propriedade especificada são retornados por último e podem ser referenciados com a palavra-chave **NULL** .</span><span class="sxs-lookup"><span data-stu-id="d64d9-127">Any items that do not have a value for the specified property are returned last and can be referred to with the **NULL** keyword.</span></span>

<span data-ttu-id="d64d9-128">Por exemplo, um limite de intervalo de ' 2006-01-01 ' para a propriedade [System. DateCreated](../properties/props-system-datecreated.md) divide o conjunto de resultados em itens com datas anteriores a 2006-01-01 (grupo MinValue), itens com datas em ou após 2006-01-01 (grupo 2006-01-01) e itens sem data (grupo **nulo** ).</span><span class="sxs-lookup"><span data-stu-id="d64d9-128">For example, a range limit of '2006-01-01' for the [System.DateCreated](../properties/props-system-datecreated.md) property divides the result set into items with dates before 2006-01-01 (MINVALUE group), items with dates on or after 2006-01-01 (2006-01-01 group), and items with no date (**NULL** group).</span></span>

<span data-ttu-id="d64d9-129">Dentro de cada grupo, os resultados são classificados pelos valores no grupo na coluna por padrão.</span><span class="sxs-lookup"><span data-stu-id="d64d9-129">Within each group, the results are sorted by the values in the GROUP ON column by default.</span></span> <span data-ttu-id="d64d9-130">A cláusula [order by](-search-sql-orderby.md) opcional pode conter um especificador de direção de ASC para crescente (baixo para alto) ou DESC para decrescente (alta para baixa) e a [ordem na cláusula Group by](-search-sql-orderingroup.md) pode ordenar cada grupo usando regras diferentes.</span><span class="sxs-lookup"><span data-stu-id="d64d9-130">The optional [ORDER BY](-search-sql-orderby.md) clause can contain a direction specifier of either ASC for ascending (low to high) or DESC for descending (high to low), and the [ORDER IN GROUP BY](-search-sql-orderingroup.md) clause can order each group using different rules.</span></span> <span data-ttu-id="d64d9-131">Consulte a seção [grupos de pedidos](#ordering-groups) abaixo para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d64d9-131">See the [Ordering Groups](#ordering-groups) section below for more information.</span></span>

## <a name="group-ranges"></a><span data-ttu-id="d64d9-132">Intervalos de grupo</span><span class="sxs-lookup"><span data-stu-id="d64d9-132">Group Ranges</span></span>

<span data-ttu-id="d64d9-133">A tabela a seguir demonstra como os resultados são divididos em grupos com base nos limites de intervalo:</span><span class="sxs-lookup"><span data-stu-id="d64d9-133">The following table demonstrates how results are divided into groups based the range limits:</span></span>



| <span data-ttu-id="d64d9-134">Exemplo ( <column> \[ intervalos de grupo \] )</span><span class="sxs-lookup"><span data-stu-id="d64d9-134">Example (<column> \[group ranges\])</span></span>        | <span data-ttu-id="d64d9-135">Resultado</span><span class="sxs-lookup"><span data-stu-id="d64d9-135">Result</span></span>                                                                                                                                                                                                                                                                         |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d64d9-136">Sistema. tamanho \[ 1000, 5000\]</span><span class="sxs-lookup"><span data-stu-id="d64d9-136">System.Size \[1000, 5000\]</span></span>                       | <span data-ttu-id="d64d9-137">Os resultados são agrupados em quatro buckets: **MinValue**: tamanho < 1000</span><span class="sxs-lookup"><span data-stu-id="d64d9-137">Results are grouped into four buckets: **MINVALUE**: Size < 1000</span></span><br/> <span data-ttu-id="d64d9-138">**1000:** 1000 <= tamanho < 5000</span><span class="sxs-lookup"><span data-stu-id="d64d9-138">**1000:** 1000 <= Size < 5000</span></span><br/> <span data-ttu-id="d64d9-139">**5000:** Tamanho >= 5000</span><span class="sxs-lookup"><span data-stu-id="d64d9-139">**5000:** Size >= 5000</span></span><br/> <span data-ttu-id="d64d9-140">**Nulo:** Nenhum valor para o tamanho</span><span class="sxs-lookup"><span data-stu-id="d64d9-140">**NULL:** No value for Size</span></span><br/>                                                                      |
| <span data-ttu-id="d64d9-141">System. Author \[ antes (' M'), After (' r ')\]</span><span class="sxs-lookup"><span data-stu-id="d64d9-141">System.Author \[BEFORE('m'),AFTER('r')\]</span></span>         | <span data-ttu-id="d64d9-142">Os resultados são agrupados em quatro buckets: **MinValue:** autor < caractere antes de "m"</span><span class="sxs-lookup"><span data-stu-id="d64d9-142">Results are grouped into four buckets: **MINVALUE:** Author < character before "m"</span></span><br/> <span data-ttu-id="d64d9-143">**m:** caractere antes de "m" <= autor < caractere após "r"</span><span class="sxs-lookup"><span data-stu-id="d64d9-143">**m:** character before "m" <= Author < character after "r"</span></span><br/> <span data-ttu-id="d64d9-144">**r:** caractere após "r" <= autor</span><span class="sxs-lookup"><span data-stu-id="d64d9-144">**r:** character after "r" <= Author</span></span><br/> <span data-ttu-id="d64d9-145">**Nulo:** Nenhum valor para o autor</span><span class="sxs-lookup"><span data-stu-id="d64d9-145">**NULL:** No value for Author</span></span><br/>      |
| <span data-ttu-id="d64d9-146">System. Author \[ MinValue/' a para l ', "m"/m para z '\]</span><span class="sxs-lookup"><span data-stu-id="d64d9-146">System.Author \[MINVALUE/'a to l',"m"/'m to z'\]</span></span> | <span data-ttu-id="d64d9-147">Os resultados são agrupados em três buckets: a **a l:** autor < "m"</span><span class="sxs-lookup"><span data-stu-id="d64d9-147">Results are grouped into three buckets: **a to l:** Author < "m"</span></span><br/> <span data-ttu-id="d64d9-148">**m a z:** "m" <= autor</span><span class="sxs-lookup"><span data-stu-id="d64d9-148">**m to z:** "m" <= Author</span></span> <br/> <span data-ttu-id="d64d9-149">**Nulo:** Nenhum valor para o autor</span><span class="sxs-lookup"><span data-stu-id="d64d9-149">**NULL:** No value for Author</span></span><br/>                                                                                                               |
| <span data-ttu-id="d64d9-150">System. DateCreated \[ ' 2005-1-01 ', ' 2006-6-01 '\]</span><span class="sxs-lookup"><span data-stu-id="d64d9-150">System.DateCreated \['2005-1-01','2006-6-01'\]</span></span>   | <span data-ttu-id="d64d9-151">Os resultados são agrupados em quatro buckets:</span><span class="sxs-lookup"><span data-stu-id="d64d9-151">Results are grouped into four buckets:</span></span><br/> <span data-ttu-id="d64d9-152">**MinValue:** DateCreated < 2005-1-01</span><span class="sxs-lookup"><span data-stu-id="d64d9-152">**MINVALUE:** DateCreated < 2005-1-01</span></span><br/> <span data-ttu-id="d64d9-153">**2005-1-01:** 2005-1-01 <= DateCreated < 2006-6-01</span><span class="sxs-lookup"><span data-stu-id="d64d9-153">**2005-1-01:** 2005-1-01 <= DateCreated < 2006-6-01</span></span><br/> <span data-ttu-id="d64d9-154">**2006-1-01:** DateCreated >= 2006-6-01</span><span class="sxs-lookup"><span data-stu-id="d64d9-154">**2006-1-01:** DateCreated >= 2006-6-01</span></span><br/> <span data-ttu-id="d64d9-155">**Nulo:** Nenhum valor para DateCreated</span><span class="sxs-lookup"><span data-stu-id="d64d9-155">**NULL:** No value for DateCreated</span></span><br/> |



 

 

> [!IMPORTANT]
>
> <span data-ttu-id="d64d9-156">Incorreto `GROUP ON System.Author['m','z','a']`</span><span class="sxs-lookup"><span data-stu-id="d64d9-156">Incorrect: `GROUP ON System.Author['m','z','a']`</span></span>
>
> <span data-ttu-id="d64d9-157">Corrigi `GROUP ON System.Author['a','m','z']`</span><span class="sxs-lookup"><span data-stu-id="d64d9-157">Correct: `GROUP ON System.Author['a','m','z']`</span></span>

 

 

## <a name="labeling-groups"></a><span data-ttu-id="d64d9-158">Rotulando grupos</span><span class="sxs-lookup"><span data-stu-id="d64d9-158">Labeling Groups</span></span>

<span data-ttu-id="d64d9-159">Para melhorar a legibilidade, você pode rotular grupos usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="d64d9-159">To improve readability, you can label groups using the following syntax:</span></span>


```
GROUP ON <column> [<range limit>/'<label>',<range limit>/'<label>']
```



<span data-ttu-id="d64d9-160">O rótulo é separado do limite de intervalo com uma barra e é colocado entre aspas simples.</span><span class="sxs-lookup"><span data-stu-id="d64d9-160">The label is separated from the range limit with a slash mark and is enclosed in single quotation marks.</span></span> <span data-ttu-id="d64d9-161">Se você não especificar um rótulo, o nome do grupo será a cadeia de caracteres de limite de intervalo.</span><span class="sxs-lookup"><span data-stu-id="d64d9-161">If you do not specify a label, the group name is the range limit string.</span></span>

<span data-ttu-id="d64d9-162">Veja a seguir um exemplo de como rotular grupos:</span><span class="sxs-lookup"><span data-stu-id="d64d9-162">The following is an example of labeling groups:</span></span>


```
GROUP ON System.Size [(MINVALUE/'Small','100')/'Medium','50000'/'Large']
    OVER (SELECT System.Size FROM SystemIndex)
```



<span data-ttu-id="d64d9-163">No Windows 7 ou posterior, você também pode usar um \[ outro \] rótulo genérico para combinar vários intervalos de agrupamento.</span><span class="sxs-lookup"><span data-stu-id="d64d9-163">In Windows 7 or later, you can also use a generic \[OTHER\] label to combine multiple grouping ranges.</span></span> <span data-ttu-id="d64d9-164">Os resultados de todos os grupos identificados com esse rótulo serão combinados em um grupo com este rótulo.</span><span class="sxs-lookup"><span data-stu-id="d64d9-164">Results from all groups identified with this label will be combined into one group with this label.</span></span> <span data-ttu-id="d64d9-165">Esse grupo de resultados é retornado após todos os outros grupos, exceto para o grupo **nulo** .</span><span class="sxs-lookup"><span data-stu-id="d64d9-165">This group of results is returned after all other groups except for the **NULL** group.</span></span> <span data-ttu-id="d64d9-166">O grupo **nulo** contém resultados para itens que não têm um valor para a propriedade especificada.</span><span class="sxs-lookup"><span data-stu-id="d64d9-166">The **NULL** group contains results for items that do not have a value for the specified property.</span></span> <span data-ttu-id="d64d9-167">Antes do Windows 7, o \[ outro \] rótulo é tratado como qualquer outro rótulo de grupo.</span><span class="sxs-lookup"><span data-stu-id="d64d9-167">Prior to Windows 7 the \[OTHER\] label is treated like any other group label.</span></span>

<span data-ttu-id="d64d9-168">O código a seguir é um exemplo de como usar o \[ outro \] rótulo para grupos que seriam criados no Windows 7 ou posterior:</span><span class="sxs-lookup"><span data-stu-id="d64d9-168">The following code is an example of using the \[OTHER\] label for groups that would be created in Windows 7 or later:</span></span>


```
GROUP ON System.Author ['0', 'A'/'[OTHER]', 'I', 'Q', 'W'/'[OTHER]', 'Y']
    OVER (SELECT System.DateCreated FROM SystemIndex)
```



<span data-ttu-id="d64d9-169">A tabela a seguir mostra os grupos que seriam criados pelo código de Agrupamento anterior no Windows 7 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="d64d9-169">The following table shows the groups that would be created by the preceding grouping code in Windows 7 or later.</span></span>



| <span data-ttu-id="d64d9-170">Grupo</span><span class="sxs-lookup"><span data-stu-id="d64d9-170">Group</span></span>     | <span data-ttu-id="d64d9-171">System.Author</span><span class="sxs-lookup"><span data-stu-id="d64d9-171">System.Author</span></span> | <span data-ttu-id="d64d9-172">System. FileName</span><span class="sxs-lookup"><span data-stu-id="d64d9-172">System.FileName</span></span> |
|-----------|---------------|-----------------|
| <span data-ttu-id="d64d9-173">0</span><span class="sxs-lookup"><span data-stu-id="d64d9-173">0</span></span>         | <span data-ttu-id="d64d9-174">1Bill</span><span class="sxs-lookup"><span data-stu-id="d64d9-174">1Bill</span></span>         | <span data-ttu-id="d64d9-175">Lorem.docx</span><span class="sxs-lookup"><span data-stu-id="d64d9-175">Lorem.docx</span></span>      |
| <span data-ttu-id="d64d9-176">Q</span><span class="sxs-lookup"><span data-stu-id="d64d9-176">Q</span></span>         | <span data-ttu-id="d64d9-177">Dama</span><span class="sxs-lookup"><span data-stu-id="d64d9-177">Queen</span></span>         | <span data-ttu-id="d64d9-178">Ipsum.docx</span><span class="sxs-lookup"><span data-stu-id="d64d9-178">Ipsum.docx</span></span>      |
|           | <span data-ttu-id="d64d9-179">Robin</span><span class="sxs-lookup"><span data-stu-id="d64d9-179">Robin</span></span>         | <span data-ttu-id="d64d9-180">dolor.docx</span><span class="sxs-lookup"><span data-stu-id="d64d9-180">dolor.docx</span></span>      |
| <span data-ttu-id="d64d9-181">S</span><span class="sxs-lookup"><span data-stu-id="d64d9-181">Y</span></span>         | <span data-ttu-id="d64d9-182">Zara</span><span class="sxs-lookup"><span data-stu-id="d64d9-182">Zara</span></span>          | <span data-ttu-id="d64d9-183">amet.docx</span><span class="sxs-lookup"><span data-stu-id="d64d9-183">amet.docx</span></span>       |
| <span data-ttu-id="d64d9-184">\[OUTROS\]</span><span class="sxs-lookup"><span data-stu-id="d64d9-184">\[OTHER\]</span></span> | <span data-ttu-id="d64d9-185">Abner</span><span class="sxs-lookup"><span data-stu-id="d64d9-185">Abner</span></span>         | <span data-ttu-id="d64d9-186">nonummy.docx</span><span class="sxs-lookup"><span data-stu-id="d64d9-186">nonummy.docx</span></span>    |
|           | <span data-ttu-id="d64d9-187">Roberto</span><span class="sxs-lookup"><span data-stu-id="d64d9-187">Bob</span></span>           | <span data-ttu-id="d64d9-188">laoreet.docx</span><span class="sxs-lookup"><span data-stu-id="d64d9-188">laoreet.docx</span></span>    |
|           | <span data-ttu-id="d64d9-189">Xaria</span><span class="sxs-lookup"><span data-stu-id="d64d9-189">Xaria</span></span>         | <span data-ttu-id="d64d9-190">magna.docx</span><span class="sxs-lookup"><span data-stu-id="d64d9-190">magna.docx</span></span>      |
| <span data-ttu-id="d64d9-191">**NULL**</span><span class="sxs-lookup"><span data-stu-id="d64d9-191">**NULL**</span></span>  |               | <span data-ttu-id="d64d9-192">aliquam.docx</span><span class="sxs-lookup"><span data-stu-id="d64d9-192">aliquam.docx</span></span>    |



 

## <a name="ordering-groups"></a><span data-ttu-id="d64d9-193">Grupos de pedidos</span><span class="sxs-lookup"><span data-stu-id="d64d9-193">Ordering Groups</span></span>

<span data-ttu-id="d64d9-194">Há três maneiras de ordenar itens em grupos:</span><span class="sxs-lookup"><span data-stu-id="d64d9-194">There are three ways to order items in groups:</span></span>

-   <span data-ttu-id="d64d9-195">Ordenação padrão: se você não especificar o contrário, os resultados serão ordenados pelos valores no grupo na coluna, em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="d64d9-195">Default ordering: If you do not specify otherwise, the results are ordered by the values in the GROUP ON column, in ascending order.</span></span>
-   <span data-ttu-id="d64d9-196">ORDENAr por: você pode especificar ordem decrescente em uma cláusula ORDER BY.</span><span class="sxs-lookup"><span data-stu-id="d64d9-196">ORDER BY: You can specify descending order in an ORDER BY clause.</span></span> <span data-ttu-id="d64d9-197">Você deve ordenar os resultados pelo grupo na coluna.</span><span class="sxs-lookup"><span data-stu-id="d64d9-197">You must order the results by the GROUP ON column.</span></span>
-   <span data-ttu-id="d64d9-198">ORDEM em Agrupar por: você pode especificar uma ordem diferente para cada grupo.</span><span class="sxs-lookup"><span data-stu-id="d64d9-198">ORDER IN GROUP BY: You can specify a different order for each group.</span></span> <span data-ttu-id="d64d9-199">Se você agrupar em [System. Kind](../properties/props-system-kind.md), poderá ordenar documentos por [System. Author](../properties/props-system-author.md) e música por [System. Music. artista](../properties/props-system-music-artist.md).</span><span class="sxs-lookup"><span data-stu-id="d64d9-199">If you group on [System.Kind](../properties/props-system-kind.md), you can order documents by [System.Author](../properties/props-system-author.md) and music by [System.Music.Artist](../properties/props-system-music-artist.md).</span></span>

<span data-ttu-id="d64d9-200">Para obter mais informações sobre como ordenar resultados, consulte as páginas de referência [ordem por cláusula](-search-sql-orderby.md) e [ordem nas cláusulas de grupo](-search-sql-orderingroup.md) .</span><span class="sxs-lookup"><span data-stu-id="d64d9-200">For more information on ordering results, see the [ORDER BY Clause](-search-sql-orderby.md) and [ORDER IN GROUP Clause](-search-sql-orderingroup.md) reference pages.</span></span>

## <a name="nesting-groups"></a><span data-ttu-id="d64d9-201">Aninhando grupos</span><span class="sxs-lookup"><span data-stu-id="d64d9-201">Nesting Groups</span></span>

<span data-ttu-id="d64d9-202">Você pode aninhar grupos com várias cláusulas GROUP ON.</span><span class="sxs-lookup"><span data-stu-id="d64d9-202">You can nest groups with multiple GROUP ON clauses.</span></span> <span data-ttu-id="d64d9-203">A ordem especificada na consulta é refletida diretamente na hierarquia do grupo de saída, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="d64d9-203">The order specified in the query is directly reflected in the output group hierarchy, as shown in the following example.</span></span>


```
GROUP ON <System.Kind> 
      OVER (GROUP ON <System.Author> 
                  OVER (SELECT <System.DateCreated>))
```





| <span data-ttu-id="d64d9-204">Sistema. Kind</span><span class="sxs-lookup"><span data-stu-id="d64d9-204">System.Kind</span></span>    | <span data-ttu-id="d64d9-205">System.Author</span><span class="sxs-lookup"><span data-stu-id="d64d9-205">System.Author</span></span> | <span data-ttu-id="d64d9-206">System. DateCreated</span><span class="sxs-lookup"><span data-stu-id="d64d9-206">System.DateCreated</span></span> |
|----------------|---------------|--------------------|
| <span data-ttu-id="d64d9-207">documentos</span><span class="sxs-lookup"><span data-stu-id="d64d9-207">documents</span></span>      | <span data-ttu-id="d64d9-208">Willa</span><span class="sxs-lookup"><span data-stu-id="d64d9-208">Willa</span></span>         | <span data-ttu-id="d64d9-209">2006-01-02</span><span class="sxs-lookup"><span data-stu-id="d64d9-209">2006-01-02</span></span>         |
|                |               | <span data-ttu-id="d64d9-210">2006-01-05</span><span class="sxs-lookup"><span data-stu-id="d64d9-210">2006-01-05</span></span>         |
|                | <span data-ttu-id="d64d9-211">Zara</span><span class="sxs-lookup"><span data-stu-id="d64d9-211">Zara</span></span>          | <span data-ttu-id="d64d9-212">2007-06-02</span><span class="sxs-lookup"><span data-stu-id="d64d9-212">2007-06-02</span></span>         |
|                |               | <span data-ttu-id="d64d9-213">2007-09-10</span><span class="sxs-lookup"><span data-stu-id="d64d9-213">2007-09-10</span></span>         |
| <span data-ttu-id="d64d9-214">comunicações</span><span class="sxs-lookup"><span data-stu-id="d64d9-214">communications</span></span> | <span data-ttu-id="d64d9-215">Abner</span><span class="sxs-lookup"><span data-stu-id="d64d9-215">Abner</span></span>         | <span data-ttu-id="d64d9-216">2006-04-16</span><span class="sxs-lookup"><span data-stu-id="d64d9-216">2006-04-16</span></span>         |
|                | <span data-ttu-id="d64d9-217">Jean</span><span class="sxs-lookup"><span data-stu-id="d64d9-217">Jean</span></span>          | <span data-ttu-id="d64d9-218">2007-02-20</span><span class="sxs-lookup"><span data-stu-id="d64d9-218">2007-02-20</span></span>         |
|                | <span data-ttu-id="d64d9-219">Willa</span><span class="sxs-lookup"><span data-stu-id="d64d9-219">Willa</span></span>         | <span data-ttu-id="d64d9-220">2006-10-15</span><span class="sxs-lookup"><span data-stu-id="d64d9-220">2006-10-15</span></span>         |
|                | <span data-ttu-id="d64d9-221">Zara</span><span class="sxs-lookup"><span data-stu-id="d64d9-221">Zara</span></span>          | <span data-ttu-id="d64d9-222">2008-01-02</span><span class="sxs-lookup"><span data-stu-id="d64d9-222">2008-01-02</span></span>         |



 

 

## <a name="grouping-on-vector-properties"></a><span data-ttu-id="d64d9-223">Agrupamento em Propriedades de vetor</span><span class="sxs-lookup"><span data-stu-id="d64d9-223">Grouping on Vector Properties</span></span>

<span data-ttu-id="d64d9-224">O agrupamento em Propriedades de vetor, propriedades que podem conter um ou mais valores simultaneamente, compara os valores de vetor individualmente por padrão.</span><span class="sxs-lookup"><span data-stu-id="d64d9-224">Grouping on vector properties, properties that can contain one or more values simultaneously, compares the vector values individually by default.</span></span> <span data-ttu-id="d64d9-225">Por exemplo, se houver um documento, Lorem.docx, com a propriedade System. Author como "Theresa; Zara "e outro documento, Ipsum.docx, com a propriedade System. Author como" Zara ", a consulta retorna o conjunto de resultados em dois grupos, como mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="d64d9-225">For example, if there is one document, Lorem.docx, with the System.Author property as "Theresa;Zara" and another document, Ipsum.docx, with the System.Author property as "Zara", the query returns the result set in two groups as shown here:</span></span>


```
GROUP ON <System.Author> 
      OVER (SELECT <System.FileName>)
```





| <span data-ttu-id="d64d9-226">System.Author</span><span class="sxs-lookup"><span data-stu-id="d64d9-226">System.Author</span></span> | <span data-ttu-id="d64d9-227">System. FileName</span><span class="sxs-lookup"><span data-stu-id="d64d9-227">System.FileName</span></span> |
|---------------|-----------------|
| <span data-ttu-id="d64d9-228">Theresa</span><span class="sxs-lookup"><span data-stu-id="d64d9-228">Theresa</span></span>       | <span data-ttu-id="d64d9-229">Lorem.docx</span><span class="sxs-lookup"><span data-stu-id="d64d9-229">Lorem.docx</span></span>      |
| <span data-ttu-id="d64d9-230">Zara</span><span class="sxs-lookup"><span data-stu-id="d64d9-230">Zara</span></span>          | <span data-ttu-id="d64d9-231">Lorem.docx</span><span class="sxs-lookup"><span data-stu-id="d64d9-231">Lorem.docx</span></span>      |
|               | <span data-ttu-id="d64d9-232">Ipsum.docx</span><span class="sxs-lookup"><span data-stu-id="d64d9-232">Ipsum.docx</span></span>      |



 

<span data-ttu-id="d64d9-233">Como você pode ver, o agrupamento nas propriedades de vetor retorna linhas duplicadas.</span><span class="sxs-lookup"><span data-stu-id="d64d9-233">As you can see, grouping on vector properties returns duplicate rows.</span></span> <span data-ttu-id="d64d9-234">Lorem.docx aparece duas vezes porque tem dois autores.</span><span class="sxs-lookup"><span data-stu-id="d64d9-234">Lorem.docx appears twice because it has two authors.</span></span>

 

## <a name="more-examples"></a><span data-ttu-id="d64d9-235">Mais exemplos</span><span class="sxs-lookup"><span data-stu-id="d64d9-235">More Examples</span></span>


```
GROUP ON System.Photo.ISOSpeed [0,10,100] 
      OVER (SELECT System.ItemName, System.Size, System.ItemUrl FROM SystemIndex)
            
GROUP ON System.DateCreated['2005/01/01 00:00:00', '2005/12/30 23:00:00'] 
      OVER (SELECT System.ItemName, System.Size, System.ItemUrl FROM SystemIndex)
            
GROUP ON System.Author ORDER BY System.Author DESC 
      OVER (GROUP ON System.DateCreated ORDER BY System.DateCreated ASC 
                  OVER (SELECT System.FileName, System.DateCreated, System.Size FROM SystemIndex 
                        WHERE CONTAINS(*, 'text')))

GROUP ON System.ItemName [before('a'), 'a', before ('c'), 'd', after('d')] 
      OVER (SELECT System.ItemName, System.ItemUrl FROM SystemIndex ORDER BY System.ItemName)                        
                        
GROUP ON System.ItemNameDisplay ['a' / 'col_a','c' / 'col_c'] 
      OVER (SELECT System.ItemNameDisplay FROM SystemIndex 
            ORDER BY System.ItemNameDisplay)

GROUP ON System.Size[1,2] 
      OVER (GROUP ON System.Author['a','f','mc','x'] 
                  OVER (GROUP ON System.DateCreated['2005/07/25 07:00:00', '2005/08/25 07:00:00']
                        ORDER BY System.DateCreated DESC 
                              OVER (SELECT System.FileName FROM SystemIndex 
                                    WHERE CONTAINS('text'))))   
```



## <a name="related-topics"></a><span data-ttu-id="d64d9-236">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d64d9-236">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d64d9-237">Funções de agregação</span><span class="sxs-lookup"><span data-stu-id="d64d9-237">Aggregate Functions</span></span>](-search-sql-aggregates.md)
</dt> <dt>

[<span data-ttu-id="d64d9-238">Cláusula ORDER BY</span><span class="sxs-lookup"><span data-stu-id="d64d9-238">ORDER BY Clause</span></span>](-search-sql-orderby.md)
</dt> <dt>

[<span data-ttu-id="d64d9-239">Cláusula ORDER IN GROUP</span><span class="sxs-lookup"><span data-stu-id="d64d9-239">ORDER IN GROUP Clause</span></span>](-search-sql-orderingroup.md)
</dt> </dl>

 

 
