---
title: Interface IVMDVDDriveEvents (VPCCOMInterfaces.h)
description: Define a interface de evento de saída para a interface IVMDVDDrive.
ms.assetid: aa68fb6f-032d-4322-8553-b1e840ae63b8
keywords:
- COMPUTADOR Virtual da interface IVMDVDDriveEvents
- INTERFACE IVMDVDDriveEvents pc virtual , descrito
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
ms.openlocfilehash: dcb34bf77b6692c90977262ac7e2177019169e3195ee44415a0693102e6d15ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136789"
---
# <a name="ivmdvddriveevents-interface"></a>Interface IVMDVDDriveEvents

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define a interface de evento de saída para a interface [**IVMDVDDrive.**](ivmdvddrive.md)

## <a name="members"></a>Membros

A interface **IVMDVDDriveEvents** herda da interface [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMDVDDriveEvents** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IVMDVDDriveEvents** tem esses métodos.



| Método                                                   | Descrição                                                                   |
|:---------------------------------------------------------|:------------------------------------------------------------------------------|
| [**OnMediaEject**](ivmdvddriveevents-onmediaeject.md)   | Recebe uma notificação de que a mídia foi ejetada da unidade.<br/>  |
| [**OnMediaInsert**](ivmdvddriveevents-onmediainsert.md) | Recebe uma notificação de que a mídia foi inserida na unidade.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMDVDDriveEvents é definido como c2a7d8e9-e76c-4eb8-94f7-71a5122d249b<br/>         |



 

