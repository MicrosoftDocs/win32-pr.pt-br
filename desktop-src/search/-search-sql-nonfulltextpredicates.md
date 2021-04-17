---
description: A linguagem de consulta do Microsoft Windows Search dá suporte a seis predicados de pesquisa de texto não completo. Os predicados descritos nesta seção estão listados na tabela a seguir.
ms.assetid: 74aa6dbc-5c0d-433e-96d9-a8db63907342
title: Predicados de texto não completo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d41076ebc61aa56ed547f13f717ac40bed35959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762364"
---
# <a name="non-full-text-predicates"></a><span data-ttu-id="72771-104">Predicados de texto não completo</span><span class="sxs-lookup"><span data-stu-id="72771-104">Non-Full-Text Predicates</span></span>

<span data-ttu-id="72771-105">A linguagem de consulta do Microsoft Windows Search dá suporte a seis predicados de pesquisa de texto não completo.</span><span class="sxs-lookup"><span data-stu-id="72771-105">The Microsoft Windows Search query language supports six non-full-text search predicates.</span></span> <span data-ttu-id="72771-106">Os predicados descritos nesta seção estão listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="72771-106">The predicates described in this section are listed in the following table.</span></span>



| <span data-ttu-id="72771-107">Predicado de texto não completo</span><span class="sxs-lookup"><span data-stu-id="72771-107">Non-full-text predicate</span></span>                                                    | <span data-ttu-id="72771-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="72771-108">Description</span></span>                                                                                                                                                                             |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72771-109">Todos os bits e a bit a bit</span><span class="sxs-lookup"><span data-stu-id="72771-109">ALL BITWISE and SOME BITWISE</span></span>](all-bitwise.md)                            | <span data-ttu-id="72771-110">É um conjunto de palavras-chave que estão prestes a testar os bits em um tipo integral.</span><span class="sxs-lookup"><span data-stu-id="72771-110">Is a set of keywords that are about testing the bits in an integral type.</span></span>                                                                                                               |
| [<span data-ttu-id="72771-111">Função DATEADD</span><span class="sxs-lookup"><span data-stu-id="72771-111">DATEADD Function</span></span>](-search-sql-dateadd.md)                                | <span data-ttu-id="72771-112">Executa cálculos de data e hora para propriedades correspondentes com tipos de data.</span><span class="sxs-lookup"><span data-stu-id="72771-112">Performs time and date calculations for matching properties having date types.</span></span> <span data-ttu-id="72771-113">Use a função DATEADD para obter datas e horas em um período de tempo especificado antes da apresentação.</span><span class="sxs-lookup"><span data-stu-id="72771-113">Use the DATEADD function to obtain dates and times in a specified amount of time before the present.</span></span>     |
| [<span data-ttu-id="72771-114">Predicado LIKE</span><span class="sxs-lookup"><span data-stu-id="72771-114">LIKE Predicate</span></span>](-search-sql-like.md)                                     | <span data-ttu-id="72771-115">Compara valores de coluna usando a correspondência de padrão simples com caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="72771-115">Compares column values using simple pattern matching with wildcard characters.</span></span>                                                                                                          |
| [<span data-ttu-id="72771-116">Comparação de valor literal</span><span class="sxs-lookup"><span data-stu-id="72771-116">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)         | <span data-ttu-id="72771-117">Compara valores de coluna com valores literais de cadeia de caracteres, data, carimbo de hora, numéricos e outros.</span><span class="sxs-lookup"><span data-stu-id="72771-117">Compares column values against string, date, time stamp, numeric, and other literal values.</span></span> <span data-ttu-id="72771-118">Esse predicado dá suporte a desigualdades, como maior que (' > ') e menor que (' < ').</span><span class="sxs-lookup"><span data-stu-id="72771-118">This predicate supports inequalities such as greater than ('>'), and less than ('<').</span></span> |
| [<span data-ttu-id="72771-119">Comparações de vários valores (matriz)</span><span class="sxs-lookup"><span data-stu-id="72771-119">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md) | <span data-ttu-id="72771-120">Compara colunas com valores de multivalors em uma matriz de valores literais.</span><span class="sxs-lookup"><span data-stu-id="72771-120">Compares multivalued columns against a multivalued array of literals.</span></span>                                                                                                                   |
| [<span data-ttu-id="72771-121">Predicado nulo</span><span class="sxs-lookup"><span data-stu-id="72771-121">NULL Predicate</span></span>](-search-sql-null.md)                                     | <span data-ttu-id="72771-122">Detecta valores de coluna indefinidos para o documento.</span><span class="sxs-lookup"><span data-stu-id="72771-122">Detects column values that are undefined for the document.</span></span>                                                                                                                              |



 

> [!IMPORTANT]
> <span data-ttu-id="72771-123">As consultas de pesquisa que usam o predicado **NULL** podem exigir que o Windows Search Verifique todo o catálogo, o que pode retardar o desempenho da consulta.</span><span class="sxs-lookup"><span data-stu-id="72771-123">Search queries using the **NULL** predicate can require that Windows Search scan the entire catalog, which might slow down the query's performance.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="72771-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="72771-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72771-125">Predicados de texto completo</span><span class="sxs-lookup"><span data-stu-id="72771-125">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> </dl>

 

 



