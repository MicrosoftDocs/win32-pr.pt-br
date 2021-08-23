---
description: Crie uma ACL (lista de controle de acesso) usando as funções de nível baixo, aloque um buffer para a ACL e, em seguida, inicialize-o chamando a função InitializeAcl.
ms.assetid: 9dcbbd4c-b3b3-43fd-b3a6-0637a53a455a
title: Funções de ACL e ACE de nível baixo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dab8c968c19e652f530abe25aaae11e47f36db1cd6ea7184120987c63a1bd9b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670656"
---
# <a name="low-level-acl-and-ace-functions"></a>Funções de ACL e ACE de nível baixo

Para criar uma ACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) usando as funções de nível baixo, aloque um buffer para a ACL e, em seguida, inicialize-o chamando a função [**InitializeAcl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializeacl) . Para adicionar ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) ao final de uma DACL (lista de controle de [*acesso discricionário*](/windows/desktop/SecGloss/d-gly) ), use as funções [**AddAccessAllowedAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace) e [**AddAccessDeniedAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedace) . A função [**AddAuditAccessAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addauditaccessace) adiciona uma ACE ao final de uma SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema. Você pode usar a função [**AddAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace) para adicionar uma ou mais ACEs em uma posição especificada em uma ACL. A função **AddAce** também permite que você adicione uma ACE herdável a uma ACL. A função [**DeleteAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-deleteace) remove uma ACE de uma posição especificada em uma ACL. A função [**GetAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getace) recupera uma ACE de uma posição especificada em uma ACL. A função [**FindFirstFreeAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-findfirstfreeace) recupera um ponteiro para o primeiro byte livre em uma ACL.

Para modificar uma ACL existente no [*descritor de segurança*](/windows/desktop/SecGloss/s-gly)de um objeto, use a função [**GetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl) ou [**GetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl) para obter a ACL existente. Você pode usar a função [**GetAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getace) para copiar Aces da ACL existente. Depois de alocar e inicializar uma nova ACL, use funções como [**AddAccessAllowedAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace) e [**AddAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace) para adicionar ACEs a ela. Quando você terminar de criar a nova ACL, use a função [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) ou [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl) para adicionar a nova ACL ao descritor de segurança do objeto.

Você pode usar as funções [**AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace), [**AddAccessDeniedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedobjectace)ou [**AddAuditAccessObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addauditaccessobjectace) para adicionar [ACEs específicas do objeto](object-specific-aces.md) ao final de uma ACL.

 

 
