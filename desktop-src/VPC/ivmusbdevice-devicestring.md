---
title: Propriedade DeviceString IVMUSBDevice (VPCCOMInterfaces.h)
description: Recupera o nome do dispositivo USB.
ms.assetid: 2ae82e2a-b33a-4039-acdb-958b094b1045
keywords:
- Propriedade DeviceString Pc Virtual
- Propriedade DeviceString Pc Virtual , interface IVMUSBDevice
- INTERFACE IVMUSB Pc Virtual , propriedade DeviceString
topic_type:
- apiref
api_name:
- IVMUSBDevice.DeviceString
- IVMUSBDevice.get_DeviceString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efab8af122c0411ffaaca23302893ef2b354611e5c2d24fbd30e17eaa4782e8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752555"
---
# <a name="ivmusbdevicedevicestring-property"></a>Propriedade IVMUSBDevice::D eviceString

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o nome do dispositivo USB.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_DeviceString(
  [out, retval] BSTR *deviceName
);
```



## <a name="property-value"></a>Valor da propriedade

O nome do dispositivo USB.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                            | Significado                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>               | O método foi concluído com êxito.<br/> |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl> | O parâmetro é **NULL.**<br/>         |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMUSBDevice é definido como \_ 63C1258C-5721-4070-B86B-A6CE2AFEC0B3<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> </dl>

 

