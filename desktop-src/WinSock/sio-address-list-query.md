---
description: O código de controle obtém uma lista de endereços de transporte locais da família de protocolos do soquete à qual o aplicativo pode ser associado.
ms.assetid: 6b23a019-812c-4623-941b-87928acabbd2
title: SIO_ADDRESS_LIST_QUERY código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 7a728293afa51ceb58d61141e7184077478b787c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762221"
---
# <a name="sio_address_list_query-control-code"></a><span data-ttu-id="1dbb1-103">SIO_ADDRESS_LIST_QUERY código de controle</span><span class="sxs-lookup"><span data-stu-id="1dbb1-103">SIO_ADDRESS_LIST_QUERY Control Code</span></span>

## <a name="description"></a><span data-ttu-id="1dbb1-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="1dbb1-104">Description</span></span>

<span data-ttu-id="1dbb1-105">O código de controle de **\_ consulta da \_ lista \_ de endereços sio** Obtém uma lista de endereços de transporte locais da família de protocolos do soquete à qual o aplicativo pode se associar.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-105">The **SIO\_ADDRESS\_LIST\_QUERY** control code obtains a list of local transport addresses of the socket's protocol family to which the application can bind.</span></span>
<span data-ttu-id="1dbb1-106">A lista de endereços varia de acordo com a família de endereços e alguns endereços são excluídos da lista.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-106">The list of addresses varies based on address family and some addresses are excluded from the list.</span></span>

<span data-ttu-id="1dbb1-107">Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-107">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="1dbb1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1dbb1-108">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="1dbb1-109">s</span><span class="sxs-lookup"><span data-stu-id="1dbb1-109">s</span></span>

<span data-ttu-id="1dbb1-110">Um descritor que identifica um soquete.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-110">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="1dbb1-111">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="1dbb1-111">dwIoControlCode</span></span>

<span data-ttu-id="1dbb1-112">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-112">The control code for the operation.</span></span>
<span data-ttu-id="1dbb1-113">Use **a \_ \_ \_ consulta de lista de endereços do sio** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-113">Use **SIO\_ADDRESS\_LIST\_QUERY** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="1dbb1-114">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="1dbb1-114">lpvInBuffer</span></span>

<span data-ttu-id="1dbb1-115">Um ponteiro para o buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-115">A pointer to the input buffer.</span></span>
<span data-ttu-id="1dbb1-116">Este parâmetro não é usado para esta operação.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-116">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="1dbb1-117">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="1dbb1-117">cbInBuffer</span></span>

<span data-ttu-id="1dbb1-118">O tamanho, em bytes, do buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-118">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="1dbb1-119">Este parâmetro não é usado para esta operação.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-119">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="1dbb1-120">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="1dbb1-120">lpvOutBuffer</span></span>

<span data-ttu-id="1dbb1-121">Um ponteiro para o buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-121">A pointer to the output buffer.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="1dbb1-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="1dbb1-122">cbOutBuffer</span></span>

<span data-ttu-id="1dbb1-123">O tamanho, em bytes, do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-123">The size, in bytes, of the output buffer.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="1dbb1-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="1dbb1-124">lpcbBytesReturned</span></span>

<span data-ttu-id="1dbb1-125">Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="1dbb1-126">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="1dbb1-126">lpvOverlapped</span></span>

<span data-ttu-id="1dbb1-127">Um ponteiro para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="1dbb1-127">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="1dbb1-128">Se o soquete *s* foi criado sem o atributo sobreposto, o parâmetro *lpOverlapped* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-128">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="1dbb1-129">Se *s* foi aberto com o atributo Overlapped e o parâmetro *LpOverlapped* não for **nulo**, a operação será executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="1dbb1-129">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="1dbb1-130">Nesse caso, o parâmetro *lpOverlapped* deve apontar para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-130">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="1dbb1-131">Para operações sobrepostas, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retorna imediatamente, e o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-131">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="1dbb1-132">Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-132">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="1dbb1-133">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="1dbb1-133">lpCompletionRoutine</span></span>

<span data-ttu-id="1dbb1-134">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="1dbb1-134">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="1dbb1-135">Um ponteiro para a rotina de conclusão chamada quando a operação foi concluída (ignorada para soquetes não sobrepostos).</span><span class="sxs-lookup"><span data-stu-id="1dbb1-135">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="1dbb1-136">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="1dbb1-136">lpThreadId</span></span>

