---
description: É uma classe base para todos os eventos intrínsecos relacionados a uma classe.
ms.assetid: 554bbabd-2639-40f5-8786-6df2188db0ec
ms.tgt_platform: multiple
title: Classe __ClassOperationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0c7a78219cec5c014e289dad4bf1cc29f0466a06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782673"
---
# <a name="__classoperationevent-class"></a>\_\_Classe ClassOperationEvent

A classe de sistema **\_ \_ ClassOperationEvent** é uma classe base para todos os eventos intrínsecos relacionados a uma classe.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __ClassOperationEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ ClassOperationEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ ClassOperationEvent** tem essas propriedades.

<dl> <dt>

**\_descritor de segurança**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento. Esta propriedade é herdada do [**\_ \_ evento**](--event.md).

</dd> <dt>

**TargetClass**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Classe afetada pelo evento. Para eventos de criação, essa é a classe recém-criada. Para eventos de modificação, esta é a nova versão da classe alterada. Para eventos de exclusão, essa é a classe excluída.

</dd> <dt>

**HORA da \_ criação**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Valor exclusivo que indica a hora em que o evento foi gerado. Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601. As informações estão no formato UTC (tempo Universal Coordenado). Esta propriedade é herdada do [**\_ \_ evento**](--event.md).

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **\_ \_ ClassOperationEvent** é derivada de [**\_ \_ Event**](--event.md).

As instâncias de **\_ \_ ClassOperationEvent** não são criadas; apenas instâncias de suas subclasses são criadas. As classes a seguir derivam de **\_ \_ ClassOperationEvent**:

[**\_\_ClassCreationEvent**](--classcreationevent.md)

[**\_\_ClassModificationEvent**](--classmodificationevent.md)

[**\_\_ClassDeletionEvent**](--classdeletionevent.md)

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

[Determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

