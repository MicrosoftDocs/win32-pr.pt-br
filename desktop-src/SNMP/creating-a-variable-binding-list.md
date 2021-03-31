---
title: Criando uma lista de associações de variáveis
description: A função SnmpCreateVbl cria uma nova lista de associação de variáveis.
ms.assetid: 18e8a04d-612f-4d85-9cff-8c541a4cdf71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34e9ef7aa208e2e2f887d14c0e124f3bb659ff8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159937"
---
# <a name="creating-a-variable-binding-list"></a>Criando uma lista de associações de variáveis

A função [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) cria uma nova lista de associação de variáveis. Se o aplicativo WinSNMP especificar um nome de variável e um valor, a função criará a lista e adicionará o nome e o valor como a primeira entrada na lista. Se o aplicativo especificar **NULL** para o nome da variável, a função criará uma lista vazia.

Para copiar uma lista de associação de variável, chame a função [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) . A função cria uma nova lista de associação de variáveis e inicializa a nova lista com uma cópia dos dados na lista de associações de variáveis de origem.

A função [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) e a função [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) alocam qualquer memória necessária para a nova lista de associações de variáveis. O aplicativo WinSNMP deve liberar os recursos associados a essas listas. É recomendável que o aplicativo faça isso correspondendo a cada chamada para [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) e [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) com uma chamada correspondente para a função [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) quando for apropriado liberar a memória alocada.

 

 




