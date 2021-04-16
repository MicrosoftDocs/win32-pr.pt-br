---
description: O \_ tipo de enumeração de modos de medição de exposição WPD \_ \_ descreve o modo de medição a ser usado ao estimar a exposição da captura de imagem ainda por um dispositivo.
ms.assetid: 5e92013c-600d-4128-ab59-1cfa8953db67
title: Enumeração de WPD_EXPOSURE_METERING_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EXPOSURE_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 76c2594339c6fa4997e4d646fc89e8c30dcdf8fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757640"
---
# <a name="wpd_exposure_metering_modes-enumeration"></a>\_Enumeração de \_ modos de medição de exposição WPD \_

O tipo de enumeração de **\_ modos de \_ medição \_ de exposição WPD** descreve o modo de medição a ser usado ao estimar a exposição da captura de imagem ainda por um dispositivo.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_EXPOSURE_METERING_MODES { 
  WPD_EXPOSURE_METERING_MODE_UNDEFINED                = 0,
  WPD_EXPOSURE_METERING_MODE_AVERAGE                  = 1,
  WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE  = 2,
  WPD_EXPOSURE_METERING_MODE_MULTI_SPOT               = 3,
  WPD_EXPOSURE_METERING_MODE_CENTER_SPOT              = 4
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_UNDEFINED"></span><span id="wpd_exposure_metering_mode_undefined"></span>**\_modo de medição de exposição WPD \_ \_ \_ indefinido**
</dt> <dd>

O modo de medição é indefinido.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_AVERAGE"></span><span id="wpd_exposure_metering_mode_average"></span>**\_média do \_ modo de medição de exposição WPD \_ \_**
</dt> <dd>

Use a exposição em média na imagem completa.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE"></span><span id="wpd_exposure_metering_mode_center_weighted_average"></span>**\_ \_ \_ \_ \_ média ponderada do modo de medição de exposição do \_ WPD**
</dt> <dd>

Use uma exposição média, com o centro da imagem, dado mais peso.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_MULTI_SPOT"></span><span id="wpd_exposure_metering_mode_multi_spot"></span>**\_ \_ \_ \_ vários pontos do modo de medição de exposição WPD \_**
</dt> <dd>

Use uma técnica de média de vários pontos.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_CENTER_SPOT"></span><span id="wpd_exposure_metering_mode_center_spot"></span>**\_ \_ \_ ponto central do modo de medição de \_ exposição WPD \_**
</dt> <dd>

Use uma técnica de média de pontos centrais.

</dd> </dl>

## <a name="remarks"></a>Comentários

Indica o modo de medição do dispositivo. Essa enumeração é usada pela propriedade [de \_ \_ modo de \_ \_ medição \_ de exposição de imagem WPD](still-image-properties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




