---
description: O \_ tipo de enumeração de transportes de dispositivos WPD \_ especifica a relação de herança para um serviço. Essa enumeração é usada pela propriedade de \_ transporte do dispositivo WPD \_ .
ms.assetid: a9d48034-3588-4e48-a03a-91cbe679cbc9
title: Enumeração de WPD_DEVICE_TRANSPORTS (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_DEVICE_TRANSPORTS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 5f091a84c573038c7d74cf5c2760c298a2542f70f06bdb45d1e72954c9dd5f25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703816"
---
# <a name="wpd_device_transports-enumeration"></a>Enumeração de transportes de \_ dispositivos WPD \_

O tipo de enumeração de [**\_ \_ transportes de dispositivos WPD**](/windows/desktop/wpd_sdk/wpd-device-transports) especifica a relação de herança para um serviço. Essa enumeração é usada pela propriedade **de \_ \_ transporte do dispositivo WPD** .

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWPD_DEVICE_TRANSPORTS { 
  WPD_DEVICE_TRANSPORT_UNSPECIFIED  = 0,
  WPD_DEVICE_TRANSPORT_USB          = 1,
  WPD_DEVICE_TRANSPORT_IP           = 2,
  WPD_DEVICE_TRANSPORT_BLUETOOTH    = 3
} WPD_DEVICE_TRANSPORTS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_DEVICE_TRANSPORT_UNSPECIFIED"></span><span id="wpd_device_transport_unspecified"></span>**\_transporte de dispositivo WPD \_ \_ não especificado**
</dt> <dd>

O tipo de transporte não foi especificado.

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_USB"></span><span id="wpd_device_transport_usb"></span>**\_USB de \_ transporte de dispositivo WPD \_**
</dt> <dd>

O dispositivo está conectado por meio de USB.

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_IP"></span><span id="wpd_device_transport_ip"></span>**\_IP de \_ transporte do dispositivo WPD \_**
</dt> <dd>

O dispositivo está conectado por meio do protocolo Internet (IP).

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_BLUETOOTH"></span><span id="wpd_device_transport_bluetooth"></span>**\_Bluetooth de \_ transporte de dispositivo WPD \_**
</dt> <dd>

O dispositivo está conectado por meio de Bluetooth.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



 

