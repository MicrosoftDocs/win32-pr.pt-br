---
description: O \_ código de controle COPYCHUNK do IOCTL inicia uma cópia do lado do servidor de um intervalo de dados, também chamado de parte.
ms.assetid: 36f68840-bd5c-4cfc-a8ad-0cfbbdc5a2a9
title: IOCTL_COPYCHUNK código de controle
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
ms.openlocfilehash: c425fc53563e6dfc16d2040fb575f47f0f8fdf35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811249"
---
# <a name="ioctl_copychunk-control-code"></a><span data-ttu-id="134eb-103">Código de controle de COPYCHUNK do IOCTL \_</span><span class="sxs-lookup"><span data-stu-id="134eb-103">IOCTL\_COPYCHUNK control code</span></span>

<span data-ttu-id="134eb-104">O código de controle **\_ COPYCHUNK do IOCTL** inicia uma cópia do lado do servidor de um intervalo de dados, também chamado de parte.</span><span class="sxs-lookup"><span data-stu-id="134eb-104">The **IOCTL\_COPYCHUNK** control code initiates a server-side copy of a range of data, also called a chunk.</span></span>

<span data-ttu-id="134eb-105">Para executar essa operação, chame a função [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="134eb-105">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_COPYCHUNK,              // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="134eb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="134eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="134eb-107">*hDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="134eb-107">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="134eb-108">Um identificador para o arquivo que é o destino da operação de cópia do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="134eb-108">A handle to the file that is the target of the server-side copy operation.</span></span> <span data-ttu-id="134eb-109">Para obter esse identificador, chame a função [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="134eb-109">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="134eb-110">*dwIoControlCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="134eb-110">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="134eb-111">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="134eb-111">The control code for the operation.</span></span> <span data-ttu-id="134eb-112">Use **o \_ COPYCHUNK do IOCTL** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="134eb-112">Use **IOCTL\_COPYCHUNK** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="134eb-113">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="134eb-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="134eb-114">Um ponteiro para o buffer de entrada, uma estrutura de **\_ \_ cópia COPYCHUNK SRV** .</span><span class="sxs-lookup"><span data-stu-id="134eb-114">A pointer to the input buffer, a **SRV\_COPYCHUNK\_COPY** structure.</span></span> <span data-ttu-id="134eb-115">Para obter mais informações, consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="134eb-115">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="134eb-116">*nInBufferSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="134eb-116">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="134eb-117">O tamanho do buffer de entrada, em bytes.</span><span class="sxs-lookup"><span data-stu-id="134eb-117">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="134eb-118">*lpOutBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="134eb-118">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="134eb-119">Um ponteiro para o buffer de saída, uma estrutura de **\_ \_ resposta de COPYCHUNK SRV** .</span><span class="sxs-lookup"><span data-stu-id="134eb-119">A pointer to the output buffer, a **SRV\_COPYCHUNK\_RESPONSE** structure.</span></span> <span data-ttu-id="134eb-120">Para obter mais informações, consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="134eb-120">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="134eb-121">*nOutBufferSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="134eb-121">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="134eb-122">O tamanho do buffer de saída em bytes.</span><span class="sxs-lookup"><span data-stu-id="134eb-122">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="134eb-123">*lpBytesReturned* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="134eb-123">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="134eb-124">Um ponteiro para uma variável que recebe o tamanho dos dados armazenados no buffer de saída, em bytes.</span><span class="sxs-lookup"><span data-stu-id="134eb-124">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="134eb-125">Se o buffer de saída for muito pequeno, a chamada falhará, a função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará um **\_ \_ buffer insuficiente de erro** e *lpBytesReturned* será zero.</span><span class="sxs-lookup"><span data-stu-id="134eb-125">If the output buffer is too small, the call fails, the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="134eb-126">Se o parâmetro *lpOverlapped* for **NULL**, *lpBytesReturned* não poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="134eb-126">If the *lpOverlapped* parameter is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="134eb-127">Mesmo quando uma operação não retorna dados de saída e o parâmetro *lpOutBuffer* é **nulo**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) faz uso de *lpBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="134eb-127">Even when an operation returns no output data and the *lpOutBuffer* parameter is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="134eb-128">Após tal operação, o valor de *lpBytesReturned* é inútil.</span><span class="sxs-lookup"><span data-stu-id="134eb-128">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="134eb-129">Se *lpOverlapped* não for **nulo**, *lpBytesReturned* poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="134eb-129">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="134eb-130">Se *lpOverlapped* não for **nulo** e a operação retornar dados, *lpBytesReturned* será inútil até que a operação sobreposta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="134eb-130">If *lpOverlapped* is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="134eb-131">Para recuperar o número de bytes retornados, chame a função [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="134eb-131">To retrieve the number of bytes returned, call the [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="134eb-132">Se o parâmetro *hDevice* estiver associado a uma porta de conclusão de e/s, você poderá recuperar o número de bytes retornados chamando a função [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="134eb-132">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="134eb-133">*lpOverlapped* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="134eb-133">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="134eb-134">Um ponteiro para uma estrutura [**sobreposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="134eb-134">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="134eb-135">Se o parâmetro *hDevice* tiver sido aberto sem especificar o **sinalizador de arquivo \_ \_ sobreposto**, *lpOverlapped* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="134eb-135">If the *hDevice* parameter was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="134eb-136">Se *hDevice* tiver sido aberto com o sinalizador de **sinalizador de arquivo \_ \_ sobreposto** , a operação será executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="134eb-136">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="134eb-137">Nesse caso, *lpOverlapped* deve apontar para uma estrutura [**sobreposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) válida que contém um identificador para um objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="134eb-137">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="134eb-138">Caso contrário, a função falhará de maneiras imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="134eb-138">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="134eb-139">Para operações sobrepostas, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retorna imediatamente e o objeto de evento é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="134eb-139">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="134eb-140">Caso contrário, a função não retorna até que a operação seja concluída ou até que ocorra um erro.</span><span class="sxs-lookup"><span data-stu-id="134eb-140">Otherwise, the function does not return until the operation has been completed or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="134eb-141">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="134eb-141">Return value</span></span>

<span data-ttu-id="134eb-142">Se a operação for concluída com êxito, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="134eb-142">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="134eb-143">Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero.</span><span class="sxs-lookup"><span data-stu-id="134eb-143">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="134eb-144">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="134eb-144">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="134eb-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="134eb-145">Remarks</span></span>

<span data-ttu-id="134eb-146">Este código de controle não tem nenhum arquivo de cabeçalho associado.</span><span class="sxs-lookup"><span data-stu-id="134eb-146">This control code has no associated header file.</span></span> <span data-ttu-id="134eb-147">Você deve definir o código de controle e as estruturas de dados da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="134eb-147">You must define the control code and data structures as follows.</span></span>

``` syntax
#define IOCTL_COPYCHUNK CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 262, METHOD_BUFFERED,  FILE_READ_ACCESS)

typedef struct _SRV_COPYCHUNK {
    LARGE_INTEGER SourceOffset;
    LARGE_INTEGER DestinationOffset;
    ULONG  Length;
} SRV_COPYCHUNK, *PSRV_COPYCHUNK;

typedef struct _SRV_COPYCHUNK_COPY {
    SRV_RESUME_KEY SourceFile;
    ULONG          ChunkCount;
    ULONG          Reserved;
    SRV_COPYCHUNK  Chunk[1];    // Array
} SRV_COPYCHUNK_COPY, *PSRV_COPYCHUNK_COPY;

typedef struct _SRV_COPYCHUNK_RESPONSE {
    ULONG          ChunksWritten;
    ULONG          ChunkBytesWritten;
    ULONG          TotalBytesWritten;
} SRV_COPYCHUNK_RESPONSE, *PSRV_COPYCHUNK_RESPONSE;
```

<span data-ttu-id="134eb-148">Esses membros podem ser descritos da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="134eb-148">These members can be described as follows.</span></span>



| <span data-ttu-id="134eb-149">Membro</span><span class="sxs-lookup"><span data-stu-id="134eb-149">Member</span></span>                                                                                                                                       | <span data-ttu-id="134eb-150">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="134eb-150">Description</span></span>                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="134eb-151"><span id="SourceOffset"></span><span id="sourceoffset"></span><span id="SOURCEOFFSET"></span>**SourceOffset**</span><span class="sxs-lookup"><span data-stu-id="134eb-151"><span id="SourceOffset"></span><span id="sourceoffset"></span><span id="SOURCEOFFSET"></span>**SourceOffset**</span></span><br/>                     | <span data-ttu-id="134eb-152">O deslocamento, em bytes, desde o início do arquivo de origem até a parte a ser copiada.</span><span class="sxs-lookup"><span data-stu-id="134eb-152">The offset, in bytes, from the beginning of the source file to the chunk to be copied.</span></span><br/>                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="134eb-153"><span id="DestinationOffset"></span><span id="destinationoffset"></span><span id="DESTINATIONOFFSET"></span>**DestinationOffset**</span><span class="sxs-lookup"><span data-stu-id="134eb-153"><span id="DestinationOffset"></span><span id="destinationoffset"></span><span id="DESTINATIONOFFSET"></span>**DestinationOffset**</span></span><br/> | <span data-ttu-id="134eb-154">O deslocamento, em bytes, desde o início do arquivo de destino até o local onde a parte deve ser copiada.</span><span class="sxs-lookup"><span data-stu-id="134eb-154">The offset, in bytes, from the beginning of the target file to the location where the chunk is to be copied.</span></span><br/>                                                                                                                                                                                                                                               |
| <span data-ttu-id="134eb-155"><span id="Length"></span><span id="length"></span><span id="LENGTH"></span>**Muito**</span><span class="sxs-lookup"><span data-stu-id="134eb-155"><span id="Length"></span><span id="length"></span><span id="LENGTH"></span>**Length**</span></span><br/>                                             | <span data-ttu-id="134eb-156">O número de bytes de dados na parte a serem copiados.</span><span class="sxs-lookup"><span data-stu-id="134eb-156">The number of bytes of data in the chunk to be copied.</span></span> <span data-ttu-id="134eb-157">Deve ser maior que zero e menor ou igual a 1 MB.</span><span class="sxs-lookup"><span data-stu-id="134eb-157">Must be greater than zero and less than or equal to 1 MB.</span></span> <span data-ttu-id="134eb-158">**Comprimento** \* **ChunkCount** deve ser menor ou igual a 16 MB.</span><span class="sxs-lookup"><span data-stu-id="134eb-158">**Length** \* **ChunkCount** must be less than or equal to 16 MB.</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="134eb-159"><span id="SourceFile"></span><span id="sourcefile"></span><span id="SOURCEFILE"></span>**SourceFile**</span><span class="sxs-lookup"><span data-stu-id="134eb-159"><span id="SourceFile"></span><span id="sourcefile"></span><span id="SOURCEFILE"></span>**SourceFile**</span></span><br/>                             | <span data-ttu-id="134eb-160">Uma chave que representa o arquivo de origem com os dados a serem copiados.</span><span class="sxs-lookup"><span data-stu-id="134eb-160">A key that represents the source file with the data to be copied.</span></span> <span data-ttu-id="134eb-161">Essa chave é obtida por meio da [**\_ \_ \_ \_ chave de retomada de solicitação do fsctl SRV**](fsctl-srv-request-resume-key.md).</span><span class="sxs-lookup"><span data-stu-id="134eb-161">This key is obtained through [**FSCTL\_SRV\_REQUEST\_RESUME\_KEY**](fsctl-srv-request-resume-key.md).</span></span><br/>                                                                                                                                                                                   |
| <span data-ttu-id="134eb-162"><span id="ChunkCount"></span><span id="chunkcount"></span><span id="CHUNKCOUNT"></span>**ChunkCount**</span><span class="sxs-lookup"><span data-stu-id="134eb-162"><span id="ChunkCount"></span><span id="chunkcount"></span><span id="CHUNKCOUNT"></span>**ChunkCount**</span></span><br/>                             | <span data-ttu-id="134eb-163">O número de partes a serem copiadas.</span><span class="sxs-lookup"><span data-stu-id="134eb-163">The number of chunks to be copied.</span></span> <span data-ttu-id="134eb-164">Deve ser maior que zero e menor ou igual a 256.</span><span class="sxs-lookup"><span data-stu-id="134eb-164">Must be greater than zero and less than or equal to 256.</span></span><br/>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="134eb-165"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reservado**</span><span class="sxs-lookup"><span data-stu-id="134eb-165"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved**</span></span><br/>                                     | <span data-ttu-id="134eb-166">Este membro é reservado para uso do sistema; Não use.</span><span class="sxs-lookup"><span data-stu-id="134eb-166">This member is reserved for system use; do not use.</span></span><br/>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="134eb-167"><span id="Chunk"></span><span id="chunk"></span><span id="CHUNK"></span>**Codificação**</span><span class="sxs-lookup"><span data-stu-id="134eb-167"><span id="Chunk"></span><span id="chunk"></span><span id="CHUNK"></span>**Chunk**</span></span><br/>                                                 | <span data-ttu-id="134eb-168">Uma matriz de estruturas **\_ COPYCHUNK** **ChunkCount** SRV, uma para cada parte a ser copiada.</span><span class="sxs-lookup"><span data-stu-id="134eb-168">An array of **ChunkCount** **SRV\_COPYCHUNK** structures, one for each chunk to be copied.</span></span> <span data-ttu-id="134eb-169">O comprimento, em bytes, dessa matriz deve ser **ChunkCount** \* sizeof (**SRV \_ COPYCHUNK**).</span><span class="sxs-lookup"><span data-stu-id="134eb-169">The length, in bytes, of this array must be **ChunkCount** \* sizeof(**SRV\_COPYCHUNK**).</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="134eb-170"><span id="ChunksWritten"></span><span id="chunkswritten"></span><span id="CHUNKSWRITTEN"></span>**ChunksWritten**</span><span class="sxs-lookup"><span data-stu-id="134eb-170"><span id="ChunksWritten"></span><span id="chunkswritten"></span><span id="CHUNKSWRITTEN"></span>**ChunksWritten**</span></span><br/>                 | <span data-ttu-id="134eb-171">Se a operação falhou com **um \_ \_ parâmetro de erro inválido**, esse valor indica o número máximo de partes que o servidor aceitará em uma única solicitação, que é 256.</span><span class="sxs-lookup"><span data-stu-id="134eb-171">If the operation failed with **ERROR\_INVALID\_PARAMETER**, this value indicates the maximum number of chunks the server will accept in a single request, which is 256.</span></span> <span data-ttu-id="134eb-172">Caso contrário, esse valor indica o número de partes que foram gravadas com êxito.</span><span class="sxs-lookup"><span data-stu-id="134eb-172">Otherwise, this value indicates the number of chunks that were successfully written.</span></span><br/>                                                                                               |
| <span data-ttu-id="134eb-173"><span id="ChunkBytesWritten"></span><span id="chunkbyteswritten"></span><span id="CHUNKBYTESWRITTEN"></span>**ChunkBytesWritten**</span><span class="sxs-lookup"><span data-stu-id="134eb-173"><span id="ChunkBytesWritten"></span><span id="chunkbyteswritten"></span><span id="CHUNKBYTESWRITTEN"></span>**ChunkBytesWritten**</span></span><br/> | <span data-ttu-id="134eb-174">Se a operação falhou com **um \_ \_ parâmetro de erro inválido**, esse valor indica o número máximo de bytes que o servidor permitirá para ser gravado em uma única parte, que é 1 MB.</span><span class="sxs-lookup"><span data-stu-id="134eb-174">If the operation failed with **ERROR\_INVALID\_PARAMETER**, this value indicates the maximum number of bytes the server will allow to be written in a single chunk, which is 1 MB.</span></span> <span data-ttu-id="134eb-175">Caso contrário, esse valor indica o número de bytes que foram gravados com êxito na última parte que não foi processada com êxito (se ocorrer uma gravação parcial).</span><span class="sxs-lookup"><span data-stu-id="134eb-175">Otherwise, this value indicates the number of bytes that were successfully written in the last chunk that was not successfully processed (if a partial write occurred).</span></span><br/> |
| <span data-ttu-id="134eb-176"><span id="TotalBytesWritten"></span><span id="totalbyteswritten"></span><span id="TOTALBYTESWRITTEN"></span>**TotalBytesWritten**</span><span class="sxs-lookup"><span data-stu-id="134eb-176"><span id="TotalBytesWritten"></span><span id="totalbyteswritten"></span><span id="TOTALBYTESWRITTEN"></span>**TotalBytesWritten**</span></span><br/> | <span data-ttu-id="134eb-177">Se a operação falhou com **um \_ \_ parâmetro de erro inválido**, esse valor indica o número máximo de bytes que o servidor copiará em uma única solicitação, que é 16 MB.</span><span class="sxs-lookup"><span data-stu-id="134eb-177">If the operation failed with **ERROR\_INVALID\_PARAMETER**, this value indicates the maximum number of bytes the server will copy in a single request, which is 16 MB.</span></span> <span data-ttu-id="134eb-178">Caso contrário, esse valor indica o número de bytes que foram gravados com êxito.</span><span class="sxs-lookup"><span data-stu-id="134eb-178">Otherwise, this value indicates the number of bytes that were successfully written.</span></span><br/>                                                                                                 |



 

## <a name="see-also"></a><span data-ttu-id="134eb-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="134eb-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="134eb-180">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="134eb-180">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="134eb-181">**\_chave de \_ \_ retomada de solicitação do fsctl SRV \_**</span><span class="sxs-lookup"><span data-stu-id="134eb-181">**FSCTL\_SRV\_REQUEST\_RESUME\_KEY**</span></span>](fsctl-srv-request-resume-key.md)
</dt> </dl>

 

 
