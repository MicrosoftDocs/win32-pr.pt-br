---
title: Enviando mensagens SNMP
description: Um aplicativo WinSNMP inicia uma solicitação de transmissão enviando uma mensagem SNMP. As mensagens SNMP incluem uma unidade de dados do protocolo SNMP. Para obter mais informações, consulte trabalhando com unidades de dados de protocolo.
ms.assetid: a7439cd2-af13-4e2b-a0a6-5cc271a011e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613ac7079f7dc206280b8d8077d2d5ea8db7151c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292526"
---
# <a name="sending-snmp-messages"></a>Enviando mensagens SNMP

Um aplicativo WinSNMP inicia uma solicitação de transmissão enviando uma mensagem SNMP. As mensagens SNMP incluem uma unidade de dados do protocolo SNMP. Para obter mais informações, consulte [trabalhando com unidades de dados de protocolo](working-with-protocol-data-units.md).

Um aplicativo WinSNMP deve chamar a função [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) para solicitar que a implementação do Microsoft WinSNMP transmita a PDU, com os outros elementos de mensagem necessários definidos pela RFC relevante. Além da entidade de destino, o aplicativo deve especificar a entidade de origem e um contexto para a solicitação. A função [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) é executada de forma assíncrona.

O aplicativo WinSNMP deve chamar a função [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) para recuperar a resposta a uma solicitação **SnmpSendMsg** .

A implementação verifica a validade da PDU e os outros elementos de mensagem quando um aplicativo chama [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg).

 

 




