---
description: Recupera a marca atual das baterias.
ms.assetid: 0bbe59ba-e037-47ce-a54a-6500ea7c9bc5
title: IOCTL_BATTERY_QUERY_TAG código de controle (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_TAG
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: 1d8435e62c4f061ac13b3e18e5bcd64afcb399c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759354"
---
# <a name="ioctl_battery_query_tag-control-code"></a><span data-ttu-id="a7d02-103">\_Código de \_ controle de marca de consulta da bateria do IOCTL \_</span><span class="sxs-lookup"><span data-stu-id="a7d02-103">IOCTL\_BATTERY\_QUERY\_TAG control code</span></span>

<span data-ttu-id="a7d02-104">Recupera a marca atual da bateria.</span><span class="sxs-lookup"><span data-stu-id="a7d02-104">Retrieves the battery's current tag.</span></span>

<span data-ttu-id="a7d02-105">Para executar essa operação, chame a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="a7d02-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to battery
  IOCTL_BATTERY_QUERY_TAG,     // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of input buffer
  (LPVOID) lpOutBuffer,        // output buffer
  (DWORD) nOutBufferSize,      // size of output buffer
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped);// OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="a7d02-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7d02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7d02-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="a7d02-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="a7d02-108">Um identificador para a bateria da qual a marca deve ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="a7d02-108">A handle to the battery from which the tag is to be retrieved.</span></span> <span data-ttu-id="a7d02-109">Para recuperar um identificador de dispositivo, chame a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="a7d02-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="a7d02-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="a7d02-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="a7d02-111">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="a7d02-111">The control code for the operation.</span></span> <span data-ttu-id="a7d02-112">Esse valor identifica a operação específica a ser executada e o tipo de dispositivo no qual executá-lo.</span><span class="sxs-lookup"><span data-stu-id="a7d02-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="a7d02-113">Use **a \_ \_ \_ marca de consulta da bateria do IOCTL** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="a7d02-113">Use **IOCTL\_BATTERY\_QUERY\_TAG** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="a7d02-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="a7d02-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="a7d02-115">Um ponteiro para um buffer de entrada **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="a7d02-115">A pointer to a **ULONG** input buffer.</span></span> <span data-ttu-id="a7d02-116">O valor indica o número de milissegundos a esperar se não houver bateria.</span><span class="sxs-lookup"><span data-stu-id="a7d02-116">The value indicates the number of milliseconds to wait if there is no battery.</span></span> <span data-ttu-id="a7d02-117">Um valor de-1 indica que a solicitação aguardará indefinidamente (ou até ser cancelada por algum outro evento).</span><span class="sxs-lookup"><span data-stu-id="a7d02-117">A value of -1 indicates the request will wait indefinitely (or until canceled by some other event).</span></span>

</dd> <dt>

<span data-ttu-id="a7d02-118">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="a7d02-118">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="a7d02-119">O tamanho do buffer de entrada, em bytes.</span><span class="sxs-lookup"><span data-stu-id="a7d02-119">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a7d02-120">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="a7d02-120">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="a7d02-121">Um ponteiro para um buffer de saída **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="a7d02-121">A pointer to a **ULONG** output buffer.</span></span> <span data-ttu-id="a7d02-122">Em caso de sucesso, esse buffer contém a marca de bateria atual, que pode ser qualquer valor, exceto a marca de bateria \_ \_ inválida.</span><span class="sxs-lookup"><span data-stu-id="a7d02-122">On success this buffer contains the current battery tag, which can be any value except BATTERY\_TAG\_INVALID.</span></span> <span data-ttu-id="a7d02-123">Em caso de falha, se [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornar o arquivo de erro de código de erro **\_ \_ não \_ encontrado**, esse buffer conterá a marca de bateria de valor **\_ \_ inválida**.</span><span class="sxs-lookup"><span data-stu-id="a7d02-123">On failure, if [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_FILE\_NOT\_FOUND**, this buffer contains the value **BATTERY\_TAG\_INVALID**.</span></span>

</dd> <dt>

<span data-ttu-id="a7d02-124">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="a7d02-124">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="a7d02-125">O tamanho do buffer de saída em bytes.</span><span class="sxs-lookup"><span data-stu-id="a7d02-125">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a7d02-126">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="a7d02-126">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="a7d02-127">Um ponteiro para uma variável que recebe o tamanho dos dados armazenados no buffer *lpOutBuffer* , em bytes.</span><span class="sxs-lookup"><span data-stu-id="a7d02-127">A pointer to a variable that receives the size of the data stored in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="a7d02-128">Se o buffer de saída for muito pequeno para retornar dados, a chamada falhará, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o erro de código de erro **\_ \_ buffer insuficiente** e o número de bytes retornados será zero.</span><span class="sxs-lookup"><span data-stu-id="a7d02-128">If the output buffer is too small to return any data then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_INSUFFICIENT\_BUFFER**, and the returned byte count is zero.</span></span>

