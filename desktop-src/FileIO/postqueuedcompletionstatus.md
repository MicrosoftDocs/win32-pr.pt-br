---
description: Posta um pacote de conclusão de e/s em uma porta de conclusão de e/s.
ms.assetid: 69a9b1e5-2d40-42de-a14a-f7b6f29bf571
title: Função PostQueuedCompletionStatus (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostQueuedCompletionStatus
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: f12de10032df7fec32dd9a577353dd20c0f4eaa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756939"
---
# <a name="postqueuedcompletionstatus-function"></a><span data-ttu-id="783a1-103">Função PostQueuedCompletionStatus</span><span class="sxs-lookup"><span data-stu-id="783a1-103">PostQueuedCompletionStatus function</span></span>

<span data-ttu-id="783a1-104">Posta um pacote de conclusão de e/s em uma porta de conclusão de e/s.</span><span class="sxs-lookup"><span data-stu-id="783a1-104">Posts an I/O completion packet to an I/O completion port.</span></span>

## <a name="syntax"></a><span data-ttu-id="783a1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="783a1-105">Syntax</span></span>


```C++
BOOL WINAPI PostQueuedCompletionStatus(
  _In_     HANDLE       CompletionPort,
  _In_     DWORD        dwNumberOfBytesTransferred,
  _In_     ULONG_PTR    dwCompletionKey,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a><span data-ttu-id="783a1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="783a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="783a1-107">*CompletionPort* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="783a1-107">*CompletionPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="783a1-108">Um identificador para uma porta de conclusão de e/s na qual o pacote de conclusão de e/s deve ser lançado.</span><span class="sxs-lookup"><span data-stu-id="783a1-108">A handle to an I/O completion port to which the I/O completion packet is to be posted.</span></span>

</dd> <dt>

<span data-ttu-id="783a1-109">*dwNumberOfBytesTransferred* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="783a1-109">*dwNumberOfBytesTransferred* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="783a1-110">O valor a ser retornado por meio do parâmetro *lpNumberOfBytesTransferred* da função [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="783a1-110">The value to be returned through the *lpNumberOfBytesTransferred* parameter of the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="783a1-111">*dwCompletionKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="783a1-111">*dwCompletionKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="783a1-112">O valor a ser retornado por meio do parâmetro *lpCompletionKey* da função [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="783a1-112">The value to be returned through the *lpCompletionKey* parameter of the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="783a1-113">*lpOverlapped* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="783a1-113">*lpOverlapped* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="783a1-114">O valor a ser retornado por meio do parâmetro *lpOverlapped* da função [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="783a1-114">The value to be returned through the *lpOverlapped* parameter of the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="783a1-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="783a1-115">Return value</span></span>

<span data-ttu-id="783a1-116">Se a função for bem-sucedida, o valor retornado será diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="783a1-116">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="783a1-117">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="783a1-117">If the function fails, the return value is zero.</span></span> <span data-ttu-id="783a1-118">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="783a1-118">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span></span>

## <a name="remarks"></a><span data-ttu-id="783a1-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="783a1-119">Remarks</span></span>

<span data-ttu-id="783a1-120">O pacote de conclusão de e/s atenderá a uma chamada pendente para a função [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="783a1-120">The I/O completion packet will satisfy an outstanding call to the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span> <span data-ttu-id="783a1-121">Essa função retorna com os três valores passados como segundo, terceiro e quarto parâmetros da chamada para **PostQueuedCompletionStatus**.</span><span class="sxs-lookup"><span data-stu-id="783a1-121">This function returns with the three values passed as the second, third, and fourth parameters of the call to **PostQueuedCompletionStatus**.</span></span> <span data-ttu-id="783a1-122">O sistema não usa nem valida esses valores.</span><span class="sxs-lookup"><span data-stu-id="783a1-122">The system does not use or validate these values.</span></span> <span data-ttu-id="783a1-123">Em particular, o parâmetro *lpOverlapped* não precisa apontar para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="783a1-123">In particular, the *lpOverlapped* parameter need not point to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="783a1-124">No Windows 8 e no Windows Server 2012, essa função é suportada pelas seguintes tecnologias.</span><span class="sxs-lookup"><span data-stu-id="783a1-124">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="783a1-125">Tecnologia</span><span class="sxs-lookup"><span data-stu-id="783a1-125">Technology</span></span>                                           | <span data-ttu-id="783a1-126">Com suporte</span><span class="sxs-lookup"><span data-stu-id="783a1-126">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="783a1-127">Protocolo SMB (Server Message Block) 3,0</span><span class="sxs-lookup"><span data-stu-id="783a1-127">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="783a1-128">Yes</span><span class="sxs-lookup"><span data-stu-id="783a1-128">Yes</span></span><br/> |
| <span data-ttu-id="783a1-129">Failover transparente SMB 3,0 (TFO)</span><span class="sxs-lookup"><span data-stu-id="783a1-129">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="783a1-130">Yes</span><span class="sxs-lookup"><span data-stu-id="783a1-130">Yes</span></span><br/> |
| <span data-ttu-id="783a1-131">SMB 3,0 com compartilhamentos de arquivos de escalabilidade horizontal (SO)</span><span class="sxs-lookup"><span data-stu-id="783a1-131">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="783a1-132">Yes</span><span class="sxs-lookup"><span data-stu-id="783a1-132">Yes</span></span><br/> |
| <span data-ttu-id="783a1-133">Sistema de arquivos Volume Compartilhado Clusterizado (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="783a1-133">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="783a1-134">Yes</span><span class="sxs-lookup"><span data-stu-id="783a1-134">Yes</span></span><br/> |
| <span data-ttu-id="783a1-135">ReFS (Sistema de Arquivos Resiliente)</span><span class="sxs-lookup"><span data-stu-id="783a1-135">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="783a1-136">Yes</span><span class="sxs-lookup"><span data-stu-id="783a1-136">Yes</span></span><br/> |



 

<span data-ttu-id="783a1-137">O CsvFs fará e/s redirecionada para arquivos compactados.</span><span class="sxs-lookup"><span data-stu-id="783a1-137">CsvFs will do redirected IO for compressed files.</span></span>

## <a name="requirements"></a><span data-ttu-id="783a1-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="783a1-138">Requirements</span></span>



| <span data-ttu-id="783a1-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="783a1-139">Requirement</span></span> | <span data-ttu-id="783a1-140">Valor</span><span class="sxs-lookup"><span data-stu-id="783a1-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="783a1-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="783a1-141">Minimum supported client</span></span><br/> | <span data-ttu-id="783a1-142">Aplicativos de \[ aplicativos \| UWP do Windows XP desktop\]</span><span class="sxs-lookup"><span data-stu-id="783a1-142">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="783a1-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="783a1-143">Minimum supported server</span></span><br/> | <span data-ttu-id="783a1-144">Aplicativos do Windows Server 2003 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="783a1-144">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="783a1-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="783a1-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="783a1-146"><dt>IoAPI. h (incluir Windows. h); </dt> <dt>Winbase. h no Windows server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="783a1-146"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="783a1-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="783a1-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="783a1-148"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="783a1-148"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                  |
| <span data-ttu-id="783a1-149">DLL</span><span class="sxs-lookup"><span data-stu-id="783a1-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="783a1-150"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="783a1-150"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a><span data-ttu-id="783a1-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="783a1-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="783a1-152">**CreateIoCompletionPort**</span><span class="sxs-lookup"><span data-stu-id="783a1-152">**CreateIoCompletionPort**</span></span>](createiocompletionport.md)
</dt> <dt>

[<span data-ttu-id="783a1-153">Funções de gerenciamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="783a1-153">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="783a1-154">**GetQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="783a1-154">**GetQueuedCompletionStatus**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[<span data-ttu-id="783a1-155">**SOBREPÕE**</span><span class="sxs-lookup"><span data-stu-id="783a1-155">**OVERLAPPED**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)
</dt> </dl>

 

