---
title: Criando uma lista de associações de variáveis
description: A função SnmpCreateVbl cria uma nova lista de associação de variáveis.
ms.assetid: 18e8a04d-612f-4d85-9cff-8c541a4cdf71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2530b59524375ad6413ff9aa1416db8e25ee3641136284cb4a0f70795e388a8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009574"
---
# <a name="creating-a-variable-binding-list"></a>Criando uma lista de associações de variáveis

A função [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) cria uma nova lista de associação de variáveis. Se o aplicativo WinSNMP especificar um nome de variável e um valor, a função criará a lista e adicionará o nome e o valor como a primeira entrada na lista. Se o aplicativo especificar **NULL** para o nome da variável, a função criará uma lista vazia.

Para copiar uma lista de associação de variável, chame a função [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) . A função cria uma nova lista de associação de variáveis e inicializa a nova lista com uma cópia dos dados na lista de associações de variáveis de origem.

A função [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) e a função [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) alocam qualquer memória necessária para a nova lista de associações de variáveis. O aplicativo WinSNMP deve liberar os recursos associados a essas listas. É recomendável que o aplicativo faça isso correspondendo a cada chamada para [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) e [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) com uma chamada correspondente para a função [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) quando for apropriado liberar a memória alocada.

 

 




