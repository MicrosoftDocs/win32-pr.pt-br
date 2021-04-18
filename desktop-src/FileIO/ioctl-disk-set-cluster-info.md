---
description: Define as informações de cluster em um disco.
ms.assetid: AB2243D9-4913-4412-87E0-2C8DB8AB10B8
title: IOCTL_DISK_SET_CLUSTER_INFO código de controle (Ntdddisk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_SET_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: 4ba0994dd1c9030e84c22e24b1eb4583eba7e3d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766914"
---
# <a name="ioctl_disk_set_cluster_info-control-code"></a><span data-ttu-id="2e062-103">\_Código de \_ controle de informações do \_ cluster do conjunto de discos do IOCTL \_</span><span class="sxs-lookup"><span data-stu-id="2e062-103">IOCTL\_DISK\_SET\_CLUSTER\_INFO control code</span></span>

<span data-ttu-id="2e062-104">Define as informações de cluster em um disco.</span><span class="sxs-lookup"><span data-stu-id="2e062-104">Sets the cluster information on a disk.</span></span>

<span data-ttu-id="2e062-105">Para executar essa operação, chame a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="2e062-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_SET_CLUSTER_INFO,    // dwIoControlCode
                 (LPVOID)       NULL,            // lpInBuffer 
                 (DWORD)        0,               // nInBufferSize 
                 (LPVOID)       lpOutBuffer,     // output buffer:GET_DISK_ATTRIBUTES
                 (DWORD)        nOutBufferSize,  // size of output buffer
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="2e062-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e062-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e062-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="2e062-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="2e062-108">Um identificador para o disco.</span><span class="sxs-lookup"><span data-stu-id="2e062-108">A handle to the disk.</span></span>

<span data-ttu-id="2e062-109">Para recuperar um identificador de dispositivo, chame a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="2e062-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="2e062-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="2e062-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="2e062-111">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="2e062-111">The control code for the operation.</span></span>

<span data-ttu-id="2e062-112">Use **as \_ \_ informações do \_ cluster \_ do conjunto de discos do IOCTL** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="2e062-112">Use **IOCTL\_DISK\_SET\_CLUSTER\_INFO** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="2e062-113">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="2e062-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="2e062-114">Um ponteiro para uma estrutura de dados de [**\_ \_ informações de cluster de disco**](disk-cluster-info.md) que contém informações de cluster para o disco.</span><span class="sxs-lookup"><span data-stu-id="2e062-114">A pointer to a [**DISK\_CLUSTER\_INFO**](disk-cluster-info.md) data structure that contains cluster information for the disk.</span></span>

</dd> <dt>

<span data-ttu-id="2e062-115">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="2e062-115">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="2e062-116">O tamanho do buffer de entrada, em bytes.</span><span class="sxs-lookup"><span data-stu-id="2e062-116">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2e062-117">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="2e062-117">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="2e062-118">Não usado com esta operação.</span><span class="sxs-lookup"><span data-stu-id="2e062-118">Not used with this operation.</span></span> <span data-ttu-id="2e062-119">Defina como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="2e062-119">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2e062-120">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="2e062-120">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="2e062-121">O tamanho do buffer de saída em bytes.</span><span class="sxs-lookup"><span data-stu-id="2e062-121">The size of the output buffer, in bytes.</span></span> <span data-ttu-id="2e062-122">Defina como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="2e062-122">Set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="2e062-123">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="2e062-123">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="2e062-124">Não usado com esta operação.</span><span class="sxs-lookup"><span data-stu-id="2e062-124">Not used with this operation.</span></span> <span data-ttu-id="2e062-125">Defina como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="2e062-125">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2e062-126">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="2e062-126">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="2e062-127">Um ponteiro para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="2e062-127">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="2e062-128">Se *hDevice* tiver sido aberto sem especificar o **sinalizador de arquivo \_ \_ sobreposto**, *lpOverlapped* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="2e062-128">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="2e062-129">Se *hDevice* tiver sido aberto com o sinalizador de **sinalizador de arquivo \_ \_ sobreposto** , a operação será executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="2e062-129">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="2e062-130">Nesse caso, *lpOverlapped* deve apontar para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida que contém um identificador para um objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="2e062-130">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="2e062-131">Caso contrário, a função falhará de maneiras imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="2e062-131">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="2e062-132">Para operações sobrepostas, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retorna imediatamente e o objeto de evento é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="2e062-132">For overlapped operations, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="2e062-133">Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.</span><span class="sxs-lookup"><span data-stu-id="2e062-133">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e062-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2e062-134">Return value</span></span>

<span data-ttu-id="2e062-135">Se a operação for concluída com êxito, indicando que todos os volumes no disco estão prontos para uso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="2e062-135">If the operation completes successfully, indicating that all volumes on the disk are ready for use, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="2e062-136">Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero.</span><span class="sxs-lookup"><span data-stu-id="2e062-136">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="2e062-137">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="2e062-137">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e062-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e062-138">Requirements</span></span>



| <span data-ttu-id="2e062-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e062-139">Requirement</span></span> | <span data-ttu-id="2e062-140">Valor</span><span class="sxs-lookup"><span data-stu-id="2e062-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e062-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e062-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2e062-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2e062-142">None supported</span></span><br/>                                                             |
| <span data-ttu-id="2e062-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e062-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2e062-144">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2e062-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e062-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2e062-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e062-146"><dt>Ntdddisk. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e062-146"><dt>Ntdddisk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e062-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e062-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e062-148">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="2e062-148">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="2e062-149">Códigos de controle de gerenciamento de disco</span><span class="sxs-lookup"><span data-stu-id="2e062-149">Disk Management Control Codes</span></span>](disk-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="2e062-150">**\_informações de cluster de disco \_**</span><span class="sxs-lookup"><span data-stu-id="2e062-150">**DISK\_CLUSTER\_INFO**</span></span>](disk-cluster-info.md)
</dt> <dt>

[<span data-ttu-id="2e062-151">**\_informações do \_ cluster de obtenção de disco de IOCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2e062-151">**IOCTL\_DISK\_GET\_CLUSTER\_INFO**</span></span>](ioctl-disk-get-cluster-info.md)
</dt> </dl>

 

