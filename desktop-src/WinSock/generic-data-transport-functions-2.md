---
description: As funções de transporte de dados expostas por Ws2spi.h.
ms.assetid: 6900faa3-79bb-4ed8-b83e-148eb10425a0
title: Funções de transporte de dados genéricos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d13b067713fe6a2600d6667ebe7eac058c5fcae87fc5bfd14311b3a263b862
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132349"
---
# <a name="generic-data-transport-functions"></a>Funções de transporte de dados genéricos

Esta seção lista as funções de transporte de dados expostas por Ws2spi.h.



| Função                                                   | Descrição                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Wspaccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)                           | Uma conexão de entrada é confirmada e associada a um soquete criado imediatamente. O soquete original é retornado para o estado de escuta. Essa função também permite a aceitação condicional. |
| [**Wspasyncselect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85))                 | Executa a versão assíncrona [**do WSPSelect.**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85))                                                                                                                                      |
| [**Wspbind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85))                               | Atribui um nome local a um soquete sem nome.                                                                                                                                                              |
| [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85))   | Cancela um bloqueio pendente Windows chamada soquetes.                                                                                                                                                   |
| [**Wspcleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85))                         | Sai do provedor de serviços Windows Sockets subjacente.                                                                                                                                         |
| [**Wspclosesocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                 | Remove um soquete da tabela de referência de objeto por processo. Só será bloqueado se SO LINGER for definido com um \_ tempo-tempo-out não zero em um soquete de bloqueio.                                                            |
| [**Wspconnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))                         | Inicia uma conexão no soquete especificado. Essa função também permite a troca de dados de conexão e especificação de QoS.                                                                           |
| [**Wspduplicatesocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85))         | Retorna uma [**estrutura INFO \_ WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) que pode ser usada para criar um novo descritor de soquete para um soquete compartilhado.                                                             |
| [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85))     | Descobre ocorrências de eventos de rede.                                                                                                                                                                |
| [**Wspeventselect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))                 | Associa eventos de rede a um objeto de evento.                                                                                                                                                         |
| [**Wspgetoverlappedresult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult) | Obtém o status de conclusão da operação sobrecarada.                                                                                                                                                         |
| [**WSPGetPeerName**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85))                 | Recupera o nome do par conectado ao soquete especificado.                                                                                                                                       |
| [**WSPGetSockName**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85))                 | Recupera o endereço local ao qual o soquete especificado está vinculado.                                                                                                                                     |
| [**Wspgetsockopt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))                   | Recupera as opções associadas ao soquete especificado.                                                                                                                                                 |
| [**WSPGetQOSByName**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetqosbyname)               | Fornece parâmetros QoS com base em um nome de serviço conhecido.                                                                                                                                             |
| [**Wspioctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))                             | Fornece controle para soquetes.                                                                                                                                                                           |
| [**Wspjoinleaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)                       | Une um nó folha em uma sessão de vários pontos.                                                                                                                                                            |
| [**Wsplisten**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))                           | Escuta conexões de entrada em um soquete especificado.                                                                                                                                                 |
| [**Wsprecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))                               | Recebe dados de um soquete conectado ou não conectado. Essa função acomoda a E/S de dispersão/coleta, soquetes sobrecodados e fornece o parâmetro flags como IN/OUT.                                    |
| [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85))           | Encerra a recepção em um soquete e recupera os dados de desconexão se o soquete é orientado a conexão.                                                                                                |
| [**Wsprecvfrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85))                       | Recebe dados de um soquete conectado ou não conectado. Essa função acomoda a E/S de dispersão/coleta, soquetes sobrecodados e fornece o parâmetro flags como IN/OUT.                              |
| [**Wspselect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85))                           | Executa a multiplexação de E/S síncrona.                                                                                                                                                                  |
| [**Wspsend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85))                               | Envia dados para um soquete conectado. Essa função também acomoda a E/S de dispersão/coleta e soquetes sobressalados.                                                                                            |
| [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85))           | Inicia o encerramento de uma conexão de soquete e, opcionalmente, envia dados de desconexão.                                                                                                                       |
| [**Wspsendto**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85))                           | Envia dados para um soquete conectado ou não conectado. Essa função também acomoda a E/S de dispersão/coleta e soquetes sobressalados.                                                                      |
| [**Wspsetsockopt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85))                   | Armazena as opções associadas ao soquete especificado.                                                                                                                                                    |
| [**Wspshutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85))                       | Desliga parte de uma conexão full duplex.                                                                                                                                                            |
| [**Wspsocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)                           | Uma função de criação de soquete que aceita uma estrutura [**INFO WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) como entrada e permite que soquetes sobressaltos sejam criados.                                                |
| [**Wspstartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup)                         | Inicializa o provedor de serviços Windows Sockets subjacente.                                                                                                                                            |



 

 

 
