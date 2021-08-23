---
title: Sobre interceptações e notificações
description: Um tipo de mensagem que um aplicativo de agente SNMP pode enviar para um aplicativo WinSNMP é uma mensagem assíncrona que informa ao aplicativo um evento significativo.
ms.assetid: 5249c5a5-9260-4a67-b00f-a12214012bb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60739041237dad462e516e43c71d552446357f3ddc188d6609de2eef508b9658
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009804"
---
# <a name="about-traps-and-notifications"></a>Sobre interceptações e notificações

Um tipo de mensagem que um aplicativo de agente SNMP pode enviar para um aplicativo WinSNMP é uma mensagem assíncrona que informa ao aplicativo um evento significativo. Um exemplo de um evento significativo é quando um link de rede é desligado ou quando ocorre uma falha de autenticação.

Esses tipos de mensagens são chamados de interceptações em SNMPv1 e notificações sob o SNMPv2C. A implementação do Microsoft WinSNMP sempre traduz as armadilhas de SNMPv1 para o formato SNMPv2C, conforme definido pelo RFC 1908.

Ao chamar a função [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) para criar uma PDU de interceptação, você pode criar apenas um PDU de interceptação de SNMPv2c. O único tipo de PDU de interceptação que você pode atualizar com uma chamada para a função [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) é um PDU de interceptação de SNMPv2c.

Para obter mais informações, consulte estes tópicos.



| Tópico                                                                                    | Descrição |
|------------------------------------------------------------------------------------------|-------------|
| [Convertendo interceptações de SNMPv1 para SNMPv2C](translating-traps-from-snmpv1-to-snmpv2c.md) |             |
| [Formatos de interceptação](trap-formats.md)                                                         |             |



 

 

 




