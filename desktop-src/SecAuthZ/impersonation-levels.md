---
description: A enumeração SECURITY IMPERSONATION LEVEL define quatro níveis de representação que determinam as operações que um \_ servidor pode executar no contexto de \_ clientes.
ms.assetid: ae152dbf-44f0-417f-a85e-09bf60dcfcb0
title: Níveis de representação (autorização)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdf80f4f6b84499a94659c137c629d66a041752e5171cb3fa7220506586f36e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414586"
---
# <a name="impersonation-levels-authorization"></a>Níveis de representação (autorização)

A [**\_ enumeração SECURITY IMPERSONATION \_ LEVEL**](/windows/desktop/api/Winnt/ne-winnt-security_impersonation_level) define quatro níveis de representação que determinam as operações que um servidor pode executar no contexto do cliente.



| Nível de representação    | Descrição                                                                                      |
|------------------------|--------------------------------------------------------------------------------------------------|
| SecurityAnonymous      | O servidor não pode representar ou identificar o cliente.                                            |
| SecurityIdentification | O servidor pode obter a identidade e os privilégios do cliente, mas não pode representar o cliente. |
| SecurityImpersonation  | O servidor pode representar o contexto de segurança do cliente no sistema local.                    |
| SecurityDelegation     | O servidor pode representar o contexto de segurança do cliente em sistemas remotos.                      |



 

O cliente de um pipe nomeado, RPC ou conexão DDE pode controlar o nível de representação. Por exemplo, um cliente de pipe nomeado pode chamar a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir um identificador para um pipe nomeado e especificar o nível de representação do servidor.

Quando a conexão de pipe, RPC ou DDE nomeada é remota, os sinalizadores passados para [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para definir o nível de representação são ignorados. Nesse caso, o nível de representação do cliente é determinado pelos níveis de representação habilitados pelo servidor, que é definido por um sinalizador na conta do servidor no serviço de diretório. Por exemplo, se o servidor estiver habilitado para delegação, o nível de representação do cliente também será definido como delegação, mesmo que os sinalizadores passados para **CreateFile** especifiquem o nível de representação de identificação.

Os clientes DDE usam a [**função DdeSetQualityOfService**](/windows/win32/api/dde/nf-dde-ddesetqualityofservice) com a estrutura [**SECURITY QUALITY OF \_ \_ \_ SERVICE**](/windows/desktop/api/Winnt/ns-winnt-security_quality_of_service) para especificar o nível de representação. O nível SecurityImpersonation é o padrão para servidores DDE, RPC e pipe nomeados. As [**funções ImpersonateSelf,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateself) [**DuplicateToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetoken)e [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) permitem que o chamador especifique um nível de representação. Use a [**função GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) para recuperar o nível de representação de um [*token de acesso*](/windows/desktop/SecGloss/a-gly).

No nível SecurityImpersonation, a maioria das ações do thread ocorre no contexto de segurança do token [](/windows/desktop/SecGloss/p-gly) de representação do [*thread,*](/windows/desktop/SecGloss/i-gly) em vez de no [*token*](/windows/desktop/SecGloss/p-gly) primário do processo que possui o thread. Por exemplo, se um thread de representação abrir um objeto de segurança [,](securable-objects.md)o sistema usará o token de representação para verificar o acesso do thread. Da mesma forma, se um thread de representação criar um novo objeto, por exemplo, chamando a função [**CreateFile,**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) o proprietário do novo objeto será o proprietário padrão do token de [*acesso do cliente.*](/windows/desktop/SecGloss/a-gly)

No entanto, o sistema usa o token primário do processo em vez do token de representação do thread de chamada nas seguintes situações:

-   Se um thread de representação chamar a [**função CreateProcess,**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) o novo processo sempre herdará o token primário do processo.
-   Para funções que exigem o privilégio ES TCB NAME, como a função \_ \_ [**LogonUser,**](/windows/desktop/api/winbase/nf-winbase-logonusera) o sistema sempre verifica o privilégio no token primário do processo.
-   Para funções que exigem ES privilégio AUDIT NAME, como a função \_ \_ [**ObjectOpenAuditAlarm,**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) o sistema sempre verifica o privilégio no token primário do processo.
-   Em uma chamada para a [**função OpenThreadToken,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) um thread pode especificar se a função usa o token de representação ou o token primário para determinar se o acesso solicitado deve ser concedido.

 

 
