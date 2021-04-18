---
description: O código de controle define o registro de redirecionamento para o novo soquete TCP usado para conectar o serviço de redirecionamento.
ms.assetid: 0AC78ED4-A6EC-4D62-919C-1EF7CDE8EE80
title: Código de controle SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 11ce07c94104ecd986dc117b00dba2a49a7b5dc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105794011"
---
# <a name="sio_set_wfp_connection_redirect_records-control-code"></a><span data-ttu-id="d520b-103">Código de controle SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS</span><span class="sxs-lookup"><span data-stu-id="d520b-103">SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS Control Code</span></span>

## <a name="description"></a><span data-ttu-id="d520b-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="d520b-104">Description</span></span>

<span data-ttu-id="d520b-105">O código de controle **sio \_ set \_ WFP \_ Connection \_ Redirect \_** define o registro de redirecionamento para o novo soquete TCP usado para se conectar ao destino final para uso por um serviço de redirecionamento WFP (Windows Filtering Platform).</span><span class="sxs-lookup"><span data-stu-id="d520b-105">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** control code sets the redirect record to the new TCP socket used for connecting to the final destination for use by a Windows Filtering Platform (WFP) redirect service.</span></span>

<span data-ttu-id="d520b-106">Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="d520b-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,                              // descriptor identifying a socket
  SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  (LPVOID) lpvInputBuffer,                 // lpvInBuffer
  (DWORD) cbInputBuffer,                   // cbInBuffer
  NULL,                                    // output buffer
  0,                                       // size of output buffer
  (LPDWORD) lpcbBytesReturned,             // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,          // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine, // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,                              // descriptor identifying a socket
  SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  (LPVOID) lpvInputBuffer,                 // lpvInBuffer
  (DWORD) cbInputBuffer,                   // cbInBuffer
  NULL,                                    // output buffer
  0,                                       // size of output buffer
  (LPDWORD) lpcbBytesReturned,             // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,          // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,              // a WSATHREADID structure
  (LPINT) lpErrno                          // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="d520b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d520b-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="d520b-108">s</span><span class="sxs-lookup"><span data-stu-id="d520b-108">s</span></span>

<span data-ttu-id="d520b-109">Um descritor que identifica um soquete.</span><span class="sxs-lookup"><span data-stu-id="d520b-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="d520b-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="d520b-110">dwIoControlCode</span></span>

<span data-ttu-id="d520b-111">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="d520b-111">The control code for the operation.</span></span>
<span data-ttu-id="d520b-112">Use **sio \_ definir \_ \_ \_ \_ registros de redirecionamento de conexão WFP** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="d520b-112">Use **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="d520b-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="d520b-113">lpvInBuffer</span></span>

<span data-ttu-id="d520b-114">Um ponteiro para o buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="d520b-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="d520b-115">Esse parâmetro contém um ponteiro para o registro de redirecionamento de WFP associado ao soquete.</span><span class="sxs-lookup"><span data-stu-id="d520b-115">This parameter contains a pointer to the WFP redirect record associated with the socket.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="d520b-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="d520b-116">cbInBuffer</span></span>

<span data-ttu-id="d520b-117">O tamanho, em bytes, do buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="d520b-117">The size, in bytes, of the input buffer.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="d520b-118">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="d520b-118">lpvOutBuffer</span></span>

<span data-ttu-id="d520b-119">Um ponteiro para o buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="d520b-119">A pointer to the output buffer.</span></span>
<span data-ttu-id="d520b-120">Este parâmetro não é usado para esta operação.</span><span class="sxs-lookup"><span data-stu-id="d520b-120">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="d520b-121">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="d520b-121">cbOutBuffer</span></span>

<span data-ttu-id="d520b-122">O tamanho, em bytes, do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="d520b-122">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="d520b-123">Esse parâmetro deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="d520b-123">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="d520b-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="d520b-124">lpcbBytesReturned</span></span>

