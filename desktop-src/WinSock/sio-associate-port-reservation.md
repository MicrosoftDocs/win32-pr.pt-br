---
description: O código de controle associa um soquete a uma reserva persistente ou de tempo de execução para um bloco de TCP ou UDP identificado pelo token de reserva de porta.
ms.assetid: 4CBFB5F8-1FA1-44BA-9932-6F0329A465CB
title: SIO_ASSOCIATE_PORT_RESERVATION código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 69af4f396fabd32f948d7e43cbf348aa34fb1a9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170775"
---
# <a name="sio_associate_port_reservation-control-code"></a><span data-ttu-id="a2971-103">SIO_ASSOCIATE_PORT_RESERVATION código de controle</span><span class="sxs-lookup"><span data-stu-id="a2971-103">SIO_ASSOCIATE_PORT_RESERVATION Control Code</span></span>

## <a name="description"></a><span data-ttu-id="a2971-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="a2971-104">Description</span></span>

<span data-ttu-id="a2971-105">O código de controle de **\_ \_ \_ reserva de porta sio** associa um soquete com uma reserva persistente ou de tempo de execução para um bloco de TCP ou UDP identificado pelo token de reserva de porta.</span><span class="sxs-lookup"><span data-stu-id="a2971-105">The **SIO\_ASSOCIATE\_PORT\_RESERVATION** control code associates a socket with a persistent or runtime reservation for a block of TCP or UDP identified by the port reservation token.</span></span>
<span data-ttu-id="a2971-106">Esse IOCTL deve ser emitido antes do soquete ser associado.</span><span class="sxs-lookup"><span data-stu-id="a2971-106">This IOCTL must be issued before the socket is bound.</span></span>
<span data-ttu-id="a2971-107">Se e quando o soquete estiver associado, a porta atribuída a ele será selecionada na reserva de porta identificada pelo token fornecido.</span><span class="sxs-lookup"><span data-stu-id="a2971-107">If and when the socket is bound, the port assigned to it will be selected from the port reservation identified by the given token.</span></span>
<span data-ttu-id="a2971-108">Se nenhuma porta estiver disponível na reserva especificada, a chamada de função de [**Associação**](/windows/desktop/api/winsock/nf-winsock-bind) falhará.</span><span class="sxs-lookup"><span data-stu-id="a2971-108">If no ports are available from the specified reservation, the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function call will fail.</span></span>

<span data-ttu-id="a2971-109">Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="a2971-109">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ASSOCIATE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RESERVATION_TOKEN
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ASSOCIATE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RESERVATION_TOKEN
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="a2971-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2971-110">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="a2971-111">s</span><span class="sxs-lookup"><span data-stu-id="a2971-111">s</span></span>

<span data-ttu-id="a2971-112">Um descritor que identifica um soquete.</span><span class="sxs-lookup"><span data-stu-id="a2971-112">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="a2971-113">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="a2971-113">dwIoControlCode</span></span>

<span data-ttu-id="a2971-114">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="a2971-114">The control code for the operation.</span></span>
<span data-ttu-id="a2971-115">Use **a \_ \_ \_ reserva de porta associada do sio** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="a2971-115">Use **SIO\_ASSOCIATE\_PORT\_RESERVATION** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="a2971-116">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="a2971-116">lpvInBuffer</span></span>

<span data-ttu-id="a2971-117">Um ponteiro para o buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="a2971-117">A pointer to the input buffer.</span></span>
<span data-ttu-id="a2971-118">Esse parâmetro contém um ponteiro para uma estrutura de [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) com o token para a reserva de porta TCP ou UDP a ser associada ao soquete.</span><span class="sxs-lookup"><span data-stu-id="a2971-118">This parameter contains a pointer to an [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) structure with the token for the TCP or UDP port reservation to associate with the socket.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="a2971-119">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="a2971-119">cbInBuffer</span></span>

<span data-ttu-id="a2971-120">O tamanho, em bytes, do buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="a2971-120">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="a2971-121">Esse parâmetro deve ter pelo menos o tamanho da estrutura de [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) .</span><span class="sxs-lookup"><span data-stu-id="a2971-121">This parameter must be at least the size of the [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) structure.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="a2971-122">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="a2971-122">lpvOutBuffer</span></span>

<span data-ttu-id="a2971-123">Um ponteiro para o buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="a2971-123">A pointer to the output buffer.</span></span>
<span data-ttu-id="a2971-124">Este parâmetro não é usado para esta operação.</span><span class="sxs-lookup"><span data-stu-id="a2971-124">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="a2971-125">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="a2971-125">cbOutBuffer</span></span>

