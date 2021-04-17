---
description: O direito de acesso de segurança do sistema de acesso \_ \_ controla a capacidade de obter ou definir a SACL em um descritor de segurança de objetos. O sistema concede esse direito de acesso se o \_ privilégio nome de segurança se \_ estiver habilitado no token de acesso do thread solicitante.
ms.assetid: 88198243-dae5-49ac-9d54-bfae7a3a0b1a
title: Direito de acesso à SACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2366f30748a93294d4f30122102d656fb2590d34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754961"
---
# <a name="sacl-access-right"></a>Direito de acesso à SACL

O direito de acesso de segurança do sistema de acesso \_ \_ controla a capacidade de obter ou definir a SACL no [*descritor de segurança*](/windows/desktop/SecGloss/s-gly)de um objeto. O sistema concede esse direito de acesso somente se o \_ privilégio nome de segurança se \_ estiver habilitado no [*token de acesso*](/windows/desktop/SecGloss/a-gly) do thread solicitante.

**Para acessar a SACL de um objeto**

1.  Chame a função [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) para habilitar o \_ privilégio de nome de segurança se \_ .
2.  Solicite o \_ \_ direito acesso de segurança do sistema ao abrir um identificador para o objeto.
3.  Obtenha ou defina a SACL do objeto usando uma função como [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) ou [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo).
4.  Chame [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) para desabilitar o \_ privilégio nome de segurança se \_ .

Para acessar uma SACL usando as funções [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) ou [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) , habilite o \_ privilégio nome de segurança se \_ . A função solicita o direito de acesso internamente.

O direito de acesso de segurança do sistema de acesso \_ \_ não é válido em uma DACL porque as DACLs não controlam o acesso a uma SACL. No entanto, você pode usar o direito de acesso de segurança do sistema de acesso \_ \_ em uma SACL para auditar tentativas de usar o direito de acesso.

 

 
