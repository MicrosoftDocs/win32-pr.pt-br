---
description: 'Saiba mais sobre: cláusula ORDER BY'
ms.assetid: e720cf0d-b034-48e2-a13e-e97dd23b2beb
title: Cláusula ORDER BY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eaa3c834ca2fe04222ef2ae452a0119bf391b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090064"
---
# <a name="order-by-clause"></a><span data-ttu-id="bc3f0-103">Cláusula ORDER BY</span><span class="sxs-lookup"><span data-stu-id="bc3f0-103">ORDER BY Clause</span></span>

<span data-ttu-id="bc3f0-104">A cláusula ORDER BY classifica os resultados com base no valor de uma ou mais colunas que você especificar.</span><span class="sxs-lookup"><span data-stu-id="bc3f0-104">The ORDER BY clause sorts the results based on the value of one or more columns you specify.</span></span> <span data-ttu-id="bc3f0-105">A seguir, a sintaxe da cláusula ORDER BY:</span><span class="sxs-lookup"><span data-stu-id="bc3f0-105">Following is the syntax of the ORDER BY clause:</span></span>


```
ORDER BY <column> [<direction>] [,<column> [<direction>]]
```



<span data-ttu-id="bc3f0-106">O especificador de coluna deve ser uma coluna válida.</span><span class="sxs-lookup"><span data-stu-id="bc3f0-106">The column specifier must be a valid column.</span></span> <span data-ttu-id="bc3f0-107">Você pode usar o especificador de coluna para fazer referência a colunas pela ordem em que elas aparecem na consulta.</span><span class="sxs-lookup"><span data-stu-id="bc3f0-107">You can use the column specifier to refer to columns by the order that they appear in the query.</span></span> <span data-ttu-id="bc3f0-108">A primeira coluna na consulta é numerada 1.</span><span class="sxs-lookup"><span data-stu-id="bc3f0-108">The first column in the query is numbered 1.</span></span> <span data-ttu-id="bc3f0-109">Você pode incluir mais de uma coluna na cláusula ORDER BY, separada por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="bc3f0-109">You can include more than one column in the ORDER BY clause, separated by commas.</span></span>

<span data-ttu-id="bc3f0-110">O especificador de direção opcional pode ser "ASC" para crescente (baixo para alto) ou "DESC" para decrescente (alto para baixo).</span><span class="sxs-lookup"><span data-stu-id="bc3f0-110">The optional direction specifier can be either "ASC" for ascending (low to high) or "DESC" for descending (high to low).</span></span> <span data-ttu-id="bc3f0-111">Se você não fornecer um especificador de direção, o padrão, Ascending, será usado.</span><span class="sxs-lookup"><span data-stu-id="bc3f0-111">If you do not provide a direction specifier, the default, ascending, is used.</span></span> <span data-ttu-id="bc3f0-112">Se você especificar mais de uma coluna, mas não especificar todas as direções, a direção especificada por último será aplicada a cada coluna até que você altere explicitamente a direção.</span><span class="sxs-lookup"><span data-stu-id="bc3f0-112">If you specify more than one column, but do not specify all directions, the direction you specify last is applied to each column until you explicitly change the direction.</span></span>

<span data-ttu-id="bc3f0-113">Por exemplo, na cláusula ORDER BY a seguir, as colunas A, B, C e G são classificadas em ordem crescente, enquanto as colunas D, E e F são classificadas em ordem decrescente.</span><span class="sxs-lookup"><span data-stu-id="bc3f0-113">For example, in the following ORDER BY clause, the columns A, B, C, and G are sorted in ascending order, while columns D, E, and F are sorted in descending order.</span></span>


```
ORDER BY A ASC, B, C, D DESC, E, F, G ASC
```



## <a name="related-topics"></a><span data-ttu-id="bc3f0-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bc3f0-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bc3f0-115">**Referência**</span><span class="sxs-lookup"><span data-stu-id="bc3f0-115">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bc3f0-116">Cláusula FROM</span><span class="sxs-lookup"><span data-stu-id="bc3f0-116">FROM Clause</span></span>](-search-sql-from.md)
</dt> <dt>

[<span data-ttu-id="bc3f0-117">CLASSIFICAR por cláusula</span><span class="sxs-lookup"><span data-stu-id="bc3f0-117">RANK BY Clause</span></span>](-search-sql-rankby.md)
</dt> <dt>

[<span data-ttu-id="bc3f0-118">Instrução SELECT</span><span class="sxs-lookup"><span data-stu-id="bc3f0-118">SELECT Statement</span></span>](-search-sql-select.md)
</dt> <dt>

<span data-ttu-id="bc3f0-119">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="bc3f0-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bc3f0-120">Predicados de texto completo</span><span class="sxs-lookup"><span data-stu-id="bc3f0-120">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="bc3f0-121">Predicados de texto não completo</span><span class="sxs-lookup"><span data-stu-id="bc3f0-121">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



