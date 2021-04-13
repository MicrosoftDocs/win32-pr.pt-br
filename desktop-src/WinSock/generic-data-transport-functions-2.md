---
description: As funções de transporte de dados expostas por Ws2spi. h.
ms.assetid: 6900faa3-79bb-4ed8-b83e-148eb10425a0
title: Funções de transporte de dados genéricos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63de41b90148210ea8a99d5271b62c5d8bc0c08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501696"
---
# <a name="generic-data-transport-functions"></a>Funções de transporte de dados genéricos

Esta seção lista as funções de transporte de dados expostas por Ws2spi. h.



| Função                                                   | Descrição                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)                           | Uma conexão de entrada é confirmada e associada a um soquete imediatamente criado. O soquete original é retornado para o estado de escuta. Essa função também permite a aceitação condicional. |
| [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85))                 | Executa a versão assíncrona do [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)).                                                                                                                                      |
| [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85))                               | Atribui um nome local a um soquete sem nome.                                                                                                                                                              |
| [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85))   | Cancela uma chamada pendente do Windows Sockets de bloqueio.                                                                                                                                                   |
| [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85))                         | Sai do provedor de serviços Windows Sockets subjacente.                                                                                                                                         |
| [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                 | Remove um soquete da tabela de referência de objeto por processo. Somente os blocos, se \_ forem remanescentes, serão definidos com um tempo limite diferente de zero em um soquete de bloqueio.                                                            |
| [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))                         | Inicia uma conexão no soquete especificado. Essa função também permite o intercâmbio de dados do Connect e especificação de QoS.                                                                           |
| [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85))         | Retorna uma estrutura de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) que pode ser usada para criar um novo descritor de soquete para um Soquete compartilhado.                                                             |
| [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85))     | Descobre ocorrências de eventos de rede.                                                                                                                                                                |
| [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))                 | Associa eventos de rede a um objeto de evento.                                                                                                                                                         |
| [**WSPGetOverlappedResult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult) | Obtém o status de conclusão da operação sobreposta.                                                                                                                                                         |
| [**WSPGetPeerName**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85))                 | Recupera o nome do ponto conectado ao soquete especificado.                                                                                                                                       |
| [**WSPGetSockName**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85))                 | Recupera o endereço local ao qual o soquete especificado está associado.                                                                                                                                     |
| [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))                   | Recupera as opções associadas ao soquete especificado.                                                                                                                                                 |
| [**WSPGetQOSByName**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetqosbyname)               | Fornece parâmetros de QoS com base em um nome de serviço conhecido.                                                                                                                                             |
| [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))                             | Fornece controle para soquetes.                                                                                                                                                                           |
| [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)                       | Une um nó folha em uma sessão do MultiPoint.                                                                                                                                                            |
| [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))                           | Escuta conexões de entrada em um soquete especificado.                                                                                                                                                 |
| [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))                               | Recebe dados de um Soquete conectado ou não conectado. Essa função acomoda dispersão/coleta de e/s, soquetes sobrepostos e fornece o parâmetro flags como IN/OUT.                                    |
| [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85))           | Encerra a recepção em um soquete e recupera os dados de desconexão se o soquete for orientado a conexão.                                                                                                |
| [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85))                       | Recebe dados de um Soquete conectado ou não conectado. Essa função acomoda dispersão/coleta de e/s, soquetes sobrepostos e fornece o parâmetro flags como IN/OUT.                              |
| [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85))                           | Executa a multiplexação de e/s síncrona.                                                                                                                                                                  |
| [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85))                               | Envia dados para um soquete conectado. Essa função também acomoda dispersão/coleta de e/s e soquetes sobrepostos.                                                                                            |
| [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85))           | Inicia o encerramento de uma conexão de soquete e, opcionalmente, envia dados de desconexão.                                                                                                                       |
| [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85))                           | Envia dados para um Soquete conectado ou não conectado. Essa função também acomoda dispersão/coleta de e/s e soquetes sobrepostos.                                                                      |
| [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85))                   | Armazena as opções associadas ao soquete especificado.                                                                                                                                                    |
| [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85))                       | Desliga parte de uma conexão Full-duplex.                                                                                                                                                            |
| [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)                           | Uma função de criação de soquete que usa uma estrutura de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) como entrada e permite que os soquetes sobrepostos sejam criados.                                                |
| [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup)                         | Inicializa o provedor de serviços do Windows Sockets subjacente.                                                                                                                                            |



 

 

 
