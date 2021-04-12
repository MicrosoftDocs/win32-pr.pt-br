---
title: Estruturas SNMP
description: A tabela a seguir lista as estruturas que são usadas com SNMP.
ms.assetid: b6dacc85-893d-4825-93df-729333b491b3
keywords:
- SNMP de estruturas SNMP
- Estruturas SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f254dfebeb3d468add8871d4b6f28f268341e9ea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366588"
---
# <a name="snmp-structures"></a>Estruturas SNMP

\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]

A tabela a seguir lista as estruturas que são usadas com SNMP.



| Estrutura SNMP                                         | Descrição                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**AsnAny**](/windows/desktop/api/Snmp/ns-snmp-asnany)                           | Descreve o tipo e o valor de uma variável SNMP especificada.                                              |
| [**AsnCounter64**](/previous-versions/windows/desktop/legacy/aa377953(v=vs.85))               | Contém um contador de 64 bits que é especificado por dois valores que descrevem seus bits de ordem inferior e de ordem superior. |
| [**AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) | Descreve um OID (identificador de objeto).                                                                   |
| [**AsnOctetString**](/windows/desktop/api/Snmp/ns-snmp-asnoctetstring)           | Representa uma cadeia de caracteres de octetos, geralmente em valores de bytes.                                                  |
| [**SnmpVarBind**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind)                 | Descreve uma associação de variável SNMP.                                                                     |
| [**SnmpVarBindList**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist)         | Contém uma lista de associações de variáveis SNMP.                                                              |



 

 

 