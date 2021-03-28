---
description: Essa classe é a classe de tipo de evento para eventos de configuração de disco físico.
ms.assetid: 90ca3089-de5c-4e15-8abf-eaab9aafff06
title: Classe SystemConfig_V0_PhyDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_PhyDisk
- SystemConfig_V0_PhyDisk.DiskNumber
- SystemConfig_V0_PhyDisk.BytesPerSector
- SystemConfig_V0_PhyDisk.SectorsPerTrack
- SystemConfig_V0_PhyDisk.TracksPerCylinder
- SystemConfig_V0_PhyDisk.Cylinders
- SystemConfig_V0_PhyDisk.SCSIPort
- SystemConfig_V0_PhyDisk.SCSIPath
- SystemConfig_V0_PhyDisk.SCSITarget
- SystemConfig_V0_PhyDisk.SCSILun
- SystemConfig_V0_PhyDisk.Manufacturer
- SystemConfig_V0_PhyDisk.PartitionCount
- SystemConfig_V0_PhyDisk.WriteCacheEnabled
- SystemConfig_V0_PhyDisk.BootDriveLetter
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f7eab1cec90630e25ee5968e5740f787acb8662
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968148"
---
# <a name="systemconfig_v0_phydisk-class"></a>\_Classe SystemConfig V0 \_ PhyDisk

Essa classe é a classe de tipo de evento para eventos de configuração de disco físico.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class SystemConfig_V0_PhyDisk : SystemConfig_V0
{
  uint32  DiskNumber;
  uint32  BytesPerSector;
  uint32  SectorsPerTrack;
  uint32  TracksPerCylinder;
  uint64  Cylinders;
  uint32  SCSIPort;
  uint32  SCSIPath;
  uint32  SCSITarget;
  uint32  SCSILun;
  char16  Manufacturer[];
  uint32  PartitionCount;
  boolean WriteCacheEnabled;
  char16  BootDriveLetter[];
};
```

## <a name="members"></a>Membros

A classe **SystemConfig \_ V0 \_ PhyDisk** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **SystemConfig \_ V0 \_ PhyDisk** tem essas propriedades.

<dl> <dt>

**BootDriveLetter**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **char16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (13), **máx** . (3)
</dt> </dl>

Letra da unidade da unidade de inicialização no formato " <letter> :".

</dd> <dt>

**BytesPerSector**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (2)
</dt> </dl>

Número de bytes em cada setor para a unidade de disco físico.

</dd> <dt>

**Cilindros**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (5)
</dt> </dl>

Número total de cilindros na unidade de disco físico. Observação: o valor dessa propriedade é obtido por meio de funções estendidas de interrupção do BIOS 13h. O valor poderá ser impreciso se a unidade usar um esquema de tradução para dar suporte a tamanhos de disco de alta capacidade. Consulte o fabricante para obter especificações precisas da unidade.

</dd> <dt>

**DiskNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (1)
</dt> </dl>

Número de índice do disco que contém esta partição.

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **char16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (10), **Max** (256)
</dt> </dl>

Nome do fabricante da unidade de disco.

</dd> <dt>

**PartitionCount**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (11)
</dt> </dl>

Número de partições nesta unidade de disco físico que são reconhecidas pelo sistema operacional.

</dd> <dt>

**SCSILun**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (9)
</dt> </dl>

LUN (número de unidade lógica) SCSI do adaptador SCSI.

</dd> <dt>

**SCSIPath**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (7)
</dt> </dl>

Número do barramento SCSI do adaptador SCSI.

</dd> <dt>

**SCSIPort**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (6)
</dt> </dl>

Número de SCSI do adaptador SCSI.

</dd> <dt>

**SCSITarget**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (8)
</dt> </dl>

Contém o número do dispositivo de destino.

</dd> <dt>

**SectorsPerTrack**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (3)
</dt> </dl>

Número de setores em cada faixa para esta unidade de disco físico.

</dd> <dt>

**TrackPerCylinder**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (4)
</dt> </dl>

Número de faixas em cada cilindro na unidade de disco físico. Observação: o valor dessa propriedade é obtido por meio de funções estendidas de interrupção do BIOS 13h. O valor poderá ser impreciso se a unidade usar um esquema de tradução para dar suporte a tamanhos de disco de alta capacidade. Consulte o fabricante para obter especificações precisas da unidade.

</dd> <dt>

**WriteCacheEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (12)
</dt> </dl>

True se o cache de gravação estiver habilitado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 




