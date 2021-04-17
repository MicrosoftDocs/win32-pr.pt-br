---
description: Uma CAP (política de autorização central) coleta as regras de autorização específicas (CAPRs) em uma única política.
ms.assetid: E3E43D9F-6826-468A-86E9-AC8F9A381FD4
title: Políticas de autorização central
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b890236b0dae0f8f8d51254def4e1607cc35894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751523"
---
# <a name="central-authorization-policies"></a>Políticas de autorização central

Uma CAP (política de autorização central) coleta as regras de autorização específicas (CAPRs) em uma única política. Para permitir que as regras de autorização específicas (CAPRs) sejam combinadas na política de autorização holística da organização, o CAPRs pode ser referenciado em conjunto e aplicado a um conjunto de recursos. Isso é feito pela coleta de vários (por referência) em um limite. Depois que um limite é definido, ele pode ser distribuído consumido pelos gerenciadores de recursos para aplicar a política de autorização de organizações aos recursos.

Um CAP tem os seguintes atributos:

-   Coleção de CAPRs – uma lista de referências a objetos CAPR existentes
-   Um identificador (SID)
-   Descrição
-   Nome

Um limite é avaliado durante a avaliação de acesso para arquivos e pastas nos quais um administrador o habilita. Durante uma chamada [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) , a verificação de Cap é logicamente combinada com a verificação de ACL condicional; Isso significa que, para obter acesso a um arquivo ao qual a CAP se aplica, um usuário precisa ter acesso de acordo com o limite (seu CAPRs associado) e a ACL condicional no arquivo.

Exemplo de CAP:

``` syntax
CORPORATE-FINANCE-CAP]
CAPID=S-1-5-3-4-56-45-67-123
Policies=HBI-CAPE;RETENTION-CAPR
```

## <a name="cap-definition"></a>Definição de CAP

Um limite é criado e editado no Active Directory usando um novo UX no ADAC (ou PowerShell) que permite ao administrador criar um limite e especificar um conjunto de CAPRs que compõem o limite.

 

 
