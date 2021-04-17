---
description: O \_ tipo de enumeração de modos de captura WPD \_ descreve o modo de captura de tempo de uma captura de imagem ainda.
ms.assetid: bfe96176-d018-4b39-a938-035757111784
title: Enumeração de WPD_CAPTURE_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CAPTURE_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e56e3e66cd20abaeb1daf0a674633a36b57a9575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105798483"
---
# <a name="wpd_capture_modes-enumeration"></a>Enumeração de modos de \_ captura WPD \_

O tipo de enumeração de **\_ \_ modos de captura WPD** descreve o modo de captura de tempo de uma captura de imagem ainda.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_CAPTURE_MODES { 
  WPD_CAPTURE_MODE_UNDEFINED  = 0,
  WPD_CAPTURE_MODE_NORMAL     = 1,
  WPD_CAPTURE_MODE_BURST      = 2,
  WPD_CAPTURE_MODE_TIMELAPSE  = 3
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_CAPTURE_MODE_UNDEFINED"></span><span id="wpd_capture_mode_undefined"></span>**\_modo de captura WPD \_ \_ indefinido**
</dt> <dd>

O modo de captura não foi definido.

</dd> <dt>

<span id="WPD_CAPTURE_MODE_NORMAL"></span><span id="wpd_capture_mode_normal"></span>**modo de captura do WPD \_ \_ \_ normal**
</dt> <dd>

Nenhum modo de atraso ou intermitência deve ser usado.

</dd> <dt>

<span id="WPD_CAPTURE_MODE_BURST"></span><span id="wpd_capture_mode_burst"></span>**\_intermitência do \_ modo de captura WPD \_**
</dt> <dd>

Especifica que um número definido de imagens deve ser capturado com um intervalo definido entre eles. O número de imagens a serem capturadas e o atraso de tempo entre elas são especificados pelo [ \_ número de \_ \_ intermitência \_ de imagem](still-image-properties.md) e pelas propriedades de [ \_ \_ \_ \_ intervalo de intermitência de imagem ainda](still-image-properties.md) mais específicas.

</dd> <dt>

<span id="WPD_CAPTURE_MODE_TIMELAPSE"></span><span id="wpd_capture_mode_timelapse"></span>**\_modo de captura WPD \_ \_ TIMELAPSE**
</dt> <dd>

A captura de imagem deve usar a fotografia de tempo. O número de imagens e o intervalo entre elas são descritos pelas propriedades de [ \_ \_ \_ \_ intervalo](still-image-properties.md) de [ \_ \_ \_ TIMELAPSE \_ de imagem WPD](still-image-properties.md) e WPD ainda.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração é usada pela propriedade [do \_ \_ modo de \_ captura \_ de imagem WPD](still-image-properties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades e atributos WPD**](properties-and-attributes.md)
</dt> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




