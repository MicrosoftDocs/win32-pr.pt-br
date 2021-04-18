---
description: A função WSAAccept permite que um aplicativo Obtenha informações do chamador, como o identificador do chamador e a qualidade do serviço, antes de decidir se deve aceitar uma solicitação de conexão de entrada.
ms.assetid: 65883556-6890-4d0a-8c7f-c4ff68642caf
title: Configuração e desmontagem da conexão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c4ac1f32524d097e11825f8104eb41fee3c528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763224"
---
# <a name="connection-setup-and-teardown"></a>Configuração e desmontagem da conexão

A função [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) permite que um aplicativo Obtenha informações do chamador, como o identificador do chamador e a qualidade do serviço, antes de decidir se deve aceitar uma solicitação de conexão de entrada. Isso é feito com um retorno de chamada para uma função de condição fornecida pelo aplicativo.

Os dados de usuário para usuário especificados por parâmetros na função [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) e a função Condition de [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) podem ser transferidos para o par durante o estabelecimento da conexão, desde que esse recurso seja suportado pelo provedor de serviços.

Também é possível (para protocolos que dão suporte a isso) para trocar dados de usuário entre os pontos de extremidade no momento da desmontagem da conexão. O final que inicia a desmontagem pode chamar a função [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) para indicar que não é mais possível enviar mais dados e iniciar a sequência de divisão de conexão. Para determinados protocolos, parte da desmontagem é a entrega de dados desconectados do iniciador de desmontagem. Após o recebimento do aviso de que a extremidade remota iniciou a subdivisão (normalmente pela \_ indicação de fechamento FD), a função [**WSARecvDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) pode ser chamada para receber os dados de desconexão, se houver.

Para ilustrar como os dados de desconexão podem ser usados, considere o cenário a seguir. A metade do cliente de um aplicativo cliente/servidor é responsável por encerrar uma conexão de soquete. Coincidente com o encerramento, ele fornece (usando dados de desconexão) o número total de transações processadas com o servidor. O servidor, por sua vez, responde com o total cumulativo de transações processadas com todos os clientes. A sequência de chamadas e indicações pode ocorrer da seguinte maneira:

| Lado do cliente                                                                                                              | Lado do Servidor                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (1) invocar [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) para concluir a sessão e fornecer o total da transação.            |                                                                                                                                                                                                                               |
|                                                                                                                          | (2) obter FD \_ Close, [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) com um valor de retorno igual a zero ou [WSAEDISCON](windows-sockets-error-codes-2.md) retorno de erro de [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) indicando que o desligamento normal está em andamento. |
|                                                                                                                          | (3) invocar [**WSARecvDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) para obter o total da transação do cliente.                                                                                                                                |
|                                                                                                                          | (4) total da computação cumulativa geral de todas as transações.                                                                                                                                                                       |
|                                                                                                                          | (5) invocar [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) para transmitir total geral.                                                                                                                                          |
| (6) receber \_ indicação de fechamento FD.                                                                                        | (5A) invocar [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket).                                                                                                                                                                             |
| (7) invocar [**WSARecvDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) para receber e armazenar o total geral cumulativo de transações. |                                                                                                                                                                                                                               |
| (8) invocar [ **fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket)                                                                          |                                                                                                                                                                                                                               |



 

Observe que a etapa (5A) deve seguir a etapa (5), mas não tem nenhuma relação de tempo com a etapa (6), (7) ou (8).

 

 



