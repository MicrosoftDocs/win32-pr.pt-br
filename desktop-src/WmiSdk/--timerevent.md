---
description: Relata um evento gerado pelo WMI em resposta a uma solicitação de consumidores para um evento de temporizador de intervalo ou um evento de timer absoluto.
ms.assetid: 5ae29312-cfda-42c9-a154-e5bb31819be0
ms.tgt_platform: multiple
title: Classe __TimerEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __TimerEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 2de8967110568e968bb241ebbf4942bf1504b332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788014"
---
# <a name="__timerevent-class"></a>\_\_Classe TimerEvent

A classe de sistema **\_ \_ TimerEvent** é relata um evento gerado pelo WMI em resposta à solicitação de um consumidor para um evento de temporizador de intervalo ou um evento de timer absoluto. Um evento de timer de intervalo é um evento que ocorre em intervalos regulares. Um evento de timer absoluto é um evento que ocorre em um momento específico. Eventos de temporizador podem ocorrer em qualquer namespace.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __TimerEvent : __Event
{
  uint32 NumFirings;
  uint8  SECURITY_DESCRIPTOR[];
  string TimerId;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ TimerEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ TimerEvent** tem essas propriedades.

<dl> <dt>

**NumFirings**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de vezes que o evento ocorreu antes de uma notificação ser entregue ao consumidor.

</dd> <dt>

**\_descritor de segurança**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento. Esta propriedade é herdada do [**\_ \_ evento**](--event.md).

</dd> <dt>

**HORA da \_ criação**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Valor exclusivo que indica a hora em que o evento foi gerado. Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601. As informações estão no formato UTC (tempo Universal Coordenado). Esta propriedade é herdada do [**\_ \_ evento**](--event.md).

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**TimerId**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Instância da subclasse [**\_ \_ TimerInstruction**](--timerinstruction.md) que fez com que o WMI acionasse este evento. Os consumidores especificam uma identificação de temporizador na propriedade **timerId** da subclasse **\_ \_ TimerInstruction** que eles criam para se registrar.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **\_ \_ TimerEvent** é derivada de [**\_ \_ Event**](--event.md).

Os consumidores de eventos se registram em um evento de timer absoluto criando uma instância da classe de sistema [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md) . Eles se registram para um evento de temporizador de intervalo criando uma instância da classe de sistema [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md) .

Durante a operação normal, a propriedade **NumFirings** é definida como 1. Quando não é possível alcançar o consumidor ou o intervalo de acionamento é muito mais rápido do que a capacidade de entregar o evento, **NumFirings** é definido como um número maior que 1. Quando **NumFirings** é maior que 1, o WMI mescla automaticamente muitos eventos de timer no mesmo evento. Essa mesclagem é semelhante ao que ocorre com as mensagens de [**\_ temporizador do WM**](/windows/desktop/winmsg/wm-timer) na programação do Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_Evento**](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Recebendo eventos cronometrados ou repetidos](receiving-a-timed-or-repeating-event.md)
</dt> <dt>

[Recebendo eventos em todos os momentos](receiving-events-at-all-times.md)
</dt> <dt>

[Recebendo eventos para a duração do seu aplicativo](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

