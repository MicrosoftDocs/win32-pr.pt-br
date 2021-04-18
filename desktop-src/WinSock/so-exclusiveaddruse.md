---
description: A \_ opção de soquete EXCLUSIVEADDRUSE impede que outros soquetes sejam ligados à força no mesmo endereço e porta.
ms.assetid: ce0d8188-54be-46e8-8753-d0680f690b84
title: Opção de soquete SO_EXCLUSIVEADDRUSE (Winsock2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d4747150f918a7e9c4ce37ec209e7261d1a00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105773031"
---
# <a name="so_exclusiveaddruse-socket-option"></a><span data-ttu-id="c3598-103">\_Opção de soquete EXCLUSIVEADDRUSE</span><span class="sxs-lookup"><span data-stu-id="c3598-103">SO\_EXCLUSIVEADDRUSE socket option</span></span>

<span data-ttu-id="c3598-104">A \_ opção de soquete EXCLUSIVEADDRUSE impede que outros soquetes sejam ligados à força no mesmo endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="c3598-104">The SO\_EXCLUSIVEADDRUSE socket option prevents other sockets from being forcibly bound to the same address and port.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3598-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3598-105">Syntax</span></span>

<span data-ttu-id="c3598-106">A \_ opção de EXCLUSIVEADDRUSE impede que outros soquetes sejam vinculados à força ao mesmo endereço e porta, uma prática habilitada pela \_ opção de soquete REUSEADDR.</span><span class="sxs-lookup"><span data-stu-id="c3598-106">The SO\_EXCLUSIVEADDRUSE option prevents other sockets from being forcibly bound to the same address and port, a practice enabled by the SO\_REUSEADDR socket option.</span></span> <span data-ttu-id="c3598-107">Essa reutilização pode ser executada por aplicativos mal-intencionados para interromper o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c3598-107">Such reuse can be executed by malicious applications to disrupt the application.</span></span> <span data-ttu-id="c3598-108">A \_ opção EXCLUSIVEADDRUSE é muito útil para serviços do sistema que exigem alta disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="c3598-108">The SO\_EXCLUSIVEADDRUSE option is very useful to system services requiring high availability.</span></span>

<span data-ttu-id="c3598-109">O exemplo de código a seguir ilustra como definir essa opção.</span><span class="sxs-lookup"><span data-stu-id="c3598-109">The following code example illustrates setting this option.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>
#include <stdlib.h>             // Needed for _wtoi

#pragma comment(lib, "Ws2_32.lib")

int __cdecl wmain(int argc, wchar_t ** argv)
{
    WSADATA wsaData;
    int iResult = 0;
    int iError = 0;

    SOCKET s = INVALID_SOCKET;
    SOCKADDR_IN saLocal;
    int iOptval = 0;

    int iFamily = AF_UNSPEC;
    int iType = 0;
    int iProtocol = 0;

    int iPort = 0;

    // Validate the parameters
    if (argc != 5) {
        wprintf(L"usage: %ws <addressfamily> <type> <protocol> <port>\n", argv[0]);
        wprintf(L"    opens a socket for the specified family, type, & protocol\n");
        wprintf(L"    sets the SO_EXCLUSIVEADDRUSE socket option on the socket\n");
        wprintf(L"    then tries to bind the port specified on the command-line\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 0 2 17 5150\n", argv[0]);
        wprintf(L"   where AF_UNSPEC=0 SOCK_DGRAM=2 IPPROTO_UDP=17  PORT=5150\n",
                argv[0]);
        wprintf(L"   %ws 2 1 17 5150\n", argv[0]);
        wprintf(L"   where AF_INET=2 SOCK_STREAM=1 IPPROTO_TCP=6  PORT=5150\n", argv[0]);
        wprintf(L"   See the documentation for the socket function for other values\n");
        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);

    iPort = _wtoi(argv[4]);

    if (iFamily != AF_INET && iFamily != AF_INET6) {
        wprintf(L"Address family must be either AF_INET (2) or AF_INET6 (23)\n");
        return 1;
    }

    if (iPort <= 0 || iPort >= 65535) {
        wprintf(L"Port specified must be greater than 0 and less than 65535\n");
        return 1;
    }
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error: %d\n", iResult);
        return 1;
    }
    // Create the socket
    s = socket(iFamily, iType, iProtocol);
    if (s == INVALID_SOCKET) {
        wprintf(L"socket failed with error: %ld\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }
    // Set the exclusive address option
    iOptval = 1;
    iResult = setsockopt(s, SOL_SOCKET, SO_EXCLUSIVEADDRUSE,
                         (char *) &iOptval, sizeof (iOptval));
    if (iResult == SOCKET_ERROR) {
        wprintf(L"setsockopt for SO_EXCLUSIVEADDRUSE failed with error: %ld\n",
                WSAGetLastError());
    }

    saLocal.sin_family = (ADDRESS_FAMILY) iFamily;
    saLocal.sin_port = htons( (u_short) iPort);
    saLocal.sin_addr.s_addr = htonl(INADDR_ANY);

    // Bind the socket
    iResult = bind(s, (SOCKADDR *) & saLocal, sizeof (saLocal));
    if (iResult == SOCKET_ERROR) {

        // Most errors related to setting SO_EXCLUSIVEADDRUSE
        //    will occur at bind.
        iError = WSAGetLastError();
        if (iError == WSAEACCES)
            wprintf(L"bind failed with WSAEACCES (access denied)\n");
        else
            wprintf(L"bind failed with error: %ld\n", iError);

    } else {
        wprintf(L"bind on socket with SO_EXCLUSIVEADDRUSE succeeded to port: %ld\n",
                iPort);
    }

    // cleanup
    closesocket(s);
    WSACleanup();

    return 0;
}

```



<span data-ttu-id="c3598-110">Para ter qualquer efeito, a \_ opção for EXCLUSIVADDRUSE deve ser definida antes de a função [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) ser chamada (isso também se aplica à \_ opção REUSEADDR, por isso).</span><span class="sxs-lookup"><span data-stu-id="c3598-110">To have any effect, the SO\_EXCLUSIVADDRUSE option must be set before the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called (this also applies to the SO\_REUSEADDR option).</span></span> <span data-ttu-id="c3598-111">A tabela 1 lista os efeitos da definição da \_ opção EXCLUSIVEADDRUSE.</span><span class="sxs-lookup"><span data-stu-id="c3598-111">Table 1 lists the effects of setting the SO\_EXCLUSIVEADDRUSE option.</span></span> <span data-ttu-id="c3598-112">O caractere curinga indica a associação ao endereço curinga, como 0.0.0.0 para IPv4 e:: para IPv6.</span><span class="sxs-lookup"><span data-stu-id="c3598-112">Wildcard indicates binding to the wildcard address, such as 0.0.0.0 for IPv4 and :: for IPv6.</span></span> <span data-ttu-id="c3598-113">Específico indica a associação a uma interface específica, como a associação de um endereço IP atribuído a um adaptador.</span><span class="sxs-lookup"><span data-stu-id="c3598-113">Specific indicates binding to a specific interface, such as binding an IP address assigned to an adapter.</span></span> <span data-ttu-id="c3598-114">Specific2 indica a associação a um endereço específico diferente do endereço associado a no caso específico.</span><span class="sxs-lookup"><span data-stu-id="c3598-114">Specific2 indicates binding to a specific address other than the address bound to in the Specific case.</span></span>

> [!Note]  
> <span data-ttu-id="c3598-115">O caso de Specific2 é aplicável somente quando a primeira ligação é executada com um endereço específico; para o caso em que o primeiro soquete está associado ao curinga, a entrada para específico abrange todos os casos de endereço específicos.</span><span class="sxs-lookup"><span data-stu-id="c3598-115">The Specific2 case is applicable only when the first bind is performed with a specific address; for the case in which the first socket is bound to the wildcard, the entry for Specific covers all specific address cases.</span></span>

 

<span data-ttu-id="c3598-116">Por exemplo, considere um computador com duas interfaces IP: 10.0.0.1 e 10.99.99.99.</span><span class="sxs-lookup"><span data-stu-id="c3598-116">For example, consider a computer with two IP interfaces: 10.0.0.1 and 10.99.99.99.</span></span> <span data-ttu-id="c3598-117">Se a primeira ligação for 10.0.0.1 e a porta 5150 com a \_ opção EXCLUSIVEADDRUSE definida, a segunda ligação a 10.99.99.99 e a porta 5150 com qualquer ou nenhuma opção definida terá sucesso.</span><span class="sxs-lookup"><span data-stu-id="c3598-117">If the first bind is to 10.0.0.1 and port 5150 with the SO\_EXCLUSIVEADDRUSE option set, then the second bind to 10.99.99.99 and port 5150 with any or no options set succeeds.</span></span> <span data-ttu-id="c3598-118">No entanto, se o primeiro soquete estiver associado ao endereço curinga (0.0.0.0) e à porta 5150 com \_ o EXCLUSIVEADDRUSE definido, qualquer associação subsequente à mesma porta, independentemente do endereço IP, falhará com WSAEADDRINUSE (10048) ou WSAEACCESS (10013), dependendo de quais opções foram definidas no segundo soquete de ligação.</span><span class="sxs-lookup"><span data-stu-id="c3598-118">However, if the first socket is bound to the wildcard address (0.0.0.0) and port 5150 with SO\_EXCLUSIVEADDRUSE set, any subsequent bind to the same port—regardless of IP address—will fail with either WSAEADDRINUSE (10048) or WSAEACCESS (10013), depending on which options were set on the second bind socket.</span></span>

### <a name="bind-behavior-with-various-options-set"></a><span data-ttu-id="c3598-119">Comportamento de ligação com várias opções definidas</span><span class="sxs-lookup"><span data-stu-id="c3598-119">Bind Behavior with Various Options Set</span></span>



<span data-ttu-id="c3598-120">Segunda Associação</span><span class="sxs-lookup"><span data-stu-id="c3598-120">Second bind</span></span>

<span data-ttu-id="c3598-121">Primeira ligação</span><span class="sxs-lookup"><span data-stu-id="c3598-121">First bind</span></span>

<span data-ttu-id="c3598-122">*\_EXCLUSIVEADDRUSE*</span><span class="sxs-lookup"><span data-stu-id="c3598-122">*SO\_EXCLUSIVEADDRUSE*</span></span>

<span data-ttu-id="c3598-123">*Nenhuma opção* ou *\_ REUSEADDR*</span><span class="sxs-lookup"><span data-stu-id="c3598-123">*No options* or *SO\_REUSEADDR*</span></span>

<span data-ttu-id="c3598-124">*Amplia*</span><span class="sxs-lookup"><span data-stu-id="c3598-124">*Wildcard*</span></span>

<span data-ttu-id="c3598-125">*Específicas*</span><span class="sxs-lookup"><span data-stu-id="c3598-125">*Specific*</span></span>

<span data-ttu-id="c3598-126">*Amplia*</span><span class="sxs-lookup"><span data-stu-id="c3598-126">*Wildcard*</span></span>

<span data-ttu-id="c3598-127">*Específicas*</span><span class="sxs-lookup"><span data-stu-id="c3598-127">*Specific*</span></span>

<span data-ttu-id="c3598-128">$ {ROWSPAN3} $*so \_ EXCLUSIVEADDRUSE*$ {remove} $</span><span class="sxs-lookup"><span data-stu-id="c3598-128">${ROWSPAN3}$*SO\_EXCLUSIVEADDRUSE*${REMOVE}$</span></span>  

<span data-ttu-id="c3598-129">*Amplia*</span><span class="sxs-lookup"><span data-stu-id="c3598-129">*Wildcard*</span></span>

<span data-ttu-id="c3598-130">Falha (10048)</span><span class="sxs-lookup"><span data-stu-id="c3598-130">Fail (10048)</span></span>

<span data-ttu-id="c3598-131">Falha (10048)</span><span class="sxs-lookup"><span data-stu-id="c3598-131">Fail (10048)</span></span>

<span data-ttu-id="c3598-132">Falha (10048)</span><span class="sxs-lookup"><span data-stu-id="c3598-132">Fail (10048)</span></span>

<span data-ttu-id="c3598-133">Falha (10048)</span><span class="sxs-lookup"><span data-stu-id="c3598-133">Fail (10048)</span></span>

<span data-ttu-id="c3598-134">*Específicas*</span><span class="sxs-lookup"><span data-stu-id="c3598-134">*Specific*</span></span>

<span data-ttu-id="c3598-135">Falha (10048)</span><span class="sxs-lookup"><span data-stu-id="c3598-135">Fail (10048)</span></span>

<span data-ttu-id="c3598-136">Falha (10048)</span><span class="sxs-lookup"><span data-stu-id="c3598-136">Fail (10048)</span></span>

<span data-ttu-id="c3598-137">Falha (10048)</span><span class="sxs-lookup"><span data-stu-id="c3598-137">Fail (10048)</span></span>

<span data-ttu-id="c3598-138">Falha (10048)</span><span class="sxs-lookup"><span data-stu-id="c3598-138">Fail (10048)</span></span>

<span data-ttu-id="c3598-139">*Specific2*</span><span class="sxs-lookup"><span data-stu-id="c3598-139">*Specific2*</span></span>

<span data-ttu-id="c3598-140">N/D</span><span class="sxs-lookup"><span data-stu-id="c3598-140">n/a</span></span>

<span data-ttu-id="c3598-141">Êxito</span><span class="sxs-lookup"><span data-stu-id="c3598-141">Success</span></span>

<span data-ttu-id="c3598-142">N/D</span><span class="sxs-lookup"><span data-stu-id="c3598-142">n/a</span></span>

<span data-ttu-id="c3598-143">Êxito</span><span class="sxs-lookup"><span data-stu-id="c3598-143">Success</span></span>

<span data-ttu-id="c3598-144">$ {ROWSPAN3} $*sem opções*$ {remover} $</span><span class="sxs-lookup"><span data-stu-id="c3598-144">${ROWSPAN3}$*No options*${REMOVE}$</span></span>  

<span data-ttu-id="c3598-145">*Amplia*</span><span class="sxs-lookup"><span data-stu-id="c3598-145">*Wildcard*</span></span>

<span data-ttu-id="c3598-146">Falha (10048)</span><span class="sxs-lookup"><span data-stu-id="c3598-146">Fail (10048)</span></span>

<span data-ttu-id="c3598-147">Falha (10048)</span><span class="sxs-lookup"><span data-stu-id="c3598-147">Fail (10048)</span></span>

<span data-ttu-id="c3598-148">Falha (10048)</span><span class="sxs-lookup"><span data-stu-id="c3598-148">Fail (10048)</span></span>

<span data-ttu-id="c3598-149">Falha (10048)</span><span class="sxs-lookup"><span data-stu-id="c3598-149">Fail (10048)</span></span>

<span data-ttu-id="c3598-150">*Específicas*</span><span class="sxs-lookup"><span data-stu-id="c3598-150">*Specific*</span></span>

<span data-ttu-id="c3598-151">Falha (10048)</span><span class="sxs-lookup"><span data-stu-id="c3598-151">Fail (10048)</span></span>

<span data-ttu-id="c3598-152">Falha (10048)</span><span class="sxs-lookup"><span data-stu-id="c3598-152">Fail (10048)</span></span>

<span data-ttu-id="c3598-153">Falha (10048)</span><span class="sxs-lookup"><span data-stu-id="c3598-153">Fail (10048)</span></span>

<span data-ttu-id="c3598-154">Falha (10048)</span><span class="sxs-lookup"><span data-stu-id="c3598-154">Fail (10048)</span></span>

<span data-ttu-id="c3598-155">*Specific2*</span><span class="sxs-lookup"><span data-stu-id="c3598-155">*Specific2*</span></span>

<span data-ttu-id="c3598-156">N/D</span><span class="sxs-lookup"><span data-stu-id="c3598-156">n/a</span></span>

<span data-ttu-id="c3598-157">Êxito</span><span class="sxs-lookup"><span data-stu-id="c3598-157">Success</span></span>

<span data-ttu-id="c3598-158">N/D</span><span class="sxs-lookup"><span data-stu-id="c3598-158">n/a</span></span>

<span data-ttu-id="c3598-159">Êxito</span><span class="sxs-lookup"><span data-stu-id="c3598-159">Success</span></span>

<span data-ttu-id="c3598-160">$ {ROWSPAN3} $*so \_ REUSEADDR*$ {remove} $</span><span class="sxs-lookup"><span data-stu-id="c3598-160">${ROWSPAN3}$*SO\_REUSEADDR*${REMOVE}$</span></span>  

<span data-ttu-id="c3598-161">*Amplia*</span><span class="sxs-lookup"><span data-stu-id="c3598-161">*Wildcard*</span></span>

<span data-ttu-id="c3598-162">Falha (10013)</span><span class="sxs-lookup"><span data-stu-id="c3598-162">Fail (10013)</span></span>

<span data-ttu-id="c3598-163">Falha (10013)</span><span class="sxs-lookup"><span data-stu-id="c3598-163">Fail (10013)</span></span>

<span data-ttu-id="c3598-164">Êxito\*</span><span class="sxs-lookup"><span data-stu-id="c3598-164">Success\*</span></span>

<span data-ttu-id="c3598-165">Êxito</span><span class="sxs-lookup"><span data-stu-id="c3598-165">Success</span></span>

<span data-ttu-id="c3598-166">*Específicas*</span><span class="sxs-lookup"><span data-stu-id="c3598-166">*Specific*</span></span>

<span data-ttu-id="c3598-167">Falha (10013)</span><span class="sxs-lookup"><span data-stu-id="c3598-167">Fail (10013)</span></span>

<span data-ttu-id="c3598-168">Falha (10013)</span><span class="sxs-lookup"><span data-stu-id="c3598-168">Fail (10013)</span></span>

<span data-ttu-id="c3598-169">Êxito</span><span class="sxs-lookup"><span data-stu-id="c3598-169">Success</span></span>

<span data-ttu-id="c3598-170">Êxito\*</span><span class="sxs-lookup"><span data-stu-id="c3598-170">Success\*</span></span>

<span data-ttu-id="c3598-171">*Specific2*</span><span class="sxs-lookup"><span data-stu-id="c3598-171">*Specific2*</span></span>

<span data-ttu-id="c3598-172">N/D</span><span class="sxs-lookup"><span data-stu-id="c3598-172">n/a</span></span>

<span data-ttu-id="c3598-173">Êxito</span><span class="sxs-lookup"><span data-stu-id="c3598-173">Success</span></span>

<span data-ttu-id="c3598-174">N/D</span><span class="sxs-lookup"><span data-stu-id="c3598-174">n/a</span></span>

<span data-ttu-id="c3598-175">Êxito</span><span class="sxs-lookup"><span data-stu-id="c3598-175">Success</span></span>

<span data-ttu-id="c3598-176">\* O comportamento é indefinido para qual soquete receberá pacotes.</span><span class="sxs-lookup"><span data-stu-id="c3598-176">\* The behavior is undefined as to which socket will receive packets.</span></span>



 

<span data-ttu-id="c3598-177">No caso em que a primeira ligação não define nenhuma opção ou tão \_ REUSEADDR, e a segunda ligação executa um \_ REUSEADDR, o segundo soquete excedeu a porta e o comportamento em relação ao qual o soquete receberá os pacotes que serão indeterminados.</span><span class="sxs-lookup"><span data-stu-id="c3598-177">In the case where the first bind sets no options or SO\_REUSEADDR, and the second bind performs a SO\_REUSEADDR, the second socket has overtaken the port and behavior regarding which socket will receive packets is undetermined.</span></span> <span data-ttu-id="c3598-178">Portanto, \_ o EXCLUSIVEADDRUSE foi introduzido para resolver essa situação.</span><span class="sxs-lookup"><span data-stu-id="c3598-178">SO\_EXCLUSIVEADDRUSE was introduced to address this situation.</span></span>

<span data-ttu-id="c3598-179">Um soquete com o \_ EXCLUSIVEADDRUSE set não pode ser sempre reutilizado imediatamente após o fechamento do soquete.</span><span class="sxs-lookup"><span data-stu-id="c3598-179">A socket with SO\_EXCLUSIVEADDRUSE set cannot always be reused immediately after socket closure.</span></span> <span data-ttu-id="c3598-180">Por exemplo, se um soquete de escuta com o sinalizador exclusivo definido aceitar uma conexão após a qual o soquete de escuta está fechado, outro Soquete não poderá se associar à mesma porta que o primeiro soquete de escuta com o sinalizador exclusivo até que a conexão aceita não esteja mais ativa.</span><span class="sxs-lookup"><span data-stu-id="c3598-180">For example, if a listening socket with the exclusive flag set accepts a connection after which the listening socket is closed, another socket cannot bind to the same port as the first listening socket with the exclusive flag until the accepted connection is no longer active.</span></span>

<span data-ttu-id="c3598-181">Essa situação pode ser bastante complicada; Embora o soquete tenha sido fechado, o transporte subjacente pode não encerrar sua conexão.</span><span class="sxs-lookup"><span data-stu-id="c3598-181">This situation can be quite complicated; even though the socket has been closed, the underlying transport may not terminate its connection.</span></span> <span data-ttu-id="c3598-182">Mesmo após o soquete ser fechado, o sistema deve enviar todos os dados armazenados em buffer, transmitir uma desconexão normal para o par e aguardar uma desconexão normal do par.</span><span class="sxs-lookup"><span data-stu-id="c3598-182">Even after the socket is closed, the system must send all of the buffered data, transmit a graceful disconnect to the peer, and wait for a graceful disconnect from the peer.</span></span> <span data-ttu-id="c3598-183">Portanto, é possível que o transporte subjacente nunca libere a conexão, como quando o mesmo anuncia uma janela de tamanho zero ou outros ataques.</span><span class="sxs-lookup"><span data-stu-id="c3598-183">It is therefore possible that the underlying transport may never release the connection, such as when the peer advertises a zero-size window, or other such attacks.</span></span> <span data-ttu-id="c3598-184">No exemplo anterior, o soquete de escuta foi fechado após a aceitação de uma conexão de cliente.</span><span class="sxs-lookup"><span data-stu-id="c3598-184">In the previous example, the listening socket was closed after a client connection was accepted.</span></span> <span data-ttu-id="c3598-185">Agora, mesmo que a conexão do cliente seja fechada, a porta ainda poderá não ser reutilizada se a conexão do cliente permanecer em um estado ativo devido a dados não confirmados e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="c3598-185">Now even if the client connection is closed, the port still may not be reused if the client connection remains in an active state because of unacknowledged data, and so forth.</span></span>

<span data-ttu-id="c3598-186">Para evitar essa situação, os aplicativos devem garantir um desligamento normal: chamar o [**desligamento**](/windows/desktop/api/winsock/nf-winsock-shutdown) com o sinalizador de envio de SD \_ e esperar em um loop de [**recepção**](/windows/desktop/api/winsock/nf-winsock-recv) até que zero bytes sejam retornados.</span><span class="sxs-lookup"><span data-stu-id="c3598-186">To avoid this situation, applications should ensure a graceful shutdown: call [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) with the SD\_SEND flag, then wait in a [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) loop until zero bytes are returned.</span></span> <span data-ttu-id="c3598-187">Isso evita o problema associado à reutilização da porta, garante que todos os dados foram recebidos pelo par e garante o ponto em que todos os seus dados foram recebidos com êxito.</span><span class="sxs-lookup"><span data-stu-id="c3598-187">Doing so avoids the problem associated with port reuse, guarantees all data was received by the peer, and assures the peer that all its data was successfully received.</span></span>

<span data-ttu-id="c3598-188">A opção de modo \_ remanescente pode ser definida em um soquete para impedir que a porta esteja entrando em um dos Estados de espera ativos; no entanto, isso não é recomendável porque pode levar a efeitos indesejados, pois pode fazer com que a conexão seja redefinida.</span><span class="sxs-lookup"><span data-stu-id="c3598-188">The SO\_LINGER option may be set on a socket to prevent the port going into one of the active wait states; however, doing so is discouraged because it can lead to undesired effects, because it can cause the connection to be reset.</span></span> <span data-ttu-id="c3598-189">Por exemplo, se os dados tiverem sido recebidos, mas ainda não confirmados pelo par, e o computador local fechar o soquete com o \_ conjunto remanescente, a conexão será redefinida e o par descartará os dados não confirmados.</span><span class="sxs-lookup"><span data-stu-id="c3598-189">For example, if data has been received but not yet acknowledged by the peer, and the local computer closes the socket with SO\_LINGER set, the connection is reset and the peer discards the unacknowledged data.</span></span> <span data-ttu-id="c3598-190">Além disso, é difícil escolher um horário adequado para o remanescente; um valor muito pequeno resulta em muitas conexões anuladas, enquanto um tempo limite grande pode deixar o sistema vulnerável a ataques de negação de serviço estabelecendo muitas conexões e, assim, paralisando vários threads de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c3598-190">Also, picking a suitable time to linger is difficult; a value too small results in many aborted connections, while a large timeout can leave the system vulnerable to denial of service attacks by establishing many connections, and thereby stalling numerous application threads.</span></span>

> [!Note]  
> <span data-ttu-id="c3598-191">Um soquete que está usando a \_ opção EXCLUSIVEADDRUSE deve ser desligado corretamente antes de fechá-lo.</span><span class="sxs-lookup"><span data-stu-id="c3598-191">A socket that is using the SO\_EXCLUSIVEADDRUSE option must be shut down properly prior to closing it.</span></span> <span data-ttu-id="c3598-192">A falha em fazer isso pode causar um ataque de negação de serviço se o serviço associado precisar ser reiniciado.</span><span class="sxs-lookup"><span data-stu-id="c3598-192">Failure to do so can cause a denial of service attack if the associated service needs to restart.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c3598-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3598-193">Requirements</span></span>



| <span data-ttu-id="c3598-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3598-194">Requirement</span></span> | <span data-ttu-id="c3598-195">Valor</span><span class="sxs-lookup"><span data-stu-id="c3598-195">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3598-196">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3598-196">Minimum supported client</span></span><br/> | <span data-ttu-id="c3598-197">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c3598-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c3598-198">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3598-198">Minimum supported server</span></span><br/> | <span data-ttu-id="c3598-199">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c3598-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c3598-200">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c3598-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3598-201"><dt>Winsock2. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3598-201"><dt>Winsock2.h</dt></span></span> </dl> |



 

 




