---
description: O código de controle recupera o valor de pendência de envio ideal para a conexão subjacente.
ms.assetid: 03fe964b-26f7-4af7-83bf-62cc877d01a8
title: SIO_IDEAL_SEND_BACKLOG_QUERY código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 440e42477a8939a62eeb84b800c0fd8feead5aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105816041"
---
# <a name="sio_ideal_send_backlog_query-control-code"></a><span data-ttu-id="a4869-103">SIO_IDEAL_SEND_BACKLOG_QUERY código de controle</span><span class="sxs-lookup"><span data-stu-id="a4869-103">SIO_IDEAL_SEND_BACKLOG_QUERY Control Code</span></span>

## <a name="description"></a><span data-ttu-id="a4869-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4869-104">Description</span></span>

<span data-ttu-id="a4869-105">O código de controle de **consulta da pendência de envio do sio \_ ideal \_ \_ \_** recupera o valor de registro posterior de envio (ISB) ideal para a conexão subjacente.</span><span class="sxs-lookup"><span data-stu-id="a4869-105">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** control code retrieves the ideal send backlog (ISB) value for the underlying connection.</span></span>

<span data-ttu-id="a4869-106">Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="a4869-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_QUERY, // dwIoControlCode
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
  SIO_IDEAL_SEND_BACKLOG_QUERY, // dwIoControlCode
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

## <a name="parameters"></a><span data-ttu-id="a4869-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4869-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="a4869-108">s</span><span class="sxs-lookup"><span data-stu-id="a4869-108">s</span></span>

<span data-ttu-id="a4869-109">Um descritor que identifica um soquete.</span><span class="sxs-lookup"><span data-stu-id="a4869-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="a4869-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="a4869-110">dwIoControlCode</span></span>

<span data-ttu-id="a4869-111">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="a4869-111">The control code for the operation.</span></span>
<span data-ttu-id="a4869-112">Use **a \_ \_ consulta de \_ pendência \_ de envio sio ideal** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="a4869-112">Use **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="a4869-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="a4869-113">lpvInBuffer</span></span>

<span data-ttu-id="a4869-114">Um ponteiro para o buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="a4869-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="a4869-115">Este parâmetro não é usado para esta operação.</span><span class="sxs-lookup"><span data-stu-id="a4869-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="a4869-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="a4869-116">cbInBuffer</span></span>

<span data-ttu-id="a4869-117">O tamanho, em bytes, do buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="a4869-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="a4869-118">Este parâmetro não é usado para esta operação.</span><span class="sxs-lookup"><span data-stu-id="a4869-118">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="a4869-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="a4869-119">lpvOutBuffer</span></span>

<span data-ttu-id="a4869-120">Um ponteiro para o buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="a4869-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="a4869-121">Esse parâmetro deve apontar para um tipo de dados **ULONG** se os parâmetros *lpOverlapped* e *lpCompletionRoutine* forem **nulos**.</span><span class="sxs-lookup"><span data-stu-id="a4869-121">This parameter should point to a **ULONG** data type if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="a4869-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="a4869-122">cbOutBuffer</span></span>

<span data-ttu-id="a4869-123">O tamanho, em bytes, do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="a4869-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="a4869-124">Esse parâmetro deve ter pelo menos o tamanho de um tipo de dados **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="a4869-124">This parameter must be at least the size of a **ULONG** data type.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="a4869-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="a4869-125">lpcbBytesReturned</span></span>

