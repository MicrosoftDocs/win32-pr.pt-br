---
description: O código de controle recupera o contexto de redirecionamento para um registro de redirecionamento usado por um serviço de redirecionamento da plataforma de filtragem
ms.assetid: 87DB11BB-E08D-49DF-A211-133D813373E0
title: SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 1e5e5f6c56411ada1e87e8cdf240a89f9c293e4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090360"
---
# <a name="sio_query_wfp_connection_redirect_context-control-code"></a><span data-ttu-id="4b6c7-103">SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT código de controle</span><span class="sxs-lookup"><span data-stu-id="4b6c7-103">SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT Control Code</span></span>

## <a name="description"></a><span data-ttu-id="4b6c7-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b6c7-104">Description</span></span>

<span data-ttu-id="4b6c7-105">O código de controle do **\_ \_ \_ \_ \_ contexto de redirecionamento de conexão WFP sio** recupera o contexto de redirecionamento para um registro de redirecionamento usado por um serviço de redirecionamento WFP (Windows Filtering Platform)</span><span class="sxs-lookup"><span data-stu-id="4b6c7-105">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** control code retrieves the redirect context for a redirect record used by a Windows Filtering Platform (WFP) redirect service.</span></span>

<span data-ttu-id="4b6c7-106">Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT, // dwIoControlCode
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
  SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT, // dwIoControlCode
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

## <a name="parameters"></a><span data-ttu-id="4b6c7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b6c7-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="4b6c7-108">s</span><span class="sxs-lookup"><span data-stu-id="4b6c7-108">s</span></span>

<span data-ttu-id="4b6c7-109">Um descritor que identifica um soquete.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="4b6c7-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="4b6c7-110">dwIoControlCode</span></span>

<span data-ttu-id="4b6c7-111">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-111">The control code for the operation.</span></span>
<span data-ttu-id="4b6c7-112">Use **o \_ \_ \_ \_ \_ contexto de redirecionamento de conexão WFP de consulta sio** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-112">Use **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="4b6c7-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="4b6c7-113">lpvInBuffer</span></span>

<span data-ttu-id="4b6c7-114">Um ponteiro para o buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="4b6c7-115">Este parâmetro não é usado para esta operação.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="4b6c7-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="4b6c7-116">cbInBuffer</span></span>

<span data-ttu-id="4b6c7-117">O tamanho, em bytes, do buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="4b6c7-118">Este parâmetro não é usado para esta operação.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-118">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="4b6c7-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="4b6c7-119">lpvOutBuffer</span></span>

<span data-ttu-id="4b6c7-120">Um ponteiro para o buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="4b6c7-121">Esse parâmetro deve apontar para um tipo de dados **ULONG** se os parâmetros *lpOverlapped* e *lpCompletionRoutine* forem **nulos**.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-121">This parameter should point to a **ULONG** data type if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="4b6c7-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="4b6c7-122">cbOutBuffer</span></span>

<span data-ttu-id="4b6c7-123">O tamanho, em bytes, do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="4b6c7-124">Esse parâmetro deve ter pelo menos o tamanho de um tipo de dados **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="4b6c7-124">This parameter must be at least the size of a **ULONG** data type.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="4b6c7-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="4b6c7-125">lpcbBytesReturned</span></span>

<span data-ttu-id="4b6c7-126">Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="4b6c7-127">Se o buffer de saída for muito pequeno, a chamada falhará, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [**WSAEINVAL**](windows-sockets-error-codes-2.md)e o parâmetro *lpcbBytesReturned* apontará para um valor **DWORD** igual a zero.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="4b6c7-128">Se *lpOverlapped* for **NULL**, o valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* retornado em uma chamada bem-sucedida não poderá ser zero.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="4b6c7-129">Se o parâmetro *lpOverlapped* não for **nulo** para os soquetes sobrepostos, as operações que não puderem ser concluídas imediatamente serão iniciadas e a conclusão será indicada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="4b6c7-130">O valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* que é retornado pode ser zero, já que o tamanho dos dados armazenados não pode ser determinado até que a operação sobreposta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="4b6c7-131">O status final de conclusão pode ser recuperado quando o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="4b6c7-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="4b6c7-132">lpvOverlapped</span></span>

