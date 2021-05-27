---
title: Notificação de congestionamento explícita do Winsock (ECN)
description: Alguns aplicativos e/ou protocolos baseados no protocolo UDP (por exemplo, QUIC) buscam aproveitar o uso de pontos de código ECN (notificação de congestionamento explícito) para melhorar a latência e a tremibilidade em redes com congestionamento.
ms.topic: article
ms.date: 11/13/2020
ms.openlocfilehash: 090ac9b0575cb491aa6d726e7507223156460ace
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110559930"
---
# <a name="winsock-explicit-congestion-notification-ecn"></a><span data-ttu-id="623f3-103">Notificação de congestionamento explícita do Winsock (ECN)</span><span class="sxs-lookup"><span data-stu-id="623f3-103">Winsock explicit congestion notification (ECN)</span></span>

## <a name="introduction"></a><span data-ttu-id="623f3-104">Introdução</span><span class="sxs-lookup"><span data-stu-id="623f3-104">Introduction</span></span>

<span data-ttu-id="623f3-105">Alguns aplicativos e/ou protocolos baseados no protocolo UDP (por exemplo, QUIC) buscam aproveitar o uso de pontos de código ECN (notificação de congestionamento explícito) para melhorar a latência e a tremibilidade em redes com congestionamento.</span><span class="sxs-lookup"><span data-stu-id="623f3-105">Some applications and/or protocols that are based on the User Datagram Protocol (UDP) (for example, QUIC) seek to leverage the use of explicit congestion notification (ECN) codepoints in order to improve latency and jitter in congested networks.</span></span>

