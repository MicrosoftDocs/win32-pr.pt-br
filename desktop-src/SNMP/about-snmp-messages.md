---
title: Sobre mensagens SNMP
description: O Protocolo de Gerenciamento de Rede Simples usa mensagens para comunicar e trocar informações entre entidades SNMP remotas.
ms.assetid: 9ba4b854-fc02-40c1-a92f-7c102c900e95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90c8e6aba33384ddaf16fbe847f20488f0be4d584c70563a34d052a37e80a23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009944"
---
# <a name="about-snmp-messages"></a>Sobre mensagens SNMP

O Protocolo de Gerenciamento de Rede Simples usa mensagens para comunicar e trocar informações entre entidades SNMP remotas. As mensagens SNMP contêm PDUs (unidades de dados de protocolo) além de elementos de header de mensagem adicionais definidos pelo RFC relevante. Uma PDU é um pacote de dados que contém componentes de dados SNMP (ou campos).

O formato de uma mensagem SNMP é o mesmo para SNMPv1 e SNMPv2C. No entanto, o SNMPv2C dá suporte a tipos de PDU adicionais. Por exemplo, ele dá suporte ao tipo de solicitação [ \_ \_ GETBULK da PDU SNMP,](snmp-variable-types-and-request-pdu-types.md) que permite que um aplicativo recupere com eficiência grandes blocos de dados de entidades de destino.

 

 




