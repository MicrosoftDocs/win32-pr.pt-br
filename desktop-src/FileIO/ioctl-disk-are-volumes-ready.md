---
description: Aguarda que todos os volumes no disco especificado estejam prontos para uso.
ms.assetid: 6cf619bb-7ff5-485e-b533-0f7f6503c6e0
title: IOCTL_DISK_ARE_VOLUMES_READY código de controle (Ntdddisk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_ARE_VOLUMES_READY
api_type:
- HeaderDef
api_location:
- ntdddisk.h
ms.openlocfilehash: dc4457af2ce6e7759ef879900803504933a09978
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782821"
---
# <a name="ioctl_disk_are_volumes_ready-control-code"></a><span data-ttu-id="9aa81-103">O \_ disco de IOCTL \_ é um código de \_ \_ controle pronto para volumes</span><span class="sxs-lookup"><span data-stu-id="9aa81-103">IOCTL\_DISK\_ARE\_VOLUMES\_READY control code</span></span>

<span data-ttu-id="9aa81-104">Aguarda que todos os volumes no disco especificado estejam prontos para uso.</span><span class="sxs-lookup"><span data-stu-id="9aa81-104">Waits for all volumes on the specified disk to be ready for use.</span></span>

<span data-ttu-id="9aa81-105">Para executar essa operação, chame a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="9aa81-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_ARE_VOLUMES_READY,   // dwIoControlCode
                 (LPVOID)       NULL,            // lpInBuffer 
                 (DWORD)        0,               // nInBufferSize 
                 (LPVOID)       NULL,            // lpOutBuffer 
                 (DWORD)        0,               // nOutBufferSize
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="9aa81-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9aa81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aa81-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="9aa81-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="9aa81-108">Um identificador para o disco.</span><span class="sxs-lookup"><span data-stu-id="9aa81-108">A handle to the disk.</span></span>

<span data-ttu-id="9aa81-109">Para recuperar um identificador de dispositivo, chame a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="9aa81-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="9aa81-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="9aa81-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="9aa81-111">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="9aa81-111">The control code for the operation.</span></span>

<span data-ttu-id="9aa81-112">Usar **o \_ disco de IOCTL são os \_ \_ volumes \_ prontos** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="9aa81-112">Use **IOCTL\_DISK\_ARE\_VOLUMES\_READY** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="9aa81-113">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="9aa81-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="9aa81-114">Não usado com esta operação.</span><span class="sxs-lookup"><span data-stu-id="9aa81-114">Not used with this operation.</span></span> <span data-ttu-id="9aa81-115">Defina como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="9aa81-115">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9aa81-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="9aa81-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="9aa81-117">O tamanho do buffer de entrada, em bytes.</span><span class="sxs-lookup"><span data-stu-id="9aa81-117">The size of the input buffer, in bytes.</span></span> <span data-ttu-id="9aa81-118">Defina como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="9aa81-118">Set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="9aa81-119">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="9aa81-119">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="9aa81-120">Não usado com esta operação.</span><span class="sxs-lookup"><span data-stu-id="9aa81-120">Not used with this operation.</span></span> <span data-ttu-id="9aa81-121">Defina como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="9aa81-121">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9aa81-122">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="9aa81-122">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="9aa81-123">Não usado com esta operação.</span><span class="sxs-lookup"><span data-stu-id="9aa81-123">Not used with this operation.</span></span> <span data-ttu-id="9aa81-124">Defina como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="9aa81-124">Set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="9aa81-125">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="9aa81-125">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="9aa81-126">Não usado com esta operação.</span><span class="sxs-lookup"><span data-stu-id="9aa81-126">Not used with this operation.</span></span> <span data-ttu-id="9aa81-127">Defina como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="9aa81-127">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9aa81-128">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="9aa81-128">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="9aa81-129">Um ponteiro para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="9aa81-129">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="9aa81-130">Se *hDevice* tiver sido aberto sem especificar o **sinalizador de arquivo \_ \_ sobreposto**, *lpOverlapped* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="9aa81-130">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="9aa81-131">Se *hDevice* tiver sido aberto com o sinalizador de **sinalizador de arquivo \_ \_ sobreposto** , a operação será executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="9aa81-131">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="9aa81-132">Nesse caso, *lpOverlapped* deve apontar para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida que contém um identificador para um objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="9aa81-132">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="9aa81-133">Caso contrário, a função falhará de maneiras imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="9aa81-133">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="9aa81-134">Para operações sobrepostas, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retorna imediatamente e o objeto de evento é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="9aa81-134">For overlapped operations, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="9aa81-135">Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.</span><span class="sxs-lookup"><span data-stu-id="9aa81-135">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aa81-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9aa81-136">Return value</span></span>

<span data-ttu-id="9aa81-137">Se a operação for concluída com êxito, indicando que todos os volumes no disco estão prontos para uso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="9aa81-137">If the operation completes successfully, indicating that all volumes on the disk are ready for use, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="9aa81-138">Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero.</span><span class="sxs-lookup"><span data-stu-id="9aa81-138">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="9aa81-139">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="9aa81-139">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="9aa81-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9aa81-140">Requirements</span></span>



| <span data-ttu-id="9aa81-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="9aa81-141">Requirement</span></span> | <span data-ttu-id="9aa81-142">Valor</span><span class="sxs-lookup"><span data-stu-id="9aa81-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9aa81-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9aa81-143">Minimum supported client</span></span><br/> | <span data-ttu-id="9aa81-144">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9aa81-144">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9aa81-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9aa81-145">Minimum supported server</span></span><br/> | <span data-ttu-id="9aa81-146">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9aa81-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9aa81-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9aa81-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="9aa81-148"><dt>Ntdddisk. h</dt></span><span class="sxs-lookup"><span data-stu-id="9aa81-148"><dt>Ntdddisk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9aa81-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="9aa81-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aa81-150">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="9aa81-150">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="9aa81-151">Códigos de controle de gerenciamento de disco</span><span class="sxs-lookup"><span data-stu-id="9aa81-151">Disk Management Control Codes</span></span>](disk-management-control-codes.md)
</dt> </dl>

 

