---
description: O tipo de enumeração WPD EXPOSURE PROGRAM MODES descreve um modo de exposição a ser usado ao \_ capturar imagens com um \_ \_ dispositivo.
ms.assetid: 68b76294-6ad3-4f4a-bf02-bc31c9e8ac62
title: WPD_EXPOSURE_PROGRAM_MODES enumeração (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EXPOSURE_PROGRAM_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: dc64012c4f13f84abef55d2426c856b931eb447e61df4f04c69781c089857930
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083270"
---
# <a name="wpd_exposure_program_modes-enumeration"></a>Enumeração WPD \_ EXPOSURE \_ PROGRAM \_ MODES

O **tipo de enumeração WPD \_ EXPOSURE PROGRAM \_ \_ MODES** descreve um modo de exposição a ser usado ao capturar imagens com um dispositivo.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_EXPOSURE_PROGRAM_MODES { 
  WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED          = 0,
  WPD_EXPOSURE_PROGRAM_MODE_MANUAL             = 1,
  WPD_EXPOSURE_PROGRAM_MODE_AUTO               = 2,
  WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY  = 3,
  WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY   = 4,
  WPD_EXPOSURE_PROGRAM_MODE_CREATIVE           = 5,
  WPD_EXPOSURE_PROGRAM_MODE_ACTION             = 6,
  WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT           = 7
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED"></span><span id="wpd_exposure_program_mode_undefined"></span>**MODO DE \_ PROGRAMA DE \_ EXPOSIÇÃO \_ WPD \_ INDEFINIDO**
</dt> <dd>

O modo de exposição não foi especificado.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_MANUAL"></span><span id="wpd_exposure_program_mode_manual"></span>**MANUAL DO \_ MODO DE PROGRAMA DE EXPOSIÇÃO \_ \_ WPD \_**
</dt> <dd>

O aplicativo deve especificar todas as configurações de exposição.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_AUTO"></span><span id="wpd_exposure_program_mode_auto"></span>**MODO DE PROGRAMA \_ DE \_ EXPOSIÇÃO \_ WPD \_ AUTOMATICAMENTE**
</dt> <dd>

Use um modo de exposição automática definido pelo dispositivo.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY"></span><span id="wpd_exposure_program_mode_aperture_priority"></span>**PRIORIDADE DE ABERTURA DO MODO DE PROGRAMA DE EXPOSIÇÃO \_ \_ \_ \_ \_ WPD**
</dt> <dd>

Um modo de exposição automatizado que indica que o valor de abertura da lente deve permanecer fixo, mas a velocidade do obturador deve ser determinada pelo dispositivo.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY"></span><span id="wpd_exposure_program_mode_shutter_priority"></span>**PRIORIDADE DO OBTURADOR DO MODO DE PROGRAMA DE EXPOSIÇÃO \_ \_ \_ \_ WPD \_**
</dt> <dd>

Um modo de exposição automatizado que indica que a velocidade do obturador deve permanecer fixa, mas que a abertura da lente deve ser determinada pelo dispositivo.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_CREATIVE"></span><span id="wpd_exposure_program_mode_creative"></span>**MODO CRIATIVO DO PROGRAMA DE \_ \_ EXPOSIÇÃO \_ WPD \_**
</dt> <dd>

Um modo de exposição automatizado que tenta maximizar a profundidade do campo.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_ACTION"></span><span id="wpd_exposure_program_mode_action"></span>**AÇÃO DE MODO \_ DE PROGRAMA DE EXPOSIÇÃO \_ \_ WPD \_**
</dt> <dd>

Um modo de exposição automatizado que tenta maximizar a velocidade do obturador.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT"></span><span id="wpd_exposure_program_mode_portrait"></span>**RETRATO DO MODO \_ DE PROGRAMA DE EXPOSIÇÃO \_ \_ WPD \_**
</dt> <dd>

Um modo de exposição automatizado que especifica uma profundidade relativamente superficial do campo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Indica o modo de programa de exposição do dispositivo. Essa enumeração é usada pela [propriedade WPD \_ STILL IMAGE EXPOSURE PROGRAM \_ \_ \_ \_ MODE.](still-image-properties.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




