---
description: O \_ tipo de enumeração de fontes de energia WPD \_ descreve a fonte de energia que um dispositivo está usando.
ms.assetid: feebf213-052d-4315-84db-2109cab5f179
title: Enumeração de WPD_POWER_SOURCES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_POWER_SOURCES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: bf9a153d4d41a64b639f796ea2ba0eeb9e567a32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749913"
---
# <a name="wpd_power_sources-enumeration"></a>Enumeração de fontes de \_ energia WPD \_

O tipo de enumeração de **\_ \_ fontes de energia WPD** descreve a fonte de energia que um dispositivo está usando.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_POWER_SOURCES { 
  WPD_POWER_SOURCE_BATTERY   = 0,
  WPD_POWER_SOURCE_EXTERNAL  = 1
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_POWER_SOURCE_BATTERY"></span><span id="wpd_power_source_battery"></span>**\_bateria de \_ fonte de energia WPD \_**
</dt> <dd>

A fonte de energia do dispositivo é uma bateria.

</dd> <dt>

<span id="WPD_POWER_SOURCE_EXTERNAL"></span><span id="wpd_power_source_external"></span>**\_fonte de energia WPD \_ \_ externa**
</dt> <dd>

O dispositivo usa uma fonte de energia externa.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração é usada pela propriedade [ \_ fonte de \_ energia \_ do dispositivo WPD](device-properties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




