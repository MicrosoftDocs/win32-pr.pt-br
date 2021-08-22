---
title: Recebendo mensagens SNMP
description: O aplicativo WinSNMP deve chamar a função SnmpRecvMsg para recuperar a resposta a uma solicitação SnmpSendMsg.
ms.assetid: 323a5565-a8a5-4efd-aa4e-e4623b581d09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bd341e71aa6b8387b82f6576599fb6cb7d3545f34e01f80267f19a73edb7cba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009174"
---
# <a name="receiving-snmp-messages"></a>Recebendo mensagens SNMP

O aplicativo WinSNMP deve chamar a função [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) para recuperar a resposta a uma solicitação [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) .

A função [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) passa um identificador de janela de aplicativo e um manipulador de mensagem de notificação para a implementação do Microsoft WinSNMP. Quando a janela do aplicativo recebe essa mensagem, ela sinaliza o aplicativo para chamar a função [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) usando o identificador de sessão retornado por [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).

A função [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) retorna dois identificadores de entidade, um identificador de contexto e o identificador para uma PDU. É recomendável que o aplicativo WinSNMP libere esses recursos usando as funções [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)e [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) .

Para obter informações adicionais sobre como gerenciar o tempo entre uma chamada para a função [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) e o recebimento da resposta correspondente, consulte [sobre retransmissão](about-retransmission.md). Para obter informações adicionais sobre como usar o campo PDU da **\_ ID de solicitação** para corresponder a uma PDU de resposta com sua PDU de solicitação, consulte [resposta correspondente e PDUs de solicitação](matching-response-and-request-pdus.md).

 

 




