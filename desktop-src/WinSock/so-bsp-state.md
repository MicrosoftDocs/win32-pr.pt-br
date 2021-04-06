---
description: Retorna o endereço local, a porta local, o endereço remoto, a porta remota, o tipo de soquete e o protocolo usados por um soquete.
ms.assetid: 2628f47e-3e73-4e02-91b8-ba4cb0800864
title: Opção de soquete SO_BSP_STATE (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d10e391d70dd67190e1aec803036d019261c9000
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661771"
---
# <a name="so_bsp_state-socket-option"></a><span data-ttu-id="8a5b1-103">\_Opção de \_ soquete de estado BSP</span><span class="sxs-lookup"><span data-stu-id="8a5b1-103">SO\_BSP\_STATE socket option</span></span>

<span data-ttu-id="8a5b1-104">A opção de soquete de **\_ \_ estado BSP de so** retorna o endereço local, a porta local, o endereço remoto, a porta remota, o tipo de soquete e o protocolo usado por um soquete.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-104">The **SO\_BSP\_STATE** socket option returns the local address, local port, remote address, remote port, socket type, and protocol used by a socket.</span></span>

<span data-ttu-id="8a5b1-105">Para executar essa operação, chame a função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-105">To perform this operation, call the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function with the following parameters.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="8a5b1-106">Valor da opção de soquete</span><span class="sxs-lookup"><span data-stu-id="8a5b1-106">Socket option value</span></span>

<span data-ttu-id="8a5b1-107">A constante que representa essa opção de soquete é 0x1009.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-107">The constant that represents this socket option is 0x1009.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a5b1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a5b1-108">Syntax</span></span>


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_BSP_STATE, // optname
  (char *) optval,         // output buffer,
  (int) *optlen,       // size of output buffer
);
```



## <a name="parameters"></a><span data-ttu-id="8a5b1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a5b1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a5b1-110">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="8a5b1-110">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a5b1-111">Um descritor que identifica o soquete.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-111">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="8a5b1-112">*nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="8a5b1-112">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a5b1-113">O nível no qual a opção é definida.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-113">The level at which the option is defined.</span></span> <span data-ttu-id="8a5b1-114">Use **o \_ soquete sol** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-114">Use **SOL\_SOCKET** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="8a5b1-115">*OptName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8a5b1-115">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a5b1-116">A opção de soquete para a qual o valor deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-116">The socket option for which the value is to be retrieved.</span></span> <span data-ttu-id="8a5b1-117">Use **o \_ \_ estado BSP** para esta operação.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-117">Use **SO\_BSP\_STATE** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="8a5b1-118">*optval* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8a5b1-118">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a5b1-119">Um ponteiro para o buffer no qual o valor da opção solicitada deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-119">A pointer to the buffer in which the value for the requested option is to be returned.</span></span> <span data-ttu-id="8a5b1-120">Esse parâmetro deve apontar para o buffer igual ou maior que o tamanho de uma estrutura de [**\_ informações de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .</span><span class="sxs-lookup"><span data-stu-id="8a5b1-120">This parameter should point to buffer equal to or larger than the size of a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8a5b1-121">*optlen* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="8a5b1-121">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a5b1-122">Um ponteiro para o tamanho, em bytes, do buffer *optval* .</span><span class="sxs-lookup"><span data-stu-id="8a5b1-122">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="8a5b1-123">Esse tamanho deve ser igual ou maior que o tamanho de uma estrutura [**de \_ informações de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .</span><span class="sxs-lookup"><span data-stu-id="8a5b1-123">This size must be equal to or larger than the size of a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a5b1-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8a5b1-124">Return value</span></span>

<span data-ttu-id="8a5b1-125">Se a operação for concluída com êxito, [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) retornará zero.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-125">If the operation completes successfully, [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) returns zero.</span></span>

<span data-ttu-id="8a5b1-126">Se a operação falhar, um valor de erro de soquete \_ será retornado e um código de erro específico poderá ser recuperado chamando [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="8a5b1-126">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="8a5b1-127">Código do erro</span><span class="sxs-lookup"><span data-stu-id="8a5b1-127">Error code</span></span>                                                                                                                                              | <span data-ttu-id="8a5b1-128">Significado</span><span class="sxs-lookup"><span data-stu-id="8a5b1-128">Meaning</span></span>                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8a5b1-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="8a5b1-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="8a5b1-130">Uma chamada [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) bem-sucedida deve ocorrer antes de usar essa função.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-130">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="8a5b1-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="8a5b1-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="8a5b1-132">Falha no subsistema de rede.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-132">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="8a5b1-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="8a5b1-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="8a5b1-134">Um dos parâmetros *optval* ou *optlen* aponta para a memória que não está em uma parte válida do espaço de endereço de usuário.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-134">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="8a5b1-135">Esse erro também será retornado se o valor apontado pelo parâmetro *optlen* for menor que o tamanho de uma estrutura [**de \_ informações de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .</span><span class="sxs-lookup"><span data-stu-id="8a5b1-135">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span><br/> |
| <dl> <span data-ttu-id="8a5b1-136"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="8a5b1-136"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="8a5b1-137">Uma chamada de bloqueio do Windows Sockets 1,1 está em andamento ou o provedor de serviços ainda está processando uma função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-137">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                                                            |
| <dl> <span data-ttu-id="8a5b1-138"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="8a5b1-138"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="8a5b1-139">O parâmetro de *nível* é desconhecido ou inválido.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-139">The *level* parameter is unknown or invalid.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="8a5b1-140"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="8a5b1-140"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="8a5b1-141">A opção é desconhecida ou não é suportada pela família de protocolos indicada.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-141">The option is unknown or unsupported by the indicated protocol family.</span></span><br/>                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="8a5b1-142"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="8a5b1-142"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="8a5b1-143">O descritor não é um soquete.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-143">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="8a5b1-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a5b1-144">Remarks</span></span>

<span data-ttu-id="8a5b1-145">A função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) chamada com a opção de soquete de **\_ \_ estado BSP de so** recupera o endereço local, a porta local, o endereço remoto, a porta remota, o tipo de soquete e o protocolo usados por um soquete.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-145">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the **SO\_BSP\_STATE** socket option retrieves the local address, local port, remote address, remote port, socket type, and protocol used by a socket.</span></span> <span data-ttu-id="8a5b1-146">A opção de soquete de **\_ \_ estado BSP de so** funciona com soquetes IPv6 ou IPv4 (as famílias de endereços da **\_ inet** **\_ INET6** e AF).</span><span class="sxs-lookup"><span data-stu-id="8a5b1-146">The **SO\_BSP\_STATE** socket option works with IPv6 or IPv4 sockets (the **AF\_INET6** and **AF\_INET** address families).</span></span>

<span data-ttu-id="8a5b1-147">Se a função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) for bem-sucedida, as informações serão retornadas em uma estrutura de [**\_ informações de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) no buffer apontado pelo parâmetro *optval* .</span><span class="sxs-lookup"><span data-stu-id="8a5b1-147">If the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function is successful, the information is returned in a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure in the buffer pointed to by the *optval* parameter.</span></span> <span data-ttu-id="8a5b1-148">O inteiro apontado por *optlen* deve conter originalmente o tamanho desse buffer; no retorno, ele será definido como o comprimento, em bytes, do valor retornado no parâmetro *optval* .</span><span class="sxs-lookup"><span data-stu-id="8a5b1-148">The integer pointed to by *optlen* should originally contain the size of this buffer; on return, it will be set to the length, in bytes, of the value returned in the *optval* parameter.</span></span>

<span data-ttu-id="8a5b1-149">Os membros **iSocketType** e **iProtocol** na estrutura de [**\_ informações de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) retornada são preenchidos para o descritor de soquete no parâmetro *s* .</span><span class="sxs-lookup"><span data-stu-id="8a5b1-149">The **iSocketType** and **iProtocol** members in the returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure are filled in for the socket descriptor in the *s* parameter.</span></span>

<span data-ttu-id="8a5b1-150">Se o soquete estiver em um estado conectado ou ligado, o membro **localaddr** da estrutura de [**\_ informações de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) retornada será definido como uma estrutura [SOCKADDR](sockaddr-2.md) que representa o endereço e a porta locais.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-150">If the socket is in a connected or bound state, then the **LocalAddr** member of the returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure will be set to a [SOCKADDR](sockaddr-2.md) structure representing the local address and port.</span></span> <span data-ttu-id="8a5b1-151">Se o soquete estiver em um estado conectado, o membro **RemoteAddr** da estrutura de **\_ informações de CSADDR** retornada será definido como uma estrutura sockaddr que representa o endereço e a porta remotos.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-151">If the socket is in a connected state, then the **RemoteAddr** member of the returned **CSADDR\_INFO** structure will be set to a SOCKADDR structure representing the remote address and port.</span></span>

<span data-ttu-id="8a5b1-152">Se o soquete não estiver em um estado conectado ou ligado, o membro **localaddr** da estrutura de [**\_ informações de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) retornada será retornado com um ponteiro **nulo** no membro **lpSockAddr** e o membro **iSockaddrLength** definido como zero.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-152">If the socket is not in a connected or bound state, then the **LocalAddr** member of the returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure is returned with a **NULL** pointer in the **lpSockaddr** member and the **iSockaddrLength** member set to zero.</span></span> <span data-ttu-id="8a5b1-153">Se o soquete não estiver em um estado ligado, o membro **RemoteAddr** da estrutura de **\_ informações de CSADDR** retornada será retornado com um ponteiro **nulo** no membro **lpSockAddr** e o membro **iSockaddrLength** definido como zero.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-153">If the socket is not in a bound state, then the **RemoteAddr** member of the returned **CSADDR\_INFO** structure is returned with a **NULL** pointer in the **lpSockaddr** member and the **iSockaddrLength** member set to zero.</span></span>

<span data-ttu-id="8a5b1-154">Se a função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) falhar, os *parâmetros optval* e *optlen* permanecerão inalterados e o parâmetro *optval* não apontará para uma estrutura de [**\_ informações de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) retornada.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-154">If the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function fails, the *optval* and *optlen* parameters are left unchanged and the *optval* parameter does not point to a returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span>

<span data-ttu-id="8a5b1-155">Observe que o arquivo de cabeçalho *Ws2def. h* é incluído automaticamente no *Winsock2. h* e nunca deve ser usado diretamente.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-155">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a5b1-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a5b1-156">Requirements</span></span>



| <span data-ttu-id="8a5b1-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a5b1-157">Requirement</span></span> | <span data-ttu-id="8a5b1-158">Valor</span><span class="sxs-lookup"><span data-stu-id="8a5b1-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a5b1-159">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a5b1-159">Minimum supported client</span></span><br/> | <span data-ttu-id="8a5b1-160">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8a5b1-160">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8a5b1-161">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a5b1-161">Minimum supported server</span></span><br/> | <span data-ttu-id="8a5b1-162">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8a5b1-162">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8a5b1-163">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8a5b1-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a5b1-164"><dt>Ws2def. h (incluir Winsock2. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8a5b1-164"><dt>Ws2def.h (include Winsock2.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a5b1-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a5b1-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a5b1-166">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="8a5b1-166">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="8a5b1-167">**informações de CSADDR \_**</span><span class="sxs-lookup"><span data-stu-id="8a5b1-167">**CSADDR\_INFO**</span></span>](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)
</dt> <dt>

[<span data-ttu-id="8a5b1-168">SOCKADDR</span><span class="sxs-lookup"><span data-stu-id="8a5b1-168">SOCKADDR</span></span>](sockaddr-2.md)
</dt> </dl>

 

 
