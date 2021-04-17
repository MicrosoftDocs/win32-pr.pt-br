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
# <a name="creating-a-new-permanent-event-consumer-class"></a><span data-ttu-id="6882a-104">Criando uma nova classe de consumidor de evento permanente</span><span class="sxs-lookup"><span data-stu-id="6882a-104">Creating a New Permanent Event Consumer Class</span></span>

<span data-ttu-id="6882a-105">Uma das primeiras etapas na criação de um consumidor de evento permanente é criar a classe WMI que descreve o consumidor do evento.</span><span class="sxs-lookup"><span data-stu-id="6882a-105">One of the first steps in creating a permanent event consumer is to create the WMI class that describes the event consumer.</span></span> <span data-ttu-id="6882a-106">Especificamente, a classe de consumidor de evento permanente define os parâmetros da ação implementada pelo consumidor físico.</span><span class="sxs-lookup"><span data-stu-id="6882a-106">Specifically, the permanent event consumer class defines the parameters of the action implemented by the physical consumer.</span></span>

<span data-ttu-id="6882a-107">O procedimento a seguir descreve como criar uma classe de consumidor de evento permanente.</span><span class="sxs-lookup"><span data-stu-id="6882a-107">The following procedure describes how to create a permanent event consumer class.</span></span>

<span data-ttu-id="6882a-108">**Para criar uma classe de consumidor de evento permanente**</span><span class="sxs-lookup"><span data-stu-id="6882a-108">**To create a permanent event consumer class**</span></span>

1.  <span data-ttu-id="6882a-109">Derive uma classe da classe de sistema [**\_ \_ EventConsumer**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="6882a-109">Derive a class from the [**\_\_EventConsumer**](--eventconsumer.md) system class.</span></span>
2.  <span data-ttu-id="6882a-110">Implemente todos os parâmetros necessários para processar uma notificação de eventos.</span><span class="sxs-lookup"><span data-stu-id="6882a-110">Implement any parameters necessary to process an event notification.</span></span>

<span data-ttu-id="6882a-111">O exemplo a seguir mostra a sintaxe usada para criar a classe SMTPConsumerEvent.</span><span class="sxs-lookup"><span data-stu-id="6882a-111">The following example shows the syntax used to create the SMTPConsumerEvent class.</span></span> <span data-ttu-id="6882a-112">Você pode usar isso como um exemplo para criar sua nova classe.</span><span class="sxs-lookup"><span data-stu-id="6882a-112">You can use this as an example for creating your new class.</span></span> <span data-ttu-id="6882a-113">A classe [**SMTPEventConsumer**](smtpeventconsumer.md) envia uma mensagem de email usando o protocolo SMTP sempre que um evento é entregue a ele.</span><span class="sxs-lookup"><span data-stu-id="6882a-113">The [**SMTPEventConsumer**](smtpeventconsumer.md) class sends an email message by using Simple Mail Transfer Protocol (SMTP) each time an event is delivered to it.</span></span> <span data-ttu-id="6882a-114">Essa classe é definida em smtpcons. mof.</span><span class="sxs-lookup"><span data-stu-id="6882a-114">This class is defined in smtpcons.mof.</span></span>

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

<span data-ttu-id="6882a-115">Você deve ser capaz de criar instâncias de sua classe de consumidor de evento permanente para descrever uma ou mais maneiras de enviar eventos para seu consumidor físico.</span><span class="sxs-lookup"><span data-stu-id="6882a-115">You should be able to create instances of your permanent event consumer class to describe one or more ways to send events to your physical consumer.</span></span> <span data-ttu-id="6882a-116">Para obter mais informações, consulte [criando um consumidor lógico](creating-a-logical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="6882a-116">For more information, see [Creating a Logical Consumer](creating-a-logical-consumer.md).</span></span>

 

 



