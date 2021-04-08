---
description: Uma das maneiras mais comuns de receber um evento é por meio de um aplicativo em execução, como um aplicativo de gerenciamento que coleta e exibe eventos para um usuário.
ms.assetid: 380ac556-ba0a-4fae-8b76-0645d99e8583
ms.tgt_platform: multiple
title: Recebendo eventos para a duração do seu aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd6b9731dd662a92296a86910a6cf8cb231cca1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010766"
---
# <a name="receiving-events-for-the-duration-of-your-application"></a>Recebendo eventos para a duração do seu aplicativo

Uma das maneiras mais comuns de receber um evento é por meio de um aplicativo em execução, como um aplicativo de gerenciamento que coleta e exibe eventos para um usuário. Esses aplicativos são chamados de "temporários" porque um consumidor temporário não recebe notificações de eventos quando ele é desligado.

Um consumidor temporário chama [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) no script ou [**IWbemServices.ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) no C++ para assinar eventos em um namespace. A identidade associada a essa assinatura é o chamador.

Um consumidor de evento temporário pode receber notificações de forma assíncrona ou semisynchronously em scripts e em C++.

> [!Note]  
> Por motivos de segurança, é importante observar que as notificações de eventos assíncronos não são recomendadas. Para obter mais informações, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md). Os consumidores de eventos têm preocupações de segurança especiais. Para obter mais informações, consulte [SECURING WMI Events](securing-wmi-events.md).

 

Para obter mais informações sobre como receber notificações de eventos assíncronas e semisynchronous, consulte [recebendo notificações de eventos assíncronos](receiving-asynchronous-event-notifications.md) e [recebendo notificações de eventos de semisynchronous](receiving-synchronous-and-semisynchronous-event-notifications.md).

 

 



