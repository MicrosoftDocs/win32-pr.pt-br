---
title: Interface IVMVirtualPCEvents (VPCCOMInterfaces. h)
description: Define a interface de evento de saída para a interface IVMVirtualPC.
ms.assetid: 40ce14d8-43e4-4c72-9729-e5503d882be6
keywords:
- Virtual PC de interface IVMVirtualPCEvents
- Virtual PC de interface IVMVirtualPCEvents, descrito
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3a6fd22f75027d1424b8605e8e36e373064069
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009609"
---
# <a name="ivmvirtualpcevents-interface"></a>Interface IVMVirtualPCEvents

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define a interface de evento de saída para a interface [**IVMVirtualPC**](ivmvirtualpc.md) . O cliente implementa esses métodos para receber eventos enviados do [**IVMVirtualPC**](ivmvirtualpc.md).

## <a name="members"></a>Membros

A interface **IVMVirtualPCEvents** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualPCEvents** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IVMVirtualPCEvents** tem esses métodos.



| Método                                                        | Descrição                                                                  |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**OnEventLogged**](ivmvirtualpcevents-oneventlogged.md)     | Recebe uma notificação de que o Windows Virtual PC registra um evento.<br/>      |
| [**OnVMStateChange**](ivmvirtualpcevents-onvmstatechange.md) | Recebe a notificação de que o estado de uma máquina virtual foi alterado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualPCEvents é definido como efed1ef1-3c09-41F7-a9c2-7e29fa286c9d<br/>        |



 

