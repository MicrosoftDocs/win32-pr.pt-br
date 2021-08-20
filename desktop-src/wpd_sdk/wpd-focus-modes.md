---
description: O tipo de enumeração WPD \_ FOCUS \_ MODES descreve o modo de foco usado por um dispositivo de captura de imagem ainda.
ms.assetid: 3b092391-e4c1-4586-8df4-b58a1dcccc81
title: WPD_FOCUS_MODES enumeração (PortableDevice.h)
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
ms.openlocfilehash: 87dca9643174b9497e0643d1c0fdcfcd8c57c18e638f7cf8441ea08b8e958a7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118026343"
---
# <a name="wpd_focus_modes-enumeration"></a>Enumeração WPD \_ FOCUS \_ MODES

O **tipo de enumeração WPD \_ FOCUS \_ MODES** descreve o modo de foco usado por um dispositivo de captura de imagem ainda.

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

<span id="WPD_FOCUS_UNDEFINED"></span><span id="wpd_focus_undefined"></span>**FOCO WPD \_ \_ INDEFINIDO**
</dt> <dd>

O modo de foco não foi especificado.

</dd> <dt>

<span id="WPD_FOCUS_MANUAL"></span><span id="wpd_focus_manual"></span>**MANUAL DE \_ FOCO WPD \_**
</dt> <dd>

Especifica o foco manual.

</dd> <dt>

<span id="WPD_FOCUS_AUTOMATIC"></span><span id="wpd_focus_automatic"></span>**WPD \_ FOCUS \_ AUTOMATIC**
</dt> <dd>

Especifica o foco automático, controlado pelo dispositivo.

</dd> <dt>

<span id="WPD_FOCUS_AUTOMATIC_MACRO"></span><span id="wpd_focus_automatic_macro"></span>**MACRO AUTOMÁTICA DE FOCO WPD \_ \_ \_**
</dt> <dd>

Especifica que o dispositivo deve alternar automaticamente entre a macro e o foco normal, conforme necessário.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração é usada pela [propriedade WPD \_ STILL IMAGE \_ FOCUS \_ \_ MODE.](still-image-properties.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




