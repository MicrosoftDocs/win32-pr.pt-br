---
title: Como ligar e desligar a retransmissão
description: Um aplicativo pode definir o modo de retransmissão com uma chamada para a função SnmpSetRetransmitMode. O novo modo de retransmissão se aplica a chamadas subsequentes à função SnmpSendMsg.
ms.assetid: 0e167014-2703-4942-91f0-c60a5c0d8e12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc7624977b4959911cc4128c9a75ac70fac7031bfb853c4b31db34d0987b4d4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885666"
---
# <a name="turning-retransmission-on-and-off"></a>Como ligar e desligar a retransmissão

Um aplicativo pode definir o modo de retransmissão com uma chamada para a [**função SnmpSetRetransmitMode.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) O novo modo de retransmissão se aplica a chamadas subsequentes à [**função SnmpSendMsg.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)

Quando o aplicativo chama **SnmpSetRetransmitMode** com o valor de modo de retransmissão SNMPAPI ON, a implementação do Microsoft WinSNMP inicia a execução da política de \_ retransmissão do aplicativo. O novo modo de retransmissão não afeta mensagens SNMP pendentes. Uma mensagem pendente é aquela que não tem resposta no momento em que o aplicativo altera o modo de retransmissão.

Quando o aplicativo WinSNMP chama a função [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) com o valor de modo de retransmissão SNMPAPI OFF, a implementação para de executar a política de \_ retransmissão. A implementação cancela tentativas de retransmissão para mensagens SNMP pendentes. Isso ocorre porque pode não ser possível para a implementação lidar com todas as solicitações e operações SNMP pendentes, além de novas solicitações, antes que um contador de tempo de tempo de execução ou de nova tentativa sinalizar um evento.

 

 




