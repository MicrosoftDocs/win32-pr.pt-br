---
description: Marca as operações de e/s síncronas pendentes emitidas pelo thread especificado como canceladas.
ms.assetid: f362c8b2-2193-443e-bb69-78f8b4147117
title: Função CancelSynchronousIo (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelSynchronousIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 3e0c1596603ef7c0d13362c2608cc59b88d366fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506178"
---
# <a name="cancelsynchronousio-function"></a><span data-ttu-id="4152f-103">Função CancelSynchronousIo</span><span class="sxs-lookup"><span data-stu-id="4152f-103">CancelSynchronousIo function</span></span>

<span data-ttu-id="4152f-104">Marca as operações de e/s síncronas pendentes emitidas pelo thread especificado como canceladas.</span><span class="sxs-lookup"><span data-stu-id="4152f-104">Marks pending synchronous I/O operations that are issued by the specified thread as canceled.</span></span>

## <a name="syntax"></a><span data-ttu-id="4152f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4152f-105">Syntax</span></span>


```C++
BOOL WINAPI CancelSynchronousIo(
  _In_ HANDLE hThread
);
```



## <a name="parameters"></a><span data-ttu-id="4152f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4152f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4152f-107">*hThread* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4152f-107">*hThread* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4152f-108">Um identificador para o thread.</span><span class="sxs-lookup"><span data-stu-id="4152f-108">A handle to the thread.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4152f-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4152f-109">Return value</span></span>

<span data-ttu-id="4152f-110">Se a função for bem-sucedida, o valor retornado será diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="4152f-110">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="4152f-111">Se a função falhar, o valor de retorno será 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="4152f-111">If the function fails, the return value is 0 (zero).</span></span> <span data-ttu-id="4152f-112">Para obter informações de erro estendidas, chame a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="4152f-112">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="4152f-113">Se essa função não puder localizar uma solicitação para cancelar, o valor de retorno será 0 (zero) e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o **erro \_ não \_ encontrado**.</span><span class="sxs-lookup"><span data-stu-id="4152f-113">If this function cannot find a request to cancel, the return value is 0 (zero), and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_NOT\_FOUND**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4152f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4152f-114">Remarks</span></span>

<span data-ttu-id="4152f-115">O chamador deve ter o direito de acesso de [ \_ término de thread](/windows/desktop/ProcThread/thread-security-and-access-rights) .</span><span class="sxs-lookup"><span data-stu-id="4152f-115">The caller must have the [THREAD\_TERMINATE](/windows/desktop/ProcThread/thread-security-and-access-rights) access right.</span></span>

<span data-ttu-id="4152f-116">Se houver alguma operação de e/s pendente em andamento para o thread especificado, a função **CancelSynchronousIo** as marcará para cancelamento.</span><span class="sxs-lookup"><span data-stu-id="4152f-116">If there are any pending I/O operations in progress for the specified thread, the **CancelSynchronousIo** function marks them for cancellation.</span></span> <span data-ttu-id="4152f-117">A maioria dos tipos de operações pode ser cancelada imediatamente; outras operações podem continuar na conclusão antes de serem realmente canceladas e o chamador é notificado.</span><span class="sxs-lookup"><span data-stu-id="4152f-117">Most types of operations can be canceled immediately; other operations can continue toward completion before they are actually canceled and the caller is notified.</span></span> <span data-ttu-id="4152f-118">A função **CancelSynchronousIo** não aguarda a conclusão de todas as operações canceladas.</span><span class="sxs-lookup"><span data-stu-id="4152f-118">The **CancelSynchronousIo** function does not wait for all canceled operations to complete.</span></span> <span data-ttu-id="4152f-119">Para obter mais informações, consulte [diretrizes de conclusão/cancelamento de e/s](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).</span><span class="sxs-lookup"><span data-stu-id="4152f-119">For more information, see [I/O Completion/Cancellation Guidelines](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).</span></span>

<span data-ttu-id="4152f-120">A operação que está sendo cancelada é concluída com um dos três status; Você deve verificar o status de conclusão para determinar o estado de conclusão.</span><span class="sxs-lookup"><span data-stu-id="4152f-120">The operation being canceled is completed with one of three statuses; you must check the completion status to determine the completion state.</span></span> <span data-ttu-id="4152f-121">Os três status são:</span><span class="sxs-lookup"><span data-stu-id="4152f-121">The three statuses are:</span></span>

-   <span data-ttu-id="4152f-122">**A operação foi concluída normalmente.**</span><span class="sxs-lookup"><span data-stu-id="4152f-122">**The operation completed normally.**</span></span> <span data-ttu-id="4152f-123">Isso pode ocorrer mesmo que a operação tenha sido cancelada, porque a solicitação de cancelamento pode não ter sido enviada a tempo para cancelar a operação.</span><span class="sxs-lookup"><span data-stu-id="4152f-123">This can occur even if the operation was canceled, because the cancel request might not have been submitted in time to cancel the operation.</span></span>
-   <span data-ttu-id="4152f-124">**A operação foi cancelada.**</span><span class="sxs-lookup"><span data-stu-id="4152f-124">**The operation was canceled.**</span></span> <span data-ttu-id="4152f-125">A função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna a **operação de erro \_ \_ anulada**.</span><span class="sxs-lookup"><span data-stu-id="4152f-125">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_OPERATION\_ABORTED**.</span></span>
-   <span data-ttu-id="4152f-126">**A operação falhou com outro erro.**</span><span class="sxs-lookup"><span data-stu-id="4152f-126">**The operation failed with another error.**</span></span> <span data-ttu-id="4152f-127">A função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna o código de erro relevante.</span><span class="sxs-lookup"><span data-stu-id="4152f-127">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns the relevant error code.</span></span>

<span data-ttu-id="4152f-128">No Windows 8 e no Windows Server 2012, essa função é suportada pelas seguintes tecnologias.</span><span class="sxs-lookup"><span data-stu-id="4152f-128">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="4152f-129">Tecnologia</span><span class="sxs-lookup"><span data-stu-id="4152f-129">Technology</span></span>                                           | <span data-ttu-id="4152f-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4152f-130">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="4152f-131">Protocolo SMB (Server Message Block) 3,0</span><span class="sxs-lookup"><span data-stu-id="4152f-131">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="4152f-132">Yes</span><span class="sxs-lookup"><span data-stu-id="4152f-132">Yes</span></span><br/> |
| <span data-ttu-id="4152f-133">Failover transparente SMB 3,0 (TFO)</span><span class="sxs-lookup"><span data-stu-id="4152f-133">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="4152f-134">Yes</span><span class="sxs-lookup"><span data-stu-id="4152f-134">Yes</span></span><br/> |
| <span data-ttu-id="4152f-135">SMB 3,0 com compartilhamentos de arquivos de escalabilidade horizontal (SO)</span><span class="sxs-lookup"><span data-stu-id="4152f-135">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="4152f-136">Yes</span><span class="sxs-lookup"><span data-stu-id="4152f-136">Yes</span></span><br/> |
| <span data-ttu-id="4152f-137">Sistema de arquivos Volume Compartilhado Clusterizado (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="4152f-137">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="4152f-138">Yes</span><span class="sxs-lookup"><span data-stu-id="4152f-138">Yes</span></span><br/> |
| <span data-ttu-id="4152f-139">ReFS (Sistema de Arquivos Resiliente)</span><span class="sxs-lookup"><span data-stu-id="4152f-139">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="4152f-140">Yes</span><span class="sxs-lookup"><span data-stu-id="4152f-140">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4152f-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4152f-141">Requirements</span></span>



| <span data-ttu-id="4152f-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="4152f-142">Requirement</span></span> | <span data-ttu-id="4152f-143">Valor</span><span class="sxs-lookup"><span data-stu-id="4152f-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4152f-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4152f-144">Minimum supported client</span></span><br/> | <span data-ttu-id="4152f-145">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4152f-145">Windows Vista \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                          |
| <span data-ttu-id="4152f-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4152f-146">Minimum supported server</span></span><br/> | <span data-ttu-id="4152f-147">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4152f-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                    |
| <span data-ttu-id="4152f-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4152f-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="4152f-149"><dt>IoAPI. h (incluir Windows. h); </dt> <dt>Winbase. h no Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4152f-149"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4152f-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4152f-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="4152f-151"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4152f-151"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="4152f-152">DLL</span><span class="sxs-lookup"><span data-stu-id="4152f-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4152f-153"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4152f-153"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a><span data-ttu-id="4152f-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="4152f-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4152f-155">**CancelIo**</span><span class="sxs-lookup"><span data-stu-id="4152f-155">**CancelIo**</span></span>](cancelio.md)
</dt> <dt>

[<span data-ttu-id="4152f-156">**CancelIoEx**</span><span class="sxs-lookup"><span data-stu-id="4152f-156">**CancelIoEx**</span></span>](cancelioex-func.md)
</dt> <dt>

[<span data-ttu-id="4152f-157">Funções de gerenciamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="4152f-157">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="4152f-158">E/s síncrona e síncrona</span><span class="sxs-lookup"><span data-stu-id="4152f-158">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

