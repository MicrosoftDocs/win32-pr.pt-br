---
title: Enumeração VMVMState (VPCCOMInterfaces.h)
description: Especifica o estado de uma máquina virtual.
ms.assetid: 952dab9d-3d38-4cc5-ab75-4ee5096f7923
keywords:
- VMVMState enumeration Virtual PC
topic_type:
- apiref
api_name:
- VMVMState
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cff8beb6d0ea01ab60be7a7908fceec32422ef3a9ba06b801df2af94130c526
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998306"
---
# <a name="vmvmstate-enumeration"></a>Enumeração VMVMState

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Especifica o estado de uma máquina virtual.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmVMState_Invalid        = 0,
  vmVMState_TurnedOff      = 1,
  vmVMState_Saved          = 2,
  vmVMState_TurningOn      = 3,
  vmVMState_Restoring      = 4,
  vmVMState_Running        = 5,
  vmVMState_Paused         = 6,
  vmVMState_Saving         = 7,
  vmVMState_TurningOff     = 8,
  vmVMState_MergingDrives  = 9,
  vmVMState_DeleteMachine  = 10
} VMVMState;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="vmVMState_Invalid"></span><span id="vmvmstate_invalid"></span><span id="VMVMSTATE_INVALID"></span>**vmVMState \_ inválido**
</dt> <dd>

Um estado inválido (não deve ocorrer se a máquina virtual existir).

</dd> <dt>

<span id="vmVMState_TurnedOff"></span><span id="vmvmstate_turnedoff"></span><span id="VMVMSTATE_TURNEDOFF"></span>**vmVMState \_ TurnedOff**
</dt> <dd>

Desligado e não salvo.

</dd> <dt>

<span id="vmVMState_Saved"></span><span id="vmvmstate_saved"></span><span id="VMVMSTATE_SAVED"></span>**vmVMState \_ salvo**
</dt> <dd>

Desligado, mas o convidado é salvo.

</dd> <dt>

<span id="vmVMState_TurningOn"></span><span id="vmvmstate_turningon"></span><span id="VMVMSTATE_TURNINGON"></span>**vmVMState \_ TurningOn**
</dt> <dd>

No processo de a ligar.

</dd> <dt>

<span id="vmVMState_Restoring"></span><span id="vmvmstate_restoring"></span><span id="VMVMSTATE_RESTORING"></span>**Restauração de vmVMState \_**
</dt> <dd>

Restaurando o estado.

</dd> <dt>

<span id="vmVMState_Running"></span><span id="vmvmstate_running"></span><span id="VMVMSTATE_RUNNING"></span>**vmVMState em \_ execução**
</dt> <dd>

Em execução e não em pausa.

</dd> <dt>

<span id="vmVMState_Paused"></span><span id="vmvmstate_paused"></span><span id="VMVMSTATE_PAUSED"></span>**vmVMState \_ em pausa**
</dt> <dd>

Em execução e em pausa.

</dd> <dt>

<span id="vmVMState_Saving"></span><span id="vmvmstate_saving"></span><span id="VMVMSTATE_SAVING"></span>**vmVMState \_ Saving**
</dt> <dd>

Salvando o estado.

</dd> <dt>

<span id="vmVMState_TurningOff"></span><span id="vmvmstate_turningoff"></span><span id="VMVMSTATE_TURNINGOFF"></span>**vmVMState \_ TurningOff**
</dt> <dd>

No processo de desligar.

</dd> <dt>

<span id="vmVMState_MergingDrives"></span><span id="vmvmstate_mergingdrives"></span><span id="VMVMSTATE_MERGINGDRIVES"></span>**vmVMState \_ MergingDrives**
</dt> <dd>

No processo de mesclar unidades de desfazer.

</dd> <dt>

<span id="vmVMState_DeleteMachine"></span><span id="vmvmstate_deletemachine"></span><span id="VMVMSTATE_DELETEMACHINE"></span>**vmVMState \_ DeleteMachine**
</dt> <dd>

Excluindo a máquina virtual.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualMachine::State**](ivmvirtualmachine-state.md)
</dt> <dt>

[**IVMVirtualMachineEvents::OnStateChange**](ivmvirtualmachineevents-onstatechange.md)
</dt> <dt>

[**IVMVirtualPCEvents::OnVMStateChange**](ivmvirtualpcevents-onvmstatechange.md)
</dt> </dl>

 

