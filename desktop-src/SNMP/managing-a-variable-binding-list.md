---
title: Gerenciando uma lista de associação de variáveis
description: A função SnmpGetVb recupera informações de associação de variáveis de uma lista de associação de variáveis. A função recupera o nome da variável e o valor associado da variável da entrada de associação de variável especificada pelo aplicativo WinSNMP.
ms.assetid: 357aebd6-171a-4221-b12a-712702f9d9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc8c1cbfa4eb0ec3acdc13e9c9cc480b88ddae8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005271"
---
# <a name="managing-a-variable-binding-list"></a>Gerenciando uma lista de associação de variáveis

A função [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb) recupera informações de associação de variáveis de uma lista de associação de variáveis. A função recupera o nome da variável e o valor associado da variável da entrada de associação de variável especificada pelo aplicativo WinSNMP.

Para atualizar entradas de associação de variáveis em uma lista de associação de variáveis, chame a função [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb) . A função **SnmpSetVb** também acrescenta novas entradas de associação de variável a uma lista de associação de variável existente.

O aplicativo WinSNMP deve chamar a função [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb) para remover entradas de uma lista de associação de variável.

Para recuperar, modificar ou excluir uma entrada de associação de variável, o aplicativo WinSNMP deve especificar a posição da entrada na lista de associação de variáveis.

Uma chamada para a função [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) associa uma lista de associação de variável a uma PDU. Uma chamada para a função [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) recupera uma lista de associação de variável de uma PDU. Uma associação de variável individual não está diretamente associada a uma PDU, mas está diretamente associada à sua inclusão em uma lista de associação de variáveis.

 

 




