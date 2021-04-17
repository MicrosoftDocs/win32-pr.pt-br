---
description: O código de controle recupera o registro de redirecionamento para a conexão TCP/IP aceita para uso por um serviço de redirecionamento da plataforma de filtragem do Windows.
ms.assetid: E0D7CC1A-8F93-45A0-9543-3F2ACAF352F5
title: SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 2389914d29bd403a33e23065c29f549a01adbb67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790426"
---
# <a name="sio_query_wfp_connection_redirect_records-control-code"></a><span data-ttu-id="384ee-103">SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS código de controle</span><span class="sxs-lookup"><span data-stu-id="384ee-103">SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS Control Code</span></span>

## <a name="description"></a><span data-ttu-id="384ee-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="384ee-104">Description</span></span>

<span data-ttu-id="384ee-105">O código de controle de **\_ \_ \_ \_ redirecionamento \_ de conexão WFP consulta sio** recupera o registro de redirecionamento para a conexão TCP/IP aceita para uso por um serviço de redirecionamento WFP (Windows Filtering Platform).</span><span class="sxs-lookup"><span data-stu-id="384ee-105">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** control code retrieves the redirect record for the accepted TCP/IP connection for use by a Windows Filtering Platform (WFP) redirect service.</span></span>

<span data-ttu-id="384ee-106">Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="384ee-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
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
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

## <a name="parameters"></a><span data-ttu-id="384ee-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="384ee-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="384ee-108">s</span><span class="sxs-lookup"><span data-stu-id="384ee-108">s</span></span>

<span data-ttu-id="384ee-109">Um descritor que identifica um soquete.</span><span class="sxs-lookup"><span data-stu-id="384ee-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="384ee-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="384ee-110">dwIoControlCode</span></span>

<span data-ttu-id="384ee-111">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="384ee-111">The control code for the operation.</span></span>
<span data-ttu-id="384ee-112">Use **sio \_ consultar \_ os \_ \_ \_ registros de redirecionamento de conexão WFP** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="384ee-112">Use **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="384ee-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="384ee-113">lpvInBuffer</span></span>

<span data-ttu-id="384ee-114">Um ponteiro para o buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="384ee-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="384ee-115">Este parâmetro não é usado para esta operação.</span><span class="sxs-lookup"><span data-stu-id="384ee-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="384ee-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="384ee-116">cbInBuffer</span></span>

<span data-ttu-id="384ee-117">O tamanho, em bytes, do buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="384ee-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="384ee-118">Este parâmetro não é usado para esta operação.</span><span class="sxs-lookup"><span data-stu-id="384ee-118">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="384ee-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="384ee-119">lpvOutBuffer</span></span>

<span data-ttu-id="384ee-120">Um ponteiro para o buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="384ee-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="384ee-121">Esse parâmetro deve apontar para um tipo de dados **ULONG** se os parâmetros *lpOverlapped* e *lpCompletionRoutine* forem **nulos**.</span><span class="sxs-lookup"><span data-stu-id="384ee-121">This parameter should point to a **ULONG** data type if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="384ee-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="384ee-122">cbOutBuffer</span></span>

<span data-ttu-id="384ee-123">O tamanho, em bytes, do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="384ee-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="384ee-124">Esse parâmetro deve ter pelo menos o tamanho de um tipo de dados **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="384ee-124">This parameter must be at least the size of a **ULONG** data type.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="384ee-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="384ee-125">lpcbBytesReturned</span></span>

<span data-ttu-id="384ee-126">Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="384ee-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="384ee-127">Se o buffer de saída for muito pequeno, a chamada falhará, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [**WSAEINVAL**](windows-sockets-error-codes-2.md)e o parâmetro *lpcbBytesReturned* apontará para um valor **DWORD** igual a zero.</span><span class="sxs-lookup"><span data-stu-id="384ee-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="384ee-128">Se *lpOverlapped* for **NULL**, o valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* retornado em uma chamada bem-sucedida não poderá ser zero.</span><span class="sxs-lookup"><span data-stu-id="384ee-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="384ee-129">Se o parâmetro *lpOverlapped* não for **nulo** para os soquetes sobrepostos, as operações que não puderem ser concluídas imediatamente serão iniciadas e a conclusão será indicada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="384ee-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="384ee-130">O valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* que é retornado pode ser zero, já que o tamanho dos dados armazenados não pode ser determinado até que a operação sobreposta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="384ee-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="384ee-131">O status final de conclusão pode ser recuperado quando o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="384ee-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="384ee-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="384ee-132">lpvOverlapped</span></span>

