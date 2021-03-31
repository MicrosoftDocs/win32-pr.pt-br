---
description: Registra provedores de consumidor de eventos com o WMI.
ms.assetid: 31ff43dc-dc70-4ba0-866f-37445912f837
ms.tgt_platform: multiple
title: Classe __EventConsumerProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumerProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 38552519221018735c3c7543d9a1f3f2d4b680e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829508"
---
# <a name="__eventconsumerproviderregistration-class"></a>\_\_Classe EventConsumerProviderRegistration

A classe de sistema **\_ \_ EventConsumerProviderRegistration** registra provedores de consumidor de eventos com o WMI.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __EventConsumerProviderRegistration : __ProviderRegistration
{
  string         ConsumerClassNames[];
  __Provider REF provider;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ EventConsumerProviderRegistration** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ EventConsumerProviderRegistration** tem essas propriedades.

<dl> <dt>

**ConsumerClassNames**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Matriz de nomes das classes de consumidor lógicas às quais o provedor de consumidor de eventos dá suporte.

</dd> <dt>

**operador**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ \_ provedor**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Caminho do objeto para o provedor. Essa propriedade é herdada de [**\_ \_ ProviderRegistration**](--providerregistration.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **\_ \_ EventConsumerProviderRegistration** é derivada de [**\_ \_ ProviderRegistration**](--providerregistration.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_ProviderRegistration**](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Registrando um provedor de consumidor de eventos](registering-an-event-consumer-provider.md)
</dt> <dt>

[Escrevendo um provedor de consumidor de eventos](writing-an-event-consumer-provider.md)
</dt> </dl>

 

