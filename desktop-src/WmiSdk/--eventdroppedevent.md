---
description: Representa a ocorrência de um evento que é Descartado. Um evento removido é um evento que não é entregue a um consumidor de evento.
ms.assetid: fae267a9-e0ec-43fa-a3c3-d50345775a1d
ms.tgt_platform: multiple
title: Classe __EventDroppedEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventDroppedEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 4e9f68328a3c5c455c98e85a65d53156da6eeada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763010"
---
# <a name="__eventdroppedevent-class"></a>\_\_Classe EventDroppedEvent

A classe de sistema **\_ \_ EventDroppedEvent** representa a ocorrência de um evento que é Descartado. Um evento removido é um evento que não é entregue a um consumidor de evento.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __EventDroppedEvent : __SystemEvent
{
  __Event             Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ EventDroppedEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ EventDroppedEvent** tem essas propriedades.

<dl> <dt>

**Evento**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ \_ evento**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Evento Descartado.

</dd> <dt>

**IntendedConsumer**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ \_ EventConsumer**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência a uma instância de [**\_ \_ EventConsumer**](--eventconsumer.md) que representa o consumidor permanente que você identifica para receber um evento. Diferentes consumidores permanentes que assinam um evento podem continuar a receber o evento.

</dd> <dt>

**\_descritor de segurança**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descritor que um provedor de eventos usa para determinar os usuários que podem receber um evento. Esta propriedade é herdada do [**\_ \_ evento**](--event.md).

</dd> <dt>

**HORA da \_ criação**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Valor exclusivo que indica a hora em que um evento é gerado. Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601. As informações estão no formato UTC (tempo Universal Coordenado). Esta propriedade é herdada do [**\_ \_ evento**](--event.md).

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **\_ \_ EventDroppedEvent** é derivada de [**\_ \_ SystemEvent**](--systemevent.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_SystemEvent**](/windows/desktop/WmiSdk/--systemevent)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

