---
title: Sobre mensagens SNMP
description: O protocolo de gerenciamento de rede simples usa mensagens para se comunicar e trocar informações entre entidades SNMP remotas.
ms.assetid: 9ba4b854-fc02-40c1-a92f-7c102c900e95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a0426bf44d976ddf9e2eafe2093dcea94956cb4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363806"
---
# <a name="about-snmp-messages"></a>Sobre mensagens SNMP

O protocolo de gerenciamento de rede simples usa mensagens para se comunicar e trocar informações entre entidades SNMP remotas. As mensagens SNMP contêm PDUs (unidades de dados de protocolo) e elementos de cabeçalho de mensagem adicionais definidos pela RFC relevante. Um PDU é um pacote de dados que contém os componentes de dados SNMP (ou campos).

O formato de uma mensagem SNMP é o mesmo para SNMPv1 e SNMPv2C. No entanto, o SNMPv2C dá suporte a tipos de PDU adicionais. Por exemplo, ele é compatível com o tipo de solicitação [ \_ \_ GetBulk do SNMP PDU](snmp-variable-types-and-request-pdu-types.md) , que permite que um aplicativo recupere com eficiência grandes blocos de dados de entidades de destino.

 

 




