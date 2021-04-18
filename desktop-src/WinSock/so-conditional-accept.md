---
description: Foi projetado para permitir que um aplicativo decida se deseja ou não aceitar uma conexão de entrada em um soquete de escuta.
ms.assetid: 964683eb-5dfc-4441-abb7-315be8b89a19
title: Opção de soquete SO_CONDITIONAL_ACCEPT (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: badfdd1f8aac49ae05fa6b77dadb2561ba5ea02f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814056"
---
# <a name="so_conditional_accept-socket-option"></a><span data-ttu-id="e216c-103">\_Opção de \_ soquete de aceitação condicional</span><span class="sxs-lookup"><span data-stu-id="e216c-103">SO\_CONDITIONAL\_ACCEPT socket option</span></span>

<span data-ttu-id="e216c-104">A opção de soquete de **\_ \_ aceitação condicional** foi projetada para permitir que um aplicativo decida se deseja ou não aceitar uma conexão de entrada em um soquete de escuta.</span><span class="sxs-lookup"><span data-stu-id="e216c-104">The **SO\_CONDITIONAL\_ACCEPT** socket option is designed to allow an application to decide whether or not to accept an incoming connection on a listening socket.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="e216c-105">Valor da opção de soquete</span><span class="sxs-lookup"><span data-stu-id="e216c-105">Socket option value</span></span>

<span data-ttu-id="e216c-106">A constante que representa essa opção de soquete é 0x3002.</span><span class="sxs-lookup"><span data-stu-id="e216c-106">The constant that represents this socket option is 0x3002.</span></span>

## <a name="syntax"></a><span data-ttu-id="e216c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e216c-107">Syntax</span></span>


```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_CONDITIONAL_ACCEPT, // optname
  (char *) optval,         // input buffer,
  (int) optlen,       // size of input buffer
);
```



## <a name="parameters"></a><span data-ttu-id="e216c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e216c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e216c-109">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="e216c-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e216c-110">Um descritor que identifica o soquete.</span><span class="sxs-lookup"><span data-stu-id="e216c-110">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="e216c-111">*nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="e216c-111">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e216c-112">O nível no qual a opção é definida.</span><span class="sxs-lookup"><span data-stu-id="e216c-112">The level at which the option is defined.</span></span> <span data-ttu-id="e216c-113">Use **o \_ soquete sol** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="e216c-113">Use **SOL\_SOCKET** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="e216c-114">*OptName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e216c-114">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e216c-115">A opção de soquete para a qual o valor deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="e216c-115">The socket option for which the value is to be set.</span></span> <span data-ttu-id="e216c-116">Use **a \_ \_ aceitação condicional** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="e216c-116">Use **SO\_CONDITIONAL\_ACCEPT** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="e216c-117">*optval* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e216c-117">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e216c-118">Um ponteiro para o buffer que contém o valor da opção a ser definida.</span><span class="sxs-lookup"><span data-stu-id="e216c-118">A pointer to the buffer containing the value for the option to set.</span></span> <span data-ttu-id="e216c-119">Esse parâmetro deve apontar para o buffer igual ou maior que o tamanho de um valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="e216c-119">This parameter should point to buffer equal to or larger than the size of a **DWORD** value.</span></span>

<span data-ttu-id="e216c-120">Esse valor é tratado como um valor booliano com 0 usado para indicar **falso** (desabilitado) e um valor diferente de zero para indicar **verdadeiro** (habilitado).</span><span class="sxs-lookup"><span data-stu-id="e216c-120">This value is treated as a boolean value with 0 used to indicate **FALSE** (disabled) and a nonzero value to indicate **TRUE** (enabled).</span></span>

</dd> <dt>

<span data-ttu-id="e216c-121">*optlen* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="e216c-121">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e216c-122">Um ponteiro para o tamanho, em bytes, do buffer *optval* .</span><span class="sxs-lookup"><span data-stu-id="e216c-122">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="e216c-123">Esse tamanho deve ser igual ou maior que o tamanho de um valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="e216c-123">This size must be equal to or larger than the size of a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e216c-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e216c-124">Return value</span></span>

<span data-ttu-id="e216c-125">Se a operação for concluída com êxito, [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) retornará zero.</span><span class="sxs-lookup"><span data-stu-id="e216c-125">If the operation completes successfully, [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) returns zero.</span></span>

<span data-ttu-id="e216c-126">Se a operação falhar, um valor de erro de soquete \_ será retornado e um código de erro específico poderá ser recuperado chamando [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="e216c-126">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="e216c-127">Código do erro</span><span class="sxs-lookup"><span data-stu-id="e216c-127">Error code</span></span>                                                                                                                                              | <span data-ttu-id="e216c-128">Significado</span><span class="sxs-lookup"><span data-stu-id="e216c-128">Meaning</span></span>                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e216c-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="e216c-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="e216c-130">Uma chamada [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) bem-sucedida deve ocorrer antes de usar essa função.</span><span class="sxs-lookup"><span data-stu-id="e216c-130">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="e216c-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="e216c-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="e216c-132">Falha no subsistema de rede.</span><span class="sxs-lookup"><span data-stu-id="e216c-132">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="e216c-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="e216c-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="e216c-134">Um dos parâmetros *optval* ou *optlen* aponta para a memória que não está em uma parte válida do espaço de endereço de usuário.</span><span class="sxs-lookup"><span data-stu-id="e216c-134">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="e216c-135">Esse erro também será retornado se o valor apontado pelo parâmetro *optlen* for menor que o tamanho de um valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="e216c-135">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a **DWORD** value.</span></span><br/> |
| <dl> <span data-ttu-id="e216c-136"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="e216c-136"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="e216c-137">Uma chamada de bloqueio do Windows Sockets 1,1 está em andamento ou o provedor de serviços ainda está processando uma função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e216c-137">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="e216c-138"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="e216c-138"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="e216c-139">O parâmetro de *nível* é desconhecido ou inválido.</span><span class="sxs-lookup"><span data-stu-id="e216c-139">The *level* parameter is unknown or invalid.</span></span> <span data-ttu-id="e216c-140">Esse erro também será retornado se o soquete já estava em um estado de escuta.</span><span class="sxs-lookup"><span data-stu-id="e216c-140">This error is also returned if the socket was already in a listening state.</span></span><br/>                                                                                                                        |
| <dl> <span data-ttu-id="e216c-141"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="e216c-141"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="e216c-142">A opção é desconhecida ou não é suportada pela família de protocolos indicada.</span><span class="sxs-lookup"><span data-stu-id="e216c-142">The option is unknown or unsupported by the indicated protocol family.</span></span><br/>                                                                                                                                                                          |
| <dl> <span data-ttu-id="e216c-143"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="e216c-143"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="e216c-144">O descritor não é um soquete.</span><span class="sxs-lookup"><span data-stu-id="e216c-144">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="e216c-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="e216c-145">Remarks</span></span>

<span data-ttu-id="e216c-146">A função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) chamada com a opção de soquete de **\_ \_ aceitação condicional** permite que um aplicativo decida se deseja ou não aceitar uma conexão de entrada em um soquete de escuta.</span><span class="sxs-lookup"><span data-stu-id="e216c-146">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function called with the **SO\_CONDITIONAL\_ACCEPT** socket option allows an application to decide whether or not to accept an incoming connection on a listening socket.</span></span> <span data-ttu-id="e216c-147">A opção Accept condicional para um soquete é desabilitada (definida como **false**) por padrão.</span><span class="sxs-lookup"><span data-stu-id="e216c-147">The conditional accept option for a socket is disabled (set to **FALSE**) by default.</span></span>

<span data-ttu-id="e216c-148">Quando essa opção de soquete está habilitada, a pilha TCP não aceita conexões automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e216c-148">When this socket option is enabled, the TCP stack does not automatically accept connections.</span></span> <span data-ttu-id="e216c-149">Ele aguarda que o aplicativo indique que ele aceita a conexão por meio do retorno de chamada de aceitação condicional registrado com a função [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) .</span><span class="sxs-lookup"><span data-stu-id="e216c-149">It waits for the application to indicate that it accepts the connection via the conditional accept callback registered with [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function.</span></span> <span data-ttu-id="e216c-150">Depois que uma solicitação de conexão é recebida, o Winsock invoca o retorno de chamada de aceitação condicional registrado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e216c-150">Once a connection request is received, Winsock invokes the conditional accept callback registered by the application.</span></span> <span data-ttu-id="e216c-151">Somente quando o retorno de chamada de aceitação condicional retorna **CF \_ Accept** , o Winsock notificará o transporte para aceitar totalmente a conexão.</span><span class="sxs-lookup"><span data-stu-id="e216c-151">Only when the conditional accept callback returns **CF\_ACCEPT** will Winsock notify the transport to fully accept the connection.</span></span>

<span data-ttu-id="e216c-152">Quando a opção de soquete de **\_ \_ aceitação condicional** estiver definida como habilitado (definido como **true**), isso terá vários efeitos colaterais no soquete:</span><span class="sxs-lookup"><span data-stu-id="e216c-152">When the **SO\_CONDITIONAL\_ACCEPT** socket option is set to enabled (set to **TRUE**), this has several side effects on the socket:</span></span>

-   <span data-ttu-id="e216c-153">Isso desabilita as defesas de proteção contra ataques SYN internas da pilha TCP, já que o aplicativo agora está assumindo a propriedade de aceitar conexões.</span><span class="sxs-lookup"><span data-stu-id="e216c-153">This disables the TCP stack's built-in SYN attack protection defenses, since the application is now taking ownership of accepting connections.</span></span>
-   <span data-ttu-id="e216c-154">Isso efetivamente desabilita a pendência de escuta, pois as conexões não são aceitas em nome de um soquete de escuta.</span><span class="sxs-lookup"><span data-stu-id="e216c-154">This effectively disables the listen backlog since connections aren't accepted on behalf of a listening socket.</span></span> <span data-ttu-id="e216c-155">Uma conexão nunca é totalmente aceita até que o aplicativo aceite totalmente usando o mecanismo de **\_ aceitação do CF** .</span><span class="sxs-lookup"><span data-stu-id="e216c-155">A connection is never fully accepted until the application fully accepts using the **CF\_ACCEPT** mechanism.</span></span>
-   <span data-ttu-id="e216c-156">Isso também significa que o aplicativo deve cuidar sempre estar em um estado para lidar prontamente com os retornos de chamada Accept para aceitar a conexão.</span><span class="sxs-lookup"><span data-stu-id="e216c-156">This also means the application take care to always be in a state to readily handle the accept callbacks to accept the connection.</span></span> <span data-ttu-id="e216c-157">Se o aplicativo estiver ocupado fazendo outro processamento, o lado do cliente poderá atingir o tempo limite antes que o aplicativo realmente aceite a conexão.</span><span class="sxs-lookup"><span data-stu-id="e216c-157">If the application is busy doing other processing, then the client side may time out before the application actually accepts the connection.</span></span> <span data-ttu-id="e216c-158">Isso leva a uma experiência de cliente ruim.</span><span class="sxs-lookup"><span data-stu-id="e216c-158">This leads to a poor client experience.</span></span>

<span data-ttu-id="e216c-159">Em geral, o principal motivo pelo qual os aplicativos usam a aceitação condicional é inspecionar o endereço IP de origem ou a porta usada pelo cliente que está se conectando e, em seguida, decidir aceitar ou rejeitar a conexão.</span><span class="sxs-lookup"><span data-stu-id="e216c-159">Generally, the main reason applications use conditional accept is to inspect the source IP address or port used by the connecting client and then decide to accept or reject the connection.</span></span> <span data-ttu-id="e216c-160">No entanto, os aplicativos provavelmente executarão melhor se \_ a \_ opção de aceitação condicional não estiver habilitada e o aplicativo permitir que a pilha TCP e a lista de pendências de escuta funcionem conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="e216c-160">However, applications are likely to perform better if the SO\_CONDITIONAL\_ACCEPT option is not enabled and the application allows the TCP stack and the listen backlog to work as expected.</span></span> <span data-ttu-id="e216c-161">Em seguida, quando o aplicativo lida com a conexão aceita, se for de uma porta ou endereço de origem de IP impróprio, o aplicativo poderá simplesmente fechar o soquete.</span><span class="sxs-lookup"><span data-stu-id="e216c-161">Then when the application handles the accepted connection, if it is from a improper IP source address or port, the application can just close the socket.</span></span> <span data-ttu-id="e216c-162">A desvantagem da segurança desse comportamento é que agora o cliente tem uma confirmação de que o aplicativo está escutando em um endereço IP e uma porta, uma vez que ele fechou de modo forçado a conexão aceita anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e216c-162">The security drawback to this behavior is that now the client has confirmation that the application is listening on an IP address and port since it forcefully closed the previously accepted connection.</span></span> <span data-ttu-id="e216c-163">No entanto, as desvantagens de habilitar a **\_ \_ aceitação condicional** geralmente superam essa limitação.</span><span class="sxs-lookup"><span data-stu-id="e216c-163">However, the drawbacks to enabling **SO\_CONDITIONAL\_ACCEPT** generally outweigh this limitation.</span></span>

<span data-ttu-id="e216c-164">A função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) chamada com a opção de soquete de **\_ \_ aceitação condicional** permite que um aplicativo recupere o estado atual da opção de aceitação condicional, embora esse recurso não seja usado normalmente.</span><span class="sxs-lookup"><span data-stu-id="e216c-164">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the **SO\_CONDITIONAL\_ACCEPT** socket option allows an application to retrieve the current state of the conditional accept option, although this is feature not normally used.</span></span> <span data-ttu-id="e216c-165">Se um aplicativo precisar habilitar a aceitação condicional em um soquete, ele apenas chamará a função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para habilitar a opção.</span><span class="sxs-lookup"><span data-stu-id="e216c-165">If an application needs to enable conditional accept on a socket, it justs calls the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to enable the option.</span></span>

