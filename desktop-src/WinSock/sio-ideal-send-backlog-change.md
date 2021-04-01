---
description: O código de controle notifica um aplicativo quando o valor da pendência de envio ideal é alterado para a conexão.
ms.assetid: 337883a5-7ceb-40d3-b318-b86dd488b94a
title: SIO_IDEAL_SEND_BACKLOG_CHANGE código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 4eb07efecd39774c60d47cbcf7245c5831760e06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661774"
---
# <a name="sio_ideal_send_backlog_change-control-code"></a><span data-ttu-id="982f2-103">SIO_IDEAL_SEND_BACKLOG_CHANGE código de controle</span><span class="sxs-lookup"><span data-stu-id="982f2-103">SIO_IDEAL_SEND_BACKLOG_CHANGE Control Code</span></span>

## <a name="description"></a><span data-ttu-id="982f2-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="982f2-104">Description</span></span>

<span data-ttu-id="982f2-105">O código de controle de **alteração da pendência de envio do sio \_ ideal \_ \_ \_** notifica um aplicativo quando o valor da pendência de envio ideal (ISB) é alterado para a conexão.</span><span class="sxs-lookup"><span data-stu-id="982f2-105">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** control code notifies an application when the ideal send backlog (ISB) value changes for the connection.</span></span>

<span data-ttu-id="982f2-106">Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="982f2-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_CHANGE, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_CHANGE, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="982f2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="982f2-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="982f2-108">s</span><span class="sxs-lookup"><span data-stu-id="982f2-108">s</span></span>

<span data-ttu-id="982f2-109">Um descritor que identifica um soquete.</span><span class="sxs-lookup"><span data-stu-id="982f2-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="982f2-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="982f2-110">dwIoControlCode</span></span>

<span data-ttu-id="982f2-111">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="982f2-111">The control code for the operation.</span></span>
<span data-ttu-id="982f2-112">Use **a \_ \_ alteração da \_ pendência \_ de envio sio ideal** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="982f2-112">Use **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="982f2-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="982f2-113">lpvInBuffer</span></span>

<span data-ttu-id="982f2-114">Um ponteiro para o buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="982f2-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="982f2-115">Este parâmetro não é usado para esta operação.</span><span class="sxs-lookup"><span data-stu-id="982f2-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="982f2-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="982f2-116">cbInBuffer</span></span>

<span data-ttu-id="982f2-117">O tamanho, em bytes, do buffer de entrada. Este parâmetro não é usado para esta operação.</span><span class="sxs-lookup"><span data-stu-id="982f2-117">The size, in bytes, of the input buffer.This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="982f2-118">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="982f2-118">lpvOutBuffer</span></span>

<span data-ttu-id="982f2-119">Um ponteiro para o buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="982f2-119">A pointer to the output buffer.</span></span>
<span data-ttu-id="982f2-120">Este parâmetro não é usado para esta operação.</span><span class="sxs-lookup"><span data-stu-id="982f2-120">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="982f2-121">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="982f2-121">cbOutBuffer</span></span>

<span data-ttu-id="982f2-122">O tamanho, em bytes, do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="982f2-122">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="982f2-123">Esse parâmetro deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="982f2-123">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="982f2-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="982f2-124">lpcbBytesReturned</span></span>

<span data-ttu-id="982f2-125">Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="982f2-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>
<span data-ttu-id="982f2-126">Esse parâmetro retornado aponta para um valor **DWORD** de zero para esta operação, pois não há nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="982f2-126">This returned parameter points to a **DWORD** value of zero for this operation, since there is no output.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="982f2-127">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="982f2-127">lpvOverlapped</span></span>

