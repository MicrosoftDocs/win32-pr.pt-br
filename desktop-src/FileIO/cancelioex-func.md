---
description: Marca todas as operações de e/s pendentes para o identificador de arquivo especificado. A função cancela apenas as operações de e/s no processo atual, independentemente de qual thread criou a operação de e/s.
ms.assetid: a2ce13b8-7da6-4848-848d-901d9667c2e3
title: Função CancelIoEx (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIoEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 3de44762ad9a230a9d8cc410c4ba3ae7c2d9964e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810922"
---
# <a name="cancelioex-function"></a><span data-ttu-id="03d9b-104">Função CancelIoEx</span><span class="sxs-lookup"><span data-stu-id="03d9b-104">CancelIoEx function</span></span>

<span data-ttu-id="03d9b-105">Marca todas as operações de e/s pendentes para o identificador de arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="03d9b-105">Marks any outstanding I/O operations for the specified file handle.</span></span> <span data-ttu-id="03d9b-106">A função cancela apenas as operações de e/s no processo atual, independentemente de qual thread criou a operação de e/s.</span><span class="sxs-lookup"><span data-stu-id="03d9b-106">The function only cancels I/O operations in the current process, regardless of which thread created the I/O operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="03d9b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03d9b-107">Syntax</span></span>


```C++
BOOL WINAPI CancelIoEx(
  _In_     HANDLE       hFile,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a><span data-ttu-id="03d9b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="03d9b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03d9b-109">*hFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="03d9b-109">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03d9b-110">Um identificador para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="03d9b-110">A handle to the file.</span></span>

</dd> <dt>

<span data-ttu-id="03d9b-111">*lpOverlapped* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="03d9b-111">*lpOverlapped* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="03d9b-112">Um ponteiro para uma estrutura de dados [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) que contém os dados usados para e/s assíncrona.</span><span class="sxs-lookup"><span data-stu-id="03d9b-112">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) data structure that contains the data used for asynchronous I/O.</span></span>

<span data-ttu-id="03d9b-113">Se esse parâmetro for **nulo**, todas as solicitações de e/s para o parâmetro *hFile* serão canceladas.</span><span class="sxs-lookup"><span data-stu-id="03d9b-113">If this parameter is **NULL**, all I/O requests for the *hFile* parameter are canceled.</span></span>

<span data-ttu-id="03d9b-114">Se esse parâmetro não for **nulo**, somente as solicitações de e/s específicas emitidas para o arquivo com a estrutura sobreposta *lpOverlapped* especificada serão marcadas como canceladas, o que significa que você pode cancelar uma ou mais solicitações, enquanto a função [**CancelIo**](cancelio.md) cancela todas as solicitações pendentes em um identificador de arquivo.</span><span class="sxs-lookup"><span data-stu-id="03d9b-114">If this parameter is not **NULL**, only those specific I/O requests that were issued for the file with the specified *lpOverlapped* overlapped structure are marked as canceled, meaning that you can cancel one or more requests, while the [**CancelIo**](cancelio.md) function cancels all outstanding requests on a file handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03d9b-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="03d9b-115">Return value</span></span>

<span data-ttu-id="03d9b-116">Se a função for bem-sucedida, o valor retornado será diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="03d9b-116">If the function succeeds, the return value is nonzero.</span></span> <span data-ttu-id="03d9b-117">A operação de cancelamento para todas as operações de e/s pendentes emitidas pelo processo de chamada para o identificador de arquivo especificado foi solicitada com êxito.</span><span class="sxs-lookup"><span data-stu-id="03d9b-117">The cancel operation for all pending I/O operations issued by the calling process for the specified file handle was successfully requested.</span></span> <span data-ttu-id="03d9b-118">O aplicativo não deve liberar ou reutilizar a estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) associada às operações de e/s canceladas até que elas sejam concluídas.</span><span class="sxs-lookup"><span data-stu-id="03d9b-118">The application must not free or reuse the [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure associated with the canceled I/O operations until they have completed.</span></span> <span data-ttu-id="03d9b-119">O thread pode usar a função [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) para determinar quando as operações de e/s propriamente ditas foram concluídas.</span><span class="sxs-lookup"><span data-stu-id="03d9b-119">The thread can use the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function to determine when the I/O operations themselves have been completed.</span></span>

<span data-ttu-id="03d9b-120">Se a função falhar, o valor de retorno será 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="03d9b-120">If the function fails, the return value is 0 (zero).</span></span> <span data-ttu-id="03d9b-121">Para obter informações de erro estendidas, chame a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="03d9b-121">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="03d9b-122">Se essa função não puder localizar uma solicitação para cancelar, o valor de retorno será 0 (zero) e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o **erro \_ não \_ encontrado**.</span><span class="sxs-lookup"><span data-stu-id="03d9b-122">If this function cannot find a request to cancel, the return value is 0 (zero), and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_NOT\_FOUND**.</span></span>

## <a name="remarks"></a><span data-ttu-id="03d9b-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="03d9b-123">Remarks</span></span>

<span data-ttu-id="03d9b-124">A função **CancelIoEx** permite que você cancele solicitações em threads diferentes do thread de chamada.</span><span class="sxs-lookup"><span data-stu-id="03d9b-124">The **CancelIoEx** function allows you to cancel requests in threads other than the calling thread.</span></span> <span data-ttu-id="03d9b-125">A função [**CancelIo**](cancelio.md) cancela apenas as solicitações no mesmo thread que chamou a função **CancelIo** .</span><span class="sxs-lookup"><span data-stu-id="03d9b-125">The [**CancelIo**](cancelio.md) function only cancels requests in the same thread that called the **CancelIo** function.</span></span> <span data-ttu-id="03d9b-126">**CancelIoEx** cancela apenas e/s pendentes no identificador, ele não altera o estado do identificador; Isso significa que você não pode contar com o estado do identificador porque não é possível saber se a operação foi concluída com êxito ou cancelada.</span><span class="sxs-lookup"><span data-stu-id="03d9b-126">**CancelIoEx** cancels only outstanding I/O on the handle, it does not change the state of the handle; this means that you cannot rely on the state of the handle because you cannot know whether the operation was completed successfully or canceled.</span></span>

<span data-ttu-id="03d9b-127">Se houver alguma operação de e/s pendente em andamento para o identificador de arquivo especificado, a função **CancelIoEx** as marcará para cancelamento.</span><span class="sxs-lookup"><span data-stu-id="03d9b-127">If there are any pending I/O operations in progress for the specified file handle, the **CancelIoEx** function marks them for cancellation.</span></span> <span data-ttu-id="03d9b-128">A maioria dos tipos de operações pode ser cancelada imediatamente; outras operações podem continuar na conclusão antes de serem realmente canceladas e o chamador é notificado.</span><span class="sxs-lookup"><span data-stu-id="03d9b-128">Most types of operations can be canceled immediately; other operations can continue toward completion before they are actually canceled and the caller is notified.</span></span> <span data-ttu-id="03d9b-129">A função **CancelIoEx** não aguarda a conclusão de todas as operações canceladas.</span><span class="sxs-lookup"><span data-stu-id="03d9b-129">The **CancelIoEx** function does not wait for all canceled operations to complete.</span></span>

<span data-ttu-id="03d9b-130">Se o identificador de arquivo estiver associado a uma porta de conclusão, um pacote de conclusão de e/s não será enfileirado para a porta se uma operação síncrona for cancelada com êxito.</span><span class="sxs-lookup"><span data-stu-id="03d9b-130">If the file handle is associated with a completion port, an I/O completion packet is not queued to the port if a synchronous operation is successfully canceled.</span></span> <span data-ttu-id="03d9b-131">Para operações assíncronas ainda pendentes, a operação de cancelamento colocará em fila um pacote de conclusão de e/s.</span><span class="sxs-lookup"><span data-stu-id="03d9b-131">For asynchronous operations still pending, the cancel operation will queue an I/O completion packet.</span></span>

<span data-ttu-id="03d9b-132">A operação que está sendo cancelada é concluída com um dos três status; Você deve verificar o status de conclusão para determinar o estado de conclusão.</span><span class="sxs-lookup"><span data-stu-id="03d9b-132">The operation being canceled is completed with one of three statuses; you must check the completion status to determine the completion state.</span></span> <span data-ttu-id="03d9b-133">Os três status são:</span><span class="sxs-lookup"><span data-stu-id="03d9b-133">The three statuses are:</span></span>

-   <span data-ttu-id="03d9b-134">A operação foi concluída normalmente.</span><span class="sxs-lookup"><span data-stu-id="03d9b-134">The operation completed normally.</span></span> <span data-ttu-id="03d9b-135">Isso pode ocorrer mesmo que a operação tenha sido cancelada, porque a solicitação de cancelamento pode não ter sido enviada a tempo para cancelar a operação.</span><span class="sxs-lookup"><span data-stu-id="03d9b-135">This can occur even if the operation was canceled, because the cancel request might not have been submitted in time to cancel the operation.</span></span>
-   <span data-ttu-id="03d9b-136">A operação foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="03d9b-136">The operation was canceled.</span></span> <span data-ttu-id="03d9b-137">A função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna a **operação de erro \_ \_ anulada**.</span><span class="sxs-lookup"><span data-stu-id="03d9b-137">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_OPERATION\_ABORTED**.</span></span>
-   <span data-ttu-id="03d9b-138">A operação falhou com outro erro.</span><span class="sxs-lookup"><span data-stu-id="03d9b-138">The operation failed with another error.</span></span> <span data-ttu-id="03d9b-139">A função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna o código de erro relevante.</span><span class="sxs-lookup"><span data-stu-id="03d9b-139">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns the relevant error code.</span></span>

<span data-ttu-id="03d9b-140">No Windows 8 e no Windows Server 2012, essa função é suportada pelas seguintes tecnologias.</span><span class="sxs-lookup"><span data-stu-id="03d9b-140">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="03d9b-141">Tecnologia</span><span class="sxs-lookup"><span data-stu-id="03d9b-141">Technology</span></span>                                           | <span data-ttu-id="03d9b-142">Com suporte</span><span class="sxs-lookup"><span data-stu-id="03d9b-142">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="03d9b-143">Protocolo SMB (Server Message Block) 3,0</span><span class="sxs-lookup"><span data-stu-id="03d9b-143">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="03d9b-144">Yes</span><span class="sxs-lookup"><span data-stu-id="03d9b-144">Yes</span></span><br/> |
| <span data-ttu-id="03d9b-145">Failover transparente SMB 3,0 (TFO)</span><span class="sxs-lookup"><span data-stu-id="03d9b-145">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="03d9b-146">Yes</span><span class="sxs-lookup"><span data-stu-id="03d9b-146">Yes</span></span><br/> |
| <span data-ttu-id="03d9b-147">SMB 3,0 com compartilhamentos de arquivos de escalabilidade horizontal (SO)</span><span class="sxs-lookup"><span data-stu-id="03d9b-147">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="03d9b-148">Yes</span><span class="sxs-lookup"><span data-stu-id="03d9b-148">Yes</span></span><br/> |
| <span data-ttu-id="03d9b-149">Sistema de arquivos Volume Compartilhado Clusterizado (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="03d9b-149">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="03d9b-150">Yes</span><span class="sxs-lookup"><span data-stu-id="03d9b-150">Yes</span></span><br/> |
| <span data-ttu-id="03d9b-151">ReFS (Sistema de Arquivos Resiliente)</span><span class="sxs-lookup"><span data-stu-id="03d9b-151">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="03d9b-152">Yes</span><span class="sxs-lookup"><span data-stu-id="03d9b-152">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="03d9b-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03d9b-153">Requirements</span></span>



| <span data-ttu-id="03d9b-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="03d9b-154">Requirement</span></span> | <span data-ttu-id="03d9b-155">Valor</span><span class="sxs-lookup"><span data-stu-id="03d9b-155">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03d9b-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03d9b-156">Minimum supported client</span></span><br/> | <span data-ttu-id="03d9b-157">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="03d9b-157">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="03d9b-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03d9b-158">Minimum supported server</span></span><br/> | <span data-ttu-id="03d9b-159">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="03d9b-159">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                             |
| <span data-ttu-id="03d9b-160">parâmetro</span><span class="sxs-lookup"><span data-stu-id="03d9b-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="03d9b-161"><dt>IoAPI. h (incluir Windows. h); </dt> <dt>Winbase. h no Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03d9b-161"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="03d9b-162">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="03d9b-162">Library</span></span><br/>                  | <dl> <span data-ttu-id="03d9b-163"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="03d9b-163"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="03d9b-164">DLL</span><span class="sxs-lookup"><span data-stu-id="03d9b-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03d9b-165"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03d9b-165"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a><span data-ttu-id="03d9b-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="03d9b-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03d9b-167">**CancelIo**</span><span class="sxs-lookup"><span data-stu-id="03d9b-167">**CancelIo**</span></span>](cancelio.md)
</dt> <dt>

[<span data-ttu-id="03d9b-168">**CancelSynchronousIo**</span><span class="sxs-lookup"><span data-stu-id="03d9b-168">**CancelSynchronousIo**</span></span>](cancelsynchronousio-func.md)
</dt> <dt>

[<span data-ttu-id="03d9b-169">Cancelando operações de e/s pendentes</span><span class="sxs-lookup"><span data-stu-id="03d9b-169">Canceling Pending I/O Operations</span></span>](canceling-pending-i-o-operations.md)
</dt> <dt>

[<span data-ttu-id="03d9b-170">Funções de gerenciamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="03d9b-170">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="03d9b-171">E/s síncrona e síncrona</span><span class="sxs-lookup"><span data-stu-id="03d9b-171">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

