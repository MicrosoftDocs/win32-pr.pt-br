---
description: A tabela a seguir lista as classes de consumidores permanentes pré-instalados do WMI.
ms.assetid: 1239ea25-2835-4546-b66d-20a83704653e
ms.tgt_platform: multiple
title: Classes de consumidor padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a5033077f3dabf90d3e935b2dfec9fad892f630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171975"
---
# <a name="standard-consumer-classes"></a><span data-ttu-id="5e064-103">Classes de consumidor padrão</span><span class="sxs-lookup"><span data-stu-id="5e064-103">Standard Consumer Classes</span></span>

<span data-ttu-id="5e064-104">A tabela a seguir lista as classes de consumidores permanentes pré-instalados do WMI.</span><span class="sxs-lookup"><span data-stu-id="5e064-104">The following table lists the classes for WMI preinstalled permanent consumers.</span></span> <span data-ttu-id="5e064-105">Você pode criar instâncias dessas classes para fornecer a classe de consumidor permanente para fornecer o consumidor lógico que responde quando disparado pelos eventos especificados no filtro.</span><span class="sxs-lookup"><span data-stu-id="5e064-105">You can create instances of these classes to provide the permanent consumer class to supply the logical consumer that responds when triggered by the events specified in the filter.</span></span> <span data-ttu-id="5e064-106">Por exemplo, use a classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) para definir o script que é executado quando um evento especificado ocorre.</span><span class="sxs-lookup"><span data-stu-id="5e064-106">For example, use the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class to define the script that executes when a specified event occurs.</span></span>

<span data-ttu-id="5e064-107">Para obter mais informações, consulte [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md) e [eventos de monitoramento](monitoring-events.md).</span><span class="sxs-lookup"><span data-stu-id="5e064-107">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md) and [Monitoring Events](monitoring-events.md).</span></span>



| <span data-ttu-id="5e064-108">Classe</span><span class="sxs-lookup"><span data-stu-id="5e064-108">Class</span></span>                                                                        | <span data-ttu-id="5e064-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e064-109">Description</span></span>                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e064-110">**ActiveScriptEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="5e064-110">**ActiveScriptEventConsumer**</span></span>](activescripteventconsumer.md)               | <span data-ttu-id="5e064-111">Executa um script predefinido em uma linguagem de script arbitrária quando um evento é entregue a ele.</span><span class="sxs-lookup"><span data-stu-id="5e064-111">Executes a predefined script in an arbitrary scripting language when an event is delivered to it.</span></span><br/> <span data-ttu-id="5e064-112">Exemplo: [executando um script com base em um evento](running-a-script-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="5e064-112">Example: [Running a Script Based on an Event](running-a-script-based-on-an-event.md)</span></span><br/>                                         |
| [<span data-ttu-id="5e064-113">**CommandLineEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="5e064-113">**CommandLineEventConsumer**</span></span>](commandlineeventconsumer.md)                 | <span data-ttu-id="5e064-114">Inicia um processo arbitrário no contexto do sistema local quando um evento é entregue a ele.</span><span class="sxs-lookup"><span data-stu-id="5e064-114">Launches an arbitrary process in the local system context when an event is delivered to it.</span></span><br/> <span data-ttu-id="5e064-115">Exemplo: [executando um programa da linha de comando com base em um evento](running-a-program-from-the-command-line-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="5e064-115">Example: [Running a Program from the Command Line Based on an Event](running-a-program-from-the-command-line-based-on-an-event.md)</span></span><br/> |
| [<span data-ttu-id="5e064-116">**LogFileEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="5e064-116">**LogFileEventConsumer**</span></span>](logfileeventconsumer.md)                         | <span data-ttu-id="5e064-117">Grava cadeias de caracteres personalizadas em um arquivo de log de texto quando os eventos são entregues a ele.</span><span class="sxs-lookup"><span data-stu-id="5e064-117">Writes customized strings to a text log file when events are delivered to it.</span></span><br/> <span data-ttu-id="5e064-118">Exemplo: [gravando em um arquivo de log baseado em um evento](writing-to-a-log-file-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="5e064-118">Example: [Writing to a Log File Based on an Event](writing-to-a-log-file-based-on-an-event.md)</span></span><br/>                                                   |
| [<span data-ttu-id="5e064-119">**NTEventLogEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="5e064-119">**NTEventLogEventConsumer**</span></span>](nteventlogeventconsumer.md)                   | <span data-ttu-id="5e064-120">Registra uma mensagem específica no log de eventos do Windows quando um evento é entregue a ele.</span><span class="sxs-lookup"><span data-stu-id="5e064-120">Logs a specific message to the Windows event log when an event is delivered to it.</span></span><br/> <span data-ttu-id="5e064-121">Exemplo: [log no log de eventos NT com base em um evento](logging-to-nt-event-log-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="5e064-121">Example: [Logging to NT Event Log Based on an Event](logging-to-nt-event-log-based-on-an-event.md)</span></span><br/>                                          |
| [<span data-ttu-id="5e064-122">**ScriptingStandardConsumerSetting**</span><span class="sxs-lookup"><span data-stu-id="5e064-122">**ScriptingStandardConsumerSetting**</span></span>](scriptingstandardconsumersetting.md) | <span data-ttu-id="5e064-123">Fornece dados de registro comuns a todas as instâncias da classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="5e064-123">Provides registration data common to all instances of the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="5e064-124">**SMTPEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="5e064-124">**SMTPEventConsumer**</span></span>](smtpeventconsumer.md)                               | <span data-ttu-id="5e064-125">Envia uma mensagem de email usando SMTP cada vez que um evento é entregue a ele.</span><span class="sxs-lookup"><span data-stu-id="5e064-125">Sends an email message using SMTP each time an event is delivered to it.</span></span><br/> <span data-ttu-id="5e064-126">Exemplo: [enviando email com base em um evento](sending-e-mail-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="5e064-126">Example: [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md)</span></span><br/>                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="5e064-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5e064-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e064-128">Eventos de monitoramento</span><span class="sxs-lookup"><span data-stu-id="5e064-128">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="5e064-129">Recebendo eventos em todos os momentos</span><span class="sxs-lookup"><span data-stu-id="5e064-129">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="5e064-130">Executando um script com base em um evento</span><span class="sxs-lookup"><span data-stu-id="5e064-130">Running a Script Based on an Event</span></span>](running-a-script-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="5e064-131">Enviando email com base em um evento</span><span class="sxs-lookup"><span data-stu-id="5e064-131">Sending Email Based on an Event</span></span>](sending-e-mail-based-on-an-event.md)
</dt> </dl>

 

 




