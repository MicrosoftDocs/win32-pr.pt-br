---
title: Interface IVMUSBDeviceCollection (VPCCOMInterfaces. h)
description: Define a coleção de dispositivos USB conectados ao sistema host. Para obter um objeto IVMUSBDeviceCollection, use a propriedade IVMVirtualPC USBDeviceCollection.
ms.assetid: a5cca485-29d3-47fa-9cda-fedcdc379155
keywords:
- Virtual PC de interface IVMUSBDeviceCollection
- Virtual PC de interface IVMUSBDeviceCollection, descrito
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
ms.openlocfilehash: 3e773f006a1d98253a20ad37d5a70db43f487980
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770582"
---
# <a name="ivmusbdevicecollection-interface"></a>Interface IVMUSBDeviceCollection

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define a coleção de dispositivos USB conectados ao sistema host. Para obter um objeto **IVMUSBDeviceCollection** , use a propriedade [**IVMVirtualPC:: USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md) .

## <a name="members"></a>Membros

A interface **IVMUSBDeviceCollection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMUSBDeviceCollection** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IVMUSBDeviceCollection** tem essas propriedades.



| Propriedade                                                        | Tipo de acesso          | Descrição                                                                         |
|:----------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmusbdevicecollection--newenum.md)<br/> | Somente leitura<br/> | Um enumerador para a coleção.<br/>                                        |
| [**Contar**](ivmusbdevicecollection-count.md)<br/>        | Somente leitura<br/> | O número de dispositivos USB nesta coleção.<br/>                            |
| [**Item**](ivmusbdevicecollection-item.md)<br/>          | Somente leitura<br/> | O objeto de dispositivo USB que corresponde ao índice especificado (baseado em 1).<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMUSBDeviceCollection é definido como 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749<br/>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> <dt>

[**IVMVirtualPC::USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md)
</dt> </dl>

 

