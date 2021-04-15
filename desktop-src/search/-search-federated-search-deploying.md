---
description: Este tópico explica como um usuário registra um novo armazenamento de dados remoto com pesquisa federada abrindo um arquivo de descrição de OpenSearch (. osdx), como implantar um arquivo. osdx e como acompanhar o uso do serviço OpenSearch.
ms.assetid: 9db0f970-4e17-492b-ab75-a8b0f8011d0a
title: Implantar conectores de pesquisa na pesquisa federada do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a870169cd6cca3537327a8631a15d61da78eb6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460989"
---
# <a name="deploying-search-connectors-in-windows-federated-search"></a><span data-ttu-id="becb2-103">Implantando conectores de pesquisa na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="becb2-103">Deploying Search Connectors in Windows Federated Search</span></span>

<span data-ttu-id="becb2-104">Este tópico explica como um usuário registra um novo armazenamento de dados remoto com pesquisa federada abrindo um arquivo de descrição de OpenSearch (. osdx), como implantar um arquivo. osdx e como acompanhar o uso do serviço [OpenSearch](https://github.com/dewitt/opensearch) .</span><span class="sxs-lookup"><span data-stu-id="becb2-104">This topic explains how a user registers a new remote data store with federated search by opening an OpenSearch Description (.osdx) file, how to deploy an .osdx file, and how to track usage of your [OpenSearch](https://github.com/dewitt/opensearch) service.</span></span>

<span data-ttu-id="becb2-105">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="becb2-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="becb2-106">O arquivo. searchconnector-MS (conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="becb2-106">The .searchconnector-ms (Search Connector) File</span></span>](#the-searchconnector-ms-search-connector-file)
-   [<span data-ttu-id="becb2-107">Métodos de implantação</span><span class="sxs-lookup"><span data-stu-id="becb2-107">Deployment Methods</span></span>](#deployment-methods)
    -   [<span data-ttu-id="becb2-108">Implantação de pull</span><span class="sxs-lookup"><span data-stu-id="becb2-108">Pull Deployment</span></span>](#pull-deployment)
    -   [<span data-ttu-id="becb2-109">Implantação por push</span><span class="sxs-lookup"><span data-stu-id="becb2-109">Push Deployment</span></span>](#push-deployment)
-   [<span data-ttu-id="becb2-110">Controlando o uso</span><span class="sxs-lookup"><span data-stu-id="becb2-110">Tracking Usage</span></span>](#tracking-usage)
-   [<span data-ttu-id="becb2-111">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="becb2-111">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="becb2-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="becb2-112">Related topics</span></span>](#related-topics)

## <a name="the-searchconnector-ms-search-connector-file"></a><span data-ttu-id="becb2-113">O arquivo. searchconnector-MS (conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="becb2-113">The .searchconnector-ms (Search Connector) File</span></span>

<span data-ttu-id="becb2-114">Simplesmente abrir o arquivo. osdx que descreve como se conectar ao serviço Web e como mapear quaisquer elementos personalizados em seu RSS ou Atom XML registra seu novo armazenamento de dados remoto com pesquisa federada.</span><span class="sxs-lookup"><span data-stu-id="becb2-114">Merely opening the .osdx file that describes how to connect to the web service and how to map any custom elements in your RSS or Atom XML registers your new remote data store with federated search.</span></span> <span data-ttu-id="becb2-115">Um armazenamento de dados que já tem um serviço Web do [OpenSearch](https://github.com/dewitt/opensearch) compatível com a pesquisa federada pode ser adicionado ao Windows Explorer quando um usuário abre um arquivo. osdx.</span><span class="sxs-lookup"><span data-stu-id="becb2-115">A data store that already has an [OpenSearch](https://github.com/dewitt/opensearch) web service that is compatible with federated search can be added to Windows Explorer when a user opens an .osdx file.</span></span>

<span data-ttu-id="becb2-116">Depois de ter dado o. osdx ao usuário e o usuário abrir o arquivo. osdx, os eventos a seguir ocorrerão.</span><span class="sxs-lookup"><span data-stu-id="becb2-116">After you have given the .osdx to your user and the user opens the .osdx file, the following events occur.</span></span>

1.  <span data-ttu-id="becb2-117">Um arquivo. searchconnector-MS é criado na pasta **pesquisas do Windows** (% USERPROFILE%/Searches).</span><span class="sxs-lookup"><span data-stu-id="becb2-117">A .searchconnector-ms file is created in the **Windows Searches** folder (%userprofile%/Searches).</span></span>
2.  <span data-ttu-id="becb2-118">Um atalho para o arquivo. searchconnector-MS é criado na pasta **links** (% USERPROFILE%/links).</span><span class="sxs-lookup"><span data-stu-id="becb2-118">A shortcut to the .searchconnector-ms file is created in the **Links** folder (%userprofile%/Links).</span></span>
3.  <span data-ttu-id="becb2-119">Um atalho é exibido no painel **favoritos** de navegação do Windows Explorer, permitindo que o usuário navegue até o novo repositório de dados e consulte o serviço Web.</span><span class="sxs-lookup"><span data-stu-id="becb2-119">A shortcut appears in the Windows Explorer navigation **Favorites** pane, enabling the user to navigate into the new data store and query the web service.</span></span>

## <a name="deployment-methods"></a><span data-ttu-id="becb2-120">Métodos de implantação</span><span class="sxs-lookup"><span data-stu-id="becb2-120">Deployment Methods</span></span>

<span data-ttu-id="becb2-121">Há duas maneiras de implantar conectores de pesquisa, implantação de pull e implantação por push.</span><span class="sxs-lookup"><span data-stu-id="becb2-121">There are two ways to deploy search connectors, pull deployment and push deployment.</span></span>

### <a name="pull-deployment"></a><span data-ttu-id="becb2-122">Implantação de pull</span><span class="sxs-lookup"><span data-stu-id="becb2-122">Pull Deployment</span></span>

<span data-ttu-id="becb2-123">A implantação de pull descreve qualquer tipo de implantação na qual o usuário final usa a iniciativa para instalar os conectores de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="becb2-123">Pull deployment describes any type of deployment in which the end user takes the initiative to install the search connectors.</span></span> <span data-ttu-id="becb2-124">Os métodos comuns de implantação pull são:</span><span class="sxs-lookup"><span data-stu-id="becb2-124">Common methods of pull deployment are:</span></span>

-   <span data-ttu-id="becb2-125">Anexando o arquivo. osdx em um email.</span><span class="sxs-lookup"><span data-stu-id="becb2-125">Attaching the .osdx file in an email.</span></span>
-   <span data-ttu-id="becb2-126">Postando o arquivo em uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="becb2-126">Posting the file on a webpage.</span></span>
-   <span data-ttu-id="becb2-127">Fornecendo um link dinâmico no site da intranet; por exemplo, um que gera arquivos. osdx personalizados com base nas opções do usuário ou no escopo atual no site.</span><span class="sxs-lookup"><span data-stu-id="becb2-127">Providing a dynamic link on your intranet site; for example, one that generates custom .osdx files based on user choices or the current scope within the site.</span></span>

<span data-ttu-id="becb2-128">Para o arquivo a ser baixado quando o usuário clica no link em seu navegador, o servidor Web que hospeda o serviço Web deve ser configurado para entregar o. osdx como um arquivo.</span><span class="sxs-lookup"><span data-stu-id="becb2-128">For the file to be downloaded when the user clicks the link in their browser, the web server hosting the web service must be configured to deliver the .osdx as a file.</span></span> <span data-ttu-id="becb2-129">Portanto, você deve configurar os tipos MIME no servidor Web para tratar arquivos. osdx como `"application/opensearchdescription+xml"` .</span><span class="sxs-lookup"><span data-stu-id="becb2-129">Hence, you must configure the MIME Types on the web server to treat .osdx files as `"application/opensearchdescription+xml"`.</span></span> <span data-ttu-id="becb2-130">Opcionalmente, você pode usar o ícone fornecido pela Microsoft para identificar o link do conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="becb2-130">Optionally, you can use the icon supplied by Microsoft to identify search connector link.</span></span>

### <a name="push-deployment"></a><span data-ttu-id="becb2-131">Implantação por push</span><span class="sxs-lookup"><span data-stu-id="becb2-131">Push Deployment</span></span>

<span data-ttu-id="becb2-132">A implantação por push descreve qualquer tipo de implantação que não depende da iniciativa de usuário para instalar os conectores de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="becb2-132">Push deployment describes any type of deployment that does not depend on user initiative to install the search connectors.</span></span> <span data-ttu-id="becb2-133">Os métodos comuns de implantação por push são:</span><span class="sxs-lookup"><span data-stu-id="becb2-133">Common methods of push deployment are:</span></span>

-   <span data-ttu-id="becb2-134">Preferências de Política de Grupo (GPP)</span><span class="sxs-lookup"><span data-stu-id="becb2-134">Group Policy Preferences (GPP)</span></span>
-   <span data-ttu-id="becb2-135">Script de logon</span><span class="sxs-lookup"><span data-stu-id="becb2-135">Logon script</span></span>
-   <span data-ttu-id="becb2-136">Perfis móveis</span><span class="sxs-lookup"><span data-stu-id="becb2-136">Roaming profiles</span></span>
-   <span data-ttu-id="becb2-137">Geração de imagens</span><span class="sxs-lookup"><span data-stu-id="becb2-137">Imaging</span></span>

## <a name="tracking-usage"></a><span data-ttu-id="becb2-138">Controlando o uso</span><span class="sxs-lookup"><span data-stu-id="becb2-138">Tracking Usage</span></span>

<span data-ttu-id="becb2-139">Para acompanhar o uso do serviço [OpenSearch](https://github.com/dewitt/opensearch) por usuários pesquisando no Windows Explorer, filtre os arquivos de log do servidor Web para esta cadeia de caracteres do agente do usuário: `Windows-Search+(Windows+NT+6.1)` .</span><span class="sxs-lookup"><span data-stu-id="becb2-139">To track the usage of your [OpenSearch](https://github.com/dewitt/opensearch) service by users searching from Windows Explorer, filter your web server log files for this user agent string: `Windows-Search+(Windows+NT+6.1)`.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="becb2-140">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="becb2-140">Additional Resources</span></span>

<span data-ttu-id="becb2-141">Para obter informações adicionais sobre como implementar a Federação de pesquisa em armazenamentos de dados remotos usando as tecnologias OpenSearch no Windows 7 e versões posteriores, consulte "recursos adicionais" em [pesquisa federada no Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="becb2-141">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="becb2-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="becb2-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="becb2-143">Pesquisa federada no Windows</span><span class="sxs-lookup"><span data-stu-id="becb2-143">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="becb2-144">Introdução com pesquisa federada no Windows</span><span class="sxs-lookup"><span data-stu-id="becb2-144">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="becb2-145">Conectando seu serviço Web na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="becb2-145">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="becb2-146">Habilitando seu armazenamento de dados na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="becb2-146">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="becb2-147">Criando um arquivo de descrição do OpenSearch na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="becb2-147">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="becb2-148">Seguindo as práticas recomendadas na pesquisa federada do Windows</span><span class="sxs-lookup"><span data-stu-id="becb2-148">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> </dl>

 

 
