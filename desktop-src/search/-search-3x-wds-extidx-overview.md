---
description: Você pode estender o Windows Search para indexar o conteúdo e as propriedades de novos formatos de arquivo e armazenamentos de dados usando interfaces de suplemento de dados.
ms.assetid: 69edf316-77a8-4cc5-9af8-fb89f440c9ea
title: Estender o índice (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a74638dd5366732716335af938c00098cc3991c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765666"
---
# <a name="extending-the-index-windows-search"></a><span data-ttu-id="3c527-103">Estender o índice (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="3c527-103">Extending the Index (Windows Search)</span></span>

<span data-ttu-id="3c527-104">Você pode estender o Windows Search para indexar o conteúdo e as propriedades de novos formatos de arquivo e armazenamentos de dados usando [interfaces de suplemento de dados](./-search-data-addins-interfaces-entry-page.md).</span><span class="sxs-lookup"><span data-stu-id="3c527-104">You can extend Windows Search to index the contents and properties of new file formats, and data stores using [data add-in interfaces](./-search-data-addins-interfaces-entry-page.md).</span></span> <span data-ttu-id="3c527-105">Para criar suplementos de pesquisa do Windows, os desenvolvedores de terceiros devem primeiro implementar um armazenamento de dados do Shell e, em seguida, desenvolver um manipulador de protocolo para que o Windows Search possa acessar os dados para indexação.</span><span class="sxs-lookup"><span data-stu-id="3c527-105">To create Windows Search add-ins, third-party developers must first implement a Shell data store, and then develop a protocol handler so that Windows Search can access the data for indexing.</span></span> <span data-ttu-id="3c527-106">Se você tiver um formato de arquivo personalizado, deverá desenvolver um manipulador de filtro para indexar o conteúdo do arquivo e um manipulador de propriedades para cada tipo de arquivo para indexar Propriedades.</span><span class="sxs-lookup"><span data-stu-id="3c527-106">If you have a custom file format, you must develop a filter handler to index file contents, and a property handler for every file type to index properties.</span></span>

<span data-ttu-id="3c527-107">A pesquisa do Windows atualmente dá suporte à indexação de mais de 200 tipos de itens (como. txt,. html e formatos de arquivo. xml) e pode trabalhar com vários tipos de armazenamentos de dados (como o sistema de arquivos NTFS e o Microsoft Outlook).</span><span class="sxs-lookup"><span data-stu-id="3c527-107">Windows Search currently supports the indexing of over 200 types of items (such as .txt, .html, and .xml file formats) and can work with multiple types of data stores (such as the NTFS file system and Microsoft Outlook).</span></span> <span data-ttu-id="3c527-108">O Windows Search usa a tecnologia de filtro e manipulador de protocolo semelhante ao SharePoint Server.</span><span class="sxs-lookup"><span data-stu-id="3c527-108">Windows Search uses filter and protocol handler technology similar to SharePoint Server.</span></span> <span data-ttu-id="3c527-109">Portanto, se você já tiver implementações para o formato de arquivo, poderá atualizar as implementações a serem inicializadas com um fluxo usando [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) para que o filtro funcione com o Windows Search.</span><span class="sxs-lookup"><span data-stu-id="3c527-109">Hence, if you already have implementations for your file format, you can update the implementations to be initialized with a stream by using [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) so that the filter will work with Windows Search.</span></span>

> [!Note]  
> <span data-ttu-id="3c527-110">Manipuladores de filtro, manipuladores de propriedade e manipuladores de protocolo devem ser escritos em código nativo.</span><span class="sxs-lookup"><span data-stu-id="3c527-110">Filter handlers, property handlers, and protocol handlers must be written in native code.</span></span> <span data-ttu-id="3c527-111">Isso ocorre devido a possíveis problemas de controle de versão de Common Language Runtime (CLR) com o processo em que vários suplementos são executados.</span><span class="sxs-lookup"><span data-stu-id="3c527-111">This is due to potential common language runtime (CLR) versioning issues with the process that multiple add-ins run in.</span></span>

 

<span data-ttu-id="3c527-112">Esta seção sobre como estender o índice com suplementos contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="3c527-112">This section on extending the index with add-ins contains the following topics:</span></span>

-   [<span data-ttu-id="3c527-113">Desenvolvendo manipuladores de filtro</span><span class="sxs-lookup"><span data-stu-id="3c527-113">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)
-   [<span data-ttu-id="3c527-114">Desenvolvendo manipuladores de propriedade para o Windows Search</span><span class="sxs-lookup"><span data-stu-id="3c527-114">Developing Property Handlers for Windows Search</span></span>](-search-3x-wds-extidx-propertyhandlers.md)
-   [<span data-ttu-id="3c527-115">Desenvolvendo manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="3c527-115">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)

## <a name="additional-resources"></a><span data-ttu-id="3c527-116">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="3c527-116">Additional Resources</span></span>

<span data-ttu-id="3c527-117">Para obter exemplos de código relacionados, consulte [exemplos de código do Windows Search](-search-samples-ovw.md).</span><span class="sxs-lookup"><span data-stu-id="3c527-117">For related code samples, see [Windows Search Code Samples](-search-samples-ovw.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c527-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3c527-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c527-119">Guia de desenvolvimento do Windows Search</span><span class="sxs-lookup"><span data-stu-id="3c527-119">Windows Search Development Guide</span></span>](-search-developers-guide-entry-page.md)
</dt> <dt>

[<span data-ttu-id="3c527-120">Gerenciar o índice</span><span class="sxs-lookup"><span data-stu-id="3c527-120">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[<span data-ttu-id="3c527-121">Consulta do índice de maneira programática</span><span class="sxs-lookup"><span data-stu-id="3c527-121">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="3c527-122">Estendendo recursos de idioma</span><span class="sxs-lookup"><span data-stu-id="3c527-122">Extending Language Resources</span></span>](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
