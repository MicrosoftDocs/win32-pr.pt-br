---
description: Alguns aplicativos precisam receber a notificação de eventos de conexão, seja antes do evento, logo após a ocorrência, ou ambos. Você pode criar uma DLL para receber a notificação de adiantamento e após o fato dos eventos de conexão.
ms.assetid: 692eb8f2-1c53-4535-b44d-babb30eecd9c
title: Recebendo notificações de conexão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c054d4f7bb78f610afe6c1cbdf028416de7b5596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501263"
---
# <a name="receiving-connection-notifications"></a>Recebendo notificações de conexão

Alguns aplicativos precisam receber a notificação de eventos de conexão, seja antes do evento, logo após a ocorrência, ou ambos. Você pode criar uma DLL para receber a notificação de adiantamento e após o fato dos eventos de conexão.

Um exemplo de um aplicativo que precisa receber notificações antecipadas de um evento de conexão é o RAS (serviço de acesso remoto). O RAS precisa ser informado antes que uma conexão seja feita porque pode ser necessário estabelecer uma conexão de modem antes de fazer a conexão de rede.

Da mesma forma, os aplicativos podem precisar limpar os recursos depois que a conexão é feita, portanto, exigindo uma notificação pós-conexão.

Os aplicativos interessados em receber o adiantamento e a notificação após o fato dos eventos de conexão devem fornecer uma DLL que exporta duas funções, [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) e [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify).

Depois de implementar essas funções, você deve registrar sua DLL, conforme descrito em [registrando para receber notificações de conexão](registering-to-receive-connection-notifications.md).

 

 



