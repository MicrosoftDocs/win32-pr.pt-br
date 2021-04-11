---
title: Registrando para notificação de alteração
description: Um cliente pode se registrar para receber notificações de alterações nas informações de roteamento armazenadas no Gerenciador de tabela de roteamento. Essa solicitação só pode ser feita depois que um cliente é registrado com o Gerenciador de tabela de roteamento.
ms.assetid: 90dc98eb-0d0b-4450-848b-c7cedab75a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c3a98062fee73c481c1f47c32fa7eeb5465a112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292090"
---
# <a name="registering-for-change-notification"></a><span data-ttu-id="e4d8f-104">Registrando para notificação de alteração</span><span class="sxs-lookup"><span data-stu-id="e4d8f-104">Registering for Change Notification</span></span>

<span data-ttu-id="e4d8f-105">Um cliente pode se registrar para receber notificações de alterações nas informações de roteamento armazenadas no Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="e4d8f-105">A client can register to receive notification of changes to routing information that is stored in the routing table manager.</span></span> <span data-ttu-id="e4d8f-106">Essa solicitação só pode ser feita depois que um cliente é registrado com o Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="e4d8f-106">This request can only be made after a client has registered with the routing table manager.</span></span>

<span data-ttu-id="e4d8f-107">Para se registrar para notificação de alteração, um cliente deve chamar [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification), especificando os tipos de alterações para as quais o cliente deve receber a notificação.</span><span class="sxs-lookup"><span data-stu-id="e4d8f-107">To register for change notification, a client must call [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification), specifying the types of changes for which the client must receive notification.</span></span> <span data-ttu-id="e4d8f-108">Se o cliente precisar ser notificado sobre alteração em destinos específicos, o cliente chamará [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification) uma vez para cada destino.</span><span class="sxs-lookup"><span data-stu-id="e4d8f-108">If the client must be notified of change to specific destinations, the client calls [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification) once for each destination.</span></span>

<span data-ttu-id="e4d8f-109">O cliente pode parar de receber notificações de alteração chamando [**RtmDeregisterFromChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification).</span><span class="sxs-lookup"><span data-stu-id="e4d8f-109">The client can stop receiving change notifications by calling [**RtmDeregisterFromChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification).</span></span>

<span data-ttu-id="e4d8f-110">Para obter um exemplo de código que mostra como usar essas funções, consulte [registrar para notificação de alteração](register-for-change-notification.md).</span><span class="sxs-lookup"><span data-stu-id="e4d8f-110">For sample code that shows how to use these functions, see [Register For Change Notification](register-for-change-notification.md).</span></span>

 

 




