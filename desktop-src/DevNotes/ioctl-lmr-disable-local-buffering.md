---
description: O LMR do IOCTL \_ \_ desabilitar o \_ \_ código de controle de buffer local desabilita o cache de dados na memória local do lado do cliente ao ler ou gravar dados em um arquivo remoto. Este é um código de controle definido internamente não disponível em um cabeçalho público.
ms.assetid: a464671b-253c-4f35-84a2-2619cb15b009
title: IOCTL_LMR_DISABLE_LOCAL_BUFFERING código de controle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPY_CHUNK
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0d596402c489caee972e1305f2a32881312fd3e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749711"
---
# <a name="ioctl_lmr_disable_local_buffering-control-code"></a><span data-ttu-id="18619-104">IOCTL \_ LMR \_ desabilitar \_ o \_ código de controle de buffer local</span><span class="sxs-lookup"><span data-stu-id="18619-104">IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING control code</span></span>

<span data-ttu-id="18619-105">O LMR do IOCTL desabilitar o código de controle de **\_ \_ \_ \_ buffer local** desabilita o cache de dados na memória local do lado do cliente ao ler ou gravar dados em um arquivo remoto.</span><span class="sxs-lookup"><span data-stu-id="18619-105">The **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code disables local client-side in-memory caching of data when reading data from or writing data to a remote file.</span></span> <span data-ttu-id="18619-106">Este é um código de controle definido internamente não disponível em um cabeçalho público.</span><span class="sxs-lookup"><span data-stu-id="18619-106">This is an internally-defined control code not available in a public header.</span></span>

