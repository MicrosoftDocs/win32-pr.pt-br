---
title: Recuperando alterações
description: Depois que um cliente tiver se registrado para notificação de determinadas alterações e uma ou mais dessas alterações ocorrerem, o cliente receberá uma notificação do Gerenciador de tabelas de roteamento.
ms.assetid: 5ddebf2d-e3cb-451c-b082-708d2c7d0f79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ccf66d8a1df671cbd9059c444cf26321911bb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498654"
---
# <a name="retrieving-changes"></a><span data-ttu-id="a3ef2-103">Recuperando alterações</span><span class="sxs-lookup"><span data-stu-id="a3ef2-103">Retrieving Changes</span></span>

<span data-ttu-id="a3ef2-104">Depois que um cliente tiver se registrado para notificação de determinadas alterações e uma ou mais dessas alterações ocorrerem, o cliente receberá uma notificação do Gerenciador de tabelas de roteamento.</span><span class="sxs-lookup"><span data-stu-id="a3ef2-104">Once a client has registered for notification of certain changes and one or more of these changes occurs, the client receives a notification from the routing table manager.</span></span> <span data-ttu-id="a3ef2-105">O Gerenciador de tabela de roteamento usa o retorno de chamada de retorno de chamada de [**\_ evento \_ RTM**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) que foi fornecido em uma chamada anterior para [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity).</span><span class="sxs-lookup"><span data-stu-id="a3ef2-105">The routing table manager uses the [**RTM\_EVENT\_CALLBACK**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) callback that was supplied in a previous call to [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity).</span></span> <span data-ttu-id="a3ef2-106">O Gerenciador de tabela de roteamento indica que \_ ocorreu um evento de notificação de alteração RTM \_ .</span><span class="sxs-lookup"><span data-stu-id="a3ef2-106">The routing table manager indicates that a RTM\_CHANGE\_NOTIFICATION event has occurred.</span></span>

<span data-ttu-id="a3ef2-107">Para obter um exemplo de código que mostra como usar essas funções, consulte [usar o retorno de chamada de notificação de evento](use-the-event-notification-callback.md).</span><span class="sxs-lookup"><span data-stu-id="a3ef2-107">For sample code that shows how to use these functions, see [Use the Event Notification Callback](use-the-event-notification-callback.md).</span></span>

 

 




