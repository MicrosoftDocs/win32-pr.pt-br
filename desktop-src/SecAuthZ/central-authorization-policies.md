---
description: Uma CAP (Política de Autorização Central) coleta as CAPRs (regras de autorização específicas) em uma única política.
ms.assetid: E3E43D9F-6826-468A-86E9-AC8F9A381FD4
title: Políticas de autorização central
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0617f6bddb606d3c3fb3e5ccb6692c79c62a60f90de591b6ec3e04988db46f63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783220"
---
# <a name="central-authorization-policies"></a>Políticas de autorização central

Uma CAP (Política de Autorização Central) coleta as CAPRs (regras de autorização específicas) em uma única política. Para permitir que as CAPRs (regras de autorização específicas) sejam combinadas na política de autorização holística da organização, os CAPRs podem ser referenciados juntos e aplicados a um conjunto de recursos. Isso é feito coletando vários (por referência) em um CAP. Depois que um CAP é definido, ele pode ser distribuído consumido pelos gerenciadores de recursos para aplicar a política de autorização das organizações aos recursos.

Um CAP tem os seguintes atributos:

-   Coleção de CAPRs – uma lista de referências a objetos CAPR existentes
-   Um identificador (Sid)
-   Descrição
-   Nome

Um CAP é avaliado durante a avaliação de acesso para arquivos e pastas nas quais um administrador o habilita. Durante uma [**chamada accessCheck,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) a verificação de CAP é combinada logicamente com a verificação de ACL discricionário; Isso significa que, para obter acesso a um arquivo ao qual o CAP se aplica, um usuário precisa ter acesso de acordo com o CAP (seus CAPRs associados) e a ACL discricionário no arquivo.

CAP de exemplo:

``` syntax
CORPORATE-FINANCE-CAP]
CAPID=S-1-5-3-4-56-45-67-123
Policies=HBI-CAPE;RETENTION-CAPR
```

## <a name="cap-definition"></a>Definição de CAP

Um CAP é criado e editado no Active Directory usando uma nova UX no ADAC (ou No PowerShell) que permite que o administrador crie um CAP e especifique um conjunto de CAPRs que comem o CAP.

 

 
