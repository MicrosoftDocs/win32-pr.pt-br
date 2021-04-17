---
description: O \_ tipo de enumeração de modos flash WPD \_ descreve um modo flash para usar ao capturar imagens com um dispositivo.
ms.assetid: 4e92c86d-2f35-4bc6-8d37-ec1ab5c518b2
title: Enumeração de WPD_FLASH_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FLASH_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 09a2a5b95e86d9d17267cafcfbf723e734ffc74f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754464"
---
# <a name="wpd_flash_modes-enumeration"></a>\_Enumeração de \_ modos flash WPD

O tipo de enumeração de **\_ \_ modos flash WPD** descreve um modo flash para usar ao capturar imagens com um dispositivo.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_FLASH_MODES { 
  WPD_FLASH_MODE_UNDEFINED      = 0,
  WPD_FLASH_MODE_AUTO           = 1,
  WPD_FLASH_MODE_OFF            = 2,
  WPD_FLASH_MODE_FILL           = 3,
  WPD_FLASH_MODE_RED_EYE_AUTO   = 4,
  WPD_FLASH_MODE_RED_EYE_FILL   = 5,
  WPD_FLASH_MODE_EXTERNAL_SYNC  = 6
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_FLASH_MODE_UNDEFINED"></span><span id="wpd_flash_mode_undefined"></span>**\_modo flash \_ WPD \_ indefinido**
</dt> <dd>

Nenhum modo flash foi especificado.

</dd> <dt>

<span id="WPD_FLASH_MODE_AUTO"></span><span id="wpd_flash_mode_auto"></span>**\_modo flash \_ WPD \_ automático**
</dt> <dd>

Especifica que o flash deve ser usado no modo automático, conforme especificado pelo dispositivo.

</dd> <dt>

<span id="WPD_FLASH_MODE_OFF"></span><span id="wpd_flash_mode_off"></span>**\_modo flash \_ WPD \_ desativado**
</dt> <dd>

Especifica que nenhum flash deve ser usado.

</dd> <dt>

<span id="WPD_FLASH_MODE_FILL"></span><span id="wpd_flash_mode_fill"></span>**\_preenchimento do \_ modo \_ flash WPD**
</dt> <dd>

Especifica um flash de tipo de preenchimento.

</dd> <dt>

<span id="WPD_FLASH_MODE_RED_EYE_AUTO"></span><span id="wpd_flash_mode_red_eye_auto"></span>**\_modo flash WPD, \_ \_ \_ olhos vermelhos \_ automáticos**
</dt> <dd>

Especifica que o flash de redução de olho vermelho deve ser usado.

</dd> <dt>

<span id="WPD_FLASH_MODE_RED_EYE_FILL"></span><span id="wpd_flash_mode_red_eye_fill"></span>**\_preenchimento de \_ \_ olho vermelho \_ do modo flash WPD \_**
</dt> <dd>

Especifica que o flash de preenchimento de olho vermelho deve ser usado.

</dd> <dt>

<span id="WPD_FLASH_MODE_EXTERNAL_SYNC"></span><span id="wpd_flash_mode_external_sync"></span>**\_ \_ sincronização externa do modo do flash WPD \_ \_**
</dt> <dd>

Especifica que o flash deve ser sincronizado com outros dispositivos flash externos.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração é usada pela propriedade [de \_ \_ \_ \_ modo flash de imagem WPD ainda](still-image-properties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




