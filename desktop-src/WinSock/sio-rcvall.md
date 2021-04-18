---
description: O código de controle permite que um soquete receba todos os pacotes IPv4 ou IPv6 passando por uma interface de rede.
ms.assetid: 1c198a70-6669-4599-bd9a-ffc26c9fe1d0
title: SIO_RCVALL código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ddff631f1fa4b6b9f9af74f71e2b1eb38a2bf48e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812415"
---
# <a name="sio_rcvall-control-code"></a><span data-ttu-id="14aca-103">SIO_RCVALL código de controle</span><span class="sxs-lookup"><span data-stu-id="14aca-103">SIO_RCVALL Control Code</span></span>

## <a name="description"></a><span data-ttu-id="14aca-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="14aca-104">Description</span></span>
<span data-ttu-id="14aca-105">O código de controle **sio \_ RCVALL** permite que um soquete receba todos os pacotes IPv4 ou IPv6 passando por uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="14aca-105">The **SIO\_RCVALL** control code enables a socket to receive all IPv4 or IPv6 packets passing through a network interface.</span></span>

<span data-ttu-id="14aca-106">Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="14aca-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_RCV_ALL,                       // dwIoControlCode
  NULL,                              // lpvInBuffer0,                                 // cbInBuffer
  NULL,                              // lpvOutBuffer output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_RCV_ALL,                       // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  NULL,                              // lpvOutBuffer output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

## <a name="parameters"></a><span data-ttu-id="14aca-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14aca-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="14aca-108">s</span><span class="sxs-lookup"><span data-stu-id="14aca-108">s</span></span>

<span data-ttu-id="14aca-109">Um descritor que identifica um soquete.</span><span class="sxs-lookup"><span data-stu-id="14aca-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="14aca-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="14aca-110">dwIoControlCode</span></span>

<span data-ttu-id="14aca-111">O código de controle para a operação.</span><span class="sxs-lookup"><span data-stu-id="14aca-111">The control code for the operation.</span></span>
<span data-ttu-id="14aca-112">Use **sio \_ RCVALL** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="14aca-112">Use **SIO\_RCVALL** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="14aca-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="14aca-113">lpvInBuffer</span></span>

<span data-ttu-id="14aca-114">Um ponteiro para o buffer de entrada que deve conter o valor da opção.</span><span class="sxs-lookup"><span data-stu-id="14aca-114">A pointer to the input buffer that should contain the option value.</span></span>
<span data-ttu-id="14aca-115">Os valores possíveis para a opção **sio \_ RCVALL** IOCTL são especificados na enumeração **RCVALL_VALUE** definida no arquivo de cabeçalho *Mstcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="14aca-115">The possible values for the **SIO\_RCVALL** IOCTL option are specified in the **RCVALL_VALUE** enumeration defined in the *Mstcpip.h* header file.</span></span>

<span data-ttu-id="14aca-116">Os valores possíveis para **sio \_ RCVALL** são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="14aca-116">The possible values for **SIO\_RCVALL** are as follows:</span></span>