<span data-ttu-id="384ee-133">Um ponteiro para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="384ee-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="384ee-134">Se o soquete *s* foi criado sem o atributo sobreposto, o parâmetro *lpOverlapped* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="384ee-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="384ee-135">Se *s* foi aberto com o atributo Overlapped e o parâmetro *LpOverlapped* não for **nulo**, a operação será executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="384ee-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="384ee-136">Nesse caso, o parâmetro *lpOverlapped* deve apontar para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="384ee-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="384ee-137">Para operações sobrepostas, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retorna imediatamente, e o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="384ee-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="384ee-138">Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.</span><span class="sxs-lookup"><span data-stu-id="384ee-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="384ee-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="384ee-139">lpCompletionRoutine</span></span>

<span data-ttu-id="384ee-140">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="384ee-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="384ee-141">Um ponteiro para a rotina de conclusão chamada quando a operação foi concluída (ignorada para soquetes não sobrepostos).</span><span class="sxs-lookup"><span data-stu-id="384ee-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="384ee-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="384ee-142">lpThreadId</span></span>

<span data-ttu-id="384ee-143">Um ponteiro para uma estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a ser usado pelo provedor em uma chamada subsequente para [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="384ee-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="384ee-144">O provedor deve armazenar a estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) referenciada (não o ponteiro para o mesmo) até que a função [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) seja retornada.</span><span class="sxs-lookup"><span data-stu-id="384ee-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="384ee-145">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="384ee-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="384ee-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="384ee-146">lpErrno</span></span>

<span data-ttu-id="384ee-147">Um ponteiro para o código de erro.</span><span class="sxs-lookup"><span data-stu-id="384ee-147">A pointer to the error code.</span></span>

<span data-ttu-id="384ee-148">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="384ee-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="384ee-149">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="384ee-149">Return value</span></span>

<span data-ttu-id="384ee-150">Se a operação for concluída com êxito, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará zero.</span><span class="sxs-lookup"><span data-stu-id="384ee-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="384ee-151">Se a operação falhar ou estiver pendente, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará **um \_ erro de soquete**.</span><span class="sxs-lookup"><span data-stu-id="384ee-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="384ee-152">Para obter informações de erro estendidas, chame [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="384ee-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="384ee-153">Código do erro</span><span class="sxs-lookup"><span data-stu-id="384ee-153">Error code</span></span> | <span data-ttu-id="384ee-154">Significado</span><span class="sxs-lookup"><span data-stu-id="384ee-154">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="384ee-155">**ERRO \_ de \_ buffer insuficiente**</span><span class="sxs-lookup"><span data-stu-id="384ee-155">**ERROR\_INSUFFICIENT\_BUFFER**</span></span> | <span data-ttu-id="384ee-156">A área de dados passada para uma chamada do sistema é muito pequena.</span><span class="sxs-lookup"><span data-stu-id="384ee-156">The data area passed to a system call is too small.</span></span> <span data-ttu-id="384ee-157">Esse erro será retornado se o buffer apontado pelo parâmetro *lpvOutBuffer* com um tamanho de buffer passado no parâmetro *cbOutBuffer* for muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="384ee-157">This error is returned if the buffer pointed to by the *lpvOutBuffer* parameter with a buffer size passed in the *cbOutBuffer* parameter is too small.</span></span> <span data-ttu-id="384ee-158">O tamanho do buffer necessário será retornado no parâmetro *lpcbBytesReturned* .</span><span class="sxs-lookup"><span data-stu-id="384ee-158">The buffer size required will be returned in the *lpcbBytesReturned* parameter.</span></span> |
| <span data-ttu-id="384ee-159">**WSA_IO_PENDING**</span><span class="sxs-lookup"><span data-stu-id="384ee-159">**WSA_IO_PENDING**</span></span> | <span data-ttu-id="384ee-160">Uma operação sobreposta foi iniciada com êxito e a conclusão será indicada em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="384ee-160">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="384ee-161">**WSA_OPERATION_ABORTED**</span><span class="sxs-lookup"><span data-stu-id="384ee-161">**WSA_OPERATION_ABORTED**</span></span> | <span data-ttu-id="384ee-162">Uma operação sobreposta foi cancelada devido ao fechamento do soquete ou à execução do comando **SIO_FLUSH** IOCTL.</span><span class="sxs-lookup"><span data-stu-id="384ee-162">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="384ee-163">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="384ee-163">**WSAEFAULT**</span></span> | <span data-ttu-id="384ee-164">O parâmetro *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço de usuário.</span><span class="sxs-lookup"><span data-stu-id="384ee-164">The *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped*, or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="384ee-165">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="384ee-165">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="384ee-166">A função é invocada quando um retorno de chamada está em andamento.</span><span class="sxs-lookup"><span data-stu-id="384ee-166">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="384ee-167">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="384ee-167">**WSAEINTR**</span></span> | <span data-ttu-id="384ee-168">Uma operação de bloqueio foi interrompida.</span><span class="sxs-lookup"><span data-stu-id="384ee-168">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="384ee-169">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="384ee-169">**WSAEINVAL**</span></span> | <span data-ttu-id="384ee-170">O parâmetro *dwIoControlCode* não é um comando válido ou um parâmetro de entrada especificado não é aceitável ou o comando não é aplicável ao tipo de soquete especificado.</span><span class="sxs-lookup"><span data-stu-id="384ee-170">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="384ee-171">Esse erro será retornado se o parâmetro *cbOutBuffer* for menor que o tamanho de um tipo de dados **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="384ee-171">This error is returned if the *cbOutBuffer* parameter is less than the size of a **ULONG** data type.</span></span> |
| <span data-ttu-id="384ee-172">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="384ee-172">**WSAENETDOWN**</span></span> | <span data-ttu-id="384ee-173">Falha no subsistema de rede.</span><span class="sxs-lookup"><span data-stu-id="384ee-173">The network subsystem has failed.</span></span> |
| <span data-ttu-id="384ee-174">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="384ee-174">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="384ee-175">Não há suporte para a opção de soquete no protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="384ee-175">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="384ee-176">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="384ee-176">**WSAENOTCONN**</span></span> | <span data-ttu-id="384ee-177">O soquete *s* não está conectado.</span><span class="sxs-lookup"><span data-stu-id="384ee-177">The socket *s* is not connected.</span></span> |
| <span data-ttu-id="384ee-178">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="384ee-178">**WSAENOTSOCK**</span></span> | <span data-ttu-id="384ee-179">O descritor *s* não é um soquete.</span><span class="sxs-lookup"><span data-stu-id="384ee-179">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="384ee-180">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="384ee-180">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="384ee-181">Não há suporte para o comando IOCTL especificado.</span><span class="sxs-lookup"><span data-stu-id="384ee-181">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="384ee-182">Esse erro será retornado se a **\_ consulta sio \_ consultar \_ \_ \_ registros de redirecionamento de conexão WFP** não for suportada pelo provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="384ee-182">This error is returned if the **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="384ee-183">Comentários</span><span class="sxs-lookup"><span data-stu-id="384ee-183">Remarks</span></span>

<span data-ttu-id="384ee-184">Os **\_ registros de \_ \_ \_ redirecionamento \_ de conexão WFP de consulta sio** são suportados no Windows 8, no Windows Server 2012 e em versões posteriores do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="384ee-184">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="384ee-185">A WFP permite o acesso ao caminho de processamento de pacotes TCP/IP, onde os pacotes de saída e de entrada podem ser examinados ou alterados antes de permitir que sejam processados ainda mais.</span><span class="sxs-lookup"><span data-stu-id="384ee-185">WFP allows access to the TCP/IP packet processing path, wherein outgoing and incoming packets can be examined or changed before allowing them to be processed further.</span></span>
<span data-ttu-id="384ee-186">Ao tocar no caminho de processamento TCP/IP, os ISVs (fornecedores independentes de software) podem criar com mais facilidade firewalls, software antivírus, software de diagnóstico e outros tipos de aplicativos e serviços.</span><span class="sxs-lookup"><span data-stu-id="384ee-186">By tapping into the TCP/IP processing path, independent software vendors (ISVs) can more easily create firewalls, antivirus software, diagnostic software, and other types of applications and services.</span></span>
<span data-ttu-id="384ee-187">A WFP fornece componentes de modo de usuário e de modo kernel para que ISVs de terceiros possam participar das decisões de filtragem que ocorrem em várias camadas na pilha do protocolo TCP/IP e em todo o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="384ee-187">WFP provides user-mode and kernel-mode components so that third-party ISVs can participate in the filtering decisions that take place at several layers in the TCP/IP protocol stack and throughout the operating system.</span></span>
<span data-ttu-id="384ee-188">O recurso de redirecionamento de conexão WFP permite que um driver de kernel de texto explicativo WFP redirecione uma conexão localmente para um processo de modo de usuário, execute a inspeção de conteúdo no modo de usuário e encaminhe o conteúdo inspecionado usando uma conexão diferente com o destino original.</span><span class="sxs-lookup"><span data-stu-id="384ee-188">The WFP connection redirect feature allows a WFP callout kernel driver to redirect a connection locally to a user-mode process, perform content inspection in user-mode, and forward the inspected content using a different connection to the original destination.</span></span>

<span data-ttu-id="384ee-189">O **sio \_ consulta \_ WFP \_ \_ redirecionar \_ registros** IOCTL e vários outros IOCTLs relacionados são componentes do modo de usuário usados para permitir que vários aplicativos de proxy de conexão baseados em WFP inspecionem o mesmo fluxo de tráfego de maneira cooperativa.</span><span class="sxs-lookup"><span data-stu-id="384ee-189">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL and several other related IOCTLS are user-mode components used to allow multiple WFP-based connection proxy applications to inspect the same traffic flow in a cooperative manner.</span></span>
<span data-ttu-id="384ee-190">Cada agente de inspeção pode Reinspecionar com segurança o tráfego de rede que já foi inspecionado por outro agente de inspeção.</span><span class="sxs-lookup"><span data-stu-id="384ee-190">Each inspection agent can safely re-inspect network traffic that has already been inspected by another inspection agent.</span></span>
<span data-ttu-id="384ee-191">Com a presença de vários proxies (desenvolvidos por diferentes ISVs, por exemplo), a conexão usada por um proxy para se comunicar com o destino final pode, por sua vez, ser redirecionada por um segundo proxy e essa nova conexão pode ser redirecionada novamente pelo proxy original.</span><span class="sxs-lookup"><span data-stu-id="384ee-191">With the presence of multiple proxies (developed by different ISVs, for example) the connection used by one proxy to communicate with the final destination could in turn be redirected by a second proxy, and that new connection could again be redirected by the original proxy.</span></span>
<span data-ttu-id="384ee-192">Sem o controle de conexão, a conexão original pode nunca alcançar seu destino final, pois fica presa em um loop de proxy infinito.</span><span class="sxs-lookup"><span data-stu-id="384ee-192">Without connection tracking, the original connection might never reach its final destination as it gets stuck in an infinite proxy loop.</span></span>

<span data-ttu-id="384ee-193">O **IOCTL \_ consulta \_ de \_ \_ \_ registros de redirecionamento de conexão WFP sio** é usado para fornecer rastreamento de conexão com proxy em conexões de soquete redirecionadas.</span><span class="sxs-lookup"><span data-stu-id="384ee-193">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is used to provide proxied connection tracking on redirected socket connections.</span></span>
<span data-ttu-id="384ee-194">Esse recurso de WFP facilita o rastreamento de registros de redirecionamento do redirecionamento inicial de uma conexão com a conexão final com o destino.</span><span class="sxs-lookup"><span data-stu-id="384ee-194">This WFP feature facilitates tracking of redirection records from the initial redirect of a connection to the final connection to the destination.</span></span>

<span data-ttu-id="384ee-195">O **sio \_ consulta \_ WFP \_ \_ redirecionar \_ registros** do IOCTL é usado por um serviço de redirecionamento baseado em WFP para recuperar o registro de redirecionamento da conexão de pacote TCP/IP aceita (o Soquete conectado para um soquete TCP ou um soquete UDP, por exemplo) Redirecionado para ele por seu texto explicativo complementar no modo kernel registrado em **ALE_CONNECT_REDIRECT** camadas em um driver de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="384ee-195">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is used by a WFP-based redirect service to retrieve the redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion kernel-mode callout registered at **ALE_CONNECT_REDIRECT** layers in a kernel-mode driver.</span></span>
<span data-ttu-id="384ee-196">O **\_ contexto de \_ \_ \_ redirecionamento \_ de conexão WFP de consulta sio** é usado por um serviço de redirecionamento baseado em WFP para recuperar o contexto de redirecionamento de um registro de redirecionamento da conexão de pacote TCP/IP aceita (o Soquete conectado para um soquete TCP ou um soquete UDP, por exemplo) Redirecionado para ele por seu balão complementar registrado nas camadas de **\_ \_ redirecionamento** do</span><span class="sxs-lookup"><span data-stu-id="384ee-196">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is used by a WFP-based redirect service to retrieve the redirect context for a redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion callout registered at **ALE\_CONNECT\_REDIRECT** layers.</span></span>
<span data-ttu-id="384ee-197">O contexto de redirecionamento é um contexto opcional alocado para driver usado se o estado de redirecionamento atual de uma conexão é que a conexão foi redirecionada pelo serviço de redirecionamento de chamada ou a conexão foi redirecionada anteriormente pelo serviço de redirecionamento de chamada, mas posterior redirecionada por um serviço de redirecionamento diferente.</span><span class="sxs-lookup"><span data-stu-id="384ee-197">The redirect context is an optional driver-allocated context used if the current redirection state of a connection is that the connection was redirected by the calling redirect service or the connection was previously redirected by the calling redirect service but later redirected again by a different redirect service.</span></span>
<span data-ttu-id="384ee-198">Para uma conexão de proxy TCP, o serviço de redirecionamento transfere o registro de redirecionamento recuperado para o soquete TCP que ele usa para fazer o proxy do conteúdo original usando o **sio \_ set \_ WFP \_ Connection \_ Redirect de \_ registros** IOCTL.</span><span class="sxs-lookup"><span data-stu-id="384ee-198">For a TCP proxy connection, the redirect service transfers the retrieved redirect record to the TCP socket it uses to proxy the original content using the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL.</span></span>

<span data-ttu-id="384ee-199">Quando o serviço de redirecionamento está redirecionando um soquete não TCP (UDP, por exemplo), os registros de redirecionamento retornados pelo **sio \_ consulta \_ WFP \_ \_ \_ registros de redirecionamento de conexão** do o IOCTL indicam isso ao serviço de redirecionamento usando a estrutura [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) usada com a função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) .</span><span class="sxs-lookup"><span data-stu-id="384ee-199">When the redirect service is redirecting a non-TCP socket (UDP, for example), the redirect records returned by the **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL indicate this to the redirect service using the [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) structure used with the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function.</span></span>
<span data-ttu-id="384ee-200">O membro Control da estrutura [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) teria um cmsg_type na estrutura **WSACMSGHDR** definida como **\_ \_ \_ registro de redirecionamento de conexão IP**.</span><span class="sxs-lookup"><span data-stu-id="384ee-200">The Control member of the [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) structure would have a cmsg_type in the **WSACMSGHDR** structure set to **IP\_CONNECTION\_REDIRECT\_RECORD**.</span></span>
<span data-ttu-id="384ee-201">O parâmetro [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) deve ser fornecido pelo serviço de redirecionamento ao aceitar redirecionamentos não TCP.</span><span class="sxs-lookup"><span data-stu-id="384ee-201">The [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) parameter must be supplied by the redirect service when accepting non-TCP redirects.</span></span>

<span data-ttu-id="384ee-202">Para o tráfego não TCP, o registro de redirecionamento é encaminhado usando a estrutura [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) com a função [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) .</span><span class="sxs-lookup"><span data-stu-id="384ee-202">For non-TCP traffic, the redirect record is forwarded using the [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) structure with the [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) function.</span></span>

<span data-ttu-id="384ee-203">Observe que, para o tráfego não TCP, somente o pacote de criação de fluxo carregará o **\_ \_ \_ registro de redirecionamento de conexão IP**.</span><span class="sxs-lookup"><span data-stu-id="384ee-203">Note that for non-TCP traffic, only the flow-creating packet will carry the **IP\_CONNECTION\_REDIRECT\_RECORD**.</span></span>
<span data-ttu-id="384ee-204">Como resultado, somente o primeiro pacote com proxy precisa incluir essas informações usando a função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) .</span><span class="sxs-lookup"><span data-stu-id="384ee-204">As a result, only the first proxied packet needs to include this information using the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function.</span></span>

