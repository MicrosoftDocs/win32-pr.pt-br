---
description: Uma das maneiras mais comuns de receber um evento é por meio de um aplicativo em execução, como um aplicativo de gerenciamento que coleta e exibe eventos para um usuário.
ms.assetid: 380ac556-ba0a-4fae-8b76-0645d99e8583
ms.tgt_platform: multiple
title: Recebendo eventos durante a duração do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6815c2ddd7725ccd12dd65b0047874ddce1038b2a2c07f90a40d6f87e6af3a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554214"
---
# <a name="receiving-events-for-the-duration-of-your-application"></a>Recebendo eventos durante a duração do aplicativo

Uma das maneiras mais comuns de receber um evento é por meio de um aplicativo em execução, como um aplicativo de gerenciamento que coleta e exibe eventos para um usuário. Esses aplicativos são chamados de "temporários" porque um consumidor temporário não recebe notificações de eventos quando desligado.

Um consumidor temporário [**chamaSWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) no script [**ouIWbemServices.ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) no C++ para assinar eventos em um namespace. A identidade associada a essa assinatura é o chamador.

Um consumidor de eventos temporários pode receber notificações de forma assíncrona ou semissíncrona em scripts e C++.

> [!Note]  
> Por motivos de segurança, é importante observar que as notificações de eventos assíncronas não são recomendadas. Para obter mais informações, consulte [Configurando a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md). Os consumidores de eventos têm preocupações de segurança especiais. Para obter mais informações, consulte [Proteger eventos WMI](securing-wmi-events.md).

 

Para obter mais informações sobre como receber notificações de eventos assíncronas e semisíncronas, consulte Recebendo notificações de eventos [assíncronas](receiving-asynchronous-event-notifications.md) e Recebendo notificações de eventos [semisíncronas](receiving-synchronous-and-semisynchronous-event-notifications.md).

 

 



