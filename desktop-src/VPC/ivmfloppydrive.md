---
title: Interface IVMFloppyDrive (VPCCOMInterfaces. h)
description: Controla uma unidade de disquete em uma máquina virtual.
ms.assetid: b652182a-27ae-4390-81b1-b644a82924df
keywords:
- Virtual PC de interface IVMFloppyDrive
- Virtual PC de interface IVMFloppyDrive, descrito
topic_type:
- apiref
api_name:
- IVMFloppyDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63db224861b547b9485b03080ce3ffb3f5c118ef0de71597db79aa0888a1528d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594802"
---
# <a name="ivmfloppydrive-interface"></a>Interface IVMFloppyDrive

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Controla uma unidade de disquete em uma máquina virtual. **IVMFloppyDrive** pode notificar clientes sobre eventos usando a interface de saída do [**IVMFloppyDriveEvents**](ivmfloppydriveevents.md) . Você pode recuperar um objeto **IVMFloppyDrive** do objeto [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md) retornado da propriedade [**IVMVirtualMachine:: FloppyDrives**](ivmvirtualmachine-floppydrives.md) .

## <a name="members"></a>Membros

A interface **IVMFloppyDrive** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMFloppyDrive** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IVMFloppyDrive** tem esses métodos.



| Método                                                      | Descrição                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**AttachHostDrive**](ivmfloppydrive-attachhostdrive.md)   | Anexa uma unidade física no host à unidade de disquete na máquina virtual.<br/> |
| [**AttachImage**](ivmfloppydrive-attachimage.md)           | Anexa uma imagem de mídia de disquete no host à unidade de disquete.<br/>                    |
| [**ReleaseHostDrive**](ivmfloppydrive-releasehostdrive.md) | Libera uma unidade física no host da unidade de disquete.<br/>                      |
| [**ReleaseImage**](ivmfloppydrive-releaseimage.md)         | Libera uma imagem de mídia de disquete no host da unidade de disquete.<br/>                  |



 

### <a name="properties"></a>Propriedades

A interface **IVMFloppyDrive** tem essas propriedades.



| Propriedade                                                             | Tipo de acesso          | Descrição                                                                               |
|:---------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------|
| [**Anexo**](ivmfloppydrive-attachment.md)<br/>           | Somente leitura<br/> | O tipo de mídia anexada à unidade de disquete na máquina virtual.<br/>     |
| [**DriveNumber**](ivmfloppydrive-drivenumber.md)<br/>         | Somente leitura<br/> | O índice de base zero do controlador ao qual esta unidade de disquete está anexada.<br/> |
| [**HostDriveLetter**](ivmfloppydrive-hostdriveletter.md)<br/> | Somente leitura<br/> | A letra da unidade do host à qual a unidade de disquete está conectada.<br/>            |
| [**ImageFile**](ivmfloppydrive-imagefile.md)<br/>             | Somente leitura<br/> | O caminho completo do arquivo de imagem ao qual a unidade de disquete está anexada.<br/>         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDrive é definido como 661abee6-112a-4ed9-babf-3c874969f10e<br/>             |



 

