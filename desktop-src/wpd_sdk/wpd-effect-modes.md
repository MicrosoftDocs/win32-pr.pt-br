---
description: O \_ tipo de enumeração de modos de efeito WPD \_ descreve vários efeitos visuais que podem ser aplicados a uma imagem.
ms.assetid: 7624fccb-e416-4db4-978e-410c4c236328
title: Enumeração de WPD_EFFECT_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EFFECT_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 7e29f89207a74d335fbe1c2561f8dcf9cec3e923
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105807247"
---
# <a name="wpd_effect_modes-enumeration"></a>Enumeração de modos de \_ efeito WPD \_

O tipo de enumeração de **\_ \_ modos de efeito WPD** descreve vários efeitos visuais que podem ser aplicados a uma imagem.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_EFFECT_MODES { 
  WPD_EFFECT_MODE_UNDEFINED        = 0,
  WPD_EFFECT_MODE_COLOR            = 1,
  WPD_EFFECT_MODE_BLACK_AND_WHITE  = 2,
  WPD_EFFECT_MODE_SEPIA            = 3
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_EFFECT_MODE_UNDEFINED"></span><span id="wpd_effect_mode_undefined"></span>**\_modo de efeito WPD \_ \_ indefinido**
</dt> <dd>

Nenhum efeito foi especificado.

</dd> <dt>

<span id="WPD_EFFECT_MODE_COLOR"></span><span id="wpd_effect_mode_color"></span>**\_cor do \_ modo de efeito WPD \_**
</dt> <dd>

A imagem deve ser colorida.

</dd> <dt>

<span id="WPD_EFFECT_MODE_BLACK_AND_WHITE"></span><span id="wpd_effect_mode_black_and_white"></span>**\_ \_ modo de efeito \_ de WPD preto \_ e \_ branco**
</dt> <dd>

A imagem deve ser preta e branca.

</dd> <dt>

<span id="WPD_EFFECT_MODE_SEPIA"></span><span id="wpd_effect_mode_sepia"></span>**modo de efeito de WPD de \_ \_ \_ sépia**
</dt> <dd>

A imagem deve ser sépia.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração é usada pela propriedade [ \_ modo de \_ \_ efeito de \_ imagem ainda em WPD](still-image-properties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




