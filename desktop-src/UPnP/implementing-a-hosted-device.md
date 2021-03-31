---
title: Implementando um dispositivo hospedado
description: O host do dispositivo com tecnologia UPnP implementa a descoberta, a descrição, o controle e o evento dos protocolos UPnP principais.
ms.assetid: ab113d76-5fc9-4be2-a814-8772dd1e9600
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172e9935dcbca73dbb285ba73270375fb5bfb6cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636927"
---
# <a name="implementing-a-hosted-device"></a><span data-ttu-id="56ba4-103">Implementando um dispositivo hospedado</span><span class="sxs-lookup"><span data-stu-id="56ba4-103">Implementing a Hosted Device</span></span>

<span data-ttu-id="56ba4-104">O host do dispositivo com tecnologia UPnP implementa os principais protocolos UPnP: descoberta, descrição, controle e eventos.</span><span class="sxs-lookup"><span data-stu-id="56ba4-104">The device host with UPnP technology implements the core UPnP protocols: discovery, description, control, and eventing.</span></span> <span data-ttu-id="56ba4-105">O desenvolvedor que implementa um dispositivo hospedado só precisa fornecer:</span><span class="sxs-lookup"><span data-stu-id="56ba4-105">The developer who implements a hosted device only needs to provide:</span></span>

-   <span data-ttu-id="56ba4-106">Uma descrição do dispositivo e seus serviços.</span><span class="sxs-lookup"><span data-stu-id="56ba4-106">A description of the device and its services.</span></span>
-   <span data-ttu-id="56ba4-107">Uma implementação da funcionalidade do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56ba4-107">An implementation of the device's functionality.</span></span>

<span data-ttu-id="56ba4-108">Por exemplo, o desenvolvedor de um dispositivo de relógio deve fornecer descrições de dispositivo e serviço baseadas em UPnP para ele e uma implementação das funções de relógio (como manter o tempo, definir o tempo e responder a consultas para a hora atual).</span><span class="sxs-lookup"><span data-stu-id="56ba4-108">For example, the developer of a clock device must provide UPnP-based device and service descriptions for it, and an implementation of the clock functions (such as keeping time, setting time, and responding to queries for the current time).</span></span> <span data-ttu-id="56ba4-109">O host do dispositivo:</span><span class="sxs-lookup"><span data-stu-id="56ba4-109">The device host:</span></span>

-   <span data-ttu-id="56ba4-110">Anuncia o dispositivo de acordo com o protocolo de descoberta UPnP.</span><span class="sxs-lookup"><span data-stu-id="56ba4-110">Announces the device according to the UPnP discovery protocol.</span></span>
-   <span data-ttu-id="56ba4-111">Responde a consultas para a descrição do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56ba4-111">Responds to queries for the device's description.</span></span>
-   <span data-ttu-id="56ba4-112">Roteia solicitações de controle para a parte do código do dispositivo que implementa as funções de relógio.</span><span class="sxs-lookup"><span data-stu-id="56ba4-112">Routes control requests to the part of the device's code that implements the clock functions.</span></span>
-   <span data-ttu-id="56ba4-113">Mantém assinaturas de evento para serviços.</span><span class="sxs-lookup"><span data-stu-id="56ba4-113">Maintains event subscriptions to services.</span></span>
-   <span data-ttu-id="56ba4-114">Envia notificações de eventos aos assinantes quando o estado do serviço é alterado.</span><span class="sxs-lookup"><span data-stu-id="56ba4-114">Sends event notifications to subscribers when the service's state changes.</span></span>

 

 




