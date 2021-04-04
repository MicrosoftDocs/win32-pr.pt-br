---
description: A \_ enumeração de unidades de fluxo WPD \_ especifica os tipos de unidade a serem usados para operações IPortableDeviceUnitsStream.
ms.assetid: BE668696-7AF3-44AA-891A-9BFF67FB5544
title: Enumeração de WPD_STREAM_UNITS (PortableDeviceTypes. h)
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
ms.openlocfilehash: 8e70455402a49673b574a0c696b6dda30cc6a884
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662934"
---
# <a name="wpd_stream_units-enumeration"></a>Enumeração de unidades de \_ fluxo WPD \_

A enumeração de **\_ \_ unidades de fluxo WPD** especifica os tipos de unidade a serem usados para operações [**IPortableDeviceUnitsStream**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream) .

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

<span id="WPD_STREAM_UNITS_BYTES"></span><span id="wpd_stream_units_bytes"></span>**\_bytes de \_ unidades de fluxo WPD \_**
</dt> <dd>

As unidades de fluxo são especificadas em bytes.

</dd> <dt>

<span id="WPD_STREAM_UNITS_FRAMES"></span><span id="wpd_stream_units_frames"></span>**\_quadros de \_ unidades de fluxo WPD \_**
</dt> <dd>

As unidades de fluxo são especificadas em quadros.

</dd> <dt>

<span id="WPD_STREAM_UNITS_ROWS"></span><span id="wpd_stream_units_rows"></span>**\_linhas de \_ unidades de fluxo WPD \_**
</dt> <dd>

As unidades de fluxo são especificadas em linhas.

</dd> <dt>

<span id="WPD_STREAM_UNITS_MILLISECONDS"></span><span id="wpd_stream_units_milliseconds"></span>**\_ \_ milissegundos de unidades de fluxo WPD \_**
</dt> <dd>

As unidades de fluxo são especificadas em milissegundos.

</dd> <dt>

<span id="WPD_STREAM_UNITS_MICROSECONDS"></span><span id="wpd_stream_units_microseconds"></span>**\_ \_ microssegundos de unidades de fluxo WPD \_**
</dt> <dd>

As unidades de fluxo são especificadas em microssegundos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                        |
| parâmetro<br/>                   | <dl> <dt>PortableDeviceTypes. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPortableDeviceUnitsStream**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream)
</dt> <dt>

[**IPortableDeviceUnitsStream::SeekInUnits**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceunitsstream-seekinunits)
</dt> </dl>

 

 




