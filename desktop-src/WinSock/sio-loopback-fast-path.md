---
description: O código de controle configura um soquete TCP para menor latência e operações mais rápidas na interface de loopback.
ms.assetid: 4F7A6454-E3ED-4529-A531-B0640B0767EF
title: SIO_LOOPBACK_FAST_PATH código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: f32cba8a081d2eb268a3e93a362ccec9bf414d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798304"
---
# <a name="sio_loopback_fast_path-control-code"></a><span data-ttu-id="26cba-103">SIO_LOOPBACK_FAST_PATH código de controle</span><span class="sxs-lookup"><span data-stu-id="26cba-103">SIO_LOOPBACK_FAST_PATH Control Code</span></span>

## <a name="description"></a><span data-ttu-id="26cba-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="26cba-104">Description</span></span>

<span data-ttu-id="26cba-105">O código de controle de **\_ \_ \_ caminho rápido de auto-retorno sio** configura um soquete TCP para latência mais baixa e operações mais rápidas na interface de loopback.</span><span class="sxs-lookup"><span data-stu-id="26cba-105">The **SIO\_LOOPBACK\_FAST\_PATH** control code configures a TCP socket for lower latency and faster operations on the loopback interface.</span></span>

<span data-ttu-id="26cba-106">**Importante**  O **\_ \_ \_ caminho rápido do loopback sio** foi preterido e não é recomendável usá-lo em seu código.</span><span class="sxs-lookup"><span data-stu-id="26cba-106">**Important**  The **SIO\_LOOPBACK\_FAST\_PATH** is deprecated and is not recommended to be used in your code.</span></span>

<span data-ttu-id="26cba-107">Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="26cba-107">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_LOOPBACK_FAST_PATH,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a Boolean value
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
  SIO_LOOPBACK_FAST_PATH,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a Boolean value
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

## <a name="parameters"></a><span data-ttu-id="26cba-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26cba-108">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="26cba-109">s</span><span class="sxs-lookup"><span data-stu-id="26cba-109">s</span></span>

<span data-ttu-id="26cba-110">Um descritor que identifica um soquete.</span><span class="sxs-lookup"><span data-stu-id="26cba-110">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="26cba-111">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="26cba-111">dwIoControlCode</span></span>

<span data-ttu-id="26cba-112">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="26cba-112">The control code for the operation.</span></span>
<span data-ttu-id="26cba-113">Use **o \_ \_ \_ caminho rápido de auto-retorno sio** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="26cba-113">Use **SIO\_LOOPBACK\_FAST\_PATH** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="26cba-114">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="26cba-114">lpvInBuffer</span></span>

<span data-ttu-id="26cba-115">Um ponteiro para o buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="26cba-115">A pointer to the input buffer.</span></span>
<span data-ttu-id="26cba-116">Esse parâmetro contém um ponteiro para um valor booliano que indica se o soquete deve ser configurado para operações de auto-retorno rápido.</span><span class="sxs-lookup"><span data-stu-id="26cba-116">This parameter contains a pointer to a Boolean value that indicates if the socket should be configured for fast loopback operations.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="26cba-117">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="26cba-117">cbInBuffer</span></span>

<span data-ttu-id="26cba-118">O tamanho, em bytes, do buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="26cba-118">The size, in bytes, of the input buffer.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="26cba-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="26cba-119">lpvOutBuffer</span></span>

<span data-ttu-id="26cba-120">Um ponteiro para o buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="26cba-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="26cba-121">Este parâmetro não é usado para esta operação.</span><span class="sxs-lookup"><span data-stu-id="26cba-121">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="26cba-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="26cba-122">cbOutBuffer</span></span>

<span data-ttu-id="26cba-123">O tamanho, em bytes, do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="26cba-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="26cba-124">Esse parâmetro deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="26cba-124">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="26cba-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="26cba-125">lpcbBytesReturned</span></span>

