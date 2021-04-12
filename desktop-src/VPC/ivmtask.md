---
title: Interface IVMTask (VPCCOMInterfaces. h)
description: Use a interface IVMTask para monitorar e controlar tarefas assíncronas para vários métodos COM.
ms.assetid: 9b593444-80f5-43e9-9b95-1a2150c66efd
keywords:
- Virtual PC de interface IVMTask
- Virtual PC de interface IVMTask, descrito
topic_type:
- apiref
api_name:
- IVMTask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e1d519471fe5b1fc32cb6365d1139243c85538
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499576"
---
# <a name="ivmtask-interface"></a><span data-ttu-id="4648a-105">Interface IVMTask</span><span class="sxs-lookup"><span data-stu-id="4648a-105">IVMTask interface</span></span>

<span data-ttu-id="4648a-106">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4648a-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4648a-107">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4648a-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4648a-108">Use a interface **IVMTask** para monitorar e controlar tarefas assíncronas para vários métodos com.</span><span class="sxs-lookup"><span data-stu-id="4648a-108">Use the **IVMTask** interface to monitor and control asynchronous tasks for various COM methods.</span></span>

## <a name="members"></a><span data-ttu-id="4648a-109">Membros</span><span class="sxs-lookup"><span data-stu-id="4648a-109">Members</span></span>

<span data-ttu-id="4648a-110">A interface **IVMTask** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="4648a-110">The **IVMTask** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="4648a-111">**IVMTask** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4648a-111">**IVMTask** also has these types of members:</span></span>

-   [<span data-ttu-id="4648a-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="4648a-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="4648a-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4648a-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4648a-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="4648a-114">Methods</span></span>

<span data-ttu-id="4648a-115">A interface **IVMTask** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="4648a-115">The **IVMTask** interface has these methods.</span></span>



| <span data-ttu-id="4648a-116">Método</span><span class="sxs-lookup"><span data-stu-id="4648a-116">Method</span></span>                                                 | <span data-ttu-id="4648a-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="4648a-117">Description</span></span>                                                                                 |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4648a-118">**Cancelar**</span><span class="sxs-lookup"><span data-stu-id="4648a-118">**Cancel**</span></span>](ivmtask-cancel.md)                       | <span data-ttu-id="4648a-119">Cancela a tarefa.</span><span class="sxs-lookup"><span data-stu-id="4648a-119">Cancels the task.</span></span><br/>                                                                |
| [<span data-ttu-id="4648a-120">**WaitForCompletion**</span><span class="sxs-lookup"><span data-stu-id="4648a-120">**WaitForCompletion**</span></span>](ivmtask-waitforcompletion.md) | <span data-ttu-id="4648a-121">Aguarda a conclusão da tarefa ou o intervalo de tempo limite especificado para decorrer.</span><span class="sxs-lookup"><span data-stu-id="4648a-121">Waits for the task to complete or for the specified time-out interval to elapse.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4648a-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4648a-122">Properties</span></span>

<span data-ttu-id="4648a-123">A interface **IVMTask** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4648a-123">The **IVMTask** interface has these properties.</span></span>



