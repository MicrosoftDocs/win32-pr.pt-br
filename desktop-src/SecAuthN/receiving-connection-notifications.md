---
description: Alguns aplicativos precisam receber notificação de eventos de conexão, antes do evento, logo após ele ocorrer ou ambos. Você pode criar uma DLL para receber notificações antecipadas e posteriores de eventos de conexão.
ms.assetid: 692eb8f2-1c53-4535-b44d-babb30eecd9c
title: Recebendo notificações de conexão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a581855ef134536df8c4c728521e796e541c963a780e2f572ad88dc704c677
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919685"
---
# <a name="receiving-connection-notifications"></a>Recebendo notificações de conexão

Alguns aplicativos precisam receber notificação de eventos de conexão, antes do evento, logo após ele ocorrer ou ambos. Você pode criar uma DLL para receber notificações antecipadas e posteriores de eventos de conexão.

Um exemplo de um aplicativo que precisa receber notificação antecipada de um evento de conexão é o RAS (Serviço de Acesso Remoto). O RAS precisa ser informado antes que uma conexão seja feita porque pode ser necessário estabelecer uma conexão de modem antes de fazer a conexão de rede.

Da mesma forma, os aplicativos talvez precisem limpar os recursos depois que a conexão for feita, exigindo, portanto, uma notificação pós-conexão.

Os aplicativos interessados em receber notificações antecipadas e posteriores de eventos de conexão devem fornecer uma DLL que exporta duas funções, [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) e [**CancelConnectNotify.**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify)

Depois de implementar essas funções, você deve registrar sua DLL, conforme descrito em Registrando-se [para receber notificações de conexão.](registering-to-receive-connection-notifications.md)

 

 



