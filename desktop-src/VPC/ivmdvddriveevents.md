---
title: Interface IVMDVDDriveEvents (VPCCOMInterfaces. h)
description: Define a interface de evento de saída para a interface IVMDVDDrive.
ms.assetid: aa68fb6f-032d-4322-8553-b1e840ae63b8
keywords:
- Virtual PC de interface IVMDVDDriveEvents
- Virtual PC de interface IVMDVDDriveEvents, descrito
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b301a423f5272288c12a900d0fbd19c0a5d5170
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455911"
---
# <a name="ivmdvddriveevents-interface"></a>Interface IVMDVDDriveEvents

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define a interface de evento de saída para a interface [**IVMDVDDrive**](ivmdvddrive.md) .

## <a name="members"></a>Membros

A interface **IVMDVDDriveEvents** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMDVDDriveEvents** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IVMDVDDriveEvents** tem esses métodos.



| Método                                                   | Descrição                                                                   |
|:---------------------------------------------------------|:------------------------------------------------------------------------------|
| [**OnMediaEject**](ivmdvddriveevents-onmediaeject.md)   | Recebe a notificação de que a mídia foi ejetada da unidade.<br/>  |
| [**OnMediaInsert**](ivmdvddriveevents-onmediainsert.md) | Recebe a notificação de que a mídia foi inserida na unidade.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMDVDDriveEvents é definido como c2a7d8e9-E76C-4eb8-94f7-71a5122d249b<br/>         |



 