<span data-ttu-id="982f2-128">Um ponteiro para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="982f2-128">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="982f2-129">Se o soquete *s* foi criado sem o atributo sobreposto, o parâmetro *lpOverlapped* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="982f2-129">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="982f2-130">Se *s* foi aberto com o atributo Overlapped e o parâmetro *LpOverlapped* não for **nulo**, a operação será executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="982f2-130">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="982f2-131">Nesse caso, o parâmetro *lpOverlapped* deve apontar para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="982f2-131">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="982f2-132">Para operações sobrepostas, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retorna imediatamente, e o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="982f2-132">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="982f2-133">Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.</span><span class="sxs-lookup"><span data-stu-id="982f2-133">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="982f2-134">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="982f2-134">lpCompletionRoutine</span></span>

<span data-ttu-id="982f2-135">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="982f2-135">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="982f2-136">Um ponteiro para a rotina de conclusão chamada quando a operação foi concluída (ignorada para soquetes não sobrepostos).</span><span class="sxs-lookup"><span data-stu-id="982f2-136">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="982f2-137">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="982f2-137">lpThreadId</span></span>

<span data-ttu-id="982f2-138">Um ponteiro para uma estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a ser usado pelo provedor em uma chamada subsequente para [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="982f2-138">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="982f2-139">O provedor deve armazenar a estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) referenciada (não o ponteiro para o mesmo) até que a função [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) seja retornada.</span><span class="sxs-lookup"><span data-stu-id="982f2-139">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="982f2-140">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="982f2-140">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="982f2-141">lpErrno</span><span class="sxs-lookup"><span data-stu-id="982f2-141">lpErrno</span></span>

<span data-ttu-id="982f2-142">Um ponteiro para o código de erro.</span><span class="sxs-lookup"><span data-stu-id="982f2-142">A pointer to the error code.</span></span>

<span data-ttu-id="982f2-143">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="982f2-143">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="982f2-144">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="982f2-144">Return value</span></span>