| <span data-ttu-id="4648a-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4648a-124">Property</span></span>                                                        | <span data-ttu-id="4648a-125">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="4648a-125">Access type</span></span>          | <span data-ttu-id="4648a-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="4648a-126">Description</span></span>                                                        |
|:----------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="4648a-127">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4648a-127">**Description**</span></span>](ivmtask-description.md)<br/>           | <span data-ttu-id="4648a-128">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4648a-128">Read-only</span></span><br/> | <span data-ttu-id="4648a-129">Uma descrição da tarefa.</span><span class="sxs-lookup"><span data-stu-id="4648a-129">A description of the task.</span></span><br/>                              |
| [<span data-ttu-id="4648a-130">**Erro**</span><span class="sxs-lookup"><span data-stu-id="4648a-130">**Error**</span></span>](ivmtask-error.md)<br/>                       | <span data-ttu-id="4648a-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4648a-131">Read-only</span></span><br/> | <span data-ttu-id="4648a-132">O erro registrado para esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="4648a-132">The error recorded for this task.</span></span><br/>                       |
| [<span data-ttu-id="4648a-133">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="4648a-133">**ErrorDescription**</span></span>](ivmtask-errordescription.md)<br/> | <span data-ttu-id="4648a-134">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4648a-134">Read-only</span></span><br/> | <span data-ttu-id="4648a-135">A descrição de erro localizada registrada para esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="4648a-135">The localized error description recorded for this task.</span></span><br/> |
| [<span data-ttu-id="4648a-136">**ID**</span><span class="sxs-lookup"><span data-stu-id="4648a-136">**ID**</span></span>](ivmtask-id.md)<br/>                             | <span data-ttu-id="4648a-137">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4648a-137">Read-only</span></span><br/> | <span data-ttu-id="4648a-138">Um identificador exclusivo para esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="4648a-138">A unique identifier for this task.</span></span><br/>                      |
| [<span data-ttu-id="4648a-139">**Iscancelável**</span><span class="sxs-lookup"><span data-stu-id="4648a-139">**IsCancelable**</span></span>](ivmtask-iscancelable.md)<br/>         | <span data-ttu-id="4648a-140">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4648a-140">Read-only</span></span><br/> | <span data-ttu-id="4648a-141">Indica se a tarefa pode ser cancelada.</span><span class="sxs-lookup"><span data-stu-id="4648a-141">Indicates whether the task can be canceled.</span></span><br/>             |
| [<span data-ttu-id="4648a-142">**IsComplete**</span><span class="sxs-lookup"><span data-stu-id="4648a-142">**IsComplete**</span></span>](ivmtask-iscomplete.md)<br/>             | <span data-ttu-id="4648a-143">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4648a-143">Read-only</span></span><br/> | <span data-ttu-id="4648a-144">Indica se a tarefa foi concluída.</span><span class="sxs-lookup"><span data-stu-id="4648a-144">Indicates whether the task has completed.</span></span><br/>               |
| [<span data-ttu-id="4648a-145">**PercentCompleted**</span><span class="sxs-lookup"><span data-stu-id="4648a-145">**PercentCompleted**</span></span>](ivmtask-percentcompleted.md)<br/> | <span data-ttu-id="4648a-146">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4648a-146">Read-only</span></span><br/> | <span data-ttu-id="4648a-147">A porcentagem de conclusão da tarefa.</span><span class="sxs-lookup"><span data-stu-id="4648a-147">The completion percentage of the task.</span></span><br/>                  |
| [<span data-ttu-id="4648a-148">**Resultado**</span><span class="sxs-lookup"><span data-stu-id="4648a-148">**Result**</span></span>](ivmtask-result.md)<br/>                     | <span data-ttu-id="4648a-149">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4648a-149">Read-only</span></span><br/> | <span data-ttu-id="4648a-150">O resultado da tarefa.</span><span class="sxs-lookup"><span data-stu-id="4648a-150">The result of the task.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="4648a-151">Comentários</span><span class="sxs-lookup"><span data-stu-id="4648a-151">Remarks</span></span>

<span data-ttu-id="4648a-152">Um objeto **IVMTask** é retornado por métodos que potencialmente podem exigir uma quantidade significativa de tempo para serem concluídos.</span><span class="sxs-lookup"><span data-stu-id="4648a-152">An **IVMTask** object is returned by methods that could potentially require a significant amount of time to complete.</span></span> <span data-ttu-id="4648a-153">Isso permite que o aplicativo monitore o progresso da operação desejada sem forçá-la a bloquear a execução adicional enquanto aguarda a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="4648a-153">This allows the application to monitor the progress of the desired operation without forcing it to block further execution while waiting for the completion of the operation.</span></span>

<span data-ttu-id="4648a-154">Os métodos a seguir retornam um objeto **IVMTask** que pode ser usado para acompanhar o progresso:</span><span class="sxs-lookup"><span data-stu-id="4648a-154">The following methods return an **IVMTask** object that can be used to track progress:</span></span>

