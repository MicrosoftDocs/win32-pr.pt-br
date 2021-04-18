---
description: Cancela todas as operações de entrada e saída (e/s) pendentes emitidas pelo thread de chamada para o arquivo especificado.
ms.assetid: b28162dc-0da8-41c6-9901-29381d2d72c4
title: Função CancelIo (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: adb1ab95b30b31670a6ff5a4cc0e0205943f7683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753301"
---
# <a name="cancelio-function"></a><span data-ttu-id="79a3e-103">Função CancelIo</span><span class="sxs-lookup"><span data-stu-id="79a3e-103">CancelIo function</span></span>

<span data-ttu-id="79a3e-104">Cancela todas as operações de entrada e saída (e/s) pendentes emitidas pelo thread de chamada para o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="79a3e-104">Cancels all pending input and output (I/O) operations that are issued by the calling thread for the specified file.</span></span> <span data-ttu-id="79a3e-105">A função não cancela as operações de e/s que outros threads emitem para um identificador de arquivo.</span><span class="sxs-lookup"><span data-stu-id="79a3e-105">The function does not cancel I/O operations that other threads issue for a file handle.</span></span>

<span data-ttu-id="79a3e-106">Para cancelar as operações de e/s de outro thread, use a função [**CancelIoEx**](cancelioex-func.md) .</span><span class="sxs-lookup"><span data-stu-id="79a3e-106">To cancel I/O operations from another thread, use the [**CancelIoEx**](cancelioex-func.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="79a3e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79a3e-107">Syntax</span></span>


```C++
BOOL WINAPI CancelIo(
  _In_ HANDLE hFile
);
```



## <a name="parameters"></a><span data-ttu-id="79a3e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79a3e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79a3e-109">*hFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="79a3e-109">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79a3e-110">Um identificador para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="79a3e-110">A handle to the file.</span></span>

<span data-ttu-id="79a3e-111">A função cancela todas as operações de e/s pendentes para este identificador de arquivo.</span><span class="sxs-lookup"><span data-stu-id="79a3e-111">The function cancels all pending I/O operations for this file handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79a3e-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="79a3e-112">Return value</span></span>

<span data-ttu-id="79a3e-113">Se a função for bem-sucedida, o valor retornado será diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="79a3e-113">If the function succeeds, the return value is nonzero.</span></span> <span data-ttu-id="79a3e-114">A operação de cancelamento para todas as operações de e/s pendentes emitidas pelo thread de chamada para o identificador de arquivo especificado foi solicitada com êxito.</span><span class="sxs-lookup"><span data-stu-id="79a3e-114">The cancel operation for all pending I/O operations issued by the calling thread for the specified file handle was successfully requested.</span></span> <span data-ttu-id="79a3e-115">O thread pode usar a função [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) para determinar quando as operações de e/s propriamente ditas foram concluídas.</span><span class="sxs-lookup"><span data-stu-id="79a3e-115">The thread can use the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function to determine when the I/O operations themselves have been completed.</span></span>

<span data-ttu-id="79a3e-116">Se a função falhar, o valor de retorno será zero (0).</span><span class="sxs-lookup"><span data-stu-id="79a3e-116">If the function fails, the return value is zero (0).</span></span> <span data-ttu-id="79a3e-117">Para obter informações de erro estendidas, chame a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="79a3e-117">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="79a3e-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="79a3e-118">Remarks</span></span>

<span data-ttu-id="79a3e-119">Se houver alguma operação de e/s pendente em andamento para o identificador de arquivo especificado e elas forem emitidas pelo thread de chamada, a função **CancelIo** as cancelará.</span><span class="sxs-lookup"><span data-stu-id="79a3e-119">If there are any pending I/O operations in progress for the specified file handle, and they are issued by the calling thread, the **CancelIo** function cancels them.</span></span> <span data-ttu-id="79a3e-120">**CancelIo** cancela apenas e/s pendentes no identificador, ele não altera o estado do identificador; Isso significa que você não pode contar com o estado do identificador porque não é possível saber se a operação foi concluída com êxito ou cancelada.</span><span class="sxs-lookup"><span data-stu-id="79a3e-120">**CancelIo** cancels only outstanding I/O on the handle, it does not change the state of the handle; this means that you cannot rely on the state of the handle because you cannot know whether the operation was completed successfully or canceled.</span></span>

<span data-ttu-id="79a3e-121">As operações de e/s devem ser emitidas como e/s sobreposta.</span><span class="sxs-lookup"><span data-stu-id="79a3e-121">The I/O operations must be issued as overlapped I/O.</span></span> <span data-ttu-id="79a3e-122">Se não forem, as operações de e/s não retornarão para permitir que o thread chame a função **CancelIo** .</span><span class="sxs-lookup"><span data-stu-id="79a3e-122">If they are not, the I/O operations do not return to allow the thread to call the **CancelIo** function.</span></span> <span data-ttu-id="79a3e-123">Chamar a função **CancelIo** com um identificador de arquivo que não está aberto com o **sinalizador de arquivo \_ \_ sobreposto** não faz nada.</span><span class="sxs-lookup"><span data-stu-id="79a3e-123">Calling the **CancelIo** function with a file handle that is not opened with **FILE\_FLAG\_OVERLAPPED** does nothing.</span></span>

<span data-ttu-id="79a3e-124">Todas as operações de e/s que foram canceladas com a operação de erro de erro foram **\_ \_ anuladas** e todas as notificações de conclusão para as operações de e/s ocorrem normalmente.</span><span class="sxs-lookup"><span data-stu-id="79a3e-124">All I/O operations that are canceled complete with the error **ERROR\_OPERATION\_ABORTED**, and all completion notifications for the I/O operations occur normally.</span></span>

<span data-ttu-id="79a3e-125">No Windows 8 e no Windows Server 2012, essa função é suportada pelas seguintes tecnologias.</span><span class="sxs-lookup"><span data-stu-id="79a3e-125">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="79a3e-126">Tecnologia</span><span class="sxs-lookup"><span data-stu-id="79a3e-126">Technology</span></span>                                           | <span data-ttu-id="79a3e-127">Com suporte</span><span class="sxs-lookup"><span data-stu-id="79a3e-127">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="79a3e-128">Protocolo SMB (Server Message Block) 3,0</span><span class="sxs-lookup"><span data-stu-id="79a3e-128">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="79a3e-129">Yes</span><span class="sxs-lookup"><span data-stu-id="79a3e-129">Yes</span></span><br/> |
| <span data-ttu-id="79a3e-130">Failover transparente SMB 3,0 (TFO)</span><span class="sxs-lookup"><span data-stu-id="79a3e-130">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="79a3e-131">Yes</span><span class="sxs-lookup"><span data-stu-id="79a3e-131">Yes</span></span><br/> |
| <span data-ttu-id="79a3e-132">SMB 3,0 com compartilhamentos de arquivos de escalabilidade horizontal (SO)</span><span class="sxs-lookup"><span data-stu-id="79a3e-132">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="79a3e-133">Yes</span><span class="sxs-lookup"><span data-stu-id="79a3e-133">Yes</span></span><br/> |
| <span data-ttu-id="79a3e-134">Sistema de arquivos Volume Compartilhado Clusterizado (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="79a3e-134">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="79a3e-135">Yes</span><span class="sxs-lookup"><span data-stu-id="79a3e-135">Yes</span></span><br/> |
| <span data-ttu-id="79a3e-136">ReFS (Sistema de Arquivos Resiliente)</span><span class="sxs-lookup"><span data-stu-id="79a3e-136">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="79a3e-137">Yes</span><span class="sxs-lookup"><span data-stu-id="79a3e-137">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="79a3e-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79a3e-138">Requirements</span></span>



| <span data-ttu-id="79a3e-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="79a3e-139">Requirement</span></span> | <span data-ttu-id="79a3e-140">Valor</span><span class="sxs-lookup"><span data-stu-id="79a3e-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79a3e-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79a3e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="79a3e-142">Aplicativos de \[ aplicativos \| UWP do Windows XP desktop\]</span><span class="sxs-lookup"><span data-stu-id="79a3e-142">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="79a3e-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79a3e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="79a3e-144">Aplicativos do Windows Server 2003 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="79a3e-144">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="79a3e-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="79a3e-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="79a3e-146"><dt>IoAPI. h (incluir Windows. h); </dt> <dt>Winbase. h no Windows server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="79a3e-146"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="79a3e-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="79a3e-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="79a3e-148"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="79a3e-148"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                  |
| <span data-ttu-id="79a3e-149">DLL</span><span class="sxs-lookup"><span data-stu-id="79a3e-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79a3e-150"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79a3e-150"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a><span data-ttu-id="79a3e-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="79a3e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79a3e-152">**CancelIoEx**</span><span class="sxs-lookup"><span data-stu-id="79a3e-152">**CancelIoEx**</span></span>](cancelioex-func.md)
</dt> <dt>

[<span data-ttu-id="79a3e-153">**CancelSynchronousIo**</span><span class="sxs-lookup"><span data-stu-id="79a3e-153">**CancelSynchronousIo**</span></span>](cancelsynchronousio-func.md)
</dt> <dt>

[<span data-ttu-id="79a3e-154">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="79a3e-154">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="79a3e-155">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="79a3e-155">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="79a3e-156">Funções de gerenciamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="79a3e-156">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="79a3e-157">**LockFileEx**</span><span class="sxs-lookup"><span data-stu-id="79a3e-157">**LockFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[<span data-ttu-id="79a3e-158">**ReadDirectoryChangesW**</span><span class="sxs-lookup"><span data-stu-id="79a3e-158">**ReadDirectoryChangesW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)
</dt> <dt>

[<span data-ttu-id="79a3e-159">**ReadFile**</span><span class="sxs-lookup"><span data-stu-id="79a3e-159">**ReadFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[<span data-ttu-id="79a3e-160">**ReadFileEx**</span><span class="sxs-lookup"><span data-stu-id="79a3e-160">**ReadFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[<span data-ttu-id="79a3e-161">E/s síncrona e síncrona</span><span class="sxs-lookup"><span data-stu-id="79a3e-161">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> <dt>

[<span data-ttu-id="79a3e-162">**WriteFile**</span><span class="sxs-lookup"><span data-stu-id="79a3e-162">**WriteFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> <dt>

[<span data-ttu-id="79a3e-163">**WriteFileEx**</span><span class="sxs-lookup"><span data-stu-id="79a3e-163">**WriteFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

