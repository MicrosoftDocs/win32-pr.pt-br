---
description: O \_ tipo de enumeração de modos de foco WPD \_ descreve o modo de foco usado por um dispositivo de captura de imagem ainda.
ms.assetid: 3b092391-e4c1-4586-8df4-b58a1dcccc81
title: Enumeração de WPD_FOCUS_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e7e1dc50f115fbd2ace84a3b631d37a42e1c4ba7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750400"
---
# <a name="wpd_focus_modes-enumeration"></a>Enumeração de modos de \_ foco WPD \_

O tipo de enumeração de **\_ \_ modos de foco WPD** descreve o modo de foco usado por um dispositivo de captura de imagem ainda.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_FOCUS_MODES { 
  WPD_FOCUS_UNDEFINED        = 0,
  WPD_FOCUS_MANUAL           = 1,
  WPD_FOCUS_AUTOMATIC        = 2,
  WPD_FOCUS_AUTOMATIC_MACRO  = 3
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_FOCUS_UNDEFINED"></span><span id="wpd_focus_undefined"></span>**foco de WPD \_ \_ indefinido**
</dt> <dd>

O modo de foco não foi especificado.

</dd> <dt>

<span id="WPD_FOCUS_MANUAL"></span><span id="wpd_focus_manual"></span>**\_manual de foco WPD \_**
</dt> <dd>

Especifica o foco manual.

</dd> <dt>

<span id="WPD_FOCUS_AUTOMATIC"></span><span id="wpd_focus_automatic"></span>**foco de WPD \_ \_ automático**
</dt> <dd>

Especifica o foco automático, controlado pelo dispositivo.

</dd> <dt>

<span id="WPD_FOCUS_AUTOMATIC_MACRO"></span><span id="wpd_focus_automatic_macro"></span>**\_ \_ macro automática de foco do WPD \_**
</dt> <dd>

Especifica que o dispositivo deve alternar automaticamente entre macro e foco normal, conforme necessário.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração é usada pela propriedade [ \_ modo de \_ \_ foco de \_ imagem do WPD](still-image-properties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




