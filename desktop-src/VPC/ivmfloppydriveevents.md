---
title: Interface IVMFloppyDriveEvents (VPCCOMInterfaces. h)
description: Define a interface de evento de saída para a interface IVMFloppyDrive. O cliente implementa esses métodos para receber eventos enviados do IVMFloppyDrive.
ms.assetid: fbb66554-f042-4891-94be-1a12b8c179c2
keywords:
- Virtual PC de interface IVMFloppyDriveEvents
- Virtual PC de interface IVMFloppyDriveEvents, descrito
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f9b799bd6227882c2991f9b310f39d38b20692d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086349"
---
# <a name="ivmfloppydriveevents-interface"></a>Interface IVMFloppyDriveEvents

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define a interface de evento de saída para a interface [**IVMFloppyDrive**](ivmfloppydrive.md) . O cliente implementa esses métodos para receber eventos enviados do **IVMFloppyDrive**.

## <a name="members"></a>Membros

A interface **IVMFloppyDriveEvents** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMFloppyDriveEvents** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IVMFloppyDriveEvents** tem esses métodos.



| Método                                                      | Descrição                                                                   |
|:------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**OnMediaEject**](ivmfloppydriveevents-onmediaeject.md)   | Recebe a notificação de que a mídia foi ejetada da unidade.<br/>  |
| [**OnMediaInsert**](ivmfloppydriveevents-onmediainsert.md) | Recebe a notificação de que a mídia foi inserida na unidade.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMFloppyDriveEvents é definido como a9ed3401-4e09-4177-86ec-a13bf9fa7d4e<br/>      |



 

