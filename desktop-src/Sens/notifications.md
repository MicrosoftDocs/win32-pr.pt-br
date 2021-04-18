---
description: O serviço de notificação de eventos do sistema permite que aplicativos com reconhecimento de mobilidade recebam notificações de eventos do sistema que o SENS monitora. Quando o evento solicitado ocorre, o SENS notifica o aplicativo.
ms.assetid: 19311dec-4611-4104-b6e4-ff8f7c8af0e7
title: Notificações (serviço de notificação de eventos do sistema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272f0ea60369015328e34d3a83231ab0b254253a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756373"
---
# <a name="notifications-system-event-notification-service"></a>Notificações (serviço de notificação de eventos do sistema)

O serviço de notificação de eventos do sistema permite que aplicativos com reconhecimento de mobilidade recebam notificações de eventos do sistema que o SENS monitora. Quando o evento solicitado ocorre, o SENS notifica o aplicativo.

O SENS pode notificar aplicativos sobre três classes de eventos do sistema:

-   Eventos de rede TCP/IP, como o status de uma conexão de rede TCP/IP ou a qualidade da conexão.
-   Eventos de logon do usuário.
-   Eventos de energia de bateria e AC.

Por exemplo, um aplicativo pode assinar qualquer um dos seguintes eventos do sistema:

-   Estabelecimento de conectividade de rede
-   Notificação quando um destino especificado pode ser alcançado dentro dos parâmetros de QOC (qualidade de conexão) especificados
-   O computador mudou para a energia da bateria
-   A porcentagem de energia restante da bateria está dentro de um parâmetro especificado
-   Ocorrem eventos agendados usando o Gerenciador de sincronização

**Windows Server 2008 R2 e Windows 7:** O Assinante tem um máximo de 3 minutos para responder a uma notificação nas interfaces [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon) e [**ISensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2) . Após 3 minutos, o SENS cancela a chamada para assinantes e desbloqueia o thread de notificação. Se uma operação demorada for necessária para responder à notificação, retorne de **ISensLogon** ou **ISensLogon2** o mais rápido possível e abra outro thread para processamento.

 

 