<span data-ttu-id="a4869-126">Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="a4869-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="a4869-127">Se o buffer de saída for muito pequeno, a chamada falhará, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [**WSAEINVAL**](windows-sockets-error-codes-2.md)e o parâmetro *lpcbBytesReturned* apontará para um valor **DWORD** igual a zero.</span><span class="sxs-lookup"><span data-stu-id="a4869-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="a4869-128">Se *lpOverlapped* for **NULL**, o valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* retornado em uma chamada bem-sucedida não poderá ser zero.</span><span class="sxs-lookup"><span data-stu-id="a4869-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="a4869-129">Se o parâmetro *lpOverlapped* não for **nulo** para os soquetes sobrepostos, as operações que não puderem ser concluídas imediatamente serão iniciadas e a conclusão será indicada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="a4869-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="a4869-130">O valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* que é retornado pode ser zero, já que o tamanho dos dados armazenados não pode ser determinado até que a operação sobreposta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="a4869-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="a4869-131">O status final de conclusão pode ser recuperado quando o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="a4869-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="a4869-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="a4869-132">lpvOverlapped</span></span>

<span data-ttu-id="a4869-133">Um ponteiro para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="a4869-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="a4869-134">Se o soquete *s* foi criado sem o atributo sobreposto, o parâmetro *lpOverlapped* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="a4869-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="a4869-135">Se *s* foi aberto com o atributo Overlapped e o parâmetro *LpOverlapped* não for **nulo**, a operação será executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="a4869-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="a4869-136">Nesse caso, o parâmetro *lpOverlapped* deve apontar para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="a4869-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="a4869-137">Para operações sobrepostas, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retorna imediatamente, e o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="a4869-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="a4869-138">Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.</span><span class="sxs-lookup"><span data-stu-id="a4869-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="a4869-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="a4869-139">lpCompletionRoutine</span></span>

<span data-ttu-id="a4869-140">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="a4869-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="a4869-141">Um ponteiro para a rotina de conclusão chamada quando a operação foi concluída (ignorada para soquetes não sobrepostos).</span><span class="sxs-lookup"><span data-stu-id="a4869-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="a4869-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="a4869-142">lpThreadId</span></span>

