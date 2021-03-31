---
title: Formatos de interceptação
description: O formato de PDUs de interceptação é diferente daquele de outra PDUs. O formato de armadilhas de SNMPv1 e interceptações de SNMPv2C também é diferente.
ms.assetid: 2d2b4520-28b7-4a2e-8dee-456e17d9d6f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87adc3222808fcc7e81904ade07c09afa13bc6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005173"
---
# <a name="trap-formats"></a>Formatos de interceptação

O formato de PDUs de interceptação é diferente daquele de outra PDUs. O formato de armadilhas de SNMPv1 e interceptações de SNMPv2C também é diferente.

Na estrutura do SNMPv2C, o formato de interceptação de PDU é uma lista de associações de variáveis de *n* entradas de associação de variáveis organizadas da seguinte maneira:

-   A primeira entrada de associação de variável contém um carimbo de data/hora.
-   A segunda entrada de associação de variável é um identificador de objeto que identifica a interceptação.
-   O terceiro a *n* entradas de associação de variável, se presente, contêm informações adicionais associadas à interceptação.

Na estrutura SNMPv1, o formato de interceptação PDU é o seguinte.

| Campo                      | Descrição                                                      |
|----------------------------|------------------------------------------------------------------|
| corporativo                 | Identifica o tipo de dispositivo que gerou a interceptação.           |
| Agente-addr                 | Identifica o endereço IP do dispositivo que gerou a interceptação. |
| desvio genérico/interceptação específica | Identifica um tipo de interceptação predefinida.                               |
| carimbo de data/hora                 | Identifica quando a interceptação foi gerada.                          |
| associações de variáveis          | Contém informações adicionais associadas à interceptação.        |



 

A função [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) sempre retorna uma mensagem no formato SNMPv2c. Se a mensagem contiver o tipo de operação **\_ \_ interceptação de PDU SNMP**, o aplicativo poderá ler as entradas de associação de variável da mensagem e recuperar as informações associadas à interceptação.

 

 




