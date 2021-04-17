---
description: O \_ tipo de \_ enumeração valores de status corrigidos de cor WPD \_ \_ descreve o status de correção de cor de um arquivo de imagem ou de vídeo.
ms.assetid: af129a1b-7760-4339-adf7-3f3c17cebde2
title: Enumeração de WPD_COLOR_CORRECTED_STATUS_VALUES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COLOR_CORRECTED_STATUS_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: ec6bfcaa3933bb70c3064f829e701509e3ff32f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791598"
---
# <a name="wpd_color_corrected_status_values-enumeration"></a>\_Enumeração de \_ valores de status corrigidos de cor WPD \_ \_

O tipo de enumeração **\_ \_ \_ \_ valores de status corrigidos de cor WPD** descreve o status de correção de cor de um arquivo de imagem ou de vídeo.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_COLOR_CORRECTED_STATUS_VALUES { 
  WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED            = 0,
  WPD_COLOR_CORRECTED_STATUS_CORRECTED                = 1,
  WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED  = 2
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED"></span><span id="wpd_color_corrected_status_not_corrected"></span>**\_status corrigido de cor WPD \_ \_ \_ não \_ corrigido**
</dt> <dd>

A imagem não foi corrigida por cor.

</dd> <dt>

<span id="WPD_COLOR_CORRECTED_STATUS_CORRECTED"></span><span id="wpd_color_corrected_status_corrected"></span>**\_status corrigido de cor WPD \_ \_ \_ corrigido**
</dt> <dd>

A imagem foi corrigida por cor.

</dd> <dt>

<span id="WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED"></span><span id="wpd_color_corrected_status_should_not_be_corrected"></span>**o \_ status corrigido da cor WPD \_ \_ \_ \_ não deve \_ ser \_ corrigido**
</dt> <dd>

A imagem não foi, e não deve ser, a cor corrigida.

</dd> </dl>

## <a name="remarks"></a>Comentários

Indica o status corrigido da cor de uma imagem. Essa enumeração é usada pela propriedade [ \_ \_ \_ \_ status corrigido de cor de imagem WPD](image-properties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




