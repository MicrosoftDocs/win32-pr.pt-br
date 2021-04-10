---
description: O SDK do Windows Search fornece um assembly de interoperabilidade para que você trabalhe com objetos Component Object Model (COM) expostos pelo Windows Search e outros programas em relação às interfaces e classes usando código gerenciado.
ms.assetid: 9ade6f55-de65-4f73-9d22-1be819549704
title: Usar código gerenciado com os dados do Shell e do Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0a4c0f4182739fe553c21b45bcfc3a3af7a68f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090100"
---
# <a name="using-managed-code-with-shell-data-and-windows-search"></a><span data-ttu-id="ce152-103">Usar código gerenciado com os dados do Shell e do Windows Search</span><span class="sxs-lookup"><span data-stu-id="ce152-103">Using Managed Code with Shell Data and Windows Search</span></span>

<span data-ttu-id="ce152-104">O SDK do Windows Search fornece um assembly de interoperabilidade para que você trabalhe com objetos Component Object Model (COM) expostos pelo Windows Search e outros programas em relação às interfaces e classes usando código gerenciado.</span><span class="sxs-lookup"><span data-stu-id="ce152-104">The Windows Search SDK provides an interopability assembly for you to work with Component Object Model (COM) objects that are exposed by Windows Search and other programs against the interfaces and classes using managed code.</span></span> <span data-ttu-id="ce152-105">O assembly de interoperabilidade é assinado digitalmente pela Microsoft e pode ser encontrado com os [exemplos do Windows Search](-search-samples-ovw.md).</span><span class="sxs-lookup"><span data-stu-id="ce152-105">The interopability assembly is digitally signed by Microsoft and can be found with the [Windows Search samples](-search-samples-ovw.md).</span></span>

