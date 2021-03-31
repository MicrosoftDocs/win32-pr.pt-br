---
title: Objetos de identificador de recurso
description: A estrutura de um objeto de recurso é restrita à implementação do Microsoft WinSNMP. Um aplicativo WinSNMP pode acessar um objeto de recurso com um identificador.
ms.assetid: c70a03b1-afac-4f1a-81e7-7f31430f5655
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1afe5e6488190f95961bff7ce37f7b719d076d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636755"
---
# <a name="resource-handle-objects"></a>Objetos de identificador de recurso

A estrutura de um objeto de recurso é restrita à implementação do Microsoft WinSNMP. Um aplicativo WinSNMP pode acessar um objeto de recurso com um identificador.

A implementação pode alocar um dos seguintes tipos de identificadores de recursos para um aplicativo WinSNMP.

| Tipo de identificador        | Descrição                       |
|--------------------|-----------------------------------|
| **\_sessão HSNMP** | Tratar de uma sessão WinSNMP       |
| **\_entidade HSNMP**  | Identificador para uma entidade SNMP          |
| **contexto de HSNMP \_** | Tratar de um contexto WinSNMP       |
| **PDU de HSNMP \_**     | Identificador para uma unidade de dados de protocolo    |
| **HSNMP \_ VBL**     | Identificador para uma lista de associação de variável |



 

Um aplicativo WinSNMP pode solicitar que a implementação crie ou exclua identificadores de recurso, mas a implementação executa a operação. Para obter informações adicionais sobre como liberar recursos individuais, consulte as funções [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)e [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext) .

 

 




