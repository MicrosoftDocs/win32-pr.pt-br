---
title: Código de controle FSCTL_DFS_GET_PKT_ENTRY_STATE (LmDfs.h)
description: O código de controle de FSCTL_DFS_GET_PKT_ENTRY_STATE pode obter as mesmas informações que a função NetDfsGetClientInfo, mas pode fornecer melhor desempenho em algumas configurações com latências altas para os servidores DFS.
ms.assetid: d4eec104-128b-43b5-9fae-08ab0b977dec
topic_type:
- apiref
api_name:
- FSCTL_DFS_GET_PKT_ENTRY_STATE
api_location:
- LmDfs.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a57fb448934908ebc1530e95a298715324aaee6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501045"
---
# <a name="fsctl_dfs_get_pkt_entry_state-control-code"></a><span data-ttu-id="8f69d-103">FSCTL_DFS_GET_PKT_ENTRY_STATE código de controle</span><span class="sxs-lookup"><span data-stu-id="8f69d-103">FSCTL_DFS_GET_PKT_ENTRY_STATE control code</span></span>

<span data-ttu-id="8f69d-104">O código de controle de **FSCTL_DFS_GET_PKT_ENTRY_STATE** pode obter as mesmas informações que a função [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) , mas pode fornecer melhor desempenho em algumas configurações com latências altas para os servidores DFS.</span><span class="sxs-lookup"><span data-stu-id="8f69d-104">The **FSCTL_DFS_GET_PKT_ENTRY_STATE** control code can get the same information as the [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) function but can provide better performance in some configurations with high latencies to the DFS servers.</span></span> <span data-ttu-id="8f69d-105">Não é recomendável usar o código de controle de **FSCTL_DFS_GET_PKT_ENTRY_STATE** , a menos que haja problemas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="8f69d-105">It is not recommended to use the **FSCTL_DFS_GET_PKT_ENTRY_STATE** control code unless there are performance issues.</span></span>

<span data-ttu-id="8f69d-106">Para executar essa operação, chame a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="8f69d-106">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>

```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,            // handle to device
                    (DWORD)        FSCTL_DFS_GET_PKT_ENTRY_STATE, // dwIoControlCode(LPDWORD)      lpInBuffer,         // input buffer
                    (DWORD)        nInBufferSize,      // size of input buffer
                    (LPDWORD)      lpOutBuffer,        // output buffer
                    (DWORD)        nOutBufferSize,     // size of output buffer
                    (LPDWORD)      lpBytesReturned,    // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );     // OVERLAPPED structure
```

## <a name="parameters"></a><span data-ttu-id="8f69d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f69d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f69d-108">*hDevice* [in]</span><span class="sxs-lookup"><span data-stu-id="8f69d-108">*hDevice* [in]</span></span>
</dt> <dd>

<span data-ttu-id="8f69d-109">Um identificador para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8f69d-109">A handle to the device.</span></span> <span data-ttu-id="8f69d-110">Para obter um identificador de dispositivo, chame a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="8f69d-110">To obtain a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="8f69d-111">*dwIoControlCode* [in]</span><span class="sxs-lookup"><span data-stu-id="8f69d-111">*dwIoControlCode* [in]</span></span>
</dt> <dd>

<span data-ttu-id="8f69d-112">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="8f69d-112">The control code for the operation.</span></span> <span data-ttu-id="8f69d-113">Use **FSCTL_DFS_GET_PKT_ENTRY_STATE** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="8f69d-113">Use **FSCTL_DFS_GET_PKT_ENTRY_STATE** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="8f69d-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="8f69d-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="8f69d-115">Endereço de uma estrutura de [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) e as cadeias de caracteres Unicode 1-3 a seguir.</span><span class="sxs-lookup"><span data-stu-id="8f69d-115">Address of a [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) structure and the 1-3 Unicode strings that follow.</span></span>

</dd> <dt>