<span data-ttu-id="26cba-126">Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="26cba-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="26cba-127">Se o buffer de saída for muito pequeno, a chamada falhará, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [**WSAEINVAL**](windows-sockets-error-codes-2.md)e o parâmetro *lpcbBytesReturned* apontará para um valor **DWORD** igual a zero.</span><span class="sxs-lookup"><span data-stu-id="26cba-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="26cba-128">Se *lpOverlapped* for **NULL**, o valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* retornado em uma chamada bem-sucedida não poderá ser zero.</span><span class="sxs-lookup"><span data-stu-id="26cba-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="26cba-129">Se o parâmetro *lpOverlapped* não for **nulo** para os soquetes sobrepostos, as operações que não puderem ser concluídas imediatamente serão iniciadas e a conclusão será indicada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="26cba-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="26cba-130">O valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* que é retornado pode ser zero, já que o tamanho dos dados armazenados não pode ser determinado até que a operação sobreposta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="26cba-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="26cba-131">O status final de conclusão pode ser recuperado quando o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="26cba-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="26cba-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="26cba-132">lpvOverlapped</span></span>

<span data-ttu-id="26cba-133">Um ponteiro para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="26cba-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="26cba-134">Se o soquete *s* foi criado sem o atributo sobreposto, o parâmetro *lpOverlapped* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="26cba-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="26cba-135">Se *s* foi aberto com o atributo Overlapped e o parâmetro *LpOverlapped* não for **nulo**, a operação será executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="26cba-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="26cba-136">Nesse caso, o parâmetro *lpOverlapped* deve apontar para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="26cba-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="26cba-137">Para operações sobrepostas, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retorna imediatamente, e o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="26cba-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="26cba-138">Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.</span><span class="sxs-lookup"><span data-stu-id="26cba-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="26cba-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="26cba-139">lpCompletionRoutine</span></span>

<span data-ttu-id="26cba-140">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="26cba-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="26cba-141">Um ponteiro para a rotina de conclusão chamada quando a operação foi concluída (ignorada para soquetes não sobrepostos).</span><span class="sxs-lookup"><span data-stu-id="26cba-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="26cba-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="26cba-142">lpThreadId</span></span>

