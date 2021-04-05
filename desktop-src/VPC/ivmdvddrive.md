---
title: Interface IVMDVDDrive (VPCCOMInterfaces. h)
description: Controla uma unidade de CD-ROM ou DVD-ROM em uma máquina virtual. IVMDVDDrive pode notificar clientes sobre eventos usando a interface de saída do IVMDVDDriveEvents.
ms.assetid: 0900b3a8-ba52-4c26-bd96-b37334d6d03c
keywords:
- Virtual PC de interface IVMDVDDrive
- Virtual PC de interface IVMDVDDrive, descrito
topic_type:
- apiref
api_name:
- IVMDVDDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 951213923f74f8425fc4d9eaec85e76f7481eeb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009504"
---
# <a name="ivmdvddrive-interface"></a>Interface IVMDVDDrive

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Controla uma unidade de CD-ROM ou DVD-ROM em uma máquina virtual. **IVMDVDDrive** pode notificar clientes sobre eventos usando a interface de saída do [**IVMDVDDriveEvents**](ivmdvddriveevents.md) .

Você pode adicionar uma nova unidade de CD-ROM ou DVD-ROM a uma máquina virtual usando o método [**IVMVirtualMachine:: AddDVDROMDrive**](ivmvirtualmachine-adddvdromdrive.md) . Você pode remover uma unidade de CD-ROM ou DVD-ROM existente de uma máquina virtual usando o método [**IVMVirtualMachine:: RemoveDVDROMDrive**](ivmvirtualmachine-removedvdromdrive.md) . Você pode recuperar um objeto **IVMDVDDrive** do objeto [**IVMDVDDriveCollection**](ivmdvddrivecollection.md) retornado da propriedade [**IVMVirtualMachine::D vdromdrives**](ivmvirtualmachine-dvdromdrives.md) .

## <a name="members"></a>Membros

A interface **IVMDVDDrive** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMDVDDrive** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IVMDVDDrive** tem esses métodos.



| Método                                                   | Descrição                                                                             |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**AttachHostDrive**](ivmdvddrive-attachhostdrive.md)   | Anexa uma unidade de host à unidade de DVD na máquina virtual.<br/>           |
| [**AttachImage**](ivmdvddrive-attachimage.md)           | Anexa uma imagem ISO à unidade de DVD na máquina virtual.<br/>           |
| [**ReleaseHostDrive**](ivmdvddrive-releasehostdrive.md) | Libera uma unidade de host capturada da unidade de DVD.<br/>                           |
| [**ReleaseImage**](ivmdvddrive-releaseimage.md)         | Libera uma imagem ISO capturada da unidade de DVD.<br/>                            |
| [**SetBusLocation**](ivmdvddrive-setbuslocation.md)     | Anexa a unidade de DVD ao local do barramento especificado na máquina virtual.<br/> |



 

### <a name="properties"></a>Propriedades

A interface **IVMDVDDrive** tem essas propriedades.



| Propriedade                                                          | Tipo de acesso          | Descrição                                                                        |
|:------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [**Anexo**](ivmdvddrive-attachment.md)<br/>           | Somente leitura<br/> | O tipo de mídia anexada à unidade de DVD na máquina virtual.<br/> |
| [**BusNumber**](ivmdvddrive-busnumber.md)<br/>             | Somente leitura<br/> | O número do barramento ao qual este dispositivo está anexado.<br/>                        |
| [**DeviceNumber**](ivmdvddrive-devicenumber.md)<br/>       | Somente leitura<br/> | O número do dispositivo ao qual esta unidade está anexada.<br/>                      |
| [**HostDriveLetter**](ivmdvddrive-hostdriveletter.md)<br/> | Somente leitura<br/> | A letra da unidade do host definida para este dispositivo.<br/>                       |
| [**ImageFile**](ivmdvddrive-imagefile.md)<br/>             | Somente leitura<br/> | O caminho completo do conjunto de arquivos de imagem para este dispositivo.<br/>                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive é definido como b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



 