-   [<span data-ttu-id="4648a-155">**IVMGuestOS:: fazer logoff**</span><span class="sxs-lookup"><span data-stu-id="4648a-155">**IVMGuestOS::Logoff**</span></span>](ivmguestos-logoff.md)
-   [<span data-ttu-id="4648a-156">**IVMGuestOS:: reiniciar**</span><span class="sxs-lookup"><span data-stu-id="4648a-156">**IVMGuestOS::Restart**</span></span>](ivmguestos-restart.md)
-   [<span data-ttu-id="4648a-157">**IVMGuestOS:: Shutdown**</span><span class="sxs-lookup"><span data-stu-id="4648a-157">**IVMGuestOS::Shutdown**</span></span>](ivmguestos-shutdown.md)
-   [<span data-ttu-id="4648a-158">**IVMHardDisk:: compactar**</span><span class="sxs-lookup"><span data-stu-id="4648a-158">**IVMHardDisk::Compact**</span></span>](ivmharddisk-compact.md)
-   [<span data-ttu-id="4648a-159">**IVMHardDisk:: Convert**</span><span class="sxs-lookup"><span data-stu-id="4648a-159">**IVMHardDisk::Convert**</span></span>](ivmharddisk-convert.md)
-   [<span data-ttu-id="4648a-160">**IVMHardDisk:: Merge**</span><span class="sxs-lookup"><span data-stu-id="4648a-160">**IVMHardDisk::Merge**</span></span>](ivmharddisk-merge.md)
-   [<span data-ttu-id="4648a-161">**IVMHardDisk:: Mergeto**</span><span class="sxs-lookup"><span data-stu-id="4648a-161">**IVMHardDisk::MergeTo**</span></span>](ivmharddisk-mergeto.md)
-   [<span data-ttu-id="4648a-162">**IVMVirtualMachine::MergeUndoDisks**</span><span class="sxs-lookup"><span data-stu-id="4648a-162">**IVMVirtualMachine::MergeUndoDisks**</span></span>](ivmvirtualmachine-mergeundodisks.md)
-   [<span data-ttu-id="4648a-163">**IVMVirtualMachine:: Reset**</span><span class="sxs-lookup"><span data-stu-id="4648a-163">**IVMVirtualMachine::Reset**</span></span>](ivmvirtualmachine-reset.md)
-   [<span data-ttu-id="4648a-164">**IVMVirtualMachine:: salvar**</span><span class="sxs-lookup"><span data-stu-id="4648a-164">**IVMVirtualMachine::Save**</span></span>](ivmvirtualmachine-save.md)
-   [<span data-ttu-id="4648a-165">**IVMVirtualMachine:: Startup**</span><span class="sxs-lookup"><span data-stu-id="4648a-165">**IVMVirtualMachine::Startup**</span></span>](ivmvirtualmachine-startup.md)
-   [<span data-ttu-id="4648a-166">**IVMVirtualMachine:: Startup2**</span><span class="sxs-lookup"><span data-stu-id="4648a-166">**IVMVirtualMachine::Startup2**</span></span>](ivmvirtualmachine-startup2.md)
-   [<span data-ttu-id="4648a-167">**IVMVirtualMachine:: desativação**</span><span class="sxs-lookup"><span data-stu-id="4648a-167">**IVMVirtualMachine::TurnOff**</span></span>](ivmvirtualmachine-turnoff.md)
-   [<span data-ttu-id="4648a-168">**IVMVirtualPC::CreateDifferencingVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="4648a-168">**IVMVirtualPC::CreateDifferencingVirtualHardDisk**</span></span>](ivmvirtualpc-createdifferencingvirtualharddisk.md)
-   [<span data-ttu-id="4648a-169">**IVMVirtualPC::CreateDynamicVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="4648a-169">**IVMVirtualPC::CreateDynamicVirtualHardDisk**</span></span>](ivmvirtualpc-createdynamicvirtualharddisk.md)
-   [<span data-ttu-id="4648a-170">**IVMVirtualPC::CreateFixedVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="4648a-170">**IVMVirtualPC::CreateFixedVirtualHardDisk**</span></span>](ivmvirtualpc-createfixedvirtualharddisk.md)

## <a name="requirements"></a><span data-ttu-id="4648a-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4648a-171">Requirements</span></span>



| <span data-ttu-id="4648a-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="4648a-172">Requirement</span></span> | <span data-ttu-id="4648a-173">Valor</span><span class="sxs-lookup"><span data-stu-id="4648a-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4648a-174">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4648a-174">Minimum supported client</span></span><br/> | <span data-ttu-id="4648a-175">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4648a-175">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4648a-176">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4648a-176">Minimum supported server</span></span><br/> | <span data-ttu-id="4648a-177">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4648a-177">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4648a-178">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4648a-178">End of client support</span></span><br/>    | <span data-ttu-id="4648a-179">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4648a-179">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4648a-180">Produto</span><span class="sxs-lookup"><span data-stu-id="4648a-180">Product</span></span><br/>                  | <span data-ttu-id="4648a-181">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4648a-181">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4648a-182">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4648a-182">Header</span></span><br/>                   | <dl> <span data-ttu-id="4648a-183"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4648a-183"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4648a-184">IID</span><span class="sxs-lookup"><span data-stu-id="4648a-184">IID</span></span><br/>                      | <span data-ttu-id="4648a-185">IID \_ IVMTask é definido como ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="4648a-185">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



 

