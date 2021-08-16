---
description: Windows dá suporte a um conjunto de funções que criam uma ACL (lista de controle de acesso) ou modificam as ACEs (entradas de controle de acesso) em uma ACL existente.
ms.assetid: 71301aab-1040-4f61-855f-2b891c8b6077
title: Criando ou modificando uma ACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120b445d37f8c4b82c2b0b2a775a06d68faa46ab5752cc25e913d43676e9a72e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782161"
---
# <a name="creating-or-modifying-an-acl"></a>Criando ou modificando uma ACL

Windows dá suporte a um conjunto de funções que criam uma ACL [*(lista*](/windows/desktop/SecGloss/a-gly) de controle de acesso) ou modificam as ACEs [*(entradas*](/windows/desktop/SecGloss/a-gly) de controle de acesso) em uma ACL existente.

A [**função SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) cria uma nova ACL. **SetEntriesInAcl** pode especificar um conjunto completamente novo de ACEs para a ACL ou pode mesclar uma ou mais ACEs novas com as ACEs de uma ACL existente. A **função SetEntriesInAcl** usa uma matriz de estruturas [**EXPLICIT \_ ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) para especificar as informações para as novas ACEs. Cada **estrutura \_ EXPLICIT ACCESS** contém informações que descrevem uma única ACE. Essas informações incluem os direitos de acesso, o tipo de ACE, os sinalizadores que controlam a herança ACE e uma estrutura [**TRUSTEE**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) que identifica o usuário confiável.

**Para adicionar uma nova ACE a uma ACL existente**

1.  Use a [**função GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) ou [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) para obter a DACL ou SACL existente do [*descritor de segurança de um objeto*](/windows/desktop/SecGloss/s-gly).
2.  Para cada nova ACE, chame a [**função BuildExplicitAccessWithName**](/windows/desktop/api/Aclapi/nf-aclapi-buildexplicitaccesswithnamea) para preencher uma estrutura [**EXPLICIT \_ ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) com as informações que descrevem a ACE.
3.  Chame [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla), especificando a ACL existente e uma matriz de estruturas [**EXPLICIT \_ ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) para as novas ACEs. A **função SetEntriesInAcl** aloca e inicializa a ACL e suas ACEs.
4.  Chame a [**função SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) ou [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) para anexar a nova ACL ao descritor de segurança do objeto.

Se o chamador especificar uma ACL existente, [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) mescla as novas informações ACE com as ACEs existentes na ACL. Considere o caso, por exemplo, em que a ACL existente concede acesso a um trustee especificado e uma estrutura [**\_ EXPLICIT ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) nega acesso ao mesmo trustee. Nesse caso, **SetEntriesInAcl** adiciona uma nova ACE de acesso negado para o usuário confiável e exclui ou modifica a ACE com acesso permitido existente para o usuário confiável.

Para o código de exemplo que mescla uma nova ACE em uma ACL existente, consulte Modificando as [ACLs de um objeto em C++.](modifying-the-acls-of-an-object-in-c--.md)

 

 
