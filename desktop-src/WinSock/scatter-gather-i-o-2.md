---
description: As funções WSARecv, WSARecvFrom, WSARecvMsg, WSASend, WSASendMsg e WSASendTo usam uma matriz de buffers de aplicativo como parâmetros de entrada e podem ser usadas para e/s de dispersão/coleta (ou vetorizada).
ms.assetid: c42e6cea-3b40-44ad-8715-09ce57e82217
title: Dispersão/coleta de e/s
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c572892a75b3532d68a39e2fabdcc971f0a3327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772989"
---
# <a name="scattergather-io"></a>Dispersão/coleta de e/s

As funções [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom), [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)e [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) usam uma matriz de buffers de aplicativo como parâmetros de entrada e podem ser usadas para e/s de dispersão/coleta (ou vetor). Isso pode ser muito útil em instâncias em que partes de cada mensagem sendo transmitida consistem em um ou mais componentes de cabeçalho de comprimento fixo, além do corpo da mensagem. Esses componentes de cabeçalho não precisam ser concatenados pelo aplicativo em um único buffer contíguo antes de enviar. Da mesma forma no recebimento, os componentes de cabeçalho podem ser divididos automaticamente em buffers separados, deixando o corpo da mensagem por si só.

Ao receber vários buffers, a conclusão ocorre conforme os dados chegam da rede, independentemente de todos os buffers fornecidos serem utilizados.

 

 
