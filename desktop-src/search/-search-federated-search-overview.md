---
description: O suporte do Windows 7 para a Federação de pesquisa para armazenamentos de dados remotos usando tecnologias OpenSearch permite que os usuários acessem e interajam com seus dados remotos no Windows Explorer.
ms.assetid: 2014b7ac-4885-4f17-b6d4-5fd95872ed59
title: Pesquisa federada no Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7d7718bb5215072ceeb8786f5728017ed329e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460988"
---
# <a name="federated-search-in-windows"></a><span data-ttu-id="be1b9-103">Pesquisa federada no Windows</span><span class="sxs-lookup"><span data-stu-id="be1b9-103">Federated Search in Windows</span></span>

<span data-ttu-id="be1b9-104">O suporte do Windows 7 para a Federação de pesquisa para armazenamentos de dados remotos usando tecnologias OpenSearch permite que os usuários acessem e interajam com seus dados remotos no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="be1b9-104">Windows 7 support for search federation to remote data stores using OpenSearch technologies enables users to access and interact with their remote data from within Windows Explorer.</span></span>

<span data-ttu-id="be1b9-105">A lista de tópicos a seguir descreve como você pode criar um armazenamento de dados baseado na Web que pode ser pesquisado usando a pesquisa federada do Windows e habilitar a integração rica de suas fontes de dados remotas com o Windows Explorer sem precisar escrever ou implantar qualquer código do lado do cliente do Windows.</span><span class="sxs-lookup"><span data-stu-id="be1b9-105">The following list of topics describe how you can build a web-based data store that can be searched using Windows federated search, and enable rich integration of your remote data sources with Windows Explorer without having to write or deploy any Windows client-side code.</span></span>

-   [<span data-ttu-id="be1b9-106">Introdução com pesquisa federada no Windows</span><span class="sxs-lookup"><span data-stu-id="be1b9-106">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
-   [<span data-ttu-id="be1b9-107">Conectando seu serviço Web na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="be1b9-107">Connecting Your Web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
-   [<span data-ttu-id="be1b9-108">Habilitando seu armazenamento de dados na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="be1b9-108">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
-   [<span data-ttu-id="be1b9-109">Criando um arquivo de descrição do OpenSearch na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="be1b9-109">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
-   [<span data-ttu-id="be1b9-110">Seguindo as práticas recomendadas na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="be1b9-110">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
-   [<span data-ttu-id="be1b9-111">Implantando conectores de pesquisa na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="be1b9-111">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
-   [<span data-ttu-id="be1b9-112">Esquema de descrição do conector de pesquisa</span><span class="sxs-lookup"><span data-stu-id="be1b9-112">Search Connector Description Schema</span></span>](search-sconn-desc-schema-entry.md)

## <a name="additional-resources"></a><span data-ttu-id="be1b9-113">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="be1b9-113">Additional Resources</span></span>

-   <span data-ttu-id="be1b9-114">O exemplo de código [OpenSearch](-search-sample-opensearch.md) demonstra como criar um serviço de pesquisa federado usando o protocolo [OpenSearch](https://github.com/dewitt/opensearch) e um arquivo de descritor de OpenSearch (. osdx) (um conector de pesquisa).</span><span class="sxs-lookup"><span data-stu-id="be1b9-114">The [OpenSearch](-search-sample-opensearch.md) code sample demonstrates how to create a federated search service using the [OpenSearch](https://github.com/dewitt/opensearch) protocol, and an OpenSearch Descriptor (.osdx) file (a search connector).</span></span>
-   <span data-ttu-id="be1b9-115">Para uma demonstração em vídeo de criação de um serviço Web de [OpenSearch](https://github.com/dewitt/opensearch) para um banco de dados SQL, consulte [Windows 7: capacitar os usuários a localizar, Visualizar e organizar seus dados com bibliotecas e o Gerenciador](https://channel9.msdn.com/pdc2008/PC16/).</span><span class="sxs-lookup"><span data-stu-id="be1b9-115">For a video demonstration of creating an [OpenSearch](https://github.com/dewitt/opensearch) web service for a SQL database, see [Windows 7: Empower Users to Find, Visualize and Organize their Data with Libraries and the Explorer](https://channel9.msdn.com/pdc2008/PC16/).</span></span>
-   <span data-ttu-id="be1b9-116">Se você estiver gravando um provedor de [OpenSearch](https://github.com/dewitt/opensearch) do lado do cliente, consulte:</span><span class="sxs-lookup"><span data-stu-id="be1b9-116">If you are writing a client-side [OpenSearch](https://github.com/dewitt/opensearch) provider, see:</span></span>
    -   <span data-ttu-id="be1b9-117">O [desenvolvedor de OpenSearch como guiar](https://github.com/dewitt/opensearch/blob/master/mediawiki/Documentation/Developer%20how%20to%20guide.wiki) para obter mais informações sobre como se conectar a um provedor do lado do cliente usando os protocolos ou as APIs de um repositório de dados proprietário.</span><span class="sxs-lookup"><span data-stu-id="be1b9-117">The [OpenSearch Developer How To Guide](https://github.com/dewitt/opensearch/blob/master/mediawiki/Documentation/Developer%20how%20to%20guide.wiki) for more information on connecting to a client-side provider by using a proprietary data store's protocols or APIs.</span></span>
    -   <span data-ttu-id="be1b9-118">A [visão geral da documentação de](search-sconn-desc-schema-entry.md) esquema do esquema de descrição do conector de pesquisa (. searchconnector-MS).</span><span class="sxs-lookup"><span data-stu-id="be1b9-118">The [Overview of the Search Connector Description Schema](search-sconn-desc-schema-entry.md) (.searchconnector-ms) schema documentation.</span></span>
-   <span data-ttu-id="be1b9-119">Consulte o site do [centro de download da Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx) para obter o seguinte recurso para download: search Server 2008 Sample: Federated Search Connector Sample.</span><span class="sxs-lookup"><span data-stu-id="be1b9-119">See the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) website for the following downloadable resource: Search Server 2008 Sample: Federated Search Connector Sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be1b9-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="be1b9-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be1b9-121">Visão geral do Windows Search</span><span class="sxs-lookup"><span data-stu-id="be1b9-121">Windows Search Overview</span></span>](-search-3x-wds-overview.md)
</dt> <dt>

[<span data-ttu-id="be1b9-122">Guia do desenvolvedor do Windows Search</span><span class="sxs-lookup"><span data-stu-id="be1b9-122">Windows Search Developer's Guide</span></span>](-search-developers-guide-entry-page.md)
</dt> <dt>

[<span data-ttu-id="be1b9-123">Referência do Windows Search</span><span class="sxs-lookup"><span data-stu-id="be1b9-123">Windows Search Reference</span></span>](-search-reference-entry-page.md)
</dt> <dt>

[<span data-ttu-id="be1b9-124">Exemplos de código do Windows Search</span><span class="sxs-lookup"><span data-stu-id="be1b9-124">Windows Search Code Samples</span></span>](-search-samples-ovw.md)
</dt> <dt>

[<span data-ttu-id="be1b9-125">Tecnologias de pesquisa relacionadas</span><span class="sxs-lookup"><span data-stu-id="be1b9-125">Related Search Technologies</span></span>](-search-3x-wds-sampleentry.md)
</dt> <dt>

[<span data-ttu-id="be1b9-126">Glossário do Windows Search</span><span class="sxs-lookup"><span data-stu-id="be1b9-126">Windows Search Glossary</span></span>](search-glossary.md)
</dt> </dl>

 

 



