---
title: Interface IVMUSBDeviceCollection (VPCCOMInterfaces.h)
description: Define a coleção de dispositivos USB anexados ao sistema host. Para obter um objeto IVMUSBDeviceCollection, use a propriedade IVMVirtualPC USBDeviceCollection.
ms.assetid: a5cca485-29d3-47fa-9cda-fedcdc379155
keywords:
- IVMUSBDeviceCollection interface Virtual PC
- INTERFACE IVMUSBDeviceCollection pc virtual , descrito
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1daf5df827bd9d890ede26242957adb2da8a025e8b1d272254e145b12f5aee91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752535"
---
# <a name="ivmusbdevicecollection-interface"></a>Interface IVMUSBDeviceCollection

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define a coleção de dispositivos USB anexados ao sistema host. Para obter um **objeto IVMUSBDeviceCollection,** use a [**propriedade IVMVirtualPC::USBDeviceCollection.**](ivmvirtualpc-usbdevicecollection.md)

## <a name="members"></a>Membros

A interface **IVMUSBDeviceCollection** herda da interface [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMUSBDeviceCollection** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IVMUSBDeviceCollection** tem essas propriedades.



| Propriedade                                                        | Tipo de acesso          | Descrição                                                                         |
|:----------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmusbdevicecollection--newenum.md)<br/> | Somente leitura<br/> | Um enumerador para a coleção.<br/>                                        |
| [**Contagem**](ivmusbdevicecollection-count.md)<br/>        | Somente leitura<br/> | O número de dispositivos USB nesta coleção.<br/>                            |
| [**Item**](ivmusbdevicecollection-item.md)<br/>          | Somente leitura<br/> | O objeto de dispositivo USB que corresponde ao índice especificado (baseado em 1).<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMUSBDeviceCollection é definido como 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749<br/>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> <dt>

[**IVMVirtualPC::USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md)
</dt> </dl>

 

