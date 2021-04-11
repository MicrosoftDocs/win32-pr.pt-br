---
description: Permite que um aplicativo habilite ou desabilite o retorno de informações de pacote pela função WSARecvMsg em um soquete IPv4.
ms.assetid: C6246899-0220-4F88-B43B-CED1B1FF7DC3
title: Opção de soquete IP_PKTINFO (Ws2ipdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2134b31ead9efeb032b4ed72fcaedcd4cc9f67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296347"
---
# <a name="ip_pktinfo-socket-option"></a><span data-ttu-id="63c20-103">\_Opção de soquete IP PKTINFO</span><span class="sxs-lookup"><span data-stu-id="63c20-103">IP\_PKTINFO socket option</span></span>

<span data-ttu-id="63c20-104">A \_ opção IP PKTINFO Socket permite que um aplicativo habilite ou desabilite o retorno das informações de pacote pela função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) em um soquete IPv4.</span><span class="sxs-lookup"><span data-stu-id="63c20-104">The IP\_PKTINFO socket option allows an application to enable or disable the return of packet information by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function on an IPv4 socket..</span></span>

<span data-ttu-id="63c20-105">Para consultar o status dessa opção de soquete, chame a função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) .</span><span class="sxs-lookup"><span data-stu-id="63c20-105">To query the status of this socket option, call the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function.</span></span> <span data-ttu-id="63c20-106">Para definir essa opção, chame a função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="63c20-106">To set this option, call the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function with the following parameters.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="63c20-107">Valor da opção de soquete</span><span class="sxs-lookup"><span data-stu-id="63c20-107">Socket option value</span></span>

<span data-ttu-id="63c20-108">A constante que representa essa opção de soquete é 19.</span><span class="sxs-lookup"><span data-stu-id="63c20-108">The constant that represents this socket option is 19.</span></span>

