---
description: Um código de controle que configura os parâmetros de RTO (tempo limite de retransmissão inicial) em um soquete.
ms.assetid: F5ABAE57-E0F0-4AEB-825C-B53AEE8210E7
title: SIO_TCP_INITIAL_RTO código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 116bab23c2c5f4ef21b77a1b7f9fefa8b3ff3099
ms.sourcegitcommit: 191184ea30e209f67267ebe5b222dc16965e54e0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2020
ms.locfileid: "104454434"
---
# <a name="sio_tcp_initial_rto-control-code"></a><span data-ttu-id="e0ab0-103">SIO_TCP_INITIAL_RTO código de controle</span><span class="sxs-lookup"><span data-stu-id="e0ab0-103">SIO_TCP_INITIAL_RTO control code</span></span>

## <a name="description"></a><span data-ttu-id="e0ab0-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0ab0-104">Description</span></span>

<span data-ttu-id="e0ab0-105">O código de controle de **SIO_TCP_INITIAL_RTO** configura os parâmetros de RTO (tempo limite de retransmissão inicial) em um soquete.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-105">The **SIO_TCP_INITIAL_RTO** control code configures initial retransmission timeout (RTO) parameters on a socket.</span></span>

<span data-ttu-id="e0ab0-106">Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INITIAL_RTO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a TCP_INITIAL_RTO_PARAMETERS structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INITIAL_RTO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a TCP_INITIAL_RTO_PARAMETERS structure
  (DWORD) cbInBuffer,           // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="e0ab0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0ab0-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="e0ab0-108">s</span><span class="sxs-lookup"><span data-stu-id="e0ab0-108">s</span></span>

<span data-ttu-id="e0ab0-109">Um descritor que identifica um soquete.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="e0ab0-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="e0ab0-110">dwIoControlCode</span></span>

<span data-ttu-id="e0ab0-111">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-111">The control code for the operation.</span></span>
<span data-ttu-id="e0ab0-112">Use **SIO_TCP_INITIAL_RTO** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-112">Use **SIO_TCP_INITIAL_RTO** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="e0ab0-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="e0ab0-113">lpvInBuffer</span></span>

<span data-ttu-id="e0ab0-114">Um ponteiro para o buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="e0ab0-115">Esse parâmetro contém um ponteiro para o [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) associado ao soquete.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-115">This parameter contains a pointer to the [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) associated with the socket.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="e0ab0-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="e0ab0-116">cbInBuffer</span></span>

<span data-ttu-id="e0ab0-117">O tamanho, em bytes, do buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-117">The size, in bytes, of the input buffer.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="e0ab0-118">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="e0ab0-118">lpvOutBuffer</span></span>

<span data-ttu-id="e0ab0-119">Um ponteiro para o buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-119">A pointer to the output buffer.</span></span>
<span data-ttu-id="e0ab0-120">Este parâmetro não é usado para esta operação.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-120">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="e0ab0-121">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="e0ab0-121">cbOutBuffer</span></span>

<span data-ttu-id="e0ab0-122">O tamanho, em bytes, do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-122">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="e0ab0-123">Esse parâmetro deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-123">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="e0ab0-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="e0ab0-124">lpcbBytesReturned</span></span>

<span data-ttu-id="e0ab0-125">Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="e0ab0-126">Se o buffer de saída for muito pequeno, a chamada falhará, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [**WSAEINVAL**](windows-sockets-error-codes-2.md)e o parâmetro *lpcbBytesReturned* apontará para um valor **DWORD** igual a zero.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="e0ab0-127">Se *lpOverlapped* for **NULL**, o valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* retornado em uma chamada bem-sucedida não poderá ser zero.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="e0ab0-128">Se o parâmetro *lpOverlapped* não for **nulo** para os soquetes sobrepostos, as operações que não puderem ser concluídas imediatamente serão iniciadas e a conclusão será indicada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="e0ab0-129">O valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* que é retornado pode ser zero, já que o tamanho dos dados armazenados não pode ser determinado até que a operação sobreposta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="e0ab0-130">O status final de conclusão pode ser recuperado quando o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="e0ab0-131">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="e0ab0-131">lpvOverlapped</span></span>

