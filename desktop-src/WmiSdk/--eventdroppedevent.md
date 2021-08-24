---
description: Representa a ocorrência de um evento que é descartado. Um evento descartado é um evento que não é entregue a um consumidor de eventos.
ms.assetid: fae267a9-e0ec-43fa-a3c3-d50345775a1d
ms.tgt_platform: multiple
title: __EventDroppedEvent classe
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
ms.openlocfilehash: 695381a3471dcc744cae10622ee9e7935b2770941a770bd0e4e4e93e591a9220
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051084"
---
# <a name="__eventdroppedevent-class"></a>\_\_Classe EventDroppedEvent

A **\_ \_ classe de sistema EventDroppedEvent** representa a ocorrência de um evento que é descartado. Um evento descartado é um evento que não é entregue a um consumidor de eventos.

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

A **\_ \_ classe EventDroppedEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **\_ \_ classe EventDroppedEvent** tem essas propriedades.

<dl> <dt>

**Evento**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ \_ Evento**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Evento que é descartado.

</dd> <dt>

**IntendedConsumer**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ \_ EventConsumer**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência a uma instância do [**\_ \_ EventConsumer que representa**](--eventconsumer.md) o consumidor permanente que você identifica para receber um evento. Diferentes consumidores permanentes que assinam um evento podem continuar recebendo o evento.

</dd> <dt>

**DESCRITOR \_ DE SEGURANÇA**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descritor que um provedor de eventos usa para determinar os usuários que podem receber um evento. Essa propriedade é herdada do [**\_ \_ Evento**](--event.md).

</dd> <dt>

**TEMPO \_ CRIADO**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Valor exclusivo que indica a hora em que um evento é gerado. Esse é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601. As informações estão no formato Tempo Universal Coordenado (UTC). Essa propriedade é herdada do [**\_ \_ Evento**](--event.md).

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Comentários

A **\_ \_ classe EventDroppedEvent** é derivada de [**\_ \_ SystemEvent.**](--systemevent.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_SystemEvent**](/windows/desktop/WmiSdk/--systemevent)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

