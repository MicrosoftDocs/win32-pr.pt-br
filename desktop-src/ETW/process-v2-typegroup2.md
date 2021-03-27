---
description: Essa classe é a classe de tipo de evento para eventos de contador de processo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 7f1fa1c4-a2ff-4a1c-ac9d-e922a13c99a1
title: Classe Process_V2_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V2_TypeGroup2
- Process_V2_TypeGroup2.ProcessId
- Process_V2_TypeGroup2.PageFaultCount
- Process_V2_TypeGroup2.HandleCount
- Process_V2_TypeGroup2.Reserved
- Process_V2_TypeGroup2.PeakVirtualSize
- Process_V2_TypeGroup2.PeakWorkingSetSize
- Process_V2_TypeGroup2.PeakPagefileUsage
- Process_V2_TypeGroup2.QuotaPeakPagedPoolUsage
- Process_V2_TypeGroup2.QuotaPeakNonPagedPoolUsage
- Process_V2_TypeGroup2.VirtualSize
- Process_V2_TypeGroup2.WorkingSetSize
- Process_V2_TypeGroup2.PagefileUsage
- Process_V2_TypeGroup2.QuotaPagedPoolUsage
- Process_V2_TypeGroup2.QuotaNonPagedPoolUsage
- Process_V2_TypeGroup2.PrivatePageCount
api_type:
- NA
api_location: ''
ms.openlocfilehash: 284b77da03b53f9c2662c8729a7bf6606c45630a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829683"
---
# <a name="process_v2_typegroup2-class"></a>\_Classe Process v2 \_ TypeGroup2

Essa classe é a classe de tipo de evento para eventos de contador de processo.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{32, 33}, EventTypeName{"PerfCtr", PerfCtrRundown"}]
class Process_V2_TypeGroup2 : Process_V2
{
  uint32 ProcessId;
  uint32 PageFaultCount;
  uint32 HandleCount;
  uint32 Reserved;
  object PeakVirtualSize;
  object PeakWorkingSetSize;
  object PeakPagefileUsage;
  object QuotaPeakPagedPoolUsage;
  object QuotaPeakNonPagedPoolUsage;
  object VirtualSize;
  object WorkingSetSize;
  object PagefileUsage;
  object QuotaPagedPoolUsage;
  object QuotaNonPagedPoolUsage;
  object PrivatePageCount;
};
```

## <a name="members"></a>Membros

A classe **process \_ v2 \_ TypeGroup2** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **process \_ v2 \_ TypeGroup2** tem essas propriedades.

<dl> <dt>

**HandleCount**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (3)
</dt> </dl>

Contagem de identificadores usados.

</dd> <dt>

**PageFaultCount**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (2)
</dt> </dl>

Contagem de falhas de página.

</dd> <dt>

**PagefileUsage**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (12), extensão ("tamanho")
</dt> </dl>

Uso do arquivo de paginação atual.

</dd> <dt>

**PeakPagefileUsage**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (7), extensão ("Tamanhot")
</dt> </dl>

Tamanho de arquivo de paginação maior usado.

</dd> <dt>

**PeakVirtualSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (5), extensão ("tamanho")
</dt> </dl>

Maior tamanho de página virtual usado.

</dd> <dt>

**PeakWorkingSetSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (6), extensão ("tamanho")
</dt> </dl>

Maior tamanho de conjunto de trabalho usado.

</dd> <dt>

**PrivatePageCount**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (15), extensão ("tamanho")
</dt> </dl>

Contagem de páginas físicas privadas atuais.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (1), formato ("x")
</dt> </dl>

Identificador de processo global que você pode usar para identificar um processo. O valor é válido a partir do momento em que um processo é criado até ser encerrado.

</dd> <dt>

**QuotaNonPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (14), extensão ("Tamanhot")
</dt> </dl>

Uso atual da memória não paginável confirmada.

</dd> <dt>

**QuotaPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (13), extensão ("tamanho")
</dt> </dl>

Uso atual da memória paginável confirmada.

</dd> <dt>

**QuotaPeakNonPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (9), extensão ("Tamanhot")
</dt> </dl>

Maior memória confirmada que não foi paginável usada.

</dd> <dt>

**QuotaPeakPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (8), extensão ("tamanho")
</dt> </dl>

Maior memória paginável confirmada usada.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (4)
</dt> </dl>

Reservado.

</dd> <dt>

**VirtualSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (10), extensão ("tamanho")
</dt> </dl>

Tamanho atual da página virtual.

</dd> <dt>

**WorkingSetSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (11), extensão ("Tamanhot")
</dt> </dl>

Tamanho atual do conjunto de trabalho.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esses eventos são registrados quando o processo termina. O evento indica como um processo tratou de uso de memória.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Processo \_ v2**](process-v2.md)
</dt> </dl>

 

 




