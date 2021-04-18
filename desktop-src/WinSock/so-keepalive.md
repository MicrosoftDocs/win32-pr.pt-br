---
description: Foi projetado para permitir que um aplicativo habilite pacotes Keep-Alive para uma conexão de soquete.
ms.assetid: d6da7761-7a09-4c91-9737-550590a773b3
title: Opção de soquete SO_KEEPALIVE (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d829f957e23c48a325444de7d992397fba26d48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760615"
---
# <a name="so_keepalive-socket-option"></a><span data-ttu-id="82ff8-103">\_Opção de soquete KeepAlive</span><span class="sxs-lookup"><span data-stu-id="82ff8-103">SO\_KEEPALIVE socket option</span></span>

<span data-ttu-id="82ff8-104">A opção de soquete **\_ KeepAlive** é projetada para permitir que um aplicativo habilite pacotes Keep-Alive para uma conexão de soquete.</span><span class="sxs-lookup"><span data-stu-id="82ff8-104">The **SO\_KEEPALIVE** socket option is designed to allow an application to enable keep-alive packets for a socket connection.</span></span>

<span data-ttu-id="82ff8-105">Para consultar o status dessa opção de soquete, chame a função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) .</span><span class="sxs-lookup"><span data-stu-id="82ff8-105">To query the status of this socket option, call the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function.</span></span> <span data-ttu-id="82ff8-106">Para definir essa opção, chame a função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="82ff8-106">To set this option, call the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function with the following parameters.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="82ff8-107">Valor da opção de soquete</span><span class="sxs-lookup"><span data-stu-id="82ff8-107">Socket option value</span></span>

<span data-ttu-id="82ff8-108">A constante que representa essa opção de soquete é 0x0008.</span><span class="sxs-lookup"><span data-stu-id="82ff8-108">The constant that represents this socket option is 0x0008.</span></span>

