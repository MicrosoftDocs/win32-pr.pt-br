---
description: Os direitos de conta determinam o tipo de logon que uma conta de usuário pode executar. Um administrador atribui direitos de conta a contas de usuário e de grupo. Os direitos de conta de cada usuário incluem aqueles concedidos ao usuário e aos grupos aos quais o usuário pertence.
ms.assetid: 42139d33-2d56-4d29-998f-5512bb795d44
title: Constantes de direitos de conta (Ntsecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4285561761908308f67585544bef6c87d2f0ebbaa25de9989f53fcab051b79b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785358"
---
# <a name="account-rights-constants"></a>Constantes de direitos de conta

Os direitos de conta determinam o tipo de logon que uma conta de usuário pode executar. Um administrador atribui direitos de conta a contas de usuário e de grupo. Os direitos de conta de cada usuário incluem aqueles concedidos ao usuário e aos grupos aos quais o usuário pertence.

Um administrador de sistema pode usar as funções de [*autoridade de segurança local*](/windows/desktop/SecGloss/l-gly) (LSA) para trabalhar com direitos de conta. As funções [**LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) e [**LsaRemoveAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaremoveaccountrights) adicionam ou removem direitos de conta de uma conta. A função [**LsaEnumerateAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountrights) enumera os direitos de conta mantidos por uma conta especificada. A função [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright) enumera as contas que mantêm um direito de conta especificada.

As constantes de conta a seguir são usadas para controlar a capacidade de logon de uma conta. As funções [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) ou [**LsaLogonUser**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser) falharão se a conta que está sendo conectada não tiver os direitos de conta necessários para o tipo de logon que está sendo executado.



| Constante/valor                                                                                                                                                                                                                                                                                                                           | Descrição                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| <span id="SE_BATCH_LOGON_NAME"></span><span id="se_batch_logon_name"></span><dl> <dt>**ES \_ Texto \_ do \_ nome de logon em lotes**</dt> <dt>("SeBatchLogonRight")</dt> </dl>                                                                         | Necessário para que uma conta faça logon usando o tipo de logon do lote.<br/>                               |
| <span id="SE_DENY_BATCH_LOGON_NAME"></span><span id="se_deny_batch_logon_name"></span><dl> <dt>**ES \_ NEGAR texto de \_ \_ \_ nome de logon em lotes**</dt> <dt>("SeDenyBatchLogonRight")</dt> </dl>                                                     | Nega explicitamente uma conta do direito de fazer logon usando o tipo de logon do lote.<br/>                |
| <span id="SE_DENY_INTERACTIVE_LOGON_NAME"></span><span id="se_deny_interactive_logon_name"></span><dl> <dt>**ES \_ NEGAR texto de \_ \_ \_ nome de logon interativo**</dt> <dt>("SeDenyInteractiveLogonRight")</dt> </dl>                             | Nega explicitamente uma conta do direito de fazer logon usando o tipo de logon interativo.<br/>          |
| <span id="SE_DENY_NETWORK_LOGON_NAME"></span><span id="se_deny_network_logon_name"></span><dl> <dt>**ES \_ NEGAR texto de \_ \_ \_ nome de logon de rede**</dt> <dt>("SeDenyNetworkLogonRight")</dt> </dl>                                             | Nega explicitamente uma conta do direito de fazer logon usando o tipo de logon de rede.<br/>              |
| <span id="SE_DENY_REMOTE_INTERACTIVE_LOGON_NAME"></span><span id="se_deny_remote_interactive_logon_name"></span><dl> <dt>**ES \_ NEGAR texto de \_ \_ \_ \_ nome de logon interativo remoto**</dt> <dt>("SeDenyRemoteInteractiveLogonRight")</dt> </dl> | Nega explicitamente uma conta do direito de fazer logon remotamente usando o tipo de logon interativo.<br/> |
| <span id="SE_DENY_SERVICE_LOGON_NAME"></span><span id="se_deny_service_logon_name"></span><dl> <dt>**ES \_ NEGAR texto do \_ \_ \_ nome de logon do serviço**</dt> <dt>("SeDenyServiceLogonRight")</dt> </dl>                                             | Nega explicitamente uma conta do direito de fazer logon usando o tipo de logon do serviço.<br/>              |
| <span id="SE_INTERACTIVE_LOGON_NAME"></span><span id="se_interactive_logon_name"></span><dl> <dt>**ES \_ Texto \_ do \_ nome de logon interativo**</dt> <dt>("SeInteractiveLogonRight")</dt> </dl>                                                 | Necessário para que uma conta faça logon usando o tipo de logon interativo.<br/>                         |
| <span id="SE_NETWORK_LOGON_NAME"></span><span id="se_network_logon_name"></span><dl> <dt>**ES \_ Texto \_ do \_ nome de logon de rede**</dt> <dt>("SeNetworkLogonRight")</dt> </dl>                                                                 | Necessário para que uma conta faça logon usando o tipo de logon de rede.<br/>                             |
| <span id="SE_REMOTE_INTERACTIVE_LOGON_NAME"></span><span id="se_remote_interactive_logon_name"></span><dl> <dt>**ES \_ Texto \_ do \_ \_ nome de logon interativo remoto**</dt> <dt>("SeRemoteInteractiveLogonRight")</dt> </dl>                     | Necessário para que uma conta faça logon remotamente usando o tipo de logon interativo.<br/>                |
| <span id="SE_SERVICE_LOGON_NAME"></span><span id="se_service_logon_name"></span><dl> <dt>**ES \_ Texto \_ do \_ nome de logon do serviço**</dt> <dt>("SeServiceLogonRight")</dt> </dl>                                                                 | Necessário para que uma conta faça logon usando o tipo de logon do serviço.<br/>                             |



## <a name="remarks"></a>Comentários

os \_ direitos de negação de ES substituem os direitos de conta correspondentes. um administrador pode atribuir um \_ direito de negação de ES a uma conta para substituir quaisquer direitos de logon que uma conta possa ter como resultado de uma associação de grupo. por exemplo, você pode atribuir o \_ direito de nome de logon de rede ES \_ \_ a todos, mas atribuir o \_ direito de nome de logon de rede ES negar \_ \_ \_ aos administradores para impedir a administração remota de computadores.

Todas as funções LSA mencionadas na introdução acima oferecem suporte a direitos e [privilégios](privilege-constants.md)de conta. Ao contrário dos privilégios, no entanto, os direitos de conta não são suportados pelas funções [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) e [**LookupPrivilegeName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) . A função [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) obterá informações sobre os direitos de conta se tokenGroups, e não TokenPrivileges, for especificado como o valor do parâmetro *TokenInformationClass* .

As constantes da conta precedentes são definidas como cadeias de caracteres em Ntsecapi. h. por exemplo, a \_ constante de nome de LOGON interativo ES \_ \_ é definida como "SeInteractiveLogonRight".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Ntsecapi. h</dt> </dl> |



 

