---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 40d26ea1-3081-4afd-8b12-bc6521fad390
ms.tgt_platform: multiple
title: E (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffbd1ce4685ee9901dfedca2a4b3a1b948d91c8f5b56def28494eb6c4c63e726
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319215"
---
# <a name="e-wmi"></a>E (WMI)

[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) E [F](gloss-f.md) G [H](gloss-h.md) [i](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_event_class"></span><span id="WMI.GLOSS_EVENT_CLASS"></span>**classe de evento**
</dt> <dd>

Uma classe WMI que os *consumidores de eventos* podem assinar por uma consulta de *evento*. A classe relata um tipo específico de ocorrência. Por exemplo, a classe [**Win32 \_ ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) relata que um processo específico foi interrompido.

</dd> <dt>

<span id="wmi.gloss_event_consumer"></span><span id="WMI.GLOSS_EVENT_CONSUMER"></span>**consumidor de evento**
</dt> <dd>

Um destinatário de notificações que relatam uma ocorrência de um evento. Um consumidor de eventos é [*temporário*](gloss-t.md) ou [*permanente*](gloss-p.md).

</dd> <dt>

<span id="wmi.gloss_event_consumer_provider"></span><span id="WMI.GLOSS_EVENT_CONSUMER_PROVIDER"></span>**provedor de consumidor de eventos**
</dt> <dd>

Um provedor que determina qual consumidor de evento permanente manipula um determinado evento. Um provedor de consumidor de eventos é registrado com o WMI por uma instância de [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md), que contém uma lista das classes de [*consumidor lógicas*](gloss-l.md) que o provedor de consumidor de eventos suporta. Um provedor de consumidor de eventos é um servidor COM que mapeia [*consumidores físicos*](gloss-p.md) para *consumidores lógicos*. Um provedor de consumidor de eventos dá suporte à interface [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) e é um componente da arquitetura de consumidor permanente.

</dd> <dt>

<span id="wmi.gloss_event_filter"></span><span id="WMI.GLOSS_EVENT_FILTER"></span>**filtro de eventos**
</dt> <dd>

Uma instância da classe de sistema [**\_ \_ EventFilter**](--eventfilter.md) que descreve um tipo de evento e as condições para entregar uma notificação. Um consumidor usa um filtro de eventos para se registrar para receber a notificação de um tipo específico de evento.

</dd> <dt>

<span id="wmi.gloss_event_provider"></span><span id="WMI.GLOSS_EVENT_PROVIDER"></span>**provedor de eventos**
</dt> <dd>

Um provedor WMI que monitora uma fonte de eventos e notifica o WMI quando ocorrem eventos. Um provedor de eventos implementa as interfaces [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) e, às vezes, [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink).

</dd> <dt>

<span id="wmi.gloss_event_query"></span><span id="WMI.GLOSS_EVENT_QUERY"></span>**consulta de evento**
</dt> <dd>

Uma instrução [*linguagem WQL*](gloss-w.md) que os consumidores de eventos usam para se registrar para receber notificações de eventos específicos. Um provedor de eventos usa uma consulta de evento para se registrar para gerar notificações de eventos específicos.

</dd> <dt>

<span id="wmi.gloss_extension_schema"></span><span id="WMI.GLOSS_EXTENSION_SCHEMA"></span>**esquema de extensão**
</dt> <dd>

a terceira camada do [*esquema cim*](gloss-c.md), que inclui extensões específicas da plataforma do esquema cim, como Windows, UNIX e Exchange Server. Consulte também [*modelo comum*](gloss-c.md) e modelo de núcleo.

</dd> <dt>

<span id="wmi.gloss_extrinsic_event"></span><span id="WMI.GLOSS_EXTRINSIC_EVENT"></span>**evento extrínsecos**
</dt> <dd>

Uma notificação de evento de um provedor. A maioria dos provedores cria uma instância de uma classe de evento definida nos arquivos MOF do provedor. Um evento extrínsecos herda de [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md). Por exemplo, o [provedor de log de eventos](/previous-versions/windows/desktop/eventlogprov/event-log-provider) define a classe de evento [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent). Consulte também [*evento intrínseco*](gloss-i.md).

</dd> </dl>

 

 