<span data-ttu-id="a2971-126">O tamanho, em bytes, do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="a2971-126">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="a2971-127">Esse parâmetro deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="a2971-127">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="a2971-128">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="a2971-128">lpcbBytesReturned</span></span>

<span data-ttu-id="a2971-129">Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="a2971-129">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="a2971-130">Se o buffer de saída for muito pequeno, a chamada falhará, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [**WSAEINVAL**](windows-sockets-error-codes-2.md)e o parâmetro *lpcbBytesReturned* apontará para um valor **DWORD** igual a zero.</span><span class="sxs-lookup"><span data-stu-id="a2971-130">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="a2971-131">Se *lpOverlapped* for **NULL**, o valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* retornado em uma chamada bem-sucedida não poderá ser zero.</span><span class="sxs-lookup"><span data-stu-id="a2971-131">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="a2971-132">Se o parâmetro *lpOverlapped* não for **nulo** para os soquetes sobrepostos, as operações que não puderem ser concluídas imediatamente serão iniciadas e a conclusão será indicada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="a2971-132">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="a2971-133">O valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* que é retornado pode ser zero, já que o tamanho dos dados armazenados não pode ser determinado até que a operação sobreposta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="a2971-133">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="a2971-134">O status final de conclusão pode ser recuperado quando o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="a2971-134">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="a2971-135">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="a2971-135">lpvOverlapped</span></span>

<span data-ttu-id="a2971-136">Um ponteiro para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="a2971-136">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="a2971-137">Se o soquete *s* foi criado sem o atributo sobreposto, o parâmetro *lpOverlapped* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="a2971-137">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="a2971-138">Se *s* foi aberto com o atributo Overlapped e o parâmetro *LpOverlapped* não for **nulo**, a operação será executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="a2971-138">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="a2971-139">Nesse caso, o parâmetro *lpOverlapped* deve apontar para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="a2971-139">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="a2971-140">Para operações sobrepostas, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retorna imediatamente, e o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="a2971-140">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="a2971-141">Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.</span><span class="sxs-lookup"><span data-stu-id="a2971-141">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="a2971-142">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="a2971-142">lpCompletionRoutine</span></span>

<span data-ttu-id="a2971-143">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="a2971-143">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="a2971-144">Um ponteiro para a rotina de conclusão chamada quando a operação foi concluída (ignorada para soquetes não sobrepostos).</span><span class="sxs-lookup"><span data-stu-id="a2971-144">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="a2971-145">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="a2971-145">lpThreadId</span></span>

<span data-ttu-id="a2971-146">Um ponteiro para uma estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a ser usado pelo provedor em uma chamada subsequente para [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="a2971-146">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="a2971-147">O provedor deve armazenar a estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) referenciada (não o ponteiro para o mesmo) até que a função [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) seja retornada.</span><span class="sxs-lookup"><span data-stu-id="a2971-147">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="a2971-148">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="a2971-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="a2971-149">lpErrno</span><span class="sxs-lookup"><span data-stu-id="a2971-149">lpErrno</span></span>

<span data-ttu-id="a2971-150">Um ponteiro para o código de erro.</span><span class="sxs-lookup"><span data-stu-id="a2971-150">A pointer to the error code.</span></span>

<span data-ttu-id="a2971-151">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="a2971-151">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="a2971-152">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a2971-152">Return value</span></span>

