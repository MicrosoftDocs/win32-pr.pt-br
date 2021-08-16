---
description: O direito de acesso de segurança do sistema de acesso \_ \_ controla a capacidade de obter ou definir a SACL em um descritor de segurança de objetos. o sistema concederá esse direito de acesso se o privilégio de nome de segurança de ES \_ \_ estiver habilitado no token de acesso do thread solicitante.
ms.assetid: 88198243-dae5-49ac-9d54-bfae7a3a0b1a
title: Direito de acesso à SACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88256664db25c6e906f3b4ca0459217a29d0cc7c0e2dd544c1cf198bc24fff5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780511"
---
# <a name="sacl-access-right"></a>Direito de acesso à SACL

O direito de acesso de segurança do sistema de acesso \_ \_ controla a capacidade de obter ou definir a SACL no [*descritor de segurança*](/windows/desktop/SecGloss/s-gly)de um objeto. o sistema concederá esse direito de acesso somente se o \_ privilégio de nome de segurança de ES \_ estiver habilitado no [*token de acesso*](/windows/desktop/SecGloss/a-gly) do thread solicitante.

**Para acessar a SACL de um objeto**

1.  chame a função [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) para habilitar o privilégio de ES \_ nome de segurança \_ .
2.  Solicite o \_ \_ direito acesso de segurança do sistema ao abrir um identificador para o objeto.
3.  Obtenha ou defina a SACL do objeto usando uma função como [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) ou [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo).
4.  chame [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) para desabilitar o \_ privilégio de nome de segurança ES \_ .

para acessar uma SACL usando as funções [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) ou [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) , habilite o \_ privilégio ES nome de segurança \_ . A função solicita o direito de acesso internamente.

O direito de acesso de segurança do sistema de acesso \_ \_ não é válido em uma DACL porque as DACLs não controlam o acesso a uma SACL. No entanto, você pode usar o direito de acesso de segurança do sistema de acesso \_ \_ em uma SACL para auditar tentativas de usar o direito de acesso.

 

 
