---
title: Ativando e desativando a retransmissão
description: Um aplicativo pode definir o modo de retransmissão com uma chamada para a função SnmpSetRetransmitMode. O novo modo de retransmissão se aplica às chamadas subsequentes para a função SnmpSendMsg.
ms.assetid: 0e167014-2703-4942-91f0-c60a5c0d8e12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24936bcc90ed0debf66eb9040334fff3bceee2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105779965"
---
# <a name="turning-retransmission-on-and-off"></a>Ativando e desativando a retransmissão

Um aplicativo pode definir o modo de retransmissão com uma chamada para a função [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) . O novo modo de retransmissão se aplica às chamadas subsequentes para a função [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) .

Quando o aplicativo chama **SnmpSetRetransmitMode** com o valor do modo de retransmissão snmpapi \_ , a implementação do Microsoft WinSNMP começa a execução da política de retransmissão do aplicativo. O novo modo de retransmissão não afeta mensagens do SNMP pendentes. Uma mensagem pendente é aquela que não tem resposta no momento em que o aplicativo altera o modo de retransmissão.

Quando o aplicativo WinSNMP chama a função [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) com o valor de modo de retransmissão snmpapi \_ desativado, a implementação para de executar a política de retransmissão. A implementação cancela as tentativas de retransmissão para mensagens SNMP pendentes. Isso ocorre porque talvez não seja possível que a implementação manipule todas as solicitações e operações SNMP pendentes, além de novas solicitações, antes que um contador de tempo limite de aplicativo ou de repetição sinalize um evento.

 

 