<span data-ttu-id="1dbb1-137">Um ponteiro para uma estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a ser usado pelo provedor em uma chamada subsequente para [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="1dbb1-137">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="1dbb1-138">O provedor deve armazenar a estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) referenciada (não o ponteiro para o mesmo) até que a função [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) seja retornada.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-138">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="1dbb1-139">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="1dbb1-139">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="1dbb1-140">lpErrno</span><span class="sxs-lookup"><span data-stu-id="1dbb1-140">lpErrno</span></span>

<span data-ttu-id="1dbb1-141">Um ponteiro para o código de erro.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-141">A pointer to the error code.</span></span>

<span data-ttu-id="1dbb1-142">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="1dbb1-142">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="1dbb1-143">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1dbb1-143">Return value</span></span>

<span data-ttu-id="1dbb1-144">Se a operação for concluída com êxito, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará zero.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-144">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="1dbb1-145">Se a operação falhar ou estiver pendente, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará **um \_ erro de soquete**.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-145">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="1dbb1-146">Para obter informações de erro estendidas, chame [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="1dbb1-146">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="1dbb1-147">Código do erro</span><span class="sxs-lookup"><span data-stu-id="1dbb1-147">Error code</span></span> | <span data-ttu-id="1dbb1-148">Significado</span><span class="sxs-lookup"><span data-stu-id="1dbb1-148">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="1dbb1-149">**\_e/s de WSA \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-149">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="1dbb1-150">Uma operação sobreposta foi iniciada com êxito e a conclusão será indicada em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-150">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="1dbb1-151">**operação de WSA \_ \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-151">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="1dbb1-152">Uma operação sobreposta foi cancelada devido ao fechamento do soquete ou à execução do comando **sio \_ flush** IOCTL.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-152">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="1dbb1-153">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-153">**WSAEFAULT**</span></span> | <span data-ttu-id="1dbb1-154">O parâmetro *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço do usuário.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-154">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="1dbb1-155">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-155">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="1dbb1-156">A função é invocada quando um retorno de chamada está em andamento.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-156">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="1dbb1-157">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-157">**WSAEINTR**</span></span> | <span data-ttu-id="1dbb1-158">Uma operação de bloqueio foi interrompida.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-158">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="1dbb1-159">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-159">**WSAEINVAL**</span></span> | <span data-ttu-id="1dbb1-160">O parâmetro *dwIoControlCode* não é um comando válido ou um parâmetro de entrada especificado não é aceitável ou o comando não é aplicável ao tipo de soquete especificado.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-160">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="1dbb1-161">Esse erro será retornado se o parâmetro *cbInBuffer* não estiver definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-161">This error is returned if the *cbInBuffer* parameter is not set to **NULL**.</span></span> |
| <span data-ttu-id="1dbb1-162">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-162">**WSAENETDOWN**</span></span> | <span data-ttu-id="1dbb1-163">Falha no subsistema de rede.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-163">The network subsystem has failed.</span></span> |
| <span data-ttu-id="1dbb1-164">**WSAENOBUFS**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-164">**WSAENOBUFS**</span></span> | <span data-ttu-id="1dbb1-165">Não há espaço disponível no buffer.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-165">No buffer space available.</span></span> |
| <span data-ttu-id="1dbb1-166">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-166">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="1dbb1-167">Não há suporte para a opção de soquete no protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-167">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="1dbb1-168">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-168">**WSAENOTSOCK**</span></span> | <span data-ttu-id="1dbb1-169">O descritor *s* não é um soquete.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-169">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="1dbb1-170">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-170">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="1dbb1-171">Não há suporte para o comando IOCTL especificado.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-171">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="1dbb1-172">Esse erro será retornado se a **\_ consulta de \_ lista \_ de endereços sio** IOCTL não tiver suporte do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-172">This error is returned if the **SIO\_ADDRESS\_LIST\_QUERY** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="1dbb1-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="1dbb1-173">Remarks</span></span>

<span data-ttu-id="1dbb1-174">A **\_ consulta de \_ lista \_ de endereços sio** do IOCTL tem suporte no Windows 2000 e em versões posteriores do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-174">The **SIO\_ADDRESS\_LIST\_QUERY** IOCTL is supported on Windows 2000 and later versions of the operating system.</span></span>

<span data-ttu-id="1dbb1-175">O código de controle de **\_ consulta da \_ lista \_ de endereços sio** Obtém uma lista de endereços de transporte locais da família de protocolos do soquete à qual o aplicativo pode se associar.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-175">The **SIO\_ADDRESS\_LIST\_QUERY** control code obtains a list of local transport addresses of the socket's protocol family to which the application can bind.</span></span>
<span data-ttu-id="1dbb1-176">A lista de endereços varia de acordo com a família de endereços.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-176">The list of addresses varies based on address family.</span></span>

<span data-ttu-id="1dbb1-177">Para a \_ família de endereços INET6 de AF, todos os endereços são retornados, exceto o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1dbb1-177">For the AF\_INET6 address family, all addresses are returned except for the following:</span></span>

* <span data-ttu-id="1dbb1-178">Qualquer endereço IP em que o estado de detecção de endereço duplicado (DAD) não é IpDadStatePreferred.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-178">Any IP address where the duplicate address detection (DAD) state is not IpDadStatePreferred.</span></span>
* <span data-ttu-id="1dbb1-179">Qualquer endereço IP com um nível de escopo inferior a ScopeLevelSubnet em uma interface em que o tipo de interface é **se for \_ tipo \_ \_ loopback de software**.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-179">Any IP address with a scope level lower than ScopeLevelSubnet on an interface where the interface type is **IF\_TYPE\_SOFTWARE\_LOOPBACK**.</span></span>
<span data-ttu-id="1dbb1-180">Isso significa que os endereços de link local (FE80: \*) e loopback (:: 1) em interfaces do **\_ tipo \_ \_ loopback de software de tipos** são excluídos, mas não se esses endereços estiverem em uma interface com um tipo diferente.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-180">This means link-local (fe80:\*) and loopback (::1) addresses on interfaces of **IF\_TYPE\_SOFTWARE\_LOOPBACK** type are excluded, but not if these addresses are on an interface with a different type.</span></span>

<span data-ttu-id="1dbb1-181">Para a família de endereços **\_ inet** da série AF, todos os endereços são retornados, exceto o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1dbb1-181">For the **AF\_INET** address family, all addresses are returned except for the following:</span></span>

* <span data-ttu-id="1dbb1-182">Qualquer endereço IP em que o estado de detecção de endereço duplicado (DAD) não é IpDadStatePreferred.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-182">Any IP address where the duplicate address detection (DAD) state is not IpDadStatePreferred.</span></span>
* <span data-ttu-id="1dbb1-183">Qualquer endereço IP em uma interface em que o tipo de interface é **se o \_ tipo \_ \_ loopback de software** e link for local.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-183">Any IP address on an interface where the interface type is **IF\_TYPE\_SOFTWARE\_LOOPBACK** and link is local.</span></span>
<span data-ttu-id="1dbb1-184">Isso significa que endereços de link local (169,254.*) e loopback (127.*) em interfaces **do \_ tipo \_ \_ loopback de software** são excluídos, mas não se esses endereços estiverem em uma interface com um tipo diferente.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-184">This means link-local (169.254.*) and loopback (127.*) addresses on interfaces of **IF\_TYPE\_SOFTWARE\_LOOPBACK** type are excluded, but not if these addresses are on an interface with a different type.</span></span>

<span data-ttu-id="1dbb1-185">Para obter mais informações sobre o estado de DAD, consulte a documentação do auxiliar de IP na estrutura de endereços [**IP \_ Dad \_**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state) Enumeration e [**IP \_ Adapter \_ unicast \_ Address**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh) e a documentação MIB na estrutura de [**\_ \_ linha MIB UNICASTIPADDRESS**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row) .</span><span class="sxs-lookup"><span data-stu-id="1dbb1-185">For more information on DAD state, see the IP Helper documentation on the [**IP\_DAD\_STATE**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state) enumeration and [**IP\_ADAPTER\_UNICAST\_ADDRESS**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh) structure and the MIB documentation on the [**MIB\_UNICASTIPADDRESS\_ROW**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row) structure.</span></span>
<span data-ttu-id="1dbb1-186">Para obter mais informações sobre o tipo de interface, consulte a documentação auxiliar de IP na estrutura [**\_ \_ endereços de adaptador IP**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) e a função [**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) e a documentação MIB na estrutura [**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2) .</span><span class="sxs-lookup"><span data-stu-id="1dbb1-186">For more information on interface type, see the IP Helper documentation on the [**IP\_ADAPTER\_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) structure and the [**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) function and the MIB documentation on [**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2) structure.</span></span>
<span data-ttu-id="1dbb1-187">Para obter mais informações sobre o nível de escopo, consulte a documentação auxiliar de IP na estrutura de [**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) e a enumeração de [**\_ nível de escopo**](/windows/desktop/api/ws2def/ne-ws2def-scope_level) .</span><span class="sxs-lookup"><span data-stu-id="1dbb1-187">For more information on the scope level, see the IP Helper documentation on the [**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) structure and the [**SCOPE\_LEVEL**](/windows/desktop/api/ws2def/ne-ws2def-scope_level) enumeration.</span></span>

<span data-ttu-id="1dbb1-188">A lista retornada no buffer de saída apontada pelo parâmetro *lpvOutBuffer* está na forma de uma estrutura de [**\_ \_ lista de endereços de soquete**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list) .</span><span class="sxs-lookup"><span data-stu-id="1dbb1-188">The list returned in the output buffer pointed to by the *lpvOutBuffer* parameter is in the form of a [**SOCKET\_ADDRESS\_LIST**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list) structure.</span></span>

<span data-ttu-id="1dbb1-189">Se o buffer de saída especificado no parâmetro *lpvOutBuffer* não for grande o suficiente para conter a lista de endereços, o **\_ erro de soquete** será retornado como resultado desse IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [WSAEFAULT](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="1dbb1-189">If the output buffer specified in the *lpvOutBuffer* parameter is not large enough to contain the address list, **SOCKET\_ERROR** is returned as the result of this IOCTL and [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [WSAEFAULT](windows-sockets-error-codes-2.md).</span></span>
<span data-ttu-id="1dbb1-190">O tamanho necessário, em bytes, para o buffer de saída é retornado no parâmetro *lpcbBytesReturned* nesse caso.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-190">The required size, in bytes, for the output buffer is returned in the *lpcbBytesReturned* parameter in this case.</span></span>
<span data-ttu-id="1dbb1-191">Observe que o código de erro [WSAEFAULT](windows-sockets-error-codes-2.md) também será retornado se o parâmetro *lpvInBuffer*, *lpvOutBuffer* ou *lpcbBytesReturned* não estiver completamente contido em uma parte válida do espaço de endereço de usuário.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-191">Note the [WSAEFAULT](windows-sockets-error-codes-2.md) error code is also returned if the *lpvInBuffer*, *lpvOutBuffer*, or *lpcbBytesReturned* parameter is not completely contained in a valid part of the user address space.</span></span>

<span data-ttu-id="1dbb1-192">A **\_ consulta de \_ lista \_ de endereços sio** IOCTL normalmente é chamada de forma síncrona com o parâmetro *lpvOverlapped* definido como **NULL**, pois a lista de endereços é retornada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-192">The **SIO\_ADDRESS\_LIST\_QUERY** IOCTL is normally called synchronously with the *lpvOverlapped* parameter set to **NULL**, since the list of addresses is returned immediately.</span></span>

<span data-ttu-id="1dbb1-193">**Observação**  Em ambientes Windows plug-n-play, os endereços podem ser adicionados e removidos dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-193">**Note**  In Windows Plug-n-Play environments, addresses can be added and removed dynamically.</span></span>
<span data-ttu-id="1dbb1-194">Portanto, os aplicativos não podem contar com as informações retornadas pela **\_ consulta de \_ lista \_ de endereços sio** para serem persistentes.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-194">Therefore, applications cannot rely on the information returned by **SIO\_ADDRESS\_LIST\_QUERY** to be persistent.</span></span>
<span data-ttu-id="1dbb1-195">Os aplicativos podem se registrar para notificações de alteração de endereço por meio do IOCTL de **\_ alteração da \_ lista \_ de endereços sio** , que fornece notificação por meio do evento de alteração da lista de endereços e/s sobreposta ou **FD \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="1dbb1-195">Applications may register for address change notifications through the **SIO\_ADDRESS\_LIST\_CHANGE** IOCTL which provides for notification through either overlapped I/O or **FD\_ADDRESS\_LIST\_CHANGE** event.</span></span>
<span data-ttu-id="1dbb1-196">A seguinte sequência de ações pode ser usada para garantir que o aplicativo sempre tenha informações da lista de endereços atual:</span><span class="sxs-lookup"><span data-stu-id="1dbb1-196">The following sequence of actions can be used to guarantee that the application always has current address list information:</span></span>

* <span data-ttu-id="1dbb1-197">Emitir o IOCTL de **\_ alteração da \_ lista \_ de endereços sio**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-197">Issue the **SIO\_ADDRESS\_LIST\_CHANGE** IOCTL</span></span>
* <span data-ttu-id="1dbb1-198">Emitir o IOCTL de **\_ consulta de \_ lista \_ de endereços sio**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-198">Issue the **SIO\_ADDRESS\_LIST\_QUERY** IOCTL</span></span>
* <span data-ttu-id="1dbb1-199">Sempre que a chamada de **\_ alteração da \_ lista \_ de endereços sio** notifica o aplicativo sobre uma alteração na lista de endereços (por meio de e/s sobreposta ou sinalizando o evento de **alteração da \_ lista de endereços \_ \_ FD** ), toda a sequência de ações deve ser repetida.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-199">Whenever the **SIO\_ADDRESS\_LIST\_CHANGE** IOCTL call notifies the application of an address list change (either through overlapped I/O or by signaling **FD\_ADDRESS\_LIST\_CHANGE** event), the whole sequence of actions should be repeated.</span></span>

<span data-ttu-id="1dbb1-200">No SDK (Software Development Kit) do Microsoft Windows lançado para Windows Vista e posterior, a organização dos arquivos de cabeçalho foi alterada e o código de controle de consulta da lista de endereços do sio é definido no arquivo de cabeçalho *Ws2def. h* . **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-200">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the **SIO\_ADDRESS\_LIST\_QUERY** control code is defined in the *Ws2def.h* header file.</span></span>
<span data-ttu-id="1dbb1-201">Observe que o arquivo de cabeçalho *Ws2def. h* é incluído automaticamente no *Winsock2. h* e nunca deve ser usado diretamente.</span><span class="sxs-lookup"><span data-stu-id="1dbb1-201">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="see-also"></a><span data-ttu-id="1dbb1-202">Confira também</span><span class="sxs-lookup"><span data-stu-id="1dbb1-202">See also</span></span>

[<span data-ttu-id="1dbb1-203">**GetAdaptersAddresses**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-203">**GetAdaptersAddresses**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

[<span data-ttu-id="1dbb1-204">**IP_ADAPTER_ADDRESSES**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-204">**IP_ADAPTER_ADDRESSES**</span></span>](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp)

[<span data-ttu-id="1dbb1-205">**IP_ADAPTER_UNICAST_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-205">**IP_ADAPTER_UNICAST_ADDRESS**</span></span>](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh)

[<span data-ttu-id="1dbb1-206">**IP_DAD_STATE**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-206">**IP_DAD_STATE**</span></span>](/windows/desktop/api/nldef/ne-nldef-nl_dad_state)

[<span data-ttu-id="1dbb1-207">**MIB_IF_ROW2**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-207">**MIB_IF_ROW2**</span></span>](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2)

[<span data-ttu-id="1dbb1-208">**MIB_UNICASTIPADDRESS_ROW**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-208">**MIB_UNICASTIPADDRESS_ROW**</span></span>](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row)

[<span data-ttu-id="1dbb1-209">**SCOPE_LEVEL**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-209">**SCOPE_LEVEL**</span></span>](/windows/desktop/api/ws2def/ne-ws2def-scope_level)

[<span data-ttu-id="1dbb1-210">**SOCKET_ADDRESS_LIST**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-210">**SOCKET_ADDRESS_LIST**</span></span>](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list)

[<span data-ttu-id="1dbb1-211">**SSA**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-211">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="1dbb1-212">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-212">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="1dbb1-213">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-213">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="1dbb1-214">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-214">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="1dbb1-215">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-215">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="1dbb1-216">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-216">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="1dbb1-217">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="1dbb1-217">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
