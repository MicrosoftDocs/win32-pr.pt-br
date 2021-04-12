---
title: Pesquisando Active Directory
description: Uma função importante do Active Directory é resolver consultas de dados para pessoas, bem como dados de configuração para computadores e serviços.
ms.assetid: 8427d69b-0974-4adc-9732-790e5d31db7a
ms.tgt_platform: multiple
keywords:
- Pesquisando Active Directory ADSI
- ADSI ADSI, pesquisando Active Directory
- consulta ADSI, pesquisando Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1881872be6092312015f22eba477599ed9394df7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291778"
---
# <a name="searching-active-directory"></a><span data-ttu-id="b1dc0-106">Pesquisando Active Directory</span><span class="sxs-lookup"><span data-stu-id="b1dc0-106">Searching Active Directory</span></span>

<span data-ttu-id="b1dc0-107">Uma função importante do Active Directory é resolver consultas de dados para pessoas, bem como dados de configuração para computadores e serviços.</span><span class="sxs-lookup"><span data-stu-id="b1dc0-107">An important function of Active Directory is to resolve data queries for people, as well as configuration data for computers and services.</span></span> <span data-ttu-id="b1dc0-108">Para escrever consultas eficientes para Active Directory, é útil estar familiarizado com o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b1dc0-108">To write efficient queries for Active Directory, it is helpful to be familiar with the following:</span></span>

-   <span data-ttu-id="b1dc0-109">Determinando o escopo da consulta: o cliente deve localizar as propriedades de objetos que podem estar localizados em qualquer lugar dentro de uma floresta ou somente dentro de um domínio ou em uma UO (unidade organizacional) específica?</span><span class="sxs-lookup"><span data-stu-id="b1dc0-109">Determining the scope of the query: Must the client find properties for objects that might be located anywhere within a forest, or only within one domain, or within a given organizational unit (OU)?</span></span>
-   <span data-ttu-id="b1dc0-110">Determinando a profundidade da consulta: a consulta deve pesquisar apenas um nível ou ela pode atravessar outros diretórios LDAP?</span><span class="sxs-lookup"><span data-stu-id="b1dc0-110">Determining the depth of the query: Must the query only search one level or might it cross into other LDAP directories?</span></span>
-   <span data-ttu-id="b1dc0-111">Desempenho e manipulação de grandes conjuntos de resultados: como o cliente deve lidar efetivamente com o potencial de um grande conjunto de resultados?</span><span class="sxs-lookup"><span data-stu-id="b1dc0-111">Performance and handling large result sets: How should the client effectively handle the potential of a large result set?</span></span>
-   <span data-ttu-id="b1dc0-112">Determinando as melhores consultas: quais tipos de consultas fornecem os resultados mais eficientes?</span><span class="sxs-lookup"><span data-stu-id="b1dc0-112">Determining the best queries: What type of queries provide the most efficient results?</span></span> <span data-ttu-id="b1dc0-113">Que tipo de consultas o desenvolvedor deve evitar?</span><span class="sxs-lookup"><span data-stu-id="b1dc0-113">What type of queries should the developer avoid?</span></span>
-   <span data-ttu-id="b1dc0-114">Compreendendo a sintaxe de consulta: a ADSI dá suporte à sintaxe LDAP, conforme documentado em RFC 2254, bem como um subconjunto de SQL.</span><span class="sxs-lookup"><span data-stu-id="b1dc0-114">Understanding the query syntax: ADSI supports both the LDAP syntax as documented in RFC 2254, as well as a subset of SQL.</span></span>
-   <span data-ttu-id="b1dc0-115">Opções de interfaces: a ADSI fornece suporte a OLE DB, bem como uma interface C/C++ chamada [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch).</span><span class="sxs-lookup"><span data-stu-id="b1dc0-115">Choice of interfaces: ADSI provides both OLE DB support as well as a C/C++ interface called [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch).</span></span> <span data-ttu-id="b1dc0-116">Como o ADSI funciona para vários namespaces, você pode usar essas interfaces para consultar outros namespaces, como o Exchange, bem como Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b1dc0-116">Because ADSI works for multiple namespaces, you can use these interfaces for querying other namespaces such as Exchange, as well as Active Directory.</span></span> <span data-ttu-id="b1dc0-117">Como o ADO (ActiveX Data Object) é um modelo de objeto de acesso a dados simples programável por scripts sobre OLE DB, as interfaces de OLE DB funcionam bem para programadores de Visual Basic e gravadores de script de página da Web.</span><span class="sxs-lookup"><span data-stu-id="b1dc0-117">Because the ActiveX Data Object (ADO) is a simple scriptable data access object model on top of OLE DB, the OLE DB interfaces work well for Visual Basic programmers and webpage script writers.</span></span> <span data-ttu-id="b1dc0-118">Os novos recursos de acesso a dados dentro de aplicativos do Visual Studio e do Office que aproveitam o ADO e o OLE DB agora podem acessar Active Directory dados da mesma forma que acessam dados de outros provedores de OLE DB, como o SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b1dc0-118">The new data access features within Visual Studio and Office applications that take advantage of ADO and OLE DB can now access Active Directory data in the same way that they access data from other OLE DB providers, such as SQL Server.</span></span> <span data-ttu-id="b1dc0-119">No entanto, se um desenvolvedor de C/C++ precisar executar uma pesquisa de diretório simples, a interface **IDirectorySearch** poderá ser mais apropriada do que as interfaces de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="b1dc0-119">However, if a C/C++ developer must perform a simple directory search, the **IDirectorySearch** interface might be more appropriate than the OLE DB interfaces.</span></span>

<span data-ttu-id="b1dc0-120">Os tópicos a seguir descrevem como Pesquisar Active Directory para garantir que seu aplicativo emita a consulta mais eficiente, considerando os requisitos do cliente:</span><span class="sxs-lookup"><span data-stu-id="b1dc0-120">The following topics describe how to search Active Directory to ensure your application issues the most efficient query, given the requirements of the client:</span></span>

-   [<span data-ttu-id="b1dc0-121">Escopo da consulta</span><span class="sxs-lookup"><span data-stu-id="b1dc0-121">Scope of Query</span></span>](scope-of-query.md)
-   [<span data-ttu-id="b1dc0-122">Desempenho e manipulação de grandes conjuntos de resultados</span><span class="sxs-lookup"><span data-stu-id="b1dc0-122">Performance and Handling Large Result Sets</span></span>](performance-and-handling-large-result-sets.md)
-   [<span data-ttu-id="b1dc0-123">Sintaxe do filtro de pesquisa</span><span class="sxs-lookup"><span data-stu-id="b1dc0-123">Search Filter Syntax</span></span>](search-filter-syntax.md)
-   [<span data-ttu-id="b1dc0-124">Interfaces de consulta</span><span class="sxs-lookup"><span data-stu-id="b1dc0-124">Query Interfaces</span></span>](query-interfaces.md)
-   [<span data-ttu-id="b1dc0-125">Pesquisando dados binários</span><span class="sxs-lookup"><span data-stu-id="b1dc0-125">Searching Binary Data</span></span>](searching-binary-data.md)
-   [<span data-ttu-id="b1dc0-126">Consulta Distribuída</span><span class="sxs-lookup"><span data-stu-id="b1dc0-126">Distributed Query</span></span>](distributed-query.md)

 

 




