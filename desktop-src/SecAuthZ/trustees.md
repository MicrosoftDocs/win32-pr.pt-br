---
description: Um confiável é a conta de usuário, a conta de grupo ou a sessão de logon à qual se aplica uma ACE (entrada de controle de acesso). Cada ACE em uma ACL (lista de controle de acesso) tem um SID (identificador de segurança) que identifica um confiável.
ms.assetid: 1c34faa0-936a-433a-9280-a94033f3f815
title: Comitê
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90084a0b6bfc7f63db12b7f47eba335adc87239a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172157"
---
# <a name="trustees"></a>Comitê

Um confiável é a conta de usuário, a conta de grupo ou a [*sessão de logon*](/windows/desktop/SecGloss/l-gly) à qual se aplica uma ACE (entrada de [*controle de acesso*](/windows/desktop/SecGloss/a-gly) ). Cada ACE em uma ACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) tem um SID (identificador de [*segurança*](/windows/desktop/SecGloss/s-gly) ) que identifica um confiável.

As contas de usuário incluem contas que os usuários ou programas humanos, como os serviços do Windows, usam para fazer logon no computador local.

As contas de grupo não podem ser usadas para fazer logon em um computador, mas elas são úteis em ACEs para permitir ou negar um conjunto de direitos de acesso a uma ou mais contas de usuário.

Um [*Sid de logon*](/windows/desktop/SecGloss/l-gly) que identifica a sessão de logon atual é útil para permitir ou negar direitos de acesso somente até que o usuário faça logoff.

As funções de controle de acesso usam a estrutura de [**confiança**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) para identificar um confiável. A estrutura de **confiança** permite que você use uma cadeia de caracteres de nome ou um SID para identificar um confiável. Se você usar um nome, as funções que criam uma ACE da estrutura de **confiança** executarão a tarefa de alocar os buffers de Sid e procurar o Sid que corresponde ao nome da conta. Há duas funções auxiliares, [**BuildTrusteeWithSid**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithsida) e [**BuildTrusteeWithName**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithnamea), que inicializam uma estrutura de **confiança** com um SID ou nome especificado. [**BuildTrusteeWithObjectsAndSid**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithobjectsandsida) e [**BuildTrusteeWithObjectsAndName**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithobjectsandnamea) permitem que você inicialize uma estrutura de **confiança** com informações de Ace específicas de objeto. Três outras funções auxiliares, [**GetTrusteeForm**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteeforma), [**getconfiávelname**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteenamea)e [**getconfiáveltype**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteetypea)recuperam os valores dos vários membros de uma estrutura de **confiança** .

O membro **ptstrName** da estrutura de [**confiança**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) pode ser um ponteiro para [**objetos \_ e \_ nomes**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) ou objetos e a estrutura [**\_ de \_ Sid**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) . Essas estruturas especificam informações sobre uma [Ace específica de objeto,](object-specific-aces.md) além de um nome de confiança ou Sid. Isso permite que funções como [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) e [**GetExplicitEntriesFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-getexplicitentriesfromacla) armazenem informações de Ace específicas de objeto no membro **Trustee** da estrutura [**de \_ acesso explícita**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) .

 

 