<span data-ttu-id="e0ab0-132">Um ponteiro para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="e0ab0-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="e0ab0-133">Se o soquete *s* foi criado sem o atributo sobreposto, o parâmetro *lpOverlapped* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="e0ab0-134">Se *s* foi aberto com o atributo Overlapped e o parâmetro *LpOverlapped* não for **nulo**, a operação será executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="e0ab0-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="e0ab0-135">Nesse caso, o parâmetro *lpOverlapped* deve apontar para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="e0ab0-136">Para operações sobrepostas, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retorna imediatamente, e o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="e0ab0-137">Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="e0ab0-138">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="e0ab0-138">lpCompletionRoutine</span></span>

<span data-ttu-id="e0ab0-139">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="e0ab0-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="e0ab0-140">Um ponteiro para a rotina de conclusão chamada quando a operação foi concluída (ignorada para soquetes não sobrepostos).</span><span class="sxs-lookup"><span data-stu-id="e0ab0-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="e0ab0-141">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="e0ab0-141">lpThreadId</span></span>

<span data-ttu-id="e0ab0-142">Um ponteiro para uma estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a ser usado pelo provedor em uma chamada subsequente para [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="e0ab0-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="e0ab0-143">O provedor deve armazenar a estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) referenciada (não o ponteiro para o mesmo) até que a função [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) seja retornada.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="e0ab0-144">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="e0ab0-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="e0ab0-145">lpErrno</span><span class="sxs-lookup"><span data-stu-id="e0ab0-145">lpErrno</span></span>

<span data-ttu-id="e0ab0-146">Um ponteiro para o código de erro.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-146">A pointer to the error code.</span></span>

<span data-ttu-id="e0ab0-147">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="e0ab0-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="e0ab0-148">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e0ab0-148">Return value</span></span>

<span data-ttu-id="e0ab0-149">Se a operação for concluída com êxito, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará zero.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="e0ab0-150">Se a operação falhar ou estiver pendente, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará **um \_ erro de soquete**.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="e0ab0-151">Para obter informações de erro estendidas, chame [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="e0ab0-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="e0ab0-152">Código do erro</span><span class="sxs-lookup"><span data-stu-id="e0ab0-152">Error code</span></span> | <span data-ttu-id="e0ab0-153">Significado</span><span class="sxs-lookup"><span data-stu-id="e0ab0-153">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="e0ab0-154">**\_e/s de WSA \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="e0ab0-154">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="e0ab0-155">A operação de e/s sobreposta está em andamento.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-155">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="e0ab0-156">Esse valor será retornado se uma operação sobreposta tiver sido iniciada com êxito e a conclusão será indicada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-156">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="e0ab0-157">**operação de WSA \_ \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="e0ab0-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="e0ab0-158">A operação de e/s foi anulada devido a uma saída de thread ou uma solicitação de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-158">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="e0ab0-159">Esse erro será retornado se uma operação sobreposta tiver sido cancelada devido ao fechamento do soquete ou à execução do comando **sio \_ flush** IOCTL.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-159">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="e0ab0-160">**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="e0ab0-160">**WSAEACCES**</span></span> | <span data-ttu-id="e0ab0-161">Foi feita uma tentativa de acessar um soquete de uma maneira proibida por suas permissões de acesso.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-161">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span> <span data-ttu-id="e0ab0-162">Esse erro é retornado sob várias condições que incluem o seguinte: o usuário não tem os privilégios administrativos necessários no computador local ou o aplicativo não está sendo executado em um shell avançado como administrador interno ( `RunAs administrator` ).</span><span class="sxs-lookup"><span data-stu-id="e0ab0-162">This error is returned under several conditions that include the following: the user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (`RunAs administrator`).</span></span> |
| <span data-ttu-id="e0ab0-163">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="e0ab0-163">**WSAEFAULT**</span></span> | <span data-ttu-id="e0ab0-164">O sistema detectou um endereço de ponteiro inválido ao tentar usar um argumento de ponteiro em uma chamada.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-164">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="e0ab0-165">Esse erro é retornado do parâmetro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço de usuário.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-165">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="e0ab0-166">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="e0ab0-166">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="e0ab0-167">Uma operação de bloqueio está atualmente em execução.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-167">A blocking operation is currently executing.</span></span> <span data-ttu-id="e0ab0-168">Esse erro será retornado se a função for invocada quando um retorno de chamada estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-168">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="e0ab0-169">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="e0ab0-169">**WSAEINTR**</span></span> | <span data-ttu-id="e0ab0-170">Uma operação de bloqueio foi interrompida por uma chamada para *WSACancelBlockingCall*.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-170">A blocking operation was interrupted by a call to *WSACancelBlockingCall*.</span></span> <span data-ttu-id="e0ab0-171">Esse erro será retornado se uma operação de bloqueio tiver sido interrompida.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-171">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="e0ab0-172">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="e0ab0-172">**WSAEINVAL**</span></span> | <span data-ttu-id="e0ab0-173">Foi fornecido um argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-173">An invalid argument was supplied.</span></span> <span data-ttu-id="e0ab0-174">Esse erro será retornado se o parâmetro *dwIoControlCode* não for um comando válido ou se um parâmetro de entrada especificado não for aceitável ou se o comando não for aplicável ao tipo de soquete especificado.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-174">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="e0ab0-175">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="e0ab0-175">**WSAENETDOWN**</span></span> | <span data-ttu-id="e0ab0-176">Uma operação de soquete encontrou uma rede inoperante.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-176">A socket operation encountered a dead network.</span></span> <span data-ttu-id="e0ab0-177">Esse erro será retornado se o subsistema de rede tiver falhado.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-177">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="e0ab0-178">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="e0ab0-178">**WSAENOTSOCK**</span></span> | <span data-ttu-id="e0ab0-179">Uma operação foi tentada em algo que não é um soquete.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-179">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="e0ab0-180">Esse erro será retornado se o descritor s não for um soquete.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-180">This error is returned if the descriptor s is not a socket.</span></span> |
| <span data-ttu-id="e0ab0-181">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="e0ab0-181">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="e0ab0-182">Não há suporte para a operação tentada para o tipo de objeto referenciado.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-182">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="e0ab0-183">Esse erro será retornado se o comando IOCTL especificado não tiver suporte.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-183">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="e0ab0-184">Esse erro também será retornado se o **SIO_TCP_INITIAL_RTO** IOCTL não tiver suporte do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-184">This error is also returned if the **SIO_TCP_INITIAL_RTO** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="e0ab0-185">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0ab0-185">Remarks</span></span>

<span data-ttu-id="e0ab0-186">Um aplicativo pode usar o **SIO_TCP_INITIAL_RTO** IOCTL para controlar as características de retransmissão iniciais (SYN/SYN + ACK) de um soquete TCP, se necessário.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-186">An application can use the **SIO_TCP_INITIAL_RTO** IOCTL to control the initial (SYN / SYN+ACK) retransmission characteristics of a TCP socket if required.</span></span>
<span data-ttu-id="e0ab0-187">Um aplicativo, se estiver usando essa opção, deve fornecer valores adequados antes de iniciar uma tentativa de conexão TCP no soquete.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-187">An application, if using this option, must supply suitable values before starting a TCP connection attempt on the socket.</span></span>

<span data-ttu-id="e0ab0-188">O [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) IOCTL permite que um aplicativo configure o RTO (tempo limite de retransmissão) inicial usado pelo soquete.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-188">The [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) IOCTL allows an application to configure the initial (SYN) retransmission timeout (RTO) used by the socket.</span></span>

<span data-ttu-id="e0ab0-189">Um ponteiro para uma estrutura de [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) passada no parâmetro *lpvInBuffer* permite que um aplicativo configure o tempo de ida e volta (RTT) inicial usado para calcular o tempo limite de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-189">A pointer to a [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) structure passed in the *lpvInBuffer* parameter allows an application to configure the initial round trip time (RTT) used to compute the retransmission timeout.</span></span>
<span data-ttu-id="e0ab0-190">O aplicativo também pode configurar o número de retransmissões que serão tentadas antes da tentativa de conexão falhar.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-190">The application can also configure the number of retransmissions that will be attempted before the connection attempt fails.</span></span>

## <a name="see-also"></a><span data-ttu-id="e0ab0-191">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0ab0-191">See also</span></span>

[<span data-ttu-id="e0ab0-192">SSA</span><span class="sxs-lookup"><span data-stu-id="e0ab0-192">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="e0ab0-193">**TCP_INITIAL_RTO_PARAMETERS**</span><span class="sxs-lookup"><span data-stu-id="e0ab0-193">**TCP_INITIAL_RTO_PARAMETERS**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters)

[<span data-ttu-id="e0ab0-194">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="e0ab0-194">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="e0ab0-195">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="e0ab0-195">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="e0ab0-196">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="e0ab0-196">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="e0ab0-197">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="e0ab0-197">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="e0ab0-198">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="e0ab0-198">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="e0ab0-199">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="e0ab0-199">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
