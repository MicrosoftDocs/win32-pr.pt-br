---
title: Criando e ligando a uma fila de solicitações
description: Uma fila de solicitações é uma fila de serviço que mantém solicitações pendentes para um aplicativo específico.
ms.assetid: 93f8b230-af0a-4582-b35b-d65f6841e525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 945b8451f9128357b7da0ddc64600b74deffd0d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364243"
---
# <a name="creating-and-binding-to-a-request-queue"></a><span data-ttu-id="eb266-103">Criando e ligando a uma fila de solicitações</span><span class="sxs-lookup"><span data-stu-id="eb266-103">Creating and Binding to a Request Queue</span></span>

<span data-ttu-id="eb266-104">Uma fila de solicitações é uma fila de serviço que mantém solicitações pendentes para um aplicativo específico.</span><span class="sxs-lookup"><span data-stu-id="eb266-104">A request queue is a service queue that holds pending requests for a specific application.</span></span> <span data-ttu-id="eb266-105">Um aplicativo cria a fila de solicitações independentemente do grupo de URLs ou da sessão de servidor chamando a função [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) e define as propriedades da fila de solicitações chamando a função [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) .</span><span class="sxs-lookup"><span data-stu-id="eb266-105">An application creates the request queue independently of the URL group or server session by calling the [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) function, and sets the request queue properties by calling the [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) function.</span></span> <span data-ttu-id="eb266-106">Essas propriedades são o detalhamento de 503 respostas, o comprimento máximo da fila e o estado da atividade.</span><span class="sxs-lookup"><span data-stu-id="eb266-106">These properties are the verbosity of 503 responses, the maximum length of the queue, and the activity state.</span></span>

<span data-ttu-id="eb266-107">Para fazer com que as solicitações sejam roteadas para sua fila de solicitações, o aplicativo associa o grupo de URLs criado como parte da [configuração de tempo de execução](run-time-configuration.md) à fila chamando [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) com **HttpServerBindingProperty** especificado no parâmetro *Property* .</span><span class="sxs-lookup"><span data-stu-id="eb266-107">To cause requests to be routed to its request queue, the application binds the URL group it created as part of [run-time configuration](run-time-configuration.md) to the queue by calling [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) with **HttpServerBindingProperty** specified in the *Property* parameter.</span></span> <span data-ttu-id="eb266-108">As solicitações de entrada das URLs no grupo são então roteadas para a fila de solicitações especificada.</span><span class="sxs-lookup"><span data-stu-id="eb266-108">Incoming requests from the URLs in the group are then routed to the specified request queue.</span></span>

 

 




