---
title: Funções da API do servidor HTTP versão 1,0
description: A API do servidor HTTP fornece as seguintes funções para gravar aplicativos.
ms.assetid: 1da9907d-a09d-41e1-aca1-9a8e2b91296f
keywords:
- Funções da API do servidor HTTP versão 1,0
- Funções HTTP, API do servidor HTTP versão 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050821e40695268d6e3fa2c946d2e8859748db2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160252"
---
# <a name="http-server-api-version-10-functions"></a><span data-ttu-id="d6814-105">Funções da API do servidor HTTP versão 1,0</span><span class="sxs-lookup"><span data-stu-id="d6814-105">HTTP Server API Version 1.0 Functions</span></span>

<span data-ttu-id="d6814-106">A API do servidor HTTP fornece as seguintes funções para gravar aplicativos.</span><span class="sxs-lookup"><span data-stu-id="d6814-106">The HTTP Server API provides the following functions for writing applications.</span></span>

## <a name="general"></a><span data-ttu-id="d6814-107">Geral</span><span class="sxs-lookup"><span data-stu-id="d6814-107">General</span></span>



| <span data-ttu-id="d6814-108">Função</span><span class="sxs-lookup"><span data-stu-id="d6814-108">Function</span></span>                                             | <span data-ttu-id="d6814-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6814-109">Description</span></span>                                                                                                                       |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6814-110">**HttpCreateHttpHandle**</span><span class="sxs-lookup"><span data-stu-id="d6814-110">**HttpCreateHttpHandle**</span></span>](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) | <span data-ttu-id="d6814-111">Cria uma fila de solicitação HTTP e retorna um identificador a ela.</span><span class="sxs-lookup"><span data-stu-id="d6814-111">Creates an HTTP request queue and returns a handle to it.</span></span>                                                                         |
| [<span data-ttu-id="d6814-112">**HttpInitialize**</span><span class="sxs-lookup"><span data-stu-id="d6814-112">**HttpInitialize**</span></span>](/windows/desktop/api/Http/nf-http-httpinitialize)             | <span data-ttu-id="d6814-113">Inicializa a API do servidor HTTP para uso pelo processo de chamada.</span><span class="sxs-lookup"><span data-stu-id="d6814-113">Initializes the HTTP Server API for use by the calling process.</span></span>                                                                   |
| [<span data-ttu-id="d6814-114">**HttpPrepareUrl**</span><span class="sxs-lookup"><span data-stu-id="d6814-114">**HttpPrepareUrl**</span></span>](/windows/desktop/api/Http/nf-http-httpprepareurl)             | <span data-ttu-id="d6814-115">Analisa, analisa e normaliza uma URL Unicode ou Punycode não normalizada para que seja segura e válida para uso em outras funções HTTP.</span><span class="sxs-lookup"><span data-stu-id="d6814-115">Parses, analyzes, and normalizes a non-normalized Unicode or punycode URL so it is safe and valid to use in other HTTP functions.</span></span> |
| [<span data-ttu-id="d6814-116">**HttpTerminate**</span><span class="sxs-lookup"><span data-stu-id="d6814-116">**HttpTerminate**</span></span>](/windows/desktop/api/Http/nf-http-httpterminate)               | <span data-ttu-id="d6814-117">Direciona a API do servidor HTTP para limpar todos os recursos associados a um processo específico.</span><span class="sxs-lookup"><span data-stu-id="d6814-117">Directs the HTTP Server API to clean up any resources associated with a particular process.</span></span>                                       |



 

## <a name="cache-management"></a><span data-ttu-id="d6814-118">Gerenciamento de cache</span><span class="sxs-lookup"><span data-stu-id="d6814-118">Cache Management</span></span>



