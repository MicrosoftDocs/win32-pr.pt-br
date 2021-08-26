---
title: Formatos de interceptação
description: O formato de PDUs de interceptação é diferente daquele de outra PDUs. O formato de armadilhas de SNMPv1 e interceptações de SNMPv2C também é diferente.
ms.assetid: 2d2b4520-28b7-4a2e-8dee-456e17d9d6f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b73e9cd2a5396bbe258fcb67c88cc207ea0243a9e8aff9f31e4866b9ee8adcc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885676"
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

 

 




