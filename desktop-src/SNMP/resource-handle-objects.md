---
title: Objetos do Resource Handle
description: A estrutura de um objeto de recurso é restrita à implementação do Microsoft WinSNMP. Um aplicativo WinSNMP pode acessar um objeto de recurso com um identificador.
ms.assetid: c70a03b1-afac-4f1a-81e7-7f31430f5655
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b05702f0ad43e5b4b80a9b1a3cada471212dec3bc377bddcc95fe9a109ec78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009114"
---
# <a name="resource-handle-objects"></a>Objetos do Resource Handle

A estrutura de um objeto de recurso é restrita à implementação do Microsoft WinSNMP. Um aplicativo WinSNMP pode acessar um objeto de recurso com um identificador.

A implementação pode alocar um dos seguintes tipos de alças de recurso para um aplicativo WinSNMP.

| Tipo de identificador        | Descrição                       |
|--------------------|-----------------------------------|
| **SESSÃO \_ HSNMP** | Manipular para uma sessão WinSNMP       |
| **ENTIDADE \_ HSNMP**  | Lidar com uma entidade SNMP          |
| **CONTEXTO \_ HSNMP** | Manipular para um contexto WinSNMP       |
| **HSNMP \_ PDU**     | Lidar com uma unidade de dados de protocolo    |
| **HSNMP \_ VBL**     | Manipular para uma lista de associação de variáveis |



 

Um aplicativo WinSNMP pode solicitar que a implementação crie ou exclua os alças de recurso, mas a implementação executa a operação. Para obter informações adicionais sobre como liberar recursos individuais, consulte as funções [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreePdu,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)e [**SnmpFreeContext.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)

 

 




