---
description: Determina se um volume é um volume CSV.
ms.assetid: 6B09B519-1E2F-4757-AAD5-1E4C81023E14
title: IOCTL_VOLUME_IS_CSV código de controle (Ntddvol. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VOLUME_IS_CSV
api_type:
- HeaderDef
api_location:
- Ntddvol.h
ms.openlocfilehash: 8121e1b89c88ad05a2c2be8537d7170bfabfc412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297357"
---
# <a name="ioctl_volume_is_csv-control-code"></a><span data-ttu-id="79bcf-103">O \_ volume do IOCTL \_ é um código de \_ controle CSV</span><span class="sxs-lookup"><span data-stu-id="79bcf-103">IOCTL\_VOLUME\_IS\_CSV control code</span></span>

<span data-ttu-id="79bcf-104">Determina se um volume é um volume CSV.</span><span class="sxs-lookup"><span data-stu-id="79bcf-104">Determines whether a volume is a CSV volume.</span></span>

<span data-ttu-id="79bcf-105">Para executar essa operação, chame a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="79bcf-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE) hDevice,              // handle to device
                 IOCTL_VOLUME_IS_CSV,           // dwIoControlCode
                 NULL,                          // input buffer
                 0,                             // size of input buffer
                 (LPVOID) lpOutBuffer,          // lpOutBuffer
                 (DWORD) nOutBufferSize,        // nOutBufferSize
                 (LPDWORD) lpBytesReturned,     // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped ); // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="79bcf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79bcf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79bcf-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="79bcf-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="79bcf-108">Um identificador para o volume.</span><span class="sxs-lookup"><span data-stu-id="79bcf-108">A handle to the volume.</span></span> <span data-ttu-id="79bcf-109">Para recuperar um identificador de volume, chame a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="79bcf-109">To retrieve a volume handle, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="79bcf-110">Somente os administradores podem abrir identificadores de volume.</span><span class="sxs-lookup"><span data-stu-id="79bcf-110">Only administrators can open volume handles.</span></span>

</dd> <dt>

<span data-ttu-id="79bcf-111">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="79bcf-111">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="79bcf-112">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="79bcf-112">The control code for the operation.</span></span> <span data-ttu-id="79bcf-113">Use **o \_ volume do IOCTL \_ é \_ CSV** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="79bcf-113">Use **IOCTL\_VOLUME\_IS\_CSV** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="79bcf-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="79bcf-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="79bcf-115">Não usado com esta operação; Defina como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="79bcf-115">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="79bcf-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="79bcf-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="79bcf-117">Não usado com esta operação; Defina como zero (0).</span><span class="sxs-lookup"><span data-stu-id="79bcf-117">Not used with this operation; set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="79bcf-118">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="79bcf-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="79bcf-119">Um ponteiro para **verdadeiro** se o volume for um volume CSV; caso contrário, a chamada de função falhará.</span><span class="sxs-lookup"><span data-stu-id="79bcf-119">A pointer to **TRUE** if the volume is a CSV volume; otherwise, the function call fails.</span></span>

</dd> <dt>

<span data-ttu-id="79bcf-120">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="79bcf-120">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="79bcf-121">O tamanho do buffer de saída em bytes.</span><span class="sxs-lookup"><span data-stu-id="79bcf-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="79bcf-122">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="79bcf-122">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="79bcf-123">Um ponteiro para uma variável que recebe o tamanho dos dados armazenados no buffer de saída, em bytes.</span><span class="sxs-lookup"><span data-stu-id="79bcf-123">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="79bcf-124">Se *lpOverlapped* for **nulo**, *lpBytesReturned* não poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="79bcf-124">If *lpOverlapped* is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="79bcf-125">Mesmo quando uma operação não retorna dados de saída e *lpOutBuffer* é **nula**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) faz uso de *lpBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="79bcf-125">Even when an operation returns no output data and *lpOutBuffer* is **NULL**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="79bcf-126">Após tal operação, o valor de *lpBytesReturned* é inútil.</span><span class="sxs-lookup"><span data-stu-id="79bcf-126">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="79bcf-127">Se *lpOverlapped* não for **nulo**, *lpBytesReturned* poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="79bcf-127">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="79bcf-128">Se esse parâmetro não for **nulo** e a operação retornar dados, *lpBytesReturned* será inútil até que a operação sobreposta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="79bcf-128">If this parameter is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="79bcf-129">Para recuperar o número de bytes retornados, chame [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult).</span><span class="sxs-lookup"><span data-stu-id="79bcf-129">To retrieve the number of bytes returned, call [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult).</span></span> <span data-ttu-id="79bcf-130">Se *hDevice* estiver associado a uma porta de conclusão de e/s, você poderá recuperar o número de bytes retornados chamando [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span><span class="sxs-lookup"><span data-stu-id="79bcf-130">If *hDevice* is associated with an I/O completion port, you can retrieve the number of bytes returned by calling [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span></span>

</dd> <dt>

<span data-ttu-id="79bcf-131">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="79bcf-131">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="79bcf-132">Um ponteiro para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="79bcf-132">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="79bcf-133">Se *hDevice* tiver sido aberto sem especificar o **sinalizador de arquivo \_ \_ sobreposto**, *lpOverlapped* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="79bcf-133">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="79bcf-134">Se *hDevice* tiver sido aberto com o sinalizador de **sinalizador de arquivo \_ \_ sobreposto** , a operação será executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="79bcf-134">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="79bcf-135">Nesse caso, *lpOverlapped* deve apontar para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida que contém um identificador para um objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="79bcf-135">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="79bcf-136">Caso contrário, a função falhará de maneiras imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="79bcf-136">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="79bcf-137">Para operações sobrepostas, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retorna imediatamente e o objeto de evento é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="79bcf-137">For overlapped operations, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="79bcf-138">Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.</span><span class="sxs-lookup"><span data-stu-id="79bcf-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79bcf-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="79bcf-139">Return value</span></span>

<span data-ttu-id="79bcf-140">Se a operação for concluída com êxito, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="79bcf-140">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="79bcf-141">Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero (0).</span><span class="sxs-lookup"><span data-stu-id="79bcf-141">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero (0).</span></span> <span data-ttu-id="79bcf-142">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="79bcf-142">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="79bcf-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79bcf-143">Requirements</span></span>



| <span data-ttu-id="79bcf-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="79bcf-144">Requirement</span></span> | <span data-ttu-id="79bcf-145">Valor</span><span class="sxs-lookup"><span data-stu-id="79bcf-145">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="79bcf-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79bcf-146">Minimum supported client</span></span><br/> | <span data-ttu-id="79bcf-147">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="79bcf-147">None supported</span></span><br/>                                                            |
| <span data-ttu-id="79bcf-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79bcf-148">Minimum supported server</span></span><br/> | <span data-ttu-id="79bcf-149">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="79bcf-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="79bcf-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="79bcf-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="79bcf-151"><dt>Ntddvol. h</dt></span><span class="sxs-lookup"><span data-stu-id="79bcf-151"><dt>Ntddvol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79bcf-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="79bcf-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79bcf-153">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="79bcf-153">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="79bcf-154">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="79bcf-154">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="79bcf-155">Códigos de controle de gerenciamento de volume</span><span class="sxs-lookup"><span data-stu-id="79bcf-155">Volume Management Control Codes</span></span>](volume-management-control-codes.md)
</dt> </dl>

 