| <span data-ttu-id="14aca-117">Valor</span><span class="sxs-lookup"><span data-stu-id="14aca-117">Value</span></span> | <span data-ttu-id="14aca-118">Significado</span><span class="sxs-lookup"><span data-stu-id="14aca-118">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="14aca-119">**RCVALL \_ desativado**</span><span class="sxs-lookup"><span data-stu-id="14aca-119">**RCVALL\_OFF**</span></span> | <span data-ttu-id="14aca-120">Desabilite essa opção para que um soquete não receba todos os pacotes IPv4 ou IPv6 passando por uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="14aca-120">Disable this option so a socket does not receive all IPv4 or IPv6 packets passing through a network interface.</span></span> |
| <span data-ttu-id="14aca-121">**RCVALL \_ em**</span><span class="sxs-lookup"><span data-stu-id="14aca-121">**RCVALL\_ON**</span></span> | <span data-ttu-id="14aca-122">Habilite essa opção para que um soquete receba todos os pacotes IPv4 ou IPv6 passando por uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="14aca-122">Enable this option so a socket receives all IPv4 or IPv6 packets passing through a network interface.</span></span> <span data-ttu-id="14aca-123">Essa opção habilita o modo promíscuo na NIC (placa de interface de rede), se a NIC der suporte ao modo promíscuo.</span><span class="sxs-lookup"><span data-stu-id="14aca-123">This option enables promiscuous mode on the network interface card (NIC), if the NIC supports promiscuous mode.</span></span> <span data-ttu-id="14aca-124">Em um segmento de LAN com um hub de rede, uma NIC que dá suporte ao modo promíscuo capturará todo o tráfego IPv4 ou IPv6 na LAN, incluindo o tráfego entre outros computadores no mesmo segmento de LAN.</span><span class="sxs-lookup"><span data-stu-id="14aca-124">On a LAN segment with a network hub, a NIC that supports promiscuous mode will capture all IPv4 or IPv6 traffic on the LAN, including traffic between other computers on the same LAN segment.</span></span> <span data-ttu-id="14aca-125">Todos os pacotes capturados (IPv4 ou IPv6, dependendo do soquete) serão entregues ao soquete bruto.</span><span class="sxs-lookup"><span data-stu-id="14aca-125">All of the captured packets (IPv4 or IPv6, depending on the socket) will be delivered to the raw socket.</span></span> <span data-ttu-id="14aca-126">Essa opção não capturará outros pacotes (ARP, IPX e pacotes NetBEUI, por exemplo) na interface.</span><span class="sxs-lookup"><span data-stu-id="14aca-126">This option will not capture other packets (ARP, IPX, and NetBEUI packets, for example) on the interface.</span></span> <span data-ttu-id="14aca-127">O Netmon usa o mesmo modo para a interface de rede, mas não usa essa opção para capturar o tráfego.</span><span class="sxs-lookup"><span data-stu-id="14aca-127">Netmon uses the same mode for the network interface, but does not use this option to capture traffic.</span></span> |
| <span data-ttu-id="14aca-128">**RCVALL \_ SOCKETLEVELONLY**</span><span class="sxs-lookup"><span data-stu-id="14aca-128">**RCVALL\_SOCKETLEVELONLY**</span></span> | <span data-ttu-id="14aca-129">Este recurso não está implementado no momento; portanto, definir essa opção não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="14aca-129">This feature is not currently implemented, so setting this option does not have any affect.</span></span> |
| <span data-ttu-id="14aca-130">**RCVALL \_ IPLEVEL**</span><span class="sxs-lookup"><span data-stu-id="14aca-130">**RCVALL\_IPLEVEL**</span></span> | <span data-ttu-id="14aca-131">Habilite essa opção para que um soquete IPv4 ou IPv6 receba todos os pacotes no nível de IP passando por uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="14aca-131">Enable this option so an IPv4 or IPv6 socket receives all packets at the IP level passing through a network interface.</span></span> <span data-ttu-id="14aca-132">Essa opção não habilita o modo promíscuo na placa de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="14aca-132">This option does not enable promiscuous mode on the network interface card.</span></span> <span data-ttu-id="14aca-133">Essa opção afeta apenas o processamento de pacotes no nível de IP.</span><span class="sxs-lookup"><span data-stu-id="14aca-133">This option only affects packet processing at the IP level.</span></span> <span data-ttu-id="14aca-134">A NIC ainda recebe apenas os pacotes direcionados para seus endereços unicast e multicast configurados.</span><span class="sxs-lookup"><span data-stu-id="14aca-134">The NIC still receives only packets directed to its configured unicast and multicast addresses.</span></span> <span data-ttu-id="14aca-135">No entanto, um soquete com essa opção habilitada receberá não apenas os pacotes direcionados para endereços IP específicos, mas receberá todos os pacotes IPv4 ou IPv6 recebidos pela NIC.</span><span class="sxs-lookup"><span data-stu-id="14aca-135">However, a socket with this option enabled will receive not only packets directed to specific IP addresses, but will receive all the IPv4 or IPv6 packets the NIC receives.</span></span> <span data-ttu-id="14aca-136">Essa opção não capturará outros pacotes (ARP, IPX e pacotes NetBEUI, por exemplo) recebidos na interface.</span><span class="sxs-lookup"><span data-stu-id="14aca-136">This option will not capture other packets (ARP, IPX, and NetBEUI packets, for example) received on the interface.</span></span> |

