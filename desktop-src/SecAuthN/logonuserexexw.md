---
description: A função LogonUserExExW tenta fazer logon de um usuário no computador local.
ms.assetid: d90db4c6-a711-4519-8b91-5069cee07738
title: Função LogonUserExExW (Winbasep. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LogonUserExExW
api_type:
- DllExport
api_location:
- Advapi32.dll
ms.openlocfilehash: 35ec65e7899f45a5222ae12b08992e77ea67f306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011525"
---
# <a name="logonuserexexw-function"></a>Função LogonUserExExW

A função **LogonUserExExW** tenta fazer logon de um usuário no computador local. O computador local é o computador do qual **LogonUserExExW** foi chamado. Você não pode usar o **LogonUserExExW** para fazer logon em um computador remoto. Especifique o usuário usando um nome de usuário e um domínio e [*autentique*](../secgloss/a-gly.md) o usuário usando uma senha de texto sem formatação. Se a função for realizada com sucesso, ela receberá um identificador para um token que representa o usuário conectado. Você pode usar esse identificador de token para representar o usuário especificado ou, na maioria dos casos, para criar um [*processo*](../secgloss/p-gly.md) que é executado no contexto do usuário especificado.

Essa função é semelhante à função [**LogonUserEx**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa) , exceto pelo fato de que ela usa o parâmetro adicional, *pTokenGroups*, que é um conjunto de um ou mais SIDs ( [*identificadores de segurança*](../secgloss/s-gly.md) ) que são adicionados ao token retornado ao chamador quando o logon é bem-sucedido.

Essa função não é declarada em um cabeçalho público e não tem biblioteca de importação associada. Você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Advapi32.dll.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI LogonUserExExW(
  _In_      LPTSTR        lpszUsername,
  _In_opt_  LPTSTR        lpszDomain,
  _In_opt_  LPTSTR        lpszPassword,
  _In_      DWORD         dwLogonType,
  _In_      DWORD         dwLogonProvider,
  _In_opt_  PTOKEN_GROUPS pTokenGroups,
  _Out_opt_ PHANDLE       phToken,
  _Out_opt_ PSID          *ppLogonSid,
  _Out_opt_ PVOID         *ppProfileBuffer,
  _Out_opt_ LPDWORD       pdwProfileLength,
  _Out_opt_ PQUOTA_LIMITS pQuotaLimits
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszUsername* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do usuário. Esse é o nome da conta de usuário para fazer logon. Se você usar o formato UPN ( [*nome principal do usuário*](../secgloss/u-gly.md) ), o parâmetro *LpszDomain* deverá ser **nulo**.

</dd> <dt>

*lpszDomain* \[ em, opcional\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do domínio ou do servidor cujo banco de dados de conta contém a conta *lpszUsername* . Se esse parâmetro for **nulo**, o nome de usuário deverá ser especificado no formato UPN. Se esse parâmetro for ".", a função validará a conta usando apenas o banco de dados de conta local.

</dd> <dt>

*lpszPassword* \[ em, opcional\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica a senha de texto não criptografado para a conta de usuário especificada por *lpszUsername*. Quando você terminar de usar a senha, limpe a senha da memória chamando a função [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) . Para obter mais informações sobre como proteger senhas, consulte [manipulando senhas](../secbp/handling-passwords.md).

</dd> <dt>

*dwLogonType* \[ no\]
</dt> <dd>

O tipo de operação de logon a ser executada. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                        | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_LOGON_INTERACTIVE"></span><span id="logon32_logon_interactive"></span><dl> <dt>**LOGON32 \_ LOGON \_ interativo**</dt> <dt>2</dt> </dl>                    | Esse tipo de logon destina-se a usuários que irão usar o computador interativamente, como um usuário conectado por um servidor de [*terminal*](../secgloss/t-gly.md) , um shell remoto ou um processo semelhante. Esse tipo de logon tem as despesas adicionais de armazenar em cache informações de logon para operações desconectadas; Portanto, não é apropriado para alguns aplicativos cliente/servidor, como um servidor de email.<br/>                                  |
| <span id="LOGON32_LOGON_NETWORK"></span><span id="logon32_logon_network"></span><dl> <dt>**LOGON32 \_ \_Rede de logon**</dt> <dt>3</dt> </dl>                                | Esse tipo de logon destina-se a servidores de alto desempenho para autenticar senhas de texto não criptografado. A função **LogonUserExExW** não armazena em cache as credenciais para esse tipo de logon.<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_BATCH"></span><span id="logon32_logon_batch"></span><dl> <dt>**LOGON32 \_ \_Lote de logon**</dt> <dt>4</dt> </dl>                                      | Esse tipo de logon destina-se a servidores de lote, em que processos podem ser executados em nome de um usuário sem sua intervenção direta. Esse tipo também é para servidores de desempenho mais alto que processam muitas tentativas de autenticação de texto sem formatação por vez, como servidores Web ou de email. A função **LogonUserExExW** não armazena em cache as credenciais para esse tipo de logon.<br/>                                                                                                           |
| <span id="LOGON32_LOGON_SERVICE"></span><span id="logon32_logon_service"></span><dl> <dt>**LOGON32 \_ \_Serviço de logon**</dt> <dt>5</dt> </dl>                                | Indica um logon de tipo de serviço. A conta fornecida deve ter o privilégio de serviço habilitado.<br/>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_UNLOCK"></span><span id="logon32_logon_unlock"></span><dl> <dt>**LOGON32 \_ \_Desbloqueio de logon**</dt> <dt>7</dt> </dl>                                   | Esse tipo de logon destina-se a DLLs de [*Gina*](../secgloss/g-gly.md) que fazem logon de usuários que serão interativamente usando o computador. Esse tipo de logon pode gerar um registro de auditoria exclusivo que mostra quando a estação de trabalho foi desbloqueada.<br/>                                                                                                                                                                                                                   |
| <span id="LOGON32_LOGON_NETWORK_CLEARTEXT"></span><span id="logon32_logon_network_cleartext"></span><dl> <dt>**LOGON32 \_ \_ \_ Texto puro da rede de logon**</dt> <dt>8</dt> </dl> | Esse tipo de logon preserva o nome e a senha no [*pacote de autenticação*](../secgloss/a-gly.md), o que permite que o servidor faça conexões com outros servidores de rede enquanto representa o cliente. Um servidor pode aceitar credenciais de texto não criptografado de um cliente, chamar **LogonUserExExW**, verificar se o usuário pode acessar o sistema pela rede e ainda se comunicar com outros servidores. <br/> |
| <span id="LOGON32_LOGON_NEW_CREDENTIALS"></span><span id="logon32_logon_new_credentials"></span><dl> <dt>**LOGON32 \_ \_Novas \_ credenciais de logon**</dt> <dt>9</dt> </dl>       | Esse tipo de logon permite que o chamador clone seu token atual e especifique novas credenciais para conexões de saída. A nova sessão de logon tem o mesmo identificador local, mas usa credenciais diferentes para outras conexões de rede.<br/> Esse tipo de logon tem suporte apenas pelo provedor de logon do **LOGON32 \_ Provider \_ WINNT50** .<br/>                                                                                                                                       |



 

</dd> <dt>

*dwLogonProvider* \[ no\]
</dt> <dd>

O provedor de logon. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                           | Significado                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_PROVIDER_DEFAULT"></span><span id="logon32_provider_default"></span><dl> <dt>**\_Padrão do provedor LOGON32 \_**</dt> </dl> | Use o provedor de logon padrão para o sistema. O [*provedor de segurança*](../secgloss/s-gly.md) padrão é NTLM.<br/> |
| <span id="LOGON32_PROVIDER_WINNT50"></span><span id="logon32_provider_winnt50"></span><dl> <dt>**\_Provedor LOGON32 \_ WINNT50**</dt> </dl> | Use o provedor de logon Negotiate. <br/>                                                                                                                                                         |
| <span id="LOGON32_PROVIDER_WINNT40"></span><span id="logon32_provider_winnt40"></span><dl> <dt>**\_Provedor LOGON32 \_ WINNT40**</dt> </dl> | Use o provedor de logon NTLM.<br/>                                                                                                                                                               |



 

</dd> <dt>

*pTokenGroups* \[ em, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ grupos de token**](/windows/win32/api/winnt/ns-winnt-token_groups) que especifica uma lista de SIDs de grupo que são adicionados ao token que essa função recebe após o logon bem-sucedido. Todos os SIDs adicionados ao token também afetam a expansão do grupo. Por exemplo, se os SIDs adicionados forem membros de grupos locais, esses grupos também serão adicionados ao token de acesso recebido.

Se esse parâmetro não for **nulo**, o chamador dessa função deverá ter o privilégio **de \_ \_ privilégio do se TCB** concedido e habilitado.

</dd> <dt>

*phToken* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma variável de identificador que recebe um identificador para um token que representa o usuário especificado.

Você pode usar o identificador retornado em chamadas para a função [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) .

Na maioria dos casos, o identificador retornado é um [*token primário*](../secgloss/p-gly.md) que você pode usar em chamadas para a função [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) . No entanto, se você especificar o sinalizador de rede de logon do LOGON32 \_ \_ , **LogonUserExExW** retornará um [*token de representação*](../secgloss/i-gly.md) que você não pode usar no **CreateProcessAsUser** , a menos que chame [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) para converter o token de representação em um token primário.

Quando você não precisar mais desse identificador, feche-o chamando a função [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) .

</dd> <dt>

*ppLogonSid* \[ out, opcional\]
</dt> <dd>

Um ponteiro para um ponteiro para um SID que recebe o SID do usuário conectado.

Quando você terminar de usar o SID, libere-o chamando a função [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) .

</dd> <dt>

*ppProfileBuffer* \[ out, opcional\]
</dt> <dd>

Um ponteiro para um ponteiro que recebe o endereço de um buffer que contém o perfil do usuário conectado.

</dd> <dt>

*pdwProfileLength* \[ out, opcional\]
</dt> <dd>

Um ponteiro para um **DWORD** que recebe o comprimento do buffer de perfil.

</dd> <dt>

*pQuotaLimits* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ limites de cota**](/windows/desktop/api/Winnt/ns-winnt-quota_limits) que recebe informações sobre as cotas para o usuário conectado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, a função retornará diferente de zero.

Se a função falhar, ela retornará zero. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

O tipo de logon de **\_ \_ rede de logon do LOGON32** é mais rápido, mas tem as seguintes limitações:

-   A função retorna um [*token de representação*](../secgloss/i-gly.md), não um token primário. Você não pode usar esse token diretamente na função [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) . No entanto, você pode chamar a função [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) para converter o token em um token primário e, em seguida, usá-lo em **CreateProcessAsUser**.
-   Se você converter o token em um token primário e usá-lo no [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) para iniciar um processo, o novo processo não poderá acessar outros recursos de rede, como servidores remotos ou impressoras, por meio do redirecionador. Uma exceção é que, se o recurso de rede não tiver acesso controlado, o novo processo poderá acessá-lo.

A conta especificada por *lpszUsername* deve ter os direitos de conta necessários. Por exemplo, para fazer logon em um usuário com o sinalizador **\_ \_ interativo de logon do LOGON32** , o usuário (ou um grupo ao qual o usuário pertence) deve ter a conta de **\_ \_ \_ nome de logon interativo do se** . Para obter uma lista dos direitos de conta que afetam as várias operações de logon, consulte [Account Object Access Rights](../secmgmt/account-object-access-rights.md).

Um usuário será considerado conectado se pelo menos um token existir. Se você chamar [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) e, em seguida, fechar o token, o usuário ainda estará conectado até que o processo (e todos os processos filho) tenha terminado.

Se o parâmetro opcional *pTokenGroups* for fornecido, o LSA não adicionará o SID local ou o Sid de logon automaticamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                                  |
| Versão<br/>                  | O LogonUserExExW também está disponível no Windows Server 2003 ou no Windows XPwith a versão de distribuição geral.<br/> |
| parâmetro<br/>                   | <dl> <dt>Winbasep. h</dt> </dl>                                 |
| DLL<br/>                      | <dl> <dt>Advapi32.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle de acesso de cliente/servidor](../secauthz/client-server-access-control.md)
</dt> <dt>

[Funções de controle de acesso de cliente/servidor](../secauthz/authorization-functions.md)
</dt> <dt>

[**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)
</dt> <dt>

[**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)
</dt> <dt>

[**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)
</dt> <dt>

[**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)
</dt> <dt>

[**LogonUserEx**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa)
</dt> <dt>

[**limites de cota \_**](/windows/desktop/api/Winnt/ns-winnt-quota_limits)
</dt> </dl>

 

 
