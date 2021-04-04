---
description: O protocolo de aplicativo pesquisa-MS é uma Convenção para consultar o índice do Windows Search.
ms.assetid: ab2695ed-4ef3-4687-81b0-416ca7086e5f
title: Consultando o índice com o protocolo Search-MS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0d835b6db1c9b05b97d5d075b62158069d89029
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646879"
---
# <a name="querying-the-index-with-the-search-ms-protocol"></a><span data-ttu-id="98f92-103">Consultando o índice com o protocolo Search-MS</span><span class="sxs-lookup"><span data-stu-id="98f92-103">Querying the Index with the search-ms Protocol</span></span>

<span data-ttu-id="98f92-104">O [protocolo de aplicativo](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) **pesquisa-MS** é uma Convenção para consultar o índice do Windows Search.  </span><span class="sxs-lookup"><span data-stu-id="98f92-104">The **search-ms**  [application protocol](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) is a convention for querying the Windows Search index.</span></span> <span data-ttu-id="98f92-105">O protocolo permite que aplicativos, como o Windows Explorer, consultem o índice com argumentos de valor de parâmetro, incluindo argumentos de propriedade, pesquisas salvas anteriormente, sintaxe de consulta avançada (AQS), sintaxe de consulta natural (NQS) e identificadores de código de idioma (LCIDs) para o indexador e a própria consulta.</span><span class="sxs-lookup"><span data-stu-id="98f92-105">The protocol enables applications, like Windows Explorer, to query the index with parameter-value arguments, including property arguments, previously saved searches, Advanced Query Syntax (AQS), Natural Query Syntax (NQS), and language code identifiers (LCIDs) for both the indexer and the query itself.</span></span>

<span data-ttu-id="98f92-106">Esta seção é organizada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="98f92-106">This section is organized as follows:</span></span>

-   [<span data-ttu-id="98f92-107">Introdução com argumentos de Parameter-Value</span><span class="sxs-lookup"><span data-stu-id="98f92-107">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
-   [<span data-ttu-id="98f92-108">Argumentos do identificador de localidade</span><span class="sxs-lookup"><span data-stu-id="98f92-108">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
-   [<span data-ttu-id="98f92-109">Argumento de trilha</span><span class="sxs-lookup"><span data-stu-id="98f92-109">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
-   [<span data-ttu-id="98f92-110">Argumento de sintaxe</span><span class="sxs-lookup"><span data-stu-id="98f92-110">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
-   [<span data-ttu-id="98f92-111">Argumento STACKEDBY</span><span class="sxs-lookup"><span data-stu-id="98f92-111">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
-   [<span data-ttu-id="98f92-112">Argumento de subconsulta</span><span class="sxs-lookup"><span data-stu-id="98f92-112">SUBQUERY Argument</span></span>](-search-3x-wds-qryidx-subquery.md)

## <a name="related-topics"></a><span data-ttu-id="98f92-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="98f92-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98f92-114">Consulta do índice de maneira programática</span><span class="sxs-lookup"><span data-stu-id="98f92-114">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="98f92-115">Usando abordagens SQL e AQS para consultar o índice</span><span class="sxs-lookup"><span data-stu-id="98f92-115">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="98f92-116">Consultando o índice com ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="98f92-116">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[<span data-ttu-id="98f92-117">Consultando o índice com a sintaxe SQL do Windows Search</span><span class="sxs-lookup"><span data-stu-id="98f92-117">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> <dt>

[<span data-ttu-id="98f92-118">Usando a sintaxe de consulta avançada programaticamente</span><span class="sxs-lookup"><span data-stu-id="98f92-118">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
</dt> </dl>

 

 
