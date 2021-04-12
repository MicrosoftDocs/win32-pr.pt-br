---
description: O \_ código de controle da obtenção de atributos do \_ NFS \_ consulta informações adicionais sobre um compartilhamento NFS.
ms.assetid: BC9E0E19-7D78-4AE7-A3E6-9FD9212B2B83
title: DA_GET_NFS_ATTRIBUTES código de controle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DA_GET_NFS_ATTRIBUTES
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4427dd48190bd12f7837c4841a98e15f7ddaff5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500880"
---
# <a name="da_get_nfs_attributes-control-code"></a><span data-ttu-id="e213c-103">\_Código de controle da obtenção de \_ \_ atributos NFS</span><span class="sxs-lookup"><span data-stu-id="e213c-103">DA\_GET\_NFS\_ATTRIBUTES control code</span></span>

<span data-ttu-id="e213c-104">O código de controle da **\_ obtenção de \_ \_ atributos do NFS** consulta informações adicionais sobre um compartilhamento NFS.</span><span class="sxs-lookup"><span data-stu-id="e213c-104">The **DA\_GET\_NFS\_ATTRIBUTES** control code queries additional information about an NFS share.</span></span>

<span data-ttu-id="e213c-105">Para executar essa operação, chame a função [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="e213c-105">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,               // handle to device
                    (DWORD)        DA_GET_NFS_ATTRIBUTES, // dwIoControlCode
                                   NULL,                  // lpInBuffer
                                   0,                     // nInBufferSize
                    (LPDWORD)      lpOutBuffer,           // output buffer
                    (DWORD)        nOutBufferSize,        // size of output buffer
                    (LPDWORD)      lpBytesReturned,       // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );        // OVERLAPPED structure
```



## <a name="parameters"></a><span data-ttu-id="e213c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e213c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e213c-107">*hDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e213c-107">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e213c-108">Um identificador para um arquivo no compartilhamento NFS.</span><span class="sxs-lookup"><span data-stu-id="e213c-108">A handle to a file on the NFS share.</span></span> <span data-ttu-id="e213c-109">Para obter esse identificador, chame a função [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="e213c-109">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="e213c-110">*dwIoControlCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e213c-110">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e213c-111">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="e213c-111">The control code for the operation.</span></span> <span data-ttu-id="e213c-112">Use **\_ \_ \_ atributos de obter NFS** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="e213c-112">Use **DA\_GET\_NFS\_ATTRIBUTES** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="e213c-113">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="e213c-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="e213c-114">Não usado com esta operação; Defina como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e213c-114">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e213c-115">*nInBufferSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e213c-115">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e213c-116">Não usado com esta operação; definido como zero.</span><span class="sxs-lookup"><span data-stu-id="e213c-116">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="e213c-117">*lpOutBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e213c-117">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e213c-118">Um ponteiro para o buffer de saída, que contém uma estrutura de **\_ \_ atributos de arquivo NFS** .</span><span class="sxs-lookup"><span data-stu-id="e213c-118">A pointer to the output buffer, which contains an **NFS\_FILE\_ATTRIBUTES** structure.</span></span> <span data-ttu-id="e213c-119">Para obter mais informações, consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="e213c-119">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="e213c-120">*nOutBufferSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e213c-120">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e213c-121">O tamanho do buffer de saída em bytes.</span><span class="sxs-lookup"><span data-stu-id="e213c-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e213c-122">*lpBytesReturned* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e213c-122">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e213c-123">Um ponteiro para uma variável que recebe o tamanho dos dados armazenados no buffer de saída, em bytes.</span><span class="sxs-lookup"><span data-stu-id="e213c-123">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="e213c-124">Se o buffer de saída for muito pequeno, a chamada falhará, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará um **erro de \_ \_ buffer insuficiente** e *lpBytesReturned* será zero.</span><span class="sxs-lookup"><span data-stu-id="e213c-124">If the output buffer is too small, the call fails, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="e213c-125">Se *lpOverlapped* for **nulo**, *lpBytesReturned* não poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e213c-125">If *lpOverlapped* is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="e213c-126">Mesmo quando uma operação não retorna dados de saída e *lpOutBuffer* é **nula**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) faz uso de *lpBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="e213c-126">Even when an operation returns no output data and *lpOutBuffer* is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="e213c-127">Após tal operação, o valor de *lpBytesReturned* é inútil.</span><span class="sxs-lookup"><span data-stu-id="e213c-127">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="e213c-128">Se *lpOverlapped* não for **nulo**, *lpBytesReturned* poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e213c-128">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="e213c-129">Se esse parâmetro não for **nulo** e a operação retornar dados, *lpBytesReturned* será inútil até que a operação sobreposta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="e213c-129">If this parameter is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="e213c-130">Para recuperar o número de bytes retornados, chame [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult).</span><span class="sxs-lookup"><span data-stu-id="e213c-130">To retrieve the number of bytes returned, call [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult).</span></span> <span data-ttu-id="e213c-131">Se o parâmetro *hDevice* estiver associado a uma porta de conclusão de e/s, você poderá recuperar o número de bytes retornados chamando [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span><span class="sxs-lookup"><span data-stu-id="e213c-131">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span></span>

</dd> <dt>

<span data-ttu-id="e213c-132">*lpOverlapped* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e213c-132">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e213c-133">Um ponteiro para uma estrutura [**sobreposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="e213c-133">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="e213c-134">Se *hDevice* tiver sido aberto sem especificar o **sinalizador de arquivo \_ \_ sobreposto**, *lpOverlapped* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="e213c-134">If *hDevice* was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="e213c-135">Se *hDevice* tiver sido aberto com o sinalizador de **sinalizador de arquivo \_ \_ sobreposto** , a operação será executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="e213c-135">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="e213c-136">Nesse caso, *lpOverlapped* deve apontar para uma estrutura [**sobreposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) válida que contém um identificador para um objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="e213c-136">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="e213c-137">Caso contrário, a função falhará de maneiras imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="e213c-137">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="e213c-138">Para operações sobrepostas, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retorna imediatamente e o objeto de evento é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="e213c-138">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="e213c-139">Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.</span><span class="sxs-lookup"><span data-stu-id="e213c-139">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e213c-140">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e213c-140">Return value</span></span>

<span data-ttu-id="e213c-141">Se a operação for concluída com êxito, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="e213c-141">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="e213c-142">Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero.</span><span class="sxs-lookup"><span data-stu-id="e213c-142">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="e213c-143">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="e213c-143">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="e213c-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="e213c-144">Remarks</span></span>

<span data-ttu-id="e213c-145">Este código de controle não tem nenhum arquivo de cabeçalho associado.</span><span class="sxs-lookup"><span data-stu-id="e213c-145">This control code has no associated header file.</span></span> <span data-ttu-id="e213c-146">Você deve definir o código de controle e as estruturas de dados da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="e213c-146">You must define the control code and data structures as follows.</span></span>

``` syntax
#define DEVICE_DA_RDR 0x80000  
 
#define DA_GET_NFS_ATTRIBUTES CTL_CODE(DEVICE_DA_RDR, 0x804, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _NFS_SPEC_DATA {  
    ULONG               SpecData1;
    ULONG               SpecData2;
} NFS_SPEC_DATA, *PNFS_SPEC_DATA;

