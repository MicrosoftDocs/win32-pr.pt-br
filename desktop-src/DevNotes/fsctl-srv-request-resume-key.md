---
description: O \_ código de \_ controle de chave de retomada de solicitação SRV fsctl \_ \_ é usado para recuperar uma referência de arquivo opaco para uso com o \_ código de controle COPYCHUNK do IOCTL.
ms.assetid: a6e0d253-5beb-4de8-8c40-d004f5794d47
title: FSCTL_SRV_REQUEST_RESUME_KEY código de controle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSCTL_SRV_REQUEST_RESUME_KEY
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8f11b70f7b4bfd05cbd5f7c29323f1dca00083a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826160"
---
# <a name="fsctl_srv_request_resume_key-control-code"></a><span data-ttu-id="9086d-103">FSCTL \_ SRV \_ solicitar \_ retomar \_ código de controle de chave</span><span class="sxs-lookup"><span data-stu-id="9086d-103">FSCTL\_SRV\_REQUEST\_RESUME\_KEY control code</span></span>

<span data-ttu-id="9086d-104">O código de controle de **\_ \_ \_ \_ chave de retomada de solicitação SRV fsctl** é usado para recuperar uma referência de arquivo opaco para uso com o código de controle [**\_ COPYCHUNK do IOCTL**](ioctl-copychunk.md) .</span><span class="sxs-lookup"><span data-stu-id="9086d-104">The **FSCTL\_SRV\_REQUEST\_RESUME\_KEY** control code is used to retrieve an opaque file reference for use with the [**IOCTL\_COPYCHUNK**](ioctl-copychunk.md) control code.</span></span>

