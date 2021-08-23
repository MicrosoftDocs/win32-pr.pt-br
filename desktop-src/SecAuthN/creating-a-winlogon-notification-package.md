---
description: Um pacote de notificação do Winlogon é uma DLL que exporta funções que manipulam eventos do Winlogon. Por exemplo, quando um usuário faz logon no sistema, o Winlogon chama a função de manipulador de eventos de logon de cada pacote de notificação para fornecer informações sobre o evento.
ms.assetid: a2a26bac-93b6-4d94-94fc-42c9821935a0
title: Criando um pacote de notificação do Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84d0290f7afeba7a427f5c50caf1638fd88bfdb4b52ee513a9b1c0506aed9df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008864"
---
# <a name="creating-a-winlogon-notification-package"></a>Criando um pacote de notificação do Winlogon

Um pacote de notificação do [*Winlogon*](/windows/desktop/SecGloss/w-gly) é uma DLL que exporta funções que manipulam eventos do Winlogon. Por exemplo, quando um usuário faz logon no sistema, o Winlogon chama a função de manipulador de eventos de logon de cada pacote de notificação para fornecer informações sobre o evento.

Os nomes das funções de manipulador de eventos implementadas em um pacote de notificação são deixados para o desenvolvedor; O Winlogon verifica o registro para obter os nomes das funções do manipulador de eventos. Por exemplo, um pacote de notificação pode implementar a função de manipulador de eventos de logon como sendo que `WLEventLogon` outro pode usar `HandleLogonEvent` .

Você não precisa implementar e registrar manipuladores de eventos para cada evento Winlogon, somente para eventos que são úteis para seu aplicativo. Cada função de manipulador de eventos deve usar o protótipo de função descrito no [protótipo de função do manipulador de eventos](event-handler-function-prototype.md). Este protótipo tem um único parâmetro: uma estrutura de [**\_ \_ informações de notificação do WLX**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) que contém detalhes sobre o evento.

O Winlogon ignora a saída das funções do manipulador de eventos. Se a manipulação de um evento exigir interação com o Winlogon, use as [funções de suporte do Winlogon](authentication-functions.md).

Para usar o pacote de notificação do Winlogon, a DLL deve ser copiada para a pasta% SystemRoot% \\ System32 e uma atualização do registro deve ser feita para o pacote de notificação. Para obter informações sobre a atualização do registro, consulte [registrando um pacote de notificação do Winlogon](registering-a-winlogon-notification-package.md).

 

 