typedef struct _NFS_TIME {
    ULONG        Seconds;
    ULONG        nSeconds;
} NFS_TIME, *PNFS_TIME;

#define NFS_TYPE_REG         1
#define NFS_TYPE_DIR         2
#define NFS_TYPE_BLK         3
#define NFS_TYPE_CHR         4
#define NFS_TYPE_LNK         5
#define NFS_TYPE_SOCK        6
#define NFS_TYPE_FIFO        7

typedef struct _NFS_FILE_ATTRIBUTES {  
    ULONG               FileType;  
    ULONG               Mode;  
    ULONG               NLink;  
    ULONG               Uid;  
    ULONG               Gid;  
    ULONGLONG           Size;  
    ULONGLONG           Used;
    NFS_SPEC_DATA       Rdev;
    ULONGLONG           Fsid;  
    ULONGLONG           FileId;  
    NFS_TIME            AccessTime;  
    NFS_TIME            ModifyTime;  
    NFS_TIME            ChangeTime;  
} NFS_FILE_ATTRIBUTES, *PNFS_FILE_ATTRIBUTES;

typedef struct _DA_FILE_ATTRIBUTES {  
    NFS_FILE_ATTRIBUTES FileAttributes;  
    ULONG               Version;  
} DA_FILE_ATTRIBUTES, *PDA_FILE_ATTRIBUTES;
```

<span data-ttu-id="e213c-147">Os membros da estrutura podem ser descritos da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="e213c-147">The structure members can be described as follows.</span></span>

<dl> <dt>

<span data-ttu-id="e213c-148"><span id="SpecData1"></span><span id="specdata1"></span><span id="SPECDATA1"></span>**SpecData1**</span><span class="sxs-lookup"><span data-stu-id="e213c-148"><span id="SpecData1"></span><span id="specdata1"></span><span id="SPECDATA1"></span>**SpecData1**</span></span>
</dt> <dd>

<span data-ttu-id="e213c-149">Um valor opaco que é usado para tipos de arquivo especiais, como arquivos de bloco especial, caracteres especiais e FIFO.</span><span class="sxs-lookup"><span data-stu-id="e213c-149">An opaque value that is used for special file types such as block-special, character-special and FIFO files.</span></span>

</dd> <dt>

<span data-ttu-id="e213c-150"><span id="SpecData2"></span><span id="specdata2"></span><span id="SPECDATA2"></span>**SpecData2**</span><span class="sxs-lookup"><span data-stu-id="e213c-150"><span id="SpecData2"></span><span id="specdata2"></span><span id="SPECDATA2"></span>**SpecData2**</span></span>
</dt> <dd>

<span data-ttu-id="e213c-151">Um valor opaco que é usado para tipos de arquivo especiais, como arquivos de bloco especial, caracteres especiais e FIFO.</span><span class="sxs-lookup"><span data-stu-id="e213c-151">An opaque value that is used for special file types such as block-special, character-special and FIFO files.</span></span>

</dd> <dt>

<span data-ttu-id="e213c-152"><span id="Seconds"></span><span id="seconds"></span><span id="SECONDS"></span>**Seg**</span><span class="sxs-lookup"><span data-stu-id="e213c-152"><span id="Seconds"></span><span id="seconds"></span><span id="SECONDS"></span>**Seconds**</span></span>
</dt> <dd>

<span data-ttu-id="e213c-153">Um valor de 64 bits que representa os segundos desde 1º de janeiro de 1970 (UTC).</span><span class="sxs-lookup"><span data-stu-id="e213c-153">A 64-bit value representing the seconds since January 1, 1970 (UTC).</span></span>

</dd> <dt>

<span data-ttu-id="e213c-154"><span id="nSeconds"></span><span id="nseconds"></span><span id="NSECONDS"></span>**nSeconds**</span><span class="sxs-lookup"><span data-stu-id="e213c-154"><span id="nSeconds"></span><span id="nseconds"></span><span id="NSECONDS"></span>**nSeconds**</span></span>
</dt> <dd>

<span data-ttu-id="e213c-155">O número de nanossegundos a ser adicionado ao membro de **segundos** .</span><span class="sxs-lookup"><span data-stu-id="e213c-155">The number of nanoseconds to be added to the **Seconds** member.</span></span>

</dd> <dt>

<span data-ttu-id="e213c-156"><span id="FileType"></span><span id="filetype"></span><span id="FILETYPE"></span>**Talvez**</span><span class="sxs-lookup"><span data-stu-id="e213c-156"><span id="FileType"></span><span id="filetype"></span><span id="FILETYPE"></span>**FileType**</span></span>
</dt> <dd>

<span data-ttu-id="e213c-157">O tipo de arquivo NFS do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="e213c-157">The NFS file type of the share.</span></span>



| <span data-ttu-id="e213c-158">Tipo de arquivo NFS</span><span class="sxs-lookup"><span data-stu-id="e213c-158">NFS File Type</span></span>                                                                              | <span data-ttu-id="e213c-159">Descrição</span><span class="sxs-lookup"><span data-stu-id="e213c-159">Description</span></span>                          |
|--------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="e213c-160"><span id="NFS_TYPE_REG"></span><span id="nfs_type_reg"></span>tipo de NFS \_ \_ reg</span><span class="sxs-lookup"><span data-stu-id="e213c-160"><span id="NFS_TYPE_REG"></span><span id="nfs_type_reg"></span>NFS\_TYPE\_REG</span></span><br/>    | <span data-ttu-id="e213c-161">Um arquivo regular.</span><span class="sxs-lookup"><span data-stu-id="e213c-161">A regular file.</span></span><br/>           |
| <span data-ttu-id="e213c-162"><span id="NFS_TYPE_DIR"></span><span id="nfs_type_dir"></span>Dir. de \_ tipo NFS \_</span><span class="sxs-lookup"><span data-stu-id="e213c-162"><span id="NFS_TYPE_DIR"></span><span id="nfs_type_dir"></span>NFS\_TYPE\_DIR</span></span><br/>    | <span data-ttu-id="e213c-163">Um diretório.</span><span class="sxs-lookup"><span data-stu-id="e213c-163">A directory.</span></span><br/>              |
| <span data-ttu-id="e213c-164"><span id="NFS_TYPE_BLK"></span><span id="nfs_type_blk"></span>tipo de NFS \_ \_ BLK</span><span class="sxs-lookup"><span data-stu-id="e213c-164"><span id="NFS_TYPE_BLK"></span><span id="nfs_type_blk"></span>NFS\_TYPE\_BLK</span></span><br/>    | <span data-ttu-id="e213c-165">Um arquivo especial de bloco.</span><span class="sxs-lookup"><span data-stu-id="e213c-165">A block-special file.</span></span><br/>     |
| <span data-ttu-id="e213c-166"><span id="NFS_TYPE_CHR"></span><span id="nfs_type_chr"></span>tipo de NFS \_ \_ Chr</span><span class="sxs-lookup"><span data-stu-id="e213c-166"><span id="NFS_TYPE_CHR"></span><span id="nfs_type_chr"></span>NFS\_TYPE\_CHR</span></span><br/>    | <span data-ttu-id="e213c-167">Um arquivo de caractere especial.</span><span class="sxs-lookup"><span data-stu-id="e213c-167">A character-special file.</span></span><br/> |
| <span data-ttu-id="e213c-168"><span id="NFS_TYPE_LNK"></span><span id="nfs_type_lnk"></span>tipo de NFS \_ \_ lnk</span><span class="sxs-lookup"><span data-stu-id="e213c-168"><span id="NFS_TYPE_LNK"></span><span id="nfs_type_lnk"></span>NFS\_TYPE\_LNK</span></span><br/>    | <span data-ttu-id="e213c-169">Um link simbólico.</span><span class="sxs-lookup"><span data-stu-id="e213c-169">A symbolic link.</span></span><br/>          |
| <span data-ttu-id="e213c-170"><span id="NFS_TYPE_SOCK"></span><span id="nfs_type_sock"></span>tipo de NFS \_ \_ Sock</span><span class="sxs-lookup"><span data-stu-id="e213c-170"><span id="NFS_TYPE_SOCK"></span><span id="nfs_type_sock"></span>NFS\_TYPE\_SOCK</span></span><br/> | <span data-ttu-id="e213c-171">Um soquete do Windows.</span><span class="sxs-lookup"><span data-stu-id="e213c-171">A Windows socket.</span></span><br/>         |
| <span data-ttu-id="e213c-172"><span id="NFS_TYPE_FIFO"></span><span id="nfs_type_fifo"></span>tipo de NFS \_ \_ FIFO</span><span class="sxs-lookup"><span data-stu-id="e213c-172"><span id="NFS_TYPE_FIFO"></span><span id="nfs_type_fifo"></span>NFS\_TYPE\_FIFO</span></span><br/> | <span data-ttu-id="e213c-173">Um arquivo FIFO.</span><span class="sxs-lookup"><span data-stu-id="e213c-173">A FIFO file.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="e213c-174"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Moda**</span><span class="sxs-lookup"><span data-stu-id="e213c-174"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Mode**</span></span>
</dt> <dd>

<span data-ttu-id="e213c-175">O modo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="e213c-175">The file mode.</span></span>

</dd> <dt>

<span data-ttu-id="e213c-176"><span id="NLink"></span><span id="nlink"></span><span id="NLINK"></span>**NLink**</span><span class="sxs-lookup"><span data-stu-id="e213c-176"><span id="NLink"></span><span id="nlink"></span><span id="NLINK"></span>**NLink**</span></span>
</dt> <dd>

<span data-ttu-id="e213c-177">O número de links para o compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="e213c-177">The number of links to the share.</span></span>

</dd> <dt>

<span data-ttu-id="e213c-178"><span id="Uid"></span><span id="uid"></span><span id="UID"></span>**UID**</span><span class="sxs-lookup"><span data-stu-id="e213c-178"><span id="Uid"></span><span id="uid"></span><span id="UID"></span>**Uid**</span></span>
</dt> <dd>

<span data-ttu-id="e213c-179">O UID (identificador de usuário do UNIX).</span><span class="sxs-lookup"><span data-stu-id="e213c-179">The UNIX user identifier (UID).</span></span>

</dd> <dt>

<span data-ttu-id="e213c-180"><span id="Gid"></span><span id="gid"></span><span id="GID"></span>**GID**</span><span class="sxs-lookup"><span data-stu-id="e213c-180"><span id="Gid"></span><span id="gid"></span><span id="GID"></span>**Gid**</span></span>
</dt> <dd>

<span data-ttu-id="e213c-181">O GID (identificador de grupo do UNIX).</span><span class="sxs-lookup"><span data-stu-id="e213c-181">The UNIX group identifier (GID).</span></span>

</dd> <dt>

<span data-ttu-id="e213c-182"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="e213c-182"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Size**</span></span>
</dt> <dd>

<span data-ttu-id="e213c-183">O tamanho do arquivo, em bytes.</span><span class="sxs-lookup"><span data-stu-id="e213c-183">The file size, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e213c-184"><span id="Used"></span><span id="used"></span><span id="USED"></span>**Utiliza**</span><span class="sxs-lookup"><span data-stu-id="e213c-184"><span id="Used"></span><span id="used"></span><span id="USED"></span>**Used**</span></span>
</dt> <dd>

<span data-ttu-id="e213c-185">O tamanho do arquivo usado, em bytes.</span><span class="sxs-lookup"><span data-stu-id="e213c-185">The file size used, in bytes.</span></span> <span data-ttu-id="e213c-186">Isso é o mesmo que o tamanho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e213c-186">This is the same as the file size.</span></span>

</dd> <dt>

<span data-ttu-id="e213c-187"><span id="Rdev"></span><span id="rdev"></span><span id="RDEV"></span>**Rdev**</span><span class="sxs-lookup"><span data-stu-id="e213c-187"><span id="Rdev"></span><span id="rdev"></span><span id="RDEV"></span>**Rdev**</span></span>
</dt> <dd>

<span data-ttu-id="e213c-188">O identificador do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e213c-188">The device identifier.</span></span>

</dd> <dt>

<span data-ttu-id="e213c-189"><span id="Fsid"></span><span id="fsid"></span><span id="FSID"></span>**Fsid**</span><span class="sxs-lookup"><span data-stu-id="e213c-189"><span id="Fsid"></span><span id="fsid"></span><span id="FSID"></span>**Fsid**</span></span>
</dt> <dd>

<span data-ttu-id="e213c-190">O identificador do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="e213c-190">The file system identifier.</span></span>

</dd> <dt>

<span data-ttu-id="e213c-191"><span id="FileId"></span><span id="fileid"></span><span id="FILEID"></span>**FileId**</span><span class="sxs-lookup"><span data-stu-id="e213c-191"><span id="FileId"></span><span id="fileid"></span><span id="FILEID"></span>**FileId**</span></span>
</dt> <dd>

<span data-ttu-id="e213c-192">O identificador de arquivo.</span><span class="sxs-lookup"><span data-stu-id="e213c-192">The file identifier.</span></span>

</dd> <dt>

<span data-ttu-id="e213c-193"><span id="AccessTime"></span><span id="accesstime"></span><span id="ACCESSTIME"></span>**Acesso ao**</span><span class="sxs-lookup"><span data-stu-id="e213c-193"><span id="AccessTime"></span><span id="accesstime"></span><span id="ACCESSTIME"></span>**AccessTime**</span></span>
</dt> <dd>

<span data-ttu-id="e213c-194">A hora do último acesso.</span><span class="sxs-lookup"><span data-stu-id="e213c-194">The last access time.</span></span>

</dd> <dt>

<span data-ttu-id="e213c-195"><span id="ModifyTime"></span><span id="modifytime"></span><span id="MODIFYTIME"></span>**Modificartime**</span><span class="sxs-lookup"><span data-stu-id="e213c-195"><span id="ModifyTime"></span><span id="modifytime"></span><span id="MODIFYTIME"></span>**ModifyTime**</span></span>
</dt> <dd>

<span data-ttu-id="e213c-196">A hora da última modificação.</span><span class="sxs-lookup"><span data-stu-id="e213c-196">The last modification time.</span></span>

</dd> <dt>

<span data-ttu-id="e213c-197"><span id="ChangeTime"></span><span id="changetime"></span><span id="CHANGETIME"></span>**Changetime**</span><span class="sxs-lookup"><span data-stu-id="e213c-197"><span id="ChangeTime"></span><span id="changetime"></span><span id="CHANGETIME"></span>**ChangeTime**</span></span>
</dt> <dd>

<span data-ttu-id="e213c-198">A hora da última alteração.</span><span class="sxs-lookup"><span data-stu-id="e213c-198">The last change time.</span></span>

</dd> <dt>

<span data-ttu-id="e213c-199"><span id="FileAttributes"></span><span id="fileattributes"></span><span id="FILEATTRIBUTES"></span>**FileAttributes**</span><span class="sxs-lookup"><span data-stu-id="e213c-199"><span id="FileAttributes"></span><span id="fileattributes"></span><span id="FILEATTRIBUTES"></span>**FileAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="e213c-200">Uma estrutura de **\_ \_ atributos de arquivo NFS** .</span><span class="sxs-lookup"><span data-stu-id="e213c-200">An **NFS\_FILE\_ATTRIBUTES** structure.</span></span>

> [!Note]  
> <span data-ttu-id="e213c-201">Para obter descrições mais detalhadas dos membros dessa estrutura, consulte a estrutura **fattr3** na especificação do protocolo NFS versão 3 (conforme definido em [RFC 1813](https://www.ietf.org/rfc/rfc1813.txt)).</span><span class="sxs-lookup"><span data-stu-id="e213c-201">For more detailed descriptions of the members of this structure, see the **fattr3** structure in the NFS Version 3 Protocol Specification (as defined in [RFC 1813](https://www.ietf.org/rfc/rfc1813.txt)).</span></span>

 

</dd> <dt>

<span data-ttu-id="e213c-202"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Versão**</span><span class="sxs-lookup"><span data-stu-id="e213c-202"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version**</span></span>
</dt> <dd>

<span data-ttu-id="e213c-203">Especifica se a conexão na qual o identificador para o compartilhamento NFS foi criado é sobre o NFS versão 2 ou o protocolo NFS versão 3.</span><span class="sxs-lookup"><span data-stu-id="e213c-203">Specifies whether the connection on which the handle to the NFS share was created is over NFS Version 2 or NFS Version 3 protocol.</span></span>



| <span data-ttu-id="e213c-204">Valor</span><span class="sxs-lookup"><span data-stu-id="e213c-204">Value</span></span>                            | <span data-ttu-id="e213c-205">Descrição</span><span class="sxs-lookup"><span data-stu-id="e213c-205">Description</span></span>              |
|----------------------------------|--------------------------|
| <span data-ttu-id="e213c-206"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="e213c-206"><span id="2"></span>2</span></span><br/> | <span data-ttu-id="e213c-207">NFS versão 2</span><span class="sxs-lookup"><span data-stu-id="e213c-207">NFS Version 2</span></span><br/> |
| <span data-ttu-id="e213c-208"><span id="3"></span>Beta</span><span class="sxs-lookup"><span data-stu-id="e213c-208"><span id="3"></span>3</span></span><br/> | <span data-ttu-id="e213c-209">NFS versão 3</span><span class="sxs-lookup"><span data-stu-id="e213c-209">NFS Version 3</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e213c-210">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e213c-210">Requirements</span></span>



| <span data-ttu-id="e213c-211">Requisito</span><span class="sxs-lookup"><span data-stu-id="e213c-211">Requirement</span></span> | <span data-ttu-id="e213c-212">Valor</span><span class="sxs-lookup"><span data-stu-id="e213c-212">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="e213c-213">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e213c-213">Minimum supported client</span></span><br/> | <span data-ttu-id="e213c-214">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e213c-214">None supported</span></span><br/>         |
| <span data-ttu-id="e213c-215">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e213c-215">Minimum supported server</span></span><br/> | <span data-ttu-id="e213c-216">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e213c-216">Windows Server 2008</span></span><br/>    |
| <span data-ttu-id="e213c-217">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e213c-217">End of client support</span></span><br/>    | <span data-ttu-id="e213c-218">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e213c-218">None supported</span></span><br/>         |
| <span data-ttu-id="e213c-219">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="e213c-219">End of server support</span></span><br/>    | <span data-ttu-id="e213c-220">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e213c-220">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e213c-221">Confira também</span><span class="sxs-lookup"><span data-stu-id="e213c-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e213c-222">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="e213c-222">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
