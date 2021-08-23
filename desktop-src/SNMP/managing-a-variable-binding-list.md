---
title: Gerenciando uma lista de associação de variáveis
description: A função SnmpGetVb recupera informações de associação de variáveis de uma lista de associação de variáveis. A função recupera o nome da variável e o valor associado da variável da entrada de associação de variável especificada pelo aplicativo WinSNMP.
ms.assetid: 357aebd6-171a-4221-b12a-712702f9d9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c382e2780ae49a1f029aab2cfef2bcd4357fcfbf7b37ce9a1fcad9aed5bc0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009444"
---
# <a name="managing-a-variable-binding-list"></a>Gerenciando uma lista de associação de variáveis

A função [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb) recupera informações de associação de variáveis de uma lista de associação de variáveis. A função recupera o nome da variável e o valor associado da variável da entrada de associação de variável especificada pelo aplicativo WinSNMP.

Para atualizar entradas de associação de variáveis em uma lista de associação de variáveis, chame a função [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb) . A função **SnmpSetVb** também acrescenta novas entradas de associação de variável a uma lista de associação de variável existente.

O aplicativo WinSNMP deve chamar a função [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb) para remover entradas de uma lista de associação de variável.

Para recuperar, modificar ou excluir uma entrada de associação de variável, o aplicativo WinSNMP deve especificar a posição da entrada na lista de associação de variáveis.

Uma chamada para a função [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) associa uma lista de associação de variável a uma PDU. Uma chamada para a função [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) recupera uma lista de associação de variável de uma PDU. Uma associação de variável individual não está diretamente associada a uma PDU, mas está diretamente associada à sua inclusão em uma lista de associação de variáveis.

 

 




