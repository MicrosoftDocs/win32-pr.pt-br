---
description: A classe de CPU HWConfig \_ é a classe de tipo de evento para eventos de configuração de CPU. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: a94714c6-009c-4300-a0a0-b7b3ce94f91e
title: HWConfig_CPU classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_CPU
- HWConfig_CPU.MHz
- HWConfig_CPU.NumberOfProcessors
- HWConfig_CPU.MemSize
- HWConfig_CPU.PageSize
- HWConfig_CPU.AllocationGranularity
- HWConfig_CPU.ComputerName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9987095c8c2a1e9b9abbb54eb66816277428e2296c98395d36340297cc541bfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070186"
---
# <a name="hwconfig_cpu-class"></a>Classe de CPU HWConfig \_

A **classe de \_ CPU HWConfig** é a classe de tipo de evento para eventos de configuração de CPU.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType(10), EventTypeName("CPU")]
class HWConfig_CPU : HWConfig
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  string ComputerName;
};
```

## <a name="members"></a>Membros

A **classe de \_ CPU HWConfig** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe de \_ CPU HWConfig** tem essas propriedades.

<dl> <dt>

AllocationGranularity
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(5)
</dt> </dl>

Granularidade com a qual a memória virtual é alocada.

</dd> <dt>

ComputerName
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(6), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Nome do computador.

</dd> <dt>

MemSize
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(3)
</dt> </dl>

Quantidade total de memória física disponível para o sistema operacional.

</dd> <dt>

Mhz
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(1)
</dt> </dl>

Velocidade máxima do processador, em megahertz.

</dd> <dt>

NumberOfProcessors
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(2)
</dt> </dl>

Número de processadores no computador.

</dd> <dt>

PageSize
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(4)
</dt> </dl>

Tamanho de uma página de permuta, em bytes.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**HWConfig**](hwconfig.md)
</dt> </dl>

 

 