<span data-ttu-id="e216c-166">Observe que o arquivo de cabeçalho *Ws2def. h* é incluído automaticamente no *Winsock2. h* e nunca deve ser usado diretamente.</span><span class="sxs-lookup"><span data-stu-id="e216c-166">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="e216c-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e216c-167">Requirements</span></span>



| <span data-ttu-id="e216c-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="e216c-168">Requirement</span></span> | <span data-ttu-id="e216c-169">Valor</span><span class="sxs-lookup"><span data-stu-id="e216c-169">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e216c-170">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e216c-170">Minimum supported client</span></span><br/> | <span data-ttu-id="e216c-171">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e216c-171">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e216c-172">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e216c-172">Minimum supported server</span></span><br/> | <span data-ttu-id="e216c-173">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e216c-173">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e216c-174">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e216c-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="e216c-175"><dt>Ws2def. h (incluir Winsock2. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e216c-175"><dt>Ws2def.h (include Winsock2.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e216c-176">Confira também</span><span class="sxs-lookup"><span data-stu-id="e216c-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e216c-177">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="e216c-177">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="e216c-178">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="e216c-178">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[<span data-ttu-id="e216c-179">**WSAAccept**</span><span class="sxs-lookup"><span data-stu-id="e216c-179">**WSAAccept**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)
</dt> </dl>

 

 




