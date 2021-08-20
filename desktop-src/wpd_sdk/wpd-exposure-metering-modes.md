---
description: O tipo de enumeração WPD EXPOSURE METERING MODES descreve o modo de medição a ser usado ao estimar a exposição para captura de imagem ainda \_ \_ por um \_ dispositivo.
ms.assetid: 5e92013c-600d-4128-ab59-1cfa8953db67
title: WPD_EXPOSURE_METERING_MODES enumeração (PortableDevice.h)
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
ms.openlocfilehash: 2a165493142fc25ea64adc2678e8bc4ccbeace32e245422f0fcea419063a26ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842276"
---
# <a name="wpd_exposure_metering_modes-enumeration"></a>Enumeração DOS MODOS DE MEDIÇÃO DE EXPOSIÇÃO \_ \_ \_ WPD

O **tipo de enumeração WPD \_ EXPOSURE \_ METERING \_ MODES** descreve o modo de medição a ser usado ao estimar a exposição para captura de imagem ainda por um dispositivo.

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

<span id="WPD_EXPOSURE_METERING_MODE_UNDEFINED"></span><span id="wpd_exposure_metering_mode_undefined"></span>**MODO DE \_ \_ MEDIÇÃO DE EXPOSIÇÃO \_ WPD \_ INDEFINIDO**
</dt> <dd>

O modo de medição é indefinido.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_AVERAGE"></span><span id="wpd_exposure_metering_mode_average"></span>**MÉDIA DO MODO DE \_ \_ MEDIÇÃO DE \_ EXPOSIÇÃO WPD \_**
</dt> <dd>

Use a exposição média em toda a imagem.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE"></span><span id="wpd_exposure_metering_mode_center_weighted_average"></span>**MÉDIA PONDERADA DO MODO DE \_ \_ MEDIÇÃO DE \_ \_ \_ EXPOSIÇÃO WPD \_**
</dt> <dd>

Use uma exposição média, com o centro da imagem dado mais peso.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_MULTI_SPOT"></span><span id="wpd_exposure_metering_mode_multi_spot"></span>**MODO DE MEDIÇÃO DE EXPOSIÇÃO WPD \_ \_ MULTI \_ \_ \_ SPOT**
</dt> <dd>

Use uma técnica de média de vários pontos.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_CENTER_SPOT"></span><span id="wpd_exposure_metering_mode_center_spot"></span>**PONTO CENTRAL DO MODO DE MEDIÇÃO DE EXPOSIÇÃO \_ \_ \_ \_ WPD \_**
</dt> <dd>

Use uma técnica de média de ponto central.

</dd> </dl>

## <a name="remarks"></a>Comentários

Indica o modo de medição do dispositivo. Essa enumeração é usada pela [propriedade WPD \_ STILL IMAGE \_ EXPOSURE \_ \_ METERING \_ MODE.](still-image-properties.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




