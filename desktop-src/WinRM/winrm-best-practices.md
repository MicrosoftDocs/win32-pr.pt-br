---
title: Práticas recomendadas do WinRM
description: Este tópico explica algumas das práticas recomendadas para usar os vários recursos da API do WinRM.
ms.assetid: FC2CD030-199F-43C2-804E-9827EA2A46D5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3452f2b8e61fb72b1fd5f99a073b48afb26dafb0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917356"
---
# <a name="winrm-best-practices"></a><span data-ttu-id="d6f2d-103">Práticas recomendadas do WinRM</span><span class="sxs-lookup"><span data-stu-id="d6f2d-103">WinRM Best Practices</span></span>

<span data-ttu-id="d6f2d-104">Este tópico explica algumas das práticas recomendadas para usar os vários recursos da API do WinRM.</span><span class="sxs-lookup"><span data-stu-id="d6f2d-104">This topic explains some of the best practices for using the various features of the WinRM API.</span></span>

## <a name="quotas"></a><span data-ttu-id="d6f2d-105">Cotas</span><span class="sxs-lookup"><span data-stu-id="d6f2d-105">Quotas</span></span>

<span data-ttu-id="d6f2d-106">Quando uma cota é atingida, o serviço WinRM retorna um erro para o cliente.</span><span class="sxs-lookup"><span data-stu-id="d6f2d-106">When a quota is hit, the WinRM service returns an error to the client.</span></span> <span data-ttu-id="d6f2d-107">Como resultado, a lógica do cliente deve repetir explicitamente a operação com base no erro retornado.</span><span class="sxs-lookup"><span data-stu-id="d6f2d-107">As a result, the client logic must explicitly retry the operation based on the returned error.</span></span>

## <a name="event-subscriptions"></a><span data-ttu-id="d6f2d-108">Assinaturas de evento</span><span class="sxs-lookup"><span data-stu-id="d6f2d-108">Event subscriptions</span></span>

<span data-ttu-id="d6f2d-109">Ao usar assinaturas iniciadas pelo coletor, limite o número de computadores remotos a 500 e isole o serviço [coletor de eventos do Windows](/windows/desktop/WEC/windows-event-collector) (Wecsvc) em um processo de host separado.</span><span class="sxs-lookup"><span data-stu-id="d6f2d-109">When using Collector-initiated subscriptions, limit the number of remote computers to 500 and isolate the [Windows Event Collector](/windows/desktop/WEC/windows-event-collector) service (wecsvc) in a separate host process.</span></span>

<span data-ttu-id="d6f2d-110">Um erro de conexão manterá um thread até atingir o tempo limite. Um grande número de erros de conexão simultâneas pode causar esgotamento do pool de threads e renderizar o servidor sem resposta.</span><span class="sxs-lookup"><span data-stu-id="d6f2d-110">A connection error will hold a thread until it times out. A large number of simultaneous connection errors can cause thread pool exhaustion and render the server unresponsive.</span></span>

 

 