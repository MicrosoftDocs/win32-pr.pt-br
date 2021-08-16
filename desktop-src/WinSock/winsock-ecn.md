---
title: Notificação de congestionamento explícito do Winsock (ECN)
description: Alguns aplicativos e/ou protocolos baseados no protocolo UDP (por exemplo, QUIC) buscam aproveitar o uso de pontos de código de ECN (notificação de congestionamento explícito) para melhorar a latência e a tremibilidade em redes com congestionamento.
ms.topic: article
ms.date: 11/13/2020
ms.openlocfilehash: 79b38611cd0301d0b5d301592eec02b68c02353246c67a6c94528417623834f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322019"
---
# <a name="winsock-explicit-congestion-notification-ecn"></a>Notificação de congestionamento explícito do Winsock (ECN)

## <a name="introduction"></a>Introdução

Alguns aplicativos e/ou protocolos baseados no protocolo UDP (por exemplo, QUIC) buscam aproveitar o uso de pontos de código de ECN (notificação de congestionamento explícito) para melhorar a latência e a tremibilidade em redes com congestionamento.

As APIs winsock ECN estendem a interface **getsockopt** setsockopt, bem como a interface de mensagem de controle /  &mdash; [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) / [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) com suporte para modificar e receber pontos de código ECN em &mdash; títulos IP. A funcionalidade fornecida permite obter e definir pontos de código ECN por pacote.

Para obter mais informações sobre eCN, consulte [Adição de ECN (Notificação de Congestionamento Explícita) ao IP](https://tools.ietf.org/html/rfc3168).

Seu aplicativo não tem permissão para especificar o ponto de código DE (Congestionamento Encontrado) ao enviar datagramas. O envio retornará com o **erro WSAEINVAL.**

## <a name="query-ecn-with-wsagetrecvipecn"></a>Consultar ECN com WSAGetRecvIPEcn

[**WSAGetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn) é uma função em linha, definida em `ws2tcpip.h` .

Chame **WSAGetRecvIPEcn** para consultar **a** habilitação atual de recebimento da mensagem de controle **IP_ECN (ou IPV6_ECN**) por meio de LPFN_WSARECVMSG [**(WSARecvMsg).**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)

Consulte também a [**estrutura WSAMSG.**](/windows/win32/api/ws2def/ns-ws2def-wsamsg)

- **Protocolo**: IPv4
- **Cmsg_level**: IPPROTO_IP
- **Cmsg_type:** IP_ECN (50 decimal)
- **Descrição:** especifica/recebe o ponto de código ECN no campo de header IPv4 do Tipo de Serviço (TOS).

- **Protocolo**: IPv6
- **Cmsg_level**: IPPROTO_IPV6
- **Cmsg_type:** IPV6_ECN (50 decimal)
- **Descrição:** especifica/recebe o ponto de código ECN no campo de header IPv6 da Classe de Tráfego.

## <a name="specify-ecn-with-wsasetrecvipecn"></a>Especificar ECN com WSASetRecvIPEcn

[**WSASetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn) é uma função em linha, definida em `ws2tcpip.h` .

Chame **WSASetRecvIPEcn** para especificar se a pilha ip deve preencher o buffer de controle com uma mensagem que contém o ponto de código ECN do campo de título Tipo de Serviço IPv4 (ou campo de título IPv6 da Classe de Tráfego) em um datagrama recebido. Quando definida como `TRUE` , a função LPFN_WSARECVMSG [**(WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) retorna dados de controle opcionais que contêm o ponto de código ECN do datagrama recebido. O tipo de mensagem de controle retornado **será IP_ECN** **(ou IPV6_ECN**) com nível **IPPROTO_IP** **(ou IPPROTO_IPV6**). Os dados da mensagem de controle são retornados como **um INT**. Essa opção é válida somente em soquetes de datagrama (o tipo de **soquete** deve ser SOCK_DGRAM ).

## <a name="code-example-1mdashapplication-advertising-ecn-support"></a>Exemplo de código 1 &mdash; aplicativo anunciando suporte a ECN

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

## <a name="code-example-2mdashapplication-detecting-congestion"></a>Exemplo de código 2 &mdash; aplicativo detectando congestionamento

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

## <a name="see-also"></a>Confira também

* [WSAGetRecvIPEcn](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn)
* [WSASetRecvIPEcn](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn)
