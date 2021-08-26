---
description: Essa classe é a classe de tipo de evento para eventos de canal do IDE. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 2265a4a6-4377-4aa9-926a-def6e8eda998
title: Classe SystemConfig_IDEChannel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_IDEChannel
- SystemConfig_IDEChannel.TargetId
- SystemConfig_IDEChannel.DeviceType
- SystemConfig_IDEChannel.DeviceTimingMode
- SystemConfig_IDEChannel.LocationInformationLen
- SystemConfig_IDEChannel.LocationInformation
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8cf764d266d98199e27b40c8690b36183aa82aa2cfb8ded006087ab55f3ddfca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041596"
---
# <a name="systemconfig_idechannel-class"></a>\_Classe SystemConfig IDEChannel

Essa classe é a classe de tipo de evento para eventos de canal do IDE.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType(23), EventTypeName("IDEChannel")]
class SystemConfig_IDEChannel : SystemConfig
{
  uint32 TargetId;
  uint32 DeviceType;
  uint32 DeviceTimingMode;
  uint32 LocationInformationLen;
  string LocationInformation;
};
```

## <a name="members"></a>Membros

A classe **SystemConfig \_ IDEChannel** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **SystemConfig \_ IDEChannel** tem essas propriedades.

<dl> <dt>

**DeviceTimingMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (3), formato ("x")
</dt> </dl>

O modo no qual o IDE pode funcionar. O valores possíveis são os seguintes:

-   PIO \_ MODE0 (0x1)
-   PIO \_ mode1 (0x2)
-   PIO \_ Mode2 (0x4)
-   PIO \_ MODE3 (0x8)
-   PIO \_ MODE4 (0x10)
-   SWDMA \_ MODE0 (0x20)
-   SWDMA \_ mode1 (0x40)
-   SWDMA \_ Mode2 (0x80)
-   MWDMA \_ MODE0 (0x100)
-   MWDMA \_ Mode2 (0x200)
-   MWDMA \_ MODE3 (0x400)
-   UDMA \_ MODE0 (0x800)
-   UDMA \_ mode1 (0x1000)
-   UDMA \_ Mode2 (0x2000)
-   UDMA \_ MODE3 (0x4000)
-   UDMA \_ MODE4 (0x8000)
-   UDMA \_ MODE5 (0x10000)

</dd> <dt>

**DeviceType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (2), formato ("x")
</dt> </dl>

O tipo de dispositivo. O valores possíveis são os seguintes:

-   ATA (1)
-   ATAPI (2)

</dd> <dt>

**LocationInformation**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (5), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

O canal IDE (por exemplo, canal primário, canal secundário e assim por diante).

</dd> <dt>

**LocationInformationLen**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (4)
</dt> </dl>

Comprimento da cadeia de caracteres **LocationInformation** .

</dd> <dt>

**TargetId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (1)
</dt> </dl>

O identificador do disco.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




