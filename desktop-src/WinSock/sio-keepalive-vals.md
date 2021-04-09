---
description: O código de controle habilita ou desabilita a configuração por conexão da opção TCP Keep-Alive que especifica o tempo limite e o intervalo de Keep-Alive TCP.
ms.assetid: c02e8ad5-bfad-489f-83bf-39b53fd68bde
title: SIO_KEEPALIVE_VALS código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ea8aabf452436ca2bbd6307366e7fc24f913dbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091306"
---
# <a name="sio_keepalive_vals-control-code"></a><span data-ttu-id="b8289-103">SIO_KEEPALIVE_VALS código de controle</span><span class="sxs-lookup"><span data-stu-id="b8289-103">SIO_KEEPALIVE_VALS Control Code</span></span>

## <a name="description"></a><span data-ttu-id="b8289-104">Description</span><span class="sxs-lookup"><span data-stu-id="b8289-104">Description</span></span>

<span data-ttu-id="b8289-105">O código de controle **sio \_ KeepAlive \_ Vals** habilita ou desabilita a configuração por conexão da opção TCP Keep-Alive que especifica o tempo limite e o intervalo de Keep-Alive TCP.</span><span class="sxs-lookup"><span data-stu-id="b8289-105">The **SIO\_KEEPALIVE\_VALS** control code enables or disables the per-connection setting of the TCP keep-alive option which specifies the TCP keep-alive timeout and interval.</span></span>

<span data-ttu-id="b8289-106">Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="b8289-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="b8289-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8289-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="b8289-108">s</span><span class="sxs-lookup"><span data-stu-id="b8289-108">s</span></span>

<span data-ttu-id="b8289-109">Um descritor que identifica um soquete.</span><span class="sxs-lookup"><span data-stu-id="b8289-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="b8289-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="b8289-110">dwIoControlCode</span></span>

<span data-ttu-id="b8289-111">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="b8289-111">The control code for the operation.</span></span>
<span data-ttu-id="b8289-112">Use **sio \_ KeepAlive \_ Vals** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="b8289-112">Use **SIO\_KEEPALIVE\_VALS** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="b8289-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="b8289-113">lpvInBuffer</span></span>

<span data-ttu-id="b8289-114">Um ponteiro para o buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="b8289-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="b8289-115">Esse parâmetro deve apontar para uma estrutura **TCP \_ KeepAlive** .</span><span class="sxs-lookup"><span data-stu-id="b8289-115">This parameter should point to a **tcp\_keepalive** structure.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="b8289-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="b8289-116">cbInBuffer</span></span>

<span data-ttu-id="b8289-117">O tamanho, em bytes, do buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="b8289-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="b8289-118">Esse parâmetro deve ser igual ou maior que o tamanho da estrutura **TCP \_ KeepAlive** apontada pelo parâmetro *lpvInBuffer* .</span><span class="sxs-lookup"><span data-stu-id="b8289-118">This parameter should equal to or greater than the size of the **tcp\_keepalive** structure pointed to by the *lpvInBuffer* parameter.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="b8289-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="b8289-119">lpvOutBuffer</span></span>

<span data-ttu-id="b8289-120">Um ponteiro para o buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="b8289-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="b8289-121">Este parâmetro não é usado para esta operação.</span><span class="sxs-lookup"><span data-stu-id="b8289-121">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="b8289-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="b8289-122">cbOutBuffer</span></span>

<span data-ttu-id="b8289-123">O tamanho, em bytes, do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="b8289-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="b8289-124">Esse parâmetro deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="b8289-124">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="b8289-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="b8289-125">lpcbBytesReturned</span></span>

<span data-ttu-id="b8289-126">Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="b8289-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>
<span data-ttu-id="b8289-127">Esse parâmetro retornado aponta para um valor **DWORD** de zero para esta operação, pois não há nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="b8289-127">This returned parameter points to a **DWORD** value of zero for this operation, since there is no output.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="b8289-128">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="b8289-128">lpvOverlapped</span></span>

<span data-ttu-id="b8289-129">Um ponteiro para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="b8289-129">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="b8289-130">Se o soquete *s* foi criado sem o atributo sobreposto, o parâmetro *lpOverlapped* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="b8289-130">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="b8289-131">Se *s* foi aberto com o atributo Overlapped e o parâmetro *LpOverlapped* não for **nulo**, a operação será executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="b8289-131">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="b8289-132">Nesse caso, o parâmetro *lpOverlapped* deve apontar para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="b8289-132">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="b8289-133">Para operações sobrepostas, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retorna imediatamente, e o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="b8289-133">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="b8289-134">Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.</span><span class="sxs-lookup"><span data-stu-id="b8289-134">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="b8289-135">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="b8289-135">lpCompletionRoutine</span></span>