<span data-ttu-id="ce152-106">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="ce152-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="ce152-107">Usando a API do Windows CodePack</span><span class="sxs-lookup"><span data-stu-id="ce152-107">Using the Windows API CodePack</span></span>](#using-the-windows-api-codepack)
    -   [<span data-ttu-id="ce152-108">Acessando resultados de índice</span><span class="sxs-lookup"><span data-stu-id="ce152-108">Accessing Index Results</span></span>](#accessing-index-results)
    -   [<span data-ttu-id="ce152-109">Aplicativo de exemplo usando a API do Windows Codepack</span><span class="sxs-lookup"><span data-stu-id="ce152-109">Sample Application Using the Windows API Codepack</span></span>](#sample-application-using-the-windows-api-codepack)
-   [<span data-ttu-id="ce152-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ce152-110">Related topics</span></span>](#related-topics)

## <a name="using-the-windows-api-codepack"></a><span data-ttu-id="ce152-111">Usando a API do Windows CodePack</span><span class="sxs-lookup"><span data-stu-id="ce152-111">Using the Windows API CodePack</span></span>

<span data-ttu-id="ce152-112">Se você estiver trabalhando no ambiente de Microsoft .NET, use o [pacote de código da API do Windows para Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) para obter resultados da pesquisa ou apenas procure o namespace.</span><span class="sxs-lookup"><span data-stu-id="ce152-112">If you are working in the Microsoft .NET environment, use the [Windows API Code Pack for Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) to obtain search results, or just browse the namespace.</span></span> <span data-ttu-id="ce152-113">O [pacote de códigos da API do Windows para Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) fornece uma coleção de itens de shell que são essencialmente invólucros em relação à [interface IShellItem](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellitem)nativa.</span><span class="sxs-lookup"><span data-stu-id="ce152-113">The [Windows API Code Pack for Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) provides you with a collection of Shell items that are essentially wrappers around the native [IShellItem Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellitem).</span></span> <span data-ttu-id="ce152-114">Você pode iterar sobre essa coleção e obter os vários valores de propriedade de maneira semelhante a como você enumeraria os resultados em uma tabela de uma consulta de vinculação de objeto e de banco de dados de incorporação (OLE DB).</span><span class="sxs-lookup"><span data-stu-id="ce152-114">You can iterate over this collection and get the various property values in a fashion similar to how you would enumerate the results in a table from an Object Linking and Embedding Database (OLE DB) query.</span></span>

<span data-ttu-id="ce152-115">O trecho de código a seguir ilustra como iterar em itens de pesquisa e obter os valores de propriedade para cada um.</span><span class="sxs-lookup"><span data-stu-id="ce152-115">The following code snippet illustrates how to iterate over Search items and obtain the property values for each.</span></span>


```
foreach (ShellObject so in KnownFolders.SavedSearches)
{
    searchFolder = new ShellSearchFolder(finalSearchCondition, (ShellContainer)so);
    List<ShellObject> items = new List<ShellObject>();
    foreach (ShellObject so2 in searchFolder) items.Add(so2);   
}
```



### <a name="accessing-index-results"></a><span data-ttu-id="ce152-116">Acessando resultados de índice</span><span class="sxs-lookup"><span data-stu-id="ce152-116">Accessing Index Results</span></span>

<span data-ttu-id="ce152-117">Você pode acessar os resultados do índice por meio de OLE DB ou do modelo de dados do Shell.</span><span class="sxs-lookup"><span data-stu-id="ce152-117">You can access index results through either OLE DB or the Shell data model.</span></span> <span data-ttu-id="ce152-118">Há vantagens e desvantagens com qualquer abordagem.</span><span class="sxs-lookup"><span data-stu-id="ce152-118">There are advantages and disadvantages with either approach.</span></span> <span data-ttu-id="ce152-119">Uma vantagem é que OLE DB e linguagem SQL (SQL) são familiares aos programadores de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ce152-119">One advantage is that OLE DB and Structured Query Language (SQL) are familiar to database programmers.</span></span> <span data-ttu-id="ce152-120">Outras vantagens são um melhor controle sobre o desempenho ao consultar apenas o indexador e o acesso a funcionalidades adicionais, como a capacidade de localizar resultados anteriores em um novo conjunto de linhas rapidamente.</span><span class="sxs-lookup"><span data-stu-id="ce152-120">Other advantages are better control over performance when querying only the indexer, and access to additional functionality such as the ability to locate previous results in a new rowset quickly.</span></span>

<span data-ttu-id="ce152-121">As vantagens do modelo de dados do shell são que elas são abstratas em diferentes fontes de informações, como OpenSearch, e fornecem acesso a funcionalidades adicionais, como miniaturas e manipuladores de propriedades.</span><span class="sxs-lookup"><span data-stu-id="ce152-121">Advantages of the Shell data model are that it abstracts across different sources of information such as OpenSearch, and provides access to additional functionality such as thumbnails and property handlers.</span></span> <span data-ttu-id="ce152-122">Nem o modelo de objeto do Shell requer suporte de caso especial para resultados que não sejam de nome de arquivo, como itens de email e resultados do OneNote, nem para qualquer item que resida no índice do usuário.</span><span class="sxs-lookup"><span data-stu-id="ce152-122">Nor does the Shell object model require special case support for non-filename results such as mail items and OneNote results, nor for any item that resides in the user's index.</span></span> <span data-ttu-id="ce152-123">Observe que no Shell [KNOWNFOLDERID](../shell/knownfolderid.md) é o escopo de pasta conhecido para conteúdo indexado local.</span><span class="sxs-lookup"><span data-stu-id="ce152-123">Note that in Shell [KNOWNFOLDERID](../shell/knownfolderid.md) is the known folder scope for local indexed content.</span></span> <span data-ttu-id="ce152-124">Para obter mais informações sobre como criar uma fonte de dados do Shell, consulte [implementando as interfaces de objeto de pasta básica](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ce152-124">For more information on creating a Shell data source, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

<span data-ttu-id="ce152-125">As fontes de dados OpenSearch não são expostas por meio de OLE DB para pesquisa federada no Windows 7 e posterior.</span><span class="sxs-lookup"><span data-stu-id="ce152-125">OpenSearch data sources are not exposed through OLE DB for federated search in Windows 7 and later.</span></span> <span data-ttu-id="ce152-126">Por esse motivo, recomendamos que você considere escrever um provedor LINQ para o namespace do Shell em vez de usar OLE DB para acessar os resultados do indexador.</span><span class="sxs-lookup"><span data-stu-id="ce152-126">For this reason we recommend that you consider writing a LINQ provider for the Shell namespace instead of using OLE DB to access the indexer results.</span></span> <span data-ttu-id="ce152-127">Para obter mais informações, consulte [Walkthrough: Criando um provedor de LINQ do IQueryable](/previous-versions/bb546158(v=vs.140)).</span><span class="sxs-lookup"><span data-stu-id="ce152-127">For more information, see [Walkthrough: Creating an IQueryable LINQ Provider](/previous-versions/bb546158(v=vs.140)).</span></span>

### <a name="sample-application-using-the-windows-api-codepack"></a><span data-ttu-id="ce152-128">Aplicativo de exemplo usando a API do Windows Codepack</span><span class="sxs-lookup"><span data-stu-id="ce152-128">Sample Application Using the Windows API Codepack</span></span>

<span data-ttu-id="ce152-129">A captura de tela a seguir representa uma simulação de um aplicativo de exemplo criado com o [pacote de códigos de API do Windows para Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility).</span><span class="sxs-lookup"><span data-stu-id="ce152-129">The following screenshot represents a mock up of a sample application created with the [Windows API Code Pack for Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility).</span></span>

![captura de tela do aplicativo player de mídia mostrando mensagens de email](images/folderid-searchhome.png)

## <a name="related-topics"></a><span data-ttu-id="ce152-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ce152-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ce152-132">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="ce152-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ce152-133">Pesquisa federada no Windows</span><span class="sxs-lookup"><span data-stu-id="ce152-133">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

<span data-ttu-id="ce152-134">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="ce152-134">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="ce152-135">[Interoperabilidade em qualquer idioma](/previous-versions/dotnet/netframework-1.1/730f1wy3(v=vs.71))</span><span class="sxs-lookup"><span data-stu-id="ce152-135">[Cross-Language Interoperability](/previous-versions/dotnet/netframework-1.1/730f1wy3(v=vs.71))</span></span>
</dt> </dl>

 

 
