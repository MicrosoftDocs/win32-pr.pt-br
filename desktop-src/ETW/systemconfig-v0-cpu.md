---
description: Classe SystemConfig_V0_CPU-essa classe é a classe de tipo de evento para eventos de configuração de CPU.
ms.assetid: 9ca77676-ff0e-4c47-ae4e-f8192376d3ca
title: Classe SystemConfig_V0_CPU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_CPU
- SystemConfig_V0_CPU.MHz
- SystemConfig_V0_CPU.NumberOfProcessors
- SystemConfig_V0_CPU.MemSize
- SystemConfig_V0_CPU.PageSize
- SystemConfig_V0_CPU.AllocationGranularity
- SystemConfig_V0_CPU.ComputerName
- SystemConfig_V0_CPU.DomainName
api_type:
- NA
api_location: ''
ms.openlocfilehash: de3b63def40cb6ead40f6f4c95625603cfc581ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105984"
---
# <a name="systemconfig_v0_cpu-class"></a>\_Classe de \_ CPU SystemConfig V0

Essa classe é a classe de tipo de evento para eventos de configuração de CPU.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType(10), EventTypeName("CPU")]
class SystemConfig_V0_CPU : SystemConfig_V0
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  char16 ComputerName[];
  char16 DomainName[];
};
```

## <a name="members"></a>Membros

A classe de **\_ \_ CPU SystemConfig V0** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ \_ CPU SystemConfig V0** tem essas propriedades.

<dl> <dt>

**AllocationGranularity**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (5)
</dt> </dl>

Granularidade com a qual a memória virtual é alocada.

</dd> <dt>

**ComputerName**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **char16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (6), **Max** (256)
</dt> </dl>

Nome do computador.

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **char16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (7), **Max** (132)
</dt> </dl>

Nome do domínio no qual o computador é membro.

</dd> <dt>

**MemSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (3)
</dt> </dl>

Quantidade total de memória física disponível para o sistema operacional.

</dd> <dt>

**GHz**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (1)
</dt> </dl>

Velocidade máxima do processador, em megahertz.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (2)
</dt> </dl>

Número de processadores no computador.

</dd> <dt>

**PageSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (4)
</dt> </dl>

Tamanho de uma página de permuta, em bytes.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 




