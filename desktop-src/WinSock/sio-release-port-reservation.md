---
description: O código de controle libera uma reserva de tempo de execução para um bloco de portas TCP ou UDP.
ms.assetid: 24D67A40-8CE9-4AF1-90BF-599D19C87B89
title: SIO_RELEASE_PORT_RESERVATION código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 57f96d0396d661eba12f9e64238c492f38e97b2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808377"
---
# <a name="sio_release_port_reservation-control-code"></a><span data-ttu-id="40a7c-103">SIO_RELEASE_PORT_RESERVATION código de controle</span><span class="sxs-lookup"><span data-stu-id="40a7c-103">SIO_RELEASE_PORT_RESERVATION Control Code</span></span>

## <a name="description"></a><span data-ttu-id="40a7c-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="40a7c-104">Description</span></span>

<span data-ttu-id="40a7c-105">O código de controle de **\_ reserva de \_ porta \_ de liberação sio** libera uma reserva de tempo de execução para um bloco de portas TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="40a7c-105">The **SIO\_RELEASE\_PORT\_RESERVATION** control code releases a runtime reservation for a block of TCP or UDP ports.</span></span>
<span data-ttu-id="40a7c-106">A reserva de tempo de execução a ser liberada deve ter sido obtida do processo emissora usando o [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL.</span><span class="sxs-lookup"><span data-stu-id="40a7c-106">The runtime reservation to be released must have been obtained from the issuing process using the [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL.</span></span>

<span data-ttu-id="40a7c-107">Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="40a7c-107">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_RELEASE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to a INET_PORT_RESERVATION_TOKEN structure
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
  SIO_RELEASE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to a INET_PORT_RESERVATION_TOKEN structure
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

## <a name="parameters"></a><span data-ttu-id="40a7c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40a7c-108">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="40a7c-109">s</span><span class="sxs-lookup"><span data-stu-id="40a7c-109">s</span></span>

<span data-ttu-id="40a7c-110">Um descritor que identifica um soquete.</span><span class="sxs-lookup"><span data-stu-id="40a7c-110">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="40a7c-111">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="40a7c-111">dwIoControlCode</span></span>

<span data-ttu-id="40a7c-112">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="40a7c-112">The control code for the operation.</span></span>
<span data-ttu-id="40a7c-113">Use **a \_ \_ \_ reserva de porta de liberação sio** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="40a7c-113">Use **SIO\_RELEASE\_PORT\_RESERVATION** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="40a7c-114">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="40a7c-114">lpvInBuffer</span></span>

<span data-ttu-id="40a7c-115">Um ponteiro para o buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="40a7c-115">A pointer to the input buffer.</span></span>
<span data-ttu-id="40a7c-116">Esse parâmetro contém um ponteiro para uma estrutura de [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) com o token da reserva de porta TCP ou UDP a ser liberada.</span><span class="sxs-lookup"><span data-stu-id="40a7c-116">This parameter contains a pointer to an [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) structure with the token for the TCP or UDP port reservation to release.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="40a7c-117">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="40a7c-117">cbInBuffer</span></span>

<span data-ttu-id="40a7c-118">O tamanho, em bytes, do buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="40a7c-118">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="40a7c-119">Esse parâmetro deve ter pelo menos o tamanho da estrutura de [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) .</span><span class="sxs-lookup"><span data-stu-id="40a7c-119">This parameter must be at least the size of the [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) structure.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="40a7c-120">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="40a7c-120">lpvOutBuffer</span></span>

<span data-ttu-id="40a7c-121">Um ponteiro para o buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="40a7c-121">A pointer to the output buffer.</span></span>
<span data-ttu-id="40a7c-122">Este parâmetro não é usado para esta operação.</span><span class="sxs-lookup"><span data-stu-id="40a7c-122">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="40a7c-123">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="40a7c-123">cbOutBuffer</span></span>

<span data-ttu-id="40a7c-124">O tamanho, em bytes, do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="40a7c-124">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="40a7c-125">Esse parâmetro deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="40a7c-125">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="40a7c-126">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="40a7c-126">lpcbBytesReturned</span></span>

<span data-ttu-id="40a7c-127">Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="40a7c-127">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="40a7c-128">Se o buffer de saída for muito pequeno, a chamada falhará, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [**WSAEINVAL**](windows-sockets-error-codes-2.md)e o parâmetro *lpcbBytesReturned* apontará para um valor **DWORD** igual a zero.</span><span class="sxs-lookup"><span data-stu-id="40a7c-128">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="40a7c-129">Se *lpOverlapped* for **NULL**, o valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* retornado em uma chamada bem-sucedida não poderá ser zero.</span><span class="sxs-lookup"><span data-stu-id="40a7c-129">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="40a7c-130">Se o parâmetro *lpOverlapped* não for **nulo** para os soquetes sobrepostos, as operações que não puderem ser concluídas imediatamente serão iniciadas e a conclusão será indicada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="40a7c-130">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="40a7c-131">O valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* que é retornado pode ser zero, já que o tamanho dos dados armazenados não pode ser determinado até que a operação sobreposta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="40a7c-131">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="40a7c-132">O status final de conclusão pode ser recuperado quando o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="40a7c-132">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="40a7c-133">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="40a7c-133">lpvOverlapped</span></span>

<span data-ttu-id="40a7c-134">Um ponteiro para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="40a7c-134">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="40a7c-135">Se o soquete *s* foi criado sem o atributo sobreposto, o parâmetro *lpOverlapped* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="40a7c-135">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="40a7c-136">Se *s* foi aberto com o atributo Overlapped e o parâmetro *LpOverlapped* não for **nulo**, a operação será executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="40a7c-136">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="40a7c-137">Nesse caso, o parâmetro *lpOverlapped* deve apontar para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="40a7c-137">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="40a7c-138">Para operações sobrepostas, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retorna imediatamente, e o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="40a7c-138">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="40a7c-139">Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.</span><span class="sxs-lookup"><span data-stu-id="40a7c-139">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="40a7c-140">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="40a7c-140">lpCompletionRoutine</span></span>

<span data-ttu-id="40a7c-141">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="40a7c-141">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="40a7c-142">Um ponteiro para a rotina de conclusão chamada quando a operação foi concluída (ignorada para soquetes não sobrepostos).</span><span class="sxs-lookup"><span data-stu-id="40a7c-142">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="40a7c-143">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="40a7c-143">lpThreadId</span></span>

<span data-ttu-id="40a7c-144">Um ponteiro para uma estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a ser usado pelo provedor em uma chamada subsequente para [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="40a7c-144">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="40a7c-145">O provedor deve armazenar a estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) referenciada (não o ponteiro para o mesmo) até que a função [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) seja retornada.</span><span class="sxs-lookup"><span data-stu-id="40a7c-145">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="40a7c-146">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="40a7c-146">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="40a7c-147">lpErrno</span><span class="sxs-lookup"><span data-stu-id="40a7c-147">lpErrno</span></span>

<span data-ttu-id="40a7c-148">Um ponteiro para o código de erro.</span><span class="sxs-lookup"><span data-stu-id="40a7c-148">A pointer to the error code.</span></span>

<span data-ttu-id="40a7c-149">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="40a7c-149">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="40a7c-150">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="40a7c-150">Return value</span></span>

<span data-ttu-id="40a7c-151">Se a operação for concluída com êxito, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará zero.</span><span class="sxs-lookup"><span data-stu-id="40a7c-151">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="40a7c-152">Se a operação falhar ou estiver pendente, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará **um \_ erro de soquete**.</span><span class="sxs-lookup"><span data-stu-id="40a7c-152">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="40a7c-153">Para obter informações de erro estendidas, chame [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="40a7c-153">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="40a7c-154">Código do erro</span><span class="sxs-lookup"><span data-stu-id="40a7c-154">Error code</span></span> | <span data-ttu-id="40a7c-155">Significado</span><span class="sxs-lookup"><span data-stu-id="40a7c-155">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="40a7c-156">**\_e/s de WSA \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="40a7c-156">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="40a7c-157">A operação de e/s sobreposta está em andamento.</span><span class="sxs-lookup"><span data-stu-id="40a7c-157">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="40a7c-158">Esse valor será retornado se uma operação sobreposta tiver sido iniciada com êxito e a conclusão será indicada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="40a7c-158">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="40a7c-159">**operação de WSA \_ \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="40a7c-159">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="40a7c-160">A operação de e/s foi anulada devido a uma saída de thread ou uma solicitação de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="40a7c-160">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="40a7c-161">Esse erro será retornado se uma operação sobreposta tiver sido cancelada devido ao fechamento do soquete ou à execução do comando **SIO_FLUSH** IOCTL.</span><span class="sxs-lookup"><span data-stu-id="40a7c-161">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="40a7c-162">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="40a7c-162">**WSAEFAULT**</span></span> | <span data-ttu-id="40a7c-163">O sistema detectou um endereço de ponteiro inválido ao tentar usar um argumento de ponteiro em uma chamada.</span><span class="sxs-lookup"><span data-stu-id="40a7c-163">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="40a7c-164">Esse erro é retornado do parâmetro *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço do usuário.</span><span class="sxs-lookup"><span data-stu-id="40a7c-164">This error is returned of the *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="40a7c-165">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="40a7c-165">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="40a7c-166">Uma operação de bloqueio está atualmente em execução.</span><span class="sxs-lookup"><span data-stu-id="40a7c-166">A blocking operation is currently executing.</span></span> <span data-ttu-id="40a7c-167">Esse erro será retornado se a função for invocada quando um retorno de chamada estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="40a7c-167">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="40a7c-168">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="40a7c-168">**WSAEINTR**</span></span> | <span data-ttu-id="40a7c-169">Uma operação de bloqueio foi interrompida por uma chamada para **WSACancelBlockingCall**.</span><span class="sxs-lookup"><span data-stu-id="40a7c-169">A blocking operation was interrupted by a call to **WSACancelBlockingCall**.</span></span> <span data-ttu-id="40a7c-170">Esse erro será retornado se uma operação de bloqueio tiver sido interrompida.</span><span class="sxs-lookup"><span data-stu-id="40a7c-170">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="40a7c-171">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="40a7c-171">**WSAEINVAL**</span></span> | <span data-ttu-id="40a7c-172">Foi fornecido um argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="40a7c-172">An invalid argument was supplied.</span></span> <span data-ttu-id="40a7c-173">Esse erro será retornado se o parâmetro *dwIoControlCode* não for um comando válido ou se um parâmetro de entrada especificado não for aceitável ou se o comando não for aplicável ao tipo de soquete especificado.</span><span class="sxs-lookup"><span data-stu-id="40a7c-173">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="40a7c-174">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="40a7c-174">**WSAENETDOWN**</span></span> | <span data-ttu-id="40a7c-175">Uma operação de soquete encontrou uma rede inoperante.</span><span class="sxs-lookup"><span data-stu-id="40a7c-175">A socket operation encountered a dead network.</span></span> <span data-ttu-id="40a7c-176">Esse erro será retornado se o subsistema de rede tiver falhado.</span><span class="sxs-lookup"><span data-stu-id="40a7c-176">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="40a7c-177">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="40a7c-177">**WSAENOTSOCK**</span></span> | <span data-ttu-id="40a7c-178">Uma operação foi tentada em algo que não é um soquete.</span><span class="sxs-lookup"><span data-stu-id="40a7c-178">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="40a7c-179">Esse erro será retornado se o descritor *s* não for um soquete.</span><span class="sxs-lookup"><span data-stu-id="40a7c-179">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="40a7c-180">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="40a7c-180">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="40a7c-181">Não há suporte para a operação tentada para o tipo de objeto referenciado.</span><span class="sxs-lookup"><span data-stu-id="40a7c-181">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="40a7c-182">Esse erro será retornado se o comando IOCTL especificado não tiver suporte.</span><span class="sxs-lookup"><span data-stu-id="40a7c-182">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="40a7c-183">Esse erro também será retornado se o IOCTL de **\_ reserva de \_ porta \_ de liberação sio** não tiver suporte do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="40a7c-183">This error is also returned if the **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="40a7c-184">Esse erro também é retornado quando uma tentativa de usar o IOCTL de **\_ reserva de \_ porta \_ de liberação sio** é feita em um soquete diferente de UDP ou TCP.</span><span class="sxs-lookup"><span data-stu-id="40a7c-184">This error is also returned when an attempt to use the **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is made on a socket other than UDP or TCP.</span></span> |

## <a name="remarks"></a><span data-ttu-id="40a7c-185">Comentários</span><span class="sxs-lookup"><span data-stu-id="40a7c-185">Remarks</span></span>

<span data-ttu-id="40a7c-186">O IOCTL de **\_ reserva de \_ porta \_ de liberação sio** tem suporte no Windows Vista e versões posteriores do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="40a7c-186">The **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is supported on Windows Vista and later versions of the operating system.</span></span>

<span data-ttu-id="40a7c-187">Os aplicativos e serviços que precisam reservar portas se enquadram em duas categorias.</span><span class="sxs-lookup"><span data-stu-id="40a7c-187">Applications and services which need to reserve ports fall into two categories.</span></span>
<span data-ttu-id="40a7c-188">A primeira categoria inclui componentes que precisam de uma porta específica como parte de sua operação.</span><span class="sxs-lookup"><span data-stu-id="40a7c-188">The first category includes components which need a particular port as part of their operation.</span></span>
<span data-ttu-id="40a7c-189">Esses componentes geralmente preferem especificar a porta necessária no momento da instalação (em um manifesto do aplicativo, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="40a7c-189">Such components will generally prefer to specify their required port at installation time (in an application manifest, for example).</span></span>
<span data-ttu-id="40a7c-190">A segunda categoria inclui componentes que precisam de qualquer porta disponível ou bloco de portas em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="40a7c-190">The second category includes components which need any available port or block of ports at runtime.</span></span>
<span data-ttu-id="40a7c-191">Essas duas categorias correspondem a solicitações específicas e de reserva de porta curinga.</span><span class="sxs-lookup"><span data-stu-id="40a7c-191">These two categories correspond to specific and wildcard port reservation requests.</span></span>
<span data-ttu-id="40a7c-192">As solicitações de reserva específicas podem ser persistentes ou tempo de execução, enquanto as solicitações de reserva de porta curinga só têm suporte em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="40a7c-192">Specific reservation requests may be persistent or runtime, while wildcard port reservation requests are only supported at runtime.</span></span>

<span data-ttu-id="40a7c-193">O [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL é usado para solicitar uma reserva de tempo de execução para um bloco de portas TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="40a7c-193">The [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL is used to request a runtime reservation for a block of TCP or UDP ports.</span></span>
<span data-ttu-id="40a7c-194">Para reservas de porta de tempo de execução, o pool de portas requer que as reservas sejam consumidas do processo em cujo soquete a reserva foi concedida.</span><span class="sxs-lookup"><span data-stu-id="40a7c-194">For runtime port reservations, the port pool requires that reservations be consumed from the process on whose socket the reservation was granted.</span></span>
<span data-ttu-id="40a7c-195">As reservas de porta de tempo de execução duram apenas desde o tempo de vida do soquete no qual o [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL foi chamado.</span><span class="sxs-lookup"><span data-stu-id="40a7c-195">Runtime port reservations last only as long as the lifetime of the socket on which the [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL was called.</span></span>
<span data-ttu-id="40a7c-196">Por outro lado, as reservas de porta persistentes criadas usando a função [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) ou [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) podem ser consumidas por qualquer processo com a capacidade de obter reservas persistentes.</span><span class="sxs-lookup"><span data-stu-id="40a7c-196">In contrast, persistent port reservations created using the [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) or [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) function may be consumed by any process with the ability to obtain persistent reservations.</span></span>

<span data-ttu-id="40a7c-197">O **IOCTL \_ \_ \_ reserva de porta de liberação sio** é usado para liberar uma reserva de tempo de execução para um bloco de portas TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="40a7c-197">The **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is used to release a runtime reservation for a block of TCP or UDP ports.</span></span>

<span data-ttu-id="40a7c-198">Se os parâmetros *lpOverlapped* e *lpCompletionRoutine* forem **nulos**, o soquete nessa função será tratado como um soquete não sobreposto.</span><span class="sxs-lookup"><span data-stu-id="40a7c-198">If both *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**, the socket in this function will be treated as a non-overlapped socket.</span></span>
<span data-ttu-id="40a7c-199">Para um soquete não sobreposto, os parâmetros *lpOverlapped* e *lpCompletionRoutine* são ignorados, exceto que a função pode bloquear se o soquete *s* estiver no modo de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="40a7c-199">For a non-overlapped socket, *lpOverlapped* and *lpCompletionRoutine* parameters are ignored, except that the function can block if socket *s* is in blocking mode.</span></span>
<span data-ttu-id="40a7c-200">Se o soquete *s* estiver no modo sem bloqueio, essa função ainda será bloqueada, pois esse IOCTL específico não oferece suporte ao modo sem bloqueio.</span><span class="sxs-lookup"><span data-stu-id="40a7c-200">If socket *s* is in non-blocking mode, this function will still block since this particular IOCTL does not support non-blocking mode.</span></span>

<span data-ttu-id="40a7c-201">Para os soquetes sobrepostos, as operações que não podem ser concluídas imediatamente serão iniciadas e a conclusão será indicada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="40a7c-201">For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>

<span data-ttu-id="40a7c-202">Qualquer IOCTL pode bloquear indefinidamente, dependendo da implementação do provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="40a7c-202">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="40a7c-203">Se o aplicativo não puder tolerar o bloqueio em uma chamada de função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** , a e/s sobreposta seria ACONSELHAda para os IOCTLs que são especialmente prováveis de bloquear.</span><span class="sxs-lookup"><span data-stu-id="40a7c-203">If the application cannot tolerate blocking in a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="40a7c-204">O **IOCTL \_ \_ \_ reserva de porta de liberação sio** pode falhar com a operação **WSAEINTR** ou **WSA \_ \_ anulada** nos seguintes casos:</span><span class="sxs-lookup"><span data-stu-id="40a7c-204">The **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

* <span data-ttu-id="40a7c-205">A solicitação é cancelada pelo Gerenciador de e/s.</span><span class="sxs-lookup"><span data-stu-id="40a7c-205">The request is canceled by the I/O Manager.</span></span>
* <span data-ttu-id="40a7c-206">O soquete está fechado.</span><span class="sxs-lookup"><span data-stu-id="40a7c-206">The socket is closed.</span></span>

## <a name="examples"></a><span data-ttu-id="40a7c-207">Exemplos</span><span class="sxs-lookup"><span data-stu-id="40a7c-207">Examples</span></span>

<span data-ttu-id="40a7c-208">O exemplo a seguir adquire uma reserva de porta de tempo de execução e libera a reserva de porta de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="40a7c-208">The following example acquires a runtime port reservation and then releases the runtime port reservation.</span></span>

```cpp
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <Windows.h.>
#include <winsock2.h>
#include <mstcpip.h>
#include <ws2ipdef.h>
#include <stdio.h>
#include <stdlib.h>

// Need to link with Ws2_32.lib for Winsock functions
#pragma comment(lib, "ws2_32.lib")

int wmain(int argc, WCHAR ** argv)
{

    // Declare and initialize variables

    int startPort = 0;          // host byte order
    int numPorts = 0;
    USHORT startPortns = 0;     // Network byte order

    INET_PORT_RANGE portRange = { 0 };
    INET_PORT_RESERVATION_INSTANCE portRes = { 0 };

    unsigned long status = 0;

    WSADATA wsaData = { 0 };
    int iResult = 0;

    SOCKET sock = INVALID_SOCKET;
    int iFamily = AF_INET;
    int iType = 0;
    int iProtocol = 0;

    SOCKET sockRes = INVALID_SOCKET;

    DWORD bytesReturned = 0;

    // Validate the parameters
    if (argc != 6) {
        wprintf
            (L"usage: %s <addressfamily> <type> <protocol> <StartingPort> <NumberOfPorts>\n",
             argv[0]);
        wprintf(L"Opens a socket for the specified family, type, & protocol\n");
        wprintf
            (L"and then acquires a runtime port reservation for the protocol specified\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 2 2 17 5000 20\n", argv[0]);
        wprintf(L"   where AF_INET=2 SOCK_DGRAM=2 IPPROTO_UDP=17 StartPort=5000 NumPorts=20", argv[0]);

        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);

    startPort = _wtoi(argv[4]);
    if (startPort < 0 || startPort > 65535) {
        wprintf(L"Starting point must be either 0 or between 1 and 65,535\n");
        return 1;
    }
    startPortns = htons((USHORT) startPort);

    numPorts = _wtoi(argv[5]);
    if (numPorts < 0) {
        wprintf(L"Number of ports must be a positive number\n");
        return 1;
    }

    portRange.StartPort = startPortns;
    portRange.NumberOfPorts = (USHORT) numPorts;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error = %d\n", iResult);
        return 1;
    }

    sock = socket(iFamily, iType, iProtocol);
    if (sock == INVALID_SOCKET) {
        wprintf(L"socket function failed with error = %d\n", WSAGetLastError());
        WSACleanup();
        return 1;
    } else {
        wprintf(L"socket function succeeded\n");

        iResult =
            WSAIoctl(sock, SIO_ACQUIRE_PORT_RESERVATION, (LPVOID) & portRange,
                     sizeof (INET_PORT_RANGE), (LPVOID) & portRes,
                     sizeof (INET_PORT_RESERVATION_INSTANCE), &bytesReturned, NULL, NULL);
        if (iResult != 0) {
            wprintf(L"WSAIoctl(SIO_ACQUIRE_PORT_RESERVATION) failed with error = %d\n",
                    WSAGetLastError());
            closesocket(sock);
            WSACleanup();
            return 1;
        } else {
            wprintf
                (L"WSAIoctl(SIO_ACQUIRE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                 bytesReturned);
            wprintf(L"  Starting port=%d,  Number of Ports=%d, Token=%I64d\n",
                    htons(portRes.Reservation.StartPort),
                    portRes.Reservation.NumberOfPorts, portRes.Token);

            iResult =
                WSAIoctl(sock, SIO_RELEASE_PORT_RESERVATION, (LPVOID) & portRes.Token,
                         sizeof (ULONG64), NULL, 0, &bytesReturned, NULL, NULL);
            if (iResult != 0) {
                wprintf
                    (L"WSAIoctl(SIO_RELEASE_PORT_RESERVATION) failed with error = %d\n",
                     WSAGetLastError());
            } else {
                wprintf
                    (L"WSAIoctl(SIO_RELEASE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                     bytesReturned);
            }
        }

        if (sock != INVALID_SOCKET) {
            iResult = closesocket(sock);
            if (iResult == SOCKET_ERROR) {
                wprintf(L"closesocket for first socket failed with error = %d\n",
                        WSAGetLastError());
            }
        }
    }

    WSACleanup();

    return 0;
}
```

## <a name="see-also"></a><span data-ttu-id="40a7c-209">Confira também</span><span class="sxs-lookup"><span data-stu-id="40a7c-209">See also</span></span>

[<span data-ttu-id="40a7c-210">**CreatePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="40a7c-210">**CreatePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[<span data-ttu-id="40a7c-211">**CreatePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="40a7c-211">**CreatePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[<span data-ttu-id="40a7c-212">**DeletePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="40a7c-212">**DeletePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[<span data-ttu-id="40a7c-213">**DeletePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="40a7c-213">**DeletePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[<span data-ttu-id="40a7c-214">**INET_PORT_RESERVATION_TOKEN**</span><span class="sxs-lookup"><span data-stu-id="40a7c-214">**INET_PORT_RESERVATION_TOKEN**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token)

[<span data-ttu-id="40a7c-215">**LookupPersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="40a7c-215">**LookupPersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[<span data-ttu-id="40a7c-216">**LookupPersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="40a7c-216">**LookupPersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[<span data-ttu-id="40a7c-217">**SIO_ACQUIRE_PORT_RESERVATION**</span><span class="sxs-lookup"><span data-stu-id="40a7c-217">**SIO_ACQUIRE_PORT_RESERVATION**</span></span>](sio-acquire-port-reservation.md)

[<span data-ttu-id="40a7c-218">**SIO_ASSOCIATE_PORT_RESERVATION**</span><span class="sxs-lookup"><span data-stu-id="40a7c-218">**SIO_ASSOCIATE_PORT_RESERVATION**</span></span>](sio-associate-port-reservation.md)

[<span data-ttu-id="40a7c-219">SSA</span><span class="sxs-lookup"><span data-stu-id="40a7c-219">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="40a7c-220">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="40a7c-220">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="40a7c-221">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="40a7c-221">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="40a7c-222">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="40a7c-222">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="40a7c-223">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="40a7c-223">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="40a7c-224">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="40a7c-224">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="40a7c-225">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="40a7c-225">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
