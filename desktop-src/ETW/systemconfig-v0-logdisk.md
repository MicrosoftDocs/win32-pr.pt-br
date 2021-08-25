---
description: Classe SystemConfig_V0_LogDisk-essa classe é a classe de tipo de evento para eventos de configuração de disco lógico.
ms.assetid: 3fa5f2e4-f6fa-4c10-9634-04908783cd28
title: Classe SystemConfig_V0_LogDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_LogDisk
- SystemConfig_V0_LogDisk.StartOffset
- SystemConfig_V0_LogDisk.PartitionSize
- SystemConfig_V0_LogDisk.DiskNumber
- SystemConfig_V0_LogDisk.Size
- SystemConfig_V0_LogDisk.DriveType
- SystemConfig_V0_LogDisk.DriveLetterString
- SystemConfig_V0_LogDisk.Pad
- SystemConfig_V0_LogDisk.PartitionNumber
- SystemConfig_V0_LogDisk.SectorsPerCluster
- SystemConfig_V0_LogDisk.BytesPerSector
- SystemConfig_V0_LogDisk.NumberOfFreeClusters
- SystemConfig_V0_LogDisk.TotalNumberOfClusters
- SystemConfig_V0_LogDisk.FileSystem
- SystemConfig_V0_LogDisk.VolumeExt
api_type:
- NA
api_location: ''
ms.openlocfilehash: 42b17cf31dcb3830cd35f046a7fcbad1858f8ae4f728fc1417339962a4be4441
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927516"
---
# <a name="systemconfig_v0_logdisk-class"></a>\_Classe SystemConfig V0 \_ LogDisk

Essa classe é a classe de tipo de evento para eventos de configuração de disco lógico.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class SystemConfig_V0_LogDisk : SystemConfig_V0
{
  uint64 StartOffset;
  uint64 PartitionSize;
  uint32 DiskNumber;
  uint32 Size;
  uint32 DriveType;
  char16 DriveLetterString[];
  uint32 Pad;
  uint32 PartitionNumber;
  uint32 SectorsPerCluster;
  uint32 BytesPerSector;
  sint64 NumberOfFreeClusters;
  sint64 TotalNumberOfClusters;
  char16 FileSystem;
  uint32 VolumeExt;
};
```

## <a name="members"></a>Membros

A classe **SystemConfig \_ V0 \_ LogDisk** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **SystemConfig \_ V0 \_ LogDisk** tem essas propriedades.

<dl> <dt>

**BytesPerSector**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (10)
</dt> </dl>

Número de bytes em cada setor para a unidade de disco físico.

</dd> <dt>

**DiskNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (3)
</dt> </dl>

Número de índice do disco que contém esta partição.

</dd> <dt>

**DriveLetterString**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **char16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (6), **Max** (4)
</dt> </dl>

Letra da unidade do disco no formato " <letter> :".

</dd> <dt>

**DriveType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (5)
</dt> </dl>

Tipo de unidade de disco. Os valores possíveis são:



| Valor                                                                        | Significado                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>1</dt> </dl> | Partition<br/>                            |
| <dl> <dt>2</dt> </dl> | Volume<br/>                               |
| <dl> <dt>3</dt> </dl> | Partição estendida em vários discos<br/> |



 

</dd> <dt>

**FileSystem**
</dt> <dd> <dl> <dt>

Tipo de dados: **char16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (13), **máx** . (16)
</dt> </dl>

Sistema de arquivos no disco lógico, por exemplo, NTFS.

</dd> <dt>

**NumberOfFreeClusters**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (11)
</dt> </dl>

Número de clusters livres no volume especificado.

</dd> <dt>

**Pad**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (7)
</dt> </dl>

Reservado.

</dd> <dt>

**PartitionNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (8)
</dt> </dl>

Número de índice da partição.

</dd> <dt>

**PartitionSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (2)
</dt> </dl>

Tamanho total da partição, em bytes.

</dd> <dt>

**SectorsPerCluster**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (9)
</dt> </dl>

Número de setores no volume.

</dd> <dt>

**Tamanho**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (4)
</dt> </dl>

Tamanho da unidade de disco, em bytes.

</dd> <dt>

**StartOffset**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (1)
</dt> </dl>

Deslocamento inicial (em bytes) da partição desde o início do disco.

</dd> <dt>

**TotalNumberOfClusters**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (12)
</dt> </dl>

Número de clusters usados e livres no volume.

</dd> <dt>

**VolumeExt**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (14)
</dt> </dl>

Reservado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                            |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 




