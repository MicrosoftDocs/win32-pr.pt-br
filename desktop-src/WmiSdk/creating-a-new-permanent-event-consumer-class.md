---
description: Uma das primeiras etapas na criação de um consumidor de evento permanente é criar a classe WMI que descreve o consumidor do evento. Especificamente, a classe de consumidor de evento permanente define os parâmetros da ação implementada pelo consumidor físico.
ms.assetid: a5b6d0b9-8df1-47e3-bb3b-cc69db6d9c0e
ms.tgt_platform: multiple
title: Criando uma nova classe de consumidor de evento permanente
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03f8ae8e1e83abcf3b340398d45aefde4c7141e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787658"
---
# <a name="creating-a-new-permanent-event-consumer-class"></a>Criando uma nova classe de consumidor de evento permanente

Uma das primeiras etapas na criação de um consumidor de evento permanente é criar a classe WMI que descreve o consumidor do evento. Especificamente, a classe de consumidor de evento permanente define os parâmetros da ação implementada pelo consumidor físico.

O procedimento a seguir descreve como criar uma classe de consumidor de evento permanente.

**Para criar uma classe de consumidor de evento permanente**

1.  Derive uma classe da classe de sistema [**\_ \_ EventConsumer**](--eventconsumer.md) .
2.  Implemente todos os parâmetros necessários para processar uma notificação de eventos.

O exemplo a seguir mostra a sintaxe usada para criar a classe SMTPConsumerEvent. Você pode usar isso como um exemplo para criar sua nova classe. A classe [**SMTPEventConsumer**](smtpeventconsumer.md) envia uma mensagem de email usando o protocolo SMTP sempre que um evento é entregue a ele. Essa classe é definida em smtpcons. mof.

``` syntax
class SMTPEventConsumer : __EventConsumer
{
  [key] string Name;
  [not_null] string SMTPServer;
  [Template] string Subject;
  [Template] string FromLine;
  [Template] string ReplyToLine;
  [Template] string Message;
  [Template] string ToLine;
  [Template] string CcLine;
  [Template] string BccLine;
  string HeaderFields[];
};
```

Você deve ser capaz de criar instâncias de sua classe de consumidor de evento permanente para descrever uma ou mais maneiras de enviar eventos para seu consumidor físico. Para obter mais informações, consulte [criando um consumidor lógico](creating-a-logical-consumer.md).

 

 



