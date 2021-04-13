---
title: Enumeração VMTaskResult (VPCCOMInterfaces. h)
description: Especifica o resultado de uma tarefa.
ms.assetid: 34aa193a-466d-492e-8648-467c286a8c11
keywords:
- VMTaskResult de enumeração Virtual PC
topic_type:
- apiref
api_name:
- VMTaskResult
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 903425ca8036e1862df7042f16946fc0f2e9cc7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499751"
---
# <a name="vmtaskresult-enumeration"></a><span data-ttu-id="d7b84-104">Enumeração VMTaskResult</span><span class="sxs-lookup"><span data-stu-id="d7b84-104">VMTaskResult enumeration</span></span>

<span data-ttu-id="d7b84-105">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d7b84-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d7b84-106">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d7b84-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d7b84-107">Especifica o resultado de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="d7b84-107">Specifies the result of a task.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7b84-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7b84-108">Syntax</span></span>


```C++
typedef enum  { 
  vmTaskResult_Success                      = 0,
  vmTaskResult_Cancelled                    = 1,
  vmTaskResult_UnexpectedError              = 2,
  vmTaskResult_OutOfMemoryError             = 3,
  vmTaskResult_DiskRelatedError             = 4,
  vmTaskResult_IncompatibleSavedStateError  = 5,
  vmTaskResult_TimeOutError                 = 6,
  vmTaskResult_IllegalValueError            = 7,
  vmTaskResult_ThreadCrashError             = 8,
  vmTaskResult_ShutdownAbort                = 9
} VMTaskResult;
```



## <a name="constants"></a><span data-ttu-id="d7b84-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="d7b84-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d7b84-110"><span id="vmTaskResult_Success"></span><span id="vmtaskresult_success"></span><span id="VMTASKRESULT_SUCCESS"></span>**vmTaskResult \_ êxito**</span><span class="sxs-lookup"><span data-stu-id="d7b84-110"><span id="vmTaskResult_Success"></span><span id="vmtaskresult_success"></span><span id="VMTASKRESULT_SUCCESS"></span>**vmTaskResult\_Success**</span></span>
</dt> <dd>

<span data-ttu-id="d7b84-111">A tarefa foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d7b84-111">The task was successful.</span></span>

</dd> <dt>

<span data-ttu-id="d7b84-112"><span id="vmTaskResult_Cancelled"></span><span id="vmtaskresult_cancelled"></span><span id="VMTASKRESULT_CANCELLED"></span>**vmTaskResult \_ cancelado**</span><span class="sxs-lookup"><span data-stu-id="d7b84-112"><span id="vmTaskResult_Cancelled"></span><span id="vmtaskresult_cancelled"></span><span id="VMTASKRESULT_CANCELLED"></span>**vmTaskResult\_Cancelled**</span></span>
</dt> <dd>

<span data-ttu-id="d7b84-113">A tarefa foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="d7b84-113">The task was canceled.</span></span>

</dd> <dt>

<span data-ttu-id="d7b84-114"><span id="vmTaskResult_UnexpectedError"></span><span id="vmtaskresult_unexpectederror"></span><span id="VMTASKRESULT_UNEXPECTEDERROR"></span>**vmTaskResult \_ UnexpectedError**</span><span class="sxs-lookup"><span data-stu-id="d7b84-114"><span id="vmTaskResult_UnexpectedError"></span><span id="vmtaskresult_unexpectederror"></span><span id="VMTASKRESULT_UNEXPECTEDERROR"></span>**vmTaskResult\_UnexpectedError**</span></span>
</dt> <dd>

<span data-ttu-id="d7b84-115">A tarefa tinha um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="d7b84-115">The task had an unexpected error.</span></span>

</dd> <dt>

<span data-ttu-id="d7b84-116"><span id="vmTaskResult_OutOfMemoryError"></span><span id="vmtaskresult_outofmemoryerror"></span><span id="VMTASKRESULT_OUTOFMEMORYERROR"></span>**vmTaskResult \_ OutOfMemoryError**</span><span class="sxs-lookup"><span data-stu-id="d7b84-116"><span id="vmTaskResult_OutOfMemoryError"></span><span id="vmtaskresult_outofmemoryerror"></span><span id="VMTASKRESULT_OUTOFMEMORYERROR"></span>**vmTaskResult\_OutOfMemoryError**</span></span>
</dt> <dd>

<span data-ttu-id="d7b84-117">Não havia memória suficiente para a tarefa ser concluída.</span><span class="sxs-lookup"><span data-stu-id="d7b84-117">There was not enough memory for the task to complete.</span></span>

</dd> <dt>

<span data-ttu-id="d7b84-118"><span id="vmTaskResult_DiskRelatedError"></span><span id="vmtaskresult_diskrelatederror"></span><span id="VMTASKRESULT_DISKRELATEDERROR"></span>**vmTaskResult \_ DiskRelatedError**</span><span class="sxs-lookup"><span data-stu-id="d7b84-118"><span id="vmTaskResult_DiskRelatedError"></span><span id="vmtaskresult_diskrelatederror"></span><span id="VMTASKRESULT_DISKRELATEDERROR"></span>**vmTaskResult\_DiskRelatedError**</span></span>
</dt> <dd>

<span data-ttu-id="d7b84-119">A tarefa teve um erro ao gravar no disco (verifique se há espaço em disco suficiente).</span><span class="sxs-lookup"><span data-stu-id="d7b84-119">The task had an error while writing to disk (make sure there is enough disk space).</span></span>