### <a name="cbinbuffer"></a><span data-ttu-id="14aca-137">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="14aca-137">cbInBuffer</span></span>

<span data-ttu-id="14aca-138">O tamanho, em bytes, do buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="14aca-138">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="14aca-139">Esse parâmetro deve ser igual ou maior que o tamanho do **RCVALL_VALUE** valor de enumeração apontado pelo parâmetro *lpvInBuffer* .</span><span class="sxs-lookup"><span data-stu-id="14aca-139">This parameter should be equal to or greater than the size of the **RCVALL_VALUE** enumeration value pointed to by the *lpvInBuffer* parameter.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="14aca-140">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="14aca-140">lpvOutBuffer</span></span>

<span data-ttu-id="14aca-141">Um ponteiro para o buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="14aca-141">A pointer to the output buffer.</span></span>
<span data-ttu-id="14aca-142">Este parâmetro não é usado para esta operação.</span><span class="sxs-lookup"><span data-stu-id="14aca-142">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="14aca-143">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="14aca-143">cbOutBuffer</span></span>

<span data-ttu-id="14aca-144">O tamanho, em bytes, do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="14aca-144">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="14aca-145">Este parâmetro não é usado para esta operação.</span><span class="sxs-lookup"><span data-stu-id="14aca-145">This parameter is unused for this operation.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="14aca-146">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="14aca-146">lpcbBytesReturned</span></span>

<span data-ttu-id="14aca-147">Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="14aca-147">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>
<span data-ttu-id="14aca-148">Este parâmetro não é usado para esta operação.</span><span class="sxs-lookup"><span data-stu-id="14aca-148">This parameter is unused for this operation.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="14aca-149">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="14aca-149">lpvOverlapped</span></span>

<span data-ttu-id="14aca-150">Um ponteiro para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="14aca-150">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="14aca-151">Se o soquete *s* foi criado sem o atributo sobreposto, o parâmetro *lpOverlapped* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="14aca-151">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="14aca-152">Se *s* foi aberto com o atributo Overlapped e o parâmetro *LpOverlapped* não for **nulo**, a operação será executada como uma operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="14aca-152">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="14aca-153">Nesse caso, o parâmetro *lpOverlapped* deve apontar para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="14aca-153">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="14aca-154">Para operações sobrepostas, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retorna imediatamente, e o método de conclusão apropriado é sinalizado quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="14aca-154">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="14aca-155">Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.</span><span class="sxs-lookup"><span data-stu-id="14aca-155">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="14aca-156">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="14aca-156">lpCompletionRoutine</span></span>

<span data-ttu-id="14aca-157">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="14aca-157">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="14aca-158">Um ponteiro para a rotina de conclusão chamada quando a operação foi concluída (ignorada para soquetes não sobrepostos).</span><span class="sxs-lookup"><span data-stu-id="14aca-158">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="14aca-159">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="14aca-159">lpThreadId</span></span>

<span data-ttu-id="14aca-160">Um ponteiro para uma estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a ser usado pelo provedor em uma chamada subsequente para [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="14aca-160">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="14aca-161">O provedor deve armazenar a estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) referenciada (não o ponteiro para o mesmo) até que a função [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) seja retornada.</span><span class="sxs-lookup"><span data-stu-id="14aca-161">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="14aca-162">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="14aca-162">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="14aca-163">lpErrno</span><span class="sxs-lookup"><span data-stu-id="14aca-163">lpErrno</span></span>

<span data-ttu-id="14aca-164">Um ponteiro para o código de erro.</span><span class="sxs-lookup"><span data-stu-id="14aca-164">A pointer to the error code.</span></span>

<span data-ttu-id="14aca-165">**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="14aca-165">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="14aca-166">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="14aca-166">Return value</span></span>