<span data-ttu-id="4b6c7-133">Um ponteiro para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="4b6c7-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="4b6c7-134">Se o soquete *s* foi criado sem o atributo sobreposto, o parâmetro *lpOverlapped* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="4b6c7-135">Se *s* foi aberto com o atributo Overlapped e o parâmetro *LpOverlapped* não for **nulo**, a operação será executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="4b6c7-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="4b6c7-136">Nesse caso, o parâmetro *lpOverlapped* deve apontar para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="4b6c7-137">Para operações sobrepostas, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retorna imediatamente, e o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="4b6c7-138">Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="4b6c7-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="4b6c7-139">lpCompletionRoutine</span></span>

<span data-ttu-id="4b6c7-140">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="4b6c7-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="4b6c7-141">Um ponteiro para a rotina de conclusão chamada quando a operação foi concluída (ignorada para soquetes não sobrepostos).</span><span class="sxs-lookup"><span data-stu-id="4b6c7-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="4b6c7-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="4b6c7-142">lpThreadId</span></span>

<span data-ttu-id="4b6c7-143">Um ponteiro para uma estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a ser usado pelo provedor em uma chamada subsequente para [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="4b6c7-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="4b6c7-144">O provedor deve armazenar a estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) referenciada (não o ponteiro para o mesmo) até que a função [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) seja retornada.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="4b6c7-145">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="4b6c7-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="4b6c7-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="4b6c7-146">lpErrno</span></span>

<span data-ttu-id="4b6c7-147">Um ponteiro para o código de erro.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-147">A pointer to the error code.</span></span>

<span data-ttu-id="4b6c7-148">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="4b6c7-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b6c7-149">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4b6c7-149">Return value</span></span>

<span data-ttu-id="4b6c7-150">Se a operação for concluída com êxito, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará zero.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="4b6c7-151">Se a operação falhar ou estiver pendente, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará **um \_ erro de soquete**.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="4b6c7-152">Para obter informações de erro estendidas, chame [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="4b6c7-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="4b6c7-153">Código do erro</span><span class="sxs-lookup"><span data-stu-id="4b6c7-153">Error code</span></span> | <span data-ttu-id="4b6c7-154">Significado</span><span class="sxs-lookup"><span data-stu-id="4b6c7-154">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="4b6c7-155">**\_e/s de WSA \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="4b6c7-155">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="4b6c7-156">Uma operação sobreposta foi iniciada com êxito e a conclusão será indicada em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-156">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="4b6c7-157">**operação de WSA \_ \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="4b6c7-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="4b6c7-158">Uma operação sobreposta foi cancelada devido ao fechamento do soquete ou à execução do comando SIO_FLUSH IOCTL.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-158">An overlapped operation was canceled due to the closure of the socket or the execution of the SIO_FLUSH IOCTL command.</span></span> |
| <span data-ttu-id="4b6c7-159">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="4b6c7-159">**WSAEFAULT**</span></span> | <span data-ttu-id="4b6c7-160">O parâmetro *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço de usuário.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-160">The *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped*, or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="4b6c7-161">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="4b6c7-161">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="4b6c7-162">A função é invocada quando um retorno de chamada está em andamento.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-162">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="4b6c7-163">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="4b6c7-163">**WSAEINTR**</span></span> | <span data-ttu-id="4b6c7-164">Uma operação de bloqueio foi interrompida.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-164">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="4b6c7-165">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="4b6c7-165">**WSAEINVAL**</span></span> | <span data-ttu-id="4b6c7-166">O parâmetro *dwIoControlCode* não é um comando válido ou um parâmetro de entrada especificado não é aceitável ou o comando não é aplicável ao tipo de soquete especificado.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-166">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="4b6c7-167">Esse erro será retornado se o parâmetro *cbOutBuffer* for menor que o tamanho de um tipo de dados **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="4b6c7-167">This error is returned if the *cbOutBuffer* parameter is less than the size of a **ULONG** data type.</span></span> |
| <span data-ttu-id="4b6c7-168">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="4b6c7-168">**WSAENETDOWN**</span></span> | <span data-ttu-id="4b6c7-169">Falha no subsistema de rede.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-169">The network subsystem has failed.</span></span> |
| <span data-ttu-id="4b6c7-170">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="4b6c7-170">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="4b6c7-171">Não há suporte para a opção de soquete no protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-171">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="4b6c7-172">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="4b6c7-172">**WSAENOTCONN**</span></span> | <span data-ttu-id="4b6c7-173">O soquete *s* não está conectado.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-173">The socket *s* is not connected.</span></span> |
| <span data-ttu-id="4b6c7-174">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="4b6c7-174">**WSAENOTSOCK**</span></span> | <span data-ttu-id="4b6c7-175">O descritor *s* não é um soquete.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-175">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="4b6c7-176">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="4b6c7-176">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="4b6c7-177">Não há suporte para o comando IOCTL especificado.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-177">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="4b6c7-178">Esse erro será retornado se o **\_ contexto de \_ \_ \_ redirecionamento \_ de conexão WFP sio consulta** não for suportado pelo provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-178">This error is returned if the **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="4b6c7-179">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b6c7-179">Remarks</span></span>

<span data-ttu-id="4b6c7-180">O **\_ contexto de \_ \_ \_ redirecionamento \_ de conexão WFP de consulta sio** é suportado no Windows 8, no Windows Server 2012 e em versões posteriores do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-180">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="4b6c7-181">A WFP permite o acesso ao caminho de processamento de pacotes TCP/IP, onde os pacotes de saída e de entrada podem ser examinados ou alterados antes de permitir que sejam processados ainda mais.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-181">WFP allows access to the TCP/IP packet processing path, wherein outgoing and incoming packets can be examined or changed before allowing them to be processed further.</span></span>
<span data-ttu-id="4b6c7-182">Ao tocar no caminho de processamento TCP/IP, os ISVs (fornecedores independentes de software) podem criar com mais facilidade firewalls, software antivírus, software de diagnóstico e outros tipos de aplicativos e serviços.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-182">By tapping into the TCP/IP processing path, independent software vendors (ISVs) can more easily create firewalls, antivirus software, diagnostic software, and other types of applications and services.</span></span>
<span data-ttu-id="4b6c7-183">A WFP fornece componentes de modo de usuário e de modo kernel para que ISVs de terceiros possam participar das decisões de filtragem que ocorrem em várias camadas na pilha do protocolo TCP/IP e em todo o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-183">WFP provides user-mode and kernel-mode components so that third-party ISVs can participate in the filtering decisions that take place at several layers in the TCP/IP protocol stack and throughout the operating system.</span></span>
<span data-ttu-id="4b6c7-184">O recurso de redirecionamento de conexão WFP permite que um driver de kernel de texto explicativo WFP redirecione uma conexão localmente para um processo de modo de usuário, execute a inspeção de conteúdo no modo de usuário e encaminhe o conteúdo inspecionado usando uma conexão diferente com o destino original.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-184">The WFP connection redirect feature allows a WFP callout kernel driver to redirect a connection locally to a user-mode process, perform content inspection in user-mode, and forward the inspected content using a different connection to the original destination.</span></span>

<span data-ttu-id="4b6c7-185">O **sio \_ consulta \_ WFP \_ de \_ redirecionamento \_ de conexão do contexto** e vários outros IOCTLs relacionados são componentes do modo de usuário usados para permitir que vários aplicativos de proxy de conexão baseados em WFP inspecionem o mesmo fluxo de tráfego de maneira cooperativa.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-185">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL and several other related IOCTLS are user-mode components used to allow multiple WFP-based connection proxy applications to inspect the same traffic flow in a cooperative manner.</span></span>
<span data-ttu-id="4b6c7-186">Cada agente de inspeção pode Reinspecionar com segurança o tráfego de rede que já foi inspecionado por outro agente de inspeção.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-186">Each inspection agent can safely re-inspect network traffic that has already been inspected by another inspection agent.</span></span>
<span data-ttu-id="4b6c7-187">Com a presença de vários proxies (desenvolvidos por diferentes ISVs, por exemplo), a conexão usada por um proxy para se comunicar com o destino final pode, por sua vez, ser redirecionada por um segundo proxy e essa nova conexão pode ser redirecionada novamente pelo proxy original.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-187">With the presence of multiple proxies (developed by different ISVs, for example) the connection used by one proxy to communicate with the final destination could in turn be redirected by a second proxy, and that new connection could again be redirected by the original proxy.</span></span>
<span data-ttu-id="4b6c7-188">Sem o controle de conexão, a conexão original pode nunca alcançar seu destino final, pois fica presa em um loop de proxy infinito.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-188">Without connection tracking, the original connection might never reach its final destination as it gets stuck in an infinite proxy loop.</span></span>

<span data-ttu-id="4b6c7-189">O **\_ contexto de \_ \_ \_ redirecionamento \_ de conexão WFP de consulta sio** é usado para permitir que vários aplicativos de proxy de conexão baseados em WFP inspecionem o mesmo fluxo de tráfego de maneira cooperativa.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-189">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is used to allow multiple WFP-based connection proxy applications to inspect the same traffic flow in a cooperative manner.</span></span>
<span data-ttu-id="4b6c7-190">Cada agente de inspeção pode Reinspecionar com segurança o tráfego de rede que já foi inspecionado por outro agente de inspeção.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-190">Each inspection agent can safely re-inspect network traffic that has already been inspected by another inspection agent.</span></span>
<span data-ttu-id="4b6c7-191">Com a presença de vários proxies (desenvolvidos por diferentes ISVs, por exemplo), a conexão usada por um proxy para se comunicar com o destino final pode, por sua vez, ser redirecionada por um segundo proxy e essa nova conexão pode ser redirecionada novamente pelo proxy original.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-191">With the presence of multiple proxies (developed by different ISVs, for example) the connection used by one proxy to communicate with the final destination could in turn be redirected by a second proxy, and that new connection could again be redirected by the original proxy.</span></span>
<span data-ttu-id="4b6c7-192">Sem o controle de conexão, a conexão original pode nunca alcançar seu destino final, pois fica presa em um loop de proxy infinito.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-192">Without connection tracking, the original connection might never reach its final destination as it gets stuck in an infinite proxy loop.</span></span>
<span data-ttu-id="4b6c7-193">O **\_ contexto de \_ \_ \_ redirecionamento \_ de conexão WFP de consulta sio** é usado para fornecer rastreamento de conexão com proxy em conexões de soquete redirecionadas.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-193">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is used to provide proxied connection tracking on redirected socket connections.</span></span>
<span data-ttu-id="4b6c7-194">Esse recurso de WFP facilita o rastreamento de registros de redirecionamento do redirecionamento inicial de uma conexão com a conexão final com o destino.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-194">This WFP feature facilitates tracking of redirection records from the initial redirect of a connection to the final connection to the destination.</span></span>

<span data-ttu-id="4b6c7-195">O **sio \_ consulta \_ WFP \_ \_ redirecionar \_ registros** do IOCTL é usado por um serviço de redirecionamento baseado em WFP para recuperar o registro de redirecionamento da conexão de pacote TCP/IP aceita (o Soquete conectado para um soquete TCP ou um soquete UDP, por exemplo) Redirecionado para ele por seu texto explicativo complementar em modo kernel registrado em camadas de **\_ \_ redirecionamento do Ale Connect** em um</span><span class="sxs-lookup"><span data-stu-id="4b6c7-195">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is used by a WFP-based redirect service to retrieve the redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion kernel-mode callout registered at **ALE\_CONNECT\_REDIRECT** layers in a kernel-mode driver.</span></span>
<span data-ttu-id="4b6c7-196">O **\_ contexto de \_ \_ \_ redirecionamento \_ de conexão WFP de consulta sio** é usado por um serviço de redirecionamento baseado em WFP para recuperar o contexto de redirecionamento de um registro de redirecionamento da conexão de pacote TCP/IP aceita (o Soquete conectado para um soquete TCP ou um soquete UDP, por exemplo) Redirecionado para ele por seu balão complementar registrado em camadas de **ALE_CONNECT_REDIRECT** .</span><span class="sxs-lookup"><span data-stu-id="4b6c7-196">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is used by a WFP-based redirect service to retrieve the redirect context for a redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion callout registered at **ALE_CONNECT_REDIRECT** layers.</span></span>
<span data-ttu-id="4b6c7-197">O contexto de redirecionamento é opcional e é usado se o estado de redirecionamento atual de uma conexão é que a conexão foi redirecionada pelo serviço de redirecionamento de chamada ou a conexão foi redirecionada anteriormente pelo serviço de redirecionamento de chamada, mas mais tarde redirecionada novamente por um serviço de redirecionamento diferente.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-197">The redirect context is optional and is used if the current redirection state of a connection is that the connection was redirected by the calling redirect service or the connection was previously redirected by the calling redirect service but later redirected again by a different redirect service.</span></span>
<span data-ttu-id="4b6c7-198">O serviço de redirecionamento transfere o registro de redirecionamento recuperado para o soquete TCP que ele usa para fazer proxy do conteúdo original usando o **sio \_ set \_ WFP \_ Connection \_ Redirect de \_ registros** IOCTL.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-198">The redirect service transfers the retrieved redirect record to the TCP socket it uses to proxy the original content using the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL.</span></span>

<span data-ttu-id="4b6c7-199">Como o contexto de redirecionamento de WFP é um blob de dados de comprimento variável definido pelo serviço de redirecionamento, o chamador pode fornecer um buffer de saída grande (um buffer de 1K apontado pelo parâmetro *lpvOutBuffer* , por exemplo) ou pode passar como um tamanho de buffer de saída no parâmetro *cbOutBuffer* de 0 para consultar o tamanho do buffer necessário para manter o blob retornado.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-199">Since the WFP redirect context is a variable length data blob set by the redirect service, the caller can either supply a large output buffer (a 1K buffer pointed to by the *lpvOutBuffer* parameter, for example) or can pass as an output buffer size in the *cbOutBuffer* parameter of 0 to query the buffer size required to hold the returned blob.</span></span>
<span data-ttu-id="4b6c7-200">Se o tamanho do buffer de saída não for suficiente para manter os dados, as funções [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornarão um **erro de \_ \_ buffer insuficiente** e o tamanho de buffer necessário será retornado no valor apontado pelo parâmetro *lpcbBytesReturned* .</span><span class="sxs-lookup"><span data-stu-id="4b6c7-200">If the output buffer size is not sufficient the hold the data, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** functions will return **ERROR\_INSUFFICIENT\_BUFFER** and the required buffer size will be returned in value pointed to by the *lpcbBytesReturned* parameter.</span></span>

<span data-ttu-id="4b6c7-201">O aplicativo que chama **a \_ consulta sio \_ WF \ P_CONNECTION \_ redirecionar \_ registros** IOCTL não precisa entender o blob que contém os registros de redirecionamento recuperados.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-201">The application calling the **SIO\_QUERY\_WF\P_CONNECTION\_REDIRECT\_RECORDS** IOCTL does not need to understand the blob containing the redirect records retrieved.</span></span>
<span data-ttu-id="4b6c7-202">Este é um blob opaco de dados que o aplicativo precisa recuperar e passar de volta para o novo soquete.</span><span class="sxs-lookup"><span data-stu-id="4b6c7-202">This is an opaque blob of data that the application needs to retrieve and pass back to the new socket.</span></span>

## <a name="see-also"></a><span data-ttu-id="4b6c7-203">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b6c7-203">See also</span></span>

[<span data-ttu-id="4b6c7-204">**Opções de soquete IPPROTO_IP**</span><span class="sxs-lookup"><span data-stu-id="4b6c7-204">**IPPROTO_IP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ip-socket-options)

[<span data-ttu-id="4b6c7-205">**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**</span><span class="sxs-lookup"><span data-stu-id="4b6c7-205">**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**</span></span>](sio-query-wfp-connection-redirect-records.md)

[<span data-ttu-id="4b6c7-206">**SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS**</span><span class="sxs-lookup"><span data-stu-id="4b6c7-206">**SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS**</span></span>](sio-set-wfp-connection-redirect-records.md)

[<span data-ttu-id="4b6c7-207">**SSA**</span><span class="sxs-lookup"><span data-stu-id="4b6c7-207">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="4b6c7-208">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="4b6c7-208">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="4b6c7-209">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="4b6c7-209">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="4b6c7-210">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="4b6c7-210">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="4b6c7-211">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="4b6c7-211">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="4b6c7-212">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="4b6c7-212">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="4b6c7-213">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="4b6c7-213">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
