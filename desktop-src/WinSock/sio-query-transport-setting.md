---
description: O código de controle consulta as configurações de transporte em um soquete.
ms.assetid: 3845BE07-A414-4118-96E8-8BEF1DEDB1D3
title: SIO_QUERY_TRANSPORT_SETTING código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 592301f0fcdbbb0d3d5babba446583d2e48db086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827732"
---
# <a name="sio_query_transport_setting-control-code"></a><span data-ttu-id="8fdfd-103">SIO_QUERY_TRANSPORT_SETTING código de controle</span><span class="sxs-lookup"><span data-stu-id="8fdfd-103">SIO_QUERY_TRANSPORT_SETTING Control Code</span></span>

## <a name="description"></a><span data-ttu-id="8fdfd-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="8fdfd-104">Description</span></span>

<span data-ttu-id="8fdfd-105">O código de controle de **\_ configuração de \_ transporte \_ de consulta sio** consultas as configurações de transporte em um soquete.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-105">The **SIO\_QUERY\_TRANSPORT\_SETTING** control code queries the transport settings on a socket.</span></span>

<span data-ttu-id="8fdfd-106">Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,     // pointer to the output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,     // pointer to the output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="8fdfd-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8fdfd-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="8fdfd-108">s</span><span class="sxs-lookup"><span data-stu-id="8fdfd-108">s</span></span>

<span data-ttu-id="8fdfd-109">Um descritor que identifica um soquete.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="8fdfd-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="8fdfd-110">dwIoControlCode</span></span>

<span data-ttu-id="8fdfd-111">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-111">The control code for the operation.</span></span>
<span data-ttu-id="8fdfd-112">Use **a \_ \_ \_ configuração de transporte de consulta sio** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-112">Use **SIO\_QUERY\_TRANSPORT\_SETTING** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="8fdfd-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="8fdfd-113">lpvInBuffer</span></span>

<span data-ttu-id="8fdfd-114">Um ponteiro para o buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="8fdfd-115">Esse parâmetro contém um ponteiro para uma estrutura em que o primeiro membro da estrutura é uma estrutura [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) que determina qual configuração de transporte está sendo consultada.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-115">This parameter contains a pointer to a structure where the first member of the structure is a [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) structure that determines what transport setting is being queried.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="8fdfd-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="8fdfd-116">cbInBuffer</span></span>

<span data-ttu-id="8fdfd-117">O tamanho, em bytes, do buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="8fdfd-118">Esse parâmetro depende da configuração de transporte que está sendo consultada.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-118">This parameter depends on the transport setting being queried.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="8fdfd-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="8fdfd-119">lpvOutBuffer</span></span>

<span data-ttu-id="8fdfd-120">Um ponteiro para o buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="8fdfd-121">Esse parâmetro depende da configuração de transporte que está sendo consultada se os parâmetros *lpOverlapped* e *lpCompletionRoutine* forem **nulos**.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-121">This parameter depends on the transport setting being queried if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="8fdfd-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="8fdfd-122">cbOutBuffer</span></span>

<span data-ttu-id="8fdfd-123">O tamanho, em bytes, do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-123">The size, in bytes, of the output buffer.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="8fdfd-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="8fdfd-124">lpcbBytesReturned</span></span>

<span data-ttu-id="8fdfd-125">Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="8fdfd-126">Se o buffer de saída for muito pequeno, a chamada falhará, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [**WSAEINVAL**](windows-sockets-error-codes-2.md)e o parâmetro *lpcbBytesReturned* apontará para um valor **DWORD** igual a zero.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="8fdfd-127">Se *lpOverlapped* for **NULL**, o valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* retornado em uma chamada bem-sucedida não poderá ser zero.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="8fdfd-128">Se o parâmetro *lpOverlapped* não for **nulo** para os soquetes sobrepostos, as operações que não puderem ser concluídas imediatamente serão iniciadas e a conclusão será indicada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="8fdfd-129">O valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* que é retornado pode ser zero, já que o tamanho dos dados armazenados não pode ser determinado até que a operação sobreposta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="8fdfd-130">O status final de conclusão pode ser recuperado quando o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="8fdfd-131">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="8fdfd-131">lpvOverlapped</span></span>

