---
description: Um token de acesso é um objeto que descreve o contexto de segurança de um processo ou thread.
ms.assetid: 350159c9-2399-427a-ba44-c897a9664299
title: Tokens de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0993c1f5aebab797ab28e61b36f59507e4d2f1ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828831"
---
# <a name="access-tokens"></a>Tokens de acesso

Um [*token de acesso*](/windows/desktop/SecGloss/a-gly) é um objeto que descreve o [*contexto de segurança*](/windows/desktop/SecGloss/s-gly) de um [*processo*](/windows/desktop/SecGloss/p-gly) ou thread. As informações em um token incluem a identidade e os privilégios da conta de usuário associada ao processo ou thread. Quando um usuário faz logon, o sistema verifica a senha do usuário comparando-a com as informações armazenadas em um banco de dados de segurança. Se a senha for [*autenticada*](/windows/desktop/SecGloss/a-gly), o sistema produzirá um token de acesso. Cada processo executado em nome desse usuário tem uma cópia desse token de acesso.

O sistema usa um token de acesso para identificar o usuário quando um thread interage com um [objeto protegível](securable-objects.md) ou tenta executar uma tarefa do sistema que exige privilégios. Os tokens de acesso contêm as seguintes informações:

-   O [identificador de segurança](security-identifiers.md) (SID) da conta do usuário
-   SIDs para os grupos dos quais o usuário é membro
-   Um [*Sid de logon*](/windows/desktop/SecGloss/l-gly) que identifica a [*sessão de logon*](/windows/desktop/SecGloss/l-gly) atual
-   Uma lista dos [privilégios](privileges.md) mantidos pelo usuário ou pelos grupos do usuário
-   Um SID de proprietário
-   O SID do grupo primário
-   A [DACL](access-control-lists.md) padrão que o sistema usa quando o usuário cria um objeto protegível sem especificar um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly)
-   A origem do token de acesso
-   Se o token é um token [*primário*](/windows/desktop/SecGloss/p-gly) ou de [representação](client-impersonation.md)
-   Uma lista opcional de [restrição de SIDs](restricted-tokens.md)
-   Níveis de representação atuais
-   Outras estatísticas

Cada processo tem um [*token primário*](/windows/desktop/SecGloss/p-gly) que descreve o [*contexto de segurança*](/windows/desktop/SecGloss/s-gly) da conta de usuário associada ao processo. Por padrão, o sistema usa o token primário quando um thread do processo interage com um objeto protegível. Além disso, um thread pode representar uma conta de cliente. A representação permite que o thread interaja com objetos protegíveis usando o contexto de segurança do cliente. Um thread que está representando um cliente tem um token primário e um [*token de representação*](/windows/desktop/SecGloss/i-gly).

Use a função [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) para recuperar um identificador para o token primário de um processo. Use a função [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) para recuperar um identificador para o token de representação de um thread. Para obter mais informações, consulte [Impersonation](client-impersonation.md).

Você pode usar as seguintes funções para manipular tokens de acesso.



| Função                                               | Descrição                                                                                                                                                            |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdjustTokenGroups**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups)         | Altera as informações do grupo em um token de acesso.                                                                                                                      |
| [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) | Habilita ou desabilita os privilégios em um token de acesso. Ele não concede novos privilégios nem revoga os existentes.                                                       |
| [**CheckTokenMembership**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership)   | Determina se um SID especificado está habilitado em um token de acesso especificado.                                                                                             |
| [**CreateRestrictedToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) | Cria um novo token que é uma versão restrita de um token existente. O token restrito pode ter SIDs desabilitados, privilégios excluídos e uma lista de SIDs restritos. |
| [**DuplicateToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetoken)               | Cria um novo token de representação que duplica um token existente.                                                                                                   |
| [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)           | Cria um novo token primário ou token de representação que duplica um token existente.                                                                                  |
| [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)     | Recupera informações sobre um token.                                                                                                                                   |
| [**IsTokenRestricted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-istokenrestricted)         | Determina se um token tem uma lista de SIDs de restrição.                                                                                                             |
| [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)           | Recupera um identificador para o token de acesso primário de um processo.                                                                                                          |
| [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken)             | Recupera um identificador para o token de acesso de representação de um thread.                                                                                                     |
| [**SetThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadtoken)               | Atribui ou remove um token de representação para um thread.                                                                                                                |
| [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation)     | Altera o proprietário de um token, o grupo primário ou a DACL padrão.                                                                                                               |



 

As funções de token de acesso usam as seguintes estruturas para descrever as partes de um token de acesso.



| Estrutura                                            | Descrição                                                                                           |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**controle de TOKEN \_**](/windows/desktop/api/Winnt/ns-winnt-token_control)              | Informações que identificam um token de acesso.                                                          |
| [**\_DACL padrão do token \_**](/windows/desktop/api/Winnt/ns-winnt-token_default_dacl)   | A DACL padrão que o sistema usa nos descritores de segurança de novos objetos criados por um thread. |
| [**grupos de TOKENs \_**](/windows/desktop/api/Winnt/ns-winnt-token_groups)                | Especifica os SIDs e atributos dos SIDs de grupo em um token de acesso.                               |
| [**proprietário do TOKEN \_**](/windows/desktop/api/Winnt/ns-winnt-token_owner)                  | O SID do proprietário padrão para os descritores de segurança dos novos objetos.                                    |
| [**\_grupo primário de tokens \_**](/windows/desktop/api/Winnt/ns-winnt-token_primary_group) | O SID do grupo primário padrão para os descritores de segurança dos novos objetos.                            |
| [**privilégios de TOKEN \_**](/windows/desktop/api/Winnt/ns-winnt-token_privileges)        | Os privilégios associados a um token de acesso. Também determina se os privilégios estão habilitados.   |
| [**origem do TOKEN \_**](/windows/desktop/api/Winnt/ns-winnt-token_source)                | A origem de um token de acesso.                                                                        |
| [**Estatísticas de TOKEN \_**](/windows/desktop/api/Winnt/ns-winnt-token_statistics)        | Estatísticas associadas a um token de acesso.                                                           |
| [**usuário do TOKEN \_**](/windows/desktop/api/Winnt/ns-winnt-token_user)                    | O SID do usuário associado a um token de acesso.                                                  |



 

As funções de token de acesso usam os seguintes tipos de enumeração.



| Tipo de enumeração                                             | Especifica                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**\_classe de informações de token \_**](/windows/desktop/api/Winnt/ne-winnt-token_information_class) | Identifica o tipo de informações que estão sendo definidas ou recuperadas de um token de acesso. |
| [**tipo de TOKEN \_**](/windows/desktop/api/Winnt/ne-winnt-token_type)                            | Identifica um token de acesso como um token primário ou de representação.                 |



 

 

 
