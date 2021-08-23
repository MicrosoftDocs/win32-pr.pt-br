---
description: A interface do dispositivo pode ser descrita por um valor de GUID. Windows Os dispositivos portáteis definem a seguinte interface de dispositivo.
ms.assetid: 47b8d3dd-ea12-461d-935d-2de2c0157f88
title: GUIDs da interface do dispositivo (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_DEVINTERFACE_WPD
- GUID_DEVINTERFACE_WPD_PRIVATE
- GUID_DEVINTERFACE_WPD_SERVICE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 6f4bd170aeae46f738f5ce4a5a98bc694583a19fe3e7fa6eccc21c86fdc871d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657916"
---
# <a name="device-interface-guids"></a>GUIDs da interface do dispositivo

A interface do dispositivo pode ser descrita por um valor de **GUID** . Windows Os dispositivos portáteis definem a seguinte interface de dispositivo.



| Constante                                                                                                                                                                                                        | Descrição                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_DEVINTERFACE_WPD"></span><span id="guid_devinterface_wpd"></span><dl> <dt>**GUID \_ DEVINTERFACE \_ WPD**</dt> </dl>                          | Identifica os dispositivos que aparecem em uma enumeração WPD normal. Qualquer dispositivo que registra esse GUID de interface será enumerado quando um aplicativo chamar o método [**IPortableDeviceManager:: Devices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) .<br/>                                 |
| <span id="GUID_DEVINTERFACE_WPD_PRIVATE"></span><span id="guid_devinterface_wpd_private"></span><dl> <dt>**GUID \_ DEVINTERFACE \_ WPD \_ particular**</dt> </dl> | Identifica os dispositivos que não serão exibidos durante uma enumeração WPD normal. Qualquer dispositivo que registra esse GUID de interface será enumerado somente quando um aplicativo chamar o método [**IPortableDeviceManager:: GetPrivateDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getprivatedevices) .<br/> |
| <span id="GUID_DEVINTERFACE_WPD_SERVICE"></span><span id="guid_devinterface_wpd_service"></span><dl> <dt>**\_serviço GUID DEVINTERFACE \_ WPD \_**</dt> </dl> | no Windows 7, os aplicativos podem enumerar todos os serviços de dispositivos WPD chamando [**IPortableDeviceServiceManager:: getdeviceservices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) e usando essa classe de interface como o GUID do tipo de serviço.<br/>                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência de programação](programming-reference.md)
</dt> </dl>

 

 




