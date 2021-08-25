---
description: Explica o uso de tokens de representação no controle de acesso.
ms.assetid: 74fcb0e3-303a-4a5e-9eb6-2aad3a4944db
title: Tokens de representação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67acf48a1f274703850fc8bfc2167014708124c46743f416591510b6c9ab559b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908136"
---
# <a name="impersonation-tokens"></a>Tokens de representação

Um thread de representação tem dois [*tokens de acesso:*](/windows/desktop/SecGloss/a-gly)

-   Um [*token de acesso*](/windows/desktop/SecGloss/p-gly) primário que descreve o contexto de [*segurança*](/windows/desktop/SecGloss/s-gly) do servidor. Para obter um handle para esse token, chame a [**função OpenProcessToken.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)
-   Um token de acesso de representação que descreve o contexto de segurança do cliente que está sendo personificado. Para obter um handle para esse token, chame a [**função OpenThreadToken.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken)

Um servidor pode usar [*o token de representação*](/windows/desktop/SecGloss/i-gly) nas seguintes funções:

-   Nas funções [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck), [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype)e [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) para determinar se um descritor [*de*](/windows/desktop/SecGloss/s-gly) segurança permite ao cliente um conjunto de direitos de acesso.
-   Na função [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) para habilitar ou desabilitar os privilégios do cliente.
-   Na função [**PrivilegeCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) para determinar se um conjunto de privilégios está habilitado no token do cliente.
-   Em funções que geram entradas no log de eventos de segurança, como [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) ou [**PrivilegedServiceAuditAlarm.**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma) Essas funções usam um token de representação para obter informações sobre o cliente para a entrada de log.

 

 
