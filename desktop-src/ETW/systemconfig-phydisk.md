---
description: SystemConfig_PhyDisk classe - essa classe é a classe de tipo de evento para eventos de configuração de disco físico.
ms.assetid: 850a6b2c-69e6-47ae-95ff-585fcc70c1c8
title: SystemConfig_PhyDisk classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_PhyDisk
- SystemConfig_PhyDisk.DiskNumber
- SystemConfig_PhyDisk.BytesPerSector
- SystemConfig_PhyDisk.SectorsPerTrack
- SystemConfig_PhyDisk.TracksPerCylinder
- SystemConfig_PhyDisk.Cylinders
- SystemConfig_PhyDisk.SCSIPort
- SystemConfig_PhyDisk.SCSIPath
- SystemConfig_PhyDisk.SCSITarget
- SystemConfig_PhyDisk.SCSILun
- SystemConfig_PhyDisk.Manufacturer
- SystemConfig_PhyDisk.PartitionCount
- SystemConfig_PhyDisk.WriteCacheEnabled
- SystemConfig_PhyDisk.Pad
- SystemConfig_PhyDisk.BootDriveLetter
- SystemConfig_PhyDisk.Spare
api_type:
- NA
api_location: ''
ms.openlocfilehash: d39c56dd5c099974c9dac281d1ed4c961b946b56
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886382"
---
# <a name="systemconfig_phydisk-class"></a>Classe SystemConfig \_ PhyDisk

Essa classe é a classe de tipo de evento para eventos de configuração de disco físico.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class SystemConfig_PhyDisk : SystemConfig
{
  uint32 DiskNumber;
  uint32 BytesPerSector;
  uint32 SectorsPerTrack;
  uint32 TracksPerCylinder;
  uint64 Cylinders;
  uint32 SCSIPort;
  uint32 SCSIPath;
  uint32 SCSITarget;
  uint32 SCSILun;
  char16 Manufacturer[];
  uint32 PartitionCount;
  uint8  WriteCacheEnabled;
  uint8  Pad;
  char16 BootDriveLetter[];
  char16 Spare[];
};
```

## <a name="members"></a>Membros

A **classe SystemConfig \_ PhyDisk** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe SystemConfig \_ PhyDisk** tem essas propriedades.

<dl> <dt>

**BootDriveLetter**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz char16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (14), **Max** (3), **Format("s")**
</dt> </dl>

Letra da unidade de inicialização no formato " &lt; letra &gt; :".

</dd> <dt>

**BytesPerSector**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (2)
</dt> </dl>

Número de bytes em cada setor para a unidade de disco físico.

</dd> <dt>

**Cilindros**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (5)
</dt> </dl>

Número total de cilindros na unidade de disco físico. Observação: o valor dessa propriedade é obtido por meio de funções estendidas de interrupção do BIOS 13h. O valor poderá ser impreciso se a unidade usar um esquema de tradução para dar suporte a tamanhos de disco de alta capacidade. Consulte o fabricante para ver as especificações precisas da unidade.

</dd> <dt>

**DiskNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (1)
</dt> </dl>

Número de índice do disco que contém essa partição.

</dd> <dt>

**Fabricante**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz char16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (10), **Max** (256), **Format("s")**
</dt> </dl>

Nome do fabricante da unidade de disco.

</dd> <dt>

**Pad**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (13)
</dt> </dl>

Não usado.

</dd> <dt>

**PartitionCount**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (11)
</dt> </dl>

Número de partições nessa unidade de disco físico que são reconhecidas pelo sistema operacional.

</dd> <dt>

**SCSILun**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (9)
</dt> </dl>

LUN (número de unidade lógica) SCSI do adaptador SCSI.

</dd> <dt>

**SCSIPath**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (7)
</dt> </dl>

Número do barramento SCSI do adaptador SCSI.

</dd> <dt>

**SCSIPort**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (6)
</dt> </dl>

Número SCSI do adaptador SCSI.

</dd> <dt>

**SCSITarget**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (8)
</dt> </dl>

Contém o número do dispositivo de destino.

</dd> <dt>

**SectorsPerTrack**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (3)
</dt> </dl>

Número de setores em cada faixa para essa unidade de disco físico.

</dd> <dt>

**Poupar**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz char16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (15), **Max** (2), **Format("s")**
</dt> </dl>

Não usado.

</dd> <dt>

**TrackPerCylinder**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (4)
</dt> </dl>

Número de faixas em cada cilindro na unidade de disco físico. Observação: o valor dessa propriedade é obtido por meio de funções estendidas de interrupção do BIOS 13h. O valor poderá ser impreciso se a unidade usar um esquema de tradução para dar suporte a tamanhos de disco de alta capacidade. Consulte o fabricante para ver as especificações precisas da unidade.

</dd> <dt>

**WriteCacheEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
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
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




