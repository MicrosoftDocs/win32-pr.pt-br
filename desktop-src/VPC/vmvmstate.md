---
title: Enumeração VMVMState (VPCCOMInterfaces. h)
description: Especifica o estado de uma máquina virtual.
ms.assetid: 952dab9d-3d38-4cc5-ab75-4ee5096f7923
keywords:
- VMVMState de enumeração Virtual PC
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
ms.openlocfilehash: 45505e4fb4b444b15697afca4576e889f2da9a6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105813460"
---
# <a name="vmvmstate-enumeration"></a><span data-ttu-id="59ad9-104">Enumeração VMVMState</span><span class="sxs-lookup"><span data-stu-id="59ad9-104">VMVMState enumeration</span></span>

<span data-ttu-id="59ad9-105">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="59ad9-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="59ad9-106">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="59ad9-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="59ad9-107">Especifica o estado de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="59ad9-107">Specifies the state of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="59ad9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="59ad9-108">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="59ad9-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="59ad9-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="59ad9-110"><span id="vmVMState_Invalid"></span><span id="vmvmstate_invalid"></span><span id="VMVMSTATE_INVALID"></span>**vmVMState \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="59ad9-110"><span id="vmVMState_Invalid"></span><span id="vmvmstate_invalid"></span><span id="VMVMSTATE_INVALID"></span>**vmVMState\_Invalid**</span></span>
</dt> <dd>

<span data-ttu-id="59ad9-111">Um estado inválido (não deve ocorrer se a máquina virtual existir).</span><span class="sxs-lookup"><span data-stu-id="59ad9-111">An invalid state (should not occur if the virtual machine exists).</span></span>

</dd> <dt>

<span data-ttu-id="59ad9-112"><span id="vmVMState_TurnedOff"></span><span id="vmvmstate_turnedoff"></span><span id="VMVMSTATE_TURNEDOFF"></span>**vmVMState \_ TurnedOff**</span><span class="sxs-lookup"><span data-stu-id="59ad9-112"><span id="vmVMState_TurnedOff"></span><span id="vmvmstate_turnedoff"></span><span id="VMVMSTATE_TURNEDOFF"></span>**vmVMState\_TurnedOff**</span></span>
</dt> <dd>

<span data-ttu-id="59ad9-113">Desativado e não salvo.</span><span class="sxs-lookup"><span data-stu-id="59ad9-113">Off and not saved.</span></span>

</dd> <dt>

<span data-ttu-id="59ad9-114"><span id="vmVMState_Saved"></span><span id="vmvmstate_saved"></span><span id="VMVMSTATE_SAVED"></span>**vmVMState \_ salvo**</span><span class="sxs-lookup"><span data-stu-id="59ad9-114"><span id="vmVMState_Saved"></span><span id="vmvmstate_saved"></span><span id="VMVMSTATE_SAVED"></span>**vmVMState\_Saved**</span></span>
</dt> <dd>

<span data-ttu-id="59ad9-115">Desativado, mas o convidado é salvo.</span><span class="sxs-lookup"><span data-stu-id="59ad9-115">Off but the guest is saved.</span></span>

</dd> <dt>

<span data-ttu-id="59ad9-116"><span id="vmVMState_TurningOn"></span><span id="vmvmstate_turningon"></span><span id="VMVMSTATE_TURNINGON"></span>**ativação do vmVMState \_**</span><span class="sxs-lookup"><span data-stu-id="59ad9-116"><span id="vmVMState_TurningOn"></span><span id="vmvmstate_turningon"></span><span id="VMVMSTATE_TURNINGON"></span>**vmVMState\_TurningOn**</span></span>
</dt> <dd>

<span data-ttu-id="59ad9-117">No processo de ativação.</span><span class="sxs-lookup"><span data-stu-id="59ad9-117">In the process of turning on.</span></span>

</dd> <dt>

<span data-ttu-id="59ad9-118"><span id="vmVMState_Restoring"></span><span id="vmvmstate_restoring"></span><span id="VMVMSTATE_RESTORING"></span>**vmVMState \_ restaurando**</span><span class="sxs-lookup"><span data-stu-id="59ad9-118"><span id="vmVMState_Restoring"></span><span id="vmvmstate_restoring"></span><span id="VMVMSTATE_RESTORING"></span>**vmVMState\_Restoring**</span></span>
</dt> <dd>

<span data-ttu-id="59ad9-119">Restaurando o estado.</span><span class="sxs-lookup"><span data-stu-id="59ad9-119">Restoring the state.</span></span>

</dd> <dt>

<span data-ttu-id="59ad9-120"><span id="vmVMState_Running"></span><span id="vmvmstate_running"></span><span id="VMVMSTATE_RUNNING"></span>**vmVMState \_ em execução**</span><span class="sxs-lookup"><span data-stu-id="59ad9-120"><span id="vmVMState_Running"></span><span id="vmvmstate_running"></span><span id="VMVMSTATE_RUNNING"></span>**vmVMState\_Running**</span></span>
</dt> <dd>

<span data-ttu-id="59ad9-121">Em execução e não em pausa.</span><span class="sxs-lookup"><span data-stu-id="59ad9-121">Running and not paused.</span></span>

</dd> <dt>

