---
title: Interface IVMFloppyDriveEvents (VPCCOMInterfaces.h)
description: Define a interface de evento de saída para a interface IVMFloppyDrive. O cliente implementa esses métodos para receber eventos enviados de IVMFloppyDrive.
ms.assetid: fbb66554-f042-4891-94be-1a12b8c179c2
keywords:
- IVMFloppyDriveEvents interface Virtual PC
- INTERFACE IVMFloppyDriveEvents pc virtual , descrito
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
ms.openlocfilehash: 53cd275c45e23de1bb437b4c233ff64118952afae76e7c6b9bc9366facf4fe8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653506"
---
# <a name="ivmfloppydriveevents-interface"></a>Interface IVMFloppyDriveEvents

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define a interface de evento de saída para a interface [**IVMFloppyDrive.**](ivmfloppydrive.md) O cliente implementa esses métodos para receber eventos enviados de **IVMFloppyDrive**.

## <a name="members"></a>Membros

A interface **IVMFloppyDriveEvents** herda da interface [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMFloppyDriveEvents** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IVMFloppyDriveEvents** tem esses métodos.



| Método                                                      | Descrição                                                                   |
|:------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**OnMediaEject**](ivmfloppydriveevents-onmediaeject.md)   | Recebe uma notificação de que a mídia foi ejetada da unidade.<br/>  |
| [**OnMediaInsert**](ivmfloppydriveevents-onmediainsert.md) | Recebe uma notificação de que a mídia foi inserida na unidade.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMFloppyDriveEvents é definido como a9ed3401-4e09-4177-86ec-a13bf9fa7d4e<br/>      |



 

