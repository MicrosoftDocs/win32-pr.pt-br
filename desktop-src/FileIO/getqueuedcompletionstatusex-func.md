---
description: Recupera simultaneamente várias entradas de porta de conclusão.
ms.assetid: 3996c02c-562c-4697-a091-e241ad54b239
title: Função GetQueuedCompletionStatusEx (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetQueuedCompletionStatusEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: d45471cc066e6de7cb388036e06e727fe828a532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757159"
---
# <a name="getqueuedcompletionstatusex-function"></a><span data-ttu-id="c43a5-103">Função GetQueuedCompletionStatusEx</span><span class="sxs-lookup"><span data-stu-id="c43a5-103">GetQueuedCompletionStatusEx function</span></span>

<span data-ttu-id="c43a5-104">Recupera simultaneamente várias entradas de porta de conclusão.</span><span class="sxs-lookup"><span data-stu-id="c43a5-104">Retrieves multiple completion port entries simultaneously.</span></span> <span data-ttu-id="c43a5-105">Ele aguarda que as operações de e/s pendentes associadas à porta de conclusão especificada sejam concluídas.</span><span class="sxs-lookup"><span data-stu-id="c43a5-105">It waits for pending I/O operations that are associated with the specified completion port to complete.</span></span>

<span data-ttu-id="c43a5-106">Para remover os pacotes de conclusão de e/s da fila um de cada vez, use a função [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="c43a5-106">To dequeue I/O completion packets one at a time, use the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="c43a5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c43a5-107">Syntax</span></span>


```C++
BOOL WINAPI GetQueuedCompletionStatusEx(
  _In_  HANDLE             CompletionPort,
  _Out_ LPOVERLAPPED_ENTRY lpCompletionPortEntries,
  _In_  ULONG              ulCount,
  _Out_ PULONG             ulNumEntriesRemoved,
  _In_  DWORD              dwMilliseconds,
  _In_  BOOL               fAlertable
);
```



## <a name="parameters"></a><span data-ttu-id="c43a5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c43a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c43a5-109">*CompletionPort* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c43a5-109">*CompletionPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c43a5-110">Um identificador para a porta de conclusão.</span><span class="sxs-lookup"><span data-stu-id="c43a5-110">A handle to the completion port.</span></span> <span data-ttu-id="c43a5-111">Para criar uma porta de conclusão, use a função [**CreateIoCompletionPort**](createiocompletionport.md) .</span><span class="sxs-lookup"><span data-stu-id="c43a5-111">To create a completion port, use the [**CreateIoCompletionPort**](createiocompletionport.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="c43a5-112">*lpCompletionPortEntries* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c43a5-112">*lpCompletionPortEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c43a5-113">Na entrada, aponta para uma matriz pré-configurada de estruturas de [**\_ entrada sobrepostas**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) .</span><span class="sxs-lookup"><span data-stu-id="c43a5-113">On input, points to a pre-allocated array of [**OVERLAPPED\_ENTRY**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) structures.</span></span>

<span data-ttu-id="c43a5-114">Na saída, recebe uma matriz de estruturas de [**\_ entrada sobrepostas**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) que contêm as entradas.</span><span class="sxs-lookup"><span data-stu-id="c43a5-114">On output, receives an array of [**OVERLAPPED\_ENTRY**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) structures that hold the entries.</span></span> <span data-ttu-id="c43a5-115">O número de elementos de matriz é fornecido por *ulNumEntriesRemoved*.</span><span class="sxs-lookup"><span data-stu-id="c43a5-115">The number of array elements is provided by *ulNumEntriesRemoved*.</span></span>

<span data-ttu-id="c43a5-116">O número de bytes transferidos durante cada e/s, a chave de conclusão que indica em qual arquivo cada e/s ocorreu e o endereço da estrutura sobreposta usado em cada e/s original são todos retornados na matriz *lpCompletionPortEntries* .</span><span class="sxs-lookup"><span data-stu-id="c43a5-116">The number of bytes transferred during each I/O, the completion key that indicates on which file each I/O occurred, and the overlapped structure address used in each original I/O are all returned in the *lpCompletionPortEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="c43a5-117">*ulCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c43a5-117">*ulCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c43a5-118">O número máximo de entradas a serem removidas.</span><span class="sxs-lookup"><span data-stu-id="c43a5-118">The maximum number of entries to remove.</span></span>

</dd> <dt>

<span data-ttu-id="c43a5-119">*ulNumEntriesRemoved* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c43a5-119">*ulNumEntriesRemoved* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c43a5-120">Um ponteiro para uma variável que recebe o número de entradas realmente removidas.</span><span class="sxs-lookup"><span data-stu-id="c43a5-120">A pointer to a variable that receives the number of entries actually removed.</span></span>

</dd> <dt>

<span data-ttu-id="c43a5-121">*dwMilliseconds* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c43a5-121">*dwMilliseconds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c43a5-122">O número de milissegundos que o chamador está disposto a aguardar a exibição de um pacote de conclusão na porta de conclusão.</span><span class="sxs-lookup"><span data-stu-id="c43a5-122">The number of milliseconds that the caller is willing to wait for a completion packet to appear at the completion port.</span></span> <span data-ttu-id="c43a5-123">Se um pacote de conclusão não aparecer dentro do tempo especificado, a função expirará e retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="c43a5-123">If a completion packet does not appear within the specified time, the function times out and returns **FALSE**.</span></span>

<span data-ttu-id="c43a5-124">Se *dwMilliseconds* for **infinito** (0xFFFFFFFF), a função nunca atingirá o tempo limite. Se *dwMilliseconds* for zero e não houver nenhuma operação de e/s para remover da fila, a função atingirá o tempo limite imediatamente.</span><span class="sxs-lookup"><span data-stu-id="c43a5-124">If *dwMilliseconds* is **INFINITE** (0xFFFFFFFF), the function will never time out. If *dwMilliseconds* is zero and there is no I/O operation to dequeue, the function will time out immediately.</span></span>

</dd> <dt>

<span data-ttu-id="c43a5-125">*fAlertable* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c43a5-125">*fAlertable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c43a5-126">Se esse parâmetro for **false**, a função não retornará até que o período de tempo limite tenha decorrido ou uma entrada seja recuperada.</span><span class="sxs-lookup"><span data-stu-id="c43a5-126">If this parameter is **FALSE**, the function does not return until the time-out period has elapsed or an entry is retrieved.</span></span>

<span data-ttu-id="c43a5-127">Se o parâmetro for **true** e não houver entradas disponíveis, a função executará uma espera alertável.</span><span class="sxs-lookup"><span data-stu-id="c43a5-127">If the parameter is **TRUE** and there are no available entries, the function performs an alertable wait.</span></span> <span data-ttu-id="c43a5-128">O thread retorna quando o sistema enfileira uma rotina de conclusão de e/s ou a APC para o thread e o thread executa a função.</span><span class="sxs-lookup"><span data-stu-id="c43a5-128">The thread returns when the system queues an I/O completion routine or APC to the thread and the thread executes the function.</span></span>

<span data-ttu-id="c43a5-129">Uma rotina de conclusão é enfileirada quando a função [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) ou [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) na qual ela foi especificada foi concluída, e o thread de chamada é o thread que iniciou a operação.</span><span class="sxs-lookup"><span data-stu-id="c43a5-129">A completion routine is queued when the [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) or [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) function in which it was specified has completed, and the calling thread is the thread that initiated the operation.</span></span> <span data-ttu-id="c43a5-130">Uma APC é enfileirada quando você chama [**QueueUserAPC**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc).</span><span class="sxs-lookup"><span data-stu-id="c43a5-130">An APC is queued when you call [**QueueUserAPC**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c43a5-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c43a5-131">Return value</span></span>

<span data-ttu-id="c43a5-132">Retorna zero (**true**) se for bem-sucedido ou zero (**false**) caso contrário.</span><span class="sxs-lookup"><span data-stu-id="c43a5-132">Returns nonzero (**TRUE**) if successful or zero (**FALSE**) otherwise.</span></span>

<span data-ttu-id="c43a5-133">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="c43a5-133">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="c43a5-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="c43a5-134">Remarks</span></span>

<span data-ttu-id="c43a5-135">Essa função associa um thread à porta de conclusão especificada.</span><span class="sxs-lookup"><span data-stu-id="c43a5-135">This function associates a thread with the specified completion port.</span></span> <span data-ttu-id="c43a5-136">Um thread pode ser associado a no máximo uma porta de conclusão.</span><span class="sxs-lookup"><span data-stu-id="c43a5-136">A thread can be associated with at most one completion port.</span></span>

<span data-ttu-id="c43a5-137">Essa função retorna **true** quando pelo menos uma e/s pendente é concluída, mas é possível que uma ou mais operações de e/s tenham falhado.</span><span class="sxs-lookup"><span data-stu-id="c43a5-137">This function returns **TRUE** when at least one pending I/O is completed, but it is possible that one or more I/O operations failed.</span></span> <span data-ttu-id="c43a5-138">Observe que cabe ao usuário dessa função verificar a lista de entradas retornadas no parâmetro *lpCompletionPortEntries* para determinar quais delas correspondem a quaisquer possíveis operações de e/s com falha examinando o status contido no membro **lpOverlapped** em cada [**\_ entrada sobreposta**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry).</span><span class="sxs-lookup"><span data-stu-id="c43a5-138">Note that it is up to the user of this function to check the list of returned entries in the *lpCompletionPortEntries* parameter to determine which of them correspond to any possible failed I/O operations by looking at the status contained in the **lpOverlapped** member in each [**OVERLAPPED\_ENTRY**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry).</span></span>

<span data-ttu-id="c43a5-139">Essa função retorna **false** quando nenhuma operação de e/s foi removida da fila.</span><span class="sxs-lookup"><span data-stu-id="c43a5-139">This function returns **FALSE** when no I/O operation was dequeued.</span></span> <span data-ttu-id="c43a5-140">Isso normalmente significa que ocorreu um erro durante o processamento dos parâmetros para esta chamada ou que o identificador *CompletionPort* foi fechado ou é inválido.</span><span class="sxs-lookup"><span data-stu-id="c43a5-140">This typically means that an error occurred while processing the parameters to this call, or that the *CompletionPort* handle was closed or is otherwise invalid.</span></span> <span data-ttu-id="c43a5-141">A função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) fornece informações de erro estendidas.</span><span class="sxs-lookup"><span data-stu-id="c43a5-141">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function provides extended error information.</span></span>

<span data-ttu-id="c43a5-142">Se uma chamada para [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) falhar porque o identificador associado a ela está fechado, a função retornará **false** e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o **erro \_ abandonado \_ aguardando \_ 0**.</span><span class="sxs-lookup"><span data-stu-id="c43a5-142">If a call to [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) fails because the handle associated with it is closed, the function returns **FALSE** and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return **ERROR\_ABANDONED\_WAIT\_0**.</span></span>

<span data-ttu-id="c43a5-143">Os aplicativos de servidor podem ter vários threads chamando a função **GetQueuedCompletionStatusEx** para a mesma porta de conclusão.</span><span class="sxs-lookup"><span data-stu-id="c43a5-143">Server applications may have several threads calling the **GetQueuedCompletionStatusEx** function for the same completion port.</span></span> <span data-ttu-id="c43a5-144">À medida que as operações de e/s são concluídas, elas são enfileiradas para essa porta na ordem de primeiro a entrar, primeiro a sair.</span><span class="sxs-lookup"><span data-stu-id="c43a5-144">As I/O operations complete, they are queued to this port in first-in-first-out order.</span></span> <span data-ttu-id="c43a5-145">Se um thread estiver aguardando ativamente nesta chamada, uma ou mais solicitações enfileiradas concluirão a chamada somente para esse thread.</span><span class="sxs-lookup"><span data-stu-id="c43a5-145">If a thread is actively waiting on this call, one or more queued requests complete the call for that thread only.</span></span>

<span data-ttu-id="c43a5-146">Para obter mais informações sobre a teoria, uso e funções associadas da porta de conclusão de e/s, consulte [portas de conclusão de e/s](i-o-completion-ports.md).</span><span class="sxs-lookup"><span data-stu-id="c43a5-146">For more information on I/O completion port theory, usage, and associated functions, see [I/O Completion Ports](i-o-completion-ports.md).</span></span>

<span data-ttu-id="c43a5-147">No Windows 8 e no Windows Server 2012, essa função é suportada pelas seguintes tecnologias.</span><span class="sxs-lookup"><span data-stu-id="c43a5-147">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="c43a5-148">Tecnologia</span><span class="sxs-lookup"><span data-stu-id="c43a5-148">Technology</span></span>                                           | <span data-ttu-id="c43a5-149">Com suporte</span><span class="sxs-lookup"><span data-stu-id="c43a5-149">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="c43a5-150">Protocolo SMB (Server Message Block) 3,0</span><span class="sxs-lookup"><span data-stu-id="c43a5-150">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="c43a5-151">Yes</span><span class="sxs-lookup"><span data-stu-id="c43a5-151">Yes</span></span><br/> |
| <span data-ttu-id="c43a5-152">Failover transparente SMB 3,0 (TFO)</span><span class="sxs-lookup"><span data-stu-id="c43a5-152">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="c43a5-153">Yes</span><span class="sxs-lookup"><span data-stu-id="c43a5-153">Yes</span></span><br/> |
| <span data-ttu-id="c43a5-154">SMB 3,0 com compartilhamentos de arquivos de escalabilidade horizontal (SO)</span><span class="sxs-lookup"><span data-stu-id="c43a5-154">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="c43a5-155">Yes</span><span class="sxs-lookup"><span data-stu-id="c43a5-155">Yes</span></span><br/> |
| <span data-ttu-id="c43a5-156">Sistema de arquivos Volume Compartilhado Clusterizado (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="c43a5-156">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="c43a5-157">Yes</span><span class="sxs-lookup"><span data-stu-id="c43a5-157">Yes</span></span><br/> |
| <span data-ttu-id="c43a5-158">ReFS (Sistema de Arquivos Resiliente)</span><span class="sxs-lookup"><span data-stu-id="c43a5-158">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="c43a5-159">Yes</span><span class="sxs-lookup"><span data-stu-id="c43a5-159">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c43a5-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c43a5-160">Requirements</span></span>



| <span data-ttu-id="c43a5-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="c43a5-161">Requirement</span></span> | <span data-ttu-id="c43a5-162">Valor</span><span class="sxs-lookup"><span data-stu-id="c43a5-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c43a5-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c43a5-163">Minimum supported client</span></span><br/> | <span data-ttu-id="c43a5-164">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="c43a5-164">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="c43a5-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c43a5-165">Minimum supported server</span></span><br/> | <span data-ttu-id="c43a5-166">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c43a5-166">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                             |
| <span data-ttu-id="c43a5-167">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c43a5-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="c43a5-168"><dt>IoAPI. h (incluir Windows. h); </dt> <dt>Winbase. h no Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c43a5-168"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c43a5-169">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c43a5-169">Library</span></span><br/>                  | <dl> <span data-ttu-id="c43a5-170"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c43a5-170"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="c43a5-171">DLL</span><span class="sxs-lookup"><span data-stu-id="c43a5-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c43a5-172"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c43a5-172"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a><span data-ttu-id="c43a5-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="c43a5-173">See also</span></span>

<dl> <dt>

<span data-ttu-id="c43a5-174">**Tópicos de visão geral**</span><span class="sxs-lookup"><span data-stu-id="c43a5-174">**Overview Topics**</span></span>
</dt> <dt>

[<span data-ttu-id="c43a5-175">Funções de gerenciamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="c43a5-175">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="c43a5-176">Portas de conclusão de e/s</span><span class="sxs-lookup"><span data-stu-id="c43a5-176">I/O Completion Ports</span></span>](i-o-completion-ports.md)
</dt> <dt>

[<span data-ttu-id="c43a5-177">Usando os cabeçalhos do Windows</span><span class="sxs-lookup"><span data-stu-id="c43a5-177">Using the Windows Headers</span></span>](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

<span data-ttu-id="c43a5-178">**Funções**</span><span class="sxs-lookup"><span data-stu-id="c43a5-178">**Functions**</span></span>
</dt> <dt>

[<span data-ttu-id="c43a5-179">**ConnectNamedPipe**</span><span class="sxs-lookup"><span data-stu-id="c43a5-179">**ConnectNamedPipe**</span></span>](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)
</dt> <dt>

[<span data-ttu-id="c43a5-180">**CreateIoCompletionPort**</span><span class="sxs-lookup"><span data-stu-id="c43a5-180">**CreateIoCompletionPort**</span></span>](createiocompletionport.md)
</dt> <dt>

[<span data-ttu-id="c43a5-181">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="c43a5-181">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="c43a5-182">**GetQueuedCompletionStatusEx**</span><span class="sxs-lookup"><span data-stu-id="c43a5-182">**GetQueuedCompletionStatusEx**</span></span>](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[<span data-ttu-id="c43a5-183">**LockFileEx**</span><span class="sxs-lookup"><span data-stu-id="c43a5-183">**LockFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[<span data-ttu-id="c43a5-184">**ReadFile**</span><span class="sxs-lookup"><span data-stu-id="c43a5-184">**ReadFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[<span data-ttu-id="c43a5-185">**PostQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="c43a5-185">**PostQueuedCompletionStatus**</span></span>](postqueuedcompletionstatus.md)
</dt> <dt>

[<span data-ttu-id="c43a5-186">**TransactNamedPipe**</span><span class="sxs-lookup"><span data-stu-id="c43a5-186">**TransactNamedPipe**</span></span>](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)
</dt> <dt>

[<span data-ttu-id="c43a5-187">**WaitCommEvent**</span><span class="sxs-lookup"><span data-stu-id="c43a5-187">**WaitCommEvent**</span></span>](/windows/desktop/api/winbase/nf-winbase-waitcommevent)
</dt> <dt>

[<span data-ttu-id="c43a5-188">**WriteFile**</span><span class="sxs-lookup"><span data-stu-id="c43a5-188">**WriteFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> </dl>

 

