---
description: O código a seguir demonstra as funções recv e Send usadas pelo servidor.
ms.assetid: 26990b06-196a-4fb1-92d8-c5fa096d2b09
title: Recebendo e enviando dados no servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f943fe9f1c4045c087b31861bc6db5f1eb394ad800ee0133e0ec8fb668fcbe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857846"
---
# <a name="receiving-and-sending-data-on-the-server"></a>Recebendo e enviando dados no servidor

O código a seguir demonstra as funções [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) e [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) usadas pelo servidor.

### <a name="to-receive-and-send-data-on-a-socket"></a>Para receber e enviar dados em um soquete


```C++
#define DEFAULT_BUFLEN 512

char recvbuf[DEFAULT_BUFLEN];
int iResult, iSendResult;
int recvbuflen = DEFAULT_BUFLEN;

// Receive until the peer shuts down the connection
do {

    iResult = recv(ClientSocket, recvbuf, recvbuflen, 0);
    if (iResult > 0) {
        printf("Bytes received: %d\n", iResult);

        // Echo the buffer back to the sender
        iSendResult = send(ClientSocket, recvbuf, iResult, 0);
        if (iSendResult == SOCKET_ERROR) {
            printf("send failed: %d\n", WSAGetLastError());
            closesocket(ClientSocket);
            WSACleanup();
            return 1;
        }
        printf("Bytes sent: %d\n", iSendResult);
    } else if (iResult == 0)
        printf("Connection closing...\n");
    else {
        printf("recv failed: %d\n", WSAGetLastError());
        closesocket(ClientSocket);
        WSACleanup();
        return 1;
    }

} while (iResult > 0);
```



As funções [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) e [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) retornam um valor inteiro do número de bytes enviados ou recebidos, respectivamente ou um erro. Cada função também usa os mesmos parâmetros: o soquete ativo, um buffer de **caracteres** , o número de bytes a serem enviados ou recebidos e os sinalizadores a serem usados.

Próxima etapa: [desconectando o servidor](disconnecting-the-server.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com o Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Aplicativo de servidor Winsock](winsock-server-application.md)
</dt> <dt>

[Aceitando uma conexão](accepting-a-connection.md)
</dt> </dl>

 

 