<span data-ttu-id="8f69d-116">*nInBufferSize* [in]</span><span class="sxs-lookup"><span data-stu-id="8f69d-116">*nInBufferSize* [in]</span></span>
</dt> <dd>

<span data-ttu-id="8f69d-117">Tamanho, em bytes, do buffer apontado pelo parâmetro *lpInBuffer* .</span><span class="sxs-lookup"><span data-stu-id="8f69d-117">Size, in bytes, of the buffer pointed to by the *lpInBuffer* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8f69d-118">*lpOutBuffer* [saída]</span><span class="sxs-lookup"><span data-stu-id="8f69d-118">*lpOutBuffer* [out]</span></span>
</dt> <dd>

<span data-ttu-id="8f69d-119">Endereço de uma estrutura de **DFS_INFO_ \#** e quaisquer cadeias de caracteres e estruturas apontadas pela estrutura de **DFS_INFO_ \#** .</span><span class="sxs-lookup"><span data-stu-id="8f69d-119">Address of a **DFS_INFO_\#** structure and any strings and structures pointed to by the **DFS_INFO_\#** structure.</span></span> <span data-ttu-id="8f69d-120">A estrutura específica retornada depende do membro de **nível** na estrutura de [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) passada no buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="8f69d-120">The specific structure returned depends on the **Level** member in the [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) structure passed in the input buffer.</span></span>

</dd> <dt>

<span data-ttu-id="8f69d-121">*nOutBufferSize* [in]</span><span class="sxs-lookup"><span data-stu-id="8f69d-121">*nOutBufferSize* [in]</span></span>
</dt> <dd>

<span data-ttu-id="8f69d-122">Tamanho, em bytes, do buffer apontado pelo parâmetro *lpOutBuffer* .</span><span class="sxs-lookup"><span data-stu-id="8f69d-122">Size, in bytes, of the buffer pointed to by the *lpOutBuffer* parameter.</span></span> <span data-ttu-id="8f69d-123">Devido às cadeias de caracteres e estruturas referenciadas pela estrutura de **DFS_INFO_ \#** retornada que também estão no buffer de saída, esse buffer deve ser maior do que a estrutura de **DFS_INFO_ \#** especificada.</span><span class="sxs-lookup"><span data-stu-id="8f69d-123">Due to the strings and structures referenced by the returned **DFS_INFO_\#** structure that are also in the output buffer, this buffer should be larger than the **DFS_INFO_\#** structure specified.</span></span>

</dd> <dt>

<span data-ttu-id="8f69d-124">*lpBytesReturned* [saída]</span><span class="sxs-lookup"><span data-stu-id="8f69d-124">*lpBytesReturned* [out]</span></span>
</dt> <dd>

