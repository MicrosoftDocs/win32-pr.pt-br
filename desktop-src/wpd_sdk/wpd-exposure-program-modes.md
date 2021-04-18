---
description: O \_ tipo de enumeração dos modos de programas de exposição WPD \_ \_ descreve um modo de exposição a ser usado ao capturar imagens com um dispositivo.
ms.assetid: 68b76294-6ad3-4f4a-bf02-bc31c9e8ac62
title: Enumeração de WPD_EXPOSURE_PROGRAM_MODES (PortableDevice. h)
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
ms.openlocfilehash: a88ce90bb9e776cd45245b32a363635c2ccf0560
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758487"
---
# <a name="wpd_exposure_program_modes-enumeration"></a>\_Enumeração de \_ modos de programas de exposição WPD \_

O tipo de enumeração dos **\_ modos de \_ programas \_ de exposição WPD** descreve um modo de exposição a ser usado ao capturar imagens com um dispositivo.

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

<span id="WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED"></span><span id="wpd_exposure_program_mode_undefined"></span>**\_modo de programa de exposição WPD \_ \_ \_ indefinido**
</dt> <dd>

O modo de exposição não foi especificado.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_MANUAL"></span><span id="wpd_exposure_program_mode_manual"></span>**\_manual do \_ modo de programa de exposição WPD \_ \_**
</dt> <dd>

O aplicativo deve especificar todas as configurações de exposição.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_AUTO"></span><span id="wpd_exposure_program_mode_auto"></span>**\_modo de \_ programa de exposição \_ WPD \_**
</dt> <dd>

Use um modo de exposição automática definido pelo dispositivo.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY"></span><span id="wpd_exposure_program_mode_aperture_priority"></span>**\_prioridade de \_ abertura do modo de programa de exposição WPD \_ \_ \_**
</dt> <dd>

Um modo de exposição automatizada que indica que o valor de abertura da lente deve permanecer fixo, mas a velocidade do obturador deve ser determinada pelo dispositivo.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY"></span><span id="wpd_exposure_program_mode_shutter_priority"></span>**\_prioridade de \_ \_ \_ obturador do modo de programa de exposição WPD \_**
</dt> <dd>

Um modo de exposição automatizada que indica que a velocidade do obturador deve permanecer fixa, mas que a abertura da lente deve ser determinada pelo dispositivo.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_CREATIVE"></span><span id="wpd_exposure_program_mode_creative"></span>**\_modo de programa de exposição WPD \_ \_ \_ Creative**
</dt> <dd>

Um modo de exposição automatizada que tenta maximizar a profundidade do campo.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_ACTION"></span><span id="wpd_exposure_program_mode_action"></span>**\_ação do \_ modo de programa de exposição WPD \_ \_**
</dt> <dd>

Um modo de exposição automatizada que tenta maximizar a velocidade do obturador.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT"></span><span id="wpd_exposure_program_mode_portrait"></span>**\_modo de programa de exposição WPD \_ \_ \_ retrato**
</dt> <dd>

Um modo de exposição automatizada que especifica uma profundidade relativamente superficial do campo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Indica o modo do programa de exposição do dispositivo. Essa enumeração é usada pela propriedade [de \_ \_ modo do \_ \_ programa de \_ exposição de imagem WPD](still-image-properties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