<span data-ttu-id="a7d02-129">Se *lpOverlapped* for **NULL** (e/s não sobreposta), *lpBytesReturned* não poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a7d02-129">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="a7d02-130">Se *lpOverlapped* não for **nulo** (e/s sobreposta), *lpBytesReturned* poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a7d02-130">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="a7d02-131">Se essa for uma operação sobreposta, você poderá recuperar o número de bytes retornados chamando a função [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="a7d02-131">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="a7d02-132">Se *hDevice* estiver associado a uma porta de conclusão de e/s, você poderá obter o número de bytes retornados chamando a função [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="a7d02-132">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="a7d02-133">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="a7d02-133">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="a7d02-134">Um ponteiro para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="a7d02-134">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="a7d02-135">Se *hDevice* tiver sido aberto com o sinalizador **\_ \_ sobreposto de sinalizador de arquivo** , *lpOverlapped* deverá apontar para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="a7d02-135">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="a7d02-136">Nesse caso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) é executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="a7d02-136">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="a7d02-137">Se o dispositivo tiver sido aberto com o sinalizador **\_ \_ sobreposto de sinalizador de arquivo** e *lpOverlapped* for **nulo**, a função falhará de maneiras imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="a7d02-137">If the device was opened with the **FILE\_FLAG\_OVERLAPPED** flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="a7d02-138">Se *hDevice* tiver sido aberto sem especificar o sinalizador **\_ \_ sobreposto do sinalizador de arquivo** , *lpOverlapped* será ignorado e a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) não retornará até que a operação seja concluída ou até que ocorra um erro.</span><span class="sxs-lookup"><span data-stu-id="a7d02-138">If *hDevice* was opened without specifying the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7d02-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a7d02-139">Return value</span></span>

<span data-ttu-id="a7d02-140">Se a operação for concluída com êxito, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="a7d02-140">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="a7d02-141">Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero.</span><span class="sxs-lookup"><span data-stu-id="a7d02-141">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="a7d02-142">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="a7d02-142">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="a7d02-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7d02-143">Remarks</span></span>

<span data-ttu-id="a7d02-144">Esta bateria IOCTL recupera a marca atual da bateria.</span><span class="sxs-lookup"><span data-stu-id="a7d02-144">This battery IOCTL retrieves the battery's current tag.</span></span> <span data-ttu-id="a7d02-145">A marca de bateria é um valor exclusivo diferente de zero que muda quando a bateria física é reinserida, substituída ou passa por alterações de características.</span><span class="sxs-lookup"><span data-stu-id="a7d02-145">The battery tag is a unique nonzero value that changes when the physical battery is reinserted, replaced, or undergoes any characteristic changes.</span></span> <span data-ttu-id="a7d02-146">Consulte a seção marcas de bateria no tópico Visão geral [das informações da bateria](battery-information.md) para obter mais detalhes sobre quando uma marca de bateria é alterada, como detectar a alteração e como um aplicativo deve continuar após uma alteração na marca da bateria.</span><span class="sxs-lookup"><span data-stu-id="a7d02-146">See the Battery Tags section in the [Battery Information](battery-information.md) overview topic for more detail on when a battery tag changes, how to detect the change, and how an application should proceed after a battery tag change.</span></span> <span data-ttu-id="a7d02-147">Quando uma bateria não estiver presente, essa solicitação aguardará o horário indicado e, se ainda não houver bateria presente, ela retornará o arquivo de **erro \_ \_ não \_ encontrado** e definirá a marca de bateria como a **marca de bateria é \_ \_ inválida**.</span><span class="sxs-lookup"><span data-stu-id="a7d02-147">When a battery is not present, this request will wait the indicated time, and if there is still no battery present, then it will return **ERROR\_FILE\_NOT\_FOUND** and set the battery tag to **BATTERY\_TAG\_INVALID**.</span></span> <span data-ttu-id="a7d02-148">(Consulte informações da bateria para obter mais informações.)</span><span class="sxs-lookup"><span data-stu-id="a7d02-148">(See Battery Information for more information.)</span></span>

<span data-ttu-id="a7d02-149">Todas as solicitações para outras informações de bateria exigem que o chamador forneça a marca de bateria correspondente.</span><span class="sxs-lookup"><span data-stu-id="a7d02-149">All requests for other battery information require the caller to supply the matching battery tag.</span></span> <span data-ttu-id="a7d02-150">Isso garante que o chamador esteja recebendo informações para a mesma bateria para cada solicitação e garante que o chamador esteja ciente das alterações de bateria sem sondagem constante.</span><span class="sxs-lookup"><span data-stu-id="a7d02-150">This ensures that the caller is receiving information for the same battery for every request and ensures that the caller is aware of battery changes without constant polling.</span></span>

<span data-ttu-id="a7d02-151">Para as implicações da e/s sobreposta nessa operação, consulte a seção comentários do tópico [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="a7d02-151">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="a7d02-152">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a7d02-152">Examples</span></span>

<span data-ttu-id="a7d02-153">Para obter um exemplo, consulte [enumerando dispositivos de bateria](enumerating-battery-devices.md).</span><span class="sxs-lookup"><span data-stu-id="a7d02-153">For an example, see [Enumerating Battery Devices](enumerating-battery-devices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a7d02-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7d02-154">Requirements</span></span>



| <span data-ttu-id="a7d02-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7d02-155">Requirement</span></span> | <span data-ttu-id="a7d02-156">Valor</span><span class="sxs-lookup"><span data-stu-id="a7d02-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7d02-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7d02-157">Minimum supported client</span></span><br/> | <span data-ttu-id="a7d02-158">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a7d02-158">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="a7d02-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7d02-159">Minimum supported server</span></span><br/> | <span data-ttu-id="a7d02-160">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a7d02-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="a7d02-161">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a7d02-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7d02-162"><dt>Poclass. h; </dt> <dt>BatClass. h no Windows server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="a7d02-162"><dt>Poclass.h; </dt> <dt>BatClass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7d02-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7d02-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7d02-164">Informações da bateria</span><span class="sxs-lookup"><span data-stu-id="a7d02-164">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="a7d02-165">Códigos de controle de gerenciamento de energia</span><span class="sxs-lookup"><span data-stu-id="a7d02-165">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="a7d02-166">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="a7d02-166">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="a7d02-167">**\_informações de \_ consulta da bateria do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="a7d02-167">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> <dt>

[<span data-ttu-id="a7d02-168">**\_status de \_ consulta da bateria do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="a7d02-168">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="a7d02-169">**\_informações do \_ conjunto de baterias do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="a7d02-169">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

