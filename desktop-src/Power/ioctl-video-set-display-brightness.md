---
description: Define os níveis atuais de luz de CA e CC.
ms.assetid: baa77811-046d-4a07-b3df-2a31fba2d9a7
title: IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS código de controle (Ntddvdeo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: a0c679f352012eea66b80335bc3ad1547501dd92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921723"
---
# <a name="ioctl_video_set_display_brightness-control-code"></a><span data-ttu-id="7262f-103">Conjunto de vídeos do IOCTL \_ \_ \_ Exibir \_ código de controle de brilho</span><span class="sxs-lookup"><span data-stu-id="7262f-103">IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS control code</span></span>

<span data-ttu-id="7262f-104">Define os níveis atuais de luz de CA e CC.</span><span class="sxs-lookup"><span data-stu-id="7262f-104">Sets the current AC and DC backlight levels.</span></span>

<span data-ttu-id="7262f-105">Para executar essa operação, chame a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="7262f-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to device
  IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS, // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of the input buffer
  NULL,                        // lpOutBuffer
  0,                           // nOutBufferSize 
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped  // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="7262f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7262f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7262f-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="7262f-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="7262f-108">Um identificador para o \\ \\ . \\ Dispositivo LCD.</span><span class="sxs-lookup"><span data-stu-id="7262f-108">A handle to the \\\\.\\LCD device.</span></span> <span data-ttu-id="7262f-109">Para recuperar um identificador de dispositivo, chame a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="7262f-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="7262f-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="7262f-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="7262f-111">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="7262f-111">The control code for the operation.</span></span> <span data-ttu-id="7262f-112">Esse valor identifica a operação específica a ser executada e o tipo de dispositivo no qual executá-lo.</span><span class="sxs-lookup"><span data-stu-id="7262f-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="7262f-113">Use **o \_ vídeo do IOCTL \_ definir \_ \_ brilho de vídeo** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="7262f-113">Use **IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="7262f-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="7262f-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="7262f-115">Um ponteiro para uma estrutura de [**\_ brilho de vídeo**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7262f-115">A pointer to a [**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7262f-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="7262f-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="7262f-117">O tamanho do buffer apontado por *lpOutBuffer*, em bytes.</span><span class="sxs-lookup"><span data-stu-id="7262f-117">The size of the buffer pointed to by *lpOutBuffer*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7262f-118">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="7262f-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="7262f-119">Não usado com esta operação; Defina como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="7262f-119">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7262f-120">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="7262f-120">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="7262f-121">Não usado com esta operação; definido como zero.</span><span class="sxs-lookup"><span data-stu-id="7262f-121">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="7262f-122">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="7262f-122">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="7262f-123">Um ponteiro para uma variável que recebe a contagem real de bytes retornados pela função no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="7262f-123">A pointer to a variable that receives the actual count of bytes returned by the function in the output buffer.</span></span>

<span data-ttu-id="7262f-124">Se *lpOverlapped* for **NULL** (e/s não sobreposta), *lpBytesReturned* será usado internamente e não poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="7262f-124">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* is used internally and cannot be **NULL**.</span></span>

<span data-ttu-id="7262f-125">Se *lpOverlapped* não for **nulo** (e/s sobreposta), *lpBytesReturned* poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="7262f-125">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7262f-126">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="7262f-126">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="7262f-127">Um ponteiro para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="7262f-127">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="7262f-128">Se *hDevice* tiver sido aberto com o \_ sinalizador sobreposto de sinalizador de arquivo \_ , *lpOverlapped* deverá apontar para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="7262f-128">If *hDevice* was opened with the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="7262f-129">Nesse caso, a operação é executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="7262f-129">In this case, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="7262f-130">Se o dispositivo tiver sido aberto com o \_ sinalizador sobreposto de sinalizador de arquivo \_ e *lpOverlapped* for **nulo**, a função falhará de maneiras imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="7262f-130">If the device was opened with the FILE\_FLAG\_OVERLAPPED flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="7262f-131">Se *hDevice* tiver sido aberto sem especificar o \_ sinalizador sobreposto do sinalizador de arquivo \_ , *lpOverlapped* será ignorado e [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) não retornará até que a operação seja concluída ou até que ocorra um erro.</span><span class="sxs-lookup"><span data-stu-id="7262f-131">If *hDevice* was opened without specifying the FILE\_FLAG\_OVERLAPPED flag, *lpOverlapped* is ignored and [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7262f-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7262f-132">Return value</span></span>

<span data-ttu-id="7262f-133">Se a operação for concluída com êxito, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="7262f-133">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="7262f-134">Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero.</span><span class="sxs-lookup"><span data-stu-id="7262f-134">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="7262f-135">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="7262f-135">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="7262f-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="7262f-136">Remarks</span></span>

<span data-ttu-id="7262f-137">Os valores especificados nos membros **ucACBrightness** e **ucDCBrightness** da estrutura de [**\_ brilho de vídeo**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) devem ter sido retornados anteriormente pelo [**\_ \_ \_ \_ brilho suportado pela consulta de vídeo do IOCTL**](ioctl-video-query-supported-brightness.md).</span><span class="sxs-lookup"><span data-stu-id="7262f-137">The values specified in the **ucACBrightness** and **ucDCBrightness** members of the [**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) structure must have been previously returned by [**IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS**](ioctl-video-query-supported-brightness.md).</span></span> <span data-ttu-id="7262f-138">Por exemplo, se os valores com suporte forem 10, 20, 30, 40, 50, 60, 70, 80, 90 e 100, o uso de um valor de 33 seria um erro.</span><span class="sxs-lookup"><span data-stu-id="7262f-138">For example, if the supported values are 10, 20, 30, 40, 50, 60, 70, 80, 90, and 100, then using a value of 33 would be an error.</span></span>

<span data-ttu-id="7262f-139">O arquivo de cabeçalho usado para criar aplicativos que incluem essa funcionalidade, Ntddvdeo. h, está incluído no Microsoft Windows Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="7262f-139">The header file used to build applications that include this functionality, Ntddvdeo.h, is included in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="7262f-140">Para obter informações sobre como obter o DDK, consulte [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .</span><span class="sxs-lookup"><span data-stu-id="7262f-140">For information on obtaining the DDK, see [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513).</span></span>

<span data-ttu-id="7262f-141">Como alternativa, você pode definir esse código de controle da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7262f-141">Alternatively, you can define this control code as follows:</span></span>

``` syntax
#define IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x127, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a><span data-ttu-id="7262f-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7262f-142">Requirements</span></span>



| <span data-ttu-id="7262f-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="7262f-143">Requirement</span></span> | <span data-ttu-id="7262f-144">Valor</span><span class="sxs-lookup"><span data-stu-id="7262f-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7262f-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7262f-145">Minimum supported client</span></span><br/> | <span data-ttu-id="7262f-146">Somente aplicativos do Windows Vista, Windows XP com SP1 para \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="7262f-146">Windows Vista, Windows XP with SP1 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="7262f-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7262f-147">Minimum supported server</span></span><br/> | <span data-ttu-id="7262f-148">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7262f-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7262f-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7262f-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="7262f-150"><dt>Ntddvdeo. h</dt></span><span class="sxs-lookup"><span data-stu-id="7262f-150"><dt>Ntddvdeo.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7262f-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="7262f-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7262f-152">Interface de controle de luz Invista</span><span class="sxs-lookup"><span data-stu-id="7262f-152">Backlight Control Interface</span></span>](backlight-control-interface.md)
</dt> <dt>

[<span data-ttu-id="7262f-153">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="7262f-153">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

<span data-ttu-id="7262f-154">[**brilho da tela \_**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7262f-154">[**DISPLAY\_BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7262f-155">**\_brilho de \_ exibição de consulta de vídeo do IOCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7262f-155">**IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS**</span></span>](ioctl-video-query-display-brightness.md)
</dt> <dt>

[<span data-ttu-id="7262f-156">**\_ \_ \_ brilho com suporte para consulta de vídeo do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="7262f-156">**IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS**</span></span>](ioctl-video-query-supported-brightness.md)
</dt> </dl>

 

