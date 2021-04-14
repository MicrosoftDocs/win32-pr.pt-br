---
title: Gerenciando identificadores de objeto
description: A API WinSNMP fornece várias funções de utilitário WinSNMP que simplificam a manipulação de identificadores de objeto para aplicativos WinSNMP.
ms.assetid: 6ca5f5bc-aa49-4826-97a7-2ea4a882dc2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9745cb8018b6833a1ef0569e69f201c621aa38e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453696"
---
# <a name="managing-object-identifiers"></a>Gerenciando identificadores de objeto

A API WinSNMP fornece várias [funções de utilitário WinSNMP](winsnmp-functions.md) que simplificam a manipulação de identificadores de objeto para aplicativos WinSNMP.

A função [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) converte a representação binária interna de um identificador de objeto em seu formato de cadeia de caracteres numérica pontilhada. Ao chamar [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr), especifique um buffer de cadeia de caracteres de comprimento MAXOBJIDSTRSIZE (1408 bytes) para garantir que o buffer de saída seja grande o suficiente para manter a cadeia de caracteres convertida. Para converter um identificador de objeto do formato de cadeia de caracteres numérica pontilhada em sua representação binária interna, chame a função [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) .

Para copiar um identificador de objeto SNMP, chame a função [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) . Essa função aloca qualquer memória necessária para o novo identificador de objeto.

Um aplicativo WinSNMP deve chamar a função [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) para liberar recursos alocados para o membro **PTR** da estrutura [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) especificada pelas funções [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) e [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) .

A função [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare) compara dois identificadores de objeto SNMP. O aplicativo WinSNMP pode especificar o número de subidentificadores para comparar. Chame **SnmpOidCompare** para determinar se dois identificadores de objeto têm prefixos comuns.

Para obter informações adicionais sobre como gerenciar a memória alocada para identificadores de objeto, consulte [alocando objetos de memória WinSNMP](allocating-winsnmp-memory-objects.md).

 

 




