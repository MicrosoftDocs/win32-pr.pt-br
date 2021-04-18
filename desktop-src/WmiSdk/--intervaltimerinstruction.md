---
description: Gera eventos em intervalos, semelhantes a uma \_ mensagem de temporizador do WM na programação do Windows.
ms.assetid: 0895a743-a0dd-4833-a2bf-0196369e18b9
ms.tgt_platform: multiple
title: Classe __IntervalTimerInstruction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __IntervalTimerInstruction
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 20dd1c9fb2d009de4d8d957b4d5980cc6d6ff45e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797948"
---
# <a name="__intervaltimerinstruction-class"></a>\_\_Classe IntervalTimerInstruction

A classe de sistema **\_ \_ IntervalTimerInstruction** gera eventos em intervalos, semelhante a uma \_ mensagem de temporizador do WM na programação do Windows. Um consumidor de eventos registra-se para receber eventos de temporizador de intervalo criando uma consulta de evento que faz referência a essa classe. Devido ao comportamento do sistema operacional, não há nenhuma garantia de que os eventos serão entregues exatamente no intervalo solicitado.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __IntervalTimerInstruction : __TimerInstruction
{
  uint32  IntervalBetweenEvents;
  boolean SkipIfPassed = FALSE;
  string  TimerId;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ IntervalTimerInstruction** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ IntervalTimerInstruction** tem essas propriedades.

<dl> <dt>

**IntervalBetweenEvents**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](standard-qualifiers.md) (milissegundos)
</dt> </dl>

Número de milissegundos entre acionamentos de evento.

</dd> <dt>

**SkipIfPassed**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **for true**, esse evento será ignorado se o intervalo já for passado. O padrão é **false**. Essa propriedade é herdada de [**\_ \_ TimerInstruction**](--timerinstruction.md).

<dt>

FALSE
</dt> <dd>

Quando o WMI ou o consumidor se tornar disponível novamente, um evento de notificação será gerado e recebido.

</dd> <dt>

TRUE
</dt> <dd>

O evento de timer não ocorrerá se o WMI não estiver disponível para gerá-lo no intervalo de tempo apropriado ou se o consumidor solicitando receber o evento não estiver disponível.

</dd> </dl>

</dd> <dt>

**TimerId**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](standard-qualifiers.md)
</dt> </dl>

Identificador exclusivo deste objeto **\_ \_ IntervalTimerInstruction** . Essa propriedade é herdada de [**\_ \_ TimerInstruction**](--timerinstruction.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **\_ \_ IntervalTimerInstruction** é derivada de [**\_ \_ TimerInstruction**](--timerinstruction.md).

A consulta de evento inserida para se registrar em um evento de timer de intervalo geralmente é baseada na propriedade **timerId** . Eventos de notificação gerados a partir de um evento de temporizador de intervalo contêm a propriedade **NumFirings** que contém dados que refletem quantos eventos foram acionados durante o tempo em que os eventos não puderam ser recebidos. Se **SkipIfPassed** for definido como **true**, essas informações serão descartadas.

O valor da propriedade **IntervalBetweenEvents** deve ser razoavelmente grande. Se for muito pequeno, o WMI poderá ignorá-lo e não gerar o evento devido a limitações em alguns sistemas operacionais.

O WMI gera o evento de timer de intervalo criando uma instância da classe [**\_ \_ TimerEvent**](--timerevent.md) .

Para receber esses eventos de timer em um consumidor de evento temporário, execute [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) com a seguinte cadeia de caracteres de consulta de evento:


```sql
SELECT * FROM __TimerEvent WHERE TimerID = "MyEvent"
```



Para receber esses eventos de temporizador em um consumidor de evento permanente, você deve carregar a consulta anterior em um filtro de evento, definir um consumidor lógico e criar uma associação de filtro para consumidor para o filtro e o consumidor. Para obter mais informações, consulte [recebendo eventos em todos os momentos](receiving-events-at-all-times.md).

## <a name="examples"></a>Exemplos

A declaração MOF a seguir mostra como gerar um evento de timer de intervalo com a propriedade de chave definida como "MyEvent" a cada 10 segundos:


```mof
instance of __IntervalTimerInstruction
{
  TimerId = "MyEvent";     // inherited from __TimerInstruction
  SkipIfPassed = FALSE;    // also inherited
  IntervalBetweenEvents = 10000;
};
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_TimerInstruction**](/windows/desktop/WmiSdk/--timerinstruction)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Recebendo eventos cronometrados ou repetidos](receiving-a-timed-or-repeating-event.md)
</dt> </dl>

 

