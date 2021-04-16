---
description: Recupera os níveis de luz de realce com suporte.
ms.assetid: b4c1ee3f-af75-477e-b7ed-53be905374d7
title: IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS código de controle (Ntddvdeo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: a5618ec29fd47ba690106b5f826e6fb145eac208
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757489"
---
# <a name="ioctl_video_query_supported_brightness-control-code"></a><span data-ttu-id="aeb51-103">\_Código de \_ controle de \_ brilho com suporte da consulta de vídeo do IOCTL \_</span><span class="sxs-lookup"><span data-stu-id="aeb51-103">IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS control code</span></span>

<span data-ttu-id="aeb51-104">Recupera os níveis de luz de realce com suporte.</span><span class="sxs-lookup"><span data-stu-id="aeb51-104">Retrieves the supported backlight levels.</span></span>

<span data-ttu-id="aeb51-105">Para executar essa operação, chame a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="aeb51-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS,  // dwIoControlCode
  NULL,                            // lpInBuffer
  0,                               // nInBufferSize
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="aeb51-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aeb51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aeb51-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="aeb51-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="aeb51-108">Um identificador para o \\ \\ . \\ Dispositivo LCD.</span><span class="sxs-lookup"><span data-stu-id="aeb51-108">A handle to the \\\\.\\LCD device.</span></span> <span data-ttu-id="aeb51-109">Para recuperar um identificador de dispositivo, chame a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="aeb51-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="aeb51-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="aeb51-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="aeb51-111">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="aeb51-111">The control code for the operation.</span></span> <span data-ttu-id="aeb51-112">Esse valor identifica a operação específica a ser executada e o tipo de dispositivo no qual executá-lo.</span><span class="sxs-lookup"><span data-stu-id="aeb51-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="aeb51-113">Use o **brilho de consulta de vídeo do IOCTL \_ \_ \_ com suporte \_** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="aeb51-113">Use **IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="aeb51-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="aeb51-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="aeb51-115">Não usado com esta operação; Defina como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="aeb51-115">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="aeb51-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="aeb51-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="aeb51-117">Não usado com esta operação; definido como zero.</span><span class="sxs-lookup"><span data-stu-id="aeb51-117">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="aeb51-118">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="aeb51-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="aeb51-119">Um ponteiro para um buffer que recebe uma matriz dos níveis de energia disponíveis.</span><span class="sxs-lookup"><span data-stu-id="aeb51-119">A pointer to a buffer that receives an array of the available power levels.</span></span> <span data-ttu-id="aeb51-120">Esse buffer deve ter 256 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="aeb51-120">This buffer should be 256 bytes long.</span></span>

</dd> <dt>

<span data-ttu-id="aeb51-121">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="aeb51-121">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="aeb51-122">O tamanho do buffer de saída em bytes.</span><span class="sxs-lookup"><span data-stu-id="aeb51-122">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="aeb51-123">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="aeb51-123">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="aeb51-124">Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados de saída retornados.</span><span class="sxs-lookup"><span data-stu-id="aeb51-124">A pointer to a variable that receives the size, in bytes, of output data returned.</span></span>

<span data-ttu-id="aeb51-125">Se o buffer de saída for muito pequeno para retornar dados, a chamada falhará, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o erro de código de erro \_ buffer insuficiente \_ e o número de bytes retornados será zero.</span><span class="sxs-lookup"><span data-stu-id="aeb51-125">If the output buffer is too small to return any data, then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_INSUFFICIENT\_BUFFER, and the returned byte count is zero.</span></span>

<span data-ttu-id="aeb51-126">Se o buffer de saída for muito pequeno para conter todos os dados, mas puder conter algumas entradas, o sistema operacional retornará o máximo que se ajustar, a chamada falhará, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o erro de código de erro com \_ mais \_ dados e *lpBytesReturned* indicará a quantidade de dados retornados.</span><span class="sxs-lookup"><span data-stu-id="aeb51-126">If the output buffer is too small to hold all of the data but can hold some entries, then the operating system returns as much as fits, the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_MORE\_DATA, and *lpBytesReturned* indicates the amount of data returned.</span></span> <span data-ttu-id="aeb51-127">Seu aplicativo deve chamar [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) novamente com a mesma operação, especificando um novo ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="aeb51-127">Your application should call [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) again with the same operation, specifying a new starting point.</span></span>

<span data-ttu-id="aeb51-128">Se *lpOverlapped* for **NULL** (e/s não sobreposta), *lpBytesReturned* não poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="aeb51-128">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="aeb51-129">Se *lpOverlapped* não for **nulo** (e/s sobreposta), *lpBytesReturned* poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="aeb51-129">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="aeb51-130">Se essa for uma operação sobreposta, você poderá recuperar o número de bytes retornados chamando a função [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="aeb51-130">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="aeb51-131">Se *hDevice* estiver associado a uma porta de conclusão de e/s, você poderá obter o número de bytes retornados chamando a função [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="aeb51-131">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="aeb51-132">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="aeb51-132">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="aeb51-133">Um ponteiro para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="aeb51-133">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="aeb51-134">Se *hDevice* tiver sido aberto com o \_ sinalizador sobreposto de sinalizador de arquivo \_ , *lpOverlapped* deverá apontar para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="aeb51-134">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="aeb51-135">Nesse caso, a operação é executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="aeb51-135">In this case, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="aeb51-136">Se o dispositivo tiver sido aberto com o \_ sinalizador sobreposto de sinalizador de arquivo \_ e *lpOverlapped* for **nulo**, a função falhará de maneiras imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="aeb51-136">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="aeb51-137">Se *hDevice* tiver sido aberto sem especificar o \_ sinalizador sobreposto do sinalizador de arquivo \_ , *lpOverlapped* será ignorado e [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) não retornará até que a operação seja concluída ou até que ocorra um erro.</span><span class="sxs-lookup"><span data-stu-id="aeb51-137">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aeb51-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aeb51-138">Return value</span></span>

<span data-ttu-id="aeb51-139">Se a operação for concluída com êxito, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="aeb51-139">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="aeb51-140">Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero.</span><span class="sxs-lookup"><span data-stu-id="aeb51-140">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="aeb51-141">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="aeb51-141">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="aeb51-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="aeb51-142">Remarks</span></span>

<span data-ttu-id="aeb51-143">Cada elemento na matriz *lpOutBuffer* tem um byte de comprimento.</span><span class="sxs-lookup"><span data-stu-id="aeb51-143">Each element in the *lpOutBuffer* array is one byte in length.</span></span> <span data-ttu-id="aeb51-144">Portanto, após o retorno, o parâmetro *lpBytesReturned* indica o número de níveis com suporte.</span><span class="sxs-lookup"><span data-stu-id="aeb51-144">Therefore, upon return, the *lpBytesReturned* parameter indicates the number of supported levels.</span></span> <span data-ttu-id="aeb51-145">Cada nível é um valor de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="aeb51-145">Each level is a value from 0 to 100.</span></span> <span data-ttu-id="aeb51-146">Quanto maior o valor, mais claro a luz.</span><span class="sxs-lookup"><span data-stu-id="aeb51-146">The larger the value, the brighter the backlight.</span></span> <span data-ttu-id="aeb51-147">Todos os níveis têm suporte se a fonte de energia for AC ou DC.</span><span class="sxs-lookup"><span data-stu-id="aeb51-147">All levels are supported whether the power source is AC or DC.</span></span>

<span data-ttu-id="aeb51-148">O arquivo de cabeçalho usado para criar aplicativos que incluem essa funcionalidade, Ntddvdeo. h, está incluído no Microsoft Windows Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="aeb51-148">The header file used to build applications that include this functionality, Ntddvdeo.h, is included in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="aeb51-149">Para obter informações sobre como obter o DDK, consulte [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .</span><span class="sxs-lookup"><span data-stu-id="aeb51-149">For information on obtaining the DDK, see [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513).</span></span>

<span data-ttu-id="aeb51-150">Como alternativa, você pode definir esse código de controle da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="aeb51-150">Alternatively, you can define this control code as follows:</span></span>

``` syntax
#define IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x125, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a><span data-ttu-id="aeb51-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aeb51-151">Requirements</span></span>



| <span data-ttu-id="aeb51-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="aeb51-152">Requirement</span></span> | <span data-ttu-id="aeb51-153">Valor</span><span class="sxs-lookup"><span data-stu-id="aeb51-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aeb51-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aeb51-154">Minimum supported client</span></span><br/> | <span data-ttu-id="aeb51-155">Somente aplicativos do Windows Vista, Windows XP com SP1 para \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="aeb51-155">Windows Vista, Windows XP with SP1 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="aeb51-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aeb51-156">Minimum supported server</span></span><br/> | <span data-ttu-id="aeb51-157">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aeb51-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aeb51-158">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aeb51-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="aeb51-159"><dt>Ntddvdeo. h</dt></span><span class="sxs-lookup"><span data-stu-id="aeb51-159"><dt>Ntddvdeo.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aeb51-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="aeb51-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeb51-161">Interface de controle de luz Invista</span><span class="sxs-lookup"><span data-stu-id="aeb51-161">Backlight Control Interface</span></span>](backlight-control-interface.md)
</dt> <dt>

[<span data-ttu-id="aeb51-162">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="aeb51-162">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

