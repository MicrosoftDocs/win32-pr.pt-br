---
description: É uma classe base abstrata que é usada no registro de um consumidor de evento permanente.
ms.assetid: c1dc9a91-76f9-4527-ad69-0323a9aef28a
ms.tgt_platform: multiple
title: Classe __EventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumer
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: b8478b76aebf293d562129d047330f33e52706b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922877"
---
# <a name="__eventconsumer-class"></a>\_\_Classe EventConsumer

A classe de sistema **\_ \_ EventConsumer** é uma classe base abstrata que é usada no registro de um consumidor de evento permanente. Você pode derivar uma nova classe de consumidor de eventos de **\_ \_ EventConsumer**.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[abstract]
class __EventConsumer : __IndicationRelated
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ EventConsumer** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ EventConsumer** tem essas propriedades.

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

SID (identificador de segurança) que identifica exclusivamente o usuário que cria um filtro. O WMI armazena o SID do usuário que cria uma instância de **\_ \_ EventConsumer** ou o SID do administrador, dependendo do sistema operacional. Para obter mais informações, consulte [associando um filtro de eventos a um consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md) e [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome do computador ao qual Instrumentação de Gerenciamento do Windows (WMI) envia eventos.

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Fila máxima para um consumidor específico, em bytes.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **\_ \_ EventConsumer** é derivada de [**\_ \_ IndicationRelated**](--indicationrelated.md), que não tem propriedades.

Os consumidores permanentes definem novas classes de consumidor para descrever uma ação a ser tomada e os dados a serem processados quando os consumidores recebem notificações de eventos. Os consumidores permanentes têm preocupações especiais de segurança. Para obter mais informações, consulte [SECURING WMI Events](securing-wmi-events.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_IndicationRelated**](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Recebendo eventos em todos os momentos](receiving-events-at-all-times.md)
</dt> <dt>

[Criando uma nova classe de consumidor de evento permanente](creating-a-new-permanent-event-consumer-class.md)
</dt> <dt>

[Criando um consumidor lógico](creating-a-logical-consumer.md)
</dt> <dt>

[Protegendo eventos WMI](securing-wmi-events.md)
</dt> </dl>

 

