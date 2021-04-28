---
description: Classe SystemConfig_Services-essa classe é a classe de tipo de evento para eventos de configuração de serviço.
ms.assetid: 7cba9992-d154-44b8-87d8-b46a8438f607
title: Classe SystemConfig_Services
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Services
- SystemConfig_Services.ProcessId
- SystemConfig_Services.ServiceState
- SystemConfig_Services.SubProcessTag
- SystemConfig_Services.ServiceName
- SystemConfig_Services.DisplayName
- SystemConfig_Services.ProcessName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 754b0e10c3882911c6e91fc2590c11739c3f7531
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106054"
---
# <a name="systemconfig_services-class"></a>Classe de serviços SystemConfigs \_

Essa classe é a classe de tipo de evento para eventos de configuração de serviço.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType(15), EventTypeName("Services")]
class SystemConfig_Services : SystemConfig
{
  uint32 ProcessId;
  uint32 ServiceState;
  uint32 SubProcessTag;
  string ServiceName[];
  string DisplayName[];
  string ProcessName[];
};
```

## <a name="members"></a>Membros

A classe de **\_ Serviços SystemConfigs** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ Serviços SystemConfigs** tem essas propriedades.

<dl> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (5), **StringTermination ("NullTerminated")**, **Format ("w")**
</dt> </dl>

Nome de exibição do serviço. O nome é, por caso, preservado no Gerenciador de controle de serviço. No entanto, as comparações do nome para exibição nunca fazem diferenciação de maiúsculas e minúsculas.

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (1), **formato ("x")**
</dt> </dl>

Identificador do processo no qual o serviço é executado.

</dd> <dt>

**ProcessName**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (6), **StringTermination ("NullTerminated")**, **Format ("w")**
</dt> </dl>

Nome do processo no qual o serviço é executado.

</dd> <dt>

**ServiceName**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (4), **StringTermination ("NullTerminated")**, **Format ("w")**
</dt> </dl>

Identificador exclusivo do serviço. O identificador fornece uma indicação da funcionalidade que o serviço fornece.

</dd> <dt>

**ServiceState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (2), **formato ("x")**
</dt> </dl>

Estado atual do serviço. Para obter os valores possíveis, consulte o membro **dwCurrentState** do **processo de \_ status \_ do serviço**.

</dd> <dt>

**SubProcessTag**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (3), **formato ("x")**
</dt> </dl>

Identifica o serviço.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