<span data-ttu-id="14aca-167">Se a operação for concluída com êxito, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará zero.</span><span class="sxs-lookup"><span data-stu-id="14aca-167">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="14aca-168">Se a operação falhar ou estiver pendente, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará **um \_ erro de soquete**.</span><span class="sxs-lookup"><span data-stu-id="14aca-168">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="14aca-169">Para obter informações de erro estendidas, chame [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="14aca-169">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="14aca-170">Código do erro</span><span class="sxs-lookup"><span data-stu-id="14aca-170">Error code</span></span> | <span data-ttu-id="14aca-171">Significado</span><span class="sxs-lookup"><span data-stu-id="14aca-171">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="14aca-172">**\_e/s de WSA \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="14aca-172">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="14aca-173">Uma operação sobreposta foi iniciada com êxito e a conclusão será indicada em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="14aca-173">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="14aca-174">**operação de WSA \_ \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="14aca-174">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="14aca-175">Uma operação sobreposta foi cancelada devido ao fechamento do soquete ou à execução do comando **SIO_FLUSH** IOCTL.</span><span class="sxs-lookup"><span data-stu-id="14aca-175">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="14aca-176">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="14aca-176">**WSAEFAULT**</span></span> | <span data-ttu-id="14aca-177">O parâmetro *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço do usuário.</span><span class="sxs-lookup"><span data-stu-id="14aca-177">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="14aca-178">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="14aca-178">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="14aca-179">A função é invocada quando um retorno de chamada está em andamento.</span><span class="sxs-lookup"><span data-stu-id="14aca-179">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="14aca-180">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="14aca-180">**WSAEINTR**</span></span> | <span data-ttu-id="14aca-181">Uma operação de bloqueio foi interrompida.</span><span class="sxs-lookup"><span data-stu-id="14aca-181">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="14aca-182">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="14aca-182">**WSAEINVAL**</span></span> | <span data-ttu-id="14aca-183">O parâmetro *dwIoControlCode* não é um comando válido ou um parâmetro de entrada especificado não é aceitável ou o comando não é aplicável ao tipo de soquete especificado.</span><span class="sxs-lookup"><span data-stu-id="14aca-183">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="14aca-184">Esse erro também será retornado se o parâmetro *cbInBuffer* for menor que o `sizeof(UCHAR)` ou o parâmetro *lpvInBuffer* apontar para um valor que não seja um **RCVALL_VALUE** valor de enumeração.</span><span class="sxs-lookup"><span data-stu-id="14aca-184">This error is also returned if the *cbInBuffer* parameter is less than the `sizeof(UCHAR)` or the *lpvInBuffer* parameter points to value that is not a **RCVALL_VALUE** enumeration value.</span></span> <span data-ttu-id="14aca-185">Esse erro também pode ser retornado se a interface de rede associada ao soquete não puder ser encontrada.</span><span class="sxs-lookup"><span data-stu-id="14aca-185">This error can also be returned if the network interface associated with the socket cannot be found.</span></span> <span data-ttu-id="14aca-186">Isso pode ocorrer se a interface de rede associada ao soquete for excluída ou removida (um dispositivo de rede PCMCIA ou USB de remoção, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="14aca-186">This could occur if the network interface associated with the socket is deleted or removed (a remove PCMCIA or USB network device, for example).</span></span> |
| <span data-ttu-id="14aca-187">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="14aca-187">**WSAENETDOWN**</span></span> | <span data-ttu-id="14aca-188">Falha no subsistema de rede.</span><span class="sxs-lookup"><span data-stu-id="14aca-188">The network subsystem has failed.</span></span> |
| <span data-ttu-id="14aca-189">**WSAENOBUFS**</span><span class="sxs-lookup"><span data-stu-id="14aca-189">**WSAENOBUFS**</span></span> | <span data-ttu-id="14aca-190">Não há espaço disponível no buffer.</span><span class="sxs-lookup"><span data-stu-id="14aca-190">No buffer space available.</span></span> |
| <span data-ttu-id="14aca-191">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="14aca-191">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="14aca-192">Não há suporte para a opção de soquete no protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="14aca-192">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="14aca-193">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="14aca-193">**WSAENOTSOCK**</span></span> | <span data-ttu-id="14aca-194">O descritor *s* não é um soquete.</span><span class="sxs-lookup"><span data-stu-id="14aca-194">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="14aca-195">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="14aca-195">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="14aca-196">Não há suporte para o comando IOCTL especificado.</span><span class="sxs-lookup"><span data-stu-id="14aca-196">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="14aca-197">Esse erro será retornado se o **sio \_ RCVALL** IOCTL não tiver suporte do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="14aca-197">This error is returned if the **SIO\_RCVALL** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="14aca-198">Comentários</span><span class="sxs-lookup"><span data-stu-id="14aca-198">Remarks</span></span>

<span data-ttu-id="14aca-199">O **sio \_ RCVALL** IOCTL tem suporte no Windows 2000 e em versões posteriores do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="14aca-199">The **SIO\_RCVALL** IOCTL is supported on Windows 2000 and later versions of the operating system.</span></span>

<span data-ttu-id="14aca-200">O IOCTL **sio \_ RCVALL** permite que um soquete receba todos os pacotes IPv4 ou IPv6 em uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="14aca-200">The **SIO\_RCVALL** IOCTL enables a socket to receive all IPv4 or IPv6 packets on a network interface.</span></span>
<span data-ttu-id="14aca-201">O identificador de soquete passado para a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** deve ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="14aca-201">The socket handle passed to the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function must be one of the following:</span></span>

* <span data-ttu-id="14aca-202">Um soquete IPv4 que foi criado com a família de endereços definida como AF_INET, o tipo de soquete definido como SOCK_RAW e o protocolo definido como IPPROTO_IP.</span><span class="sxs-lookup"><span data-stu-id="14aca-202">An IPv4 socket that was created with the address family set to AF_INET, the socket type set to SOCK_RAW, and the protocol set to IPPROTO_IP.</span></span>
* <span data-ttu-id="14aca-203">Um soquete IPv6 que foi criado com a família de endereços definida como AF_INET6, o tipo de soquete definido como SOCK_RAW e o protocolo definido como IPPROTO_IPV6.</span><span class="sxs-lookup"><span data-stu-id="14aca-203">An IPv6 socket that was created with the address family set to AF_INET6, the socket type set to SOCK_RAW, and the protocol set to IPPROTO_IPV6.</span></span>

<span data-ttu-id="14aca-204">Para obter mais informações sobre soquetes brutos, consulte [**soquetes brutos TCP/IP**](/windows/desktop/winsock/tcp-ip-raw-sockets-2).</span><span class="sxs-lookup"><span data-stu-id="14aca-204">For more information on raw sockets, see [**TCP/IP Raw Sockets**](/windows/desktop/winsock/tcp-ip-raw-sockets-2).</span></span>

<span data-ttu-id="14aca-205">O soquete também deve estar associado a uma interface IPv4 ou IPv6 local explícita, o que significa que você não pode fazer a ligação com **\_ qualquer endereço** ou **in6addr \_**.</span><span class="sxs-lookup"><span data-stu-id="14aca-205">The socket also must be bound to an explicit local IPv4 or IPv6 interface, which means that you cannot bind to **INADDR\_ANY** or **in6addr\_any**.</span></span>

<span data-ttu-id="14aca-206">Depois que o soquete é associado e o IOCTL é concluído com êxito, as chamadas para as funções [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv) ou [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) retornam datagrams IPv4 que passam pela interface IPv4 fornecida ou retornam datagrams IPv6 passando pela interface IPv6 fornecida.</span><span class="sxs-lookup"><span data-stu-id="14aca-206">Once the socket is bound and the IOCTL completes successfully, calls to the [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv) or [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) functions return IPv4 datagrams passing through the given IPv4 interface or return IPv6 datagrams passing through the given IPv6 interface.</span></span>
<span data-ttu-id="14aca-207">Observe que você deve fornecer um buffer suficientemente grande.</span><span class="sxs-lookup"><span data-stu-id="14aca-207">Note that you must supply a sufficiently large buffer.</span></span>
<span data-ttu-id="14aca-208">Definir esse IOCTL só capturará pacotes IPv4 ou IPv6 em uma determinada interface.</span><span class="sxs-lookup"><span data-stu-id="14aca-208">Setting this IOCTL will only capture IPv4 or IPv6 packets on a given interface.</span></span>
<span data-ttu-id="14aca-209">Esse IOCTL não capturará outros pacotes (ARP, IPX e pacotes NetBEUI, por exemplo) na interface.</span><span class="sxs-lookup"><span data-stu-id="14aca-209">This IOCTL will not capture other packets (ARP, IPX, and NetBEUI packets, for example) on the interface.</span></span>

<span data-ttu-id="14aca-210">Um soquete associado a uma interface local específica com o IOCTL **sio \_ RCVALL** receberá apenas os pacotes que passam pela interface.</span><span class="sxs-lookup"><span data-stu-id="14aca-210">A socket bound to a specific local interface with the **SIO\_RCVALL** IOCTL will receive only packets passing through that interface.</span></span>
<span data-ttu-id="14aca-211">Ele não receberá pacotes recebidos em outra interface e será encaminhado em outra interface diferente do soquete associado com **sio \_ RCVALL** IOCTL.</span><span class="sxs-lookup"><span data-stu-id="14aca-211">It will not receive packets received on another interface and getting forwarded out on another interface different from the socket bound with **SIO\_RCVALL** IOCTL.</span></span>

<span data-ttu-id="14aca-212">No Windows Server 2008 e versões anteriores, a configuração de IOCTL **sio \_ RCVALL** não capturaria pacotes locais enviados de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="14aca-212">On Windows Server 2008 and earlier, the **SIO\_RCVALL** IOCTL setting would not capture local packets sent out of a network interface.</span></span>
<span data-ttu-id="14aca-213">Isso incluiu os pacotes recebidos em outra interface e encaminhou a interface de rede especificada para o **sio \_ RCVALL** IOCTL.</span><span class="sxs-lookup"><span data-stu-id="14aca-213">This included packets received on another interface and forwarded out the network interface specified for the **SIO\_RCVALL** IOCTL.</span></span>

<span data-ttu-id="14aca-214">No Windows 7 e no Windows Server 2008 R2, isso foi alterado para que os pacotes locais enviados de uma interface de rede também sejam capturados.</span><span class="sxs-lookup"><span data-stu-id="14aca-214">On Windows 7 and Windows Server 2008 R2 , this was changed so that local packets sent out of a network interface are also captured.</span></span>
<span data-ttu-id="14aca-215">Isso inclui os pacotes recebidos em outra interface e, em seguida, encaminhado o adaptador de rede associado ao soquete com **sio \_ RCVALL** IOCTL.</span><span class="sxs-lookup"><span data-stu-id="14aca-215">This includes packets received on another interface and then forwarded out the network interface bound to the socket with **SIO\_RCVALL** IOCTL.</span></span>

<span data-ttu-id="14aca-216">Definir esse IOCTL requer privilégio de administrador no computador local.</span><span class="sxs-lookup"><span data-stu-id="14aca-216">Setting this IOCTL requires Administrator privilege on the local computer.</span></span>

<span data-ttu-id="14aca-217">Esse recurso é, às vezes, chamado de modo promíscuo.</span><span class="sxs-lookup"><span data-stu-id="14aca-217">This feature is sometimes referred to as promiscuous mode.</span></span>
<span data-ttu-id="14aca-218">Qualquer alteração direta da aplicação dessa opção em uma interface e, em seguida, a outra interface com uma única chamada usando esse IOCTL não é suportada.</span><span class="sxs-lookup"><span data-stu-id="14aca-218">Any direct change from applying this option on one interface and then to another interface with a single call using this IOCTL is not supported.</span></span>
<span data-ttu-id="14aca-219">Um aplicativo deve primeiro usar este IOCTL para desativar o comportamento na primeira interface e, em seguida, usar este IOCTL para habilitar o comportamento em uma nova interface.</span><span class="sxs-lookup"><span data-stu-id="14aca-219">An application must first use this IOCTL to turn off the behavior on the first interface, and then use this IOCTL to enable the behavior on a new interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="14aca-220">Confira também</span><span class="sxs-lookup"><span data-stu-id="14aca-220">See also</span></span>

[<span data-ttu-id="14aca-221">**SSA**</span><span class="sxs-lookup"><span data-stu-id="14aca-221">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="14aca-222">**Soquetes brutos TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="14aca-222">**TCP/IP Raw Sockets**</span></span>](/windows/desktop/winsock/tcp-ip-raw-sockets-2)

[<span data-ttu-id="14aca-223">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="14aca-223">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="14aca-224">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="14aca-224">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="14aca-225">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="14aca-225">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="14aca-226">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="14aca-226">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="14aca-227">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="14aca-227">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="14aca-228">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="14aca-228">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
