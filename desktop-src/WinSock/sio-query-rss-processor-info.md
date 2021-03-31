---
description: O código de controle consulta a associação entre um soquete e um núcleo de processador RSS e um nó NUMA.
ms.assetid: DAF18C92-B479-474F-B438-0746CBA20653
title: SIO_QUERY_RSS_PROCESSOR_INFO código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: a2d251fa4fee996adaec51599e7b1d140a296b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920902"
---
# <a name="sio_query_rss_processor_info-control-code"></a><span data-ttu-id="f47ca-103">SIO_QUERY_RSS_PROCESSOR_INFO código de controle</span><span class="sxs-lookup"><span data-stu-id="f47ca-103">SIO_QUERY_RSS_PROCESSOR_INFO Control Code</span></span>

## <a name="description"></a><span data-ttu-id="f47ca-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="f47ca-104">Description</span></span>

<span data-ttu-id="f47ca-105">O código de controle de **\_ \_ \_ \_ informações do processador RSS do sio Query** consulta a associação entre um soquete e um núcleo de processador RSS e um nó numa.</span><span class="sxs-lookup"><span data-stu-id="f47ca-105">The **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** control code queries the association between a socket and an RSS processor core and NUMA node.</span></span>

<span data-ttu-id="f47ca-106">Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="f47ca-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_RSS_PROCESSOR_INFO, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_RSS_PROCESSOR_INFO, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="f47ca-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f47ca-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="f47ca-108">s</span><span class="sxs-lookup"><span data-stu-id="f47ca-108">s</span></span>

<span data-ttu-id="f47ca-109">Um descritor que identifica um soquete.</span><span class="sxs-lookup"><span data-stu-id="f47ca-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="f47ca-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="f47ca-110">dwIoControlCode</span></span>

<span data-ttu-id="f47ca-111">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="f47ca-111">The control code for the operation.</span></span>
<span data-ttu-id="f47ca-112">Use **as \_ \_ informações do \_ processador \_ RSS da consulta sio** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="f47ca-112">Use **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="f47ca-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="f47ca-113">lpvInBuffer</span></span>

<span data-ttu-id="f47ca-114">Um ponteiro para o buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="f47ca-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="f47ca-115">Este parâmetro não é usado para esta operação.</span><span class="sxs-lookup"><span data-stu-id="f47ca-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="f47ca-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="f47ca-116">cbInBuffer</span></span>

<span data-ttu-id="f47ca-117">O tamanho, em bytes, do buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="f47ca-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="f47ca-118">Este parâmetro não é usado para esta operação.</span><span class="sxs-lookup"><span data-stu-id="f47ca-118">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="f47ca-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="f47ca-119">lpvOutBuffer</span></span>

<span data-ttu-id="f47ca-120">Um ponteiro para o buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="f47ca-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="f47ca-121">Esse parâmetro deve apontar para uma estrutura de [**\_ \_ afinidade de processador de soquete**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) se os parâmetros *lpOverlapped* e *lpCompletionRoutine* forem **nulos**.</span><span class="sxs-lookup"><span data-stu-id="f47ca-121">This parameter should point to a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="f47ca-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="f47ca-122">cbOutBuffer</span></span>

<span data-ttu-id="f47ca-123">O tamanho, em bytes, do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="f47ca-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="f47ca-124">Esse parâmetro deve ter pelo menos o tamanho de uma estrutura de [**\_ \_ afinidade de processador de soquete**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) .</span><span class="sxs-lookup"><span data-stu-id="f47ca-124">This parameter must be at least the size of a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="f47ca-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="f47ca-125">lpcbBytesReturned</span></span>

<span data-ttu-id="f47ca-126">Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="f47ca-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="f47ca-127">Se o buffer de saída for muito pequeno, a chamada falhará, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [**WSAEINVAL**](windows-sockets-error-codes-2.md)e o parâmetro *lpcbBytesReturned* apontará para um valor *DWORD* igual a zero.</span><span class="sxs-lookup"><span data-stu-id="f47ca-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a *DWORD* value of zero.</span></span>

