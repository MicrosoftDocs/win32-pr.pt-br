---
description: As funções WSARecv, WSARecvFrom, WSARecvMsg, WSASend, WSASendMsg e WSASendTo levam uma matriz de buffers de aplicativo como parâmetros de entrada e podem ser usadas para dispersão/coleta (ou vetor de) E/S.
ms.assetid: c42e6cea-3b40-44ad-8715-09ce57e82217
title: Dispersão/Coleta de E/S
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4dc580065655c2d69485a49cd41919345c566c32ec2ff9cd1055383853c7438
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794676"
---
# <a name="scattergather-io"></a>Dispersão/Coleta de E/S

As funções [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom), [**LPFN_WSARECVMSG (WSARecvMsg),**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) [**WSASend,**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)e [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) levam uma matriz de buffers de aplicativo como parâmetros de entrada e podem ser usadas para dispersão/coleta (ou vetorada). Isso pode ser muito útil em instâncias em que partes de cada mensagem transmitida consistem em um ou mais componentes de título de comprimento fixo, além do corpo da mensagem. Esses componentes de header não precisam ser concatenados pelo aplicativo em um único buffer contíguo antes do envio. Da mesma forma, ao receber, os componentes de header podem ser divididos automaticamente em buffers separados, deixando o corpo da mensagem sozinho.

Ao receber em vários buffers, a conclusão ocorre à medida que os dados chegam da rede, independentemente de todos os buffers fornecidos serem utilizados.

 

 