<span data-ttu-id="982f2-145">Se a operação for concluída com êxito, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará zero.</span><span class="sxs-lookup"><span data-stu-id="982f2-145">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="982f2-146">Se a operação falhar ou estiver pendente, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará **um \_ erro de soquete**.</span><span class="sxs-lookup"><span data-stu-id="982f2-146">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="982f2-147">Para obter informações de erro estendidas, chame [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="982f2-147">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="982f2-148">Código do erro</span><span class="sxs-lookup"><span data-stu-id="982f2-148">Error code</span></span> | <span data-ttu-id="982f2-149">Significado</span><span class="sxs-lookup"><span data-stu-id="982f2-149">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="982f2-150">**\_e/s de WSA \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="982f2-150">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="982f2-151">Uma operação sobreposta foi iniciada com êxito e a conclusão será indicada em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="982f2-151">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="982f2-152">**operação de WSA \_ \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="982f2-152">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="982f2-153">Uma operação sobreposta foi cancelada devido ao fechamento do soquete ou à execução do comando **sio \_ flush** IOCTL.</span><span class="sxs-lookup"><span data-stu-id="982f2-153">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="982f2-154">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="982f2-154">**WSAEFAULT**</span></span> | <span data-ttu-id="982f2-155">O parâmetro *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço do usuário.</span><span class="sxs-lookup"><span data-stu-id="982f2-155">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="982f2-156">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="982f2-156">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="982f2-157">A função é invocada quando um retorno de chamada está em andamento.</span><span class="sxs-lookup"><span data-stu-id="982f2-157">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="982f2-158">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="982f2-158">**WSAEINTR**</span></span> | <span data-ttu-id="982f2-159">Uma operação de bloqueio foi interrompida.</span><span class="sxs-lookup"><span data-stu-id="982f2-159">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="982f2-160">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="982f2-160">**WSAEINVAL**</span></span> | <span data-ttu-id="982f2-161">O parâmetro *dwIoControlCode* não é um comando válido ou um parâmetro de entrada especificado não é aceitável ou o comando não é aplicável ao tipo de soquete especificado.</span><span class="sxs-lookup"><span data-stu-id="982f2-161">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="982f2-162">Esse erro será retornado se o parâmetro *cbOutBuffer* não for zero.</span><span class="sxs-lookup"><span data-stu-id="982f2-162">This error is returned if the *cbOutBuffer* parameter is not zero.</span></span> |
| <span data-ttu-id="982f2-163">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="982f2-163">**WSAENETDOWN**</span></span> | <span data-ttu-id="982f2-164">Falha no subsistema de rede.</span><span class="sxs-lookup"><span data-stu-id="982f2-164">The network subsystem has failed.</span></span> |
| <span data-ttu-id="982f2-165">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="982f2-165">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="982f2-166">Não há suporte para a opção de soquete no protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="982f2-166">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="982f2-167">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="982f2-167">**WSAENOTCONN**</span></span> | <span data-ttu-id="982f2-168">O soquete *s* não está conectado.</span><span class="sxs-lookup"><span data-stu-id="982f2-168">The socket *s* is not connected.</span></span> |
| <span data-ttu-id="982f2-169">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="982f2-169">**WSAENOTSOCK**</span></span> | <span data-ttu-id="982f2-170">O descritor *s* não é um soquete.</span><span class="sxs-lookup"><span data-stu-id="982f2-170">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="982f2-171">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="982f2-171">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="982f2-172">Não há suporte para o comando IOCTL especificado.</span><span class="sxs-lookup"><span data-stu-id="982f2-172">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="982f2-173">Esse erro será retornado se o provedor de transporte não oferecer suporte ao **sio \_ ideal para \_ Enviar \_ pendências de \_ alteração** .</span><span class="sxs-lookup"><span data-stu-id="982f2-173">This error is returned if the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="982f2-174">Esse erro também é retornado quando uma tentativa de usar o **sio \_ ideal \_ de \_ \_ alteração de pendência de envio** do IOCTL é feita em um soquete de datagrama.</span><span class="sxs-lookup"><span data-stu-id="982f2-174">This error is also returned when an attempt to use the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is made on a datagram socket.</span></span> |

## <a name="remarks"></a><span data-ttu-id="982f2-175">Comentários</span><span class="sxs-lookup"><span data-stu-id="982f2-175">Remarks</span></span>

<span data-ttu-id="982f2-176">O **sio \_ ideal para \_ Enviar \_ pendências de \_ alteração do registro posterior** tem suporte no Windows Server 2008, no Windows Vista com Service Pack 1 (SP1) e em versões posteriores do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="982f2-176">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is supported on Windows Server 2008, Windows Vista with Service Pack 1 (SP1), and later versions of the operating system.</span></span>

<span data-ttu-id="982f2-177">Ao enviar dados por uma conexão TCP usando o Windows Sockets, é importante manter uma quantidade suficiente de dados pendentes (enviados mas não confirmados ainda) no TCP para alcançar a taxa de transferência mais alta.</span><span class="sxs-lookup"><span data-stu-id="982f2-177">When sending data over a TCP connection using Windows sockets, it is important to keep a sufficient amount of data outstanding (sent but not acknowledged yet) in TCP in order to achieve the highest throughput.</span></span>
<span data-ttu-id="982f2-178">O valor ideal para a quantidade de dados pendentes para atingir a melhor taxa de transferência para a conexão TCP é chamado de tamanho ideal de envio de pendências (ISB).</span><span class="sxs-lookup"><span data-stu-id="982f2-178">The ideal value for the amount of data outstanding to achieve the best throughput for the TCP connection is called the ideal send backlog (ISB) size.</span></span>
<span data-ttu-id="982f2-179">O valor ISB é uma função do produto de atraso de largura de banda da conexão TCP e da janela de recebimento anunciada do receptor (e parcialmente a quantidade de congestionamento na rede).</span><span class="sxs-lookup"><span data-stu-id="982f2-179">The ISB value is a function of the bandwidth-delay product of the TCP connection and the receiver's advertised receive window (and partly the amount of congestion in the network).</span></span>

<span data-ttu-id="982f2-180">O valor do ISB por conexão está disponível na implementação do protocolo TCP no Windows Server 2008, no Windows Vista com SP1 e em versões posteriores do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="982f2-180">The ISB value per connection is available from the TCP protocol implementation in Windows Server 2008, Windows Vista with SP1, and later versions of the operating system.</span></span>
<span data-ttu-id="982f2-181">O IOCTL de **alteração da pendência de envio do sio \_ ideal \_ \_ \_** pode ser usado por um aplicativo para receber uma notificação quando o valor do ISB é alterado dinamicamente para uma conexão.</span><span class="sxs-lookup"><span data-stu-id="982f2-181">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL can be used by an application to get a notification when the ISB value changes dynamically for a connection.</span></span>

<span data-ttu-id="982f2-182">No Windows Server 2008, no Windows Vista com SP1 e em versões posteriores do sistema operacional, a **sio ideal de enviar lista de \_ \_ \_ pendências de envio \_** e sio ideais de envio de consulta da lista de [**\_ \_ \_ pendências \_**](sio-ideal-send-backlog-query.md) têm suporte em soquetes orientados a fluxo que estão em um estado conectado.</span><span class="sxs-lookup"><span data-stu-id="982f2-182">On Windows Server 2008, Windows Vista with SP1, and later versions of the operating system, the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** and [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTLs are supported on stream-oriented sockets that are in a connected state.</span></span>

<span data-ttu-id="982f2-183">Teoricamente, o intervalo para o valor do ISB para uma conexão TCP pode variar de 0 a um máximo de 16 megabytes.</span><span class="sxs-lookup"><span data-stu-id="982f2-183">The range for the ISB value for a TCP connection can theoretically vary from 0 to a maximum of 16 megabytes.</span></span>

<span data-ttu-id="982f2-184">Consulte a página de referência do IOCTL [**sio \_ ideal \_ Enviar \_ \_ consulta de pendência**](sio-ideal-send-backlog-query.md) para uso típico do mecanismo do ISB para obter uma melhor taxa de transferência em conexões de produto com atraso de largura de banda alta.</span><span class="sxs-lookup"><span data-stu-id="982f2-184">See the [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTL reference page for typical usage of the ISB mechanism for achieving better throughput over high bandwidth-delay product connections.</span></span>

<span data-ttu-id="982f2-185">O IOCTL de **\_ alteração da pendência de \_ envio \_ \_ sio ideal** só é permitido em um soquete de fluxo que esteja no estado conectado.</span><span class="sxs-lookup"><span data-stu-id="982f2-185">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is allowed only on a stream socket that is in the connected state.</span></span>
<span data-ttu-id="982f2-186">Caso contrário, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** falhará com **WSAENOTCONN**.</span><span class="sxs-lookup"><span data-stu-id="982f2-186">Otherwise the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function will fail with **WSAENOTCONN**.</span></span>

<span data-ttu-id="982f2-187">O IOCTL de **\_ alteração da pendência de \_ envio \_ \_ sio ideal** não usa buffers de entrada ou saída e pends ou blocos até que uma alteração do ISB ocorra na conexão subjacente.</span><span class="sxs-lookup"><span data-stu-id="982f2-187">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL uses no input or output buffers and pends or blocks until an ISB change occurs on the underlying connection.</span></span>
<span data-ttu-id="982f2-188">Quando esse IOCTL é concluído, um aplicativo Winsock pode usar a [**\_ consulta de \_ \_ pendência \_ de envio sio ideal**](sio-ideal-send-backlog-query.md) para recuperar o novo valor do ISB na conexão.</span><span class="sxs-lookup"><span data-stu-id="982f2-188">When this IOCTL is completed, a Winsock application can use the [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTL to retrieve the new ISB value on the connection.</span></span>

<span data-ttu-id="982f2-189">O IOCTL de **\_ alteração da pendência de \_ envio \_ \_ sio ideal** não dá suporte ao modo sem bloqueio.</span><span class="sxs-lookup"><span data-stu-id="982f2-189">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL does not support non-blocking mode.</span></span>
<span data-ttu-id="982f2-190">Um aplicativo pode emitir esse IOCTL em um soquete sem bloqueio, mas o IOCTL simplesmente bloqueará ou ficará pendente até que o valor do ISB seja alterado.</span><span class="sxs-lookup"><span data-stu-id="982f2-190">An application is allowed to issue this IOCTL on a non-blocking socket, but the IOCTL will simply block or pend until the ISB value changes.</span></span>

<span data-ttu-id="982f2-191">Se os parâmetros *lpOverlapped* e *lpCompletionRoutine* forem nulos, o soquete nessa função será tratado como um soquete não sobreposto.</span><span class="sxs-lookup"><span data-stu-id="982f2-191">If both *lpOverlapped* and *lpCompletionRoutine* parameters are NULL, the socket in this function will be treated as a non-overlapped socket.</span></span>
<span data-ttu-id="982f2-192">Para um soquete não sobreposto, os parâmetros *lpOverlapped* e *lpCompletionRoutine* são ignorados, exceto que a função pode bloquear se o soquete *s* estiver no modo de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="982f2-192">For a non-overlapped socket, *lpOverlapped* and *lpCompletionRoutine* parameters are ignored, except that the function can block if socket *s* is in blocking mode.</span></span>
<span data-ttu-id="982f2-193">Se o soquete *s* estiver no modo sem bloqueio, essa função ainda será bloqueada, pois esse IOCTL específico não oferece suporte ao modo sem bloqueio.</span><span class="sxs-lookup"><span data-stu-id="982f2-193">If socket *s* is in non-blocking mode, this function will still block since this particular IOCTL does not support non-blocking mode.</span></span>

<span data-ttu-id="982f2-194">Para os soquetes sobrepostos, as operações que não podem ser concluídas imediatamente serão iniciadas e a conclusão será indicada mais tarde.</span><span class="sxs-lookup"><span data-stu-id="982f2-194">For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>

<span data-ttu-id="982f2-195">Qualquer IOCTL pode bloquear indefinidamente, dependendo da implementação do provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="982f2-195">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="982f2-196">Se o aplicativo não puder tolerar o bloqueio em uma chamada de função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** , a e/s sobreposta seria ACONSELHAda para os IOCTLs que são especialmente prováveis de bloquear.</span><span class="sxs-lookup"><span data-stu-id="982f2-196">If the application cannot tolerate blocking in a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="982f2-197">O IOCTL de alteração da lista de **\_ \_ \_ pendências \_ de envio sio ideal** fornece uma notificação e é esperado para bloquear ou ficar pendente até que o valor do ISB seja alterado.</span><span class="sxs-lookup"><span data-stu-id="982f2-197">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL provides a notification and is expected to block or pend until the ISB value changes.</span></span>
<span data-ttu-id="982f2-198">Em geral, ele seria chamado de forma assíncrona com o parâmetro *lpOverlapped* definido como uma estrutura WSAOVERLAPPED válida.</span><span class="sxs-lookup"><span data-stu-id="982f2-198">So it would commonly be called asynchronously with the *lpOverlapped* parameter set to a valid WSAOVERLAPPED structure.</span></span>

<span data-ttu-id="982f2-199">O IOCTL de **alteração da pendência de envio do sio \_ ideal \_ \_ \_** pode falhar com a operação **WSAEINTR** ou **WSA \_ \_ anulada** nos seguintes casos:</span><span class="sxs-lookup"><span data-stu-id="982f2-199">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

* <span data-ttu-id="982f2-200">A conexão TCP é desconectada normalmente na direção de envio.</span><span class="sxs-lookup"><span data-stu-id="982f2-200">The TCP connection is gracefully disconnected in the send direction.</span></span> <span data-ttu-id="982f2-201">Isso pode ocorrer como resultado de uma chamada para a função de desligamento com o parâmetro de como definido como **SD \_ Send**, uma chamada para a função **DisconnectEx** ou uma chamada para a função **TransmitFile** ou **TransmitPackets** com o parâmetro *dwFlags* definido como **TF \_ Disconnect** ou **TF \_ reutilization**.</span><span class="sxs-lookup"><span data-stu-id="982f2-201">This can occur as a result of a call to shutdown function with the how parameter set to **SD\_SEND**, a call to the **DisconnectEx** function, or a call to the **TransmitFile** or **TransmitPackets** function with *dwFlags* parameter set to **TF\_DISCONNECT** or **TF\_REUSE**.</span></span>
* <span data-ttu-id="982f2-202">A conexão TCP foi redefinida ou anulada.</span><span class="sxs-lookup"><span data-stu-id="982f2-202">The TCP connection has been reset or aborted.</span></span>
* <span data-ttu-id="982f2-203">O aplicativo emite um **sio \_ ideal \_ Enviar \_ pendências de alteração do registro de \_ alterações** quando já existe uma solicitação de notificação pendente.</span><span class="sxs-lookup"><span data-stu-id="982f2-203">The application issues a **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL when there is already a pended notification request.</span></span> <span data-ttu-id="982f2-204">Somente 1 1 sio pendentes a solicitação de **\_ alteração de pendência de envio do \_ \_ registro posterior \_** é permitida por vez.</span><span class="sxs-lookup"><span data-stu-id="982f2-204">Only one one pended **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** request is allowed at a time.</span></span>
* <span data-ttu-id="982f2-205">A solicitação é cancelada pelo Gerenciador de e/s.</span><span class="sxs-lookup"><span data-stu-id="982f2-205">The request is canceled by the I/O Manager.</span></span>
* <span data-ttu-id="982f2-206">O soquete está fechado.</span><span class="sxs-lookup"><span data-stu-id="982f2-206">The socket is closed.</span></span>

<span data-ttu-id="982f2-207">Duas funções de wrapper embutidas para esses IOCTLs são definidas no arquivo de cabeçalho *Ws2tcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="982f2-207">Two inline wrapper functions for these IOCTLs are defined in the *Ws2tcpip.h* header file.</span></span>
<span data-ttu-id="982f2-208">É recomendável que essas funções embutidas sejam usadas em vez de usar a consulta de **\_ pendência de envio sio ideal \_ \_ \_** e o [**sio \_ ideal \_ Enviar \_ \_ consultas de pendências**](sio-ideal-send-backlog-query.md) para os IOCTLs diretamente.</span><span class="sxs-lookup"><span data-stu-id="982f2-208">It is recommended that these inline functions be used instead of using the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** and [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTLs directly.</span></span>

<span data-ttu-id="982f2-209">A função de wrapper embutido para o **sio \_ ideal \_ Enviar \_ registro da pendência de \_ alteração** do IOCTL é a função **idealsendbacklognotify** .</span><span class="sxs-lookup"><span data-stu-id="982f2-209">The inline wrapper function for the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is the **idealsendbacklognotify** function.</span></span>

<span data-ttu-id="982f2-210">A função de wrapper embutida para a [**consulta de pendência de \_ \_ envio sio \_ \_ ideal**](sio-ideal-send-backlog-query.md) é a função **idealsendbacklogquery** .</span><span class="sxs-lookup"><span data-stu-id="982f2-210">The inline wrapper function for the [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTL is the **idealsendbacklogquery** function.</span></span>

## <a name="see-also"></a><span data-ttu-id="982f2-211">Confira também</span><span class="sxs-lookup"><span data-stu-id="982f2-211">See also</span></span>

[<span data-ttu-id="982f2-212">**SIO_IDEAL_SEND_BACKLOG_QUERY**</span><span class="sxs-lookup"><span data-stu-id="982f2-212">**SIO_IDEAL_SEND_BACKLOG_QUERY**</span></span>](sio-ideal-send-backlog-query.md)

[<span data-ttu-id="982f2-213">**SSA**</span><span class="sxs-lookup"><span data-stu-id="982f2-213">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="982f2-214">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="982f2-214">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="982f2-215">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="982f2-215">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="982f2-216">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="982f2-216">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="982f2-217">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="982f2-217">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="982f2-218">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="982f2-218">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="982f2-219">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="982f2-219">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