<span data-ttu-id="f47ca-128">Se *lpOverlapped* for **NULL**, o valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* retornado em uma chamada bem-sucedida não poderá ser zero.</span><span class="sxs-lookup"><span data-stu-id="f47ca-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="f47ca-129">Se o parâmetro *lpOverlapped* não for **nulo** para os soquetes sobrepostos, as operações que não puderem ser concluídas imediatamente serão iniciadas e a conclusão será indicada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="f47ca-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="f47ca-130">O valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* que é retornado pode ser zero, já que o tamanho dos dados armazenados não pode ser determinado até que a operação sobreposta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="f47ca-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="f47ca-131">O status final de conclusão pode ser recuperado quando o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="f47ca-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="f47ca-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="f47ca-132">lpvOverlapped</span></span>

<span data-ttu-id="f47ca-133">Um ponteiro para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="f47ca-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="f47ca-134">Se o soquete *s* foi criado sem o atributo sobreposto, o parâmetro *lpOverlapped* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="f47ca-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="f47ca-135">Se *s* foi aberto com o atributo Overlapped e o parâmetro *LpOverlapped* não for **nulo**, a operação será executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="f47ca-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="f47ca-136">Nesse caso, o parâmetro *lpOverlapped* deve apontar para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="f47ca-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="f47ca-137">Para operações sobrepostas, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retorna imediatamente, e o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="f47ca-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="f47ca-138">Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.</span><span class="sxs-lookup"><span data-stu-id="f47ca-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="f47ca-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="f47ca-139">lpCompletionRoutine</span></span>

<span data-ttu-id="f47ca-140">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="f47ca-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="f47ca-141">Um ponteiro para a rotina de conclusão chamada quando a operação foi concluída (ignorada para soquetes não sobrepostos).</span><span class="sxs-lookup"><span data-stu-id="f47ca-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="f47ca-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="f47ca-142">lpThreadId</span></span>

