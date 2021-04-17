---
description: A enumeração de nível de representação de segurança \_ \_ define quatro níveis de representação que determinam as operações que um servidor pode executar no contexto de clientes.
ms.assetid: ae152dbf-44f0-417f-a85e-09bf60dcfcb0
title: Níveis de representação (autorização)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b91654f42a86e5c47069197bed084df56f5445dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769194"
---
# <a name="impersonation-levels-authorization"></a>Níveis de representação (autorização)

A enumeração de [**\_ \_ nível de representação de segurança**](/windows/desktop/api/Winnt/ne-winnt-security_impersonation_level) define quatro níveis de representação que determinam as operações que um servidor pode executar no contexto do cliente.



| Nível de representação    | Descrição                                                                                      |
|------------------------|--------------------------------------------------------------------------------------------------|
| SecurityAnonymous      | O servidor não pode representar ou identificar o cliente.                                            |
| SecurityIdentification | O servidor pode obter a identidade e os privilégios do cliente, mas não pode representar o cliente. |
| SecurityImpersonation  | O servidor pode representar o contexto de segurança do cliente no sistema local.                    |
| SecurityDelegation     | O servidor pode representar o contexto de segurança do cliente em sistemas remotos.                      |



 

O cliente de um pipe nomeado, RPC ou conexão DDE pode controlar o nível de representação. Por exemplo, um cliente de pipe nomeado pode chamar a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir um identificador para um pipe nomeado e especificar o nível de representação do servidor.

Quando o pipe nomeado, RPC ou conexão DDE é remoto, os sinalizadores passados para [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para definir o nível de representação são ignorados. Nesse caso, o nível de representação do cliente é determinado pelos níveis de representação habilitados pelo servidor, que é definido por um sinalizador na conta do servidor no serviço de diretório. Por exemplo, se o servidor estiver habilitado para delegação, o nível de representação do cliente também será definido como delegação, mesmo que os sinalizadores passados para **CreateFile** especifiquem o nível de representação de identificação.

Os clientes DDE usam a função [**DdeSetQualityOfService**](/windows/win32/api/dde/nf-dde-ddesetqualityofservice) com a estrutura [**\_ \_ de qualidade de \_ serviço de segurança**](/windows/desktop/api/Winnt/ns-winnt-security_quality_of_service) para especificar o nível de representação. O nível de SecurityImpersonation é o padrão para servidores de pipe nomeado, RPC e DDE. As funções [**ImpersonateSelf**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateself), [**DuplicateToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetoken)e [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) permitem que o chamador especifique um nível de representação. Use a função [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) para recuperar o nível de representação de um [*token de acesso*](/windows/desktop/SecGloss/a-gly).

No nível de SecurityImpersonation, a maioria das ações do thread ocorre no contexto de segurança do [*token de representação*](/windows/desktop/SecGloss/i-gly) do thread, em vez de no [*token primário*](/windows/desktop/SecGloss/p-gly) do [*processo*](/windows/desktop/SecGloss/p-gly) que possui o thread. Por exemplo, se um thread de representação abrir um [objeto protegível](securable-objects.md), o sistema usará o token de representação para verificar o acesso do thread. Da mesma forma, se um thread de representação criar um novo objeto, por exemplo, chamando a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) , o proprietário do novo objeto será o proprietário padrão do [*token de acesso*](/windows/desktop/SecGloss/a-gly)do cliente.

No entanto, o sistema usa o token primário do processo em vez do token de representação do thread de chamada nas seguintes situações:

-   Se um thread de representação chamar a função [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) , o novo processo sempre herdará o token primário do processo.
-   Para funções que exigem o \_ privilégio de \_ nome TCB se, como a função [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) , o sistema sempre verifica o privilégio no token primário do processo.
-   Para funções que exigem o \_ privilégio de nome de auditoria se \_ , como a função [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) , o sistema sempre verifica o privilégio no token primário do processo.
-   Em uma chamada para a função [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) , um thread pode especificar se a função usa o token de representação ou o token primário para determinar se deve conceder o acesso solicitado.

 

 