<span data-ttu-id="8fdfd-132">Um ponteiro para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="8fdfd-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="8fdfd-133">Se o soquete *s* foi criado sem o atributo sobreposto, o parâmetro *lpOverlapped* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="8fdfd-134">Se *s* foi aberto com o atributo Overlapped e o parâmetro *LpOverlapped* não for **nulo**, a operação será executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="8fdfd-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="8fdfd-135">Nesse caso, o parâmetro *lpOverlapped* deve apontar para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="8fdfd-136">Para operações sobrepostas, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retorna imediatamente, e o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="8fdfd-137">Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="8fdfd-138">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="8fdfd-138">lpCompletionRoutine</span></span>

<span data-ttu-id="8fdfd-139">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="8fdfd-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="8fdfd-140">Um ponteiro para a rotina de conclusão chamada quando a operação foi concluída (ignorada para soquetes não sobrepostos).</span><span class="sxs-lookup"><span data-stu-id="8fdfd-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="8fdfd-141">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="8fdfd-141">lpThreadId</span></span>

<span data-ttu-id="8fdfd-142">Um ponteiro para uma estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a ser usado pelo provedor em uma chamada subsequente para [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="8fdfd-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="8fdfd-143">O provedor deve armazenar a estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) referenciada (não o ponteiro para o mesmo) até que a função [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) seja retornada.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="8fdfd-144">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="8fdfd-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="8fdfd-145">lpErrno</span><span class="sxs-lookup"><span data-stu-id="8fdfd-145">lpErrno</span></span>

<span data-ttu-id="8fdfd-146">Um ponteiro para o código de erro.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-146">A pointer to the error code.</span></span>

<span data-ttu-id="8fdfd-147">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="8fdfd-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="8fdfd-148">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8fdfd-148">Return value</span></span>

<span data-ttu-id="8fdfd-149">Se a operação for concluída com êxito, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará zero.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="8fdfd-150">Se a operação falhar ou estiver pendente, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará **um \_ erro de soquete**.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="8fdfd-151">Para obter informações de erro estendidas, chame [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="8fdfd-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="8fdfd-152">Código do erro</span><span class="sxs-lookup"><span data-stu-id="8fdfd-152">Error code</span></span> | <span data-ttu-id="8fdfd-153">Significado</span><span class="sxs-lookup"><span data-stu-id="8fdfd-153">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="8fdfd-154">**ERRO \_ de \_ buffer insuficiente**</span><span class="sxs-lookup"><span data-stu-id="8fdfd-154">**ERROR\_INSUFFICIENT\_BUFFER**</span></span> | <span data-ttu-id="8fdfd-155">A área de dados passada para uma chamada do sistema é muito pequena.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-155">The data area passed to a system call is too small.</span></span> <span data-ttu-id="8fdfd-156">Esse erro será retornado se o buffer apontado pelo parâmetro *lpvOutBuffer* com um tamanho de buffer passado no parâmetro *cbOutBuffer* for muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-156">This error is returned if the buffer pointed to by the *lpvOutBuffer* parameter with a buffer size passed in the *cbOutBuffer* parameter is too small.</span></span> <span data-ttu-id="8fdfd-157">O tamanho do buffer necessário será retornado no parâmetro *lpcbBytesReturned* .</span><span class="sxs-lookup"><span data-stu-id="8fdfd-157">The buffer size required will be returned in the *lpcbBytesReturned* parameter.</span></span> |
| <span data-ttu-id="8fdfd-158">**\_e/s de WSA \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="8fdfd-158">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="8fdfd-159">Uma operação sobreposta foi iniciada com êxito e a conclusão será indicada em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-159">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="8fdfd-160">**operação de WSA \_ \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="8fdfd-160">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="8fdfd-161">Uma operação sobreposta foi cancelada devido ao fechamento do soquete ou à execução do comando **sio \_ flush** IOCTL.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-161">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="8fdfd-162">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="8fdfd-162">**WSAEFAULT**</span></span> | <span data-ttu-id="8fdfd-163">O parâmetro *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço de usuário.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-163">The *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped*, or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="8fdfd-164">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="8fdfd-164">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="8fdfd-165">A função é invocada quando um retorno de chamada está em andamento.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-165">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="8fdfd-166">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="8fdfd-166">**WSAEINTR**</span></span> | <span data-ttu-id="8fdfd-167">Uma operação de bloqueio foi interrompida.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-167">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="8fdfd-168">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="8fdfd-168">**WSAEINVAL**</span></span> | <span data-ttu-id="8fdfd-169">O parâmetro *dwIoControlCode* não é um comando válido ou um parâmetro de entrada especificado não é aceitável ou o comando não é aplicável ao tipo de soquete especificado.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-169">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="8fdfd-170">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="8fdfd-170">**WSAENETDOWN**</span></span> | <span data-ttu-id="8fdfd-171">Falha no subsistema de rede.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-171">The network subsystem has failed.</span></span> |
| <span data-ttu-id="8fdfd-172">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="8fdfd-172">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="8fdfd-173">Não há suporte para a opção de soquete no protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-173">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="8fdfd-174">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="8fdfd-174">**WSAENOTCONN**</span></span> | <span data-ttu-id="8fdfd-175">O Soquete s não está conectado.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-175">The socket s is not connected.</span></span> |
| <span data-ttu-id="8fdfd-176">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="8fdfd-176">**WSAENOTSOCK**</span></span> | <span data-ttu-id="8fdfd-177">O descritor s não é um soquete.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-177">The descriptor s is not a socket.</span></span> |
| <span data-ttu-id="8fdfd-178">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="8fdfd-178">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="8fdfd-179">Não há suporte para o comando IOCTL especificado.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-179">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="8fdfd-180">Esse erro será retornado se a **\_ configuração de \_ transporte \_ de consulta sio** do IOCTL não for suportada pelo provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-180">This error is returned if the **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="8fdfd-181">Comentários</span><span class="sxs-lookup"><span data-stu-id="8fdfd-181">Remarks</span></span>

<span data-ttu-id="8fdfd-182">A **\_ configuração de \_ transporte \_ de consulta sio** do IOCTL tem suporte no Windows 8, no Windows Server 2012 e em versões posteriores do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-182">The **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="8fdfd-183">A **\_ configuração de \_ transporte \_ de consulta sio** do IOCTL é um IOCTL genérico usado para consultar as configurações de transporte em um soquete.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-183">The **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL is a generic IOCTL used to query the transport settings on a socket.</span></span>
<span data-ttu-id="8fdfd-184">A configuração de transporte sendo consultada se baseia no [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passado no parâmetro *lpvInBuffer* .</span><span class="sxs-lookup"><span data-stu-id="8fdfd-184">The transport setting being queried is based on the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the *lpvInBuffer* parameter.</span></span>

<span data-ttu-id="8fdfd-185">A única configuração de transporte definida atualmente é para o recurso de **\_ capacidade de \_ notificação \_ em tempo real** em um soquete TCP.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-185">The only transport setting currently defines is for the **REAL\_TIME\_NOTIFICATION\_CAPABILITY** capability on a TCP socket.</span></span>

<span data-ttu-id="8fdfd-186">Se o [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passado no parâmetro *lpvInBuffer* tiver o membro GUID definido como **recurso de \_ \_ notificação em \_ tempo real**, essa será uma solicitação para consultar as configurações de notificação em tempo real para o soquete TCP usado com o [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) para receber notificações de rede em segundo plano em um aplicativo da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-186">If the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the *lpvInBuffer* parameter has the Guid member set to **REAL\_TIME\_NOTIFICATION\_CAPABILITY**, then this is a request to query the real time notification settings for the TCP socket used with the [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) to receive background network notifications in a Windows Store app.</span></span>
<span data-ttu-id="8fdfd-187">O parâmetro *lpvInBuffer* deve apontar para uma estrutura de [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) .</span><span class="sxs-lookup"><span data-stu-id="8fdfd-187">The *lpvInBuffer* parameter should point to a [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) structure.</span></span>
<span data-ttu-id="8fdfd-188">O parâmetro *lpvOutBuffer* deve apontar para uma estrutura de saída de **configuração de \_ \_ notificação em \_ \_ tempo real** .</span><span class="sxs-lookup"><span data-stu-id="8fdfd-188">The *lpvOutBuffer* parameter should point to a **REAL\_TIME\_NOTIFICATION\_SETTING\_OUTPUT** structure.</span></span>
<span data-ttu-id="8fdfd-189">Essa configuração de transporte aplica-se somente a soquetes TCP.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-189">This transport setting applies only to TCP sockets.</span></span>
<span data-ttu-id="8fdfd-190">Essa configuração de transporte fornece uma maneira para que o WinInet ou serviços de rede semelhantes consultem um determinado soquete TCP para determinar o status do [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) .</span><span class="sxs-lookup"><span data-stu-id="8fdfd-190">This transport setting provides a way for WinInet or similar network services to query a given TCP socket to determine the [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) status.</span></span>
<span data-ttu-id="8fdfd-191">Um aplicativo da Windows Store não chamará esse IOCTL diretamente.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-191">A Windows Store app will not call this IOCTL directly.</span></span>
<span data-ttu-id="8fdfd-192">Se a chamada [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** for bem-sucedida, esse IOCTL retornará uma estrutura de saída de **configuração de \_ \_ notificação em \_ \_ tempo real** com o status atual.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-192">If the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** call is successful, this IOCTL returns a **REAL\_TIME\_NOTIFICATION\_SETTING\_OUTPUT** structure with the current status.</span></span>

<span data-ttu-id="8fdfd-193">A **\_ configuração de \_ transporte \_ de consulta sio** do IOCTL fornece uma maneira para que o WinInet ou serviços de rede semelhantes consultem o status de configuração de transporte de um determinado soquete TCP para determinar se o [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) está habilitado no soquete.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-193">The **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL provides a way for WinInet or similar network services to query for the transport setting status for a given TCP socket to determine if [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) is enabled on the socket.</span></span>
<span data-ttu-id="8fdfd-194">Um aplicativo da Windows Store não chamará esse IOCTL diretamente.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-194">A Windows Store app will not call this IOCTL directly.</span></span>

<span data-ttu-id="8fdfd-195">Este IOCTL aplica-se somente a soquetes TCP.</span><span class="sxs-lookup"><span data-stu-id="8fdfd-195">This IOCTL applies only to TCP sockets.</span></span>

## <a name="see-also"></a><span data-ttu-id="8fdfd-196">Confira também</span><span class="sxs-lookup"><span data-stu-id="8fdfd-196">See also</span></span>

[<span data-ttu-id="8fdfd-197">**CONTROL_CHANNEL_TRIGGER_STATUS**</span><span class="sxs-lookup"><span data-stu-id="8fdfd-197">**CONTROL_CHANNEL_TRIGGER_STATUS**</span></span>](/windows/desktop/api/mstcpip/ne-mstcpip-control_channel_trigger_status)

[<span data-ttu-id="8fdfd-198">**ControlChannelTrigger**</span><span class="sxs-lookup"><span data-stu-id="8fdfd-198">**ControlChannelTrigger**</span></span>](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)

[<span data-ttu-id="8fdfd-199">**REAL_TIME_NOTIFICATION_SETTING_OUTPUT**</span><span class="sxs-lookup"><span data-stu-id="8fdfd-199">**REAL_TIME_NOTIFICATION_SETTING_OUTPUT**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-real_time_notification_setting_output)

[<span data-ttu-id="8fdfd-200">**SIO_APPLY_TRANSPORT_SETTING**</span><span class="sxs-lookup"><span data-stu-id="8fdfd-200">**SIO_APPLY_TRANSPORT_SETTING**</span></span>](sio-apply-transport-setting.md)

[<span data-ttu-id="8fdfd-201">SSA</span><span class="sxs-lookup"><span data-stu-id="8fdfd-201">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="8fdfd-202">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="8fdfd-202">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="8fdfd-203">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="8fdfd-203">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="8fdfd-204">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="8fdfd-204">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="8fdfd-205">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="8fdfd-205">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="8fdfd-206">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="8fdfd-206">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="8fdfd-207">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="8fdfd-207">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