<span data-ttu-id="8f69d-125">Um ponteiro para uma variável que recebe o tamanho dos dados armazenados no buffer de saída, em bytes.</span><span class="sxs-lookup"><span data-stu-id="8f69d-125">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="8f69d-126">Se o buffer de saída for muito pequeno, mas pelo menos grande o suficiente para manter um **DWORD**, a chamada falhará, [**getlasterror**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará **ERROR_MORE_DATA** e a primeira **DWORD** do buffer de saída conterá o tamanho necessário.</span><span class="sxs-lookup"><span data-stu-id="8f69d-126">If the output buffer is too small, but at least large enough to hold a **DWORD**, the call fails, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR_MORE_DATA**, and the first **DWORD** of the output buffer contains the size that would have been required.</span></span> <span data-ttu-id="8f69d-127">Se o buffer de saída não puder conter um **DWORD** , a chamada falhará com **ERROR_INSUFFICIENT_BUFFER** e *lpBytesReturned* será zero.</span><span class="sxs-lookup"><span data-stu-id="8f69d-127">If the output buffer cannot hold a **DWORD** then the call fails with **ERROR_INSUFFICIENT_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="8f69d-128">Se *lpOverlapped* for **nulo**, *lpBytesReturned* não poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="8f69d-128">If *lpOverlapped* is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="8f69d-129">Mesmo quando uma operação não retorna dados de saída e *lpOutBuffer* é **nula**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) faz uso de *lpBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="8f69d-129">Even when an operation returns no output data and *lpOutBuffer* is **NULL**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="8f69d-130">Após tal operação, o valor de *lpBytesReturned* é inútil.</span><span class="sxs-lookup"><span data-stu-id="8f69d-130">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="8f69d-131">Se *lpOverlapped* não for **nulo**, *lpBytesReturned* poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="8f69d-131">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="8f69d-132">Se esse parâmetro não for **nulo** e a operação retornar dados, *lpBytesReturned* será inútil até que a operação sobreposta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="8f69d-132">If this parameter is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="8f69d-133">Para recuperar o número de bytes retornados, chame [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult).</span><span class="sxs-lookup"><span data-stu-id="8f69d-133">To retrieve the number of bytes returned, call [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult).</span></span> <span data-ttu-id="8f69d-134">Se o parâmetro *hDevice* estiver associado a uma porta de conclusão de e/s, você poderá recuperar o número de bytes retornados chamando [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span><span class="sxs-lookup"><span data-stu-id="8f69d-134">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span></span>

</dd> <dt>

<span data-ttu-id="8f69d-135">*lpOverlapped* [in]</span><span class="sxs-lookup"><span data-stu-id="8f69d-135">*lpOverlapped* [in]</span></span>
</dt> <dd>

<span data-ttu-id="8f69d-136">Um ponteiro para uma estrutura [**sobreposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="8f69d-136">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="8f69d-137">Se *hDevice* tiver sido aberto sem especificar **FILE_FLAG_OVERLAPPED**, *lpOverlapped* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="8f69d-137">If *hDevice* was opened without specifying **FILE_FLAG_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="8f69d-138">Se *hDevice* tiver sido aberto com o sinalizador **FILE_FLAG_OVERLAPPED** , a operação será executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="8f69d-138">If *hDevice* was opened with the **FILE_FLAG_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="8f69d-139">Nesse caso, *lpOverlapped* deve apontar para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida que contém um identificador para um objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="8f69d-139">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="8f69d-140">Caso contrário, a função falhará de maneiras imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="8f69d-140">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="8f69d-141">Para operações sobrepostas, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retorna imediatamente e o objeto de evento é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="8f69d-141">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="8f69d-142">Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.</span><span class="sxs-lookup"><span data-stu-id="8f69d-142">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f69d-143">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8f69d-143">Return value</span></span>

<span data-ttu-id="8f69d-144">Se a operação for concluída com êxito, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="8f69d-144">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="8f69d-145">Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero.</span><span class="sxs-lookup"><span data-stu-id="8f69d-145">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="8f69d-146">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="8f69d-146">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f69d-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f69d-147">Requirements</span></span>

| <span data-ttu-id="8f69d-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f69d-148">Requirement</span></span> | <span data-ttu-id="8f69d-149">Valor</span><span class="sxs-lookup"><span data-stu-id="8f69d-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f69d-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f69d-150">Minimum supported client</span></span><br/> | <span data-ttu-id="8f69d-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f69d-151">Windows Vista</span></span><br/>                                                                             |
| <span data-ttu-id="8f69d-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f69d-152">Minimum supported server</span></span><br/> | <span data-ttu-id="8f69d-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f69d-153">Windows Server 2008</span></span><br/>                                                                       |
| <span data-ttu-id="8f69d-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8f69d-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f69d-155"><dt>LmDfs. h (incluir LmDfs. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f69d-155"><dt>LmDfs.h (include LmDfs.h)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="8f69d-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f69d-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f69d-157">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="8f69d-157">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="8f69d-158">**NetDfsGetClientInfo**</span><span class="sxs-lookup"><span data-stu-id="8f69d-158">**NetDfsGetClientInfo**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> </dl>