<span data-ttu-id="a4869-143">Um ponteiro para uma estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a ser usado pelo provedor em uma chamada subsequente para [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="a4869-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="a4869-144">O provedor deve armazenar a estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) referenciada (não o ponteiro para o mesmo) até que a função [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) seja retornada.</span><span class="sxs-lookup"><span data-stu-id="a4869-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="a4869-145">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="a4869-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="a4869-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="a4869-146">lpErrno</span></span>

<span data-ttu-id="a4869-147">Um ponteiro para o código de erro.</span><span class="sxs-lookup"><span data-stu-id="a4869-147">A pointer to the error code.</span></span>

<span data-ttu-id="a4869-148">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="a4869-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="a4869-149">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a4869-149">Return value</span></span>

<span data-ttu-id="a4869-150">Se a operação for concluída com êxito, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará zero.</span><span class="sxs-lookup"><span data-stu-id="a4869-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="a4869-151">Se a operação falhar ou estiver pendente, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará **um \_ erro de soquete**.</span><span class="sxs-lookup"><span data-stu-id="a4869-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="a4869-152">Para obter informações de erro estendidas, chame [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="a4869-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="a4869-153">Código do erro</span><span class="sxs-lookup"><span data-stu-id="a4869-153">Error code</span></span> | <span data-ttu-id="a4869-154">Significado</span><span class="sxs-lookup"><span data-stu-id="a4869-154">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="a4869-155">**\_e/s de WSA \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="a4869-155">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="a4869-156">Uma operação sobreposta foi iniciada com êxito e a conclusão será indicada em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="a4869-156">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="a4869-157">**operação de WSA \_ \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="a4869-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="a4869-158">Uma operação sobreposta foi cancelada devido ao fechamento do soquete ou à execução do comando **sio \_ flush** IOCTL.</span><span class="sxs-lookup"><span data-stu-id="a4869-158">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="a4869-159">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="a4869-159">**WSAEFAULT**</span></span> | <span data-ttu-id="a4869-160">O parâmetro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço de usuário.</span><span class="sxs-lookup"><span data-stu-id="a4869-160">The *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="a4869-161">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="a4869-161">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="a4869-162">A função é invocada quando um retorno de chamada está em andamento.</span><span class="sxs-lookup"><span data-stu-id="a4869-162">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="a4869-163">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="a4869-163">**WSAEINTR**</span></span> | <span data-ttu-id="a4869-164">Uma operação de bloqueio foi interrompida.</span><span class="sxs-lookup"><span data-stu-id="a4869-164">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="a4869-165">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="a4869-165">**WSAEINVAL**</span></span> | <span data-ttu-id="a4869-166">O parâmetro *dwIoControlCode* não é um comando válido ou um parâmetro de entrada especificado não é aceitável ou o comando não é aplicável ao tipo de soquete especificado.</span><span class="sxs-lookup"><span data-stu-id="a4869-166">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="a4869-167">Esse erro será retornado se o parâmetro *cbOutBuffer* for menor que o tamanho de um tipo de dados **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="a4869-167">This error is returned if the *cbOutBuffer* parameter is less than the size of a **ULONG** data type.</span></span>
| <span data-ttu-id="a4869-168">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="a4869-168">**WSAENETDOWN**</span></span> | <span data-ttu-id="a4869-169">Falha no subsistema de rede.</span><span class="sxs-lookup"><span data-stu-id="a4869-169">The network subsystem has failed.</span></span> |
| <span data-ttu-id="a4869-170">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="a4869-170">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="a4869-171">Não há suporte para a opção de soquete no protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="a4869-171">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="a4869-172">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="a4869-172">**WSAENOTCONN**</span></span> | <span data-ttu-id="a4869-173">O Soquete s não está conectado.</span><span class="sxs-lookup"><span data-stu-id="a4869-173">The socket s is not connected.</span></span> |
| <span data-ttu-id="a4869-174">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="a4869-174">**WSAENOTSOCK**</span></span> | <span data-ttu-id="a4869-175">O descritor *s* não é um soquete.</span><span class="sxs-lookup"><span data-stu-id="a4869-175">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="a4869-176">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="a4869-176">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="a4869-177">Não há suporte para o comando IOCTL especificado.</span><span class="sxs-lookup"><span data-stu-id="a4869-177">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="a4869-178">Esse erro será retornado se a **\_ consulta de \_ \_ pendência \_ de envio sio ideal** não tiver suporte do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="a4869-178">This error is returned if the **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="a4869-179">Esse erro também é retornado quando uma tentativa de usar a **\_ consulta de \_ \_ pendência \_ de envio sio ideal** é feita em um soquete de datagrama.</span><span class="sxs-lookup"><span data-stu-id="a4869-179">This error is also returned when an attempt to use the **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is made on a datagram socket.</span></span> |

## <a name="remarks"></a><span data-ttu-id="a4869-180">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4869-180">Remarks</span></span>

<span data-ttu-id="a4869-181">O IOCTL de **\_ consulta de pendência de \_ envio \_ \_ sio ideal** tem suporte no Windows Server 2008, no Windows Vista com Service Pack 1 (SP1) e em versões posteriores do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a4869-181">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is supported on Windows Server 2008, Windows Vista with Service Pack 1 (SP1), and later versions of the operating system.</span></span>

<span data-ttu-id="a4869-182">Ao enviar dados por uma conexão TCP usando o Windows Sockets, é importante manter uma quantidade suficiente de dados pendentes (enviados mas não confirmados ainda) no TCP para alcançar a taxa de transferência mais alta.</span><span class="sxs-lookup"><span data-stu-id="a4869-182">When sending data over a TCP connection using Windows sockets, it is important to keep a sufficient amount of data outstanding (sent but not acknowledged yet) in TCP in order to achieve the highest throughput.</span></span>
<span data-ttu-id="a4869-183">O valor ideal para a quantidade de dados pendentes para atingir a melhor taxa de transferência para a conexão TCP é chamado de tamanho ideal de envio de pendências (ISB).</span><span class="sxs-lookup"><span data-stu-id="a4869-183">The ideal value for the amount of data outstanding to achieve the best throughput for the TCP connection is called the ideal send backlog (ISB) size.</span></span>
<span data-ttu-id="a4869-184">O valor ISB é uma função do produto de atraso de largura de banda da conexão TCP e da janela de recebimento anunciada do receptor (e parcialmente a quantidade de congestionamento na rede).</span><span class="sxs-lookup"><span data-stu-id="a4869-184">The ISB value is a function of the bandwidth-delay product of the TCP connection and the receiver's advertised receive window (and partly the amount of congestion in the network).</span></span>

<span data-ttu-id="a4869-185">O valor do ISB por conexão está disponível na implementação do protocolo TCP no Windows Server 2008, no Windows Vista com SP1 e em versões posteriores do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a4869-185">The ISB value per connection is available from the TCP protocol implementation in Windows Server 2008, Windows Vista with SP1, and later versions of the operating system.</span></span>
<span data-ttu-id="a4869-186">O IOCTL de **\_ consulta de pendência de \_ envio \_ \_ sio ideal** pode ser usado por um aplicativo para receber uma notificação quando o valor do ISB é alterado dinamicamente para uma conexão.</span><span class="sxs-lookup"><span data-stu-id="a4869-186">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL can be used by an application to get a notification when the ISB value changes dynamically for a connection.</span></span>

<span data-ttu-id="a4869-187">No Windows Server 2008, no Windows Vista com SP1 e em versões posteriores do sistema operacional, a [**sio ideal de enviar lista de \_ \_ \_ pendências de envio \_**](sio-ideal-send-backlog-change.md) e sio ideais de envio de consulta da lista de **\_ \_ \_ pendências \_** têm suporte em soquetes orientados a fluxo que estão em um estado conectado.</span><span class="sxs-lookup"><span data-stu-id="a4869-187">On Windows Server 2008, Windows Vista with SP1, and later versions of the operating system, the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs are supported on stream-oriented sockets that are in a connected state.</span></span>

<span data-ttu-id="a4869-188">Teoricamente, o intervalo para o valor do ISB para uma conexão TCP pode variar de 0 a um máximo de 16 megabytes.</span><span class="sxs-lookup"><span data-stu-id="a4869-188">The range for the ISB value for a TCP connection can theoretically vary from 0 to a maximum of 16 megabytes.</span></span>

<span data-ttu-id="a4869-189">O uso típico do [**sio \_ ideal de \_ Enviar \_ pendências \_ de envio**](sio-ideal-send-backlog-change.md) e de **sio ideais de \_ \_ \_ \_ consulta de pendências de envio** é baseado no método Send usado pelos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="a4869-189">The typical usage of the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs is based on the send method used by the applications.</span></span>
<span data-ttu-id="a4869-190">Dois casos comuns são discutidos.</span><span class="sxs-lookup"><span data-stu-id="a4869-190">Two common cases are discussed.</span></span>

<span data-ttu-id="a4869-191">Os aplicativos que executam um bloqueio ou solicitação de envio sem bloqueio por vez normalmente dependem do buffer de envio interno pelo Winsock para obter uma taxa de transferência razoável.</span><span class="sxs-lookup"><span data-stu-id="a4869-191">Applications that perform one blocking or non-blocking send request at a time typically rely on internal send buffering by Winsock to achieve decent throughput.</span></span>
<span data-ttu-id="a4869-192">O limite do buffer de envio para uma determinada conexão é controlado pela opção de soquete **\_ SNDBUF** .</span><span class="sxs-lookup"><span data-stu-id="a4869-192">The send buffer limit for a given connection is controlled by the **SO\_SNDBUF** socket option.</span></span>
<span data-ttu-id="a4869-193">Para o método Send de bloqueio e sem bloqueio, o limite do buffer de envio determina a quantidade de dados mantida pendente no TCP.</span><span class="sxs-lookup"><span data-stu-id="a4869-193">For the blocking and non-blocking send method, the send buffer limit determines how much data is kept outstanding in TCP.</span></span>
<span data-ttu-id="a4869-194">Se o valor do ISB para a conexão for maior que o limite do buffer de envio, a taxa de transferência obtida na conexão não será ideal.</span><span class="sxs-lookup"><span data-stu-id="a4869-194">If the ISB value for the connection is larger than the send buffer limit, then the throughput achieved on the connection will not be optimal.</span></span>
<span data-ttu-id="a4869-195">Para obter uma melhor taxa de transferência, os aplicativos podem definir o limite do buffer de envio com base no resultado da consulta do ISB conforme as notificações de alteração do ISB ocorrem na conexão.</span><span class="sxs-lookup"><span data-stu-id="a4869-195">In order to achieve better throughput, the applications can set the send buffer limit based on the result of the ISB query as ISB change notifications occur on the connection.</span></span>

<span data-ttu-id="a4869-196">Para aplicativos que usam o método de envio sobreposto com várias solicitações Send pendentes, a quantidade de dados mantidas pendentes no TCP é determinada pelo limite do buffer de envio no Winsock e pela quantidade total de dados contidos nas solicitações de envio sobrepostas pendentes.</span><span class="sxs-lookup"><span data-stu-id="a4869-196">For applications that use the overlapped send method with multiple send requests outstanding, the amount of data kept outstanding in TCP is determined by the send buffer limit in Winsock and the total amount of data contained in the outstanding overlapped send requests.</span></span>
<span data-ttu-id="a4869-197">Nesse caso, os aplicativos devem usar o valor ISB para determinar quantas solicitações de envio pendentes devem ser mantidas e qual deve ser o tamanho dos dados de cada solicitação de envio.</span><span class="sxs-lookup"><span data-stu-id="a4869-197">In this case, applications should use the ISB value to determine how many outstanding send requests they should keep and what the data size for each send request should be.</span></span>
<span data-ttu-id="a4869-198">O ideal é que o aplicativo tente manter a equação a seguir satisfeita:</span><span class="sxs-lookup"><span data-stu-id="a4869-198">Ideally, the application should try to keep the following equation satisfied:</span></span>

`ISB value == send buffer limit + (number of simultaneous overlapped send requests * data length per send request)`

<span data-ttu-id="a4869-199">Observe que usar os IOCTLs do ISB sobre Soquetes TCP na maneira acima pode levar a um aumento no uso de memória no Exchange para maior taxa de transferência em conexões com um produto de atraso de largura de banda alta.</span><span class="sxs-lookup"><span data-stu-id="a4869-199">Note that using the ISB IOCTLs over TCP sockets in the above fashion can lead to increased memory usage in exchange for increased throughput on connections with a high bandwidth-delay product.</span></span>
<span data-ttu-id="a4869-200">A implementação TCP no Windows limitará os valores do ISB conforme necessário com base no uso geral da memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="a4869-200">The TCP implementation in Windows will throttle ISB values as necessary based on overall system memory usage.</span></span>

<span data-ttu-id="a4869-201">O IOCTL de **\_ consulta de pendência de \_ envio \_ \_ sio ideal** é permitido somente em um soquete de fluxo que está no estado conectado.</span><span class="sxs-lookup"><span data-stu-id="a4869-201">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is allowed only on a stream socket that is in the connected state.</span></span>
<span data-ttu-id="a4869-202">Caso contrário, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** falhará com **WSAENOTCONN**.</span><span class="sxs-lookup"><span data-stu-id="a4869-202">Otherwise the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function will fail with **WSAENOTCONN**.</span></span>

<span data-ttu-id="a4869-203">Qualquer IOCTL pode bloquear indefinidamente, dependendo da implementação do provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="a4869-203">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="a4869-204">Se o aplicativo não puder tolerar o bloqueio em uma chamada de função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** , a e/s sobreposta seria ACONSELHAda para os IOCTLs que são especialmente prováveis de bloquear.</span><span class="sxs-lookup"><span data-stu-id="a4869-204">If the application cannot tolerate blocking in a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="a4869-205">A **\_ consulta de \_ \_ pendência de \_ envio sio ideal** não é provavelmente bloqueada, portanto, ela normalmente é chamada de forma síncrona com os parâmetros *lpOverlapped* e *lpCompletionRoutine* definidos como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a4869-205">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is not likely to block so it is normally called synchronously with the *lpOverlapped* and *lpCompletionRoutine* parameters set to **NULL**.</span></span>

<span data-ttu-id="a4869-206">O IOCTL de **consulta de pendência de \_ \_ envio \_ \_ sio ideal** pode falhar com a operação **WSAEINTR** ou **WSA \_ \_ anulada** nos seguintes casos:</span><span class="sxs-lookup"><span data-stu-id="a4869-206">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

<span data-ttu-id="a4869-207">A conexão TCP é desconectada normalmente na direção de envio.</span><span class="sxs-lookup"><span data-stu-id="a4869-207">The TCP connection is gracefully disconnected in the send direction.</span></span>
<span data-ttu-id="a4869-208">Isso pode ocorrer como resultado de uma chamada para a função de desligamento com o parâmetro de como definido como **SD \_ Send**, uma chamada para a função **DisconnectEx** ou uma chamada para a função **TransmitFile** ou **TransmitPackets** com o parâmetro *dwFlags* definido como **TF \_ Disconnect** ou **TF \_ reutilization**.</span><span class="sxs-lookup"><span data-stu-id="a4869-208">This can occur as a result of a call to shutdown function with the how parameter set to **SD\_SEND**, a call to the **DisconnectEx** function, or a call to the **TransmitFile** or **TransmitPackets** function with *dwFlags* parameter set to **TF\_DISCONNECT** or **TF\_REUSE**.</span></span>
<span data-ttu-id="a4869-209">A conexão TCP foi redefinida ou anulada.</span><span class="sxs-lookup"><span data-stu-id="a4869-209">The TCP connection has been reset or aborted.</span></span>
<span data-ttu-id="a4869-210">A solicitação é cancelada pelo Gerenciador de e/s.</span><span class="sxs-lookup"><span data-stu-id="a4869-210">The request is canceled by the I/O Manager.</span></span>

<span data-ttu-id="a4869-211">Duas funções de wrapper embutidas para esses IOCTLs são definidas no arquivo de cabeçalho *Ws2tcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="a4869-211">Two inline wrapper functions for these IOCTLs are defined in the *Ws2tcpip.h* header file.</span></span>
<span data-ttu-id="a4869-212">É recomendável que essas funções embutidas sejam usadas em vez de usar a consulta de [**\_ pendência de envio sio ideal \_ \_ \_**](sio-ideal-send-backlog-change.md) e o **sio \_ ideal \_ Enviar \_ \_ consultas de pendências** para os IOCTLs diretamente.</span><span class="sxs-lookup"><span data-stu-id="a4869-212">It is recommended that these inline functions be used instead of using the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs directly.</span></span>

<span data-ttu-id="a4869-213">A função de wrapper embutido para o [**sio \_ ideal \_ Enviar \_ registro da pendência de \_ alteração**](sio-ideal-send-backlog-change.md) do IOCTL é a função **idealsendbacklognotify** .</span><span class="sxs-lookup"><span data-stu-id="a4869-213">The inline wrapper function for the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) IOCTL is the **idealsendbacklognotify** function.</span></span>

<span data-ttu-id="a4869-214">A função de wrapper embutida para a **consulta de pendência de \_ \_ envio sio \_ \_ ideal** é a função **idealsendbacklogquery** .</span><span class="sxs-lookup"><span data-stu-id="a4869-214">The inline wrapper function for the **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is the **idealsendbacklogquery** function.</span></span>

<span data-ttu-id="a4869-215">O buffer de envio dinâmico para TCP foi adicionado no Windows 7 e no Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="a4869-215">Dynamic send buffering for TCP was added on Windows 7 and Windows Server 2008 R2.</span></span>
<span data-ttu-id="a4869-216">Por padrão, o buffer de envio dinâmico para TCP é habilitado, a menos que um aplicativo defina a opção de soquete **\_ SNDBUF** no soquete de fluxo.</span><span class="sxs-lookup"><span data-stu-id="a4869-216">By default, dynamic send buffering for TCP is enabled unless an application sets the **SO\_SNDBUF** socket option on the stream socket.</span></span>

<span data-ttu-id="a4869-217">Usar o netsh é o método recomendado para consultar ou definir o buffer de envio dinâmico para TCP.</span><span class="sxs-lookup"><span data-stu-id="a4869-217">Using netsh is the recommended method to query or set dynamic send buffering for TCP.</span></span>

<span data-ttu-id="a4869-218">O valor atual para o buffer de envio dinâmico para TCP pode ser recuperado usando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="a4869-218">The current value for dynamic send buffering for TCP can be retrieved using the following command:</span></span>

`netsh winsock show autotuning`

<span data-ttu-id="a4869-219">O buffer de envio dinâmico para TCP pode ser desabilitado usando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="a4869-219">Dynamic send buffering for TCP can be disabled using the following command:</span></span>

`netsh winsock set autotuning off`

<span data-ttu-id="a4869-220">O buffer de envio dinâmico para TCP pode ser habilitado usando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="a4869-220">Dynamic send buffering for TCP can be enabled using the following command:</span></span>

`netsh winsock set autotuning on`

<span data-ttu-id="a4869-221">Embora não seja recomendado, o buffer de envio dinâmico pode ser desabilitado em um aplicativo definindo o seguinte valor de registro como zero:</span><span class="sxs-lookup"><span data-stu-id="a4869-221">While it is discouraged, dynamic send buffering can be disabled from an application by setting the following registry value to zero:</span></span>

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\AFD\Parameters\DynamicSendBufferDisable`

<span data-ttu-id="a4869-222">Ao alterar o valor de buffer de envio dinâmico usando NetSh.exe ou alterar o valor do registro, o computador deve ser reiniciado para que a alteração entre em vigor.</span><span class="sxs-lookup"><span data-stu-id="a4869-222">When changing the value for dynamic send buffering using NetSh.exe or changing the registry value, the computer must be restarted for the change to take effect.</span></span>

<span data-ttu-id="a4869-223">Com o buffer de envio dinâmico no Windows 7 e no Windows Server 2008 R2, o uso da consulta de [**\_ pendência de envio sio ideal \_ \_ \_**](sio-ideal-send-backlog-change.md) e os IOCTLs de **\_ \_ \_ \_ consultas pendentes de envio da lista de pendências sio ideais** são necessários apenas em circunstâncias especiais.</span><span class="sxs-lookup"><span data-stu-id="a4869-223">With dynamic send buffering on Windows 7 and Windows Server 2008 R2, the use of the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs are needed only in special circumstances.</span></span>

## <a name="see-also"></a><span data-ttu-id="a4869-224">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4869-224">See also</span></span>

[<span data-ttu-id="a4869-225">**SIO_IDEAL_SEND_BACKLOG_CHANGE**</span><span class="sxs-lookup"><span data-stu-id="a4869-225">**SIO_IDEAL_SEND_BACKLOG_CHANGE**</span></span>](sio-ideal-send-backlog-change.md)

[<span data-ttu-id="a4869-226">**SSA**</span><span class="sxs-lookup"><span data-stu-id="a4869-226">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="a4869-227">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="a4869-227">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="a4869-228">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="a4869-228">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="a4869-229">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="a4869-229">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="a4869-230">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="a4869-230">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="a4869-231">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="a4869-231">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="a4869-232">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="a4869-232">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
