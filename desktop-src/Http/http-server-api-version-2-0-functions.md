---
title: Funções da API do Servidor HTTP versão 2.0
description: A API do Servidor HTTP versão 2.0 fornece as seguintes funções.
ms.assetid: 12daffca-b403-4f06-8037-206f90e33252
keywords:
- Funções da API do Servidor HTTP versão 2.0
- Funções HTTP, API do Servidor HTTP versão 2.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92e4d5c09c001caa58d43c1e61d800f66b39706b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549071"
---
# <a name="http-server-api-version-20-functions"></a><span data-ttu-id="6f605-105">Funções da API do Servidor HTTP versão 2.0</span><span class="sxs-lookup"><span data-stu-id="6f605-105">HTTP Server API version 2.0 functions</span></span>

<span data-ttu-id="6f605-106">A API do Servidor HTTP versão 2.0 fornece as seguintes funções.</span><span class="sxs-lookup"><span data-stu-id="6f605-106">The HTTP Server API version 2.0 provides the following functions.</span></span>

| <span data-ttu-id="6f605-107">Função</span><span class="sxs-lookup"><span data-stu-id="6f605-107">Function</span></span> | <span data-ttu-id="6f605-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f605-108">Description</span></span> |
|-|-|
| [<span data-ttu-id="6f605-109">**HttpDelegateRequestEx**</span><span class="sxs-lookup"><span data-stu-id="6f605-109">**HttpDelegateRequestEx**</span></span>](/windows/win32/api/http/nf-http-httpdelegaterequestex) | <span data-ttu-id="6f605-110">Delega uma solicitação da fila de solicitação de origem para a fila de solicitação de destino.</span><span class="sxs-lookup"><span data-stu-id="6f605-110">Delegates a request from the source request queue to the target request queue.</span></span> |
| [<span data-ttu-id="6f605-111">**HttpFindUrlGroupId**</span><span class="sxs-lookup"><span data-stu-id="6f605-111">**HttpFindUrlGroupId**</span></span>](/windows/win32/api/http/nf-http-httpfindurlgroupid) | <span data-ttu-id="6f605-112">Recupera uma ID de grupo de URL para uma URL e uma fila de solicitação.</span><span class="sxs-lookup"><span data-stu-id="6f605-112">Retrieves a URL group ID for a URL and a request queue.</span></span> |
| [<span data-ttu-id="6f605-113">**HttpIsFeatureSupported**</span><span class="sxs-lookup"><span data-stu-id="6f605-113">**HttpIsFeatureSupported**</span></span>](/windows/win32/api/http/nf-http-httpisfeaturesupported) | <span data-ttu-id="6f605-114">Verifica se há suporte para um recurso específico.</span><span class="sxs-lookup"><span data-stu-id="6f605-114">Checks whether a particular feature is supported.</span></span> |

## <a name="server-session"></a><span data-ttu-id="6f605-115">Sessão do servidor</span><span class="sxs-lookup"><span data-stu-id="6f605-115">Server session</span></span>

| <span data-ttu-id="6f605-116">Função</span><span class="sxs-lookup"><span data-stu-id="6f605-116">Function</span></span> | <span data-ttu-id="6f605-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f605-117">Description</span></span> |
|-|-|
| [<span data-ttu-id="6f605-118">**HttpCloseServerSession**</span><span class="sxs-lookup"><span data-stu-id="6f605-118">**HttpCloseServerSession**</span></span>](/windows/desktop/api/Http/nf-http-httpcloseserversession) | |
| [<span data-ttu-id="6f605-119">**HttpCreateServerSession**</span><span class="sxs-lookup"><span data-stu-id="6f605-119">**HttpCreateServerSession**</span></span>](/windows/desktop/api/Http/nf-http-httpcreateserversession) | |
| [<span data-ttu-id="6f605-120">**HttpQueryServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="6f605-120">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty) | |
| [<span data-ttu-id="6f605-121">**HttpSetServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="6f605-121">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) | |

## <a name="url-groups"></a><span data-ttu-id="6f605-122">Grupos de URL</span><span class="sxs-lookup"><span data-stu-id="6f605-122">URL Groups</span></span>

| <span data-ttu-id="6f605-123">Função</span><span class="sxs-lookup"><span data-stu-id="6f605-123">Function</span></span> | <span data-ttu-id="6f605-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f605-124">Description</span></span> |
|-|-|
| [<span data-ttu-id="6f605-125">**HttpAddUrlToUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="6f605-125">**HttpAddUrlToUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) | |
| [<span data-ttu-id="6f605-126">**HttpCreateUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="6f605-126">**HttpCreateUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) | |
| [<span data-ttu-id="6f605-127">**HttpCloseUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="6f605-127">**HttpCloseUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) | |
| [<span data-ttu-id="6f605-128">**HttpQueryUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="6f605-128">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty) | |
| [<span data-ttu-id="6f605-129">**HttpRemoveUrlFromUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="6f605-129">**HttpRemoveUrlFromUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) | |
| [<span data-ttu-id="6f605-130">**HttpSetUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="6f605-130">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) | |

## <a name="request-queue"></a><span data-ttu-id="6f605-131">Fila de solicitação</span><span class="sxs-lookup"><span data-stu-id="6f605-131">Request Queue</span></span>

| <span data-ttu-id="6f605-132">Função</span><span class="sxs-lookup"><span data-stu-id="6f605-132">Function</span></span> | <span data-ttu-id="6f605-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f605-133">Description</span></span> |
|-|-|
| [<span data-ttu-id="6f605-134">**HttpCloseRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="6f605-134">**HttpCloseRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpcloserequestqueue) | |
| [<span data-ttu-id="6f605-135">**HttpCreateRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="6f605-135">**HttpCreateRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) | |
| [<span data-ttu-id="6f605-136">**HttpQueryRequestQueueProperty**</span><span class="sxs-lookup"><span data-stu-id="6f605-136">**HttpQueryRequestQueueProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty) | |
| [<span data-ttu-id="6f605-137">**HttpSetRequestQueueProperty**</span><span class="sxs-lookup"><span data-stu-id="6f605-137">**HttpSetRequestQueueProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) | |
| [<span data-ttu-id="6f605-138">**HttpShutdownRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="6f605-138">**HttpShutdownRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpshutdownrequestqueue) | |
| [<span data-ttu-id="6f605-139">**HttpWaitForDemandStart**</span><span class="sxs-lookup"><span data-stu-id="6f605-139">**HttpWaitForDemandStart**</span></span>](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) | |

## <a name="related-topics"></a><span data-ttu-id="6f605-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6f605-140">Related topics</span></span>

[<span data-ttu-id="6f605-141">Estruturas da API do servidor HTTP versão 2,0</span><span class="sxs-lookup"><span data-stu-id="6f605-141">HTTP Server API version 2.0 structures</span></span>](http-server-api-version-2-0-structures.md)
