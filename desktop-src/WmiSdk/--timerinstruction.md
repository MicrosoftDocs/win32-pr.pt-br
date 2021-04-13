---
description: Especifica instruções sobre como os eventos de temporizador devem ser gerados para os consumidores.
ms.assetid: b08edb25-bedf-4014-a835-4050f5749479
ms.tgt_platform: multiple
title: Classe __TimerInstruction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __TimerInstruction
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5c6bbbf905a141fb7e9e3621c78709fd78999393
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297668"
---
# <a name="__timerinstruction-class"></a>\_\_Classe TimerInstruction

A classe de sistema abstrata **\_ \_ TimerInstruction** especifica instruções sobre como os [eventos de temporizador](receiving-a-timed-or-repeating-event.md) devem ser gerados para os consumidores.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[abstract]
class __TimerInstruction : __EventGenerator
{
  boolean SkipIfPassed = FALSE;
  string  TimerId;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ TimerInstruction** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ TimerInstruction** tem essas propriedades.

<dl> <dt>

**SkipIfPassed**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descreve se um evento de notificação será gerado e receberá quando um consumidor ficar disponível.

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

Cadeia de caracteres exclusiva atribuída pelo usuário que identifica esse evento de temporizador específico. Para evitar conflitos de nomenclatura com outros identificadores de temporizador, a forma de cadeia de caracteres de um GUID do estilo de ambiente de computador distribuído (DCE) pode ser usada. Essa propriedade faz parte da instância de [**\_ \_ TimerEvent**](--timerevent.md) que representa o evento.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **\_ \_ TimerInstruction** é derivada de [**\_ \_ EventGenerator**](--eventgenerator.md).

As subclasses **\_ \_ TimerInstruction** são [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md), usadas pelos consumidores para se registrar em um evento de timer absoluto e [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md), usadas para se registrar em um evento de timer de intervalo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_EventGenerator**](/windows/desktop/WmiSdk/--eventgenerator)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

