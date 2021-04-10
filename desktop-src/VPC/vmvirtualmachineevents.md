---
title: Enumeração VMVirtualMachineEvents (VPCCOMInterfaces. h)
description: Especifica os eventos da VM.
ms.assetid: 158bdada-6fd3-488c-9ff1-e04df9a79127
keywords:
- VMVirtualMachineEvents de enumeração Virtual PC
topic_type:
- apiref
api_name:
- VMVirtualMachineEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1e1d8f4d89c28f63886444537fb9d894fc42e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009666"
---
# <a name="vmvirtualmachineevents-enumeration"></a><span data-ttu-id="0a734-104">Enumeração VMVirtualMachineEvents</span><span class="sxs-lookup"><span data-stu-id="0a734-104">VMVirtualMachineEvents enumeration</span></span>

<span data-ttu-id="0a734-105">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0a734-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0a734-106">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0a734-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0a734-107">Especifica os eventos de máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="0a734-107">Specifies the virtual machine (VM) events.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a734-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a734-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVirtualMachineEvent_StateChanged              = 1,
  vmVirtualMachineEvent_RequestShutdown           = 2,
  vmVirtualMachineEvent_Reset                     = 3,
  vmVirtualMachineEvent_TripleFault               = 4,
  vmVirtualMachineEvent_HeartbeatStopped          = 5,
  vmVirtualMachineEvent_ConfigurationChanged      = 6,
  vmVirtualMachineEvent_EnhancedVideoModeChanged  = 7,
  vmVirtualMachineEvent_AdditionsUninstalled      = 8,
  vmVirtualMachineEvent_AdditionsAvailable        = 9,
  vmVirtualMachineEvent_GuestShutdown             = 10,
  vmVirtualMachineEvent_GuestLogoff               = 11,
  vmVirtualMachineEvent_DiskOutOfSpace            = 12
} VMVirtualMachineEvents;
```



## <a name="constants"></a><span data-ttu-id="0a734-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="0a734-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0a734-110"><span id="vmVirtualMachineEvent_StateChanged"></span><span id="vmvirtualmachineevent_statechanged"></span><span id="VMVIRTUALMACHINEEVENT_STATECHANGED"></span>**\_estado vmVirtualMachineEvent**</span><span class="sxs-lookup"><span data-stu-id="0a734-110"><span id="vmVirtualMachineEvent_StateChanged"></span><span id="vmvirtualmachineevent_statechanged"></span><span id="VMVIRTUALMACHINEEVENT_STATECHANGED"></span>**vmVirtualMachineEvent\_StateChanged**</span></span>
</dt> <dd>

<span data-ttu-id="0a734-111">O estado de uma VM foi alterado.</span><span class="sxs-lookup"><span data-stu-id="0a734-111">A VM's state has changed.</span></span>

</dd> <dt>

<span data-ttu-id="0a734-112"><span id="vmVirtualMachineEvent_RequestShutdown"></span><span id="vmvirtualmachineevent_requestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_REQUESTSHUTDOWN"></span>**vmVirtualMachineEvent \_ RequestShutdown**</span><span class="sxs-lookup"><span data-stu-id="0a734-112"><span id="vmVirtualMachineEvent_RequestShutdown"></span><span id="vmvirtualmachineevent_requestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_REQUESTSHUTDOWN"></span>**vmVirtualMachineEvent\_RequestShutdown**</span></span>
</dt> <dd>

<span data-ttu-id="0a734-113">Foi solicitado um desligamento.</span><span class="sxs-lookup"><span data-stu-id="0a734-113">A shutdown has been requested.</span></span>

</dd> <dt>

<span data-ttu-id="0a734-114"><span id="vmVirtualMachineEvent_Reset"></span><span id="vmvirtualmachineevent_reset"></span><span id="VMVIRTUALMACHINEEVENT_RESET"></span>**redefinição de vmVirtualMachineEvent \_**</span><span class="sxs-lookup"><span data-stu-id="0a734-114"><span id="vmVirtualMachineEvent_Reset"></span><span id="vmvirtualmachineevent_reset"></span><span id="VMVIRTUALMACHINEEVENT_RESET"></span>**vmVirtualMachineEvent\_Reset**</span></span>
</dt> <dd>

<span data-ttu-id="0a734-115">Uma VM foi redefinida.</span><span class="sxs-lookup"><span data-stu-id="0a734-115">A VM has been reset.</span></span>

</dd> <dt>

<span data-ttu-id="0a734-116"><span id="vmVirtualMachineEvent_TripleFault"></span><span id="vmvirtualmachineevent_triplefault"></span><span id="VMVIRTUALMACHINEEVENT_TRIPLEFAULT"></span>**vmVirtualMachineEvent \_ TripleFault**</span><span class="sxs-lookup"><span data-stu-id="0a734-116"><span id="vmVirtualMachineEvent_TripleFault"></span><span id="vmvirtualmachineevent_triplefault"></span><span id="VMVIRTUALMACHINEEVENT_TRIPLEFAULT"></span>**vmVirtualMachineEvent\_TripleFault**</span></span>
</dt> <dd>

<span data-ttu-id="0a734-117">Uma VM tem três falhas.</span><span class="sxs-lookup"><span data-stu-id="0a734-117">A VM has triple-faulted.</span></span>

</dd> <dt>

<span data-ttu-id="0a734-118"><span id="vmVirtualMachineEvent_HeartbeatStopped"></span><span id="vmvirtualmachineevent_heartbeatstopped"></span><span id="VMVIRTUALMACHINEEVENT_HEARTBEATSTOPPED"></span>**vmVirtualMachineEvent \_ HeartbeatStopped**</span><span class="sxs-lookup"><span data-stu-id="0a734-118"><span id="vmVirtualMachineEvent_HeartbeatStopped"></span><span id="vmvirtualmachineevent_heartbeatstopped"></span><span id="VMVIRTUALMACHINEEVENT_HEARTBEATSTOPPED"></span>**vmVirtualMachineEvent\_HeartbeatStopped**</span></span>
</dt> <dd>

<span data-ttu-id="0a734-119">A pulsação de uma VM foi interrompida.</span><span class="sxs-lookup"><span data-stu-id="0a734-119">A VM's heartbeat has stopped.</span></span> <span data-ttu-id="0a734-120">Isso geralmente indica que o sistema operacional convidado falhou.</span><span class="sxs-lookup"><span data-stu-id="0a734-120">This usually indicates that the guest operating system has crashed.</span></span>

</dd> <dt>

<span data-ttu-id="0a734-121"><span id="vmVirtualMachineEvent_ConfigurationChanged"></span><span id="vmvirtualmachineevent_configurationchanged"></span><span id="VMVIRTUALMACHINEEVENT_CONFIGURATIONCHANGED"></span>**configuração de vmVirtualMachineEvent \_**</span><span class="sxs-lookup"><span data-stu-id="0a734-121"><span id="vmVirtualMachineEvent_ConfigurationChanged"></span><span id="vmvirtualmachineevent_configurationchanged"></span><span id="VMVIRTUALMACHINEEVENT_CONFIGURATIONCHANGED"></span>**vmVirtualMachineEvent\_ConfigurationChanged**</span></span>
</dt> <dd>

<span data-ttu-id="0a734-122">Um valor na configuração para esta VM foi alterado</span><span class="sxs-lookup"><span data-stu-id="0a734-122">A value in the configuration for this VM has changed</span></span>

</dd> <dt>

<span data-ttu-id="0a734-123"><span id="vmVirtualMachineEvent_EnhancedVideoModeChanged"></span><span id="vmvirtualmachineevent_enhancedvideomodechanged"></span><span id="VMVIRTUALMACHINEEVENT_ENHANCEDVIDEOMODECHANGED"></span>**vmVirtualMachineEvent \_ EnhancedVideoModeChanged**</span><span class="sxs-lookup"><span data-stu-id="0a734-123"><span id="vmVirtualMachineEvent_EnhancedVideoModeChanged"></span><span id="vmvirtualmachineevent_enhancedvideomodechanged"></span><span id="VMVIRTUALMACHINEEVENT_ENHANCEDVIDEOMODECHANGED"></span>**vmVirtualMachineEvent\_EnhancedVideoModeChanged**</span></span>
</dt> <dd>

<span data-ttu-id="0a734-124">O modo de vídeo de uma VM foi alterado.</span><span class="sxs-lookup"><span data-stu-id="0a734-124">A VM's video mode has changed.</span></span>

</dd> <dt>

<span data-ttu-id="0a734-125"><span id="vmVirtualMachineEvent_AdditionsUninstalled"></span><span id="vmvirtualmachineevent_additionsuninstalled"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSUNINSTALLED"></span>**vmVirtualMachineEvent \_ AdditionsUninstalled**</span><span class="sxs-lookup"><span data-stu-id="0a734-125"><span id="vmVirtualMachineEvent_AdditionsUninstalled"></span><span id="vmvirtualmachineevent_additionsuninstalled"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSUNINSTALLED"></span>**vmVirtualMachineEvent\_AdditionsUninstalled**</span></span>
</dt> <dd>

<span data-ttu-id="0a734-126">Os componentes de integração foram desinstalados da VM.</span><span class="sxs-lookup"><span data-stu-id="0a734-126">Integration components have been uninstalled from the VM.</span></span>

</dd> <dt>

<span data-ttu-id="0a734-127"><span id="vmVirtualMachineEvent_AdditionsAvailable"></span><span id="vmvirtualmachineevent_additionsavailable"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSAVAILABLE"></span>**vmVirtualMachineEvent \_ AdditionsAvailable**</span><span class="sxs-lookup"><span data-stu-id="0a734-127"><span id="vmVirtualMachineEvent_AdditionsAvailable"></span><span id="vmvirtualmachineevent_additionsavailable"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSAVAILABLE"></span>**vmVirtualMachineEvent\_AdditionsAvailable**</span></span>
</dt> <dd>

<span data-ttu-id="0a734-128">A integração está disponível no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="0a734-128">Integration are available in the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="0a734-129"><span id="vmVirtualMachineEvent_GuestShutdown"></span><span id="vmvirtualmachineevent_guestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_GUESTSHUTDOWN"></span>**vmVirtualMachineEvent \_ GuestShutdown**</span><span class="sxs-lookup"><span data-stu-id="0a734-129"><span id="vmVirtualMachineEvent_GuestShutdown"></span><span id="vmvirtualmachineevent_guestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_GUESTSHUTDOWN"></span>**vmVirtualMachineEvent\_GuestShutdown**</span></span>
</dt> <dd>

<span data-ttu-id="0a734-130">Um sistema operacional convidado está sendo desligado.</span><span class="sxs-lookup"><span data-stu-id="0a734-130">A guest operating system is shutting down.</span></span>

</dd> <dt>

<span data-ttu-id="0a734-131"><span id="vmVirtualMachineEvent_GuestLogoff"></span><span id="vmvirtualmachineevent_guestlogoff"></span><span id="VMVIRTUALMACHINEEVENT_GUESTLOGOFF"></span>**vmVirtualMachineEvent \_ GuestLogoff**</span><span class="sxs-lookup"><span data-stu-id="0a734-131"><span id="vmVirtualMachineEvent_GuestLogoff"></span><span id="vmvirtualmachineevent_guestlogoff"></span><span id="VMVIRTUALMACHINEEVENT_GUESTLOGOFF"></span>**vmVirtualMachineEvent\_GuestLogoff**</span></span>
</dt> <dd>

<span data-ttu-id="0a734-132">Um usuário fez logoff do sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="0a734-132">A user logged off from the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="0a734-133"><span id="vmVirtualMachineEvent_DiskOutOfSpace"></span><span id="vmvirtualmachineevent_diskoutofspace"></span><span id="VMVIRTUALMACHINEEVENT_DISKOUTOFSPACE"></span>**vmVirtualMachineEvent \_ DiskOutOfSpace**</span><span class="sxs-lookup"><span data-stu-id="0a734-133"><span id="vmVirtualMachineEvent_DiskOutOfSpace"></span><span id="vmvirtualmachineevent_diskoutofspace"></span><span id="VMVIRTUALMACHINEEVENT_DISKOUTOFSPACE"></span>**vmVirtualMachineEvent\_DiskOutOfSpace**</span></span>
</dt> <dd>

<span data-ttu-id="0a734-134">Um disco exigido pela VM está com pouco espaço.</span><span class="sxs-lookup"><span data-stu-id="0a734-134">A disk required by the VM is low on space.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0a734-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a734-135">Requirements</span></span>



| <span data-ttu-id="0a734-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a734-136">Requirement</span></span> | <span data-ttu-id="0a734-137">Valor</span><span class="sxs-lookup"><span data-stu-id="0a734-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a734-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a734-138">Minimum supported client</span></span><br/> | <span data-ttu-id="0a734-139">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0a734-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0a734-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a734-140">Minimum supported server</span></span><br/> | <span data-ttu-id="0a734-141">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0a734-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0a734-142">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="0a734-142">End of client support</span></span><br/>    | <span data-ttu-id="0a734-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0a734-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0a734-144">Produto</span><span class="sxs-lookup"><span data-stu-id="0a734-144">Product</span></span><br/>                  | <span data-ttu-id="0a734-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0a734-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0a734-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0a734-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a734-147"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a734-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a734-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a734-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a734-149">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="0a734-149">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

