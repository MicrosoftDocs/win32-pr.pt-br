---
description: A função WSADuplicateSocket é introduzida para habilitar o compartilhamento de soquete entre processos.
ms.assetid: f7cf40e9-f3a6-4b62-8a78-df25464e2365
title: Soquetes compartilhados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98e3f2663aa618b1bacab40b1cb29735c972e1d8b9e9db3528ee5079a336747c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612906"
---
# <a name="shared-sockets"></a>Soquetes compartilhados

A função [**WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) é introduzida para habilitar o compartilhamento de soquete entre processos. Um processo de origem chama **WSADuplicateSocket** para obter uma estrutura de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) especial para um identificador de processo de destino. Ele usa um mecanismo de IPC (comunicação entre processos) para passar o conteúdo dessa estrutura para um processo de destino. Em seguida, o processo de destino usa a estrutura de **\_ informações WSAPROTOCOL** em uma chamada para [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket). O descritor de soquete retornado por essa função será um descritor de soquete adicional para um soquete subjacente que, portanto, se tornará compartilhado. Os soquetes podem ser compartilhados entre threads em um determinado processo sem usar a função **WSADuplicateSocket** porque um descritor de soquete é válido em todos os threads de um processo.

Os dois (ou mais) descritores que fazem referência a um Soquete compartilhado podem ser usados de forma independente no que diz respeito à e/s. No entanto, a interface Winsock não implementa nenhum tipo de controle de acesso, portanto, os processos devem coordenar qualquer operação em um Soquete compartilhado. Um exemplo típico de compartilhamento de soquetes é usar um processo para criar soquetes e estabelecer conexões. Esse processo então transfere os soquetes para outros processos responsáveis pela troca de informações.

A função [**WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) cria descritores de soquete e não o soquete subjacente. Como resultado, todos os Estados associados a um soquete são mantidos em comum em todos os descritores. Por exemplo, uma operação [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) executada usando um descritor é posteriormente visível usando um [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) de qualquer um ou de todos os descritores. Um processo pode chamar [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket) em um soquete duplicado e o descritor ficará desalocado. No entanto, o soquete subjacente permanece aberto até que **fechamento** seja chamado com o último descritor restante.

A notificação em soquetes compartilhados está sujeita às restrições usuais das funções [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) e [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) . A emissão de qualquer uma dessas chamadas usando qualquer um dos descritores compartilhados cancela qualquer registro de evento anterior para o soquete, independentemente do qual foi usado para fazer esse registro. Portanto, por exemplo, não seria possível ter o processo A receber \_ eventos de leitura FD e o processo B receber eventos de gravação FD \_ . Para situações em que tal coordenação rígida é necessária, é recomendável que os desenvolvedores usem threads em vez de processos separados.

 

 
