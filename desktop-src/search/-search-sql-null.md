---
description: O predicado NULL indica se o documento tem um valor para a coluna indicada.
ms.assetid: 078ffd99-2020-4da2-8968-301dba8cc436
title: Predicado nulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea02a04313ac2b86afe809633bee5ad2cbcf764e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105786181"
---
# <a name="null-predicate"></a><span data-ttu-id="587df-103">Predicado nulo</span><span class="sxs-lookup"><span data-stu-id="587df-103">NULL Predicate</span></span>

<span data-ttu-id="587df-104">O predicado **NULL** indica se o documento tem um valor para a coluna indicada.</span><span class="sxs-lookup"><span data-stu-id="587df-104">The **NULL** predicate indicates whether the document has a value for the indicated column.</span></span>

<span data-ttu-id="587df-105">O predicado **NULL** tem a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="587df-105">The **NULL** predicate has the following syntax:</span></span>


```
...WHERE <column> IS [NOT] NULL
```



<span data-ttu-id="587df-106">A palavra-chave NOT opcional nega o resultado.</span><span class="sxs-lookup"><span data-stu-id="587df-106">The optional NOT keyword negates the result.</span></span> <span data-ttu-id="587df-107">A coluna pode ser um [identificador](-search-sql-identifiers.md)regular ou delimitado.</span><span class="sxs-lookup"><span data-stu-id="587df-107">The column can be a regular or delimited [identifier](-search-sql-identifiers.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="587df-108">Para testar se uma coluna tem o valor **nulo** , você deve usar o predicado **NULL** .</span><span class="sxs-lookup"><span data-stu-id="587df-108">To test whether a column has the **NULL** value, you must use the **NULL** predicate.</span></span> <span data-ttu-id="587df-109">Não é válido usar o valor **nulo** em um predicado de comparação.</span><span class="sxs-lookup"><span data-stu-id="587df-109">It is not valid to use the **NULL** value in a comparison predicate.</span></span> <span data-ttu-id="587df-110">"Onde a coluna é **nula**" está correta.</span><span class="sxs-lookup"><span data-stu-id="587df-110">"WHERE column IS **NULL**" is correct.</span></span> <span data-ttu-id="587df-111">"WHERE Column = **NULL**" não é válido.</span><span class="sxs-lookup"><span data-stu-id="587df-111">"WHERE column = **NULL**" is not valid.</span></span>

 

## <a name="example"></a><span data-ttu-id="587df-112">Exemplo</span><span class="sxs-lookup"><span data-stu-id="587df-112">Example</span></span>

<span data-ttu-id="587df-113">O exemplo a seguir retorna documentos que não têm um valor de System. video. director.</span><span class="sxs-lookup"><span data-stu-id="587df-113">The following example returns documents that do not have a System.Video.Director value.</span></span>


```
...WHERE System.Video.Director IS NULL
```



## <a name="related-topics"></a><span data-ttu-id="587df-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="587df-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="587df-115">**Referência**</span><span class="sxs-lookup"><span data-stu-id="587df-115">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="587df-116">Predicado LIKE</span><span class="sxs-lookup"><span data-stu-id="587df-116">LIKE Predicate</span></span>](-search-sql-like.md)
</dt> <dt>

[<span data-ttu-id="587df-117">Comparação de valor literal</span><span class="sxs-lookup"><span data-stu-id="587df-117">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="587df-118">Comparações de vários valores (matriz)</span><span class="sxs-lookup"><span data-stu-id="587df-118">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

<span data-ttu-id="587df-119">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="587df-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="587df-120">Predicados de texto completo</span><span class="sxs-lookup"><span data-stu-id="587df-120">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="587df-121">Predicados de texto não completo</span><span class="sxs-lookup"><span data-stu-id="587df-121">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



