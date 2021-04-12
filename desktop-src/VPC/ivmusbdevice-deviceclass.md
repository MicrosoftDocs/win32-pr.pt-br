---
title: Propriedade IVMUSBDevice DeviceClass (VPCCOMInterfaces. h)
description: Recupera a classe de dispositivo do dispositivo USB.
ms.assetid: 46c258b9-6064-4e8c-aa5d-71b26c07351c
keywords:
- Propriedade DeviceClass Virtual PC
- Propriedade DeviceClass Virtual PC, interface IVMUSBDevice
- IVMUSBDevice interface virtual PC, Propriedade DeviceClass
topic_type:
- apiref
api_name:
- IVMUSBDevice.DeviceClass
- IVMUSBDevice.get_DeviceClass
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b758092763c95c4443caeaca3f50be08e31c112c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369807"
---
# <a name="ivmusbdevicedeviceclass-property"></a>IVMUSBDevice: Propriedade eviceClass de:D

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera a classe de dispositivo do dispositivo USB.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_DeviceClass(
  [out, retval] VMUSBDeviceClassEnum *deviceClass
);
```



## <a name="property-value"></a>Valor da propriedade

A classe de dispositivo. Para obter uma lista de valores, consulte [**VMUSBDeviceClassEnum**](vmusbdeviceclassenum.md).

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                            | Significado                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>               | O método foi concluído com êxito.<br/> |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl> | O parâmetro é **NULL**.<br/>         |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMUSBDevice é definido como 63C1258C-5721-4070-B86B-A6CE2AFEC0B3<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> </dl>

 