<span data-ttu-id="59ad9-122"><span id="vmVMState_Paused"></span><span id="vmvmstate_paused"></span><span id="VMVMSTATE_PAUSED"></span>**vmVMState em \_ pausa**</span><span class="sxs-lookup"><span data-stu-id="59ad9-122"><span id="vmVMState_Paused"></span><span id="vmvmstate_paused"></span><span id="VMVMSTATE_PAUSED"></span>**vmVMState\_Paused**</span></span>
</dt> <dd>

<span data-ttu-id="59ad9-123">Em execução e em pausa.</span><span class="sxs-lookup"><span data-stu-id="59ad9-123">Running and paused.</span></span>

</dd> <dt>

<span data-ttu-id="59ad9-124"><span id="vmVMState_Saving"></span><span id="vmvmstate_saving"></span><span id="VMVMSTATE_SAVING"></span>**vmVMState \_ salvar**</span><span class="sxs-lookup"><span data-stu-id="59ad9-124"><span id="vmVMState_Saving"></span><span id="vmvmstate_saving"></span><span id="VMVMSTATE_SAVING"></span>**vmVMState\_Saving**</span></span>
</dt> <dd>

<span data-ttu-id="59ad9-125">Salvando o estado.</span><span class="sxs-lookup"><span data-stu-id="59ad9-125">Saving the state.</span></span>

</dd> <dt>

<span data-ttu-id="59ad9-126"><span id="vmVMState_TurningOff"></span><span id="vmvmstate_turningoff"></span><span id="VMVMSTATE_TURNINGOFF"></span>**vmVMState \_ TurningOff**</span><span class="sxs-lookup"><span data-stu-id="59ad9-126"><span id="vmVMState_TurningOff"></span><span id="vmvmstate_turningoff"></span><span id="VMVMSTATE_TURNINGOFF"></span>**vmVMState\_TurningOff**</span></span>
</dt> <dd>

<span data-ttu-id="59ad9-127">No processo de desligamento.</span><span class="sxs-lookup"><span data-stu-id="59ad9-127">In the process of turning off.</span></span>

</dd> <dt>

<span data-ttu-id="59ad9-128"><span id="vmVMState_MergingDrives"></span><span id="vmvmstate_mergingdrives"></span><span id="VMVMSTATE_MERGINGDRIVES"></span>**vmVMState \_ MergingDrives**</span><span class="sxs-lookup"><span data-stu-id="59ad9-128"><span id="vmVMState_MergingDrives"></span><span id="vmvmstate_mergingdrives"></span><span id="VMVMSTATE_MERGINGDRIVES"></span>**vmVMState\_MergingDrives**</span></span>
</dt> <dd>

<span data-ttu-id="59ad9-129">No processo de mesclagem de unidades de desfazer.</span><span class="sxs-lookup"><span data-stu-id="59ad9-129">In the process of merging undo drives.</span></span>

</dd> <dt>

<span data-ttu-id="59ad9-130"><span id="vmVMState_DeleteMachine"></span><span id="vmvmstate_deletemachine"></span><span id="VMVMSTATE_DELETEMACHINE"></span>**vmVMState \_ DeleteMachine**</span><span class="sxs-lookup"><span data-stu-id="59ad9-130"><span id="vmVMState_DeleteMachine"></span><span id="vmvmstate_deletemachine"></span><span id="VMVMSTATE_DELETEMACHINE"></span>**vmVMState\_DeleteMachine**</span></span>
</dt> <dd>

<span data-ttu-id="59ad9-131">Excluindo a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="59ad9-131">Deleting the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="59ad9-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59ad9-132">Requirements</span></span>



| <span data-ttu-id="59ad9-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="59ad9-133">Requirement</span></span> | <span data-ttu-id="59ad9-134">Valor</span><span class="sxs-lookup"><span data-stu-id="59ad9-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="59ad9-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59ad9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="59ad9-136">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="59ad9-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="59ad9-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59ad9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="59ad9-138">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="59ad9-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="59ad9-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="59ad9-139">End of client support</span></span><br/>    | <span data-ttu-id="59ad9-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="59ad9-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="59ad9-141">Produto</span><span class="sxs-lookup"><span data-stu-id="59ad9-141">Product</span></span><br/>                  | <span data-ttu-id="59ad9-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="59ad9-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="59ad9-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="59ad9-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="59ad9-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="59ad9-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59ad9-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="59ad9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59ad9-146">**IVMVirtualMachine:: State**</span><span class="sxs-lookup"><span data-stu-id="59ad9-146">**IVMVirtualMachine::State**</span></span>](ivmvirtualmachine-state.md)
</dt> <dt>

[<span data-ttu-id="59ad9-147">**IVMVirtualMachineEvents:: OnStateChange**</span><span class="sxs-lookup"><span data-stu-id="59ad9-147">**IVMVirtualMachineEvents::OnStateChange**</span></span>](ivmvirtualmachineevents-onstatechange.md)
</dt> <dt>

[<span data-ttu-id="59ad9-148">**IVMVirtualPCEvents::OnVMStateChange**</span><span class="sxs-lookup"><span data-stu-id="59ad9-148">**IVMVirtualPCEvents::OnVMStateChange**</span></span>](ivmvirtualpcevents-onvmstatechange.md)
</dt> </dl>

 

