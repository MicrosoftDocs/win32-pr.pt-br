---
description: Várias funções são fornecidas que recuperam informações de controle de acesso de uma ACL (lista de controle de acesso).
ms.assetid: a0839c49-09e9-4407-8702-051b88ef2231
title: Obter informações de uma ACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df5ef90d40058efd19790829f92c37a976359cbc61601d72fa2fee4cc4a93ec7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913668"
---
# <a name="getting-information-from-an-acl"></a>Obter informações de uma ACL

Várias funções são fornecidas que recuperam informações de controle de acesso de uma ACL (lista [*de controle de*](/windows/desktop/SecGloss/a-gly) acesso). Isso inclui funções para determinar os direitos de acesso que uma ACL concede ou audita para um [trustee especificado.](trustees.md) Outras funções permitem extrair informações sobre [*as*](/windows/desktop/SecGloss/a-gly) ACEs (entradas de controle de acesso) em uma ACL.

A [**função GetExplicitEntriesFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-getexplicitentriesfromacla) recupera uma matriz de estruturas [**EXPLICIT \_ ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) que descrevem as ACEs em uma ACL. Isso pode ser útil ao copiar informações ACE de uma ACL para outra. Por exemplo, uma chamada para **GetExplicitEntriesFromAcl** para obter informações sobre os ACEs em uma ACL pode ser seguida passando as estruturas **\_ EXPLICIT ACCESS** retornadas em uma chamada para a função [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) para criar ACEs equivalentes em uma nova ACL.

A [**função GetEffectiveRightsFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-geteffectiverightsfromacla) permite que você determine os direitos de acesso efetivos que uma DACL concede a um usuário confiável especificado. Os direitos de acesso efetivos do usuário confiável são os direitos de acesso que uma DACL concede ao usuário confiável ou a todos os grupos dos quais o usuário confiável é membro. **GetEffectiveRightsFromAcl** verifica todas as ACEs com acesso permitido e negado no DACL especificado.

**Use as etapas a seguir para determinar os direitos de acesso de um objeto de confiança**

1.  Chame a [**função GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) ou [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) para obter um ponteiro para a DACL de um objeto.
2.  Chame a [**função GetEffectiveRightsFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-geteffectiverightsfromacla) para recuperar os direitos de acesso que a DACL concede a um trustee especificado.

A [**função GetAuditedPermissionsFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-getauditedpermissionsfromacla) permite que você verifique uma SACL para determinar os direitos de acesso auditados para um usuário confiável especificado ou para quaisquer grupos dos quais o usuário confiável seja membro. Os direitos auditados indicam os tipos de tentativas de acesso que causam ao sistema gerar um registro de auditoria no log de eventos de segurança. A função retorna duas [*máscaras de acesso:*](/windows/desktop/SecGloss/a-gly)uma contendo os direitos de acesso monitorados para tentativas de acesso com falha e outra contendo os direitos de acesso monitorados para acesso bem-sucedido. **GetAuditedPermissionsFromAcl** verifica todas as ACEs de auditoria do sistema em uma SACL.

 

 
