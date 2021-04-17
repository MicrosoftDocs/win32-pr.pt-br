---
description: Usado para registrar provedores de eventos com Instrumentação de Gerenciamento do Windows (WMI).
ms.assetid: d87f61a8-5549-4f33-ba67-31b5d72b5282
ms.tgt_platform: multiple
title: Classe __EventProviderRegistration
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
ms.openlocfilehash: caaad1b4ab03cfc1b43e4239b9144d3ceeade82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811495"
---
# <a name="__eventproviderregistration-class"></a>\_\_Classe EventProviderRegistration

A classe de sistema **\_ \_ EventProviderRegistration** é usada para registrar provedores de eventos com instrumentação de gerenciamento do Windows (WMI).

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

A classe **\_ \_ EventProviderRegistration** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ EventProviderRegistration** tem essas propriedades.

<dl> <dt>

**EventQueryList**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Uma ou mais consultas WQL (linguagem de consulta Instrumentação de Gerenciamento do Windows) que descrevem os eventos aos quais o provedor de eventos dá suporte.

</dd> <dt>

**operador**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ \_ provedor**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Caminho do objeto para o provedor de eventos. Essa propriedade é herdada de [**\_ \_ ProviderRegistration**](--providerregistration.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Somente os administradores podem registrar ou excluir um provedor de eventos criando uma instância do [**\_ \_ Win32Provider**](--win32provider.md) e do [**\_ \_ EventProviderRegistration**](--eventconsumerproviderregistration.md). A classe **\_ \_ EventProviderRegistration** é derivada de [**\_ \_ ProviderRegistration**](--providerregistration.md).

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

[Registrando um provedor de eventos](registering-an-event-provider.md)
</dt> <dt>

[Escrevendo um provedor de eventos](writing-an-event-provider.md)
</dt> </dl>

 

