---
description: Um token de acesso é um objeto que descreve o contexto de segurança de um processo ou thread.
ms.assetid: 350159c9-2399-427a-ba44-c897a9664299
title: Tokens de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9067df376006f7f7b61dedadc074c23674b2278fb5c311794bbddd12256277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785385"
---
# <a name="access-tokens"></a>Tokens de acesso

Um [*token de*](/windows/desktop/SecGloss/a-gly) acesso é um objeto que descreve o contexto de [*segurança*](/windows/desktop/SecGloss/s-gly) de um [*processo*](/windows/desktop/SecGloss/p-gly) ou thread. As informações em um token incluem a identidade e os privilégios da conta de usuário associada ao processo ou thread. Quando um usuário faz o login, o sistema verifica a senha do usuário comparando-a com as informações armazenadas em um banco de dados de segurança. Se a senha for [*autenticada,*](/windows/desktop/SecGloss/a-gly)o sistema produzirá um token de acesso. Cada processo executado em nome desse usuário tem uma cópia desse token de acesso.

O sistema usa um token de acesso para identificar [](securable-objects.md) o usuário quando um thread interage com um objeto de segurança ou tenta executar uma tarefa do sistema que requer privilégios. Os tokens de acesso contêm as seguintes informações:

-   O [SID (identificador de](security-identifiers.md) segurança) da conta do usuário
-   SIDs para os grupos dos quais o usuário é membro
-   Um [*SID de logon*](/windows/desktop/SecGloss/l-gly) que identifica a sessão [*de logon atual*](/windows/desktop/SecGloss/l-gly)
-   Uma lista dos [privilégios mantidos](privileges.md) pelo usuário ou pelos grupos do usuário
-   Um SID de proprietário
-   O SID do grupo primário
-   A [DACL padrão](access-control-lists.md) que o sistema usa quando o usuário cria um objeto seguro sem especificar um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly)
-   A origem do token de acesso
-   Se o token é um [*token primário*](/windows/desktop/SecGloss/p-gly) ou [de representação](client-impersonation.md)
-   Uma lista opcional de [restrição de SIDs](restricted-tokens.md)
-   Níveis de representação atuais
-   Outras estatísticas

Cada processo tem [*um token primário*](/windows/desktop/SecGloss/p-gly) que descreve o contexto de [*segurança*](/windows/desktop/SecGloss/s-gly) da conta de usuário associada ao processo. Por padrão, o sistema usa o token primário quando um thread do processo interage com um objeto securável. Além disso, um thread pode representar uma conta de cliente. A representação permite que o thread interaja com objetos que podem sercuráveis usando o contexto de segurança do cliente. Um thread que está representando um cliente tem um token primário e um [*token de representação*](/windows/desktop/SecGloss/i-gly).

Use a [**função OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) para recuperar um handle para o token primário de um processo. Use a [**função OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) para recuperar um alça para o token de representação de um thread. Para obter mais informações, consulte [Representação](client-impersonation.md).

Você pode usar as funções a seguir para manipular tokens de acesso.



| Função                                               | Descrição                                                                                                                                                            |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdjustTokenGroups**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups)         | Altera as informações do grupo em um token de acesso.                                                                                                                      |
| [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) | Habilita ou desabilita os privilégios em um token de acesso. Ele não concede novos privilégios nem revoga os existentes.                                                       |
| [**CheckTokenMembership**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership)   | Determina se um SID especificado está habilitado em um token de acesso especificado.                                                                                             |
| [**Createrestrictedtoken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) | Cria um novo token que é uma versão restrita de um token existente. O token restrito pode ter sids desabilitados, privilégios excluídos e uma lista de SIDs restritos. |
| [**DuplicateToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetoken)               | Cria um novo token de representação que duplica um token existente.                                                                                                   |
| [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)           | Cria um novo token primário ou token de representação que duplica um token existente.                                                                                  |
| [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)     | Recupera informações sobre um token.                                                                                                                                   |
| [**IsTokenRestricted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-istokenrestricted)         | Determina se um token tem uma lista de restrições de SIDs.                                                                                                             |
| [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)           | Recupera um alça para o token de acesso primário para um processo.                                                                                                          |
| [**Openthreadtoken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken)             | Recupera um alça para o token de acesso de representação para um thread.                                                                                                     |
| [**Setthreadtoken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadtoken)               | Atribui ou remove um token de representação para um thread.                                                                                                                |
| [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation)     | Altera o proprietário, o grupo primário ou a DACL padrão de um token.                                                                                                               |



 

As funções de token de acesso usam as estruturas a seguir para descrever as partes de um token de acesso.



| Estrutura                                            | Descrição                                                                                           |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**CONTROLE \_ DE TOKEN**](/windows/desktop/api/Winnt/ns-winnt-token_control)              | Informações que identificam um token de acesso.                                                          |
| [**\_ \_ DACL PADRÃO DO TOKEN**](/windows/desktop/api/Winnt/ns-winnt-token_default_dacl)   | A DACL padrão que o sistema usa nos descritores de segurança de novos objetos criados por um thread. |
| [**GRUPOS DE \_ TOKENS**](/windows/desktop/api/Winnt/ns-winnt-token_groups)                | Especifica os SIDs e atributos dos SIDs de grupo em um token de acesso.                               |
| [**PROPRIETÁRIO \_ DO TOKEN**](/windows/desktop/api/Winnt/ns-winnt-token_owner)                  | O SID do proprietário padrão para os descritores de segurança de novos objetos.                                    |
| [**GRUPO \_ PRIMÁRIO \_ DO TOKEN**](/windows/desktop/api/Winnt/ns-winnt-token_primary_group) | O SID do grupo primário padrão para os descritores de segurança de novos objetos.                            |
| [**PRIVILÉGIOS \_ DE TOKEN**](/windows/desktop/api/Winnt/ns-winnt-token_privileges)        | Os privilégios associados a um token de acesso. Também determina se os privilégios estão habilitados.   |
| [**ORIGEM \_ DO TOKEN**](/windows/desktop/api/Winnt/ns-winnt-token_source)                | A origem de um token de acesso.                                                                        |
| [**ESTATÍSTICAS \_ DE TOKEN**](/windows/desktop/api/Winnt/ns-winnt-token_statistics)        | Estatísticas associadas a um token de acesso.                                                           |
| [**USUÁRIO \_ DO TOKEN**](/windows/desktop/api/Winnt/ns-winnt-token_user)                    | O SID do usuário associado a um token de acesso.                                                  |



 

As funções de token de acesso usam os seguintes tipos de enumeração.



| Tipo de enumeração                                             | Especifica                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**CLASSE \_ DE INFORMAÇÕES DE \_ TOKEN**](/windows/desktop/api/Winnt/ne-winnt-token_information_class) | Identifica o tipo de informação que está sendo definida ou recuperada de um token de acesso. |
| [**TIPO \_ DE TOKEN**](/windows/desktop/api/Winnt/ne-winnt-token_type)                            | Identifica um token de acesso como um token primário ou de representação.                 |



 

 

 
