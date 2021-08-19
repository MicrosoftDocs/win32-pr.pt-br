---
description: A função LogonUserExW tenta fazer logon de um usuário no computador local.
ms.assetid: d90db4c6-a711-4519-8b91-5069cee07738
title: Função LogonUserExW (Winbasep.h)
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
ms.openlocfilehash: 8e6b7c5b377ffa7b517ccd19d1dfbffa08d26191af3822f9d9b17cc02c33d055
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922331"
---
# <a name="logonuserexexw-function"></a>Função LogonUserExExW

A **função LogonUserExW** tenta fazer logon de um usuário no computador local. O computador local é o computador do **qual LogonUserExExW** foi chamado. Você não pode usar **LogonUserExExW** para fazer logon em um computador remoto. Especifique o usuário usando um nome de usuário e um domínio [*e autenture*](../secgloss/a-gly.md) o usuário usando uma senha de texto não criptografado. Se a função for bem-sucedida, ela receberá um handle para um token que representa o usuário conectado. Em seguida, você pode usar esse alçamento de token para representar [](../secgloss/p-gly.md) o usuário especificado ou, na maioria dos casos, para criar um processo que é executado no contexto do usuário especificado.

Essa função é semelhante à função [**LogonUserEx,**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa) exceto que ela usa o parâmetro *adicional, pTokenGroups*, que é um conjunto de um ou mais SIDs [*(identificadores*](../secgloss/s-gly.md) de segurança) que são adicionados ao token retornado ao chamador quando o logon é bem-sucedido.

