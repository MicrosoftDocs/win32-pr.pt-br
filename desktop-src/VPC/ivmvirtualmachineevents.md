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
ms.openlocfilehash: 8fddcc2ded96f5a39a520d3b5a712e63fbb0a65d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455797"
---
# <a name="ivmvirtualmachineevents-interface"></a><span data-ttu-id="506e0-105">Interface IVMVirtualMachineEvents</span><span class="sxs-lookup"><span data-stu-id="506e0-105">IVMVirtualMachineEvents interface</span></span>

<span data-ttu-id="506e0-106">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="506e0-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="506e0-107">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="506e0-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="506e0-108">Define a interface de evento de saída para a interface [**IVMVirtualMachine**](ivmvirtualmachine.md) .</span><span class="sxs-lookup"><span data-stu-id="506e0-108">Defines the outgoing event interface for the [**IVMVirtualMachine**](ivmvirtualmachine.md) interface.</span></span> <span data-ttu-id="506e0-109">O cliente implementa esses métodos para receber eventos enviados do [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="506e0-109">The client implements these methods to receive events sent from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="members"></a><span data-ttu-id="506e0-110">Membros</span><span class="sxs-lookup"><span data-stu-id="506e0-110">Members</span></span>

<span data-ttu-id="506e0-111">A interface **IVMVirtualMachineEvents** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="506e0-111">The **IVMVirtualMachineEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="506e0-112">**IVMVirtualMachineEvents** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="506e0-112">**IVMVirtualMachineEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="506e0-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="506e0-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="506e0-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="506e0-114">Methods</span></span>

<span data-ttu-id="506e0-115">A interface **IVMVirtualMachineEvents** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="506e0-115">The **IVMVirtualMachineEvents** interface has these methods.</span></span>



| <span data-ttu-id="506e0-116">Método</span><span class="sxs-lookup"><span data-stu-id="506e0-116">Method</span></span>                                                                                   | <span data-ttu-id="506e0-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="506e0-117">Description</span></span>                                                                                                                                     |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="506e0-118">**OnAdditionsAvailable**</span><span class="sxs-lookup"><span data-stu-id="506e0-118">**OnAdditionsAvailable**</span></span>](ivmvirtualmachineevents-onadditionsavailable.md)             | <span data-ttu-id="506e0-119">Recebe a notificação de que os componentes de integração estão disponíveis em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="506e0-119">Receives notification that integration components are available in a virtual machine.</span></span><br/>                                                |
| [<span data-ttu-id="506e0-120">**OnAdditionsUninstalled**</span><span class="sxs-lookup"><span data-stu-id="506e0-120">**OnAdditionsUninstalled**</span></span>](ivmvirtualmachineevents-onadditionsuninstalled.md)         | <span data-ttu-id="506e0-121">Recebe a notificação de que os componentes de integração são desinstalados em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="506e0-121">Receives notification that integration components are uninstalled in a virtual machine.</span></span><br/>                                              |
| [<span data-ttu-id="506e0-122">**Onconfigurationchanged**</span><span class="sxs-lookup"><span data-stu-id="506e0-122">**OnConfigurationChanged**</span></span>](ivmvirtualmachineevents-onconfigurationchanged.md)         | <span data-ttu-id="506e0-123">Recebe uma notificação de que um valor na configuração para esta máquina virtual foi alterado.</span><span class="sxs-lookup"><span data-stu-id="506e0-123">Receives notification that a value in the configuration for this virtual machine has changed.</span></span><br/>                                        |
| [<span data-ttu-id="506e0-124">**OnDiskOutOfSpace**</span><span class="sxs-lookup"><span data-stu-id="506e0-124">**OnDiskOutOfSpace**</span></span>](ivmvirtualmachineevents-ondiskoutofspace.md)                     | <span data-ttu-id="506e0-125">Recebe uma notificação de que um disco necessário para uma máquina virtual está sem espaço e a máquina virtual não pode ser executada.</span><span class="sxs-lookup"><span data-stu-id="506e0-125">Receives notification that a disk required for a virtual machine is out of space and the virtual machine is unable to run.</span></span><br/>           |
| [<span data-ttu-id="506e0-126">**OnEnhancedVideoModeChanged**</span><span class="sxs-lookup"><span data-stu-id="506e0-126">**OnEnhancedVideoModeChanged**</span></span>](ivmvirtualmachineevents-onenhancedvideomodechanged.md) | <span data-ttu-id="506e0-127">Recebe a notificação de que o suporte de uma máquina virtual para o modo de vídeo avançado foi alterado.</span><span class="sxs-lookup"><span data-stu-id="506e0-127">Receives notification that a virtual machine's support for enhanced video mode has changed.</span></span><br/>                                          |
| [<span data-ttu-id="506e0-128">**OnGuestLogoff**</span><span class="sxs-lookup"><span data-stu-id="506e0-128">**OnGuestLogoff**</span></span>](ivmvirtualmachineevents-onguestlogoff.md)                           | <span data-ttu-id="506e0-129">Recebe a notificação de que um usuário fez logoff do sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="506e0-129">Receives notification that a user has logged off from the guest operating system.</span></span><br/>                                                    |
| [<span data-ttu-id="506e0-130">**OnGuestShutdown**</span><span class="sxs-lookup"><span data-stu-id="506e0-130">**OnGuestShutdown**</span></span>](ivmvirtualmachineevents-onguestshutdown.md)                       | <span data-ttu-id="506e0-131">Recebe a notificação de que o sistema operacional convidado foi desligado.</span><span class="sxs-lookup"><span data-stu-id="506e0-131">Receives notification that guest operating system has shut down.</span></span><br/>                                                                     |
| [<span data-ttu-id="506e0-132">**OnHeartbeatStopped**</span><span class="sxs-lookup"><span data-stu-id="506e0-132">**OnHeartbeatStopped**</span></span>](ivmvirtualmachineevents-onheartbeatstopped.md)                 | <span data-ttu-id="506e0-133">Recebe a notificação de que a pulsação de uma máquina virtual foi interrompida.</span><span class="sxs-lookup"><span data-stu-id="506e0-133">Receives notification that a virtual machine's heartbeat has stopped.</span></span> <span data-ttu-id="506e0-134">Isso geralmente indica que o sistema operacional convidado falhou.</span><span class="sxs-lookup"><span data-stu-id="506e0-134">This usually indicates the guest operating system has crashed.</span></span><br/> |
| [<span data-ttu-id="506e0-135">**OnRequestShutdown**</span><span class="sxs-lookup"><span data-stu-id="506e0-135">**OnRequestShutdown**</span></span>](ivmvirtualmachineevents-onrequestshutdown.md)                   | <span data-ttu-id="506e0-136">Recebe a notificação de que uma solicitação de desligamento foi feita.</span><span class="sxs-lookup"><span data-stu-id="506e0-136">Receives notification that a shutdown request has been made.</span></span><br/>                                                                         |
| [<span data-ttu-id="506e0-137">**OnReset**</span><span class="sxs-lookup"><span data-stu-id="506e0-137">**OnReset**</span></span>](ivmvirtualmachineevents-onreset.md)                                       | <span data-ttu-id="506e0-138">Recebe a notificação de que uma máquina virtual foi redefinida.</span><span class="sxs-lookup"><span data-stu-id="506e0-138">Receives notification that a virtual machine has been reset.</span></span><br/>                                                                         |
| [<span data-ttu-id="506e0-139">**OnStateChange**</span><span class="sxs-lookup"><span data-stu-id="506e0-139">**OnStateChange**</span></span>](ivmvirtualmachineevents-onstatechange.md)                           | <span data-ttu-id="506e0-140">Recebe a notificação de que o estado de uma máquina virtual foi alterado.</span><span class="sxs-lookup"><span data-stu-id="506e0-140">Receives notification that a virtual machine's state has changed.</span></span><br/>                                                                    |
| [<span data-ttu-id="506e0-141">**OnTripleFault**</span><span class="sxs-lookup"><span data-stu-id="506e0-141">**OnTripleFault**</span></span>](ivmvirtualmachineevents-ontriplefault.md)                           | <span data-ttu-id="506e0-142">Recebe uma notificação de que uma máquina virtual tem falha tripla.</span><span class="sxs-lookup"><span data-stu-id="506e0-142">Receives notification that a virtual machine has triple-faulted.</span></span><br/>                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="506e0-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="506e0-143">Requirements</span></span>



| <span data-ttu-id="506e0-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="506e0-144">Requirement</span></span> | <span data-ttu-id="506e0-145">Valor</span><span class="sxs-lookup"><span data-stu-id="506e0-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="506e0-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="506e0-146">Minimum supported client</span></span><br/> | <span data-ttu-id="506e0-147">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="506e0-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="506e0-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="506e0-148">Minimum supported server</span></span><br/> | <span data-ttu-id="506e0-149">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="506e0-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="506e0-150">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="506e0-150">End of client support</span></span><br/>    | <span data-ttu-id="506e0-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="506e0-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="506e0-152">Produto</span><span class="sxs-lookup"><span data-stu-id="506e0-152">Product</span></span><br/>                  | <span data-ttu-id="506e0-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="506e0-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="506e0-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="506e0-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="506e0-155"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="506e0-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="506e0-156">IID</span><span class="sxs-lookup"><span data-stu-id="506e0-156">IID</span></span><br/>                      | <span data-ttu-id="506e0-157">DIID \_ IVMVirtualMachineEvents é definido como 9d84f560-bb67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="506e0-157">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



 

