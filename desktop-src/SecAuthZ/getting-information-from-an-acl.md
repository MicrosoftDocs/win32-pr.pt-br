---
description: São fornecidas várias funções que recuperam informações de controle de acesso de uma ACL (lista de controle de acesso).
ms.assetid: a0839c49-09e9-4407-8702-051b88ef2231
title: Obtendo informações de uma ACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f87aebc2bc9b05191b5026b990714c2519091be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171246"
---
# <a name="getting-information-from-an-acl"></a>Obtendo informações de uma ACL

São fornecidas várias funções que recuperam informações de controle de acesso de uma ACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/a-gly) ). Isso inclui funções para determinar os direitos de acesso que uma ACL concede ou audita para um [confiável](trustees.md)especificado. Outras funções permitem que você extraia informações sobre as ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) em uma ACL.

A função [**GetExplicitEntriesFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-getexplicitentriesfromacla) recupera uma matriz de estruturas de [**\_ acesso explícita**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) que DESCREVEM as ACEs em uma ACL. Isso pode ser útil ao copiar informações de ACE de uma ACL para outra. Por exemplo, uma chamada para **GetExplicitEntriesFromAcl** para obter informações sobre as ACEs em uma ACL pode ser seguida passando as estruturas de **\_ acesso explícita** retornadas em uma chamada para a função [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) para criar ACEs equivalentes em uma nova ACL.

A função [**GetEffectiveRightsFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-geteffectiverightsfromacla) permite que você determine os direitos de acesso efetivos que uma DACL concede a um confiável especificado. Os direitos de acesso efetivos do Trustee são os direitos de acesso que uma DACL concede ao Trustee ou a qualquer grupo do qual o confiável é membro. **GetEffectiveRightsFromAcl** verifica todas as ACEs de acesso permitido e negado pelo acesso na DACL especificada.

**Use as etapas a seguir para determinar os direitos de acesso de um objeto de confiança para um Object**

1.  Chame a função [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) ou [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) para obter um ponteiro para a DACL de um objeto.
2.  Chame a função [**GetEffectiveRightsFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-geteffectiverightsfromacla) para recuperar os direitos de acesso que a DACL concede a um confiável especificado.

A função [**GetAuditedPermissionsFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-getauditedpermissionsfromacla) permite que você verifique uma SACL para determinar os direitos de acesso auditados para um confiável especificado ou para qualquer grupo do qual o confiável seja membro. Os direitos auditados indicam os tipos de tentativas de acesso que fazem com que o sistema gere um registro de auditoria no log de eventos de segurança. A função retorna duas [*máscaras de acesso*](/windows/desktop/SecGloss/a-gly): uma contendo os direitos de acesso monitorados para tentativas de acesso com falha e outra que contém os direitos de acesso monitorados para acesso bem-sucedido. **GetAuditedPermissionsFromAcl** verifica todas as ACEs de auditoria do sistema em uma SACL.

 

 
