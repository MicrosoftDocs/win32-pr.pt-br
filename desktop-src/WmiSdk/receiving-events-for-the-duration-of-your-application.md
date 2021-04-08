---
description: Uma das maneiras mais comuns de receber um evento é por meio de um aplicativo em execução, como um aplicativo de gerenciamento que coleta e exibe eventos para um usuário.
ms.assetid: 380ac556-ba0a-4fae-8b76-0645d99e8583
ms.tgt_platform: multiple
title: Recebendo eventos para a duração do seu aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd6b9731dd662a92296a86910a6cf8cb231cca1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010766"
---
# <a name="receiving-events-for-the-duration-of-your-application"></a><span data-ttu-id="33787-103">Recebendo eventos para a duração do seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="33787-103">Receiving Events for the Duration of Your Application</span></span>

<span data-ttu-id="33787-104">Uma das maneiras mais comuns de receber um evento é por meio de um aplicativo em execução, como um aplicativo de gerenciamento que coleta e exibe eventos para um usuário.</span><span class="sxs-lookup"><span data-stu-id="33787-104">One of the most common ways to receive an event is through a running application, such as a management application that collects and displays events to a user.</span></span> <span data-ttu-id="33787-105">Esses aplicativos são chamados de "temporários" porque um consumidor temporário não recebe notificações de eventos quando ele é desligado.</span><span class="sxs-lookup"><span data-stu-id="33787-105">Such applications are called "temporary" because a temporary consumer does not receive event notifications when shut down.</span></span>

<span data-ttu-id="33787-106">Um consumidor temporário chama [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) no script ou [**IWbemServices.ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) no C++ para assinar eventos em um namespace.</span><span class="sxs-lookup"><span data-stu-id="33787-106">A temporary consumer calls [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) in script or [**IWbemServices.ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) in C++ to subscribe to events in a namespace.</span></span> <span data-ttu-id="33787-107">A identidade associada a essa assinatura é o chamador.</span><span class="sxs-lookup"><span data-stu-id="33787-107">The identity associated with this subscription is the caller.</span></span>

<span data-ttu-id="33787-108">Um consumidor de evento temporário pode receber notificações de forma assíncrona ou semisynchronously em scripts e em C++.</span><span class="sxs-lookup"><span data-stu-id="33787-108">A temporary event consumer can receive notifications either asynchronously or semisynchronously in both scripts and C++.</span></span>

> [!Note]  
> <span data-ttu-id="33787-109">Por motivos de segurança, é importante observar que as notificações de eventos assíncronos não são recomendadas.</span><span class="sxs-lookup"><span data-stu-id="33787-109">For security reasons, it is important to note that asynchronous event notifications are not recommended.</span></span> <span data-ttu-id="33787-110">Para obter mais informações, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="33787-110">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span> <span data-ttu-id="33787-111">Os consumidores de eventos têm preocupações de segurança especiais.</span><span class="sxs-lookup"><span data-stu-id="33787-111">Event consumers have special security concerns.</span></span> <span data-ttu-id="33787-112">Para obter mais informações, consulte [SECURING WMI Events](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="33787-112">For more information, see [Securing WMI Events](securing-wmi-events.md).</span></span>

 

<span data-ttu-id="33787-113">Para obter mais informações sobre como receber notificações de eventos assíncronas e semisynchronous, consulte [recebendo notificações de eventos assíncronos](receiving-asynchronous-event-notifications.md) e [recebendo notificações de eventos de semisynchronous](receiving-synchronous-and-semisynchronous-event-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="33787-113">For more information about receiving asynchronous and semisynchronous event notifications, see [Receiving Asynchronous Event Notifications](receiving-asynchronous-event-notifications.md) and [Receiving Semisynchronous Event Notifications](receiving-synchronous-and-semisynchronous-event-notifications.md).</span></span>

 

 



