---
description: Gera eventos em intervalos, semelhantes a uma mensagem TIMER \_ WM Windows programação.
ms.assetid: 0895a743-a0dd-4833-a2bf-0196369e18b9
ms.tgt_platform: multiple
title: __IntervalTimerInstruction classe
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
ms.openlocfilehash: 17f0c55edceb3c5fb009f49ae97e3765ec3e0255a82f8c75e133344379c24d90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640756"
---
# <a name="__intervaltimerinstruction-class"></a>\_\_Classe IntervalTimerInstruction

A **\_ \_ classe do sistema IntervalTimerInstruction** gera eventos em intervalos, semelhantes a uma mensagem TIMER WM \_ Windows programação. Um consumidor de eventos registra-se para receber eventos de temporizador de intervalo criando uma consulta de evento que faz referência a essa classe. Devido ao comportamento do sistema operacional, não há nenhuma garantia de que os eventos serão entregues exatamente no intervalo solicitado.

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

A **\_ \_ classe IntervalTimerInstruction** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **\_ \_ classe IntervalTimerInstruction** tem essas propriedades.

<dl> <dt>

**IntervalBetweenEvents**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Unidades**](standard-qualifiers.md) (milissegundos)
</dt> </dl>

Número de milissegundos entre acionamentos de eventos.

</dd> <dt>

**SkipIfPassed**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **TRUE**, esse evento será ignorado se o intervalo já tiver sido passado. O padrão é **FALSE.** Essa propriedade é herdada [**\_ \_ de TimerInstruction**](--timerinstruction.md).

<dt>

FALSE
</dt> <dd>

Quando o WMI ou o consumidor ficar disponível novamente, um evento de notificação será gerado e recebido.

</dd> <dt>

TRUE
</dt> <dd>

O evento de temporizador não ocorrerá se o WMI não estiver disponível para gerá-lo no intervalo de tempo apropriado ou se o consumidor solicitando para receber o evento não estiver disponível.

</dd> </dl>

</dd> <dt>

**Timerid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **Chave**](standard-qualifiers.md)
</dt> </dl>

Identificador exclusivo para este **\_ \_ objeto IntervalTimerInstruction.** Essa propriedade é herdada [**\_ \_ de TimerInstruction**](--timerinstruction.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A **\_ \_ classe IntervalTimerInstruction** é derivada de [**\_ \_ TimerInstruction**](--timerinstruction.md).

A consulta de evento inserida para se registrar para um evento de temporizador de intervalo geralmente é baseada na **propriedade TimerId.** Os eventos de notificação gerados de um evento de temporizador de intervalo contêm a propriedade **NumFirings** que contém dados que refletem quantos eventos disparados durante o tempo em que os eventos não puderam ser recebidos. Se **SkipIfPassed** for definido como **TRUE,** essas informações são descartadas.

O valor da **propriedade IntervalBetweenEvents** deve ser razoavelmente grande. Se for muito pequeno, o WMI poderá ignorá-lo e não gerar o evento devido a limitações em alguns sistemas operacionais.

O WMI gera o evento de temporizador de intervalo criando uma instância da [**\_ \_ classe TimerEvent.**](--timerevent.md)

Para receber esses eventos de temporizador em um consumidor de eventos temporário, execute [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) com a seguinte cadeia de caracteres de consulta de evento:


```sql
SELECT * FROM __TimerEvent WHERE TimerID = "MyEvent"
```



Para receber esses eventos de temporizador em um consumidor de eventos permanente, você deve carregar a consulta anterior em um filtro de evento, definir um consumidor lógico e criar uma associação de filtro para consumidor para o filtro e o consumidor. Para obter mais informações, consulte [Recebendo eventos em todos os momentos.](receiving-events-at-all-times.md)

## <a name="examples"></a>Exemplos

A seguinte declaração MOF mostra como gerar um evento de temporizador de intervalo com a propriedade de chave definida como "MyEvent" a cada 10 segundos:


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
| Namespace<br/>                | Todos os namespaces WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_TimerInstruction**](/windows/desktop/WmiSdk/--timerinstruction)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Recebendo eventos temporados ou repetidos](receiving-a-timed-or-repeating-event.md)
</dt> </dl>

 

