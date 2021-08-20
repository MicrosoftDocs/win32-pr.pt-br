---
title: Interface IVMVirtualMachineEvents (VPCCOMInterfaces. h)
description: Define a interface de evento de saída para a interface IVMVirtualMachine.
ms.assetid: 52901a95-0f4f-4503-97c5-1459179feeb8
keywords:
- Virtual PC de interface IVMVirtualMachineEvents
- Virtual PC de interface IVMVirtualMachineEvents, descrito
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6686585333f33d4732284ab448a82ac722fea03315b08aaa276f2eeabaf2e02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122616"
---
# <a name="ivmvirtualmachineevents-interface"></a>Interface IVMVirtualMachineEvents

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define a interface de evento de saída para a interface [**IVMVirtualMachine**](ivmvirtualmachine.md) . O cliente implementa esses métodos para receber eventos enviados do [**IVMVirtualMachine**](ivmvirtualmachine.md).

## <a name="members"></a>Membros

A interface **IVMVirtualMachineEvents** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualMachineEvents** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IVMVirtualMachineEvents** tem esses métodos.



| Método                                                                                   | Descrição                                                                                                                                     |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnAdditionsAvailable**](ivmvirtualmachineevents-onadditionsavailable.md)             | Recebe a notificação de que os componentes de integração estão disponíveis em uma máquina virtual.<br/>                                                |
| [**OnAdditionsUninstalled**](ivmvirtualmachineevents-onadditionsuninstalled.md)         | Recebe a notificação de que os componentes de integração são desinstalados em uma máquina virtual.<br/>                                              |
| [**Onconfigurationchanged**](ivmvirtualmachineevents-onconfigurationchanged.md)         | Recebe uma notificação de que um valor na configuração para esta máquina virtual foi alterado.<br/>                                        |
| [**OnDiskOutOfSpace**](ivmvirtualmachineevents-ondiskoutofspace.md)                     | Recebe uma notificação de que um disco necessário para uma máquina virtual está sem espaço e a máquina virtual não pode ser executada.<br/>           |
| [**OnEnhancedVideoModeChanged**](ivmvirtualmachineevents-onenhancedvideomodechanged.md) | Recebe a notificação de que o suporte de uma máquina virtual para o modo de vídeo avançado foi alterado.<br/>                                          |
| [**OnGuestLogoff**](ivmvirtualmachineevents-onguestlogoff.md)                           | Recebe a notificação de que um usuário fez logoff do sistema operacional convidado.<br/>                                                    |
| [**OnGuestShutdown**](ivmvirtualmachineevents-onguestshutdown.md)                       | Recebe a notificação de que o sistema operacional convidado foi desligado.<br/>                                                                     |
| [**OnHeartbeatStopped**](ivmvirtualmachineevents-onheartbeatstopped.md)                 | Recebe a notificação de que a pulsação de uma máquina virtual foi interrompida. Isso geralmente indica que o sistema operacional convidado falhou.<br/> |
| [**OnRequestShutdown**](ivmvirtualmachineevents-onrequestshutdown.md)                   | Recebe a notificação de que uma solicitação de desligamento foi feita.<br/>                                                                         |
| [**OnReset**](ivmvirtualmachineevents-onreset.md)                                       | Recebe a notificação de que uma máquina virtual foi redefinida.<br/>                                                                         |
| [**OnStateChange**](ivmvirtualmachineevents-onstatechange.md)                           | Recebe a notificação de que o estado de uma máquina virtual foi alterado.<br/>                                                                    |
| [**OnTripleFault**](ivmvirtualmachineevents-ontriplefault.md)                           | Recebe uma notificação de que uma máquina virtual tem falha tripla.<br/>                                                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents é definido como 9d84f560-bb67-4961-BD12-a4da780c67e4<br/>   |



 

