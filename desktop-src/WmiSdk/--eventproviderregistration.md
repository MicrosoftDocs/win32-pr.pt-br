---
description: Usado para registrar provedores de eventos com Windows WMI (Instrumentação de Gerenciamento de Dados).
ms.assetid: d87f61a8-5549-4f33-ba67-31b5d72b5282
ms.tgt_platform: multiple
title: __EventProviderRegistration classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: ce973f05aec0a1c859598c558ef8c2cc637a8faec22fd1d7f2ad2aaf383bd201
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557940"
---
# <a name="__eventproviderregistration-class"></a>\_\_Classe EventProviderRegistration

A **\_ \_ classe de sistema EventProviderRegistration** é usada para registrar provedores de eventos com o WMI (Instrumentação de Gerenciamento de Windows).

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __EventProviderRegistration : __ProviderRegistration
{
  string         EventQueryList[];
  __Provider REF provider;
};
```

## <a name="members"></a>Membros

A **\_ \_ classe EventProviderRegistration** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **\_ \_ classe EventProviderRegistration** tem essas propriedades.

<dl> <dt>

**EventQueryList**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Uma ou mais Windows WQL (Linguagem de Consulta de Instrumentação de Gerenciamento) que descrevem os eventos aos qual o provedor de eventos dá suporte.

</dd> <dt>

**Provedor**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ \_ Provedor**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Caminho do objeto para o provedor de eventos. Essa propriedade é herdada [**\_ \_ de ProviderRegistration.**](--providerregistration.md)

</dd> </dl>

## <a name="remarks"></a>Comentários

Somente os administradores podem registrar ou excluir um provedor de eventos criando uma instância de [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ EventProviderRegistration**](--eventconsumerproviderregistration.md). A **\_ \_ classe EventProviderRegistration** é derivada de [**\_ \_ ProviderRegistration**](--providerregistration.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_ProviderRegistration**](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Registrando um provedor de eventos](registering-an-event-provider.md)
</dt> <dt>

[Escrevendo um provedor de eventos](writing-an-event-provider.md)
</dt> </dl>

 

