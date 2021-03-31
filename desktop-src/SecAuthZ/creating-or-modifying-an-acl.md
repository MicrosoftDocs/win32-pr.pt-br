---
description: O Windows dá suporte a um conjunto de funções que criam uma ACL (lista de controle de acesso) ou modificam as ACEs (entradas de controle de acesso) em uma ACL existente.
ms.assetid: 71301aab-1040-4f61-855f-2b891c8b6077
title: Criando ou modificando uma ACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0deb72bcd1a1c805dd8524027601952dda0eac1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827453"
---
# <a name="creating-or-modifying-an-acl"></a>Criando ou modificando uma ACL

O Windows dá suporte a um conjunto de funções que criam uma ACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) ou modificam as ACEs (entradas de controle de [*acesso*](/windows/desktop/SecGloss/a-gly) ) em uma ACL existente.

A função [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) cria uma nova ACL. **SetEntriesInAcl** pode especificar um conjunto completamente novo de ACEs para a ACL ou pode mesclar uma ou mais ACEs novas com as ACEs de uma ACL existente. A função **SetEntriesInAcl** usa uma matriz de estruturas de [**\_ acesso explícita**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) para especificar as informações para as novas ACEs. Cada estrutura de **\_ acesso explícita** contém informações que DESCREVEM uma única Ace. Essas informações incluem os direitos de acesso, o tipo de ACE, os sinalizadores que controlam a herança de ACE e uma estrutura de [**confiança**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) que identifica o Trustee.

**Para adicionar uma nova ACE a uma ACL existente**

1.  Use a função [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) ou [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) para obter a DACL ou SACL existente do [*descritor de segurança*](/windows/desktop/SecGloss/s-gly)de um objeto.
2.  Para cada nova ACE, chame a função [**BuildExplicitAccessWithName**](/windows/desktop/api/Aclapi/nf-aclapi-buildexplicitaccesswithnamea) para preencher uma estrutura de [**\_ acesso explícita**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) com as informações que descrevem a Ace.
3.  Chame [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla), ESPECIFICANDO a ACL existente e uma matriz de estruturas de [**\_ acesso explícita**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) para as novas ACEs. A função **SetEntriesInAcl** aloca e INICIALIZA a ACL e suas ACEs.
4.  Chame a função [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) ou [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) para anexar a nova ACL ao descritor de segurança do objeto.

Se o chamador especificar uma ACL existente, o [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) mesclará as novas informações de ACE com as ACEs existentes na ACL. Considere o caso, por exemplo, no qual a ACL existente concede acesso a um confiável especificado e uma estrutura de [**\_ acesso explícita**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) nega o acesso ao mesmo Trustee. Nesse caso, **SetEntriesInAcl** adiciona uma nova ACE de acesso negado para o Trustee e exclui ou modifica a Ace permitida pelo Access existente para o Trustee.

Para obter um exemplo de código que mescla uma nova ACE em uma ACL existente, consulte [modificando as ACLs de um objeto em C++](modifying-the-acls-of-an-object-in-c--.md).

 

 
