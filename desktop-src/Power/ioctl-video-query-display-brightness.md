---
description: Recupera os níveis atuais de luz de CA e CC e o estado de energia atual.
ms.assetid: c7b7c302-6e92-46a7-b9a6-e3f2a3e44d1b
title: IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS código de controle (Ntddvdeo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: 547501a28492aecfe06f63f95b0e007fc80d3d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812886"
---
# <a name="ioctl_video_query_display_brightness-control-code"></a><span data-ttu-id="b39f2-103">\_Código de \_ controle de brilho de \_ exibição de consulta de vídeo do IOCTL \_</span><span class="sxs-lookup"><span data-stu-id="b39f2-103">IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS control code</span></span>

<span data-ttu-id="b39f2-104">\[Esse código de controle está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="b39f2-104">\[This control code is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b39f2-105">O suporte para esse código de controle foi removido do Windows Server 2008 e do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b39f2-105">Support for this control code was removed in Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="b39f2-106">Em vez disso, use a classe [**WmiMonitorBrightness**](/windows/desktop/WmiCoreProv/wmimonitorbrightness) .\]</span><span class="sxs-lookup"><span data-stu-id="b39f2-106">Use the [**WmiMonitorBrightness**](/windows/desktop/WmiCoreProv/wmimonitorbrightness) class instead.\]</span></span>

<span data-ttu-id="b39f2-107">Recupera os níveis atuais de luz de CA e CC e o estado de energia atual.</span><span class="sxs-lookup"><span data-stu-id="b39f2-107">Retrieves the current AC and DC backlight levels and the current power state.</span></span>

<span data-ttu-id="b39f2-108">Para executar essa operação, chame a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="b39f2-108">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS,  // dwIoControlCode
  NULL,                            // lpInBuffer
  0,                               // nInBufferSize
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="b39f2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b39f2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b39f2-110">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="b39f2-110">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="b39f2-111">Um identificador para o \\ \\ . \\ Dispositivo LCD.</span><span class="sxs-lookup"><span data-stu-id="b39f2-111">A handle to the \\\\.\\LCD device.</span></span> <span data-ttu-id="b39f2-112">Para recuperar um identificador de dispositivo, chame a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="b39f2-112">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="b39f2-113">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="b39f2-113">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="b39f2-114">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="b39f2-114">The control code for the operation.</span></span> <span data-ttu-id="b39f2-115">Esse valor identifica a operação específica a ser executada e o tipo de dispositivo no qual executá-lo.</span><span class="sxs-lookup"><span data-stu-id="b39f2-115">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="b39f2-116">Use **o \_ \_ brilho de \_ exibição \_ da consulta de vídeo do IOCTL** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="b39f2-116">Use **IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="b39f2-117">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="b39f2-117">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="b39f2-118">Não usado com esta operação; Defina como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b39f2-118">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b39f2-119">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="b39f2-119">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="b39f2-120">Não usado com esta operação; definido como zero.</span><span class="sxs-lookup"><span data-stu-id="b39f2-120">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="b39f2-121">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="b39f2-121">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="b39f2-122">Um ponteiro para um buffer que receberá uma estrutura de [**\_ brilho de vídeo**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b39f2-122">A pointer to a buffer that will receive a [**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b39f2-123">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="b39f2-123">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="b39f2-124">O tamanho do buffer de saída em bytes.</span><span class="sxs-lookup"><span data-stu-id="b39f2-124">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b39f2-125">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="b39f2-125">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="b39f2-126">Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados de saída retornados.</span><span class="sxs-lookup"><span data-stu-id="b39f2-126">A pointer to a variable that receives the size, in bytes, of output data returned.</span></span>

<span data-ttu-id="b39f2-127">Se o buffer de saída for muito pequeno para retornar dados, a chamada falhará, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o erro de código de erro \_ buffer insuficiente \_ e o número de bytes retornados será zero.</span><span class="sxs-lookup"><span data-stu-id="b39f2-127">If the output buffer is too small to return any data, then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_INSUFFICIENT\_BUFFER, and the returned byte count is zero.</span></span>

<span data-ttu-id="b39f2-128">Se o buffer de saída for muito pequeno para conter todos os dados, mas puder conter algumas entradas, o sistema operacional retornará o máximo que se ajustar, a chamada falhará, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o erro de código de erro com \_ mais \_ dados e *lpBytesReturned* indicará a quantidade de dados retornados.</span><span class="sxs-lookup"><span data-stu-id="b39f2-128">If the output buffer is too small to hold all of the data but can hold some entries, then the operating system returns as much as fits, the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code ERROR\_MORE\_DATA, and *lpBytesReturned* indicates the amount of data returned.</span></span> <span data-ttu-id="b39f2-129">Seu aplicativo deve chamar [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) novamente com a mesma operação, especificando um novo ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="b39f2-129">Your application should call [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) again with the same operation, specifying a new starting point.</span></span>

<span data-ttu-id="b39f2-130">Se *lpOverlapped* for **NULL** (e/s não sobreposta), *lpBytesReturned* não poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b39f2-130">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="b39f2-131">Se *lpOverlapped* não for **nulo** (e/s sobreposta), *lpBytesReturned* poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b39f2-131">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="b39f2-132">Se essa for uma operação sobreposta, você poderá recuperar o número de bytes retornados chamando a função [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="b39f2-132">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="b39f2-133">Se *hDevice* estiver associado a uma porta de conclusão de e/s, você poderá obter o número de bytes retornados chamando a função [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="b39f2-133">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="b39f2-134">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="b39f2-134">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="b39f2-135">Um ponteiro para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="b39f2-135">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="b39f2-136">Se *hDevice* tiver sido aberto com o \_ sinalizador sobreposto de sinalizador de arquivo \_ , *lpOverlapped* deverá apontar para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="b39f2-136">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="b39f2-137">Nesse caso, a operação é executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="b39f2-137">In this case, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="b39f2-138">Se o dispositivo tiver sido aberto com o \_ sinalizador sobreposto de sinalizador de arquivo \_ e *lpOverlapped* for **nulo**, a função falhará de maneiras imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="b39f2-138">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="b39f2-139">Se *hDevice* tiver sido aberto sem especificar o \_ sinalizador sobreposto do sinalizador de arquivo \_ , *lpOverlapped* será ignorado e [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) não retornará até que a operação seja concluída ou até que ocorra um erro.</span><span class="sxs-lookup"><span data-stu-id="b39f2-139">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b39f2-140">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b39f2-140">Return value</span></span>

<span data-ttu-id="b39f2-141">Se a operação for concluída com êxito, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="b39f2-141">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="b39f2-142">Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero.</span><span class="sxs-lookup"><span data-stu-id="b39f2-142">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="b39f2-143">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="b39f2-143">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="b39f2-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="b39f2-144">Remarks</span></span>

<span data-ttu-id="b39f2-145">O arquivo de cabeçalho usado para criar aplicativos que incluem essa funcionalidade, Ntddvdeo. h, está incluído no Microsoft Windows Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="b39f2-145">The header file used to build applications that include this functionality, Ntddvdeo.h, is included in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="b39f2-146">Para obter informações sobre como obter o DDK, consulte [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .</span><span class="sxs-lookup"><span data-stu-id="b39f2-146">For information on obtaining the DDK, see [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513).</span></span>

<span data-ttu-id="b39f2-147">Como alternativa, você pode definir esse código de controle da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b39f2-147">Alternatively, you can define this control code as follows:</span></span>

``` syntax
#define IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x126, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a><span data-ttu-id="b39f2-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b39f2-148">Requirements</span></span>



| <span data-ttu-id="b39f2-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="b39f2-149">Requirement</span></span> | <span data-ttu-id="b39f2-150">Valor</span><span class="sxs-lookup"><span data-stu-id="b39f2-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b39f2-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b39f2-151">Minimum supported client</span></span><br/> | <span data-ttu-id="b39f2-152">\[Somente aplicativos da área de trabalho do Windows XP com SP1\]</span><span class="sxs-lookup"><span data-stu-id="b39f2-152">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b39f2-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b39f2-153">Minimum supported server</span></span><br/> | <span data-ttu-id="b39f2-154">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b39f2-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b39f2-155">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b39f2-155">End of client support</span></span><br/>    | <span data-ttu-id="b39f2-156">Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="b39f2-156">Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="b39f2-157">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="b39f2-157">End of server support</span></span><br/>    | <span data-ttu-id="b39f2-158">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b39f2-158">Windows Server 2003 R2</span></span><br/>                                                     |
| <span data-ttu-id="b39f2-159">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b39f2-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="b39f2-160"><dt>Ntddvdeo. h</dt></span><span class="sxs-lookup"><span data-stu-id="b39f2-160"><dt>Ntddvdeo.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b39f2-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="b39f2-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b39f2-162">Interface de controle de luz Invista</span><span class="sxs-lookup"><span data-stu-id="b39f2-162">Backlight Control Interface</span></span>](backlight-control-interface.md)
</dt> <dt>

[<span data-ttu-id="b39f2-163">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="b39f2-163">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

<span data-ttu-id="b39f2-164">[**brilho da tela \_**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b39f2-164">[**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b39f2-165">**vídeo do IOCTL \_ \_ definir \_ brilho de vídeo \_**</span><span class="sxs-lookup"><span data-stu-id="b39f2-165">**IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS**</span></span>](ioctl-video-set-display-brightness.md)
</dt> </dl>

 