<span data-ttu-id="384ee-205">Como o registro de redirecionamento de WFP é um blob de dados de comprimento variável, o chamador pode fornecer um buffer de saída grande (um buffer de 1.024 bytes apontado pelo parâmetro *lpvOutBuffer* , por exemplo) ou pode passar um tamanho de buffer de saída no parâmetro *cbOutBuffer* de 0 para consultar o tamanho do buffer necessário para manter o blob retornado.</span><span class="sxs-lookup"><span data-stu-id="384ee-205">Since the WFP redirect record is a variable length data blob, the caller can either supply a large output buffer (a 1,024 byte buffer pointed to by the *lpvOutBuffer* parameter, for example) or can pass an output buffer size in the *cbOutBuffer* parameter of 0 to query the buffer size required to hold the returned blob.</span></span>
<span data-ttu-id="384ee-206">Se o tamanho do buffer de saída não for suficiente para manter os dados, as funções [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornarão um **erro de \_ \_ buffer insuficiente** e o tamanho de buffer necessário será retornado no valor apontado pelo parâmetro *lpcbBytesReturned* .</span><span class="sxs-lookup"><span data-stu-id="384ee-206">If the output buffer size is not sufficient to the hold the data, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** functions will return **ERROR\_INSUFFICIENT\_BUFFER** and the required buffer size will be returned in value pointed to by the *lpcbBytesReturned* parameter.</span></span>

<span data-ttu-id="384ee-207">O aplicativo que chama o [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) não precisa entender o blob que contém o contexto de redirecionamento recuperado.</span><span class="sxs-lookup"><span data-stu-id="384ee-207">The application calling the [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) does not need to understand the blob containing the redirect context retrieved.</span></span>
<span data-ttu-id="384ee-208">Este é um blob opaco de dados que o aplicativo precisa recuperar e passar de volta para o novo soquete.</span><span class="sxs-lookup"><span data-stu-id="384ee-208">This is an opaque blob of data that the application needs to retrieve and pass back to the new socket.</span></span>

## <a name="see-also"></a><span data-ttu-id="384ee-209">Confira também</span><span class="sxs-lookup"><span data-stu-id="384ee-209">See also</span></span>

[<span data-ttu-id="384ee-210">**Opções de soquete IPPROTO_IP**</span><span class="sxs-lookup"><span data-stu-id="384ee-210">**IPPROTO_IP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ip-socket-options)

[<span data-ttu-id="384ee-211">**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="384ee-211">**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**</span></span>](sio-query-wfp-connection-redirect-context.md)

[<span data-ttu-id="384ee-212">**SSA**</span><span class="sxs-lookup"><span data-stu-id="384ee-212">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="384ee-213">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="384ee-213">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="384ee-214">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="384ee-214">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="384ee-215">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="384ee-215">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="384ee-216">**WSAMSG**</span><span class="sxs-lookup"><span data-stu-id="384ee-216">**WSAMSG**</span></span>](/windows/desktop/api/ws2def/ns-ws2def-wsamsg)

[<span data-ttu-id="384ee-217">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="384ee-217">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="384ee-218">**LPFN_WSARECVMSG (WSARecvMsg)**</span><span class="sxs-lookup"><span data-stu-id="384ee-218">**LPFN_WSARECVMSG (WSARecvMsg)**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)

[<span data-ttu-id="384ee-219">**WSASendMsg**</span><span class="sxs-lookup"><span data-stu-id="384ee-219">**WSASendMsg**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)

[<span data-ttu-id="384ee-220">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="384ee-220">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="384ee-221">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="384ee-221">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