<span data-ttu-id="623f3-106">As APIs winsock ECN estendem a interface **getsockopt** setsockopt, bem como a interface de mensagem de controle /  &mdash; [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) / [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) com suporte para modificar e receber pontos de código ECN em &mdash; títulos IP.</span><span class="sxs-lookup"><span data-stu-id="623f3-106">The Winsock ECN APIs extend the **getsockopt**/**setsockopt** interface&mdash;as well as the [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg)/[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) control message interface&mdash;with support for modifying and receiving ECN codepoints in IP headers.</span></span> <span data-ttu-id="623f3-107">A funcionalidade fornecida permite obter e definir pontos de código ECN por pacote.</span><span class="sxs-lookup"><span data-stu-id="623f3-107">The functionality provided allows you to get and set ECN codepoints on a per-packet basis.</span></span>

<span data-ttu-id="623f3-108">Para obter mais informações sobre ECN, consulte [Adição de ECN (Notificação de Congestionamento Explícita) ao IP](https://tools.ietf.org/html/rfc3168).</span><span class="sxs-lookup"><span data-stu-id="623f3-108">For more information regarding ECN, see [The Addition of Explicit Congestion Notification (ECN) to IP](https://tools.ietf.org/html/rfc3168).</span></span>

<span data-ttu-id="623f3-109">Seu aplicativo não tem permissão para especificar o ponto de código DE (Congestionamento Encontrado) ao enviar datagramas.</span><span class="sxs-lookup"><span data-stu-id="623f3-109">Your application isn't allowed to specify the Congestion Encountered (CE) code point when sending datagrams.</span></span> <span data-ttu-id="623f3-110">O envio retornará com o **erro WSAEINVAL.**</span><span class="sxs-lookup"><span data-stu-id="623f3-110">The send will return with error **WSAEINVAL**.</span></span>

## <a name="query-ecn-with-wsagetrecvipecn"></a><span data-ttu-id="623f3-111">Consultar ECN com WSAGetRecvIPEcn</span><span class="sxs-lookup"><span data-stu-id="623f3-111">Query ECN with WSAGetRecvIPEcn</span></span>

<span data-ttu-id="623f3-112">[**WSAGetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn) é uma função em linha, definida em `ws2tcpip.h` .</span><span class="sxs-lookup"><span data-stu-id="623f3-112">[**WSAGetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn) is an inline function, defined in `ws2tcpip.h`.</span></span>

<span data-ttu-id="623f3-113">Chame **WSAGetRecvIPEcn** para consultar **a** habilitação atual de recebimento da mensagem de controle **IP_ECN (ou IPV6_ECN**) por meio de LPFN_WSARECVMSG [**(WSARecvMsg).**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)</span><span class="sxs-lookup"><span data-stu-id="623f3-113">Call **WSAGetRecvIPEcn** to query the current enablement of receiving the **IP_ECN** (or **IPV6_ECN**) control message via [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg).</span></span>

<span data-ttu-id="623f3-114">Consulte também a [**estrutura WSAMSG.**](/windows/win32/api/ws2def/ns-ws2def-wsamsg)</span><span class="sxs-lookup"><span data-stu-id="623f3-114">Also see the [**WSAMSG**](/windows/win32/api/ws2def/ns-ws2def-wsamsg) structure.</span></span>

- <span data-ttu-id="623f3-115">**Protocolo**: IPv4</span><span class="sxs-lookup"><span data-stu-id="623f3-115">**Protocol**: IPv4</span></span>
- <span data-ttu-id="623f3-116">**Cmsg_level**: IPPROTO_IP</span><span class="sxs-lookup"><span data-stu-id="623f3-116">**Cmsg_level**: IPPROTO_IP</span></span>
- <span data-ttu-id="623f3-117">**Cmsg_type:** IP_ECN (50 decimal)</span><span class="sxs-lookup"><span data-stu-id="623f3-117">**Cmsg_type**: IP_ECN (50 decimal)</span></span>
- <span data-ttu-id="623f3-118">**Descrição:** especifica/recebe o ponto de código ECN no campo de header IPv4 do Tipo de Serviço (TOS).</span><span class="sxs-lookup"><span data-stu-id="623f3-118">**Description**: Specifies/receives ECN codepoint in the Type of Service (TOS) IPv4 header field.</span></span>

- <span data-ttu-id="623f3-119">**Protocolo**: IPv6</span><span class="sxs-lookup"><span data-stu-id="623f3-119">**Protocol**: IPv6</span></span>
- <span data-ttu-id="623f3-120">**Cmsg_level**: IPPROTO_IPV6</span><span class="sxs-lookup"><span data-stu-id="623f3-120">**Cmsg_level**: IPPROTO_IPV6</span></span>
- <span data-ttu-id="623f3-121">**Cmsg_type:** IPV6_ECN (50 decimal)</span><span class="sxs-lookup"><span data-stu-id="623f3-121">**Cmsg_type**: IPV6_ECN (50 decimal)</span></span>
- <span data-ttu-id="623f3-122">**Descrição**: especifica/recebe o ECN ponto no campo de cabeçalho IPv6 da classe de tráfego.</span><span class="sxs-lookup"><span data-stu-id="623f3-122">**Description**: Specifies/receives ECN codepoint in the Traffic Class IPv6 header field.</span></span>

## <a name="specify-ecn-with-wsasetrecvipecn"></a><span data-ttu-id="623f3-123">Especificar ECN com WSASetRecvIPEcn</span><span class="sxs-lookup"><span data-stu-id="623f3-123">Specify ECN with WSASetRecvIPEcn</span></span>

<span data-ttu-id="623f3-124">[**WSASetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn) é uma função embutida, definida em `ws2tcpip.h` .</span><span class="sxs-lookup"><span data-stu-id="623f3-124">[**WSASetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn) is an inline function, defined in `ws2tcpip.h`.</span></span>

<span data-ttu-id="623f3-125">Chame **WSASetRecvIPEcn** para especificar se a pilha de IP deve preencher o buffer de controle com uma mensagem contendo o ECN ponto do tipo de campo de cabeçalho IPv4 de serviço (ou campo de cabeçalho IPv6 de classe de tráfego) em um datagrama recebido.</span><span class="sxs-lookup"><span data-stu-id="623f3-125">Call **WSASetRecvIPEcn** to specify whether the IP stack should populate the control buffer with a message containing the ECN codepoint of the Type of Service IPv4 header field (or Traffic Class IPv6 header field) on a received datagram.</span></span> <span data-ttu-id="623f3-126">Quando definido como `TRUE` , a função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) retorna dados de controle opcionais contendo o ponto ECN do datagrama recebido.</span><span class="sxs-lookup"><span data-stu-id="623f3-126">When set to `TRUE`, the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function returns optional control data containing the ECN codepoint of the received datagram.</span></span> <span data-ttu-id="623f3-127">O tipo de mensagem de controle retornado será **IP_ECN** (ou **IPV6_ECN**) com o nível **IPPROTO_IP** (ou **IPPROTO_IPV6**).</span><span class="sxs-lookup"><span data-stu-id="623f3-127">The returned control message type will be **IP_ECN** (or **IPV6_ECN**) with level **IPPROTO_IP** (or **IPPROTO_IPV6**).</span></span> <span data-ttu-id="623f3-128">Os dados da mensagem de controle são retornados como um **int**.</span><span class="sxs-lookup"><span data-stu-id="623f3-128">The control message data is returned as an **INT**.</span></span> <span data-ttu-id="623f3-129">Essa opção só é válida em soquetes de datagrama (o tipo de soquete deve ser **SOCK_DGRAM**).</span><span class="sxs-lookup"><span data-stu-id="623f3-129">This option is valid only on datagram sockets (the socket type must be **SOCK_DGRAM**).</span></span>

## <a name="code-example-1mdashapplication-advertising-ecn-support"></a><span data-ttu-id="623f3-130">Exemplo de código 1 &mdash; anúncio de aplicativo com suporte a ECN</span><span class="sxs-lookup"><span data-stu-id="623f3-130">Code example 1&mdash;application advertising ECN support</span></span>

```cpp
#define ECN_ECT_0 2

void sendEcn(SOCKET sock, PSOCKADDR_STORAGE addr, LPFN_WSASENDMSG sendmsg, PCHAR data, INT datalen)
{
    DWORD numBytes;
    INT error;

    CHAR control[WSA_CMSG_SPACE(sizeof(INT))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    PCMSGHDR cmsg;

    dataBuf.buf = data;
    dataBuf.len = datalen;
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = (PSOCKADDR)addr;
    wsaMsg.namelen = (INT)INET_SOCKADDR_LENGTH(addr->ss_family);
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    cmsg->cmsg_len = WSA_CMSG_LEN(sizeof(INT));
    cmsg->cmsg_level = (addr->ss_family == AF_INET) ? IPPROTO_IP : IPPROTO_IPV6;
    cmsg->cmsg_type = (addr->ss_family == AF_INET) ? IP_ECN : IPV6_ECN;
    *(PINT)WSA_CMSG_DATA(cmsg) = ECN_ECT_0;

    error =
        sendmsg(
            sock,
            &wsaMsg,
            0,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("sendmsg failed %d\n", WSAGetLastError());
    }
}
```

## <a name="code-example-2mdashapplication-detecting-congestion"></a><span data-ttu-id="623f3-131">Exemplo de código 2 &mdash; aplicativo de detecção de congestionamento</span><span class="sxs-lookup"><span data-stu-id="623f3-131">Code example 2&mdash;application detecting congestion</span></span>

```cpp
#define ECN_ECT_CE 3

int recvEcn(SOCKET sock, PSOCKADDR_STORAGE addr, LPFN_WSARECVMSG recvmsg, PCHAR data, INT datalen, PBOOLEAN congestionEncountered)
{
    DWORD numBytes;
    INT error;
    INT ecnVal;
    SOCKADDR_STORAGE remoteAddr = { 0 };

    CHAR control[WSA_CMSG_SPACE(sizeof(INT))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    PCMSGHDR cmsg;

    dataBuf.buf = data;
    dataBuf.len = datalen;
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = (PSOCKADDR)&remoteAddr;
    wsaMsg.namelen = sizeof(remoteAddr);
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    *congestionEncountered = FALSE;

    error =
        recvmsg(
            sock,
            &wsaMsg,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("recvmsg failed %d\n", WSAGetLastError());
        return -1;
    }

    cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    while (cmsg != NULL) {
        if ((cmsg->cmsg_level == IPPROTO_IP && cmsg->cmsg_type == IP_ECN) ||
            (cmsg->cmsg_level == IPPROTO_IPV6 && cmsg->cmsg_type == IPV6_ECN)) {
            ecnVal = *(PINT)WSA_CMSG_DATA(cmsg);
            if (ecnVal == ECN_ECT_CE) {
                *congestionEncountered = TRUE;
            }
            break;
        }
        cmsg = WSA_CMSG_NXTHDR(&wsaMsg, cmsg);
    }

    return numBytes;
}

void receiver(SOCKET sock, PSOCKADDR_STORAGE addr, LPFN_WSARECVMSG recvmsg)
{
    DWORD numBytes;
    INT error;
    DWORD enabled;
    CHAR data[512];
    BOOLEAN congestionEncountered;

    error = bind(sock, (PSOCKADDR)addr, sizeof(*addr));
    if (error == SOCKET_ERROR) {
        printf("bind failed %d\n", WSAGetLastError());
        return;
    }

    enabled = TRUE;
    error = WSASetRecvIPEcn(sock, enabled);
    if (error == SOCKET_ERROR) {
        printf(" WSASetRecvIPEcn failed %d\n", WSAGetLastError());
        return;
    }

    do {
        numBytes = recvEcn(sock, addr, recvmsg, data, sizeof(data), &congestionEncountered);
        if (congestionEncountered) {
            // Tell sender to slow down
        }
    } while (numBytes > 0);
}
```

## <a name="see-also"></a><span data-ttu-id="623f3-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="623f3-132">See also</span></span>

* [<span data-ttu-id="623f3-133">WSAGetRecvIPEcn</span><span class="sxs-lookup"><span data-stu-id="623f3-133">WSAGetRecvIPEcn</span></span>](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn)
* [<span data-ttu-id="623f3-134">WSASetRecvIPEcn</span><span class="sxs-lookup"><span data-stu-id="623f3-134">WSASetRecvIPEcn</span></span>](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn)
