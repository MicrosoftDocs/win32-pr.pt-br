---
description: Depois que o soquete for vinculado a um endereço IP e porta no sistema, o servidor deverá escutar esse endereço IP e a porta para solicitações de conexão de entrada.
ms.assetid: 83c9f0e7-2e6d-449b-8d97-3d13154112cd
title: Escutando em um soquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d6d98a13fc6e994fb5a264827b6b93047fd24e03d3e3f9953203b1fa15140f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569776"
---
# <a name="listening-on-a-socket"></a>Escutando em um soquete

Depois que o soquete for vinculado a um endereço IP e porta no sistema, o servidor deverá escutar esse endereço IP e a porta para solicitações de conexão de entrada.

## <a name="to-listen-on-a-socket"></a>Para escutar em um soquete

Chame a [**função listen,**](/windows/desktop/api/Winsock2/nf-winsock2-listen) passando como parâmetros o soquete criado e um valor para a lista de pendências *,* comprimento máximo da fila de conexões pendentes a aceitar. Neste exemplo, o parâmetro *da pendência* foi definido como **SOMAXCONN.** Esse valor é uma constante especial que instrui o provedor Winsock para esse soquete a permitir um número máximo razoável de conexões pendentes na fila. Verifique se há erros gerais no valor de retorno.


```C++
if ( listen( ListenSocket, SOMAXCONN ) == SOCKET_ERROR ) {
    printf( "Listen failed with error: %ld\n", WSAGetLastError() );
    closesocket(ListenSocket);
    WSACleanup();
    return 1;
}
```



Próxima etapa: [aceitar uma conexão](accepting-a-connection.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ponto de Partida com Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Aplicativo Winsock Server](winsock-server-application.md)
</dt> <dt>

[Associação de um soquete](binding-a-socket.md)
</dt> </dl>

 

 



