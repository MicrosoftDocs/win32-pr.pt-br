---
title: Funções da API do servidor HTTP versão 2,0
description: A API do servidor HTTP versão 2,0 fornece as funções a seguir.
ms.assetid: 12daffca-b403-4f06-8037-206f90e33252
keywords:
- Funções da API do servidor HTTP versão 2,0
- Funções HTTP, API do servidor HTTP versão 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136ab885d7fe45ed45d2233bd216b884d1cf9852
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364028"
---
# <a name="http-server-api-version-20-functions"></a><span data-ttu-id="5e859-105">Funções da API do servidor HTTP versão 2,0</span><span class="sxs-lookup"><span data-stu-id="5e859-105">HTTP Server API Version 2.0 Functions</span></span>

<span data-ttu-id="5e859-106">A API do servidor HTTP versão 2,0 fornece as funções a seguir.</span><span class="sxs-lookup"><span data-stu-id="5e859-106">The HTTP Server API version 2.0 provides the following functions.</span></span>

## <a name="server-session"></a><span data-ttu-id="5e859-107">Sessão de servidor</span><span class="sxs-lookup"><span data-stu-id="5e859-107">Server Session</span></span>



| <span data-ttu-id="5e859-108">Função</span><span class="sxs-lookup"><span data-stu-id="5e859-108">Function</span></span>                                                                 | <span data-ttu-id="5e859-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e859-109">Description</span></span> |
|--------------------------------------------------------------------------|-------------|
| [<span data-ttu-id="5e859-110">**HttpCloseServerSession**</span><span class="sxs-lookup"><span data-stu-id="5e859-110">**HttpCloseServerSession**</span></span>](/windows/desktop/api/Http/nf-http-httpcloseserversession)                 |             |
| [<span data-ttu-id="5e859-111">**HttpCreateServerSession**</span><span class="sxs-lookup"><span data-stu-id="5e859-111">**HttpCreateServerSession**</span></span>](/windows/desktop/api/Http/nf-http-httpcreateserversession)               |             |
| [<span data-ttu-id="5e859-112">**HttpQueryServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="5e859-112">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty) |             |
| [<span data-ttu-id="5e859-113">**HttpSetServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="5e859-113">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)     |             |



 

## <a name="url-groups"></a><span data-ttu-id="5e859-114">Grupos de URLs</span><span class="sxs-lookup"><span data-stu-id="5e859-114">URL Groups</span></span>



| <span data-ttu-id="5e859-115">Função</span><span class="sxs-lookup"><span data-stu-id="5e859-115">Function</span></span>                                                       | <span data-ttu-id="5e859-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e859-116">Description</span></span> |
|----------------------------------------------------------------|-------------|
| [<span data-ttu-id="5e859-117">**HttpAddUrlToUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="5e859-117">**HttpAddUrlToUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup)           |             |
| [<span data-ttu-id="5e859-118">**HttpCreateUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="5e859-118">**HttpCreateUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpcreateurlgroup)               |             |
| [<span data-ttu-id="5e859-119">**HttpCloseUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="5e859-119">**HttpCloseUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpcloseurlgroup)                 |             |
| [<span data-ttu-id="5e859-120">**HttpQueryUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="5e859-120">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty) |             |
| [<span data-ttu-id="5e859-121">**HttpRemoveUrlFromUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="5e859-121">**HttpRemoveUrlFromUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) |             |
| [<span data-ttu-id="5e859-122">**HttpSetUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="5e859-122">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)     |             |



 

## <a name="request-queue"></a><span data-ttu-id="5e859-123">Fila de solicitação</span><span class="sxs-lookup"><span data-stu-id="5e859-123">Request Queue</span></span>



| <span data-ttu-id="5e859-124">Função</span><span class="sxs-lookup"><span data-stu-id="5e859-124">Function</span></span>                                                               | <span data-ttu-id="5e859-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e859-125">Description</span></span> |
|------------------------------------------------------------------------|-------------|
| [<span data-ttu-id="5e859-126">**HttpCloseRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="5e859-126">**HttpCloseRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpcloserequestqueue)                 |             |
| [<span data-ttu-id="5e859-127">**HttpCreateRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="5e859-127">**HttpCreateRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue)               |             |
| [<span data-ttu-id="5e859-128">**HttpQueryRequestQueueProperty**</span><span class="sxs-lookup"><span data-stu-id="5e859-128">**HttpQueryRequestQueueProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty) |             |
| [<span data-ttu-id="5e859-129">**HttpSetRequestQueueProperty**</span><span class="sxs-lookup"><span data-stu-id="5e859-129">**HttpSetRequestQueueProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty)     |             |
| [<span data-ttu-id="5e859-130">**HttpShutdownRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="5e859-130">**HttpShutdownRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpshutdownrequestqueue)           |             |
| [<span data-ttu-id="5e859-131">**HttpWaitForDemandStart**</span><span class="sxs-lookup"><span data-stu-id="5e859-131">**HttpWaitForDemandStart**</span></span>](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart)               |             |



 

## <a name="related-topics"></a><span data-ttu-id="5e859-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5e859-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e859-133">Estruturas da API do servidor HTTP versão 2,0</span><span class="sxs-lookup"><span data-stu-id="5e859-133">HTTP Server API Version 2.0 Structures</span></span>](http-server-api-version-2-0-structures.md)
</dt> </dl>

 

 




