---
title: Convertendo solicitações de mensagem
description: Este tópico descreve o processo de conversão de solicitações de SNMPv1 em solicitações de SNMPv2.
ms.assetid: 7671ae36-99b1-47b1-930a-f376021d56a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1775d59a8de0bd0473570f3028018a1a25cad2ebd4ee004025ad11a38e37e69c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885886"
---
# <a name="translating-message-requests"></a>Convertendo solicitações de mensagem

Este tópico descreve o processo de conversão de solicitações de SNMPv1 em solicitações de SNMPv2.

Se um aplicativo de WinSNMP solicitar uma funcionalidade que esteja disponível na estrutura do SNMP versão 2C (SNMPv2C), mas a entidade de destino der suporte apenas ao SNMPv1 (SNMP versão 1 Framework), a implementação do Microsoft WinSNMP tentará converter a solicitação para o formato SNMPv1. Para fazer isso, a implementação usa os procedimentos definidos na RFC 1908, "coexistência entre a versão 1 e a versão 2 do Internet-Standard estrutura de gerenciamento de rede". Se a conversão não for possível, a função [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) falhará com o código de erro estendido snmpapi \_ operação \_ inválida.

 

 




