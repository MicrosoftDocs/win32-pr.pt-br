---
description: Classe SystemConfig_V0_Video-essa classe é a classe de tipo de evento para eventos de configuração de vídeo.
ms.assetid: 06aab3a3-a55e-4eb8-897a-2ad8349e5900
title: Classe SystemConfig_V0_Video
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Video
- SystemConfig_V0_Video.MemorySize
- SystemConfig_V0_Video.XResolution
- SystemConfig_V0_Video.YResolution
- SystemConfig_V0_Video.BitsPerPixel
- SystemConfig_V0_Video.VRefresh
- SystemConfig_V0_Video.ChipType
- SystemConfig_V0_Video.DACType
- SystemConfig_V0_Video.AdapterString
- SystemConfig_V0_Video.BiosString
- SystemConfig_V0_Video.DeviceId
- SystemConfig_V0_Video.StateFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7121d56d2acf0890a75bccdaf397f184c8780f1f1d3152d3ce2ea4db7781ecaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151365"
---
# <a name="systemconfig_v0_video-class"></a>\_Classe de \_ vídeo SystemConfig V0

Essa classe é a classe de tipo de evento para eventos de configuração de vídeo.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType(14), EventTypeName("Video")]
class SystemConfig_V0_Video : SystemConfig_V0
{
  uint32 MemorySize;
  uint32 XResolution;
  uint32 YResolution;
  uint32 BitsPerPixel;
  uint32 VRefresh;
  char16 ChipType[];
  char16 DACType[];
  char16 AdapterString[];
  char16 BiosString[];
  char16 DeviceId[];
  uint32 StateFlags;
};
```

## <a name="members"></a>Membros

A classe de **\_ \_ vídeo SystemConfig V0** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ \_ vídeo SystemConfig V0** tem essas propriedades.

<dl> <dt>

**Adaptadorstring**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **char16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (8), **Max** (256)
</dt> </dl>

Nome ou descrição do adaptador.

</dd> <dt>

**Biosstring**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **char16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (9), **máx** . (256)
</dt> </dl>

Nome do BIOS do adaptador.

</dd> <dt>

**BitsPerPixel**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (4)
</dt> </dl>

Número de bits usados para exibir cada pixel.

</dd> <dt>

**Chiptype**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **char16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (6), **Max** (256)
</dt> </dl>

Nome do chip do adaptador.

</dd> <dt>

**DACType**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **char16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (7), **Max** (256)
</dt> </dl>

Nome do chip do conversor digital para analógico (DAC) do adaptador.

</dd> <dt>

**DeviceId**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **char16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (10), **Max** (256)
</dt> </dl>

Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.

</dd> <dt>

**MemorySize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (1)
</dt> </dl>

Quantidade máxima de memória com suporte, em bytes.

</dd> <dt>

**StateFlags**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (11)
</dt> </dl>

Sinalizadores de estado do dispositivo. Pode ser qualquer combinação razoável do seguinte.



| Valor                                                                                                                                                                                                                                                                                        | Significado                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISPLAY_DEVICE_ATTACHED_TO_DESKTOP"></span><span id="display_device_attached_to_desktop"></span><dl> <dt>**Exibir \_ DISPOSITIVO \_ conectado \_ à \_ área de trabalho**</dt> <dt>1 (0x1)</dt> </dl> | O dispositivo faz parte da área de trabalho.<br/>                                                                                                                                                                                |
| <span id="DISPLAY_DEVICE_MIRRORING_DRIVER"></span><span id="display_device_mirroring_driver"></span><dl> <dt>**Exibir \_ \_ \_ Driver de espelhamento de dispositivo**</dt> <dt>8 (0x8)</dt> </dl>           | Representa um pseudodispositivo usado para espelhar o desenho do aplicativo para se conectar a um computador remoto ou a outras finalidades. Um pseudo monitor invisível está associado a este dispositivo. Por exemplo, o NetMeeting o utiliza.<br/> |
| <span id="DISPLAY_DEVICE_MODESPRUNED"></span><span id="display_device_modespruned"></span><dl> <dt>**Exibir \_ DISPOSITIVO \_ MODESPRUNED**</dt> <dt>134217728 (0x8000000)</dt> </dl>             | O dispositivo tem mais modos de exibição do que seus dispositivos de saída dão suporte.<br/>                                                                                                                                                |
| <span id="DISPLAY_DEVICE_PRIMARY_DEVICE"></span><span id="display_device_primary_device"></span><dl> <dt>**Exibir \_ \_ \_ Dispositivo primário**</dt> <dt>4 do dispositivo (0x4)</dt> </dl>                 | A área de trabalho principal está no dispositivo. Para um sistema com um único cartão de vídeo, ele é sempre definido. Para um sistema com vários cartões de vídeo, somente um dispositivo pode ter esse conjunto.<br/>                                   |
| <span id="DISPLAY_DEVICE_REMOVABLE"></span><span id="display_device_removable"></span><dl> <dt>**Exibir \_ \_Removível do dispositivo**</dt> <dt>32 (0x20)</dt> </dl>                               | O dispositivo é removível; Ela não pode ser a exibição primária.<br/>                                                                                                                                                        |
| <span id="DISPLAY_DEVICE_VGA_COMPATIBLE"></span><span id="display_device_vga_compatible"></span><dl> <dt>**Exibir \_ DISPOSITIVO \_ \_ compatível com VGA**</dt> <dt>16 (0x10)</dt> </dl>               | O dispositivo é compatível com VGA.<br/>                                                                                                                                                                                     |



 

</dd> <dt>

**VRefresh**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (5)
</dt> </dl>

Taxa de atualização atual, em Hertz.

</dd> <dt>

**XResolution**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (2)
</dt> </dl>

Número atual de pixels horizontais.

</dd> <dt>

**YResolution**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **WmiDataId** (3)
</dt> </dl>

Número atual de pixels verticais.

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

 

 