<span data-ttu-id="9086d-105">Para executar essa operação, chame a função [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="9086d-105">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_SRV_REQUEST_RESUME_KEY, // dwIoControlCode
  NULL,                         // lpInBuffer
  0,                            // nInBufferSize
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="9086d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9086d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9086d-107">*hDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9086d-107">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9086d-108">Um identificador para o arquivo para o qual a chave do arquivo de origem deve ser solicitada.</span><span class="sxs-lookup"><span data-stu-id="9086d-108">A handle to the file for which the source file key is to be requested.</span></span> <span data-ttu-id="9086d-109">Para obter esse identificador, chame a função [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="9086d-109">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="9086d-110">*dwIoControlCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9086d-110">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9086d-111">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="9086d-111">The control code for the operation.</span></span> <span data-ttu-id="9086d-112">Use **a \_ \_ \_ \_ chave de retomada de solicitação do fsctl SRV** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="9086d-112">Use **FSCTL\_SRV\_REQUEST\_RESUME\_KEY** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="9086d-113">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="9086d-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="9086d-114">Não usado com esta operação; Defina como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="9086d-114">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9086d-115">*nInBufferSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9086d-115">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9086d-116">Não usado com esta operação; definido como zero.</span><span class="sxs-lookup"><span data-stu-id="9086d-116">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="9086d-117">*lpOutBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9086d-117">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9086d-118">Um ponteiro para o buffer de saída, **uma \_ solicitação \_ SRV \_ retomar** estrutura de chave.</span><span class="sxs-lookup"><span data-stu-id="9086d-118">A pointer to the output buffer, a **SRV\_REQUEST\_RESUME\_KEY** structure.</span></span> <span data-ttu-id="9086d-119">Para obter mais informações, consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="9086d-119">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="9086d-120">*nOutBufferSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9086d-120">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9086d-121">O tamanho do buffer de saída em bytes.</span><span class="sxs-lookup"><span data-stu-id="9086d-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9086d-122">*lpBytesReturned* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9086d-122">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9086d-123">Um ponteiro para uma variável que recebe o tamanho dos dados armazenados no buffer de saída, em bytes.</span><span class="sxs-lookup"><span data-stu-id="9086d-123">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="9086d-124">Se o buffer de saída for muito pequeno, a chamada falhará, a função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará um **\_ \_ buffer insuficiente de erro** e *lpBytesReturned* será zero.</span><span class="sxs-lookup"><span data-stu-id="9086d-124">If the output buffer is too small, the call fails, the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="9086d-125">Se o parâmetro *lpOverlapped* for **NULL**, *lpBytesReturned* não poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="9086d-125">If the *lpOverlapped* parameter is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="9086d-126">Mesmo quando uma operação não retorna dados de saída e o parâmetro *lpOutBuffer* é **nulo**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) faz uso de *lpBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="9086d-126">Even when an operation returns no output data and the *lpOutBuffer* parameter is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="9086d-127">Após tal operação, o valor de *lpBytesReturned* é inútil.</span><span class="sxs-lookup"><span data-stu-id="9086d-127">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="9086d-128">Se *lpOverlapped* não for **nulo**, *lpBytesReturned* poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="9086d-128">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="9086d-129">Se *lpOverlapped* não for **nulo** e a operação retornar dados, *lpBytesReturned* será inútil até que a operação sobreposta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="9086d-129">If *lpOverlapped* is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="9086d-130">Para recuperar o número de bytes retornados, chame a função [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="9086d-130">To retrieve the number of bytes returned, call the [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="9086d-131">Se o parâmetro *hDevice* estiver associado a uma porta de conclusão de e/s, você poderá recuperar o número de bytes retornados chamando a função [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="9086d-131">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="9086d-132">*lpOverlapped* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9086d-132">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9086d-133">Um ponteiro para uma estrutura [**sobreposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="9086d-133">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="9086d-134">Se o parâmetro *hDevice* tiver sido aberto sem especificar o **sinalizador de arquivo \_ \_ sobreposto**, *lpOverlapped* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="9086d-134">If the *hDevice* parameter was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="9086d-135">Se *hDevice* tiver sido aberto com o sinalizador de **sinalizador de arquivo \_ \_ sobreposto** , a operação será executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="9086d-135">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="9086d-136">Nesse caso, *lpOverlapped* deve apontar para uma estrutura [**sobreposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) válida que contém um identificador para um objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="9086d-136">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="9086d-137">Caso contrário, a função falhará de maneiras imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="9086d-137">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="9086d-138">Para operações sobrepostas, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retorna imediatamente e o objeto de evento é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="9086d-138">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="9086d-139">Caso contrário, a função não retorna até que a operação seja concluída ou até que ocorra um erro.</span><span class="sxs-lookup"><span data-stu-id="9086d-139">Otherwise, the function does not return until the operation has been completed or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9086d-140">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9086d-140">Return value</span></span>

<span data-ttu-id="9086d-141">Se a operação for concluída com êxito, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="9086d-141">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="9086d-142">Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero.</span><span class="sxs-lookup"><span data-stu-id="9086d-142">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="9086d-143">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="9086d-143">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="9086d-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="9086d-144">Remarks</span></span>

<span data-ttu-id="9086d-145">Este código de controle não tem nenhum arquivo de cabeçalho associado.</span><span class="sxs-lookup"><span data-stu-id="9086d-145">This control code has no associated header file.</span></span> <span data-ttu-id="9086d-146">Você deve definir o código de controle e as estruturas de dados da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="9086d-146">You must define the control code and data structures as follows.</span></span>

``` syntax
#define FSCTL_SRV_REQUEST_RESUME_KEY CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 30, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _SRV_RESUME_KEY {
    UINT64 ResumeKey;
    UINT64 Timestamp;
    UINT64 Pid;
} SRV_RESUME_KEY, *PSRV_RESUME_KEY;

typedef struct _SRV_REQUEST_RESUME_KEY {
    SRV_RESUME_KEY Key;
    ULONG  ContextLength;
    BYTE   Context[1];
} SRV_REQUEST_RESUME_KEY, *PSRV_REQUEST_RESUME_KEY;
```

<span data-ttu-id="9086d-147">Esses membros podem ser descritos da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="9086d-147">These members can be described as follows.</span></span>



| <span data-ttu-id="9086d-148">Membro</span><span class="sxs-lookup"><span data-stu-id="9086d-148">Member</span></span>                                                                                                                       | <span data-ttu-id="9086d-149">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="9086d-149">Description</span></span>                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9086d-150"><span id="ResumeKey"></span><span id="resumekey"></span><span id="RESUMEKEY"></span>**ResumeKey**</span><span class="sxs-lookup"><span data-stu-id="9086d-150"><span id="ResumeKey"></span><span id="resumekey"></span><span id="RESUMEKEY"></span>**ResumeKey**</span></span><br/>                 | <span data-ttu-id="9086d-151">Um valor opaco que identifica o arquivo de origem para o servidor.</span><span class="sxs-lookup"><span data-stu-id="9086d-151">An opaque value that identifies the source file to the server.</span></span><br/>                                                                                                   |
| <span data-ttu-id="9086d-152"><span id="Timestamp"></span><span id="timestamp"></span><span id="TIMESTAMP"></span>**Estampa**</span><span class="sxs-lookup"><span data-stu-id="9086d-152"><span id="Timestamp"></span><span id="timestamp"></span><span id="TIMESTAMP"></span>**Timestamp**</span></span><br/>                 | <span data-ttu-id="9086d-153">Um valor opaco que identifica a hora em que o arquivo foi aberto.</span><span class="sxs-lookup"><span data-stu-id="9086d-153">An opaque value that identifies the time when the file was opened.</span></span><br/>                                                                                               |
| <span data-ttu-id="9086d-154"><span id="Pid"></span><span id="pid"></span><span id="PID"></span>**Pessoal**</span><span class="sxs-lookup"><span data-stu-id="9086d-154"><span id="Pid"></span><span id="pid"></span><span id="PID"></span>**Pid**</span></span><br/>                                         | <span data-ttu-id="9086d-155">Um valor opaco que identifica o processo que abriu o arquivo.</span><span class="sxs-lookup"><span data-stu-id="9086d-155">An opaque value that identifies the process that opened the file.</span></span><br/>                                                                                                |
| <span data-ttu-id="9086d-156"><span id="Key"></span><span id="key"></span><span id="KEY"></span>**Chaves**</span><span class="sxs-lookup"><span data-stu-id="9086d-156"><span id="Key"></span><span id="key"></span><span id="KEY"></span>**Key**</span></span><br/>                                         | <span data-ttu-id="9086d-157">Uma estrutura de **\_ \_ chave de retomada SRV** .</span><span class="sxs-lookup"><span data-stu-id="9086d-157">A **SRV\_RESUME\_KEY** structure.</span></span> <span data-ttu-id="9086d-158">Para executar uma operação de cópia do lado do servidor, use essa estrutura com o código de controle [**\_ COPYCHUNK do IOCTL**](ioctl-copychunk.md) .</span><span class="sxs-lookup"><span data-stu-id="9086d-158">To perform a server-side copy operation, use this structure with the [**IOCTL\_COPYCHUNK**](ioctl-copychunk.md) control code.</span></span><br/> |
| <span data-ttu-id="9086d-159"><span id="ContextLength"></span><span id="contextlength"></span><span id="CONTEXTLENGTH"></span>**ContextLength**</span><span class="sxs-lookup"><span data-stu-id="9086d-159"><span id="ContextLength"></span><span id="contextlength"></span><span id="CONTEXTLENGTH"></span>**ContextLength**</span></span><br/> | <span data-ttu-id="9086d-160">Este membro é reservado para uso do sistema; Não use.</span><span class="sxs-lookup"><span data-stu-id="9086d-160">This member is reserved for system use; do not use.</span></span><br/>                                                                                                              |
| <span data-ttu-id="9086d-161"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>**Noticioso**</span><span class="sxs-lookup"><span data-stu-id="9086d-161"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>**Context**</span></span><br/>                         | <span data-ttu-id="9086d-162">Este membro é reservado para uso do sistema; Não use.</span><span class="sxs-lookup"><span data-stu-id="9086d-162">This member is reserved for system use; do not use.</span></span><br/>                                                                                                              |



 

## <a name="see-also"></a><span data-ttu-id="9086d-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="9086d-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9086d-164">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="9086d-164">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="9086d-165">**COPYCHUNK de IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="9086d-165">**IOCTL\_COPYCHUNK**</span></span>](ioctl-copychunk.md)
</dt> </dl>

 

 
