---
description: O Serviço de Notificação de Eventos do Sistema permite que aplicativos com conhecimento de dispositivo móvel recebam notificações de eventos do sistema monitorados pelo SENS. Quando o evento solicitado ocorre, o SENS notifica o aplicativo.
ms.assetid: 19311dec-4611-4104-b6e4-ff8f7c8af0e7
title: Notificações (Serviço de Notificação de Eventos do Sistema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db908c48c38ccd39c6c9a427b77e3cefffc7b9bf8fad6e464ebdf146a138e57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003964"
---
# <a name="notifications-system-event-notification-service"></a>Notificações (Serviço de Notificação de Eventos do Sistema)

O Serviço de Notificação de Eventos do Sistema permite que aplicativos com conhecimento de dispositivo móvel recebam notificações de eventos do sistema monitorados pelo SENS. Quando o evento solicitado ocorre, o SENS notifica o aplicativo.

O SENS pode notificar os aplicativos sobre três classes de eventos do sistema:

-   Eventos de rede TCP/IP, como o status de uma conexão de rede TCP/IP ou a qualidade da conexão.
-   Eventos de logon do usuário.
-   Eventos de energia de bateria e AC.

Por exemplo, um aplicativo pode assinar qualquer um dos seguintes eventos do sistema:

-   Estabelecimento de conectividade de rede
-   Notificação quando um destino especificado pode ser alcançado dentro dos parâmetros de QOC (Qualidade de Conexão) especificados
-   O computador alternou para a energia da bateria
-   O percentual de energia restante da bateria está dentro de um parâmetro especificado
-   Eventos agendados usando o Synchronization Manager ocorrem

**Windows Server 2008 R2 e Windows 7:** O assinante tem no máximo 3 minutos para responder a uma notificação nas interfaces [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon) e [**ISensLogon2.**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2) Após 3 minutos, o SENS cancela a chamada aos assinantes e desbloqueia o thread de notificação. Se uma operação demorada for necessária para responder à notificação, retorne de **ISensLogon** ou **ISensLogon2** o mais rápido possível e abra outro thread para processamento.

 

 



