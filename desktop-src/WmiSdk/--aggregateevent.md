---
description: Representa um evento de agregação de vários eventos intrínsecos ou extrínsecos individuais.
ms.assetid: 99afa390-01fe-4a13-ba21-27587470f111
ms.tgt_platform: multiple
title: Classe __AggregateEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __AggregateEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: f93a962e57452ac555214e42f00af8ac8a4ea3db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796289"
---
# <a name="__aggregateevent-class"></a>\_\_Classe AggregateEvent

A classe de sistema **\_ \_ AggregateEvent** representa um evento agregado de vários eventos intrínsecos ou extrínsecos individuais. O WMI gera uma instância de **\_ \_ AggregateEvent** em vez de [**\_ \_ evento**](--event.md) quando os consumidores se registram com a cláusula [Group Within](group-clause.md) em sua consulta de evento.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __AggregateEvent : __IndicationRelated
{
  uint32 NumberOfEvents;
  object Representative;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ AggregateEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ AggregateEvent** tem essas propriedades.

<dl> <dt>

**NumberOfEvents**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de eventos combinados para produzir esse único evento de resumo.

</dd> <dt>

**Representante**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Cópia de um dos eventos entregues no intervalo de agregação. Por exemplo, se um consumidor tiver se registrado para eventos de alteração da chave do registro do provedor de eventos do registro, **representaria** uma instância da classe **RegistryKeyChangeEvent** .

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **\_ \_ AggregateEvent** é derivada de [**\_ \_ IndicationRelated**](--indicationrelated.md), que não tem propriedades.

Provedores de eventos nunca geram eventos de agregação. Eles devem ignorar a cláusula GROUP WITHIN em seu processamento de consultas de eventos.

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

[Consultando com WQL](querying-with-wql.md)
</dt> </dl>

 

