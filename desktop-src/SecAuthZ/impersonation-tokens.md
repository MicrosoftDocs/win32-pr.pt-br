---
description: Explica o uso de tokens de representação no controle de acesso.
ms.assetid: 74fcb0e3-303a-4a5e-9eb6-2aad3a4944db
title: Tokens de representação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f468a4c7a9c6ff04a4481ffe7347e227a447db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755967"
---
# <a name="impersonation-tokens"></a>Tokens de representação

Um thread de representação tem dois [*tokens de acesso*](/windows/desktop/SecGloss/a-gly):

-   Um [*token de acesso primário*](/windows/desktop/SecGloss/p-gly) que descreve o [*contexto de segurança*](/windows/desktop/SecGloss/s-gly) do servidor. Para obter um identificador para esse token, chame a função [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) .
-   Um token de acesso de representação que descreve o contexto de segurança do cliente que está sendo representado. Para obter um identificador para esse token, chame a função [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) .

Um servidor pode usar o [*token de representação*](/windows/desktop/SecGloss/i-gly) nas seguintes funções:

-   Nas funções [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck), [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype)e [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) para determinar se um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) permite ao cliente um conjunto de direitos de acesso.
-   Na função [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) para habilitar ou desabilitar os privilégios do cliente.
-   Na função [**PrivilegeCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) para determinar se um conjunto de privilégios está habilitado no token do cliente.
-   Em funções que geram entradas no log de eventos de segurança, como [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) ou [**PrivilegedServiceAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma). Essas funções usam um token de representação para obter informações sobre o cliente para a entrada de log.

 

 
