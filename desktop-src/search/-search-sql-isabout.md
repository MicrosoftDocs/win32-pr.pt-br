---
description: O termo ISABOUT corresponde a colunas em um grupo de um ou mais termos de pesquisa.
ms.assetid: e2629c4c-4b44-4427-ac1d-17f55fd969e3
title: '@ SOBRE o termo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f79fc2fa4a56b3ca6b3b412141f096b282e3aa9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646870"
---
# <a name="isabout-term"></a><span data-ttu-id="b5945-103">@ SOBRE o termo</span><span class="sxs-lookup"><span data-stu-id="b5945-103">ISABOUT Term</span></span>

<span data-ttu-id="b5945-104">**Preterido**</span><span class="sxs-lookup"><span data-stu-id="b5945-104">**Deprecated**</span></span>

<span data-ttu-id="b5945-105">Esse recurso foi removido a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b5945-105">This feature has been removed as of Windows 8.</span></span> <span data-ttu-id="b5945-106">Se você escrever novos aplicativos, evite usar esse recurso preterido.</span><span class="sxs-lookup"><span data-stu-id="b5945-106">If you write new applications, avoid using this deprecated feature.</span></span> <span data-ttu-id="b5945-107">Se você modificar os aplicativos existentes, será altamente recomendável remover qualquer dependência desse recurso.</span><span class="sxs-lookup"><span data-stu-id="b5945-107">If you modify existing applications, you are strongly encouraged to remove any dependency on this feature.</span></span>

<span data-ttu-id="b5945-108">O termo ISABOUT corresponde a colunas em um grupo de um ou mais termos de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b5945-108">The ISABOUT term matches columns against a group of one or more search terms.</span></span> <span data-ttu-id="b5945-109">Ele tem a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="b5945-109">It has the following syntax:</span></span>


```
ISABOUT(<components>) [RANKMETHOD <method>]
```



<span data-ttu-id="b5945-110">O Termo RANKMETHOD opcional especifica o método de cálculo usado para classificar os documentos que correspondem a um ou mais dos componentes.</span><span class="sxs-lookup"><span data-stu-id="b5945-110">The optional RANKMETHOD term specifies the calculation method used to rank the documents that match one or more of the components.</span></span> <span data-ttu-id="b5945-111">Se nenhum RANKMETHOD for especificado, o método de classificação de coeficiente Jaccard padrão será usado.</span><span class="sxs-lookup"><span data-stu-id="b5945-111">If no RANKMETHOD is specified, the default Jaccard Coefficient ranking method is used.</span></span>

<span data-ttu-id="b5945-112">O termo ISABOUT pode ter um ou mais componentes.</span><span class="sxs-lookup"><span data-stu-id="b5945-112">The ISABOUT term can have one or more components.</span></span> <span data-ttu-id="b5945-113">As colunas especificadas no predicado [Contains](-search-sql-contains.md) são testadas em relação a cada componente.</span><span class="sxs-lookup"><span data-stu-id="b5945-113">The columns specified in the [CONTAINS](-search-sql-contains.md) predicate are tested against each component.</span></span> <span data-ttu-id="b5945-114">O documento será incluído nos resultados se pelo menos um dos componentes corresponder.</span><span class="sxs-lookup"><span data-stu-id="b5945-114">The document is included in the results if at least one of the components matches.</span></span> <span data-ttu-id="b5945-115">Vírgulas separam vários componentes.</span><span class="sxs-lookup"><span data-stu-id="b5945-115">Commas separate multiple components.</span></span>

<span data-ttu-id="b5945-116">A parte do componente tem a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="b5945-116">The component part has the following syntax:</span></span>


```
<match_term> [<weight_term>]
```



<span data-ttu-id="b5945-117">Você pode usar a condição de peso opcional para alterar a importância relativa de cada termo dentro do termo ISABOUT.</span><span class="sxs-lookup"><span data-stu-id="b5945-117">You can use the optional WEIGHT term to change the relative importance of each term within the ISABOUT term.</span></span> <span data-ttu-id="b5945-118">Se nenhum termo de peso for aplicado, o peso de 1,0 padrão será implícito.</span><span class="sxs-lookup"><span data-stu-id="b5945-118">If no weight term is applied, the default 1.0 weight is implied.</span></span>