<span data-ttu-id="b8289-136">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="b8289-136">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="b8289-137">Um ponteiro para a rotina de conclusão chamada quando a operação foi concluída (ignorada para soquetes não sobrepostos).</span><span class="sxs-lookup"><span data-stu-id="b8289-137">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="b8289-138">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="b8289-138">lpThreadId</span></span>

<span data-ttu-id="b8289-139">Um ponteiro para uma estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a ser usado pelo provedor em uma chamada subsequente para [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="b8289-139">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="b8289-140">O provedor deve armazenar a estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) referenciada (não o ponteiro para o mesmo) até que a função [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) seja retornada.</span><span class="sxs-lookup"><span data-stu-id="b8289-140">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="b8289-141">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="b8289-141">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="b8289-142">lpErrno</span><span class="sxs-lookup"><span data-stu-id="b8289-142">lpErrno</span></span>

<span data-ttu-id="b8289-143">Um ponteiro para o código de erro.</span><span class="sxs-lookup"><span data-stu-id="b8289-143">A pointer to the error code.</span></span>

<span data-ttu-id="b8289-144">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="b8289-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="b8289-145">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b8289-145">Return value</span></span>

<span data-ttu-id="b8289-146">Se a operação for concluída com êxito, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará zero.</span><span class="sxs-lookup"><span data-stu-id="b8289-146">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="b8289-147">Se a operação falhar ou estiver pendente, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará **um \_ erro de soquete**.</span><span class="sxs-lookup"><span data-stu-id="b8289-147">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="b8289-148">Para obter informações de erro estendidas, chame [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="b8289-148">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="b8289-149">Código do erro</span><span class="sxs-lookup"><span data-stu-id="b8289-149">Error code</span></span> | <span data-ttu-id="b8289-150">Significado</span><span class="sxs-lookup"><span data-stu-id="b8289-150">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="b8289-151">**\_e/s de WSA \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="b8289-151">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="b8289-152">Uma operação sobreposta foi iniciada com êxito e a conclusão será indicada em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="b8289-152">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="b8289-153">**operação de WSA \_ \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="b8289-153">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="b8289-154">Uma operação sobreposta foi cancelada devido ao fechamento do soquete ou à execução do comando **SIO_FLUSH IOCTL** .</span><span class="sxs-lookup"><span data-stu-id="b8289-154">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH IOCTL** command.</span></span> |
| <span data-ttu-id="b8289-155">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="b8289-155">**WSAEFAULT**</span></span> | <span data-ttu-id="b8289-156">O parâmetro *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço do usuário.</span><span class="sxs-lookup"><span data-stu-id="b8289-156">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="b8289-157">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="b8289-157">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="b8289-158">A função é invocada quando um retorno de chamada está em andamento.</span><span class="sxs-lookup"><span data-stu-id="b8289-158">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="b8289-159">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="b8289-159">**WSAEINTR**</span></span> | <span data-ttu-id="b8289-160">Uma operação de bloqueio foi interrompida.</span><span class="sxs-lookup"><span data-stu-id="b8289-160">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="b8289-161">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="b8289-161">**WSAEINVAL**</span></span> | <span data-ttu-id="b8289-162">O parâmetro *dwIoControlCode* não é um comando válido ou um parâmetro de entrada especificado não é aceitável ou o comando não é aplicável ao tipo de soquete especificado.</span><span class="sxs-lookup"><span data-stu-id="b8289-162">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="b8289-163">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="b8289-163">**WSAENETDOWN**</span></span> | <span data-ttu-id="b8289-164">Falha no subsistema de rede.</span><span class="sxs-lookup"><span data-stu-id="b8289-164">The network subsystem has failed.</span></span> |
| <span data-ttu-id="b8289-165">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="b8289-165">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="b8289-166">Não há suporte para a opção de soquete no protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="b8289-166">The socket option is not supported on the specified protocol.</span></span> <span data-ttu-id="b8289-167">Esse erro é retornado para um soquete de datagrama.</span><span class="sxs-lookup"><span data-stu-id="b8289-167">This error is returned for a datagram socket.</span></span> |
| <span data-ttu-id="b8289-168">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="b8289-168">**WSAENOTSOCK**</span></span> | <span data-ttu-id="b8289-169">O descritor s não é um soquete.</span><span class="sxs-lookup"><span data-stu-id="b8289-169">The descriptor s is not a socket.</span></span> |
| <span data-ttu-id="b8289-170">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="b8289-170">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="b8289-171">Não há suporte para o comando IOCTL especificado.</span><span class="sxs-lookup"><span data-stu-id="b8289-171">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="b8289-172">Esse erro será retornado se o **sio \_ KeepAlive \_ Vals** IOCTL não tiver suporte do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="b8289-172">This error is returned if the **SIO\_KEEPALIVE\_VALS** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="b8289-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8289-173">Remarks</span></span>

<span data-ttu-id="b8289-174">O **sio \_ KeepAlive \_ Vals** IOCTL tem suporte no Windows 2000 e versões posteriores do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b8289-174">The **SIO\_KEEPALIVE\_VALS** IOCTL is supported on Windows 2000 and later versions of the operating system.</span></span>

<span data-ttu-id="b8289-175">O código de controle do **sio \_ KeepAlive \_ Vals** habilita ou desabilita a configuração por conexão da opção TCP Keep-Alive que especifica o tempo limite e o intervalo de Keep-Alive TCP usados para pacotes Keep-Alive TCP.</span><span class="sxs-lookup"><span data-stu-id="b8289-175">The **SIO\_KEEPALIVE\_VALS** control code enables or disables the per-connection setting of the TCP keep-alive option which specifies the TCP keep-alive timeout and interval used for TCP keep-alive packets.</span></span>
<span data-ttu-id="b8289-176">Para obter mais informações sobre a opção keep-alive, consulte a seção 4.2.3.6 sobre os requisitos para hosts da Internet — camadas de comunicação especificadas no RFC 1122 disponíveis no [site da IETF](https://www.ietf.org/rfc/rfc1122.txt).</span><span class="sxs-lookup"><span data-stu-id="b8289-176">For more information on the keep-alive option, see section 4.2.3.6 on the Requirements for Internet Hosts—Communication Layers specified in RFC 1122 available at the [IETF website](https://www.ietf.org/rfc/rfc1122.txt).</span></span>
<span data-ttu-id="b8289-177">(Este recurso só pode estar disponível em inglês.)</span><span class="sxs-lookup"><span data-stu-id="b8289-177">(This resource may only be available in English.)</span></span>

<span data-ttu-id="b8289-178">O parâmetro *lpvInBuffer* deve apontar para uma estrutura **TCP \_ KeepAlive** definida no arquivo de cabeçalho *Mstcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="b8289-178">The *lpvInBuffer* parameter should point to a **tcp\_keepalive** structure defined in the *Mstcpip.h* header file.</span></span>
<span data-ttu-id="b8289-179">Essa estrutura é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b8289-179">This structure is defined as follows:</span></span>

```cpp
/* Argument structure for SIO_KEEPALIVE_VALS */
struct tcp_keepalive {
    u_long  onoff;
    u_long  keepalivetime;
    u_long  keepaliveinterval;
};
```

<span data-ttu-id="b8289-180">O valor especificado no membro **Onoff** determina se o TCP Keep-Alive está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="b8289-180">The value specified in the **onoff** member determines if TCP keep-alive is enabled or disabled.</span></span>
<span data-ttu-id="b8289-181">Se o membro **Onoff** for definido como um valor diferente de zero, o TCP Keep-Alive será habilitado e os outros membros da estrutura serão usados.</span><span class="sxs-lookup"><span data-stu-id="b8289-181">If the **onoff** member is set to a nonzero value, TCP keep-alive is enabled and the other members in the structure are used.</span></span>
<span data-ttu-id="b8289-182">O membro **KeepAliveTime** especifica o tempo limite, em milissegundos, sem atividade até que o primeiro pacote keep-alive seja enviado.</span><span class="sxs-lookup"><span data-stu-id="b8289-182">The **keepalivetime** member specifies the timeout, in milliseconds, with no activity until the first keep-alive packet is sent.</span></span>
<span data-ttu-id="b8289-183">O membro **KeepAliveInterval** especifica o intervalo, em milissegundos, entre quando os pacotes Keep Alive sucessivos são enviados, caso nenhuma confirmação seja recebida.</span><span class="sxs-lookup"><span data-stu-id="b8289-183">The **keepaliveinterval** member specifies the interval, in milliseconds, between when successive keep-alive packets are sent if no acknowledgement is received.</span></span>

<span data-ttu-id="b8289-184">A opção [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) , que é uma das [**opções de Soquete SOL_SOCKET**](/windows/desktop/winsock/sol-socket-socket-options), também pode ser usada para habilitar ou desabilitar o TCP Keep-Alive em uma conexão, bem como consultar o estado atual dessa opção.</span><span class="sxs-lookup"><span data-stu-id="b8289-184">The [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) option, which is one of the [**SOL_SOCKET Socket Options**](/windows/desktop/winsock/sol-socket-socket-options), can also be used to enable or disable the TCP keep-alive on a connection, as well as query the current state of this option.</span></span>
<span data-ttu-id="b8289-185">Para consultar se o TCP Keep-Alive está habilitado em um soquete, a função getsockopt pode ser chamada com a opção [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) .</span><span class="sxs-lookup"><span data-stu-id="b8289-185">To query whether TCP keep-alive is enabled on a socket, the getsockopt function can be called with the [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) option.</span></span>
<span data-ttu-id="b8289-186">Para habilitar ou desabilitar o TCP Keep-Alive, a função **setsockopt** pode ser chamada com a opção [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) .</span><span class="sxs-lookup"><span data-stu-id="b8289-186">To enable or disable TCP keep-alive, the **setsockopt** function can be called with the [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) option.</span></span>
<span data-ttu-id="b8289-187">Se o TCP Keep-Alive estiver habilitado com [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive), as configurações de TCP padrão serão usadas para tempo limite de Keep-Alive e intervalo, a menos que esses valores tenham sido alterados usando **sio \_ KeepAlive \_ Vals**.</span><span class="sxs-lookup"><span data-stu-id="b8289-187">If TCP keep-alive is enabled with [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive), then the default TCP settings are used for keep-alive timeout and interval unless these values have been changed using **SIO\_KEEPALIVE\_VALS**.</span></span>

<span data-ttu-id="b8289-188">O valor padrão em todo o sistema do tempo limite de Keep-Alive é controlável por meio da configuração do registro [**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) que usa um valor em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="b8289-188">The default system-wide value of the keep-alive timeout is controllable through the [**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) registry setting which takes a value in milliseconds.</span></span> <span data-ttu-id="b8289-189">Se a chave não for definida, o tempo limite de Keep-Alive padrão será de 2 horas.</span><span class="sxs-lookup"><span data-stu-id="b8289-189">If the key is not set, the default keep-alive timeout is 2 hours.</span></span>
<span data-ttu-id="b8289-190">O valor padrão em todo o sistema do intervalo Keep-Alive é controlável por meio da configuração do registro [**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) , que usa um valor em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="b8289-190">The default system-wide value of the keep-alive interval is controllable through the [**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) registry setting which takes a value in milliseconds.</span></span> <span data-ttu-id="b8289-191">Se a chave não for definida, o intervalo de Keep-Alive padrão será de 1 segundo.</span><span class="sxs-lookup"><span data-stu-id="b8289-191">If the key is not set, the default keep-alive interval is 1 second.</span></span>

<span data-ttu-id="b8289-192">No Windows Vista e posterior, o número de investigações de Keep-Alive (retransmissões de dados) é definido como 10 e não pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="b8289-192">On Windows Vista and later, the number of keep-alive probes (data retransmissions) is set to 10 and cannot be changed.</span></span>

<span data-ttu-id="b8289-193">No Windows Server 2003, Windows XP e Windows 2000, a configuração padrão para o número de investigações Keep-Alive é 5.</span><span class="sxs-lookup"><span data-stu-id="b8289-193">On Windows Server 2003, Windows XP, and Windows 2000, the default setting for number of keep-alive probes is 5.</span></span>
<span data-ttu-id="b8289-194">O número de investigações Keep Alive é controlável por meio das configurações de registro **TcpMaxDataRetransmissions** e [**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) .</span><span class="sxs-lookup"><span data-stu-id="b8289-194">The number of keep-alive probes is controllable through the **TcpMaxDataRetransmissions** and [**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) registry settings.</span></span>
<span data-ttu-id="b8289-195">O número de investigações Keep Alive é definido como o maior dos dois valores de chave do registro.</span><span class="sxs-lookup"><span data-stu-id="b8289-195">The number of keep-alive probes is set to the larger of the two registry key values.</span></span>
<span data-ttu-id="b8289-196">Se esse número for 0, as investigações Keep-Alive não serão enviadas.</span><span class="sxs-lookup"><span data-stu-id="b8289-196">If this number is 0, then keep-alive probes will not be sent.</span></span>
<span data-ttu-id="b8289-197">Se esse número estiver acima de 255, ele será ajustado para 255.</span><span class="sxs-lookup"><span data-stu-id="b8289-197">If this number is above 255, then it is adjusted to 255.</span></span>

## <a name="see-also"></a><span data-ttu-id="b8289-198">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8289-198">See also</span></span>

<span data-ttu-id="b8289-199">[**KeepAlivetime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b8289-199">[**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span></span>

<span data-ttu-id="b8289-200">[**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b8289-200">[**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span></span>

<span data-ttu-id="b8289-201">[**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b8289-201">[**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span></span>

[<span data-ttu-id="b8289-202">SSA</span><span class="sxs-lookup"><span data-stu-id="b8289-202">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="b8289-203">**SO_KEEPALIVE**</span><span class="sxs-lookup"><span data-stu-id="b8289-203">**SO_KEEPALIVE**</span></span>](/windows/desktop/winsock/so-keepalive)

[<span data-ttu-id="b8289-204">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="b8289-204">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="b8289-205">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="b8289-205">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="b8289-206">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="b8289-206">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="b8289-207">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="b8289-207">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="b8289-208">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="b8289-208">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="b8289-209">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="b8289-209">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