## <a name="syntax"></a><span data-ttu-id="82ff8-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82ff8-109">Syntax</span></span>


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_KEEPALIVE, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_KEEPALIVE, // optname
  (char *) optval, // input buffer,
  (int) optlen,  // size of input buffer
);
```



## <a name="parameters"></a><span data-ttu-id="82ff8-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82ff8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82ff8-111">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="82ff8-111">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82ff8-112">Um descritor que identifica o soquete.</span><span class="sxs-lookup"><span data-stu-id="82ff8-112">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="82ff8-113">*nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="82ff8-113">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82ff8-114">O nível no qual a opção é definida.</span><span class="sxs-lookup"><span data-stu-id="82ff8-114">The level at which the option is defined.</span></span> <span data-ttu-id="82ff8-115">Use **o \_ soquete sol** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="82ff8-115">Use **SOL\_SOCKET** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="82ff8-116">*OptName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="82ff8-116">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82ff8-117">A opção de soquete para a qual o valor deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="82ff8-117">The socket option for which the value is to be set.</span></span> <span data-ttu-id="82ff8-118">Use **o \_ KeepAlive** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="82ff8-118">Use **SO\_KEEPALIVE** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="82ff8-119">*optval* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="82ff8-119">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82ff8-120">Um ponteiro para o buffer que contém o valor da opção a ser definida.</span><span class="sxs-lookup"><span data-stu-id="82ff8-120">A pointer to the buffer containing the value for the option to set.</span></span> <span data-ttu-id="82ff8-121">Esse parâmetro deve apontar para o buffer igual ou maior que o tamanho de um valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="82ff8-121">This parameter should point to buffer equal to or larger than the size of a **DWORD** value.</span></span>

<span data-ttu-id="82ff8-122">Esse valor é tratado como um valor booliano com 0 usado para indicar **falso** (desabilitado) e um valor diferente de zero para indicar **verdadeiro** (habilitado).</span><span class="sxs-lookup"><span data-stu-id="82ff8-122">This value is treated as a boolean value with 0 used to indicate **FALSE** (disabled) and a nonzero value to indicate **TRUE** (enabled).</span></span>

</dd> <dt>

<span data-ttu-id="82ff8-123">*optlen* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="82ff8-123">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="82ff8-124">Um ponteiro para o tamanho, em bytes, do buffer *optval* .</span><span class="sxs-lookup"><span data-stu-id="82ff8-124">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="82ff8-125">Esse tamanho deve ser igual ou maior que o tamanho de um valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="82ff8-125">This size must be equal to or larger than the size of a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82ff8-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="82ff8-126">Return value</span></span>

<span data-ttu-id="82ff8-127">Se a operação for concluída com êxito, [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) retornará zero.</span><span class="sxs-lookup"><span data-stu-id="82ff8-127">If the operation completes successfully, [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) returns zero.</span></span>

<span data-ttu-id="82ff8-128">Se a operação falhar, um valor de erro de soquete \_ será retornado e um código de erro específico poderá ser recuperado chamando [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="82ff8-128">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="82ff8-129">Código do erro</span><span class="sxs-lookup"><span data-stu-id="82ff8-129">Error code</span></span>                                                                                                                                              | <span data-ttu-id="82ff8-130">Significado</span><span class="sxs-lookup"><span data-stu-id="82ff8-130">Meaning</span></span>                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="82ff8-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="82ff8-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="82ff8-132">Uma chamada [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) bem-sucedida deve ocorrer antes de usar essa função.</span><span class="sxs-lookup"><span data-stu-id="82ff8-132">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="82ff8-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="82ff8-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="82ff8-134">Falha no subsistema de rede.</span><span class="sxs-lookup"><span data-stu-id="82ff8-134">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="82ff8-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="82ff8-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="82ff8-136">Um dos parâmetros *optval* ou *optlen* aponta para a memória que não está em uma parte válida do espaço de endereço de usuário.</span><span class="sxs-lookup"><span data-stu-id="82ff8-136">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="82ff8-137">Esse erro também será retornado se o valor apontado pelo parâmetro *optlen* for menor que o tamanho de um valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="82ff8-137">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a **DWORD** value.</span></span><br/> |
| <dl> <span data-ttu-id="82ff8-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="82ff8-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="82ff8-139">Uma chamada de bloqueio do Windows Sockets 1,1 está em andamento ou o provedor de serviços ainda está processando uma função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="82ff8-139">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="82ff8-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="82ff8-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="82ff8-141">O parâmetro de *nível* é desconhecido ou inválido.</span><span class="sxs-lookup"><span data-stu-id="82ff8-141">The *level* parameter is unknown or invalid.</span></span> <span data-ttu-id="82ff8-142">No Windows Vista e posterior, esse erro também será retornado se o soquete estava em um estado de transição.</span><span class="sxs-lookup"><span data-stu-id="82ff8-142">On Windows Vista and later, this error is also returned if the socket was in a transitional state.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="82ff8-143"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="82ff8-143"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="82ff8-144">A opção é desconhecida ou não é suportada pela família de protocolos indicada.</span><span class="sxs-lookup"><span data-stu-id="82ff8-144">The option is unknown or unsupported by the indicated protocol family.</span></span> <span data-ttu-id="82ff8-145">Esse erro será retornado se o descritor de soquete passado no parâmetro *s* for para um soquete de datagrama.</span><span class="sxs-lookup"><span data-stu-id="82ff8-145">This error is returned if the socket descriptor passed in the *s* parameter was for a datagram socket.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="82ff8-146"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="82ff8-146"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="82ff8-147">O descritor não é um soquete.</span><span class="sxs-lookup"><span data-stu-id="82ff8-147">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="82ff8-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="82ff8-148">Remarks</span></span>

<span data-ttu-id="82ff8-149">A função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) chamada com a opção de soquete **\_ Keep Alive** permite que um aplicativo recupere o estado atual da opção KeepAlive, embora esse recurso não seja usado normalmente.</span><span class="sxs-lookup"><span data-stu-id="82ff8-149">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the **SO\_KEEPALIVE** socket option allows an application to retrieve the current state of the keepalive option, although this is feature not normally used.</span></span> <span data-ttu-id="82ff8-150">Se um aplicativo precisar habilitar pacotes KeepAlive em um soquete, ele apenas chamará a função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para habilitar a opção.</span><span class="sxs-lookup"><span data-stu-id="82ff8-150">If an application needs to enable keepalive packets on a socket, it justs calls the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to enable the option.</span></span>

<span data-ttu-id="82ff8-151">A função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) chamada com a opção de soquete **\_ Keep Alive** permite que um aplicativo habilite pacotes Keep-Alive para uma conexão de soquete.</span><span class="sxs-lookup"><span data-stu-id="82ff8-151">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function called with the **SO\_KEEPALIVE** socket option allows an application to enable keep-alive packets for a socket connection.</span></span> <span data-ttu-id="82ff8-152">A opção de **\_ KeepAlive** para um soquete é desabilitada (definida como **false**) por padrão.</span><span class="sxs-lookup"><span data-stu-id="82ff8-152">The **SO\_KEEPALIVE** option for a socket is disabled (set to **FALSE**) by default.</span></span>

<span data-ttu-id="82ff8-153">Quando essa opção de soquete estiver habilitada, a pilha TCP enviará pacotes Keep-Alive quando nenhum pacote de dados ou de confirmação tiver sido recebido para a conexão em um intervalo.</span><span class="sxs-lookup"><span data-stu-id="82ff8-153">When this socket option is enabled, the TCP stack sends keep-alive packets when no data or acknowledgement packets have been received for the connection within an interval.</span></span> <span data-ttu-id="82ff8-154">Para obter mais informações sobre a opção keep-alive, consulte a seção 4.2.3.6 sobre os *requisitos para hosts da Internet — camadas de comunicação* especificadas no RFC 1122 disponíveis no [site da IETF](https://www.ietf.org/rfc/rfc1122.txt).</span><span class="sxs-lookup"><span data-stu-id="82ff8-154">For more information on the keep-alive option, see section 4.2.3.6 on the *Requirements for Internet Hosts—Communication Layers* specified in RFC 1122 available at the [IETF website](https://www.ietf.org/rfc/rfc1122.txt).</span></span> <span data-ttu-id="82ff8-155">(Este recurso só pode estar disponível em inglês.)</span><span class="sxs-lookup"><span data-stu-id="82ff8-155">(This resource may only be available in English.)</span></span>

<span data-ttu-id="82ff8-156">A opção de soquete **\_ KeepAlive** é válida somente para protocolos que dão suporte à noção de Keep-Alive (protocolos orientados a conexões).</span><span class="sxs-lookup"><span data-stu-id="82ff8-156">The **SO\_KEEPALIVE** socket option is valid only for protocols that support the notion of keep-alive (connection-oriented protocols).</span></span> <span data-ttu-id="82ff8-157">Para TCP, o tempo limite de Keep-Alive padrão é 2 horas e o intervalo de Keep-Alive é de 1 segundo.</span><span class="sxs-lookup"><span data-stu-id="82ff8-157">For TCP, the default keep-alive timeout is 2 hours and the keep-alive interval is 1 second.</span></span> <span data-ttu-id="82ff8-158">O número padrão de investigações Keep-Alive varia de acordo com a versão do Windows.</span><span class="sxs-lookup"><span data-stu-id="82ff8-158">The default number of keep-alive probes varies based on the version of Windows.</span></span>

<span data-ttu-id="82ff8-159">O código de controle do [**sio \_ KeepAlive \_ Vals**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) pode ser usado para habilitar ou desabilitar Keep-Alive e ajustar o tempo limite e o intervalo para uma única conexão.</span><span class="sxs-lookup"><span data-stu-id="82ff8-159">The [**SIO\_KEEPALIVE\_VALS**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) control code can be used to enable or disable keep-alive, and adjust the timeout and interval, for a single connection.</span></span> <span data-ttu-id="82ff8-160">Se Keep-Alive estiver habilitado com **o \_ KeepAlive**, as configurações de TCP padrão serão usadas para tempo limite de Keep-Alive e intervalo, a menos que esses valores tenham sido alterados usando **sio \_ KeepAlive \_ Vals**.</span><span class="sxs-lookup"><span data-stu-id="82ff8-160">If keep-alive is enabled with **SO\_KEEPALIVE**, then the default TCP settings are used for keep-alive timeout and interval unless these values have been changed using **SIO\_KEEPALIVE\_VALS**.</span></span>

<span data-ttu-id="82ff8-161">O valor padrão em todo o sistema do tempo limite de Keep-Alive é controlável por meio da configuração do registro [KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) que usa um valor em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="82ff8-161">The default system-wide value of the keep-alive timeout is controllable through the [KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) registry setting which takes a value in milliseconds.</span></span> <span data-ttu-id="82ff8-162">O valor padrão em todo o sistema do intervalo Keep-Alive é controlável por meio da configuração do registro [KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) , que usa um valor em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="82ff8-162">The default system-wide value of the keep-alive interval is controllable through the [KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) registry setting which takes a value in milliseconds.</span></span>

<span data-ttu-id="82ff8-163">No Windows Vista e posterior, o número de investigações de Keep-Alive (retransmissões de dados) é definido como 10 e não pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="82ff8-163">On Windows Vista and later, the number of keep-alive probes (data retransmissions) is set to 10 and cannot be changed.</span></span>

<span data-ttu-id="82ff8-164">No Windows Server 2003, Windows XP e Windows 2000, a configuração padrão para o número de investigações Keep-Alive é 5.</span><span class="sxs-lookup"><span data-stu-id="82ff8-164">On Windows Server 2003, Windows XP, and Windows 2000, the default setting for number of keep-alive probes is 5.</span></span> <span data-ttu-id="82ff8-165">O número de investigações Keep Alive é controlável por meio das configurações de registro [TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10)) e [PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) .</span><span class="sxs-lookup"><span data-stu-id="82ff8-165">The number of keep-alive probes is controllable through the [TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10)) and [PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) registry settings.</span></span> <span data-ttu-id="82ff8-166">O número de investigações Keep Alive é definido como o maior dos dois valores de chave do registro.</span><span class="sxs-lookup"><span data-stu-id="82ff8-166">The number of keep-alive probes is set to the larger of the two registry key values.</span></span> <span data-ttu-id="82ff8-167">Se esse número for 0, as investigações Keep-Alive não serão enviadas.</span><span class="sxs-lookup"><span data-stu-id="82ff8-167">If this number is 0, then keep-alive probes will not be sent.</span></span> <span data-ttu-id="82ff8-168">Se esse número estiver acima de 255, ele será ajustado para 255.</span><span class="sxs-lookup"><span data-stu-id="82ff8-168">If this number is above 255, then it is adjusted to 255.</span></span>

<span data-ttu-id="82ff8-169">No Windows Vista e posterior, a opção de soquete de **\_ KeepAlive** só pode ser definida usando a função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) quando o soquete está em um estado bem conhecido, não em um estado de transição.</span><span class="sxs-lookup"><span data-stu-id="82ff8-169">On Windows Vista and later, the **SO\_KEEPALIVE** socket option can only be set using the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function when the socket is in a well-known state not a transitional state.</span></span> <span data-ttu-id="82ff8-170">Para TCP, a opção de soquete **\_ KeepAlive** deve ser definida antes da função Connect ([**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)ou [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)) ser chamada, ou após a solicitação de conexão ser realmente concluída.</span><span class="sxs-lookup"><span data-stu-id="82ff8-170">For TCP, the **SO\_KEEPALIVE** socket option should be set either before the connect function ([**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist), or [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)) is called, or after the connection request is actually completed.</span></span> <span data-ttu-id="82ff8-171">Se a função Connect tiver sido chamada de forma assíncrona, isso exigirá aguardar a conclusão da conexão antes de tentar definir a opção de soquete **\_ KeepAlive** .</span><span class="sxs-lookup"><span data-stu-id="82ff8-171">If the connect function was called asynchronously, then this requires waiting for the connection completion before trying to set the **SO\_KEEPALIVE** socket option.</span></span> <span data-ttu-id="82ff8-172">Se um aplicativo tentar definir a opção de soquete de **\_ KeepAlive** quando uma solicitação de conexão ainda estiver em andamento, a função **setsockopt** falhará e retornará [WSAEINVAL](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="82ff8-172">If an application attempts to set the **SO\_KEEPALIVE** socket option when a connection request is still in process, the **setsockopt** function will fail and return [WSAEINVAL](windows-sockets-error-codes-2.md).</span></span>

<span data-ttu-id="82ff8-173">No Windows Server 2003, Windows XP e Windows 2000, a opção de soquete **\_ KeepAlive** pode ser definida usando a função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) quando o soquete é um estado de transição (uma solicitação de conexão ainda está em andamento), bem como um estado bem conhecido.</span><span class="sxs-lookup"><span data-stu-id="82ff8-173">On Windows Server 2003, Windows XP, and Windows 2000, the **SO\_KEEPALIVE** socket option can be set using the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function when the socket is a transitional state (a connection request is still in progress) as well as a well-known state.</span></span>

<span data-ttu-id="82ff8-174">Observe que o arquivo de cabeçalho *Ws2def. h* é incluído automaticamente no *Winsock2. h* e nunca deve ser usado diretamente.</span><span class="sxs-lookup"><span data-stu-id="82ff8-174">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="82ff8-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82ff8-175">Requirements</span></span>



| <span data-ttu-id="82ff8-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="82ff8-176">Requirement</span></span> | <span data-ttu-id="82ff8-177">Valor</span><span class="sxs-lookup"><span data-stu-id="82ff8-177">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82ff8-178">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82ff8-178">Minimum supported client</span></span><br/> | <span data-ttu-id="82ff8-179">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="82ff8-179">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="82ff8-180">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82ff8-180">Minimum supported server</span></span><br/> | <span data-ttu-id="82ff8-181">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="82ff8-181">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="82ff8-182">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="82ff8-182">Header</span></span><br/>                   | <dl> <span data-ttu-id="82ff8-183"><dt>Ws2def. h (incluir Winsock2. h)</dt></span><span class="sxs-lookup"><span data-stu-id="82ff8-183"><dt>Ws2def.h (include Winsock2.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82ff8-184">Confira também</span><span class="sxs-lookup"><span data-stu-id="82ff8-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82ff8-185">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="82ff8-185">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="82ff8-186">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="82ff8-186">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

<span data-ttu-id="82ff8-187">[KeepAlivetime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="82ff8-187">[KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="82ff8-188">[KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="82ff8-188">[KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="82ff8-189">[PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="82ff8-189">[PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="82ff8-190">**SSA**</span><span class="sxs-lookup"><span data-stu-id="82ff8-190">**socket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

<span data-ttu-id="82ff8-191">[**SIO \_ KeepAlive \_ Vals**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="82ff8-191">[**SIO\_KEEPALIVE\_VALS**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="82ff8-192">[TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="82ff8-192">[TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="82ff8-193">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="82ff8-193">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)
</dt> </dl>

 

 
