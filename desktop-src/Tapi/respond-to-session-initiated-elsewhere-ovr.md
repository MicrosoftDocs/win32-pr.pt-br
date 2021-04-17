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
# <a name="respond-to-session-initiated-elsewhere"></a>Responder à sessão iniciada em outro lugar

Quando chega uma nova sessão de comunicações, os aplicativos TAPI que registraram um interesse no [tipo de mídia](media-type-ovr.md) e [endereço](address-ovr.md) receberão uma [notificação de evento](event-notification.md). Somente um aplicativo receberá [privilégios](privilege-ovr.md) de propriedade pela sessão. Este aplicativo não pode recusar a sessão.

O estado de chamada inicial de uma sessão de entrada é oferta. Embora a chamada esteja no estado de oferta, um aplicativo pode obter informações como o modo de portador e o motivo da chamada, se os provedores de serviços fornecerem essas informações e estiverem disponíveis. Algumas informações de chamada podem não estar disponíveis imediatamente, como a ID do chamador.

Há seis respostas básicas para uma sessão oferecida: [responder](answer-ovr.md), [aceitar](accept-ovr.md), [entrega](handoffs-ovr.md), [soltar](drop-ovr.md), [encaminhar](forward-ovr.md)e [redirecionar](redirect-ovr.md). Dependendo do provedor de serviços, o conjunto completo dessas operações pode não estar disponível.

 

 