<span data-ttu-id="26cba-143">Um ponteiro para uma estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a ser usado pelo provedor em uma chamada subsequente para [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="26cba-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="26cba-144">O provedor deve armazenar a estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) referenciada (não o ponteiro para o mesmo) até que a função [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) seja retornada.</span><span class="sxs-lookup"><span data-stu-id="26cba-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="26cba-145">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="26cba-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="26cba-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="26cba-146">lpErrno</span></span>

<span data-ttu-id="26cba-147">Um ponteiro para o código de erro.</span><span class="sxs-lookup"><span data-stu-id="26cba-147">A pointer to the error code.</span></span>

<span data-ttu-id="26cba-148">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="26cba-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="26cba-149">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="26cba-149">Return value</span></span>

<span data-ttu-id="26cba-150">Se a operação for concluída com êxito, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará zero.</span><span class="sxs-lookup"><span data-stu-id="26cba-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="26cba-151">Se a operação falhar ou estiver pendente, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará **um \_ erro de soquete**.</span><span class="sxs-lookup"><span data-stu-id="26cba-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="26cba-152">Para obter informações de erro estendidas, chame [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="26cba-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="26cba-153">Código do erro</span><span class="sxs-lookup"><span data-stu-id="26cba-153">Error code</span></span> | <span data-ttu-id="26cba-154">Significado</span><span class="sxs-lookup"><span data-stu-id="26cba-154">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="26cba-155">**\_e/s de WSA \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="26cba-155">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="26cba-156">A operação de e/s sobreposta está em andamento.</span><span class="sxs-lookup"><span data-stu-id="26cba-156">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="26cba-157">Esse valor será retornado se uma operação sobreposta tiver sido iniciada com êxito e a conclusão será indicada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="26cba-157">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="26cba-158">**operação de WSA \_ \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="26cba-158">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="26cba-159">A operação de e/s foi anulada devido a uma saída de thread ou uma solicitação de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="26cba-159">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="26cba-160">Esse erro será retornado se uma operação sobreposta tiver sido cancelada devido ao fechamento do soquete ou à execução do comando **sio \_ flush IOCTL** .</span><span class="sxs-lookup"><span data-stu-id="26cba-160">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH IOCTL** command.</span></span> |
| <span data-ttu-id="26cba-161">**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="26cba-161">**WSAEACCES**</span></span> | <span data-ttu-id="26cba-162">Foi feita uma tentativa de acessar um soquete de uma maneira proibida por suas permissões de acesso.</span><span class="sxs-lookup"><span data-stu-id="26cba-162">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span> <span data-ttu-id="26cba-163">Esse erro é retornado sob várias condições para reservas de porta persistentes que incluem o seguinte: o usuário não tem os privilégios administrativos necessários no computador local ou o aplicativo não está sendo executado em um shell avançado como o administrador interno ( `RunAs administrator` ).</span><span class="sxs-lookup"><span data-stu-id="26cba-163">This error is returned under several conditions for persistent port reservations that include the following: the user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (`RunAs administrator`).</span></span> |
| <span data-ttu-id="26cba-164">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="26cba-164">**WSAEFAULT**</span></span> | <span data-ttu-id="26cba-165">O sistema detectou um endereço de ponteiro inválido ao tentar usar um argumento de ponteiro em uma chamada.</span><span class="sxs-lookup"><span data-stu-id="26cba-165">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="26cba-166">Esse erro é retornado do parâmetro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço de usuário.</span><span class="sxs-lookup"><span data-stu-id="26cba-166">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="26cba-167">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="26cba-167">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="26cba-168">Uma operação de bloqueio está atualmente em execução.</span><span class="sxs-lookup"><span data-stu-id="26cba-168">A blocking operation is currently executing.</span></span> <span data-ttu-id="26cba-169">Esse erro será retornado se a função for invocada quando um retorno de chamada estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="26cba-169">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="26cba-170">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="26cba-170">**WSAEINTR**</span></span> | <span data-ttu-id="26cba-171">Uma operação de bloqueio foi interrompida por uma chamada para [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span><span class="sxs-lookup"><span data-stu-id="26cba-171">A blocking operation was interrupted by a call to [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span></span> <span data-ttu-id="26cba-172">Esse erro será retornado se uma operação de bloqueio tiver sido interrompida.</span><span class="sxs-lookup"><span data-stu-id="26cba-172">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="26cba-173">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="26cba-173">**WSAEINVAL**</span></span> | <span data-ttu-id="26cba-174">Foi fornecido um argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="26cba-174">An invalid argument was supplied.</span></span> <span data-ttu-id="26cba-175">Esse erro será retornado se o parâmetro *dwIoControlCode* não for um comando válido ou se um parâmetro de entrada especificado não for aceitável ou se o comando não for aplicável ao tipo de soquete especificado.</span><span class="sxs-lookup"><span data-stu-id="26cba-175">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="26cba-176">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="26cba-176">**WSAENETDOWN**</span></span> | <span data-ttu-id="26cba-177">Uma operação de soquete encontrou uma rede inoperante.</span><span class="sxs-lookup"><span data-stu-id="26cba-177">A socket operation encountered a dead network.</span></span> <span data-ttu-id="26cba-178">Esse erro será retornado se o subsistema de rede tiver falhado.</span><span class="sxs-lookup"><span data-stu-id="26cba-178">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="26cba-179">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="26cba-179">**WSAENOTSOCK**</span></span> | <span data-ttu-id="26cba-180">Uma operação foi tentada em algo que não é um soquete.</span><span class="sxs-lookup"><span data-stu-id="26cba-180">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="26cba-181">Esse erro será retornado se o descritor *s* não for um soquete.</span><span class="sxs-lookup"><span data-stu-id="26cba-181">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="26cba-182">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="26cba-182">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="26cba-183">Não há suporte para a operação tentada para o tipo de objeto referenciado.</span><span class="sxs-lookup"><span data-stu-id="26cba-183">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="26cba-184">Esse erro será retornado se o comando IOCTL especificado não tiver suporte.</span><span class="sxs-lookup"><span data-stu-id="26cba-184">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="26cba-185">Esse erro também será retornado se o **sio \_ de \_ circuito \_ rápido de auto-retorno** não tiver suporte do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="26cba-185">This error is also returned if the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="26cba-186">Comentários</span><span class="sxs-lookup"><span data-stu-id="26cba-186">Remarks</span></span>

<span data-ttu-id="26cba-187">Um aplicativo pode usar o **sio \_ loopback \_ Fast \_ Path** IOCTL para reduzir a latência e melhorar o desempenho de operações de auto-retorno em um soquete TCP.</span><span class="sxs-lookup"><span data-stu-id="26cba-187">An application can use the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL to reduce the latency and improve the performance of loopback operations on a TCP socket.</span></span>
<span data-ttu-id="26cba-188">Esse IOCTL solicita que a pilha TCP/IP use um caminho rápido especial para operações de loopback neste soquete.</span><span class="sxs-lookup"><span data-stu-id="26cba-188">This IOCTL requests that the TCP/IP stack uses a special fast path for loopback operations on this socket.</span></span>
<span data-ttu-id="26cba-189">O IOCTL de **\_ \_ \_ caminho rápido de auto-retorno sio** só pode ser usado com soquetes TCP.</span><span class="sxs-lookup"><span data-stu-id="26cba-189">The **SIO\_LOOPBACK\_FAST\_PATH** IOCTL can be used only with TCP sockets.</span></span>
<span data-ttu-id="26cba-190">Esse IOCTL deve ser usado em ambos os lados da sessão de loopback.</span><span class="sxs-lookup"><span data-stu-id="26cba-190">This IOCTL must be used on both sides of the loopback session.</span></span>
<span data-ttu-id="26cba-191">O caminho rápido de loopback de TCP tem suporte usando a interface de loopback IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="26cba-191">The TCP loopback fast path is supported using either the IPv4 or IPv6 loopback interface.</span></span>

<span data-ttu-id="26cba-192">O soquete que planeja iniciar a solicitação de conexão deve aplicar esse IOCTL antes de fazer a solicitação de conexão.</span><span class="sxs-lookup"><span data-stu-id="26cba-192">The socket that plans to initiate the connection request must apply this IOCTL before making the connection request.</span></span>
<span data-ttu-id="26cba-193">Portanto, o soquete usado pela função [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist)ou [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamew) para iniciar a conexão deve aplicar esse IOCTL para usar o caminho rápido para operações de loopback.</span><span class="sxs-lookup"><span data-stu-id="26cba-193">So the socket used by the [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist), or [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamew) function to initiate the connection must apply this IOCTL to use the fast path for loopback operations.</span></span>

<span data-ttu-id="26cba-194">O soquete que está escutando a solicitação de conexão deve aplicar esse IOCTL antes de aceitar a conexão.</span><span class="sxs-lookup"><span data-stu-id="26cba-194">The socket that is listening for the connection request must apply this IOCTL before accepting the connection.</span></span>
<span data-ttu-id="26cba-195">Portanto, o soquete usado pela função Listen deve aplicar esse IOCTL para que qualquer soquete aceito use o caminho rápido para loopback.</span><span class="sxs-lookup"><span data-stu-id="26cba-195">So the socket used by the listen function must apply this IOCTL so any sockets that are accepted will use the fast path for loopback.</span></span>
<span data-ttu-id="26cba-196">Todos os soquetes retornados pela função Listen e passados para a função [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/desktop/api/winsock/nf-winsock-acceptex)ou [**WSAAccept**](/windows/desktop/api/winsock2/nf-winsock2-wsaaccept) serão marcados para usar o caminho rápido especial para operações de loopback.</span><span class="sxs-lookup"><span data-stu-id="26cba-196">Any sockets returned by the listen function and passed to the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/desktop/api/winsock/nf-winsock-acceptex), or [**WSAAccept**](/windows/desktop/api/winsock2/nf-winsock2-wsaaccept) function will be marked to use the special fast path for loopback operations.</span></span>

<span data-ttu-id="26cba-197">Depois que um aplicativo estabelece a conexão em uma interface de loopback usando o caminho rápido, todos os pacotes para o tempo de vida da conexão devem usar o caminho rápido.</span><span class="sxs-lookup"><span data-stu-id="26cba-197">Once an application establishes the connection on a loopback interface using the fast path, all packets for the lifetime of the connection must use the fast path.</span></span>

<span data-ttu-id="26cba-198">A aplicação do **\_ \_ \_ caminho rápido de auto-retorno sio** a um soquete que será conectado a um caminho de não loopback não terá nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="26cba-198">Applying **SIO\_LOOPBACK\_FAST\_PATH** to a socket which will be connected to a non-loopback path will have no effect.</span></span>

<span data-ttu-id="26cba-199">Essa otimização de auto-retorno de TCP resulta em pacotes que fluem pela camada de transporte (TL) em vez do loopback tradicional por meio da camada de rede.</span><span class="sxs-lookup"><span data-stu-id="26cba-199">This TCP loopback optimization results in packets that flow through the Transport Layer (TL) instead of the traditional loopback through the Network Layer.</span></span>
<span data-ttu-id="26cba-200">Essa otimização melhora a latência de pacotes de loopback.</span><span class="sxs-lookup"><span data-stu-id="26cba-200">This optimization improves the latency for loopback packets.</span></span>
<span data-ttu-id="26cba-201">Quando um aplicativo opta por uma configuração de nível de conexão para usar o caminho rápido de loopback, todos os pacotes seguirão o caminho de loopback.</span><span class="sxs-lookup"><span data-stu-id="26cba-201">Once an application opts in for a connection level setting to use the loopback fast path, all packets will follow the loopback path.</span></span>
<span data-ttu-id="26cba-202">Para comunicações de loopback, o congestionamento e o descarte de pacotes não são esperados.</span><span class="sxs-lookup"><span data-stu-id="26cba-202">For loopback communications, congestion and packet drop are not expected.</span></span>
<span data-ttu-id="26cba-203">A noção do controle de congestionamento e da entrega confiável no TCP será desnecessária.</span><span class="sxs-lookup"><span data-stu-id="26cba-203">The notion of congestion control and reliable delivery in TCP will be unnecessary.</span></span>
<span data-ttu-id="26cba-204">No entanto, isso não é verdadeiro para o controle de fluxo.</span><span class="sxs-lookup"><span data-stu-id="26cba-204">This, however, is not true for flow control.</span></span>
<span data-ttu-id="26cba-205">Sem o controle de fluxo, o remetente pode sobrecarregar o buffer de recebimento, levando ao comportamento de loopback de TCP errado.</span><span class="sxs-lookup"><span data-stu-id="26cba-205">Without flow control, the sender can overwhelm the receive buffer, leading to erroneous TCP loopback behavior.</span></span>
<span data-ttu-id="26cba-206">O controle de fluxo no caminho de loopback otimizado para TCP é mantido colocando solicitações de envio em uma fila.</span><span class="sxs-lookup"><span data-stu-id="26cba-206">The flow control in the TCP optimized loopback path is maintained by placing send requests in a queue.</span></span>
<span data-ttu-id="26cba-207">Quando o buffer de recebimento estiver cheio, a pilha TCP/IP garante que os envios não serão concluídos até que a fila seja atendida mantendo o controle de fluxo.</span><span class="sxs-lookup"><span data-stu-id="26cba-207">When receive buffer is full, the TCP/IP stack guarantees that the sends won't complete until the queue is serviced maintaining flow control.</span></span>

<span data-ttu-id="26cba-208">As conexões de loopback de caminho rápido TCP na presença de um texto explicativo da WFP (plataforma de filtragem do Windows) para dados de conexão devem usar o caminho lento não otimizado para loopback.</span><span class="sxs-lookup"><span data-stu-id="26cba-208">TCP fast path loopback connections in the presence of a Windows Filtering Platform (WFP) callout for connection data must take the un-optimized slow path for loopback.</span></span>
<span data-ttu-id="26cba-209">Portanto, os filtros de WFP impedirão que esse novo caminho rápido de loopback seja usado.</span><span class="sxs-lookup"><span data-stu-id="26cba-209">So WFP filters will prevent this new loopback fast path from being used.</span></span>
<span data-ttu-id="26cba-210">Quando um filtro WFP estiver habilitado, o sistema usará o caminho lento mesmo que o IOCTL **de \_ \_ \_ caminho rápido de auto-retorno sio** fosse definido.</span><span class="sxs-lookup"><span data-stu-id="26cba-210">When a WFP filter is enabled, the system we will use the slow path even if the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL was set.</span></span>
<span data-ttu-id="26cba-211">Isso garante que os aplicativos de modo de usuário tenham o recurso de segurança WFP completo.</span><span class="sxs-lookup"><span data-stu-id="26cba-211">This ensures that user-mode applications have the full WFP security capability.</span></span>

<span data-ttu-id="26cba-212">Por padrão, **o \_ \_ \_ caminho rápido de auto-retorno sio** está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="26cba-212">By default, **SIO\_LOOPBACK\_FAST\_PATH** is disabled.</span></span>

<span data-ttu-id="26cba-213">Há suporte apenas para um subconjunto das opções de soquete TCP/IP quando o IOCTL de **\_ \_ \_ caminho rápido de loopback sio** é usado para habilitar o caminho rápido de loopback em um soquete.</span><span class="sxs-lookup"><span data-stu-id="26cba-213">Only a subset of the TCP/IP socket options are supported when the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL is used to enable the loopback fast path on a socket.</span></span>
<span data-ttu-id="26cba-214">A lista de opções com suporte inclui o seguinte:</span><span class="sxs-lookup"><span data-stu-id="26cba-214">The list of supported options includes the following:</span></span>

* <span data-ttu-id="26cba-215">**TTL de IP \_**</span><span class="sxs-lookup"><span data-stu-id="26cba-215">**IP\_TTL**</span></span>
* <span data-ttu-id="26cba-216">**IP \_ unicast \_ se**</span><span class="sxs-lookup"><span data-stu-id="26cba-216">**IP\_UNICAST\_IF**</span></span>
* <span data-ttu-id="26cba-217">**\_Saltos de unicast IPv6 \_**</span><span class="sxs-lookup"><span data-stu-id="26cba-217">**IPV6\_UNICAST\_HOPS**</span></span>
* <span data-ttu-id="26cba-218">**Unicast IPV6 \_ \_ se**</span><span class="sxs-lookup"><span data-stu-id="26cba-218">**IPV6\_UNICAST\_IF**</span></span>
* <span data-ttu-id="26cba-219">**\_V6ONLY IPv6**</span><span class="sxs-lookup"><span data-stu-id="26cba-219">**IPV6\_V6ONLY**</span></span>
* <span data-ttu-id="26cba-220">**por isso, \_ \_ aceite condicional**</span><span class="sxs-lookup"><span data-stu-id="26cba-220">**SO\_CONDITIONAL\_ACCEPT**</span></span>
* <span data-ttu-id="26cba-221">**\_EXCLUSIVEADDRUSE**</span><span class="sxs-lookup"><span data-stu-id="26cba-221">**SO\_EXCLUSIVEADDRUSE**</span></span>
* <span data-ttu-id="26cba-222">**Portanto \_ , \_ escalabilidade de porta**</span><span class="sxs-lookup"><span data-stu-id="26cba-222">**SO\_PORT\_SCALABILITY**</span></span>
* <span data-ttu-id="26cba-223">**\_RCVBUF**</span><span class="sxs-lookup"><span data-stu-id="26cba-223">**SO\_RCVBUF**</span></span>
* <span data-ttu-id="26cba-224">**\_REUSEADDR**</span><span class="sxs-lookup"><span data-stu-id="26cba-224">**SO\_REUSEADDR**</span></span>
* <span data-ttu-id="26cba-225">**\_BSDURGENT TCP**</span><span class="sxs-lookup"><span data-stu-id="26cba-225">**TCP\_BSDURGENT**</span></span>

## <a name="see-also"></a><span data-ttu-id="26cba-226">Confira também</span><span class="sxs-lookup"><span data-stu-id="26cba-226">See also</span></span>

[<span data-ttu-id="26cba-227">**Opções de soquete IPPROTO_IP**</span><span class="sxs-lookup"><span data-stu-id="26cba-227">**IPPROTO_IP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ip-socket-options)

[<span data-ttu-id="26cba-228">**Opções de Soquete IPPROTO_IPV6**</span><span class="sxs-lookup"><span data-stu-id="26cba-228">**IPPROTO_IPV6 Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ipv6-socket-options)

[<span data-ttu-id="26cba-229">**Opções de soquete IPPROTO_TCP**</span><span class="sxs-lookup"><span data-stu-id="26cba-229">**IPPROTO_TCP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-tcp-socket-options)

[<span data-ttu-id="26cba-230">**SSA**</span><span class="sxs-lookup"><span data-stu-id="26cba-230">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="26cba-231">**Opções de Soquete SOL_SOCKET**</span><span class="sxs-lookup"><span data-stu-id="26cba-231">**SOL_SOCKET Socket Options**</span></span>](/windows/desktop/winsock/sol-socket-socket-options)

[<span data-ttu-id="26cba-232">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="26cba-232">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="26cba-233">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="26cba-233">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="26cba-234">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="26cba-234">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="26cba-235">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="26cba-235">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="26cba-236">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="26cba-236">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="26cba-237">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="26cba-237">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
