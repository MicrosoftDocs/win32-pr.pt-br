---
title: Níveis de suporte a SNMP
description: A implementação do Microsoft WinSNMP fornece suporte a comunicações SNMP de nível 2.
ms.assetid: 9874ad9b-4eb9-4d63-816b-fe444c5b4d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa76a475ed266a7a4928a79f809b7011a537c777c89ea0a97d06983d6656a9ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009454"
---
# <a name="levels-of-snmp-support"></a>Níveis de suporte a SNMP

A implementação do Microsoft WinSNMP fornece suporte a comunicações SNMP de nível 2. O nível 2 dá suporte ao protocolo SNMPv2 padrão de Internet Engineering Task Force (IETF), conforme definido nas RFCs 1902-1908. Ele também dá suporte ao wrapper de mensagens baseado na Comunidade, conforme definido no RFC 1901 (SNMPv2C).

O suporte de comunicações de nível 2 inclui codificação de mensagens e serviços de decodificação, anteriormente chamados de suporte de comunicações de nível 0 no WinSNMP versão 1.1 a. O nível 2 também dá suporte a todas as operações de protocolo SNMPv1, anteriormente chamadas de suporte de comunicações de nível 1 no WinSNMP versão 1.1 a.

A implementação retorna o nível máximo de comunicações SNMP que ele dá suporte em resposta a uma chamada pelo aplicativo WinSNMP para a função [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) .

Se o aplicativo WinSNMP usar a implementação para codificação e decodificação de mensagens SNMP somente, o aplicativo deverá executar as transformações necessárias que a implementação teria feito. Isso inclui a conversão de desvios de SNMPv1 retornados por uma chamada à função [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) , para interceptações de SNMPv2c. Ele também inclui a tradução de tipos de PDU definidos por SNMPv1 para o tipo de PDU relevante definido pelo SNMPv2C, de acordo com a RFC 1908.

 

 




