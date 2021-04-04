---
title: Configurando a fila de solicitações
description: Configurando a fila de solicitações
ms.assetid: ab03089c-2ef1-457d-a5f5-a4d400f3a7f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ed397ffbcb42d887d519bc4492bd167dd98c57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822624"
---
# <a name="configuring-the-request-queue"></a><span data-ttu-id="03b84-103">Configurando a fila de solicitações</span><span class="sxs-lookup"><span data-stu-id="03b84-103">Configuring the Request Queue</span></span>

<span data-ttu-id="03b84-104">Quando a fila de solicitações é aberta ou criada, o aplicativo de chamada recebe um identificador para ele que pode ser usado para enviar solicitações ou configurar a fila de solicitações.</span><span class="sxs-lookup"><span data-stu-id="03b84-104">When the request queue is opened or created, the calling application receives a handle to it that can be used to send requests or configure the request queue.</span></span> <span data-ttu-id="03b84-105">Chamar [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) com **HttpServerBindingProperty** e fornecer o identificador da fila de solicitações na estrutura de [**\_ \_ informações de associação http**](/windows/desktop/api/Http/ns-http-http_binding_info) , especificado no parâmetro *pPropertyInformation* , associa o grupo de URLs à fila de solicitações.</span><span class="sxs-lookup"><span data-stu-id="03b84-105">Calling [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) with **HttpServerBindingProperty** and supplying the request queue handle in the [**HTTP\_BINDING\_INFO**](/windows/desktop/api/Http/ns-http-http_binding_info) structure, specified in the *pPropertyInformation* parameter, associates the URL group with the request queue.</span></span> <span data-ttu-id="03b84-106">As propriedades da fila de solicitações são definidas somente pelo aplicativo que cria a fila de solicitações.</span><span class="sxs-lookup"><span data-stu-id="03b84-106">Request queue properties are set only by the application that creates the request queue.</span></span> <span data-ttu-id="03b84-107">Por exemplo, para definir a propriedade comprimento da fila do servidor, o aplicativo criador chama [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) especificando **HttpServerQueueLengthProperty** no parâmetro *Property* .</span><span class="sxs-lookup"><span data-stu-id="03b84-107">For example, to set the server queue length property, the creator application calls [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) specifying **HttpServerQueueLengthProperty** in the *Property* parameter.</span></span>

 

 