<span data-ttu-id="18619-107">Para executar essa operação, chame a função [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="18619-107">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_LMR_DISABLE_LOCAL_BUFFERING, // dwIoControlCode
  (LPVOID) NULL,                // lpInBuffer
  (DWORD) 0,                    // nInBufferSize
  (LPVOID) NULL,                // lpOutBuffer
  (DWORD) 0,                    // nOutBufferSize
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="18619-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18619-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18619-109">*hDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="18619-109">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18619-110">Um identificador para o arquivo remoto.</span><span class="sxs-lookup"><span data-stu-id="18619-110">A handle to the remote file.</span></span> <span data-ttu-id="18619-111">Para obter esse identificador, chame a função [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="18619-111">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="18619-112">*dwIoControlCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="18619-112">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18619-113">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="18619-113">The control code for the operation.</span></span> <span data-ttu-id="18619-114">Use o valor 0x140390 para esta operação.</span><span class="sxs-lookup"><span data-stu-id="18619-114">Use the value 0x140390 for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="18619-115">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="18619-115">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="18619-116">Não usado, deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="18619-116">Not used, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="18619-117">*nInBufferSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="18619-117">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18619-118">O tamanho do buffer de entrada, em bytes.</span><span class="sxs-lookup"><span data-stu-id="18619-118">The size of the input buffer, in bytes.</span></span> <span data-ttu-id="18619-119">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="18619-119">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="18619-120">*lpOutBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="18619-120">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18619-121">Não usado, deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="18619-121">Not used, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="18619-122">*nOutBufferSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="18619-122">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18619-123">O tamanho do buffer de saída em bytes.</span><span class="sxs-lookup"><span data-stu-id="18619-123">The size of the output buffer, in bytes.</span></span> <span data-ttu-id="18619-124">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="18619-124">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="18619-125">*lpBytesReturned* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="18619-125">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18619-126">Um ponteiro para uma variável que recebe o tamanho dos dados armazenados no buffer de saída, em bytes.</span><span class="sxs-lookup"><span data-stu-id="18619-126">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="18619-127">Se o buffer de saída for muito pequeno, a chamada falhará, a função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará um **\_ \_ buffer insuficiente de erro** e *lpBytesReturned* será zero.</span><span class="sxs-lookup"><span data-stu-id="18619-127">If the output buffer is too small, then the call fails, the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="18619-128">Se o parâmetro *lpOverlapped* for **NULL**, *lpBytesReturned* não poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="18619-128">If the *lpOverlapped* parameter is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="18619-129">Mesmo quando uma operação não retorna dados de saída e o parâmetro *lpOutBuffer* é **nulo**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) faz uso de *lpBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="18619-129">Even when an operation returns no output data and the *lpOutBuffer* parameter is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="18619-130">Após tal operação, o valor de *lpBytesReturned* é inútil.</span><span class="sxs-lookup"><span data-stu-id="18619-130">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="18619-131">Se *lpOverlapped* não for **nulo**, *lpBytesReturned* poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="18619-131">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="18619-132">Se *lpOverlapped* não for **nulo** e a operação retornar dados, *lpBytesReturned* será inútil até que a operação sobreposta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="18619-132">If *lpOverlapped* is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="18619-133">Para recuperar o número de bytes retornados, chame a função [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="18619-133">To retrieve the number of bytes returned, call the [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="18619-134">Se o parâmetro *hDevice* estiver associado a uma porta de conclusão de e/s, você poderá recuperar o número de bytes retornados chamando a função [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="18619-134">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="18619-135">*lpOverlapped* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="18619-135">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18619-136">Um ponteiro para uma estrutura [**sobreposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="18619-136">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="18619-137">Se o parâmetro *hDevice* tiver sido aberto sem especificar o **sinalizador de arquivo \_ \_ sobreposto**, *lpOverlapped* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="18619-137">If the *hDevice* parameter was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="18619-138">Se *hDevice* tiver sido aberto com o sinalizador de **sinalizador de arquivo \_ \_ sobreposto** , a operação será executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="18619-138">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="18619-139">Nesse caso, *lpOverlapped* deve apontar para uma estrutura [**sobreposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) válida que contém um identificador para um objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="18619-139">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="18619-140">Caso contrário, a função falhará de maneiras imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="18619-140">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="18619-141">Para operações sobrepostas, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retorna imediatamente e o objeto de evento é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="18619-141">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="18619-142">Caso contrário, a função não retorna até que a operação seja concluída ou até que ocorra um erro.</span><span class="sxs-lookup"><span data-stu-id="18619-142">Otherwise, the function does not return until the operation has been completed or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18619-143">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="18619-143">Return value</span></span>

<span data-ttu-id="18619-144">Se a operação for concluída com êxito, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="18619-144">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="18619-145">Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero.</span><span class="sxs-lookup"><span data-stu-id="18619-145">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="18619-146">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="18619-146">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="18619-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="18619-147">Remarks</span></span>

<span data-ttu-id="18619-148">O código de controle de **\_ \_ \_ \_ buffer local de LMR de IOCTL desabilitado** é definido internamente pelo sistema como 0x140390 e não em um arquivo de cabeçalho público.</span><span class="sxs-lookup"><span data-stu-id="18619-148">The **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code is defined internally by the system as 0x140390 and not in a public header file.</span></span> <span data-ttu-id="18619-149">Ele é usado por aplicativos de finalidade especial para desabilitar o cache de dados na memória local do lado do cliente ao ler ou gravar dados em um arquivo remoto.</span><span class="sxs-lookup"><span data-stu-id="18619-149">It is used by special-purpose applications to disable local client-side in-memory caching of data when reading data from or writing data to a remote file.</span></span> <span data-ttu-id="18619-150">Depois que o buffer local é desabilitado, a configuração permanece em vigor até que todos os identificadores abertos para o arquivo sejam fechados e o redirecionador Limpe suas estruturas de dados internas.</span><span class="sxs-lookup"><span data-stu-id="18619-150">After local buffering is disabled, the setting remains in effect until all open handles to the file are closed and the redirector cleans up its internal data structures.</span></span>

<span data-ttu-id="18619-151">Os aplicativos de uso geral não devem usar o **IOCTL \_ LMR \_ desabilitar o \_ \_ buffer local**, pois isso pode resultar em excesso de tráfego de rede e perda associada de desempenho.</span><span class="sxs-lookup"><span data-stu-id="18619-151">General-purpose applications should not use **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING**, because it can result in excessive network traffic and associated loss of performance.</span></span> <span data-ttu-id="18619-152">O LMR de dados do IOCTL desabilitar o código de controle de **\_ \_ \_ \_ buffer local** deve ser usado somente em aplicativos especializados que movem grandes quantidades de dados pela rede ao tentar maximizar o uso da largura de banda da rede.</span><span class="sxs-lookup"><span data-stu-id="18619-152">The **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code should be used only in specialized applications moving large amounts of data over the network while attempting to maximize use of network bandwidth.</span></span> <span data-ttu-id="18619-153">Por exemplo, as funções [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile) e [**CopyFileEx**](/windows/win32/api/winbase/nf-winbase-copyfileexa) usam o **IOCTL \_ LMR \_ desabilitar o \_ \_ buffer local** para melhorar o desempenho de cópia de arquivo grande.</span><span class="sxs-lookup"><span data-stu-id="18619-153">For example, the [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile) and [**CopyFileEx**](/windows/win32/api/winbase/nf-winbase-copyfileexa) functions use **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** to improve large file copy performance.</span></span>

<span data-ttu-id="18619-154">**IOCTL \_ LMR \_ desabilitar \_ o \_ buffer local** não é implementado por sistemas de arquivos locais e falhará com a **função erro de erro \_ inválida \_**.</span><span class="sxs-lookup"><span data-stu-id="18619-154">**IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** is not implemented by local file systems and will fail with the error **ERROR\_INVALID\_FUNCTION**.</span></span> <span data-ttu-id="18619-155">A emissão do código de controle de **\_ \_ \_ \_ buffer local LMR de IOCTL de desativação** em identificadores de diretório remoto falhará, com o erro de erro **\_ não \_ suportado**.</span><span class="sxs-lookup"><span data-stu-id="18619-155">Issuing the **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code on remote directory handles will fail with the error **ERROR\_NOT\_SUPPORTED**.</span></span>

## <a name="see-also"></a><span data-ttu-id="18619-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="18619-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18619-157">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="18619-157">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
