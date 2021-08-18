---
title: Enviando mensagens SNMP
description: Um aplicativo WinSNMP inicia uma solicitação de transmissão enviando uma mensagem SNMP. As mensagens SNMP incluem uma unidade de dados de protocolo SNMP. Para obter mais informações, consulte Trabalhando com unidades de dados de protocolo.
ms.assetid: a7439cd2-af13-4e2b-a0a6-5cc271a011e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4461c5d554444b2a7a5384a0ca79825b27ebe3c3bc489b6152c81ae71d172f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009064"
---
# <a name="sending-snmp-messages"></a>Enviando mensagens SNMP

Um aplicativo WinSNMP inicia uma solicitação de transmissão enviando uma mensagem SNMP. As mensagens SNMP incluem uma unidade de dados de protocolo SNMP. Para obter mais informações, consulte [Trabalhando com unidades de dados de protocolo](working-with-protocol-data-units.md).

Um aplicativo WinSNMP deve chamar a função [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) para solicitar que a implementação do Microsoft WinSNMP transmita a PDU, com os outros elementos de mensagem necessários definidos pelo RFC relevante. Além da entidade de destino, o aplicativo deve especificar a entidade de origem e um contexto para a solicitação. A [**função SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) é executada de forma assíncrona.

O aplicativo WinSNMP deve chamar a [**função SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) para recuperar a resposta a **uma solicitação SnmpSendMsg.**

A implementação verifica a validade da PDU e dos outros elementos de mensagem quando um aplicativo chama [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg).

 

 




