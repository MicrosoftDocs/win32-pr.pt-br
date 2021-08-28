---
description: Serve como uma classe pai para todos os tipos de evento definidos pelo usuário, também conhecidos como eventos extrínteses.
ms.assetid: 8fddbcd1-7393-4a3b-8a10-a8b620efc19f
ms.tgt_platform: multiple
title: __ExtrinsicEvent classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ExtrinsicEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 592632a7d0b5593a9de200062ef1ae6b167e72aaa2d2f41c44a8f955324b6b6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118321015"
---
# <a name="__extrinsicevent-class"></a>\_\_Classe ExtrinsicEvent

A **\_ \_ classe de sistema ExtrinsicEvent** é uma classe base abstrata que serve como uma classe pai para todos os tipos de evento definidos pelo usuário, também conhecidos como [eventos extrítico.](determining-the-type-of-event-to-receive.md)

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __ExtrinsicEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Membros

A **\_ \_ classe ExtrinsicEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **\_ \_ classe ExtrinsicEvent** tem essas propriedades.

<dl> <dt>

**DESCRITOR \_ DE SEGURANÇA**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento. Essa propriedade é herdada do [**\_ \_ Evento**](--event.md). Para obter mais informações sobre constantes usadas para definir esse descritor de segurança, consulte [Constantes de segurança WMI](wmi-security-constants.md).

</dd> <dt>

**TEMPO \_ CRIADO**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Valor exclusivo que indica a hora em que o evento foi gerado. Esse é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601. As informações estão no formato UTC (Tempos Universais Coordenados). Essa propriedade é herdada do [**\_ \_ Evento**](--event.md).

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Comentários

A **\_ \_ classe ExtrinsicEvent** é derivada de [**\_ \_ Event**](--event.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_Evento**](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

