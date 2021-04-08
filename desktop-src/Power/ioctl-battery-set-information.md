---
description: Define várias informações de bateria.
ms.assetid: b827983d-5fb8-43f2-b732-541d16b3eb7b
title: IOCTL_BATTERY_SET_INFORMATION código de controle (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_SET_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: f540037486f16e920b3346620ff934b279652e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828370"
---
# <a name="ioctl_battery_set_information-control-code"></a><span data-ttu-id="4dddc-103">\_Código de \_ controle de informações do conjunto de baterias do IOCTL \_</span><span class="sxs-lookup"><span data-stu-id="4dddc-103">IOCTL\_BATTERY\_SET\_INFORMATION control code</span></span>

<span data-ttu-id="4dddc-104">Define várias informações de bateria.</span><span class="sxs-lookup"><span data-stu-id="4dddc-104">Sets various battery information.</span></span> <span data-ttu-id="4dddc-105">A estrutura do parâmetro de entrada, [**\_ \_ as informações do conjunto de bateria**](battery-set-information-str.md), indicam quais informações de status da bateria serão definidas.</span><span class="sxs-lookup"><span data-stu-id="4dddc-105">The input parameter structure, [**BATTERY\_SET\_INFORMATION**](battery-set-information-str.md), indicates which battery status information is to be set.</span></span>

<span data-ttu-id="4dddc-106">Para executar essa operação, chame a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="4dddc-106">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,              // handle to battery
  IOCTL_BATTERY_SET_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,           // input buffer
  (DWORD) nInBufferSize,         // size of input buffer
  NULL,                          // lpOutBuffer
  0,                             // nOutBufferSize
  (LPDWORD) lpBytesReturned,     // number of bytes returned
  (LPOVERLAPPED) lpOverlapped    // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="4dddc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4dddc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dddc-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="4dddc-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="4dddc-109">Um identificador para a bateria na qual as informações serão definidas.</span><span class="sxs-lookup"><span data-stu-id="4dddc-109">A handle to the battery on which the information is to be set.</span></span> <span data-ttu-id="4dddc-110">Para recuperar um identificador de dispositivo, chame a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="4dddc-110">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="4dddc-111">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="4dddc-111">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="4dddc-112">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="4dddc-112">The control code for the operation.</span></span> <span data-ttu-id="4dddc-113">Esse valor identifica a operação específica a ser executada e o tipo de dispositivo no qual executá-lo.</span><span class="sxs-lookup"><span data-stu-id="4dddc-113">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="4dddc-114">Use **\_ \_ \_ as informações do conjunto de bateria do IOCTL** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="4dddc-114">Use **IOCTL\_BATTERY\_SET\_INFORMATION** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="4dddc-115">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="4dddc-115">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="4dddc-116">Um ponteiro para uma estrutura de [**\_ \_ informações de conjunto de bateria**](battery-set-information-str.md) .</span><span class="sxs-lookup"><span data-stu-id="4dddc-116">A pointer to a [**BATTERY\_SET\_INFORMATION**](battery-set-information-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4dddc-117">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="4dddc-117">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="4dddc-118">O tamanho do buffer de entrada, em bytes.</span><span class="sxs-lookup"><span data-stu-id="4dddc-118">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="4dddc-119">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="4dddc-119">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="4dddc-120">Não usado com esta operação; Defina como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="4dddc-120">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4dddc-121">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="4dddc-121">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="4dddc-122">Não usado com esta operação; definido como zero.</span><span class="sxs-lookup"><span data-stu-id="4dddc-122">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="4dddc-123">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="4dddc-123">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="4dddc-124">Um ponteiro para uma variável que recebe o tamanho dos dados retornados no buffer *lpOutBuffer* , em bytes.</span><span class="sxs-lookup"><span data-stu-id="4dddc-124">A pointer to a variable that receives the size of data returned in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="4dddc-125">Se o buffer de saída for muito pequeno para retornar dados, a chamada falhará, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o erro de código de erro \_ buffer insuficiente \_ e o número de bytes retornados será zero.</span><span class="sxs-lookup"><span data-stu-id="4dddc-125">If the output buffer is too small to return any data, then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_INSUFFICIENT\_BUFFER, and the returned byte count is zero.</span></span>

<span data-ttu-id="4dddc-126">Se *lpOverlapped* for **NULL** (e/s não sobreposta), *lpBytesReturned* não poderá ser **nulo**, mesmo se *lpOutBuffer* for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="4dddc-126">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**, even if *lpOutBuffer* is **NULL**.</span></span>

<span data-ttu-id="4dddc-127">Se *lpOverlapped* não for **nulo** (e/s sobreposta), *lpBytesReturned* poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="4dddc-127">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="4dddc-128">Se essa for uma operação sobreposta, você poderá recuperar o número de bytes retornados chamando a função [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="4dddc-128">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="4dddc-129">Se *hDevice* estiver associado a uma porta de conclusão de e/s, você poderá obter o número de bytes retornados chamando a função [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="4dddc-129">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="4dddc-130">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="4dddc-130">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="4dddc-131">Um ponteiro para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="4dddc-131">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="4dddc-132">Se *hDevice* tiver sido aberto com o \_ sinalizador sobreposto de sinalizador de arquivo \_ , *lpOverlapped* deverá apontar para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="4dddc-132">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="4dddc-133">Nesse caso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) é executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="4dddc-133">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="4dddc-134">Se o dispositivo tiver sido aberto com o \_ sinalizador sobreposto de sinalizador de arquivo \_ e *lpOverlapped* for **nulo**, a função falhará de maneiras imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="4dddc-134">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="4dddc-135">Se *hDevice* tiver sido aberto sem especificar o \_ sinalizador sobreposto do sinalizador de arquivo \_ , *lpOverlapped* será ignorado e a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) não retornará até que a operação seja concluída ou até que ocorra um erro.</span><span class="sxs-lookup"><span data-stu-id="4dddc-135">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dddc-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4dddc-136">Return value</span></span>

<span data-ttu-id="4dddc-137">Se a operação for concluída com êxito, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="4dddc-137">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="4dddc-138">Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero.</span><span class="sxs-lookup"><span data-stu-id="4dddc-138">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="4dddc-139">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="4dddc-139">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="4dddc-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="4dddc-140">Remarks</span></span>

<span data-ttu-id="4dddc-141">Todas as solicitações para definir as informações da bateria serão concluídas com o status do arquivo de erro \_ \_ não \_ encontrado se a marca de bateria da solicitação não corresponder à da marca da bateria atual.</span><span class="sxs-lookup"><span data-stu-id="4dddc-141">All requests to set battery information will complete with the status of ERROR\_FILE\_NOT\_FOUND if the battery tag of the request does not match that of the current battery tag.</span></span>

<span data-ttu-id="4dddc-142">Para as implicações da e/s sobreposta nessa operação, consulte a seção comentários do tópico [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="4dddc-142">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dddc-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4dddc-143">Requirements</span></span>



| <span data-ttu-id="4dddc-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="4dddc-144">Requirement</span></span> | <span data-ttu-id="4dddc-145">Valor</span><span class="sxs-lookup"><span data-stu-id="4dddc-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dddc-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4dddc-146">Minimum supported client</span></span><br/> | <span data-ttu-id="4dddc-147">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4dddc-147">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="4dddc-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4dddc-148">Minimum supported server</span></span><br/> | <span data-ttu-id="4dddc-149">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4dddc-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="4dddc-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4dddc-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dddc-151"><dt>Poclass. h; </dt> <dt>Batclass. h no Windows server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="4dddc-151"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dddc-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="4dddc-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dddc-153">Informações da bateria</span><span class="sxs-lookup"><span data-stu-id="4dddc-153">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="4dddc-154">Códigos de controle de gerenciamento de energia</span><span class="sxs-lookup"><span data-stu-id="4dddc-154">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="4dddc-155">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="4dddc-155">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="4dddc-156">**\_informações de conjunto de bateria \_**</span><span class="sxs-lookup"><span data-stu-id="4dddc-156">**BATTERY\_SET\_INFORMATION**</span></span>](battery-set-information-str.md)
</dt> <dt>

[<span data-ttu-id="4dddc-157">**\_informações de \_ consulta da bateria do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="4dddc-157">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> <dt>

[<span data-ttu-id="4dddc-158">**\_status de \_ consulta da bateria do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="4dddc-158">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="4dddc-159">**\_marca de \_ consulta da bateria do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="4dddc-159">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> </dl>

 

