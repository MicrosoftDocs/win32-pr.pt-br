---
description: Faz com que um evento seja gerado em uma data específica em um momento específico.
ms.assetid: bcb64c81-3b40-4665-a880-a100629656e0
ms.tgt_platform: multiple
title: Classe __AbsoluteTimerInstruction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __AbsoluteTimerInstruction
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5f4f55e635e42ec34e9b3558a0784d319e4d91ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807182"
---
# <a name="__absolutetimerinstruction-class"></a>\_\_Classe AbsoluteTimerInstruction

A classe de sistema **\_ \_ AbsoluteTimerInstruction** faz com que um evento seja gerado em uma data específica em um momento específico. Um consumidor de eventos registra-se para receber um evento de timer absoluto criando uma instância dessa classe. O evento é gerado uma vez.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __AbsoluteTimerInstruction : __TimerInstruction
{
  datetime EventDateTime;
  boolean  SkipIfPassed = FALSE;
  string   TimerId;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ AbsoluteTimerInstruction** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ AbsoluteTimerInstruction** tem essas propriedades.

<dl> <dt>

**EventDateTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Cadeia de caracteres de comprimento fixo no [formato DMTF](date-and-time-format.md) que especifica quando o temporizador é acionado.

</dd> <dt>

**SkipIfPassed**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **for true**, o evento timer ocorrerá se o WMI não puder gerá-lo no intervalo de tempo correto ou se o consumidor solicitando receber o evento não estiver disponível. Se **for true**, o evento não ocorrerá. O padrão é **false**. Quando o WMI ou o consumidor se torna disponível, um evento de notificação é gerado e recebido. Essa propriedade é herdada de [**\_ \_ TimerInstruction**](--timerinstruction.md).

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

Cadeia de caracteres exclusiva atribuída pelo usuário que identifica um evento de temporizador específico. Para evitar conflitos de nomenclatura com outros identificadores de temporizador, a forma de cadeia de caracteres de um GUID de estilo de ambiente de computador distribuído pode ser usada. Essa propriedade é herdada de [**\_ \_ TimerInstruction**](--timerinstruction.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **\_ \_ AbsoluteTimerInstruction** é derivada de [**\_ \_ TimerInstruction**](--timerinstruction.md).

O WMI gera o evento de timer absoluto criando uma instância da classe [**\_ \_ TimerEvent**](--timerevent.md) .

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
</dt> <dt>

[Recebendo eventos em todos os momentos](receiving-events-at-all-times.md)
</dt> <dt>

[Recebendo eventos para a duração do seu aplicativo](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

