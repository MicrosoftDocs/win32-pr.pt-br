---
description: O erro de soquete constante de manifesto \_ é fornecido para verificar a falha da função. Embora o uso dessa constante não seja obrigatório, é recomendável. O exemplo a seguir ilustra o uso da constante de erro de soquete \_ .
ms.assetid: b46203dc-5666-413b-90fe-8432318f3037
title: Valores de retorno em falha de função
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b277da114c8c86c53339590eeff3e831cbaf2a4277765bf53047b3d07991b026
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740928"
---
# <a name="return-values-on-function-failure"></a>Valores de retorno em falha de função

O erro de **soquete \_** constante de manifesto é fornecido para verificar a falha da função. Embora o uso dessa constante não seja obrigatório, é recomendável. O exemplo a seguir ilustra o uso da constante de **\_ erro de soquete** .

Estilo BSD típico (não funcionará em Windows)


```C++
        r = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (r == -1     /* or r < 0 */
            && errno == EWOULDBLOCK) {
            printf("recv failed with error: EWOULDBLOCK\n");
        }    
```



Windows Estilo


```C++
        iResult = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (iResult == SOCKET_ERROR ) {
            iError = WSAGetLastError();
            if (iError == WSAEWOULDBLOCK)
                printf("recv failed with error: WSAEWOULDBLOCK\n");
            else
                printf("recv failed with error: %ld\n", iError);

            closesocket(ClientSocket);
            WSACleanup();
            return 1;
        }    
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Códigos de erro-errno, h \_ errno e WSAGetLastError](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
</dt> <dt>

[Manipulando erros do Winsock](handling-winsock-errors.md)
</dt> <dt>

[Portando aplicativos de soquete para Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Considerações sobre programação do Winsock](winsock-programming-considerations.md)
</dt> <dt>

[Windows Códigos de erro de soquetes](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