## <a name="syntax"></a><span data-ttu-id="63c20-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63c20-109">Syntax</span></span>


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IP,   // level
  (int) IP_PKTINFO, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IP,   // level
  (int) IP_PKTINFO, // optname
  (char *) optval, // input buffer,
  (int) optlen,  // size of input buffer
);
```



## <a name="parameters"></a><span data-ttu-id="63c20-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63c20-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63c20-111">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="63c20-111">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63c20-112">Um descritor que identifica o soquete.</span><span class="sxs-lookup"><span data-stu-id="63c20-112">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="63c20-113">*nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="63c20-113">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63c20-114">O nível no qual a opção é definida.</span><span class="sxs-lookup"><span data-stu-id="63c20-114">The level at which the option is defined.</span></span> <span data-ttu-id="63c20-115">Use **o \_ IP IPPROTO** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="63c20-115">Use **IPPROTO\_IP** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="63c20-116">*OptName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63c20-116">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63c20-117">A opção de soquete para obter ou definir o valor.</span><span class="sxs-lookup"><span data-stu-id="63c20-117">The socket option for which to get or set the value.</span></span> <span data-ttu-id="63c20-118">Use \_ PKTINFO IP para esta operação.</span><span class="sxs-lookup"><span data-stu-id="63c20-118">Use IP\_PKTINFO for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="63c20-119">*optval* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="63c20-119">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63c20-120">Um ponteiro para o buffer que contém o valor da opção a ser definida.</span><span class="sxs-lookup"><span data-stu-id="63c20-120">A pointer to the buffer containing the value for the option to set.</span></span> <span data-ttu-id="63c20-121">Esse parâmetro deve apontar para o buffer igual ou maior que o tamanho de um valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="63c20-121">This parameter should point to buffer equal to or larger than the size of a **DWORD** value.</span></span>

<span data-ttu-id="63c20-122">Esse valor é tratado como um valor booliano com 0 usado para indicar **falso** (desabilitado) e um valor diferente de zero para indicar **verdadeiro** (habilitado).</span><span class="sxs-lookup"><span data-stu-id="63c20-122">This value is treated as a boolean value with 0 used to indicate **FALSE** (disabled) and a nonzero value to indicate **TRUE** (enabled).</span></span>

</dd> <dt>

<span data-ttu-id="63c20-123">*optlen* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="63c20-123">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="63c20-124">Um ponteiro para o tamanho, em bytes, do buffer *optval* .</span><span class="sxs-lookup"><span data-stu-id="63c20-124">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="63c20-125">Esse tamanho deve ser igual ou maior que o tamanho de um valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="63c20-125">This size must be equal to or larger than the size of a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63c20-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="63c20-126">Return value</span></span>

<span data-ttu-id="63c20-127">Se a operação for concluída com êxito, a função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) ou [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) retornará zero.</span><span class="sxs-lookup"><span data-stu-id="63c20-127">If the operation completes successfully, the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) or [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function returns zero.</span></span>

<span data-ttu-id="63c20-128">Se a operação falhar, um valor de erro de soquete \_ será retornado e um código de erro específico poderá ser recuperado chamando [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="63c20-128">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="63c20-129">Código do erro</span><span class="sxs-lookup"><span data-stu-id="63c20-129">Error code</span></span>                                                                                                                                              | <span data-ttu-id="63c20-130">Significado</span><span class="sxs-lookup"><span data-stu-id="63c20-130">Meaning</span></span>                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="63c20-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="63c20-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="63c20-132">Uma chamada [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) bem-sucedida deve ocorrer antes de usar essa função.</span><span class="sxs-lookup"><span data-stu-id="63c20-132">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="63c20-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="63c20-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="63c20-134">Falha no subsistema de rede.</span><span class="sxs-lookup"><span data-stu-id="63c20-134">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="63c20-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="63c20-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="63c20-136">Um dos parâmetros *optval* ou *optlen* aponta para a memória que não está em uma parte válida do espaço de endereço de usuário.</span><span class="sxs-lookup"><span data-stu-id="63c20-136">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="63c20-137">Esse erro também será retornado se o valor apontado pelo parâmetro *optlen* for menor que o tamanho de um valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="63c20-137">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a **DWORD** value.</span></span><br/> |
| <dl> <span data-ttu-id="63c20-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="63c20-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="63c20-139">Uma chamada de bloqueio do Windows Sockets 1,1 está em andamento ou o provedor de serviços ainda está processando uma função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="63c20-139">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="63c20-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="63c20-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="63c20-141">Foi fornecido um argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="63c20-141">An invalid argument was supplied.</span></span> <span data-ttu-id="63c20-142">Esse erro será retornado se o parâmetro de *nível* for desconhecido ou inválido.</span><span class="sxs-lookup"><span data-stu-id="63c20-142">This error is returned if the *level* parameter is unknown or invalid.</span></span> <span data-ttu-id="63c20-143">No Windows Vista e posterior, esse erro também será retornado se o soquete estava em um estado de transição.</span><span class="sxs-lookup"><span data-stu-id="63c20-143">On Windows Vista and later, this error is also returned if the socket was in a transitional state.</span></span><br/>                                     |
| <dl> <span data-ttu-id="63c20-144"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="63c20-144"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="63c20-145">A opção é desconhecida ou não é suportada pela família de protocolos indicada.</span><span class="sxs-lookup"><span data-stu-id="63c20-145">The option is unknown or unsupported by the indicated protocol family.</span></span> <span data-ttu-id="63c20-146">Esse erro será retornado se o parâmetro de *tipo* para o descritor de soquete passado no parâmetro *s* não tiver sido **Sock \_ DGRAM** ou **Sock \_ RAW**.</span><span class="sxs-lookup"><span data-stu-id="63c20-146">This error is returned if the *type* parameter for the socket descriptor passed in the *s* parameter was not **SOCK\_DGRAM** or **SOCK\_RAW**.</span></span> <br/>                          |
| <dl> <span data-ttu-id="63c20-147"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="63c20-147"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="63c20-148">O descritor não é um soquete.</span><span class="sxs-lookup"><span data-stu-id="63c20-148">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="63c20-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="63c20-149">Remarks</span></span>

<span data-ttu-id="63c20-150">A função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) chamada com a opção de soquete de PKTINFO de IP \_ permite que um aplicativo determine se as informações de pacote serão retornadas pela função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)para um soquete IPv4.</span><span class="sxs-lookup"><span data-stu-id="63c20-150">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the IP\_PKTINFO socket option allows an application to determine if packet information is to be returned by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)function for an IPv4 socket.</span></span>

<span data-ttu-id="63c20-151">A função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) chamada com a \_ opção de soquete de PKTINFO de IP permite que um aplicativo habilite ou desabilite o retorno de informações de pacote pela função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) .</span><span class="sxs-lookup"><span data-stu-id="63c20-151">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function called with the IP\_PKTINFO socket option allows an application to enable or disable the return of packet information by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function.</span></span> <span data-ttu-id="63c20-152">A \_ opção de PKTINFO de IP para um soquete é desabilitada (definida como **false**) por padrão.</span><span class="sxs-lookup"><span data-stu-id="63c20-152">The IP\_PKTINFO option for a socket is disabled (set to **FALSE**) by default.</span></span>

<span data-ttu-id="63c20-153">Quando essa opção de soquete é habilitada em um soquete IPv4 do tipo **Sock \_ DGRAM** ou **Sock \_ RAW**, a função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) retorna informações de pacote na estrutura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) apontada pelo parâmetro *lpMsg* .</span><span class="sxs-lookup"><span data-stu-id="63c20-153">When this socket option is enabled on an IPv4 socket of type **SOCK\_DGRAM** or **SOCK\_RAW**, the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function returns packet information in the [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure pointed to by the *lpMsg* parameter.</span></span> <span data-ttu-id="63c20-154">Um dos objetos de dados de controle na estrutura **WSAMSG** retornada conterá uma estrutura [**in \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) usada para armazenar informações de endereço de pacote recebido.</span><span class="sxs-lookup"><span data-stu-id="63c20-154">One of the control data objects in the returned **WSAMSG** structure will contain an [**in\_pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) structure used to store received packet address information.</span></span>

<span data-ttu-id="63c20-155">Para datagrams recebidos pela função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) sobre IPv4, o membro **Control** da estrutura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) recebido conterá uma estrutura [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) que contém uma estrutura **WSACMSGHDR** .</span><span class="sxs-lookup"><span data-stu-id="63c20-155">For datagrams received by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function over IPv4, the **Control** member of the [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure received will contain a [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) structure that contains a **WSACMSGHDR** structure.</span></span> <span data-ttu-id="63c20-156">O membro de **\_ nível CMsg** dessa estrutura **WSACMSGHDR** conteria **o \_ IP IPPROTO**, o membro de **\_ tipo CMsg** dessa estrutura conteria o **IP \_ PKTINFO** e o membro de **\_ dados CMsg** conteria uma estrutura [**in \_ PKTINFO**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) usada para armazenar informações de endereço de pacote IPv4 recebido.</span><span class="sxs-lookup"><span data-stu-id="63c20-156">The **cmsg\_level** member of this **WSACMSGHDR** structure would contain **IPPROTO\_IP**, the **cmsg\_type** member of this structure would contain **IP\_PKTINFO**, and the **cmsg\_data** member would contain an [**in\_pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) structure used to store received IPv4 packet address information.</span></span> <span data-ttu-id="63c20-157">O endereço IPv4 na estrutura **\_ pktinfo** é o endereço IPv4 do qual o pacote foi recebido.</span><span class="sxs-lookup"><span data-stu-id="63c20-157">The IPv4 address in the **in\_pktinfo** structure is the IPv4 address from which the packet was received.</span></span>

<span data-ttu-id="63c20-158">Para um soquete de datagrama de pilha dupla, se um aplicativo exigir que a função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) retorne informações de pacote em uma estrutura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) para datagramas recebidos por IPv4, \_ a opção IP PKTINFO Socket deverá ser definida como true no soquete.</span><span class="sxs-lookup"><span data-stu-id="63c20-158">For a dual-stack datagram socket, if an application requires the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function to return packet information in a [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure for datagrams received over IPv4, then IP\_PKTINFO socket option must be set to true on the socket.</span></span> <span data-ttu-id="63c20-159">Se apenas a [opção \_ PKTINFO IPv6](ipv6-pktinfo.md) for definida como true no soquete, as informações de pacote serão fornecidas para datagramas recebidos via IPv6, mas podem não ser fornecidas para datagramas recebidos via IPv4.</span><span class="sxs-lookup"><span data-stu-id="63c20-159">If only the [IPV6\_PKTINFO](ipv6-pktinfo.md) option is set to true on the socket, packet information will be provided for datagrams received over IPv6 but may not be provided for datagrams received over IPv4.</span></span>

<span data-ttu-id="63c20-160">Se um aplicativo tentar definir a opção de \_ soquete de IP PKTINFO em um soquete de datastack de pilha dupla e o IPv4 estiver desabilitado no sistema, a função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) falhará e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará com um erro de [WSAEINVAL](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="63c20-160">If an application tries to set the IP\_PKTINFO socket option on a dual-stack datagram socket and IPv4 is disabled on the system, then the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function will fail and [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) will return with an error of [WSAEINVAL](windows-sockets-error-codes-2.md).</span></span> <span data-ttu-id="63c20-161">Esse mesmo erro também é retornado pela função **setsockopt** como resultado de outros erros.</span><span class="sxs-lookup"><span data-stu-id="63c20-161">This same error is also returned by the **setsockopt** function as a result of other errors.</span></span> <span data-ttu-id="63c20-162">Se um aplicativo tentar definir uma opção de \_ soquete de nível de IP IPPROTO em um soquete de pilha dupla e falhar com [WSAEINVAL](windows-sockets-error-codes-2.md), o aplicativo deverá determinar se o IPv4 está desabilitado no computador local.</span><span class="sxs-lookup"><span data-stu-id="63c20-162">If an application tries to set an IPPROTO\_IP level socket option on a dual-stack socket and it fails with [WSAEINVAL](windows-sockets-error-codes-2.md), then the application should determine if IPv4 is disabled on the local computer.</span></span> <span data-ttu-id="63c20-163">Um método que pode ser usado para detectar se o IPv4 está habilitado ou desabilitado é chamar a função de [**soquete**](/windows/desktop/api/Winsock2/nf-winsock2-socket) com o parâmetro *AF* definido como série AF para \_ tentar criar um soquete IPv4.</span><span class="sxs-lookup"><span data-stu-id="63c20-163">One method that can be used to detect if IPv4 is enabled or disabled is to call the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function with the *af* parameter set to AF\_INET to try and create an IPv4 socket.</span></span> <span data-ttu-id="63c20-164">Se a função **Socket** falhar e **WSAGetLastError** retornar um erro de [WSAEAFNOSUPPORT](windows-sockets-error-codes-2.md), isso significará que o IPv4 não está habilitado.</span><span class="sxs-lookup"><span data-stu-id="63c20-164">If the **socket** function fails and **WSAGetLastError** returns an error of [WSAEAFNOSUPPORT](windows-sockets-error-codes-2.md), then it means IPv4 is not enabled.</span></span> <span data-ttu-id="63c20-165">Nesse caso, uma falha de função **setsockopt** ao tentar definir a opção de soquete de PKTINFO de IP \_ pode ser ignorada pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="63c20-165">In this case, a **setsockopt** function failure when attempting to set the IP\_PKTINFO socket option can be ignored by the application.</span></span> <span data-ttu-id="63c20-166">Caso contrário, uma falha ao tentar definir a \_ opção de soquete IP PKTINFO deve ser tratada como um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="63c20-166">Otherwise a failure when attempting to set the IP\_PKTINFO socket option should be treated as an unexpected error.</span></span>

<span data-ttu-id="63c20-167">Observe que o arquivo de cabeçalho *Ws2ipdef. h* é incluído automaticamente em *Ws2tcpip. h* e nunca deve ser usado diretamente.</span><span class="sxs-lookup"><span data-stu-id="63c20-167">Note that the *Ws2ipdef.h* header file is automatically included in *Ws2tcpip.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="63c20-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63c20-168">Requirements</span></span>



| <span data-ttu-id="63c20-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="63c20-169">Requirement</span></span> | <span data-ttu-id="63c20-170">Valor</span><span class="sxs-lookup"><span data-stu-id="63c20-170">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63c20-171">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63c20-171">Minimum supported client</span></span><br/> | <span data-ttu-id="63c20-172">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="63c20-172">Windows XP \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="63c20-173">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63c20-173">Minimum supported server</span></span><br/> | <span data-ttu-id="63c20-174">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="63c20-174">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="63c20-175">parâmetro</span><span class="sxs-lookup"><span data-stu-id="63c20-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="63c20-176"><dt>Ws2ipdef. h (incluir Ws2tcpip. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63c20-176"><dt>Ws2ipdef.h (include Ws2tcpip.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63c20-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="63c20-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63c20-178">Soquetes de pilha dupla</span><span class="sxs-lookup"><span data-stu-id="63c20-178">Dual-Stack Sockets</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="63c20-179">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="63c20-179">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="63c20-180">**em \_ pktinfo**</span><span class="sxs-lookup"><span data-stu-id="63c20-180">**in\_pktinfo**</span></span>](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo)
</dt> <dt>

[<span data-ttu-id="63c20-181">**\_Opções de soquete de IP IPPROTO**</span><span class="sxs-lookup"><span data-stu-id="63c20-181">**IPPROTO\_IP Socket Options**</span></span>](ipproto-ip-socket-options.md)
</dt> <dt>

[<span data-ttu-id="63c20-182">\_PKTINFO IPv6</span><span class="sxs-lookup"><span data-stu-id="63c20-182">IPV6\_PKTINFO</span></span>](ipv6-pktinfo.md)
</dt> <dt>

[<span data-ttu-id="63c20-183">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="63c20-183">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[<span data-ttu-id="63c20-184">**SSA**</span><span class="sxs-lookup"><span data-stu-id="63c20-184">**socket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[<span data-ttu-id="63c20-185">**WSAMSG**</span><span class="sxs-lookup"><span data-stu-id="63c20-185">**WSAMSG**</span></span>](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)
</dt> <dt>

[<span data-ttu-id="63c20-186">**LPFN_WSARECVMSG (WSARecvMsg)**</span><span class="sxs-lookup"><span data-stu-id="63c20-186">**LPFN_WSARECVMSG (WSARecvMsg)**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> </dl>

 

 