<span data-ttu-id="d520b-125">Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="d520b-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="d520b-126">Se o buffer de saída for muito pequeno, a chamada falhará, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [**WSAEINVAL**](windows-sockets-error-codes-2.md)e o parâmetro *lpcbBytesReturned* apontará para um valor **DWORD** igual a zero.</span><span class="sxs-lookup"><span data-stu-id="d520b-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="d520b-127">Se *lpOverlapped* for **NULL**, o valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* retornado em uma chamada bem-sucedida não poderá ser zero.</span><span class="sxs-lookup"><span data-stu-id="d520b-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="d520b-128">Se o parâmetro *lpOverlapped* não for **nulo** para os soquetes sobrepostos, as operações que não puderem ser concluídas imediatamente serão iniciadas e a conclusão será indicada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="d520b-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="d520b-129">O valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* que é retornado pode ser zero, já que o tamanho dos dados armazenados não pode ser determinado até que a operação sobreposta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="d520b-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="d520b-130">O status final de conclusão pode ser recuperado quando o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="d520b-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="d520b-131">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="d520b-131">lpvOverlapped</span></span>

<span data-ttu-id="d520b-132">Um ponteiro para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="d520b-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="d520b-133">Se o soquete *s* foi criado sem o atributo sobreposto, o parâmetro *lpOverlapped* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="d520b-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="d520b-134">Se *s* foi aberto com o atributo Overlapped e o parâmetro *LpOverlapped* não for **nulo**, a operação será executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="d520b-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="d520b-135">Nesse caso, o parâmetro *lpOverlapped* deve apontar para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="d520b-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="d520b-136">Para operações sobrepostas, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retorna imediatamente, e o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="d520b-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="d520b-137">Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.</span><span class="sxs-lookup"><span data-stu-id="d520b-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="d520b-138">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="d520b-138">lpCompletionRoutine</span></span>

<span data-ttu-id="d520b-139">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="d520b-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="d520b-140">Um ponteiro para a rotina de conclusão chamada quando a operação foi concluída (ignorada para soquetes não sobrepostos).</span><span class="sxs-lookup"><span data-stu-id="d520b-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="d520b-141">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="d520b-141">lpThreadId</span></span>