<span data-ttu-id="b5945-119">A tabela a seguir descreve os tipos de termo de correspondência possíveis.</span><span class="sxs-lookup"><span data-stu-id="b5945-119">The following table describes possible match term types.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b5945-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="b5945-120">Type</span></span></th>
<th><span data-ttu-id="b5945-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5945-121">Description</span></span></th>
<th><span data-ttu-id="b5945-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b5945-122">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b5945-123">Word</span><span class="sxs-lookup"><span data-stu-id="b5945-123">Word</span></span></td>
<td><span data-ttu-id="b5945-124">Uma única palavra sem espaços ou outra Pontuação.</span><span class="sxs-lookup"><span data-stu-id="b5945-124">A single word without spaces or other punctuation.</span></span></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
 (&#39;ISABOUT (&quot;computer&quot;,&quot;software&quot;)&#39;)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5945-125">Frase</span><span class="sxs-lookup"><span data-stu-id="b5945-125">Phrase</span></span></td>
<td><span data-ttu-id="b5945-126">Várias palavras ou espaços incluídos.</span><span class="sxs-lookup"><span data-stu-id="b5945-126">Multiple words or included spaces.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
 (&#39;ISABOUT (&quot;computer software&quot;,&quot;hardware&quot;)&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5945-127">Curinga</span><span class="sxs-lookup"><span data-stu-id="b5945-127">Wildcard</span></span></td>
<td><span data-ttu-id="b5945-128">Palavras ou frases com o asterisco (\*) adicionado ao final.</span><span class="sxs-lookup"><span data-stu-id="b5945-128">Words or phrases with the asterisk (\*) added to the end.</span></span> <span data-ttu-id="b5945-129">Para obter mais informações, consulte <a href="-search-sql-wildcards.md">usando curingas no predicado CONTAINS</a>.</span><span class="sxs-lookup"><span data-stu-id="b5945-129">For more information, see <a href="-search-sql-wildcards.md">Using Wildcards in the CONTAINS Predicate</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
 (&#39;ISABOUT (&quot;compu*&quot;,&quot;soft*&quot;)&#39;)

Matches &quot;computer&quot;, &quot;computers&quot;, &quot;computation&quot;, 
and &quot;compulsory&quot;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="isabout-column-weighting"></a><span data-ttu-id="b5945-130">Issobre o peso da coluna</span><span class="sxs-lookup"><span data-stu-id="b5945-130">ISABOUT Column Weighting</span></span>

<span data-ttu-id="b5945-131">O termo ISABOUT classifica os documentos correspondentes com base no quão próximo cada documento corresponde ao conjunto de termos de correspondência na consulta.</span><span class="sxs-lookup"><span data-stu-id="b5945-131">The ISABOUT term ranks matching documents based on how closely each document matches the set of match terms in the query.</span></span> <span data-ttu-id="b5945-132">Você pode usar o peso de coluna para posicionar mais importância na correspondência de alguns termos de correspondência do que outros.</span><span class="sxs-lookup"><span data-stu-id="b5945-132">You can use column weighting to place more importance on matching some match terms than others.</span></span> <span data-ttu-id="b5945-133">Cada termo de correspondência no termo ISABOUT pode ter um valor de peso aplicado.</span><span class="sxs-lookup"><span data-stu-id="b5945-133">Each match term in the ISABOUT term can have a weight value applied.</span></span> <span data-ttu-id="b5945-134">O peso é aplicado a um único termo de correspondência e é indicado pela palavra-chave "WEIGHT".</span><span class="sxs-lookup"><span data-stu-id="b5945-134">The weight is applied to a single match term and is indicated by the keyword "WEIGHT".</span></span> <span data-ttu-id="b5945-135">O termo de peso tem duas sintaxes alternativas:</span><span class="sxs-lookup"><span data-stu-id="b5945-135">The WEIGHT term has two alternative syntaxes:</span></span>


```
<match_term> WEIGHT(<weight_value>)
<match_term>:(<weight_value>)
```



<span data-ttu-id="b5945-136">O valor de peso deve estar entre 0 e 1,0, com no máximo três casas decimais.</span><span class="sxs-lookup"><span data-stu-id="b5945-136">The weight value must be between 0 and 1.0, with no more than three decimal places.</span></span> <span data-ttu-id="b5945-137">A especificação de um valor de peso fora desse intervalo resulta em uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="b5945-137">Specifying a weight value outside this range results in an error message.</span></span> <span data-ttu-id="b5945-138">O valor de classificação não ponderada para um termo é multiplicado pelo valor de peso do termo.</span><span class="sxs-lookup"><span data-stu-id="b5945-138">The unweighted ranking value for a term is multiplied by the weight value for the term.</span></span>

<span data-ttu-id="b5945-139">Se nenhum peso for especificado para um termo de correspondência, o valor padrão, 1,0, será implícito.</span><span class="sxs-lookup"><span data-stu-id="b5945-139">If no weight is specified for a match term, the default value, 1.0, is implied.</span></span>

### <a name="example"></a><span data-ttu-id="b5945-140">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b5945-140">Example</span></span>

<span data-ttu-id="b5945-141">O exemplo a seguir aplica pesos aos dois termos de correspondência, usando a sintaxe longa e curta para valores de peso.</span><span class="sxs-lookup"><span data-stu-id="b5945-141">The following example applies weights to the two ISABOUT match terms, using both the long and short syntax for weight values.</span></span>


```
WHERE CONTAINS( System.FileName,
      'ISABOUT("computer" WEIGHT (0.75),"software":0.25)')
```



## <a name="related-topics"></a><span data-ttu-id="b5945-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b5945-142">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b5945-143">**Referência**</span><span class="sxs-lookup"><span data-stu-id="b5945-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b5945-144">Predicado FREETEXT</span><span class="sxs-lookup"><span data-stu-id="b5945-144">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

[<span data-ttu-id="b5945-145">Cláusula WHERE</span><span class="sxs-lookup"><span data-stu-id="b5945-145">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



