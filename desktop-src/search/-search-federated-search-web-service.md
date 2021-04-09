---
description: Este tópico descreve as etapas envolvidas na conexão de um serviço Web entre o armazenamento de dados e a pesquisa federada do Windows e como enviar consultas e retornar os resultados da pesquisa em RSS ou Atom.
ms.assetid: 4c8de310-49e6-4d90-a920-0c715351c86a
title: Conectando seu serviço Web na pesquisa federada do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45632d1d3c7b820ab1f39db0896c9f2927b24ccb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090085"
---
# <a name="connecting-your-web-service-in-windows-federated-search"></a><span data-ttu-id="5c1e5-103">Conectando seu serviço Web na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="5c1e5-103">Connecting Your Web Service in Windows Federated Search</span></span>

<span data-ttu-id="5c1e5-104">Este tópico descreve as etapas envolvidas na conexão de um serviço Web entre o armazenamento de dados e a pesquisa federada do Windows e como enviar consultas e retornar os resultados da pesquisa em RSS ou Atom.</span><span class="sxs-lookup"><span data-stu-id="5c1e5-104">This topic describes the steps involved in connecting a web service between your data store and Windows Federated Search, and how to send queries and return search results in RSS or Atom.</span></span>

<span data-ttu-id="5c1e5-105">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="5c1e5-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="5c1e5-106">Conectar seu serviço Web</span><span class="sxs-lookup"><span data-stu-id="5c1e5-106">Connect Your web Service</span></span>](#connect-your-web-service)
-   [<span data-ttu-id="5c1e5-107">Registrar um armazenamento de dados remoto existente</span><span class="sxs-lookup"><span data-stu-id="5c1e5-107">Register an Existing Remote Data Store</span></span>](#register-an-existing-remote-data-store)
-   [<span data-ttu-id="5c1e5-108">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="5c1e5-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="5c1e5-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5c1e5-109">Related topics</span></span>](#related-topics)

## <a name="connect-your-web-service"></a><span data-ttu-id="5c1e5-110">Conectar seu serviço Web</span><span class="sxs-lookup"><span data-stu-id="5c1e5-110">Connect Your web Service</span></span>

<span data-ttu-id="5c1e5-111">**Para conectar o serviço Web do armazenamento de dados à pesquisa federada, execute as seguintes etapas:**</span><span class="sxs-lookup"><span data-stu-id="5c1e5-111">**To connect the web service of your data store to federated search, perform the following steps:**</span></span>

1.  <span data-ttu-id="5c1e5-112">Crie um arquivo. osdx.</span><span class="sxs-lookup"><span data-stu-id="5c1e5-112">Create an .osdx file.</span></span>
2.  <span data-ttu-id="5c1e5-113">Forneça o arquivo. osdx aos usuários para que eles possam adicionar o serviço sob demanda abrindo o arquivo. osdx.</span><span class="sxs-lookup"><span data-stu-id="5c1e5-113">Supply the .osdx file to users so that they can add the service on demand by opening the .osdx file.</span></span>
3.  <span data-ttu-id="5c1e5-114">Gere um conector de pesquisa e implante-o ativamente em sua empresa.</span><span class="sxs-lookup"><span data-stu-id="5c1e5-114">Generate a search connector and actively deploy it in your enterprise.</span></span>

## <a name="register-an-existing-remote-data-store"></a><span data-ttu-id="5c1e5-115">Registrar um armazenamento de dados remoto existente</span><span class="sxs-lookup"><span data-stu-id="5c1e5-115">Register an Existing Remote Data Store</span></span>

<span data-ttu-id="5c1e5-116">Um usuário registra um novo armazenamento de dados remoto com a pesquisa federada do Windows abrindo um arquivo de descrição de OpenSearch (. osdx).</span><span class="sxs-lookup"><span data-stu-id="5c1e5-116">A user registers a new remote data store with Windows Federated Search by opening an OpenSearch Description (.osdx) file.</span></span> <span data-ttu-id="5c1e5-117">Quando o usuário faz isso, ocorrem os seguintes eventos:</span><span class="sxs-lookup"><span data-stu-id="5c1e5-117">When the user does so, the following events occur:</span></span>

1.  <span data-ttu-id="5c1e5-118">Um arquivo. searchconnector-MS (conector de pesquisa) é criado na pasta pesquisas do Windows (% USERPROFILE%/Searches).</span><span class="sxs-lookup"><span data-stu-id="5c1e5-118">A .searchconnector-ms file (search connector) is created in the Windows Searches folder (%userprofile%/Searches).</span></span>
2.  <span data-ttu-id="5c1e5-119">Um atalho para o arquivo. searchconnector-MS é criado na pasta links (% USERPROFILE%/links).</span><span class="sxs-lookup"><span data-stu-id="5c1e5-119">A shortcut to the .searchconnector-ms file is created in the Links folder (%userprofile%/Links).</span></span>
3.  <span data-ttu-id="5c1e5-120">Um atalho é exibido no painel **favoritos** de navegação do Windows Explorer, permitindo que o usuário navegue até o novo armazenamento de dados e consulte o serviço Web.</span><span class="sxs-lookup"><span data-stu-id="5c1e5-120">A shortcut appears in the Windows Explorer navigation **Favorites** pane, enabling the user to navigate into the new data store, and query the web service.</span></span>

> [!Note]  
> <span data-ttu-id="5c1e5-121">Um armazenamento de dados que já tem um serviço Web [OpenSearch](https://github.com/dewitt/opensearch) compatível com a pesquisa federada do Windows pode ser adicionado ao Windows Explorer quando um usuário abre um arquivo. osdx.</span><span class="sxs-lookup"><span data-stu-id="5c1e5-121">A data store that already has an [OpenSearch](https://github.com/dewitt/opensearch) web service that is compatible with Windows Federated Search can be added to Windows Explorer when a user opens an .osdx file.</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="5c1e5-122">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="5c1e5-122">Additional Resources</span></span>

<span data-ttu-id="5c1e5-123">Para obter informações adicionais sobre como implementar a Federação de pesquisa em armazenamentos de dados remotos usando as tecnologias OpenSearch no Windows 7 e versões posteriores, consulte "recursos adicionais" em [pesquisa federada no Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5c1e5-123">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c1e5-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5c1e5-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c1e5-125">Pesquisa federada no Windows</span><span class="sxs-lookup"><span data-stu-id="5c1e5-125">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="5c1e5-126">Introdução com pesquisa federada no Windows</span><span class="sxs-lookup"><span data-stu-id="5c1e5-126">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="5c1e5-127">Habilitando seu armazenamento de dados na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="5c1e5-127">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="5c1e5-128">Criando um arquivo de descrição do OpenSearch na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="5c1e5-128">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="5c1e5-129">Seguindo as práticas recomendadas na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="5c1e5-129">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="5c1e5-130">Implantando conectores de pesquisa na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="5c1e5-130">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 
