---
description: Quando uma nova sessão de comunicação chegar, os aplicativos TAPI que registraram interesse no endereço e no tipo de mídia receberão uma notificação de evento.
ms.assetid: 6074619c-6aa0-4b03-9208-10268682e704
title: Responder à sessão iniciada em outro lugar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c74554b48919f7532561bfdf0bab7a163a58fbeb3734dc15e4a8d7e0869dad2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072846"
---
# <a name="respond-to-session-initiated-elsewhere"></a>Responder à sessão iniciada em outro lugar

Quando uma nova sessão de comunicação chegar, os [](address-ovr.md) aplicativos [](media-type-ovr.md) TAPI que registraram interesse no endereço e no tipo de mídia receberão uma [notificação de evento](event-notification.md). Somente um aplicativo receberá privilégios de [propriedade](privilege-ovr.md) durante a sessão. Esse aplicativo não pode recusar a sessão.

O estado de chamada inicial de uma sessão de entrada está sendo oferecido. Enquanto a chamada estiver no estado de oferta, um aplicativo poderá obter informações como o modo de portador e o motivo da chamada, se os provedores de serviços fornecerem essas informações e eles estarão disponíveis. Algumas informações de chamada podem não estar disponíveis imediatamente, como a ID do chamador.

Há seis respostas básicas para uma sessão oferecida: [responder](answer-ovr.md), [aceitar](accept-ovr.md) [,](handoffs-ovr.md)entregar, [soltar,](drop-ovr.md)encaminhar [e](forward-ovr.md) [redirecionar](redirect-ovr.md). Dependendo do provedor de serviços, o conjunto completo dessas operações pode não estar disponível.

 

 



