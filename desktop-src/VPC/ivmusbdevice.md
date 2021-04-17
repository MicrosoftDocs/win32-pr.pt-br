---
title: Interface IVMUSBDevice (VPCCOMInterfaces. h)
description: Define a interface para um dispositivo USB conectado ao host. Você pode anexar o dispositivo USB a uma máquina virtual para usar o dispositivo dentro da máquina virtual.
ms.assetid: f491fe8f-bc43-4dfa-b9c1-c93b4e5a7df6
keywords:
- Virtual PC de interface IVMUSBDevice
- Virtual PC de interface IVMUSBDevice, descrito
topic_type:
- apiref
api_name:
- IVMUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a1547bd812ea6d8f117f5910a254334676cafd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105794598"
---
# <a name="ivmusbdevice-interface"></a>Interface IVMUSBDevice

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define a interface para um dispositivo USB conectado ao host. Você pode anexar o dispositivo USB a uma máquina virtual para usar o dispositivo dentro da máquina virtual.

## <a name="members"></a>Membros

A interface **IVMUSBDevice** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMUSBDevice** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IVMUSBDevice** tem essas propriedades.



| Propriedade                                                                 | Tipo de acesso          | Descrição                                                                     |
|:-------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [**AttachedToVM**](ivmusbdevice-attachedtovm.md)<br/>             | Somente leitura<br/> | O nome da máquina virtual à qual o dispositivo USB está anexado.<br/> |
| [**DeviceClass**](ivmusbdevice-deviceclass.md)<br/>               | Somente leitura<br/> | A classe de dispositivo do dispositivo USB.<br/>                                  |
| [**DeviceString**](ivmusbdevice-devicestring.md)<br/>             | Somente leitura<br/> | O nome do dispositivo USB.<br/>                                          |
| [**HubID**](ivmusbdevice-hubid.md)<br/>                           | Somente leitura<br/> | O identificador do Hub no qual o dispositivo está conectado.<br/>          |
| [**Manufacturerstring**](ivmusbdevice-manufacturerstring.md)<br/> | Somente leitura<br/> | O nome do fabricante do dispositivo USB.<br/>                             |
| [**Porta**](ivmusbdevice-port.md)<br/>                             | Somente leitura<br/> | O identificador da porta na qual o dispositivo está conectado.<br/>         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMUSBDevice é definido como 63C1258C-5721-4070-B86B-A6CE2AFEC0B3<br/>               |



 

