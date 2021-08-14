---
description: A tabela a seguir lista as classes para consumidores permanentes pré-instalados do WMI.
ms.assetid: 1239ea25-2835-4546-b66d-20a83704653e
ms.tgt_platform: multiple
title: Classes de consumidor padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f89463a459adb3dd800f77564002366c7500a2abbaa6010444ba7890802d5a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315273"
---
# <a name="standard-consumer-classes"></a>Classes de consumidor padrão

A tabela a seguir lista as classes para consumidores permanentes pré-instalados do WMI. Você pode criar instâncias dessas classes para fornecer a classe de consumidor permanente para fornecer o consumidor lógico que responde quando disparado pelos eventos especificados no filtro. Por exemplo, use a [**classe ActiveScriptEventConsumer**](activescripteventconsumer.md) para definir o script que é executado quando ocorre um evento especificado.

Para obter mais informações, [consulte Monitoramento e resposta a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md) e eventos de [monitoramento](monitoring-events.md).



| Classe                                                                        | Descrição                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActiveScriptEventConsumer**](activescripteventconsumer.md)               | Executa um script predefinido em uma linguagem de script arbitrária quando um evento é entregue a ele.<br/> Exemplo: [executando um script com base em um evento](running-a-script-based-on-an-event.md)<br/>                                         |
| [**CommandLineEventConsumer**](commandlineeventconsumer.md)                 | Inicia um processo arbitrário no contexto do sistema local quando um evento é entregue a ele.<br/> Exemplo: [executando um programa na linha de comando com base em um evento](running-a-program-from-the-command-line-based-on-an-event.md)<br/> |
| [**LogFileEventConsumer**](logfileeventconsumer.md)                         | Grava cadeias de caracteres personalizadas em um arquivo de log de texto quando os eventos são entregues a ele.<br/> Exemplo: [escrevendo em um arquivo de log com base em um evento](writing-to-a-log-file-based-on-an-event.md)<br/>                                                   |
| [**NTEventLogEventConsumer**](nteventlogeventconsumer.md)                   | Registra uma mensagem específica no log Windows eventos quando um evento é entregue a ele.<br/> Exemplo: [registro em log no log de eventos do NT com base em um evento](logging-to-nt-event-log-based-on-an-event.md)<br/>                                          |
| [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md) | Fornece dados de registro comuns a todas as instâncias da [**classe ActiveScriptEventConsumer.**](activescripteventconsumer.md)<br/>                                                                                                            |
| [**SMTPEventConsumer**](smtpeventconsumer.md)                               | Envia uma mensagem de email usando SMTP sempre que um evento é entregue a ele.<br/> Exemplo: [enviar email com base em um evento](sending-e-mail-based-on-an-event.md)<br/>                                                                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Eventos de monitoramento](monitoring-events.md)
</dt> <dt>

[Recebendo eventos em todos os momentos](receiving-events-at-all-times.md)
</dt> <dt>

[Executando um script com base em um evento](running-a-script-based-on-an-event.md)
</dt> <dt>

[Enviar email com base em um evento](sending-e-mail-based-on-an-event.md)
</dt> </dl>

 

 




