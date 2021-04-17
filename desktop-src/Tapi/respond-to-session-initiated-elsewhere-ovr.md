---
description: Quando chega uma nova sessão de comunicações, os aplicativos TAPI que registraram um interesse no tipo de mídia e endereço receberão uma notificação de evento.
ms.assetid: 6074619c-6aa0-4b03-9208-10268682e704
title: Responder à sessão iniciada em outro lugar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e25651b58f8841ac4de9bf14f4d139161c1359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755174"
---
# <a name="respond-to-session-initiated-elsewhere"></a><span data-ttu-id="13508-103">Responder à sessão iniciada em outro lugar</span><span class="sxs-lookup"><span data-stu-id="13508-103">Respond to Session Initiated Elsewhere</span></span>

<span data-ttu-id="13508-104">Quando chega uma nova sessão de comunicações, os aplicativos TAPI que registraram um interesse no [tipo de mídia](media-type-ovr.md) e [endereço](address-ovr.md) receberão uma [notificação de evento](event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="13508-104">When a new communications session arrives, TAPI applications that registered an interest in the [address](address-ovr.md) and [media type](media-type-ovr.md) will be sent an [event notification](event-notification.md).</span></span> <span data-ttu-id="13508-105">Somente um aplicativo receberá [privilégios](privilege-ovr.md) de propriedade pela sessão.</span><span class="sxs-lookup"><span data-stu-id="13508-105">Only one application will be offered ownership [privileges](privilege-ovr.md) over the session.</span></span> <span data-ttu-id="13508-106">Este aplicativo não pode recusar a sessão.</span><span class="sxs-lookup"><span data-stu-id="13508-106">This application cannot refuse the session.</span></span>

<span data-ttu-id="13508-107">O estado de chamada inicial de uma sessão de entrada é oferta.</span><span class="sxs-lookup"><span data-stu-id="13508-107">The initial call state of an incoming session is offering.</span></span> <span data-ttu-id="13508-108">Embora a chamada esteja no estado de oferta, um aplicativo pode obter informações como o modo de portador e o motivo da chamada, se os provedores de serviços fornecerem essas informações e estiverem disponíveis.</span><span class="sxs-lookup"><span data-stu-id="13508-108">While the call is in the offering state, an application can obtain information such as bearer mode and call reason, if the service providers supplied this information and it is available.</span></span> <span data-ttu-id="13508-109">Algumas informações de chamada podem não estar disponíveis imediatamente, como a ID do chamador.</span><span class="sxs-lookup"><span data-stu-id="13508-109">Some call information may not be available immediately, such as caller ID.</span></span>

<span data-ttu-id="13508-110">Há seis respostas básicas para uma sessão oferecida: [responder](answer-ovr.md), [aceitar](accept-ovr.md), [entrega](handoffs-ovr.md), [soltar](drop-ovr.md), [encaminhar](forward-ovr.md)e [redirecionar](redirect-ovr.md).</span><span class="sxs-lookup"><span data-stu-id="13508-110">There are six basic responses to an offered session: [answer](answer-ovr.md), [accept](accept-ovr.md), [handoff](handoffs-ovr.md), [drop](drop-ovr.md), [forward](forward-ovr.md), and [redirect](redirect-ovr.md).</span></span> <span data-ttu-id="13508-111">Dependendo do provedor de serviços, o conjunto completo dessas operações pode não estar disponível.</span><span class="sxs-lookup"><span data-stu-id="13508-111">Depending on the service provider, the full set of these operations may not be available.</span></span>

 

 



