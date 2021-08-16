---
description: O Gerenciador de Autorização oferece uma estrutura flexível para a integração entre o controle de acesso com base na função e os aplicativos Isso permite aos administradores que usam esses aplicativos fornecer acesso por meio de funções atribuídas de usuário relativas a funções de trabalho.
ms.assetid: c6d37b2e-b149-43e2-8155-cb2f669e421c
title: Modelo do Gerenciador de autorização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20973b8b3e1b35780cc771c04302430b44352a112745842dcbdb66e92b948aad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784189"
---
# <a name="authorization-manager-model"></a>Modelo do Gerenciador de autorização

O Gerenciador de Autorização oferece uma estrutura flexível para a integração entre o controle de acesso com base na função e os aplicativos Isso permite aos administradores que usam esses aplicativos fornecer acesso por meio de funções atribuídas de usuário relativas a funções de trabalho.

Os aplicativos do Gerenciador de autorização armazenam a política de autorização na forma de armazenamentos de autorização armazenados em arquivos Active Directory ou XML e aplicam a política de autorização em tempo de execução.

Em seguida, os aplicativos chamam um método de verificação de acesso em tempo de execução que verifica o acesso às informações de política no repositório de autorização.

A política de autorização inclui as seguintes partes:

-   [Repositórios de política, aplicativos e escopos](policy-stores--applications--and-scopes.md)
-   [Usuários e grupos](users-and-groups.md)
-   [Operações e tarefas](operations-and-tasks.md)
-   [Funções](roles.md)
-   [Regras de negócios](business-rules.md)
-   [Coleções](collections.md)

 

 