<span data-ttu-id="a2971-153">Se a operação for concluída com êxito, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará zero.</span><span class="sxs-lookup"><span data-stu-id="a2971-153">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="a2971-154">Se a operação falhar ou estiver pendente, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará **um \_ erro de soquete**.</span><span class="sxs-lookup"><span data-stu-id="a2971-154">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="a2971-155">Para obter informações de erro estendidas, chame [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="a2971-155">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="a2971-156">Código do erro</span><span class="sxs-lookup"><span data-stu-id="a2971-156">Error code</span></span> | <span data-ttu-id="a2971-157">Significado</span><span class="sxs-lookup"><span data-stu-id="a2971-157">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="a2971-158">**\_e/s de WSA \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="a2971-158">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="a2971-159">A operação de e/s sobreposta está em andamento.</span><span class="sxs-lookup"><span data-stu-id="a2971-159">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="a2971-160">Esse valor será retornado se uma operação sobreposta tiver sido iniciada com êxito e a conclusão será indicada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="a2971-160">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="a2971-161">**operação de WSA \_ \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="a2971-161">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="a2971-162">A operação de e/s foi anulada devido a uma saída de thread ou uma solicitação de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a2971-162">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="a2971-163">Esse erro será retornado se uma operação sobreposta tiver sido cancelada devido ao fechamento do soquete ou à execução do comando **sio \_ flush IOCTL** .</span><span class="sxs-lookup"><span data-stu-id="a2971-163">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH IOCTL** command.</span></span> |
| <span data-ttu-id="a2971-164">**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="a2971-164">**WSAEACCES**</span></span> | <span data-ttu-id="a2971-165">Foi feita uma tentativa de acessar um soquete de uma maneira proibida por suas permissões de acesso.</span><span class="sxs-lookup"><span data-stu-id="a2971-165">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span> <span data-ttu-id="a2971-166">Esse erro é retornado sob várias condições para reservas de porta persistentes que incluem o seguinte: o usuário não tem os privilégios administrativos necessários no computador local ou o aplicativo não está sendo executado em um shell avançado como o administrador interno ( `RunAs administrator` ).</span><span class="sxs-lookup"><span data-stu-id="a2971-166">This error is returned under several conditions for persistent port reservations that include the following: the user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (`RunAs administrator`).</span></span> |
| <span data-ttu-id="a2971-167">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="a2971-167">**WSAEFAULT**</span></span> | <span data-ttu-id="a2971-168">O sistema detectou um endereço de ponteiro inválido ao tentar usar um argumento de ponteiro em uma chamada.</span><span class="sxs-lookup"><span data-stu-id="a2971-168">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="a2971-169">Esse erro é retornado do parâmetro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço de usuário.</span><span class="sxs-lookup"><span data-stu-id="a2971-169">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="a2971-170">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="a2971-170">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="a2971-171">Uma operação de bloqueio está atualmente em execução.</span><span class="sxs-lookup"><span data-stu-id="a2971-171">A blocking operation is currently executing.</span></span> <span data-ttu-id="a2971-172">Esse erro será retornado se a função for invocada quando um retorno de chamada estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="a2971-172">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="a2971-173">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="a2971-173">**WSAEINTR**</span></span> | <span data-ttu-id="a2971-174">Uma operação de bloqueio foi interrompida por uma chamada para [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span><span class="sxs-lookup"><span data-stu-id="a2971-174">A blocking operation was interrupted by a call to [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span></span> <span data-ttu-id="a2971-175">Esse erro será retornado se uma operação de bloqueio tiver sido interrompida.</span><span class="sxs-lookup"><span data-stu-id="a2971-175">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="a2971-176">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="a2971-176">**WSAEINVAL**</span></span> | <span data-ttu-id="a2971-177">Foi fornecido um argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="a2971-177">An invalid argument was supplied.</span></span> <span data-ttu-id="a2971-178">Esse erro será retornado se o parâmetro *dwIoControlCode* não for um comando válido ou se um parâmetro de entrada especificado não for aceitável ou se o comando não for aplicável ao tipo de soquete especificado.</span><span class="sxs-lookup"><span data-stu-id="a2971-178">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="a2971-179">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="a2971-179">**WSAENETDOWN**</span></span> | <span data-ttu-id="a2971-180">Uma operação de soquete encontrou uma rede inoperante.</span><span class="sxs-lookup"><span data-stu-id="a2971-180">A socket operation encountered a dead network.</span></span> <span data-ttu-id="a2971-181">Esse erro será retornado se o subsistema de rede tiver falhado.</span><span class="sxs-lookup"><span data-stu-id="a2971-181">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="a2971-182">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="a2971-182">**WSAENOTSOCK**</span></span> | <span data-ttu-id="a2971-183">Uma operação foi tentada em algo que não é um soquete.</span><span class="sxs-lookup"><span data-stu-id="a2971-183">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="a2971-184">Esse erro será retornado se o descritor *s* não for um soquete.</span><span class="sxs-lookup"><span data-stu-id="a2971-184">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="a2971-185">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="a2971-185">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="a2971-186">Não há suporte para a operação tentada para o tipo de objeto referenciado.</span><span class="sxs-lookup"><span data-stu-id="a2971-186">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="a2971-187">Esse erro será retornado se o comando IOCTL especificado não tiver suporte.</span><span class="sxs-lookup"><span data-stu-id="a2971-187">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="a2971-188">Esse erro também será retornado se o **sio \_ associar \_ a \_ reserva de porta** IOCTL não for suportado pelo provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="a2971-188">This error is also returned if the **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="a2971-189">Esse erro também é retornado quando uma tentativa de usar o **IOCTL \_ \_ \_ reserva de porta de associação sio** é feita em um soquete diferente de UDP ou TCP.</span><span class="sxs-lookup"><span data-stu-id="a2971-189">This error is also returned when an attempt to use the **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL is made on a socket other than UDP or TCP.</span></span> |

## <a name="remarks"></a><span data-ttu-id="a2971-190">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2971-190">Remarks</span></span>

<span data-ttu-id="a2971-191">O **sio \_ associar \_ a \_ reserva de porta** IOCTL tem suporte no Windows Vista e em versões posteriores do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a2971-191">The **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL is supported on Windows Vista and later versions of the operating system.</span></span>

<span data-ttu-id="a2971-192">Os aplicativos e serviços que precisam reservar portas se enquadram em duas categorias.</span><span class="sxs-lookup"><span data-stu-id="a2971-192">Applications and services which need to reserve ports fall into two categories.</span></span>
<span data-ttu-id="a2971-193">A primeira categoria inclui componentes que precisam de uma porta específica como parte de sua operação.</span><span class="sxs-lookup"><span data-stu-id="a2971-193">The first category includes components which need a particular port as part of their operation.</span></span>
<span data-ttu-id="a2971-194">Esses componentes geralmente preferem especificar a porta necessária no momento da instalação (em um manifesto do aplicativo, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="a2971-194">Such components will generally prefer to specify their required port at installation time (in an application manifest, for example).</span></span>
<span data-ttu-id="a2971-195">A segunda categoria inclui componentes que precisam de qualquer porta disponível ou bloco de portas em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="a2971-195">The second category includes components which need any available port or block of ports at runtime.</span></span>
<span data-ttu-id="a2971-196">Essas duas categorias correspondem a solicitações específicas e de reserva de porta curinga.</span><span class="sxs-lookup"><span data-stu-id="a2971-196">These two categories correspond to specific and wildcard port reservation requests.</span></span>
<span data-ttu-id="a2971-197">As solicitações de reserva específicas podem ser persistentes ou tempo de execução, enquanto as solicitações de reserva de porta curinga só têm suporte em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="a2971-197">Specific reservation requests may be persistent or runtime, while wildcard port reservation requests are only supported at runtime.</span></span>

<span data-ttu-id="a2971-198">O IOCTL de reserva de porta de associação de sio é usado para associar uma reserva de porta TCP ou UDP a uma reserva persistente ou de tempo de execução. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a2971-198">The **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL is used to associate a TCP or UDP port reservation with either a persistent or runtime reservation.</span></span>

<span data-ttu-id="a2971-199">A função [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) ou [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) fornece a capacidade de um aplicativo ou serviço reservar um bloco persistente de portas TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="a2971-199">The [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) or [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) function provides the ability for an application or service to reserve a persistent block of TCP or UDP ports.</span></span>
<span data-ttu-id="a2971-200">As reservas de porta persistentes são registradas em um repositório persistente para o módulo TCP ou UDP no Windows.</span><span class="sxs-lookup"><span data-stu-id="a2971-200">Persistent port reservations are recorded in a persistent store for the TCP or UDP module in Windows.</span></span>
<span data-ttu-id="a2971-201">Observe que o token de uma determinada reserva de porta persistente pode ser alterado cada vez que o sistema é reiniciado.</span><span class="sxs-lookup"><span data-stu-id="a2971-201">Note that the token for a given persistent port reservation may change each time the system is restarted.</span></span>

<span data-ttu-id="a2971-202">Depois que uma reserva de porta TCP ou UDP persistente tiver sido obtida, um aplicativo poderá solicitar atribuições de porta da reserva de porta abrindo um soquete TCP ou UDP e, em seguida, chamando a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) especificando o IOCTL de **reserva de \_ porta de associação \_ \_ sio** e passando o token de reserva antes de emitir uma chamada para a função de [**Associação**](/windows/desktop/api/winsock/nf-winsock-bind) no soquete.</span><span class="sxs-lookup"><span data-stu-id="a2971-202">Once a persistent TCP or UDP port reservation has been obtained, an application can request port assignments from the port reservation by opening a TCP or UDP socket, then calling the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) function specifying the **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL and passing the reservation token before issuing a call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function on the socket.</span></span>

<span data-ttu-id="a2971-203">O [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL pode ser usado para solicitar uma reserva de tempo de execução para um bloco de portas TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="a2971-203">The [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL can be used to request a runtime reservation for a block of TCP or UDP ports.</span></span>
<span data-ttu-id="a2971-204">Para reservas de porta de tempo de execução, o pool de portas requer que as reservas sejam consumidas do processo em cujo soquete a reserva foi concedida.</span><span class="sxs-lookup"><span data-stu-id="a2971-204">For runtime port reservations, the port pool requires that reservations be consumed from the process on whose socket the reservation was granted.</span></span>
<span data-ttu-id="a2971-205">As reservas de porta de tempo de execução duram apenas desde o tempo de vida do soquete no qual o [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL foi chamado.</span><span class="sxs-lookup"><span data-stu-id="a2971-205">Runtime port reservations last only as long as the lifetime of the socket on which the [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL was called.</span></span>
<span data-ttu-id="a2971-206">Por outro lado, as reservas de porta persistentes criadas usando a função [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) ou [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) podem ser consumidas por qualquer processo com a capacidade de obter reservas persistentes.</span><span class="sxs-lookup"><span data-stu-id="a2971-206">In contrast, persistent port reservations created using the [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) or [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) function may be consumed by any process with the ability to obtain persistent reservations.</span></span>

<span data-ttu-id="a2971-207">Depois que uma reserva de porta TCP ou UDP de tempo de execução for obtida, um aplicativo poderá solicitar atribuições de porta da reserva de porta abrindo um soquete TCP ou UDP e, em seguida, chamando a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) especificando o IOCTL de **reserva de \_ porta de associação \_ \_ sio** e passando o token de reserva antes de emitir uma chamada para a função de [**Associação**](/windows/desktop/api/winsock/nf-winsock-bind) no soquete.</span><span class="sxs-lookup"><span data-stu-id="a2971-207">Once a runtime TCP or UDP port reservation has been obtained, an application can request port assignments from the port reservation by opening a TCP or UDP socket, then calling the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) function specifying the **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL and passing the reservation token before issuing a call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function on the socket.</span></span>

<span data-ttu-id="a2971-208">Se os parâmetros *lpOverlapped* e *lpCompletionRoutine* forem nulos, o soquete nessa função será tratado como um soquete não sobreposto.</span><span class="sxs-lookup"><span data-stu-id="a2971-208">If both *lpOverlapped* and *lpCompletionRoutine* parameters are NULL, the socket in this function will be treated as a non-overlapped socket.</span></span>
<span data-ttu-id="a2971-209">Para um soquete não sobreposto, os parâmetros *lpOverlapped* e *lpCompletionRoutine* são ignorados, exceto que a função pode bloquear se o soquete *s* estiver no modo de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="a2971-209">For a non-overlapped socket, *lpOverlapped* and *lpCompletionRoutine* parameters are ignored, except that the function can block if socket *s* is in blocking mode.</span></span>
<span data-ttu-id="a2971-210">Se o soquete *s* estiver no modo sem bloqueio, essa função ainda será bloqueada, pois esse IOCTL específico não oferece suporte ao modo sem bloqueio.</span><span class="sxs-lookup"><span data-stu-id="a2971-210">If socket *s* is in non-blocking mode, this function will still block since this particular IOCTL does not support non-blocking mode.</span></span>

<span data-ttu-id="a2971-211">Para os soquetes sobrepostos, as operações que não podem ser concluídas imediatamente serão iniciadas e a conclusão será indicada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="a2971-211">For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>

<span data-ttu-id="a2971-212">Qualquer IOCTL pode bloquear indefinidamente, dependendo da implementação do provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="a2971-212">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="a2971-213">Se o aplicativo não puder tolerar o bloqueio em uma chamada de função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** , a e/s sobreposta seria ACONSELHAda para os IOCTLs que são especialmente prováveis de bloquear.</span><span class="sxs-lookup"><span data-stu-id="a2971-213">If the application cannot tolerate blocking in a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="a2971-214">O **sio \_ associar \_ a \_ reserva de porta** do IOCTL pode falhar com **WSAEINTR** ou **WSA_OPERATION_ABORTED** nos seguintes casos:</span><span class="sxs-lookup"><span data-stu-id="a2971-214">The **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL can fail with **WSAEINTR** or **WSA_OPERATION_ABORTED** under the following cases:</span></span>

* <span data-ttu-id="a2971-215">A solicitação é cancelada pelo Gerenciador de e/s.</span><span class="sxs-lookup"><span data-stu-id="a2971-215">The request is canceled by the I/O Manager.</span></span>
* <span data-ttu-id="a2971-216">O soquete está fechado.</span><span class="sxs-lookup"><span data-stu-id="a2971-216">The socket is closed.</span></span>

<span data-ttu-id="a2971-217">O IOCTL de reserva de porta de associação de sio passado para a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** para uma reserva de porta persistente só pode ser usado em um aplicativo quando o usuário está conectado como um membro do grupo Administradores. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a2971-217">The **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL passed to the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function for a persistent port reservation can only be used in an application when the user is logged on as a member of the Administrators group.</span></span>
<span data-ttu-id="a2971-218">Se **sio \_ associar \_ \_ reserva de porta** IOCTL for usado em um aplicativo quando o usuário não for um membro do grupo Administradores, a chamada de função falhará e **WSAEACCES** será retornado.</span><span class="sxs-lookup"><span data-stu-id="a2971-218">If **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL is used in an application when the user is not a member of the Administrators group, the function call will fail and **WSAEACCES** is returned.</span></span>
<span data-ttu-id="a2971-219">O uso do IOCTL **de \_ \_ \_ reserva de porta de associação de sio** também pode falhar devido ao UAC (controle de conta de usuário) no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="a2971-219">The use of the **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL can also fail because of user account control (UAC) on Windows Vista and later.</span></span>
<span data-ttu-id="a2971-220">Se um aplicativo que usa esse IOCTL com uma reserva de porta persistente for executado por um usuário conectado como um membro do grupo de administradores que não seja o administrador interno, essa chamada falhará, a menos que o aplicativo tenha sido marcado no arquivo de manifesto com um **requestedExecutionLevel** definido como *requireAdministrator*.</span><span class="sxs-lookup"><span data-stu-id="a2971-220">If an application that uses this IOCTL with a persistent port reservation is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a **requestedExecutionLevel** set to *requireAdministrator*.</span></span>
<span data-ttu-id="a2971-221">Se o aplicativo não tiver esse arquivo de manifesto, um usuário conectado como membro do grupo Administradores que não seja o administrador interno deverá, então, executar o aplicativo em um shell avançado como o administrador interno ( `RunAs administrator` ) para que essa função tenha sucesso.</span><span class="sxs-lookup"><span data-stu-id="a2971-221">If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (`RunAs administrator`) for this function to succeed.</span></span>

## <a name="see-also"></a><span data-ttu-id="a2971-222">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2971-222">See also</span></span>

[<span data-ttu-id="a2971-223">**associa**</span><span class="sxs-lookup"><span data-stu-id="a2971-223">**bind**</span></span>](/windows/desktop/api/winsock/nf-winsock-bind)

[<span data-ttu-id="a2971-224">**CreatePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="a2971-224">**CreatePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[<span data-ttu-id="a2971-225">**CreatePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="a2971-225">**CreatePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[<span data-ttu-id="a2971-226">**DeletePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="a2971-226">**DeletePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[<span data-ttu-id="a2971-227">**DeletePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="a2971-227">**DeletePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[<span data-ttu-id="a2971-228">**INET_PORT_RESERVATION_TOKEN**</span><span class="sxs-lookup"><span data-stu-id="a2971-228">**INET_PORT_RESERVATION_TOKEN**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token)

[<span data-ttu-id="a2971-229">**LookupPersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="a2971-229">**LookupPersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[<span data-ttu-id="a2971-230">**LookupPersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="a2971-230">**LookupPersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[<span data-ttu-id="a2971-231">**SIO_ACQUIRE_PORT_RESERVATION**</span><span class="sxs-lookup"><span data-stu-id="a2971-231">**SIO_ACQUIRE_PORT_RESERVATION**</span></span>](sio-acquire-port-reservation.md)

[<span data-ttu-id="a2971-232">**SIO_RELEASE_PORT_RESERVATION**</span><span class="sxs-lookup"><span data-stu-id="a2971-232">**SIO_RELEASE_PORT_RESERVATION**</span></span>](sio-release-port-reservation.md)

[<span data-ttu-id="a2971-233">SSA</span><span class="sxs-lookup"><span data-stu-id="a2971-233">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="a2971-234">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="a2971-234">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="a2971-235">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="a2971-235">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="a2971-236">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="a2971-236">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="a2971-237">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="a2971-237">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="a2971-238">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="a2971-238">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="a2971-239">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="a2971-239">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