| <span data-ttu-id="d6814-119">Função</span><span class="sxs-lookup"><span data-stu-id="d6814-119">Function</span></span>                                                       | <span data-ttu-id="d6814-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6814-120">Description</span></span>                                                                                            |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6814-121">**HttpAddFragmentToCache**</span><span class="sxs-lookup"><span data-stu-id="d6814-121">**HttpAddFragmentToCache**</span></span>](/windows/desktop/api/Http/nf-http-httpaddfragmenttocache)       | <span data-ttu-id="d6814-122">Armazena em cache um fragmento de dados para que ele possa ser usado para compor uma resposta dinâmica sem ler do disco.</span><span class="sxs-lookup"><span data-stu-id="d6814-122">Caches a data fragment so that it can be used to compose a dynamic response without reading from disk.</span></span> |
| [<span data-ttu-id="d6814-123">**HttpFlushResponseCache**</span><span class="sxs-lookup"><span data-stu-id="d6814-123">**HttpFlushResponseCache**</span></span>](/windows/desktop/api/Http/nf-http-httpflushresponsecache)       | <span data-ttu-id="d6814-124">Remove os fragmentos em cache especificados do cache HTTP.</span><span class="sxs-lookup"><span data-stu-id="d6814-124">Removes specified cached fragments from the HTTP cache.</span></span>                                                |
| [<span data-ttu-id="d6814-125">**HttpReadFragmentFromCache**</span><span class="sxs-lookup"><span data-stu-id="d6814-125">**HttpReadFragmentFromCache**</span></span>](/windows/desktop/api/Http/nf-http-httpreadfragmentfromcache) | <span data-ttu-id="d6814-126">Recupera um fragmento de resposta armazenado em cache especificado.</span><span class="sxs-lookup"><span data-stu-id="d6814-126">Retrieves a specified cached response fragment.</span></span>                                                        |



 

## <a name="configuration"></a><span data-ttu-id="d6814-127">Configuração</span><span class="sxs-lookup"><span data-stu-id="d6814-127">Configuration</span></span>



| <span data-ttu-id="d6814-128">Função</span><span class="sxs-lookup"><span data-stu-id="d6814-128">Function</span></span>                                                                 | <span data-ttu-id="d6814-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6814-129">Description</span></span>                                                       |
|--------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="d6814-130">**HttpDeleteServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="d6814-130">**HttpDeleteServiceConfiguration**</span></span>](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) | <span data-ttu-id="d6814-131">Exclui as informações especificadas do repositório de configuração de HTTP.</span><span class="sxs-lookup"><span data-stu-id="d6814-131">Deletes specified information from the HTTP configuration store.</span></span>  |
| [<span data-ttu-id="d6814-132">**HttpQueryServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="d6814-132">**HttpQueryServiceConfiguration**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration)   | <span data-ttu-id="d6814-133">Consulta o repositório de configuração HTTP para obter informações especificadas.</span><span class="sxs-lookup"><span data-stu-id="d6814-133">Queries the HTTP configuration store for specified information.</span></span>   |
| [<span data-ttu-id="d6814-134">**HttpSetServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="d6814-134">**HttpSetServiceConfiguration**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration)       | <span data-ttu-id="d6814-135">Define valores especificados no repositório de configuração da API do servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="d6814-135">Sets specified values in the HTTP Server API configuration store.</span></span> |



 

## <a name="input-and-output"></a><span data-ttu-id="d6814-136">Entrada e saída</span><span class="sxs-lookup"><span data-stu-id="d6814-136">Input and Output</span></span>