</dd> <dt>

<span data-ttu-id="d7b84-120"><span id="vmTaskResult_IncompatibleSavedStateError"></span><span id="vmtaskresult_incompatiblesavedstateerror"></span><span id="VMTASKRESULT_INCOMPATIBLESAVEDSTATEERROR"></span>**vmTaskResult \_ IncompatibleSavedStateError**</span><span class="sxs-lookup"><span data-stu-id="d7b84-120"><span id="vmTaskResult_IncompatibleSavedStateError"></span><span id="vmtaskresult_incompatiblesavedstateerror"></span><span id="VMTASKRESULT_INCOMPATIBLESAVEDSTATEERROR"></span>**vmTaskResult\_IncompatibleSavedStateError**</span></span>
</dt> <dd>

<span data-ttu-id="d7b84-121">A máquina virtual não pôde ser restaurada porque o estado salvo era incompatível.</span><span class="sxs-lookup"><span data-stu-id="d7b84-121">The virtual machine could not restore because the saved state was incompatible.</span></span>

</dd> <dt>

<span data-ttu-id="d7b84-122"><span id="vmTaskResult_TimeOutError"></span><span id="vmtaskresult_timeouterror"></span><span id="VMTASKRESULT_TIMEOUTERROR"></span>**vmTaskResult \_ TimeOutError**</span><span class="sxs-lookup"><span data-stu-id="d7b84-122"><span id="vmTaskResult_TimeOutError"></span><span id="vmtaskresult_timeouterror"></span><span id="VMTASKRESULT_TIMEOUTERROR"></span>**vmTaskResult\_TimeOutError**</span></span>
</dt> <dd>

<span data-ttu-id="d7b84-123">O tempo limite da tarefa foi atingido.</span><span class="sxs-lookup"><span data-stu-id="d7b84-123">The task timed out.</span></span>

</dd> <dt>

<span data-ttu-id="d7b84-124"><span id="vmTaskResult_IllegalValueError"></span><span id="vmtaskresult_illegalvalueerror"></span><span id="VMTASKRESULT_ILLEGALVALUEERROR"></span>**vmTaskResult \_ IllegalValueError**</span><span class="sxs-lookup"><span data-stu-id="d7b84-124"><span id="vmTaskResult_IllegalValueError"></span><span id="vmtaskresult_illegalvalueerror"></span><span id="VMTASKRESULT_ILLEGALVALUEERROR"></span>**vmTaskResult\_IllegalValueError**</span></span>
</dt> <dd>

<span data-ttu-id="d7b84-125">Um valor de preferência inválido foi lido enquanto a tarefa estava sendo processada.</span><span class="sxs-lookup"><span data-stu-id="d7b84-125">An illegal preference value was read while the task was processing.</span></span>

</dd> <dt>

<span data-ttu-id="d7b84-126"><span id="vmTaskResult_ThreadCrashError"></span><span id="vmtaskresult_threadcrasherror"></span><span id="VMTASKRESULT_THREADCRASHERROR"></span>**vmTaskResult \_ ThreadCrashError**</span><span class="sxs-lookup"><span data-stu-id="d7b84-126"><span id="vmTaskResult_ThreadCrashError"></span><span id="vmtaskresult_threadcrasherror"></span><span id="VMTASKRESULT_THREADCRASHERROR"></span>**vmTaskResult\_ThreadCrashError**</span></span>
</dt> <dd>

<span data-ttu-id="d7b84-127">Um thread associado à tarefa falhou.</span><span class="sxs-lookup"><span data-stu-id="d7b84-127">A thread associated with the task crashed.</span></span>

</dd> <dt>

<span data-ttu-id="d7b84-128"><span id="vmTaskResult_ShutdownAbort"></span><span id="vmtaskresult_shutdownabort"></span><span id="VMTASKRESULT_SHUTDOWNABORT"></span>**vmTaskResult \_ ShutdownAbort**</span><span class="sxs-lookup"><span data-stu-id="d7b84-128"><span id="vmTaskResult_ShutdownAbort"></span><span id="vmtaskresult_shutdownabort"></span><span id="VMTASKRESULT_SHUTDOWNABORT"></span>**vmTaskResult\_ShutdownAbort**</span></span>
</dt> <dd>

<span data-ttu-id="d7b84-129">O desligamento solicitado foi anulado.</span><span class="sxs-lookup"><span data-stu-id="d7b84-129">The shutdown requested was aborted.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d7b84-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7b84-130">Requirements</span></span>



| <span data-ttu-id="d7b84-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7b84-131">Requirement</span></span> | <span data-ttu-id="d7b84-132">Valor</span><span class="sxs-lookup"><span data-stu-id="d7b84-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7b84-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7b84-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d7b84-134">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d7b84-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d7b84-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7b84-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d7b84-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d7b84-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d7b84-137">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="d7b84-137">End of client support</span></span><br/>    | <span data-ttu-id="d7b84-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d7b84-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d7b84-139">Produto</span><span class="sxs-lookup"><span data-stu-id="d7b84-139">Product</span></span><br/>                  | <span data-ttu-id="d7b84-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d7b84-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d7b84-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7b84-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7b84-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7b84-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7b84-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7b84-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7b84-144">**IVMTask:: resultado**</span><span class="sxs-lookup"><span data-stu-id="d7b84-144">**IVMTask::Result**</span></span>](ivmtask-result.md)
</dt> </dl>

 

