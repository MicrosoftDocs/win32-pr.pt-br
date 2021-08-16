---
description: Compartilhamento de soquete Windows soquetes (Winsock).
ms.assetid: dad31820-6f60-4c3b-9cdf-e301a5ffce48
title: Soquetes compartilhados na SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab0992768a7f3b38f27e4d40c54673e63e855687d0e9b9162e8b9e3cd1d1711d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559694"
---
# <a name="shared-sockets-in-the-spi"></a>Soquetes compartilhados na SPI

O compartilhamento de soquete entre Windows soquetes é implementado da seguinte forma. Um processo de origem [**chama WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) para obter uma estrutura [**especial de \_ INFORMAÇÕES WSAPROTOCOL.**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Ele usa algum mecanismo de IPC (comunicação entre processos) para passar o conteúdo dessa estrutura para um processo de destino. Em seguida, o processo de destino usa a estrutura **INFO WSAPROTOCOL \_** em uma chamada para [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket). O descritor de soquete retornado por essa função será um descritor de soquete adicional para um soquete subjacente que, portanto, se torna compartilhado.

É responsabilidade do provedor de serviços executar as operações necessárias no contexto do processo de origem e criar uma estrutura [**INFO WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) que será reconhecida quando aparecer subsequentemente como um parâmetro para [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) no contexto dos processos de destino. O **membro dwProviderReserved** da estrutura **INFO \_ WSAPROTOCOL** está disponível para uso do provedor de serviços e pode ser usado para armazenar qualquer informação de contexto útil, incluindo um handle duplicado.

Esse mecanismo foi projetado para ser apropriado para versões multithread de thread único e preemptivas do Windows. No entanto, observe que os soquetes podem ser compartilhados entre threads em um determinado processo sem usar a [**função WSPDuplicateSocket,**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) pois um descritor de soquete é válido em todos os threads de um processo.

Conforme descrito na seção Alocação do descritor [,](descriptor-allocation-2.md)quando novos descritores de soquete são alocados provedores IFS devem chamar [**WPUModifyIFSHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle) e provedores não IFS devem chamar [**WPUCreateSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle).

Um cenário possível para estabelecer e usar um soquete compartilhado em um modo de entrega é ilustrado na tabela a seguir.

| Processo de origem                                                                                                                          | IPC    | Processo de Destino                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------|
| 1) [**WSPSocket,**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))                                                                 |        |                                                                               |
| 2) Solicita o identificador do processo de destino.                                                                                                  | ==> |                                                                               |
|                                                                                                                                         |        | 3) Recebe a solicitação do identificador de processo e responde.                          |
| 4) Recebe o identificador do processo.                                                                                                         | <== |                                                                               |
| 5) Chama [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) para obter uma estrutura [**especial de \_ INFORMAÇÕES WSAPROTOCOL.**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) |        |                                                                               |
| 6) Envia a **estrutura WSAPROTOCOL \_ INFO** para o destino.                                                                                     |        |                                                                               |
|                                                                                                                                         | ==> | 7) Recebe a [**estrutura WSAPROTOCOL \_ INFO.**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)        |
|                                                                                                                                         |        | 8) Chama [**WSPSocket para**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) criar descritor de soquete compartilhado. |
|                                                                                                                                         |        | 9)Usa o soquete compartilhado para troca de dados.                                       |
| 10) [ **WSPClosesocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                          | <== |                                                                               |



 

 

 