<span data-ttu-id="f47ca-143">Um ponteiro para uma estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a ser usado pelo provedor em uma chamada subsequente para [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="f47ca-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="f47ca-144">O provedor deve armazenar a estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) referenciada (não o ponteiro para o mesmo) até que a função [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) seja retornada.</span><span class="sxs-lookup"><span data-stu-id="f47ca-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="f47ca-145">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="f47ca-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="f47ca-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="f47ca-146">lpErrno</span></span>

<span data-ttu-id="f47ca-147">Um ponteiro para o código de erro.</span><span class="sxs-lookup"><span data-stu-id="f47ca-147">A pointer to the error code.</span></span>

<span data-ttu-id="f47ca-148">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="f47ca-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="f47ca-149">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f47ca-149">Return value</span></span>

<span data-ttu-id="f47ca-150">Se a operação for concluída com êxito, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará zero.</span><span class="sxs-lookup"><span data-stu-id="f47ca-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="f47ca-151">Se a operação falhar ou estiver pendente, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará **um \_ erro de soquete**.</span><span class="sxs-lookup"><span data-stu-id="f47ca-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="f47ca-152">Para obter informações de erro estendidas, chame [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="f47ca-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="f47ca-153">Código do erro</span><span class="sxs-lookup"><span data-stu-id="f47ca-153">Error code</span></span> | <span data-ttu-id="f47ca-154">Significado</span><span class="sxs-lookup"><span data-stu-id="f47ca-154">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="f47ca-155">**ERRO \_ de \_ buffer insuficiente**</span><span class="sxs-lookup"><span data-stu-id="f47ca-155">**ERROR\_INSUFFICIENT\_BUFFER**</span></span> | <span data-ttu-id="f47ca-156">A área de dados passada para uma chamada do sistema é muito pequena.</span><span class="sxs-lookup"><span data-stu-id="f47ca-156">The data area passed to a system call is too small.</span></span> <span data-ttu-id="f47ca-157">Esse erro será retornado se o buffer apontado pelo parâmetro *lpvOutBuffer* com um tamanho de buffer passado no parâmetro *cbOutBuffer* for muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="f47ca-157">This error is returned if the buffer pointed to by the *lpvOutBuffer* parameter with a buffer size passed in the *cbOutBuffer* parameter is too small.</span></span> <span data-ttu-id="f47ca-158">O tamanho do buffer necessário será retornado no parâmetro *lpcbBytesReturned* .</span><span class="sxs-lookup"><span data-stu-id="f47ca-158">The buffer size required will be returned in the *lpcbBytesReturned* parameter.</span></span> <span data-ttu-id="f47ca-159">Esse erro será retornado se o parâmetro *cbOutBuffer* for menor que o tamanho de uma estrutura de [**\_ \_ afinidade de processador de soquete**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) .</span><span class="sxs-lookup"><span data-stu-id="f47ca-159">This error is returned if the *cbOutBuffer* parameter is less than the size of a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure.</span></span> |
| <span data-ttu-id="f47ca-160">**\_e/s de WSA \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="f47ca-160">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="f47ca-161">Uma operação sobreposta foi iniciada com êxito e a conclusão será indicada em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="f47ca-161">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="f47ca-162">**operação de WSA \_ \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="f47ca-162">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="f47ca-163">Uma operação sobreposta foi cancelada devido ao fechamento do soquete ou à execução do comando **sio \_ flush** IOCTL.</span><span class="sxs-lookup"><span data-stu-id="f47ca-163">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="f47ca-164">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="f47ca-164">**WSAEFAULT**</span></span> | <span data-ttu-id="f47ca-165">O parâmetro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço de usuário.</span><span class="sxs-lookup"><span data-stu-id="f47ca-165">The *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="f47ca-166">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="f47ca-166">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="f47ca-167">A função é invocada quando um retorno de chamada está em andamento.</span><span class="sxs-lookup"><span data-stu-id="f47ca-167">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="f47ca-168">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="f47ca-168">**WSAEINTR**</span></span> | <span data-ttu-id="f47ca-169">Uma operação de bloqueio foi interrompida.</span><span class="sxs-lookup"><span data-stu-id="f47ca-169">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="f47ca-170">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="f47ca-170">**WSAEINVAL**</span></span> | <span data-ttu-id="f47ca-171">O parâmetro *dwIoControlCode* não é um comando válido ou um parâmetro de entrada especificado não é aceitável ou o comando não é aplicável ao tipo de soquete especificado.</span><span class="sxs-lookup"><span data-stu-id="f47ca-171">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="f47ca-172">Esse erro será retornado se o parâmetro *cbOutBuffer* for menor que o tamanho de uma estrutura de [**\_ \_ afinidade de processador de soquete**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) .</span><span class="sxs-lookup"><span data-stu-id="f47ca-172">This error is returned if the *cbOutBuffer* parameter is less than the size of a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure.</span></span>
| <span data-ttu-id="f47ca-173">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="f47ca-173">**WSAENETDOWN**</span></span> | <span data-ttu-id="f47ca-174">Falha no subsistema de rede.</span><span class="sxs-lookup"><span data-stu-id="f47ca-174">The network subsystem has failed.</span></span> |
| <span data-ttu-id="f47ca-175">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="f47ca-175">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="f47ca-176">Não há suporte para a opção de soquete no protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="f47ca-176">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="f47ca-177">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="f47ca-177">**WSAENOTCONN**</span></span> | <span data-ttu-id="f47ca-178">O soquete *s* não está conectado.</span><span class="sxs-lookup"><span data-stu-id="f47ca-178">The socket *s* is not connected.</span></span> |
| <span data-ttu-id="f47ca-179">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="f47ca-179">**WSAENOTSOCK**</span></span> | <span data-ttu-id="f47ca-180">O descritor *s* não é um soquete.</span><span class="sxs-lookup"><span data-stu-id="f47ca-180">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="f47ca-181">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="f47ca-181">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="f47ca-182">Não há suporte para o comando IOCTL especificado.</span><span class="sxs-lookup"><span data-stu-id="f47ca-182">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="f47ca-183">Esse erro será retornado se o provedor de transporte não oferecer suporte ao IOCTL de **\_ \_ \_ \_ informações do processador RSS de consulta sio** .</span><span class="sxs-lookup"><span data-stu-id="f47ca-183">This error is returned if the **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="f47ca-184">Comentários</span><span class="sxs-lookup"><span data-stu-id="f47ca-184">Remarks</span></span>

<span data-ttu-id="f47ca-185">O **sio \_ de \_ \_ \_ informações do processador RSS da consulta** do Microsoft Azure tem suporte no windows 8, no Windows Server 2012 e em versões posteriores do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f47ca-185">The **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="f47ca-186">O IOCTL de **\_ \_ \_ \_ informações do processador RSS de consulta sio** é usado para determinar a associação entre um soquete e um núcleo de processador RSS e um nó numa.</span><span class="sxs-lookup"><span data-stu-id="f47ca-186">The **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL is used to determine the association between a socket and an RSS processor core and NUMA node.</span></span>
<span data-ttu-id="f47ca-187">Esse IOCTL retorna uma estrutura de [**\_ \_ afinidade de processador de soquete**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) que contém o [**\_ número do processador**](/windows/desktop/api/winnt/ns-winnt-processor_number) e a ID do nó numa.</span><span class="sxs-lookup"><span data-stu-id="f47ca-187">This IOCTL returns a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure that contains the [**PROCESSOR\_NUMBER**](/windows/desktop/api/winnt/ns-winnt-processor_number) and the NUMA node ID.</span></span>
<span data-ttu-id="f47ca-188">A estrutura [**de \_ número de processador**](/windows/desktop/api/winnt/ns-winnt-processor_number) retornada contém um número de grupo e um número de processador relativo no grupo.</span><span class="sxs-lookup"><span data-stu-id="f47ca-188">The returned [**PROCESSOR\_NUMBER**](/windows/desktop/api/winnt/ns-winnt-processor_number) structure contains a group number and relative processor number within the group.</span></span>

<span data-ttu-id="f47ca-189">Se o soquete for um soquete UDP, o soquete deverá estar conectado para que **as \_ \_ informações do \_ processador \_ RSS de consulta sio** do IOCTL funcionem corretamente.</span><span class="sxs-lookup"><span data-stu-id="f47ca-189">If the socket is a UDP socket, the socket must be connected for the **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL to work properly.</span></span>

## <a name="see-also"></a><span data-ttu-id="f47ca-190">Confira também</span><span class="sxs-lookup"><span data-stu-id="f47ca-190">See also</span></span>

[<span data-ttu-id="f47ca-191">**PROCESSOR_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="f47ca-191">**PROCESSOR_NUMBER**</span></span>](/windows/desktop/api/winnt/ns-winnt-processor_number)

[<span data-ttu-id="f47ca-192">**SSA**</span><span class="sxs-lookup"><span data-stu-id="f47ca-192">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="f47ca-193">**SOCKET_PROCESSOR_AFFINITY**</span><span class="sxs-lookup"><span data-stu-id="f47ca-193">**SOCKET_PROCESSOR_AFFINITY**</span></span>](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity)

[<span data-ttu-id="f47ca-194">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="f47ca-194">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="f47ca-195">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="f47ca-195">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="f47ca-196">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="f47ca-196">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="f47ca-197">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="f47ca-197">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="f47ca-198">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="f47ca-198">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="f47ca-199">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="f47ca-199">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
