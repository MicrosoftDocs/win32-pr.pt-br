---
description: compartilhamento de soquetes no Windows sockets (Winsock).
ms.assetid: dad31820-6f60-4c3b-9cdf-e301a5ffce48
title: Soquetes compartilhados no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab0992768a7f3b38f27e4d40c54673e63e855687d0e9b9162e8b9e3cd1d1711d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559694"
---
# <a name="shared-sockets-in-the-spi"></a>Soquetes compartilhados no SPI

o compartilhamento de soquete entre processos no Windows sockets é implementado da seguinte maneira. Um processo de origem chama [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) para obter uma estrutura de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) especial. Ele usa um mecanismo de IPC (comunicação entre processos) para passar o conteúdo dessa estrutura para um processo de destino. Em seguida, o processo de destino usa a estrutura de **\_ informações WSAPROTOCOL** em uma chamada para [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket). O descritor de soquete retornado por essa função será um descritor de soquete adicional para um soquete subjacente que, portanto, se tornará compartilhado.

É responsabilidade do provedor de serviços executar quaisquer operações necessárias no contexto do processo de origem e criar uma estrutura de [**\_ informações do WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) que será reconhecida quando aparecer posteriormente como um parâmetro para [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) no contexto dos processos de destino. O membro **dwProviderReserved** da estrutura **de \_ informações do WSAPROTOCOL** está disponível para uso do provedor de serviços e pode ser usado para armazenar qualquer informação de contexto útil, incluindo um identificador duplicado.

Esse mecanismo foi projetado para ser apropriado para versões multithreads e preemptivas de um único thread e de Windows. No entanto, observe que os soquetes podem ser compartilhados entre threads em um determinado processo sem usar a função [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) , já que um descritor de soquete é válido em todos os threads de um processo.

Como é descrito em [alocação de descritor](descriptor-allocation-2.md)de seção, quando novos descritores de soquete são alocados provedores de IFS devem chamar [**WPUModifyIFSHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle) e os provedores não-IFS devem chamar [**WPUCreateSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle).

Um cenário possível para estabelecer e usar um Soquete compartilhado em um modo de entrega é ilustrado na tabela a seguir.

| Processo de origem                                                                                                                          | IPC    | Processo de Destino                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------|
| 1) [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket), [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))                                                                 |        |                                                                               |
| 2) solicita o identificador do processo de destino.                                                                                                  | ==> |                                                                               |
|                                                                                                                                         |        | 3) recebe a solicitação de identificador de processo e responde.                          |
| 4) recebe o identificador do processo.                                                                                                         | <== |                                                                               |
| 5) chama [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) para obter uma estrutura [**de \_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) especial. |        |                                                                               |
| 6) envia a estrutura de **\_ informações do WSAPROTOCOL** para o destino.                                                                                     |        |                                                                               |
|                                                                                                                                         | ==> | 7) recebe a estrutura de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .        |
|                                                                                                                                         |        | 8) chama [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) para criar descritor de soquete compartilhado. |
|                                                                                                                                         |        | 9) usa Soquete compartilhado para troca de dados.                                       |
| 10) [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                          | <== |                                                                               |



 

 

 
