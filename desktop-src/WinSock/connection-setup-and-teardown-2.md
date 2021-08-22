---
description: A função WSAAccept permite que um aplicativo obtenha informações do chamador, como identificador de chamador e Qualidade de Serviço, antes de decidir se deve aceitar uma solicitação de conexão de entrada.
ms.assetid: 65883556-6890-4d0a-8c7f-c4ff68642caf
title: Instalação e rebaixamento de conexão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c5e8c8a95c9baa90e95bd7b7da2702f3522b2a575d3d0181271428837e27b7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051714"
---
# <a name="connection-setup-and-teardown"></a>Instalação e rebaixamento de conexão

A [**função WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) permite que um aplicativo obtenha informações do chamador, como identificador de chamador e Qualidade de Serviço, antes de decidir se deve aceitar uma solicitação de conexão de entrada. Isso é feito com um retorno de chamada para uma função de condição fornecida pelo aplicativo.

Os dados de usuário para usuário especificados por parâmetros na função [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) e a função de condição [**de WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) podem ser transferidos para o par durante o estabelecimento da conexão, desde que esse recurso seja suportado pelo provedor de serviços.

Também é possível (para protocolos que suportam isso) trocar dados de usuário entre os pontos de extremidade no momento da redução da conexão. O final que inicia a rebaixamento pode chamar a função [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) para indicar que nenhum dado mais será enviado e para iniciar a sequência de encerramento de conexão. Para determinados protocolos, parte da rebaixamento é a entrega de dados de desconexão do iniciador de rebaixamento. Depois de receber um aviso de que o final remoto iniciou a rebaixamento (normalmente pela indicação FD CLOSE), a \_ [**função WSARecvDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) pode ser chamada para receber os dados de desconexão, se algum.

Para ilustrar como os dados de desconexão podem ser usados, considere o cenário a seguir. A metade do cliente de um aplicativo cliente/servidor é responsável por encerrar uma conexão de soquete. Coincidente com o encerramento, ele fornece (usando dados de desconexão) o número total de transações processadas com o servidor. O servidor, por sua vez, responde com o total cumulativo de transações que ele processou com todos os clientes. A sequência de chamadas e indicações pode ocorrer da seguinte forma:

| Lado do cliente                                                                                                              | Lado do Servidor                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (1) [**Invoque WSASendDisconnect para**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) concluir a sessão e fornecer o total de transações.            |                                                                                                                                                                                                                               |
|                                                                                                                          | (2) Obter FD CLOSE, recv com um valor de retorno de zero ou retorno de erro \_ [WSAEDISCON](windows-sockets-error-codes-2.md) de [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) indicando desligamento normalmente em andamento. [](/windows/desktop/api/winsock/nf-winsock-recv) |
|                                                                                                                          | (3) [**Invoque WSARecvDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) para obter o total de transações do cliente.                                                                                                                                |
|                                                                                                                          | (4) Computar o total geral cumulativo de todas as transações.                                                                                                                                                                       |
|                                                                                                                          | (5) [**Invoque WSASendDisconnect para**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) transmitir o total geral.                                                                                                                                          |
| (6) Receber indicação FD \_ CLOSE.                                                                                        | (5a) Invocar [**closesocket.**](/windows/desktop/api/winsock/nf-winsock-closesocket)                                                                                                                                                                             |
| (7) [**Invoque WSARecvDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) para receber e armazenar o total geral cumulativo de transações. |                                                                                                                                                                                                                               |
| (8) Invocar [ **closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)                                                                          |                                                                                                                                                                                                                               |



 

Observe que a etapa (5a) deve seguir a etapa (5), mas não tem relação de tempo com a etapa (6), (7) ou (8).

 

 