| <span data-ttu-id="d6814-137">Função</span><span class="sxs-lookup"><span data-stu-id="d6814-137">Function</span></span>                                                             | <span data-ttu-id="d6814-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6814-138">Description</span></span>                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="d6814-139">**HttpReceiveHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="d6814-139">**HttpReceiveHttpRequest**</span></span>](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)             | <span data-ttu-id="d6814-140">Recupera uma solicitação HTTP de uma fila de solicitações especificada.</span><span class="sxs-lookup"><span data-stu-id="d6814-140">Retrieves an HTTP request from a specified request queue.</span></span>      |
| [<span data-ttu-id="d6814-141">**HttpReceiveRequestEntityBody**</span><span class="sxs-lookup"><span data-stu-id="d6814-141">**HttpReceiveRequestEntityBody**</span></span>](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) | <span data-ttu-id="d6814-142">Recupera os dados do corpo da entidade de uma solicitação HTTP específica.</span><span class="sxs-lookup"><span data-stu-id="d6814-142">Retrieves entity-body data of a particular HTTP request.</span></span>       |
| [<span data-ttu-id="d6814-143">**HttpSendHttpResponse**</span><span class="sxs-lookup"><span data-stu-id="d6814-143">**HttpSendHttpResponse**</span></span>](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)                 | <span data-ttu-id="d6814-144">Envia uma resposta HTTP para uma solicitação HTTP específica.</span><span class="sxs-lookup"><span data-stu-id="d6814-144">Sends an HTTP response for a particular HTTP request.</span></span>          |
| [<span data-ttu-id="d6814-145">**HttpSendResponseEntityBody**</span><span class="sxs-lookup"><span data-stu-id="d6814-145">**HttpSendResponseEntityBody**</span></span>](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)     | <span data-ttu-id="d6814-146">Envia dados de corpo de entidade de uma resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="d6814-146">Sends entity-body data of an HTTP response.</span></span>                    |
| [<span data-ttu-id="d6814-147">**HttpWaitForDisconnect**</span><span class="sxs-lookup"><span data-stu-id="d6814-147">**HttpWaitForDisconnect**</span></span>](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect)               | <span data-ttu-id="d6814-148">Notifica o aplicativo quando um cliente HTTP é desconectado.</span><span class="sxs-lookup"><span data-stu-id="d6814-148">Notifies the application when an HTTP client has disconnected.</span></span> |



 

## <a name="ssl"></a><span data-ttu-id="d6814-149">SSL</span><span class="sxs-lookup"><span data-stu-id="d6814-149">SSL</span></span>



| <span data-ttu-id="d6814-150">Função</span><span class="sxs-lookup"><span data-stu-id="d6814-150">Function</span></span>                                                             | <span data-ttu-id="d6814-151">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6814-151">Description</span></span>                                             |
|----------------------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="d6814-152">**HttpReceiveClientCertificate**</span><span class="sxs-lookup"><span data-stu-id="d6814-152">**HttpReceiveClientCertificate**</span></span>](/windows/desktop/api/Http/nf-http-httpreceiveclientcertificate) | <span data-ttu-id="d6814-153">Recupera o certificado do cliente para uma conexão SSL.</span><span class="sxs-lookup"><span data-stu-id="d6814-153">Retrieves the client certificate for an SSL connection.</span></span> |



 

## <a name="url-registration"></a><span data-ttu-id="d6814-154">Registro de URL</span><span class="sxs-lookup"><span data-stu-id="d6814-154">URL Registration</span></span>



| <span data-ttu-id="d6814-155">Função</span><span class="sxs-lookup"><span data-stu-id="d6814-155">Function</span></span>                               | <span data-ttu-id="d6814-156">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6814-156">Description</span></span>                                                                                     |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6814-157">**HttpAddUrl**</span><span class="sxs-lookup"><span data-stu-id="d6814-157">**HttpAddUrl**</span></span>](/windows/desktop/api/Http/nf-http-httpaddurl)       | <span data-ttu-id="d6814-158">Registra uma URL para que as solicitações HTTP para ele sejam roteadas para uma fila de solicitações especificada.</span><span class="sxs-lookup"><span data-stu-id="d6814-158">Registers a URL so that HTTP requests for it are routed to a specified request queue.</span></span>           |
| [<span data-ttu-id="d6814-159">**HttpRemoveUrl**</span><span class="sxs-lookup"><span data-stu-id="d6814-159">**HttpRemoveUrl**</span></span>](/windows/desktop/api/Http/nf-http-httpremoveurl) | <span data-ttu-id="d6814-160">Cancela o registro de uma URL especificada, para que as solicitações para ela não sejam mais roteadas para uma fila especificada.</span><span class="sxs-lookup"><span data-stu-id="d6814-160">Unregisters a specified URL, so that requests for it are no longer routed to a specified queue.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d6814-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d6814-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6814-162">Estruturas da API do servidor HTTP versão 1,0</span><span class="sxs-lookup"><span data-stu-id="d6814-162">HTTP Server API Version 1.0 Structures</span></span>](http-server-api-version-1-0-structures.md)
</dt> </dl>

 

 




