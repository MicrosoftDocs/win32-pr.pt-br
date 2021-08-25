---
description: O \_ tipo de enumeração de modos de medição de foco WPD \_ \_ descreve como um dispositivo deve decidir que parte de um quadro usar para definir o foco.
ms.assetid: 0e68d0e8-2ce3-4994-99c2-2ff2293d8a20
title: Enumeração de WPD_FOCUS_METERING_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: eb37cdd32673c385617d9c0c0ae8616c8dae0ab711d1253391ae2c1e6b2f8789
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703766"
---
# <a name="wpd_focus_metering_modes-enumeration"></a>\_Enumeração de \_ modos de medição de foco WPD \_

O tipo de enumeração de **\_ modos de \_ medição \_ de foco WPD** descreve como um dispositivo deve decidir que parte de um quadro usar para definir o foco.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_FOCUS_METERING_MODES { 
  WPD_FOCUS_METERING_MODE_UNDEFINED    = 0,
  WPD_FOCUS_METERING_MODE_CENTER_SPOT  = 1,
  WPD_FOCUS_METERING_MODE_MULTI_SPOT   = 2
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_FOCUS_METERING_MODE_UNDEFINED"></span><span id="wpd_focus_metering_mode_undefined"></span>**\_modo de medição de foco WPD \_ \_ \_ indefinido**
</dt> <dd>

Indica que nenhum modo de foco foi especificado.

</dd> <dt>

<span id="WPD_FOCUS_METERING_MODE_CENTER_SPOT"></span><span id="wpd_focus_metering_mode_center_spot"></span>**\_ \_ \_ ponto central do modo de medição de \_ foco WPD \_**
</dt> <dd>

Concentra-se no centro da área emoldurada.

</dd> <dt>

<span id="WPD_FOCUS_METERING_MODE_MULTI_SPOT"></span><span id="wpd_focus_metering_mode_multi_spot"></span>**\_ \_ \_ \_ vários pontos do modo de medição de foco WPD \_**
</dt> <dd>

Determine o foco analisando várias partes da área de quadros.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração é especificada pela propriedade [de \_ \_ modo de \_ \_ medição \_ de foco de imagem WPD](still-image-properties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




