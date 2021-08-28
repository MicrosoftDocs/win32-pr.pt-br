---
description: Depois que o soquete estiver ouvindo uma conexão, o programa deverá lidar com as solicitações de conexão nesse soquete.
ms.assetid: d01f3d90-4d83-442e-aada-e7b082ef7699
title: aceitando uma conexão (Windows sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 410dcdebb660ec290ee5723b569ca358e0317777300a479e17a516e594744b49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996886"
---
# <a name="accepting-a-connection-windows-sockets-2"></a>aceitando uma conexão (Windows sockets 2)

Depois que o soquete estiver ouvindo uma conexão, o programa deverá lidar com as solicitações de conexão nesse soquete.

**Para aceitar uma conexão em um soquete**

1.  Crie um objeto de **soquete** temporário chamado ClientSocket para aceitar conexões de clientes.
    ```C++
    
    SOCKET ClientSocket;

    
    ```

    

2.  Normalmente, um aplicativo de servidor seria projetado para escutar conexões de vários clientes. Para servidores de alto desempenho, vários threads são comumente usados para lidar com várias conexões de cliente.

    Há várias técnicas de programação diferentes usando o Winsock que podem ser usadas para escutar várias conexões de cliente. Uma técnica de programação é criar um loop contínuo que verifica as solicitações de conexão usando a função [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) (Confira [escuta em um soquete](listening-on-a-socket.md)). Se ocorrer uma solicitação de conexão, o aplicativo chamará a função [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)ou [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) e passará o trabalho para outro thread para lidar com a solicitação. Várias outras técnicas de programação são possíveis.

    Observe que esse exemplo básico é muito simples e não usa vários threads. O exemplo também apenas ouve e aceita uma única conexão.

    ```C++
    
    ClientSocket = INVALID_SOCKET;

    // Accept a client socket
    ClientSocket = accept(ListenSocket, NULL, NULL);
    if (ClientSocket == INVALID_SOCKET) {
        printf("accept failed: %d\n", WSAGetLastError());
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
     
    
    ```

    

3.  Quando a conexão do cliente tiver sido aceita, um aplicativo de servidor normalmente passaria o soquete de cliente aceito (a variável ClientSocket no código de exemplo acima) para um thread de trabalho ou uma porta de conclusão de e/s e continuaria aceitando conexões adicionais. Neste exemplo básico, o servidor continua para a próxima etapa.

    Há uma série de outras técnicas de programação que podem ser usadas para escutar e aceitar várias conexões. Isso inclui o uso das funções [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) . exemplos de algumas dessas várias técnicas de programação são ilustrados nos [exemplos de Winsock avançados](getting-started-with-winsock.md) incluídos no Microsoft Windows Software Development Kit (SDK).

    > [!Note]  
    > Em sistemas UNIX, uma técnica de programação comum para servidores era para um aplicativo escutar conexões. Quando uma conexão foi aceita, o processo pai chamaria a função **Fork** para criar um novo processo filho para lidar com a conexão do cliente, herdando o soquete do pai. não há suporte para essa técnica de programação na Windows, pois não há suporte para a função **fork** . Essa técnica também não é normalmente adequada para servidores de alto desempenho, pois os recursos necessários para criar um novo processo são muito maiores do que os necessários para um thread.

     

Próxima etapa: [recebendo e enviando dados no servidor](receiving-and-sending-data-on-the-server.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com o Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Aplicativo de servidor Winsock](winsock-server-application.md)
</dt> <dt>

[Ouvindo em um soquete](listening-on-a-socket.md)
</dt> </dl>

 

 