<span data-ttu-id="d520b-142">Um ponteiro para uma estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a ser usado pelo provedor em uma chamada subsequente para [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="d520b-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="d520b-143">O provedor deve armazenar a estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) referenciada (não o ponteiro para o mesmo) até que a função [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) seja retornada.</span><span class="sxs-lookup"><span data-stu-id="d520b-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="d520b-144">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="d520b-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="d520b-145">lpErrno</span><span class="sxs-lookup"><span data-stu-id="d520b-145">lpErrno</span></span>

<span data-ttu-id="d520b-146">Um ponteiro para o código de erro.</span><span class="sxs-lookup"><span data-stu-id="d520b-146">A pointer to the error code.</span></span>

<span data-ttu-id="d520b-147">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="d520b-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="d520b-148">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d520b-148">Return value</span></span>

<span data-ttu-id="d520b-149">Se a operação for concluída com êxito, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará zero.</span><span class="sxs-lookup"><span data-stu-id="d520b-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="d520b-150">Se a operação falhar ou estiver pendente, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará **um \_ erro de soquete**.</span><span class="sxs-lookup"><span data-stu-id="d520b-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="d520b-151">Para obter informações de erro estendidas, chame [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="d520b-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="d520b-152">Código do erro</span><span class="sxs-lookup"><span data-stu-id="d520b-152">Error code</span></span> | <span data-ttu-id="d520b-153">Significado</span><span class="sxs-lookup"><span data-stu-id="d520b-153">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="d520b-154">**\_e/s de WSA \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="d520b-154">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="d520b-155">A operação de e/s sobreposta está em andamento.</span><span class="sxs-lookup"><span data-stu-id="d520b-155">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="d520b-156">Esse valor será retornado se uma operação sobreposta tiver sido iniciada com êxito e a conclusão será indicada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="d520b-156">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="d520b-157">**operação de WSA \_ \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="d520b-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="d520b-158">A operação de e/s foi anulada devido a uma saída de thread ou uma solicitação de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d520b-158">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="d520b-159">Esse erro será retornado se uma operação sobreposta tiver sido cancelada devido ao fechamento do soquete ou à execução do comando **SIO_FLUSH** IOCTL.</span><span class="sxs-lookup"><span data-stu-id="d520b-159">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="d520b-160">**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="d520b-160">**WSAEACCES**</span></span> | <span data-ttu-id="d520b-161">Foi feita uma tentativa de acessar um soquete de uma maneira proibida por suas permissões de acesso.</span><span class="sxs-lookup"><span data-stu-id="d520b-161">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span> <span data-ttu-id="d520b-162">Esse erro é retornado sob várias condições que incluem o seguinte: o usuário não tem os privilégios administrativos necessários no computador local ou o aplicativo não está sendo executado em um shell avançado como administrador interno ( `RunAs administrator` ).</span><span class="sxs-lookup"><span data-stu-id="d520b-162">This error is returned under several conditions that include the following: the user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (`RunAs administrator`).</span></span> |
| <span data-ttu-id="d520b-163">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="d520b-163">**WSAEFAULT**</span></span> | <span data-ttu-id="d520b-164">O sistema detectou um endereço de ponteiro inválido ao tentar usar um argumento de ponteiro em uma chamada.</span><span class="sxs-lookup"><span data-stu-id="d520b-164">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="d520b-165">Esse erro é retornado do parâmetro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço de usuário.</span><span class="sxs-lookup"><span data-stu-id="d520b-165">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="d520b-166">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="d520b-166">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="d520b-167">Uma operação de bloqueio está atualmente em execução.</span><span class="sxs-lookup"><span data-stu-id="d520b-167">A blocking operation is currently executing.</span></span> <span data-ttu-id="d520b-168">Esse erro será retornado se a função for invocada quando um retorno de chamada estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="d520b-168">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="d520b-169">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="d520b-169">**WSAEINTR**</span></span> | <span data-ttu-id="d520b-170">Uma operação de bloqueio foi interrompida por uma chamada para **WSACancelBlockingCall**.</span><span class="sxs-lookup"><span data-stu-id="d520b-170">A blocking operation was interrupted by a call to **WSACancelBlockingCall**.</span></span> <span data-ttu-id="d520b-171">Esse erro será retornado se uma operação de bloqueio tiver sido interrompida.</span><span class="sxs-lookup"><span data-stu-id="d520b-171">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="d520b-172">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="d520b-172">**WSAEINVAL**</span></span> | <span data-ttu-id="d520b-173">Foi fornecido um argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="d520b-173">An invalid argument was supplied.</span></span> <span data-ttu-id="d520b-174">Esse erro será retornado se o parâmetro *dwIoControlCode* não for um comando válido ou se um parâmetro de entrada especificado não for aceitável ou se o comando não for aplicável ao tipo de soquete especificado.</span><span class="sxs-lookup"><span data-stu-id="d520b-174">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="d520b-175">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="d520b-175">**WSAENETDOWN**</span></span> | <span data-ttu-id="d520b-176">Uma operação de soquete encontrou uma rede inoperante.</span><span class="sxs-lookup"><span data-stu-id="d520b-176">A socket operation encountered a dead network.</span></span> <span data-ttu-id="d520b-177">Esse erro será retornado se o subsistema de rede tiver falhado.</span><span class="sxs-lookup"><span data-stu-id="d520b-177">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="d520b-178">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="d520b-178">**WSAENOTSOCK**</span></span> | <span data-ttu-id="d520b-179">Uma operação foi tentada em algo que não é um soquete.</span><span class="sxs-lookup"><span data-stu-id="d520b-179">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="d520b-180">Esse erro será retornado se o descritor *s* não for um soquete.</span><span class="sxs-lookup"><span data-stu-id="d520b-180">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="d520b-181">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="d520b-181">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="d520b-182">Não há suporte para a operação tentada para o tipo de objeto referenciado.</span><span class="sxs-lookup"><span data-stu-id="d520b-182">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="d520b-183">Esse erro será retornado se o comando IOCTL especificado não tiver suporte.</span><span class="sxs-lookup"><span data-stu-id="d520b-183">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="d520b-184">Esse erro também será retornado se o **sio \_ definir \_ os \_ \_ \_ registros de redirecionamento de conexão WFP** não for suportado pelo provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="d520b-184">This error is also returned if the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="d520b-185">Comentários</span><span class="sxs-lookup"><span data-stu-id="d520b-185">Remarks</span></span>

<span data-ttu-id="d520b-186">O **sio \_ conjunto \_ de \_ \_ \_ registros de redirecionamento de conexão WFP** não tem suporte no Windows 8, no Windows Server 2012 e em versões posteriores do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d520b-186">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="d520b-187">A WFP permite o acesso ao caminho de processamento de pacotes TCP/IP, onde os pacotes de saída e de entrada podem ser examinados ou alterados antes de permitir que sejam processados ainda mais.</span><span class="sxs-lookup"><span data-stu-id="d520b-187">WFP allows access to the TCP/IP packet processing path, wherein outgoing and incoming packets can be examined or changed before allowing them to be processed further.</span></span>
<span data-ttu-id="d520b-188">Ao tocar no caminho de processamento TCP/IP, os ISVs (fornecedores independentes de software) podem criar com mais facilidade firewalls, software antivírus, software de diagnóstico e outros tipos de aplicativos e serviços.</span><span class="sxs-lookup"><span data-stu-id="d520b-188">By tapping into the TCP/IP processing path, independent software vendors (ISVs) can more easily create firewalls, antivirus software, diagnostic software, and other types of applications and services.</span></span>
<span data-ttu-id="d520b-189">A WFP fornece componentes de modo de usuário e de modo kernel para que ISVs de terceiros possam participar das decisões de filtragem que ocorrem em várias camadas na pilha do protocolo TCP/IP e em todo o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d520b-189">WFP provides user-mode and kernel-mode components so that third-party ISVs can participate in the filtering decisions that take place at several layers in the TCP/IP protocol stack and throughout the operating system.</span></span>
<span data-ttu-id="d520b-190">O recurso de redirecionamento de conexão WFP permite que um driver de kernel de texto explicativo WFP redirecione uma conexão localmente para um processo de modo de usuário, execute a inspeção de conteúdo no modo de usuário e encaminhe o conteúdo inspecionado usando uma conexão diferente com o destino original.</span><span class="sxs-lookup"><span data-stu-id="d520b-190">The WFP connection redirect feature allows a WFP callout kernel driver to redirect a connection locally to a user-mode process, perform content inspection in user-mode, and forward the inspected content using a different connection to the original destination.</span></span>

<span data-ttu-id="d520b-191">O **sio \_ set \_ WFP \_ \_ reredirect \_ RECORDs** IOCTL e vários outros IOCTLs relacionados são componentes do modo de usuário usados para permitir que vários aplicativos de proxy de conexão baseados em WFP inspecionem o mesmo fluxo de tráfego de maneira cooperativa.</span><span class="sxs-lookup"><span data-stu-id="d520b-191">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL and several other related IOCTLS are user-mode components used to allow multiple WFP-based connection proxy applications to inspect the same traffic flow in a cooperative manner.</span></span>
<span data-ttu-id="d520b-192">Cada agente de inspeção pode Reinspecionar com segurança o tráfego de rede que já foi inspecionado por outro agente de inspeção.</span><span class="sxs-lookup"><span data-stu-id="d520b-192">Each inspection agent can safely re-inspect network traffic that has already been inspected by another inspection agent.</span></span>
<span data-ttu-id="d520b-193">Com a presença de vários proxies (desenvolvidos por diferentes ISVs, por exemplo), a conexão usada por um proxy para se comunicar com o destino final pode, por sua vez, ser redirecionada por um segundo proxy e essa nova conexão pode ser redirecionada novamente pelo proxy original.</span><span class="sxs-lookup"><span data-stu-id="d520b-193">With the presence of multiple proxies (developed by different ISVs, for example) the connection used by one proxy to communicate with the final destination could in turn be redirected by a second proxy, and that new connection could again be redirected by the original proxy.</span></span>
<span data-ttu-id="d520b-194">Sem o controle de conexão, a conexão original pode nunca alcançar seu destino final, pois fica presa em um loop de proxy infinito.</span><span class="sxs-lookup"><span data-stu-id="d520b-194">Without connection tracking, the original connection might never reach its final destination as it gets stuck in an infinite proxy loop.</span></span>

<span data-ttu-id="d520b-195">O **sio \_ set \_ WFP \_ Connection \_ Redirect \_ Records** IOCTL é usado para fornecer rastreamento de conexão com proxy em conexões de soquete redirecionadas.</span><span class="sxs-lookup"><span data-stu-id="d520b-195">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is used to provide proxied connection tracking on redirected socket connections.</span></span>
<span data-ttu-id="d520b-196">Esse recurso de WFP facilita o rastreamento de registros de redirecionamento do redirecionamento inicial de uma conexão com a conexão final com o destino.</span><span class="sxs-lookup"><span data-stu-id="d520b-196">This WFP feature facilitates tracking of redirection records from the initial redirect of a connection to the final connection to the destination.</span></span>

<span data-ttu-id="d520b-197">O [**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md) IOCTL é usado por um serviço de redirecionamento baseado em WFP para recuperar o registro de redirecionamento da conexão de pacote TCP/IP aceita (o Soquete conectado para um soquete TCP ou um soquete UDP, por exemplo) Redirecionado para ele por seu texto explicativo do modo kernel complementar registrado em camadas de  **\_ \_ redirecionamento da conexão Ale** em um driver de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="d520b-197">The [**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md) IOCTL is used by a WFP-based redirect service to retrieve the redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion kernel-mode callout registered at  **ALE\_CONNECT\_REDIRECT** layers in a kernel-mode driver.</span></span>
<span data-ttu-id="d520b-198">O [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) IOCTL recupera o contexto de redirecionamento para um registro de redirecionamento, que é usado.</span><span class="sxs-lookup"><span data-stu-id="d520b-198">The [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) IOCTL retrieves the redirect context for a redirect record, which is used.</span></span>
<span data-ttu-id="d520b-199">O contexto de redirecionamento é opcional e é usado se o estado de redirecionamento atual de uma conexão é que a conexão foi redirecionada pelo serviço de redirecionamento de chamada ou a conexão foi redirecionada anteriormente pelo serviço de redirecionamento de chamada, mas mais tarde redirecionada novamente por um serviço de redirecionamento diferente. O serviço de redirecionamento transfere o registro de redirecionamento recuperado para o soquete TCP que ele usa para fazer proxy do conteúdo original usando o **sio \_ set \_ WFP \_ Connection \_ Redirect de \_ registros** IOCTL.</span><span class="sxs-lookup"><span data-stu-id="d520b-199">The redirect context is optional and is used if the current redirection state of a connection is that the connection was redirected by the calling redirect service or the connection was previously redirected by the calling redirect service but later redirected again by a different redirect service.The redirect service transfers the retrieved redirect record to the TCP socket it uses to proxy the original content using the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL.</span></span>

<span data-ttu-id="d520b-200">O aplicativo que chama o **sio \_ set \_ WFP \_ Connection Redirect de \_ \_ registros** IOCTL não precisa entender o blob que contém o registro de redirecionamento que está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="d520b-200">The application calling the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL does not need to understand the blob containing the redirect record being set.</span></span>
<span data-ttu-id="d520b-201">Este é um blob opaco de dados que o aplicativo precisa passar para o novo soquete.</span><span class="sxs-lookup"><span data-stu-id="d520b-201">This is an opaque blob of data that the application needs to pass back to the new socket.</span></span>

## <a name="see-also"></a><span data-ttu-id="d520b-202">Confira também</span><span class="sxs-lookup"><span data-stu-id="d520b-202">See also</span></span>

[<span data-ttu-id="d520b-203">**Opções de soquete IPPROTO_IP**</span><span class="sxs-lookup"><span data-stu-id="d520b-203">**IPPROTO_IP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ip-socket-options)

[<span data-ttu-id="d520b-204">**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="d520b-204">**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**</span></span>](sio-query-wfp-connection-redirect-context.md)

[<span data-ttu-id="d520b-205">**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**</span><span class="sxs-lookup"><span data-stu-id="d520b-205">**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**</span></span>](sio-query-wfp-connection-redirect-records.md)

[<span data-ttu-id="d520b-206">**SSA**</span><span class="sxs-lookup"><span data-stu-id="d520b-206">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="d520b-207">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="d520b-207">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="d520b-208">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="d520b-208">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="d520b-209">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="d520b-209">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="d520b-210">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="d520b-210">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="d520b-211">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="d520b-211">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="d520b-212">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="d520b-212">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
