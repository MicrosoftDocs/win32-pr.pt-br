---
description: Representa um evento de modificação de classe, que é um tipo de evento intrínseco gerado quando uma classe é alterada no namespace.
ms.assetid: 77e8e025-d584-495d-98f8-71e7fb2c9698
ms.tgt_platform: multiple
title: Classe __ClassModificationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassModificationEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: a5561f7cdb0bcb434ae43fb393e39b3edba47987f47b15583702d96bdb3ded7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732946"
---
# <a name="__classmodificationevent-class"></a>\_\_Classe ClassModificationEvent

A classe de sistema **\_ \_ ClassModificationEvent** representa um evento de modificação de classe, que é um tipo de [evento intrínseco](determining-the-type-of-event-to-receive.md) gerado quando uma classe é alterada no namespace.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __ClassModificationEvent : __ClassOperationEvent
{
  object PreviousClass;
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ ClassModificationEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ ClassModificationEvent** tem essas propriedades.

<dl> <dt>

**PreviousClass**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Cópia da versão original da classe.

</dd> <dt>

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

Cópia da classe recém modificada relatada pelo evento de modificação de classe. Essa propriedade é herdada de [**\_ \_ ClassOperationEvent**](--classoperationevent.md).

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

A classe **\_ \_ ClassModificationEvent** é derivada de [**\_ \_ ClassOperationEvent**](--classoperationevent.md).

O evento relata as versões novas e antigas da definição de classe.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_ClassOperationEvent**](/windows/desktop/WmiSdk/--classoperationevent)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

