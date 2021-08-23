---
description: A enumeração WPD STREAM UNITS especifica os tipos de unidade a serem usados para \_ \_ operações IPortableDeviceUnitsStream.
ms.assetid: BE668696-7AF3-44AA-891A-9BFF67FB5544
title: WPD_STREAM_UNITS enumeração (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_STREAM_UNITS
api_type:
- HeaderDef
api_location:
- PortableDeviceTypes.h
ms.openlocfilehash: d2419453beac6b493ddd1bbbe1281b1596ce00456599074b3872fecb003550c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119440756"
---
# <a name="wpd_stream_units-enumeration"></a>Enumeração WPD \_ STREAM \_ UNITS

A **enumeração WPD \_ STREAM \_ UNITS** especifica os tipos de unidade a serem usados para [**operações IPortableDeviceUnitsStream.**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream)

## <a name="syntax"></a>Sintaxe


```C++
typedef enum _WPD_STREAM_UNITS { 
  WPD_STREAM_UNITS_BYTES         = 0,
  WPD_STREAM_UNITS_FRAMES        = 1,
  WPD_STREAM_UNITS_ROWS          = 2,
  WPD_STREAM_UNITS_MILLISECONDS  = 3,
  WPD_STREAM_UNITS_MICROSECONDS  = 4
} WPD_STREAM_UNITS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_STREAM_UNITS_BYTES"></span><span id="wpd_stream_units_bytes"></span>**BYTES DE \_ UNIDADES DE \_ FLUXO WPD \_**
</dt> <dd>

As unidades de fluxo são especificadas em bytes.

</dd> <dt>

<span id="WPD_STREAM_UNITS_FRAMES"></span><span id="wpd_stream_units_frames"></span>**QUADROS DE \_ UNIDADES \_ DE FLUXO \_ WPD**
</dt> <dd>

As unidades de fluxo são especificadas em quadros.

</dd> <dt>

<span id="WPD_STREAM_UNITS_ROWS"></span><span id="wpd_stream_units_rows"></span>**LINHAS DE \_ UNIDADES \_ DE FLUXO \_ WPD**
</dt> <dd>

As unidades de fluxo são especificadas em linhas.

</dd> <dt>

<span id="WPD_STREAM_UNITS_MILLISECONDS"></span><span id="wpd_stream_units_milliseconds"></span>**MILISSEGUNDOS DE UNIDADES DE \_ \_ FLUXO \_ WPD**
</dt> <dd>

As unidades de fluxo são especificadas em milissegundos.

</dd> <dt>

<span id="WPD_STREAM_UNITS_MICROSECONDS"></span><span id="wpd_stream_units_microseconds"></span>**MICROSSEGUNDOS DE \_ \_ UNIDADES DE FLUXO \_ WPD**
</dt> <dd>

As unidades de fluxo são especificadas em microssegundos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                        |
| parâmetro<br/>                   | <dl> <dt>PortableDeviceTypes.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPortableDeviceUnitsStream**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream)
</dt> <dt>

[**IPortableDeviceUnitsStream::SeekInUnits**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceunitsstream-seekinunits)
</dt> </dl>

 

 