Essa função não é declarada em um header público e não tem nenhuma biblioteca de importação associada. Você deve usar as [**funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Advapi32.dll.

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

*lpszUsername* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do usuário. Esse é o nome da conta de usuário para fazer logoff. Se você usar o formato UPN (nome [*upn),*](../secgloss/u-gly.md) o *parâmetro lpszDomain* deverá ser **NULL.**

</dd> <dt>

*lpszDomain* \[ in, opcional\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do domínio ou servidor cujo banco de dados de conta contém a *conta lpszUsername.* Se esse parâmetro for **NULL,** o nome de usuário deverá ser especificado no formato UPN. Se esse parâmetro for ".", a função validará a conta usando apenas o banco de dados da conta local.

</dd> <dt>

*lpszPassword* \[ in, opcional\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica a senha de texto não criptografado para a conta de usuário especificada por *lpszUsername*. Quando terminar de usar a senha, limpe a senha da memória chamando a [**função SecureZeroMemory.**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) Para obter mais informações sobre como proteger senhas, consulte [Tratamento de senhas](../secbp/handling-passwords.md).

</dd> <dt>

*dwLogonType* \[ Em\]
</dt> <dd>

O tipo de operação de logon a ser realizada. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                        | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_LOGON_INTERACTIVE"></span><span id="logon32_logon_interactive"></span><dl> <dt>**LOGON32 \_ LOGON \_ INTERATIVO**</dt> <dt>2</dt> </dl>                    | Esse tipo de logon destina-se a usuários que usarão interativamente o computador, como um usuário que está sendo conectado por um servidor [*de terminal,*](../secgloss/t-gly.md) shell remoto ou processo semelhante. Esse tipo de logon tem a despesa adicional de cache de informações de logon para operações desconectadas; portanto, é inadequado para alguns aplicativos cliente/servidor, como um servidor de email.<br/>                                  |
| <span id="LOGON32_LOGON_NETWORK"></span><span id="logon32_logon_network"></span><dl> <dt>**LOGON32 \_ LOGON \_ NETWORK**</dt> <dt>3</dt> </dl>                                | Esse tipo de logon destina-se a servidores de alto desempenho para autenticar senhas de texto não criptografado. A **função LogonUserExW** não armazena credenciais em cache para esse tipo de logon.<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_BATCH"></span><span id="logon32_logon_batch"></span><dl> <dt>**LOGON32 \_ LOGON \_ LOTE**</dt> <dt>4</dt> </dl>                                      | Esse tipo de logon destina-se a servidores em lotes, em que os processos podem estar sendo executados em nome de um usuário sem a intervenção direta. Esse tipo também é para servidores de alto desempenho que processam muitas tentativas de autenticação de texto não criptografado por vez, como servidores Web ou de email. A **função LogonUserExW** não armazena credenciais em cache para esse tipo de logon.<br/>                                                                                                           |
| <span id="LOGON32_LOGON_SERVICE"></span><span id="logon32_logon_service"></span><dl> <dt>**LOGON32 \_ LOGON \_ SERVICE**</dt> <dt>5</dt> </dl>                                | Indica um logon de tipo de serviço. A conta fornecida deve ter o privilégio de serviço habilitado.<br/>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_UNLOCK"></span><span id="logon32_logon_unlock"></span><dl> <dt>**LOGON32 \_ DESBLOQUEIO \_ DE LOGON**</dt> <dt>7</dt> </dl>                                   | Esse tipo de logon é para DLLs [*DOIS*](../secgloss/g-gly.md) que fizerem logon em usuários que usarão o computador interativamente. Esse tipo de logon pode gerar um registro de auditoria exclusivo que mostra quando a estação de trabalho foi desbloqueada.<br/>                                                                                                                                                                                                                   |
| <span id="LOGON32_LOGON_NETWORK_CLEARTEXT"></span><span id="logon32_logon_network_cleartext"></span><dl> <dt>**LOGON32 \_ LOGON \_ NETWORK \_ CLEARTEXT**</dt> <dt>8</dt> </dl> | Esse tipo de logon preserva o nome e a senha no pacote de autenticação [*,*](../secgloss/a-gly.md)que permite que o servidor faça conexões com outros servidores de rede ao representar o cliente. Um servidor pode aceitar credenciais de texto não criptografado de um cliente, chamar **LogonUserExExW**, verificar se o usuário pode acessar o sistema pela rede e ainda se comunicar com outros servidores. <br/> |
| <span id="LOGON32_LOGON_NEW_CREDENTIALS"></span><span id="logon32_logon_new_credentials"></span><dl> <dt>**LOGON32 \_ LOGON \_ NOVAS \_ CREDENCIAIS**</dt> <dt>9</dt> </dl>       | Esse tipo de logon permite que o chamador clone seu token atual e especifique novas credenciais para conexões de saída. A nova sessão de logon tem o mesmo identificador local, mas usa credenciais diferentes para outras conexões de rede.<br/> Esse tipo de logon tem suporte apenas pelo **provedor de logon LOGON32 \_ PROVIDER \_ WINNT50.**<br/>                                                                                                                                       |



 

</dd> <dt>

*dwLogonProvider* \[ Em\]
</dt> <dd>

O provedor de logon. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                           | Significado                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_PROVIDER_DEFAULT"></span><span id="logon32_provider_default"></span><dl> <dt>**LOGON32 \_ PROVIDER \_ DEFAULT**</dt> </dl> | Use o provedor de logon padrão para o sistema. O provedor [*de segurança padrão*](../secgloss/s-gly.md) é NTLM.<br/> |
| <span id="LOGON32_PROVIDER_WINNT50"></span><span id="logon32_provider_winnt50"></span><dl> <dt>**LOGON32 \_ PROVIDER \_ WINNT50**</dt> </dl> | Use o provedor de logon negotiate. <br/>                                                                                                                                                         |
| <span id="LOGON32_PROVIDER_WINNT40"></span><span id="logon32_provider_winnt40"></span><dl> <dt>**LOGON32 \_ PROVIDER \_ WINNT40**</dt> </dl> | Use o provedor de logon NTLM.<br/>                                                                                                                                                               |



 

</dd> <dt>

*pTokenGroups* \[ in, opcional\]
</dt> <dd>

Um ponteiro para uma [**estrutura TOKEN \_ GROUPS**](/windows/win32/api/winnt/ns-winnt-token_groups) que especifica uma lista de SIDs de grupo que são adicionados ao token que essa função recebe após o logon bem-sucedido. Quaisquer SIDs adicionados ao token também têm efeito sobre a expansão do grupo. Por exemplo, se os SIDs adicionados são membros de grupos locais, esses grupos também são adicionados ao token de acesso recebido.

Se esse parâmetro não for **NULL,** o chamador dessa função deverá ter o ES **privilégio \_ TCB \_ PRIVILEGE** concedido e habilitado.

</dd> <dt>

*phToken* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma variável de alça que recebe um handle para um token que representa o usuário especificado.

Você pode usar o alça retornado em chamadas para a [**função ImpersonateLoggedOnUser.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)

Na maioria dos casos, o handle retornado é um [*token primário*](../secgloss/p-gly.md) que você pode usar em chamadas para a [**função CreateProcessAsUser.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) No entanto, se você especificar o sinalizador \_ LOGON32 LOGON \_ NETWORK, **LogonUserExExW** retornará um [*token*](../secgloss/i-gly.md) de representação que não poderá ser usado em **CreateProcessAsUser,** a menos que você chame [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) para converter o token de representação em um token primário.

Quando você não precisar mais desse alça, feche-o chamando a [**função CloseHandle.**](/windows/win32/api/handleapi/nf-handleapi-closehandle)

</dd> <dt>

*ppLogonSid* \[ out, opcional\]
</dt> <dd>

Um ponteiro para um ponteiro para um SID que recebe o SID do usuário conectado.

Quando terminar de usar o SID, livre-o chamando a [**função LocalFree.**](/windows/win32/api/winbase/nf-winbase-localfree)

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

Um ponteiro para uma [**estrutura QUOTA \_ LIMITS**](/windows/desktop/api/Winnt/ns-winnt-quota_limits) que recebe informações sobre as cotas para o usuário conectado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, a função retornará diferentes de zero.

Se a função falhar, ela retornará zero. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

O **tipo de \_ logon LOGON NETWORK LOGON32 \_** é mais rápido, mas tem as seguintes limitações:

-   A função retorna um [*token de representação*](../secgloss/i-gly.md), não um token primário. Você não pode usar esse token diretamente na [**função CreateProcessAsUser.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) No entanto, você pode chamar a [**função DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) para converter o token em um token primário e, em seguida, usá-lo **em CreateProcessAsUser.**
-   Se você converter o token em um token primário e usá-lo em [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) para iniciar um processo, o novo processo não poderá acessar outros recursos de rede, como servidores remotos ou impressoras, por meio do redirecionador. Uma exceção é que, se o recurso de rede não for controlado pelo acesso, o novo processo poderá acessá-lo.

A conta especificada por *lpszUsername* deve ter os direitos de conta necessários. Por exemplo, para fazer logon em um usuário com o sinalizador **\_ LOGON32 LOGON \_ INTERATIVO,** o usuário (ou um grupo ao qual o usuário pertence) deve ter o direito ES NOME DO **\_ \_ LOGON \_** INTERATIVO. Para ver uma lista dos direitos de conta que afetam as várias operações de logon, consulte [Direitos de acesso ao objeto de conta](../secmgmt/account-object-access-rights.md).

Um usuário será considerado conectado se pelo menos um token existir. Se você chamar [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) e fechar o token, o usuário ainda será conectado até que o processo (e todos os processos filho) tenham terminado.

Se o parâmetro *pTokenGroups* opcional for fornecido, o LSA não adicionará o SID local ou o SID de logon automaticamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                                  |
| Versão<br/>                  | LogonUserExExW também está disponível noWindows Server 2003 ou Windows XP com a Versão de Distribuição Geral.<br/> |
| Cabeçalho<br/>                   | <dl> <dt>Winbasep.h</dt> </dl>                                 |
| DLL<br/>                      | <dl> <dt>Advapi32.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle de acesso de cliente/servidor](../secauthz/client-server-access-control.md)
</dt> <dt>

[Funções de controle de acesso de cliente/servidor](../secauthz/authorization-functions.md)
</dt> <dt>

[**Closehandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)
</dt> <dt>

[**Createprocessasuser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)
</dt> <dt>

[**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)
</dt> <dt>

[**Impersonateloggedonuser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)
</dt> <dt>

[**LogonUserEx**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa)
</dt> <dt>

[**LIMITES \_ DE COTA**](/windows/desktop/api/Winnt/ns-winnt-quota_limits)
</dt> </dl>

 

 
