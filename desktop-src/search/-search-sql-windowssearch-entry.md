---
description: O Windows Search fornece recursos de rastreamento e pesquisa de conteúdo que dão suporte à pesquisa de texto completo. A linguagem de consulta usada pelo Windows Search estende a sintaxe de consulta de banco de dados SQL-92 e SQL-99 padrão para aprimorar sua utilidade com pesquisas baseadas em texto.
ms.assetid: a2eb550a-bb55-4dbd-9ca1-60b776eb9339
title: Consultando o índice com a sintaxe SQL do Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5696891b14340e8d8fe97f0c0cfbdc75db08e464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460982"
---
# <a name="querying-the-index-with-windows-search-sql-syntax"></a><span data-ttu-id="15c76-104">Consultando o índice com a sintaxe SQL do Windows Search</span><span class="sxs-lookup"><span data-stu-id="15c76-104">Querying the Index with Windows Search SQL Syntax</span></span>

<span data-ttu-id="15c76-105">O Windows Search fornece recursos de rastreamento e pesquisa de conteúdo que dão suporte à pesquisa de texto completo.</span><span class="sxs-lookup"><span data-stu-id="15c76-105">Windows Search provides content crawling and search features that support full-text searching.</span></span> <span data-ttu-id="15c76-106">A linguagem de consulta usada pelo Windows Search estende a sintaxe de consulta de banco de dados SQL-92 e SQL-99 padrão para aprimorar sua utilidade com pesquisas baseadas em texto.</span><span class="sxs-lookup"><span data-stu-id="15c76-106">The query language used by Windows Search extends the standard SQL-92 and SQL-99 database query syntax to enhance its usefulness with text-based searches.</span></span>

<span data-ttu-id="15c76-107">Todos os recursos do Windows Search linguagem SQL (SQL) são compatíveis com o Windows Search no Windows Vista e posterior, incluindo todas as versões do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="15c76-107">All features of Windows Search Structured Query Language (SQL) are compatible with Windows Search on Windows Vista, and later, including all versions of Windows 10.</span></span>

<span data-ttu-id="15c76-108">Esta seção fornece uma visão geral da sintaxe SQL no Windows Search e inclui os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="15c76-108">This section provides an overview of SQL syntax in Windows Search, and includes the following topics:</span></span>

- [<span data-ttu-id="15c76-109">Visão geral da sintaxe SQL do Windows Search</span><span class="sxs-lookup"><span data-stu-id="15c76-109">Overview of Windows Search SQL Syntax</span></span>](-search-sql-ovwofsearchquery.md)
- [<span data-ttu-id="15c76-110">Informações gerais da linguagem de consulta</span><span class="sxs-lookup"><span data-stu-id="15c76-110">General Query Language Information</span></span>](-search-sql-generalqueryinfo.md)
- [<span data-ttu-id="15c76-111">AGRUPAR EM... SOBRE... Privacidade</span><span class="sxs-lookup"><span data-stu-id="15c76-111">GROUP ON ... OVER... Statement</span></span>](-search-sql-group-on-over.md)
- [<span data-ttu-id="15c76-112">Instrução SELECT</span><span class="sxs-lookup"><span data-stu-id="15c76-112">SELECT Statement</span></span>](-search-sql-select.md)
- [<span data-ttu-id="15c76-113">Cláusula FROM</span><span class="sxs-lookup"><span data-stu-id="15c76-113">FROM Clause</span></span>](-search-sql-from.md)
- [<span data-ttu-id="15c76-114">Cláusula WHERE</span><span class="sxs-lookup"><span data-stu-id="15c76-114">WHERE Clause</span></span>](-search-sql-where.md)
- [<span data-ttu-id="15c76-115">Cláusula ORDER BY</span><span class="sxs-lookup"><span data-stu-id="15c76-115">ORDER BY Clause</span></span>](-search-sql-orderby.md)
- [<span data-ttu-id="15c76-116">CLASSIFICAR por cláusula</span><span class="sxs-lookup"><span data-stu-id="15c76-116">RANK BY Clause</span></span>](-search-sql-rankby.md)
- [<span data-ttu-id="15c76-117">Instrução SET</span><span class="sxs-lookup"><span data-stu-id="15c76-117">SET Statement</span></span>](-search-sql-set.md)
- [<span data-ttu-id="15c76-118">Propriedades do conjunto de linhas</span><span class="sxs-lookup"><span data-stu-id="15c76-118">Rowset Properties</span></span>](-search-sql-rowset-properties.md)

<span data-ttu-id="15c76-119">Esta documentação pressupõe familiaridade com a vinculação de objetos e o banco de dados de incorporação (OLE DB) e SQL.</span><span class="sxs-lookup"><span data-stu-id="15c76-119">This documentation assumes familiarity with Object Linking and Embedding Database (OLE DB), and SQL.</span></span>

## <a name="code-samples"></a><span data-ttu-id="15c76-120">Exemplos de código</span><span class="sxs-lookup"><span data-stu-id="15c76-120">Code samples</span></span>

<span data-ttu-id="15c76-121">O exemplo de código WSSQL demonstra como se comunicar entre o Microsoft OLE DB e o Windows Search por meio do SQL.</span><span class="sxs-lookup"><span data-stu-id="15c76-121">The WSSQL code sample demonstrates how to communicate between Microsoft OLE DB and Windows Search through SQL.</span></span> <span data-ttu-id="15c76-122">O exemplo de código WSOleDB ilustra Active Template Library (ATL) OLE DB acesso aos aplicativos do Windows Search e dois métodos adicionais para recuperar os resultados do Windows Search.</span><span class="sxs-lookup"><span data-stu-id="15c76-122">The WSOleDB code sample illustrates Active Template Library (ATL) OLE DB access to Windows Search applications, and two additional methods for retrieving results from Windows Search.</span></span> <span data-ttu-id="15c76-123">Ambos os exemplos estão disponíveis nos [exemplos do Windows Search](-search-samples-ovw.md) e no [SDK do Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span><span class="sxs-lookup"><span data-stu-id="15c76-123">Both samples are available in the [Windows Search Samples](-search-samples-ovw.md) and the [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span></span>

## <a name="related-topics"></a><span data-ttu-id="15c76-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="15c76-124">Related topics</span></span>

[<span data-ttu-id="15c76-125">Consulta do índice de maneira programática</span><span class="sxs-lookup"><span data-stu-id="15c76-125">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)

[<span data-ttu-id="15c76-126">Usando abordagens SQL e AQS para consultar o índice</span><span class="sxs-lookup"><span data-stu-id="15c76-126">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)

[<span data-ttu-id="15c76-127">Consultando o índice com ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="15c76-127">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)

[<span data-ttu-id="15c76-128">Consultando o índice com o protocolo Search-MS</span><span class="sxs-lookup"><span data-stu-id="15c76-128">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)

[<span data-ttu-id="15c76-129">Consultando o índice com a sintaxe SQL do Windows Search</span><span class="sxs-lookup"><span data-stu-id="15c76-129">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)

[<span data-ttu-id="15c76-130">Usando a sintaxe de consulta avançada programaticamente</span><span class="sxs-lookup"><span data-stu-id="15c76-130">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
