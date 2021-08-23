---
description: Representa a ocorrência de algum outro evento que está sendo descartado devido à falha de um consumidor de evento.
ms.assetid: bb6a1ce9-72a2-4528-8bc8-71ac053b6b1d
ms.tgt_platform: multiple
title: Classe __ConsumerFailureEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ConsumerFailureEvent
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: e8276716a1ca706a0027f35f9b554b960efebadacf3d8841b23415a43a9663c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732934"
---
# <a name="__consumerfailureevent-class"></a>\_\_Classe ConsumerFailureEvent

A classe de sistema **\_ \_ ConsumerFailureEvent** representa a ocorrência de algum outro evento que está sendo descartado devido à falha de um consumidor de evento.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __ConsumerFailureEvent : __EventDroppedEvent
{
  uint32              ErrorCode;
  string              ErrorDescription;
  object              ErrorObject;
  object              Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ ConsumerFailureEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ ConsumerFailureEvent** tem essas propriedades.

<dl> <dt>

**ErrorCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Código de erro retornado pelo consumidor.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição do código de erro estendido, se disponível.

</dd> <dt>

**Erroobject**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Objeto com erro.

</dd> <dt>

**Evento**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Evento em erro. Essa propriedade é herdada de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).

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

A classe **\_ \_ ConsumerFailureEvent** é derivada de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).

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

 

