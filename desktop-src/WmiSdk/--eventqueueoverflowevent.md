---
description: Relata quando um evento é Descartado como resultado do estouro da fila de entrega.
ms.assetid: 7cb1ef3b-3b0a-4f72-96de-862022fd6db8
ms.tgt_platform: multiple
title: Classe __EventQueueOverflowEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventQueueOverflowEvent
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 058b03b8a3311aad805f47a04d20e9f1fa8c2477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788627"
---
# <a name="__eventqueueoverflowevent-class"></a>\_\_Classe EventQueueOverflowEvent

A classe de sistema **\_ \_ EventQueueOverflowEvent** relata quando um evento é Descartado como resultado do estouro da fila de entrega.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __EventQueueOverflowEvent : __EventDroppedEvent
{
  uint32              CurrentQueueSize;
  object              Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ EventQueueOverflowEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ EventQueueOverflowEvent** tem essas propriedades.

<dl> <dt>

**CurrentQueueSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tamanho da fila atual, em bytes. Essa propriedade usa como padrão 10 MB para todas as filas combinadas.

</dd> <dt>

**Evento**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Evento de interesse. Essa propriedade é herdada de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).

</dd> <dt>

**IntendedConsumer**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ \_ EventConsumer**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência ao consumidor pretendido. Essa propriedade é herdada de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).

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

</dd> </dl>

## <a name="remarks"></a>Comentários

Somente os usuários com privilégios de administrador podem receber esse evento. A classe **\_ \_ EventQueueOverflowEvent** é derivada de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).

Para obter mais informações, consulte a propriedade [**MaximumQueueSize**](--eventconsumer.md) na classe [**\_ \_ EventConsumer**](--eventconsumer.md) e a propriedade [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) na classe **Win32 \_ WMISetting** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_EventDroppedEvent**](/windows/desktop/WmiSdk/--eventdroppedevent)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

