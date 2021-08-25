---
description: A classe HWConfig PhyDisk é a classe de tipo de evento \_ para eventos de configuração de disco físico. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: b134ab45-b161-452f-be84-ccbdfa3fe4af
title: HWConfig_PhyDisk classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_PhyDisk
- HWConfig_PhyDisk.DiskNumber
- HWConfig_PhyDisk.BytesPerSector
- HWConfig_PhyDisk.SectorsPerTrack
- HWConfig_PhyDisk.TracksPerCylinder
- HWConfig_PhyDisk.Cylinders
- HWConfig_PhyDisk.SCSIPort
- HWConfig_PhyDisk.SCSIPath
- HWConfig_PhyDisk.SCSITarget
- HWConfig_PhyDisk.SCSILun
- HWConfig_PhyDisk.Manufacturer
api_type:
- NA
api_location: ''
ms.openlocfilehash: ee8a578154e2acedb5d5c8ca6d5eea4f79737e5a2cfb89b0cb658526094fd09c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086396"
---
# <a name="hwconfig_phydisk-class"></a>Classe HWConfig \_ PhyDisk

A **classe HWConfig \_ PhyDisk** é a classe de tipo de evento para eventos de configuração de disco físico.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class HWConfig_PhyDisk : HWConfig
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
  string Manufacturer;
};
```

## <a name="members"></a>Membros

A **classe HWConfig \_ PhyDisk** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe HWConfig \_ PhyDisk** tem essas propriedades.

<dl> <dt>

BytesPerSector
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(2)
</dt> </dl>

Número de bytes em cada setor para a unidade de disco físico.

</dd> <dt>

Cilindros
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(5)
</dt> </dl>

Número total de cilindros na unidade de disco físico. Observação: o valor dessa propriedade é obtido por meio de funções estendidas de interrupção do BIOS 13h. O valor poderá ser impreciso se a unidade usar um esquema de tradução para dar suporte a tamanhos de disco de alta capacidade. Consulte o fabricante para ver as especificações precisas da unidade.

</dd> <dt>

DiskNumber
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(1)
</dt> </dl>

Número de índice do disco que contém essa partição.

</dd> <dt>

Fabricante
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(10), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Nome do fabricante da unidade de disco.

</dd> <dt>

SCSILun
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(9)
</dt> </dl>

LUN (número de unidade lógica) SCSI do adaptador SCSI.

</dd> <dt>

SCSIPath
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(7)
</dt> </dl>

Número do barramento SCSI do adaptador SCSI.

</dd> <dt>

SCSIPort
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(6)
</dt> </dl>

Número SCSI do adaptador SCSI.

</dd> <dt>

SCSITarget
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(8)
</dt> </dl>

Contém o número do dispositivo de destino.

</dd> <dt>

SectorsPerTrack
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(3)
</dt> </dl>

Número de setores em cada faixa para essa unidade de disco físico.

</dd> <dt>

TrackPerCylinder
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(4)
</dt> </dl>

Número de faixas em cada cilindro na unidade de disco físico. Observação: o valor dessa propriedade é obtido por meio de funções estendidas de interrupção do BIOS 13h. O valor poderá ser impreciso se a unidade usar um esquema de tradução para dar suporte a tamanhos de disco de alta capacidade. Consulte o fabricante para ver as especificações precisas da unidade.

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

 

 




