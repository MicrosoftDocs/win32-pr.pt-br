---
description: Recupera o status atual da bateria.
ms.assetid: 7a7bf429-9b2c-4faf-9f27-fb5fd8dd18df
title: IOCTL_BATTERY_QUERY_STATUS código de controle (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: e2de9d3ab48aec13a9a5c1957a5f98aefbe6a09f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787471"
---
# <a name="ioctl_battery_query_status-control-code"></a><span data-ttu-id="cca55-103">\_Código de \_ controle do status de consulta da bateria do IOCTL \_</span><span class="sxs-lookup"><span data-stu-id="cca55-103">IOCTL\_BATTERY\_QUERY\_STATUS control code</span></span>

<span data-ttu-id="cca55-104">Recupera o status atual da bateria.</span><span class="sxs-lookup"><span data-stu-id="cca55-104">Retrieves the current status of the battery.</span></span>

<span data-ttu-id="cca55-105">Para executar essa operação, chame a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="cca55-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,           // handle to battery
  IOCTL_BATTERY_QUERY_STATUS, // dwIoControlCode
  (LPVOID) lpInBuffer,        // input buffer
  (DWORD) nInBufferSize,      // size of input buffer
  (LPVOID) lpOutBuffer,       // output buffer
  (DWORD) nOutBufferSize,     // size of output buffer
  (LPDWORD) lpBytesReturned,  // number of bytes returned
  (LPOVERLAPPED) lpOverlapped // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="cca55-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cca55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cca55-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="cca55-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="cca55-108">Um identificador para a bateria a partir da qual as informações serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="cca55-108">A handle to the battery from which information is to be returned.</span></span> <span data-ttu-id="cca55-109">Para recuperar um identificador de dispositivo, chame a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="cca55-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="cca55-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="cca55-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="cca55-111">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="cca55-111">The control code for the operation.</span></span> <span data-ttu-id="cca55-112">Esse valor identifica a operação específica a ser executada e o tipo de dispositivo no qual executá-lo.</span><span class="sxs-lookup"><span data-stu-id="cca55-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="cca55-113">Use **o \_ \_ \_ status de consulta da bateria do IOCTL** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="cca55-113">Use **IOCTL\_BATTERY\_QUERY\_STATUS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="cca55-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="cca55-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="cca55-115">Um ponteiro para uma estrutura de [**\_ \_ status de espera da bateria**](battery-wait-status-str.md) .</span><span class="sxs-lookup"><span data-stu-id="cca55-115">A pointer to a [**BATTERY\_WAIT\_STATUS**](battery-wait-status-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cca55-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="cca55-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="cca55-117">O tamanho do buffer de entrada, em bytes.</span><span class="sxs-lookup"><span data-stu-id="cca55-117">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="cca55-118">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="cca55-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="cca55-119">Um ponteiro para uma estrutura de [**\_ status da bateria**](battery-status-str.md) .</span><span class="sxs-lookup"><span data-stu-id="cca55-119">A pointer to a [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cca55-120">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="cca55-120">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="cca55-121">O tamanho do buffer de saída em bytes.</span><span class="sxs-lookup"><span data-stu-id="cca55-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="cca55-122">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="cca55-122">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="cca55-123">Um ponteiro para uma variável que recebe o tamanho dos dados retornados no buffer *lpOutBuffer* , em bytes.</span><span class="sxs-lookup"><span data-stu-id="cca55-123">A pointer to a variable that receives the size of the data returned in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="cca55-124">Se o buffer de saída for muito pequeno para retornar dados, a chamada falhará, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o erro de código de erro **\_ \_ buffer insuficiente** e o número de bytes retornados será zero.</span><span class="sxs-lookup"><span data-stu-id="cca55-124">If the output buffer is too small to return any data then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_INSUFFICIENT\_BUFFER**, and the returned byte count is zero.</span></span>

<span data-ttu-id="cca55-125">Se *lpOverlapped* for **NULL** (e/s não sobreposta), *lpBytesReturned* não poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="cca55-125">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="cca55-126">Se *lpOverlapped* não for **nulo** (e/s sobreposta), *lpBytesReturned* poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="cca55-126">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="cca55-127">Se essa for uma operação sobreposta, você poderá recuperar o número de bytes retornados chamando a função [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="cca55-127">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="cca55-128">Se *hDevice* estiver associado a uma porta de conclusão de e/s, você poderá obter o número de bytes retornados chamando a função [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="cca55-128">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="cca55-129">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="cca55-129">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="cca55-130">Um ponteiro para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="cca55-130">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="cca55-131">Se *hDevice* tiver sido aberto com o sinalizador **\_ \_ sobreposto de sinalizador de arquivo** , *lpOverlapped* deverá apontar para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="cca55-131">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="cca55-132">Nesse caso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) é executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="cca55-132">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="cca55-133">Se o dispositivo tiver sido aberto com o sinalizador **\_ \_ sobreposto de sinalizador de arquivo** e *lpOverlapped* for **nulo**, a função falhará de maneiras imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="cca55-133">If the device was opened with the **FILE\_FLAG\_OVERLAPPED** flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="cca55-134">Se *hDevice* tiver sido aberto sem especificar o sinalizador **\_ \_ sobreposto do sinalizador de arquivo** , *lpOverlapped* será ignorado e a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) não retornará até que a operação seja concluída ou até que ocorra um erro.</span><span class="sxs-lookup"><span data-stu-id="cca55-134">If *hDevice* was opened without specifying the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cca55-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cca55-135">Return value</span></span>

<span data-ttu-id="cca55-136">Se a operação for concluída com êxito, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="cca55-136">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="cca55-137">Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero.</span><span class="sxs-lookup"><span data-stu-id="cca55-137">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="cca55-138">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="cca55-138">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="cca55-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="cca55-139">Remarks</span></span>

<span data-ttu-id="cca55-140">Essa bateria IOCTL recupera o status da bateria no momento em que a operação retorna.</span><span class="sxs-lookup"><span data-stu-id="cca55-140">This battery IOCTL retrieves the status of the battery at the time the operation returns.</span></span> <span data-ttu-id="cca55-141">A estrutura do parâmetro de entrada, o [**\_ \_ status de espera da bateria**](battery-wait-status-str.md), indica quando o status da bateria deve ser processado e retornado.</span><span class="sxs-lookup"><span data-stu-id="cca55-141">The input parameter structure, [**BATTERY\_WAIT\_STATUS**](battery-wait-status-str.md), indicates when the battery status is to be processed and returned.</span></span>

<span data-ttu-id="cca55-142">As solicitações de status da bateria podem ser para o retorno imediato ou podem ser definidas para aguardar uma determinada condição antes de concluir.</span><span class="sxs-lookup"><span data-stu-id="cca55-142">Requests for battery status can be for immediate return or can be set to wait for a particular condition before completing.</span></span> <span data-ttu-id="cca55-143">Por exemplo, é possível fazer uma solicitação de informações da bateria que aguarde até que a capacidade da bateria atinja um ponto especificado ou o estado da bateria seja alterado.</span><span class="sxs-lookup"><span data-stu-id="cca55-143">For example, a request for battery information can be made that waits until the battery capacity reaches a specified point or the battery state changes.</span></span>

<span data-ttu-id="cca55-144">Todas as solicitações de informações da bateria serão concluídas com o status do **arquivo de erro \_ \_ não \_ encontrado** sempre que o elemento **BatteryTag** da solicitação não corresponder ao da marca da bateria atual.</span><span class="sxs-lookup"><span data-stu-id="cca55-144">All requests for battery information will complete with the status of **ERROR\_FILE\_NOT\_FOUND** whenever the **BatteryTag** element of the request does not match that of the current battery tag.</span></span> <span data-ttu-id="cca55-145">(Consulte [marcas de bateria](battery-information.md) para obter mais informações.) Isso é usado para garantir que as informações de bateria retornadas correspondam àquela da bateria solicitada.</span><span class="sxs-lookup"><span data-stu-id="cca55-145">(See [Battery Tags](battery-information.md) for more information.) This is used to ensure that the returned battery information matches that of the requested battery.</span></span>

<span data-ttu-id="cca55-146">Para as implicações da e/s sobreposta nessa operação, consulte a seção comentários do tópico [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="cca55-146">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="cca55-147">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cca55-147">Examples</span></span>

<span data-ttu-id="cca55-148">Para obter um exemplo, consulte [enumerando dispositivos de bateria](enumerating-battery-devices.md).</span><span class="sxs-lookup"><span data-stu-id="cca55-148">For an example, see [Enumerating Battery Devices](enumerating-battery-devices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cca55-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cca55-149">Requirements</span></span>



| <span data-ttu-id="cca55-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="cca55-150">Requirement</span></span> | <span data-ttu-id="cca55-151">Valor</span><span class="sxs-lookup"><span data-stu-id="cca55-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cca55-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cca55-152">Minimum supported client</span></span><br/> | <span data-ttu-id="cca55-153">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cca55-153">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="cca55-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cca55-154">Minimum supported server</span></span><br/> | <span data-ttu-id="cca55-155">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cca55-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="cca55-156">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cca55-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="cca55-157"><dt>Poclass. h; </dt> <dt>BatClass. h no Windows server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="cca55-157"><dt>Poclass.h; </dt> <dt>BatClass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cca55-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="cca55-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cca55-159">Informações da bateria</span><span class="sxs-lookup"><span data-stu-id="cca55-159">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="cca55-160">Códigos de controle de gerenciamento de energia</span><span class="sxs-lookup"><span data-stu-id="cca55-160">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="cca55-161">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="cca55-161">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="cca55-162">**STATUS da bateria \_**</span><span class="sxs-lookup"><span data-stu-id="cca55-162">**BATTERY\_STATUS**</span></span>](battery-status-str.md)
</dt> <dt>

[<span data-ttu-id="cca55-163">**\_status de espera da bateria \_**</span><span class="sxs-lookup"><span data-stu-id="cca55-163">**BATTERY\_WAIT\_STATUS**</span></span>](battery-wait-status-str.md)
</dt> <dt>

[<span data-ttu-id="cca55-164">**\_informações de \_ consulta da bateria do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="cca55-164">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> <dt>

[<span data-ttu-id="cca55-165">**\_marca de \_ consulta da bateria do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="cca55-165">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> <dt>

[<span data-ttu-id="cca55-166">**\_informações do \_ conjunto de baterias do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="cca55-166">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

