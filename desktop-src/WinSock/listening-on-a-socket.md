---
description: Depois que o soquete estiver associado a um endereço IP e a uma porta no sistema, o servidor deverá escutar nesse endereço IP e na porta para solicitações de conexão de entrada.
ms.assetid: 83c9f0e7-2e6d-449b-8d97-3d13154112cd
title: Ouvindo em um soquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c36fe1718493d1b92ca52bb3c648ebd1aa5b0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781219"
---
# <a name="listening-on-a-socket"></a>Ouvindo em um soquete

Depois que o soquete estiver associado a um endereço IP e a uma porta no sistema, o servidor deverá escutar nesse endereço IP e na porta para solicitações de conexão de entrada.

## <a name="to-listen-on-a-socket"></a>Para escutar em um soquete

Chame a função [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) , passando como parâmetros o soquete criado e um valor para a *pendência*, o comprimento máximo da fila de conexões pendentes a serem aceitas. Neste exemplo, o parâmetro *backlog* foi definido como **SOMAXCONN**. Esse valor é uma constante especial que instrui o provedor Winsock para esse soquete para permitir um número máximo razoável de conexões pendentes na fila. Verifique o valor de retorno de erros gerais.


```C++
if ( listen( ListenSocket, SOMAXCONN ) == SOCKET_ERROR ) {
    printf( "Listen failed with error: %ld\n", WSAGetLastError() );
    closesocket(ListenSocket);
    WSACleanup();
    return 1;
}
```



Próxima etapa: [aceitando uma conexão](accepting-a-connection.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com o Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Aplicativo de servidor Winsock](winsock-server-application.md)
</dt> <dt>

[Ligando um soquete](binding-a-socket.md)
</dt> </dl>

 

 



