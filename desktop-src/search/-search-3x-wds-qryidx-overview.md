---
description: Há várias maneiras de usar o Windows Search para consultar o índice.
ms.assetid: 2c161b7f-4e28-4e8a-add6-3c1cda00a622
title: Consulta do índice de maneira programática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6390b31f4a1cc01ca723978a5107d5d9a502c4ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755238"
---
# <a name="querying-the-index-programmatically"></a><span data-ttu-id="56560-103">Consulta do índice de maneira programática</span><span class="sxs-lookup"><span data-stu-id="56560-103">Querying the Index Programmatically</span></span>

<span data-ttu-id="56560-104">Há várias maneiras de usar o Windows Search para consultar o índice.</span><span class="sxs-lookup"><span data-stu-id="56560-104">There are several ways to use Windows Search to query the index.</span></span>

<span data-ttu-id="56560-105">Esta seção fornece a estrutura conceitual para consultar o índice programaticamente:</span><span class="sxs-lookup"><span data-stu-id="56560-105">This section provides the conceptual framework for querying the index programmatically:</span></span>

-   [<span data-ttu-id="56560-106">Usando abordagens SQL e AQS para consultar o índice</span><span class="sxs-lookup"><span data-stu-id="56560-106">Using SQL and AQS Approaches to Query the Index</span></span>](using-sql-and-aqs-to-query-the-index.md)
-   [<span data-ttu-id="56560-107">Consultando o índice com ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="56560-107">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)
-   [<span data-ttu-id="56560-108">Consultando o índice com o protocolo Search-MS</span><span class="sxs-lookup"><span data-stu-id="56560-108">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)
-   [<span data-ttu-id="56560-109">Consultando o índice com a sintaxe SQL do Windows Search</span><span class="sxs-lookup"><span data-stu-id="56560-109">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
-   [<span data-ttu-id="56560-110">Usando a sintaxe de consulta avançada programaticamente</span><span class="sxs-lookup"><span data-stu-id="56560-110">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)

> [!Note]  
> <span data-ttu-id="56560-111">Compatibilidade do Microsoft Windows Desktop Search (WDS) 2x herdada: em computadores que executam o Windows XP e posterior, o [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) foi preterido.</span><span class="sxs-lookup"><span data-stu-id="56560-111">Legacy Microsoft Windows Desktop Search (WDS) 2x compatibility: On computers running Windows XP and later, [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) is deprecated.</span></span> <span data-ttu-id="56560-112">Em vez disso, os desenvolvedores devem usar [**ISearchQueryHelper**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) para obter uma cadeia de conexão e analisar a consulta do usuário em linguagem SQL (SQL) e consultar o banco de dados de incorporação e vinculação de objetos (OLE DB).</span><span class="sxs-lookup"><span data-stu-id="56560-112">Instead, developers should use [**ISearchQueryHelper**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) to get a connection string and to parse the user's query into Structured Query Language (SQL), and then query through Object Linking and Embedding Database (OLE DB).</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="56560-113">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="56560-113">Additional Resources</span></span>

-   <span data-ttu-id="56560-114">Para obter informações sobre OLE DB, consulte [visão geral da programação de OLE DB](https://msdn.microsoft.com/library/Cc522830(v=VS.71).aspx).</span><span class="sxs-lookup"><span data-stu-id="56560-114">For information on OLE DB, see [OLE DB Programming Overview](https://msdn.microsoft.com/library/Cc522830(v=VS.71).aspx).</span></span> <span data-ttu-id="56560-115">Para obter informações sobre o Provedor de Dados de .NET Framework para OLE DB, consulte o [namespace System. Data. OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1).</span><span class="sxs-lookup"><span data-stu-id="56560-115">For information on the .NET Framework Data Provider for OLE DB, see the [System.Data.OleDb Namespace](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1).</span></span>
-   <span data-ttu-id="56560-116">Para obter mais informações sobre como usar as propriedades na consulta, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="56560-116">For additional background on using properties in querying, see the following topics:</span></span>
    -   [<span data-ttu-id="56560-117">Sistema de propriedades</span><span class="sxs-lookup"><span data-stu-id="56560-117">Property System</span></span>](../properties/building-property-handlers.md)
    -   <span data-ttu-id="56560-118">[Propriedades do sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="56560-118">[System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span></span>
-   <span data-ttu-id="56560-119">Para obter informações sobre como criar e modificar pastas de pesquisa, consulte [**interface ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory).</span><span class="sxs-lookup"><span data-stu-id="56560-119">For information on how to create and modify search folders, see [**ISearchFolderItemFactory Interface**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory).</span></span>
-   <span data-ttu-id="56560-120">Para ver os quadros de mensagens de perguntas e discussões com suporte da Comunidade em tecnologias de pesquisa, consulte [Fórum do MSDN: desenvolvimento do Windows Desktop Search](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).</span><span class="sxs-lookup"><span data-stu-id="56560-120">For community-supported question and discussion message boards on Search technologies, see [MSDN Forum: Windows Desktop Search Development](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).</span></span>
-   <span data-ttu-id="56560-121">Para baixar os exemplos de código do SDK de pesquisa:</span><span class="sxs-lookup"><span data-stu-id="56560-121">To download the Search SDK Code Samples:</span></span>
    -   <span data-ttu-id="56560-122">Para o Windows 7: [exemplos do Windows Search no GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)</span><span class="sxs-lookup"><span data-stu-id="56560-122">For Windows 7: [Windows Search Samples on GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)</span></span>
    -   <span data-ttu-id="56560-123">Para o Windows Vista: [exemplos do SDK do Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)</span><span class="sxs-lookup"><span data-stu-id="56560-123">For Windows Vista: [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)</span></span>
-   <span data-ttu-id="56560-124">Para baixar o SDK do Windows:</span><span class="sxs-lookup"><span data-stu-id="56560-124">To download the Windows SDK:</span></span>
    -   <span data-ttu-id="56560-125">Para o Windows 7: [SDK do Windows para Windows 7 e .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="56560-125">For Windows 7: [Windows SDK for Windows 7 and .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span></span>
    -   <span data-ttu-id="56560-126">Para o Windows Vista: [SDK do Windows para Windows Vista e .NET Framework](https://www.microsoft.com/download/details.aspx?id=31950)</span><span class="sxs-lookup"><span data-stu-id="56560-126">For Windows Vista: [Windows SDK for Windows Vista and .NET Framework](https://www.microsoft.com/download/details.aspx?id=31950)</span></span>

## <a name="related-topics"></a><span data-ttu-id="56560-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="56560-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56560-128">Guia de desenvolvimento do Windows Search</span><span class="sxs-lookup"><span data-stu-id="56560-128">Windows Search Development Guide</span></span>](-search-developers-guide-entry-page.md)
</dt> <dt>

[<span data-ttu-id="56560-129">Gerenciar o índice</span><span class="sxs-lookup"><span data-stu-id="56560-129">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[<span data-ttu-id="56560-130">Estendendo o índice do Windows Search</span><span class="sxs-lookup"><span data-stu-id="56560-130">Extending the Windows Search Index</span></span>](-search-3x-wds-extidx-overview.md)
</dt> <dt>

[<span data-ttu-id="56560-131">Estendendo recursos de idioma</span><span class="sxs-lookup"><span data-stu-id="56560-131">Extending Language Resources</span></span>](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
