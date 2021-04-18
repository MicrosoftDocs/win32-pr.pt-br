---
description: Adquire um identificador para credenciais preexistentes de uma entidade de segurança que está usando Negotiate.
ms.assetid: ff372163-c73b-41bb-afcb-7d5de7720967
title: Função falha AcquireCredentialsHandle (Negotiate) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 80ab4b67866b60831dadb7d8eb9bf9f632c0661c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793749"
---
# <a name="acquirecredentialshandle-negotiate-function"></a>Função falha AcquireCredentialsHandle (Negotiate)

A função **falha AcquireCredentialsHandle (Negotiate)** adquire um identificador para credenciais preexistentes de uma [*entidade de segurança*](../secgloss/s-gly.md). Esse identificador é exigido pelas funções [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) e [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) . Elas podem ser *credenciais* preexistentes, que são estabelecidas por meio de um logon do sistema que não está descrito aqui, ou o chamador pode fornecer credenciais alternativas.

> [!Note]  
> Isso não é um "logon na rede" e não implica a coleta de credenciais.

 

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS SEC_Entry AcquireCredentialsHandle(
  _In_  SEC_CHAR       *pszPrincipal,
  _In_  SEC_CHAR       *pszPackage,
  _In_  ULONG          fCredentialUse,
  _In_  PLUID          pvLogonID,
  _In_  PVOID          pAuthData,
  _In_  SEC_GET_KEY_FN pGetKeyFn,
  _In_  PVOID          pvGetKeyArgument,
  _Out_ PCredHandle    phCredential,
  _Out_ PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszPrincipal* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome da entidade de segurança cujas credenciais serão referenciadas pelo identificador.

> [!Note]  
> Se o processo que solicita o identificador não tiver acesso às credenciais, a função retornará um erro. Uma cadeia de caracteres nula indica que o processo requer um identificador para as credenciais do usuário em cujo [*contexto de segurança*](../secgloss/s-gly.md) está sendo executado.

 

</dd> <dt>

*pszPackage* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do [*pacote de segurança*](../secgloss/s-gly.md) com o qual essas credenciais serão usadas. Esse é um nome de [*pacote de segurança*](../secgloss/s-gly.md) retornado no membro **Name** de uma estrutura [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) retornada pela função [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) . Depois que um contexto é estabelecido, [**QueryContextAttributes (Negotiate)**](querycontextattributes--negotiate.md) pode ser chamado com *ULATTRIBUTE* definido como SECPKG \_ \_ \_ informações do pacote attr para retornar informações sobre o [*pacote de segurança*](../secgloss/s-gly.md) em uso.

Para chamar essa função com êxito usando o Negotiate SSP, defina esse parâmetro como "Negotiate".

</dd> <dt>

*fCredentialUse* \[ no\]
</dt> <dd>

Um sinalizador que indica como essas credenciais serão usadas. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_AUTOLOGON_RESTRICTED"></span><span id="secpkg_cred_autologon_restricted"></span><dl> <dt>**SECPKG \_ Credenciais \_ \_ restritas de logon automático do cred**</dt> <dt></dt> </dl> | A segurança não usa credenciais de logon padrão ou credenciais do [Gerenciador de credenciais](credential-manager.md).<br/> **Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Não há suporte para esse valor.<br/>                                                                                                                                                                                                                    |
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <dt>**SECPKG \_ cred \_**</dt> </dl>                                                                                                                  | Valide uma credencial de entrada ou use uma credencial local para preparar um token de saída. Esse sinalizador habilita ambos os outros sinalizadores.<br/>                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <dt>**\_entrada de credenciais SECPKG \_**</dt> </dl>                                                                                                         | Valide uma credencial de servidor de entrada. As credenciais de entrada podem ser validadas usando uma autoridade de autenticação quando [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) ou [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) é chamado. Se essa autoridade não estiver disponível, a função falhará e retornará s \_ e \_ nenhuma autoridade de \_ autenticação \_ . A validação é específica do pacote.<br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <dt>**\_saída de credenciais SECPKG \_**</dt> </dl>                                                                                                      | Permitir que uma credencial de cliente local Prepare um token de saída.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="SECPKG_CRED_PROCESS_POLICY_ONLY"></span><span id="secpkg_cred_process_policy_only"></span><dl> <dt>**SECPKG \_ Política de processo de credenciais \_ \_ \_ apenas**</dt> <dt>0x00000020</dt> </dl>   | A função processa a política de servidor e retorna **s \_ e \_ nenhuma \_ credencial**, indicando que o aplicativo deve solicitar credenciais.<br/> **Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Não há suporte para esse valor.<br/>                                                                                                                                                                                             |



 

</dd> <dt>

*pvLogonID* \[ no\]
</dt> <dd>

Um ponteiro para um [*identificador local exclusivo*](../secgloss/l-gly.md) (LUID) que identifica o usuário. Esse parâmetro é fornecido para processos do sistema de arquivos, como redirecionadores de rede. Este parâmetro pode ser **NULL**.

</dd> <dt>

*pAuthData* \[ no\]
</dt> <dd>

Um ponteiro para dados específicos do pacote. Esse parâmetro pode ser **nulo**, o que indica que as credenciais padrão para esse [*pacote de segurança*](../secgloss/s-gly.md) devem ser usadas. Para usar credenciais fornecidas, passe uma **estrutura \_ \_ opaca de \_ identidade \_ de autenticação WinNT PSEC** retornada de uma chamada anterior para a função [**SspiPromptForCredentials**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) .

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Não há suporte para o tipo **opaco da identidade de autenticação do PSEC \_ \_ \_ \_ WinNT** e para a função [**SspiPromptForCredentials**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) . Para usar credenciais fornecidas, passe um ponteiro para uma [**identidade de \_ \_ autenticação do \_ WinNT da SEC**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) ou a estrutura da identidade de autenticação do Winnt de s, por [**\_ \_ \_ \_ exemplo**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) , que inclui essas credenciais.

O tempo de execução RPC passa o que foi fornecido em [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).

Ao usar o pacote Negotiate, os comprimentos máximos de caracteres para o nome de usuário, a senha e o domínio são 256, 256 e 15, respectivamente.

</dd> <dt>

*pGetKeyFn* \[ no\]
</dt> <dd>

Esse parâmetro não é usado e deve ser definido como **nulo**.

</dd> <dt>

*pvGetKeyArgument* \[ no\]
</dt> <dd>

Esse parâmetro não é usado e deve ser definido como **nulo**.

</dd> <dt>

*phCredential* \[ fora\]
</dt> <dd>

Um ponteiro para uma estrutura [CredHandle](sspi-handles.md) para receber o identificador de credencial.

</dd> <dt>

*ptsExpiry* \[ fora\]
</dt> <dd>

Um ponteiro para uma estrutura de [**carimbo de data/**](timestamp.md) hora que recebe a hora em que as credenciais retornadas expiram. O valor retornado nessa estrutura de **carimbo de data/hora** depende da [*delegação restrita*](../secgloss/s-gly.md). O [*pacote de segurança*](../secgloss/s-gly.md) deve retornar esse valor na hora local.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, a função retornará s \_ E \_ OK.

Se a função falhar, ela retornará um dos seguintes códigos de erro.



| Código de retorno                                                                                                 | Descrição                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**s \_ E \_ memória insuficiente \_**</dt> </dl> | Não há memória suficiente disponível para concluir a ação solicitada.<br/>                                                                  |
| <dl> <dt>**s \_ E \_ \_ erro interno**</dt> </dl>      | Ocorreu um erro que não foi mapeado para um código de erro SSPI.<br/>                                                                               |
| <dl> <dt>**s \_ E \_ sem \_ credenciais**</dt> </dl>      | Não há credenciais disponíveis na [*delegação restrita*](../secgloss/s-gly.md).<br/> |
| <dl> <dt>**s \_ E \_ não \_ proprietário**</dt> </dl>           | O chamador da função não tem as credenciais necessárias.<br/>                                                                     |
| <dl> <dt>**s \_ E \_ SECPKG \_ não \_ encontrados**</dt> </dl>   | O [*pacote de segurança*](../secgloss/s-gly.md) solicitado não existe.<br/>                                                                                          |
| <dl> <dt>**s \_ E \_ credenciais desconhecidas \_**</dt> </dl> | As credenciais fornecidas para o pacote não foram reconhecidas.<br/>                                                                            |



 

## <a name="remarks"></a>Comentários

A função **falha AcquireCredentialsHandle (Negotiate)** retorna um identificador para as credenciais de uma entidade de segurança, como um usuário ou cliente, conforme usado por uma [*delegação restrita*](../secgloss/s-gly.md)específica. Isso pode ser o identificador para credenciais preexistentes ou a função pode criar um novo conjunto de credenciais e retorná-la. Esse identificador pode ser usado em chamadas subsequentes para as funções [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) e [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) .

Em geral, **falha AcquireCredentialsHandle (Negotiate)** não permite que um processo obtenha um identificador para as credenciais de outros usuários conectados ao mesmo computador. No entanto, um \_ \_ [*privilégio*](../secgloss/s-gly.md) de nome do chamador com o Name TCB tem a opção de especificar o [*identificador de logon*](../secgloss/l-gly.md) (LUID) de qualquer token de sessão de logon existente para obter um identificador para as credenciais dessa sessão. Normalmente, isso é usado por módulos de modo kernel que devem agir em nome de um usuário conectado.

Um pacote pode chamar a função no *pGetKeyFn* fornecido pelo transporte de tempo de execução RPC. Se o transporte não oferecer suporte à noção de retorno de chamada para recuperar credenciais, esse parâmetro deverá ser **nulo**.

Para chamadores de modo kernel, as seguintes diferenças devem ser observadas:

-   Os dois parâmetros String devem ser cadeias de caracteres [*Unicode*](../secgloss/u-gly.md) .
-   Os valores do buffer devem ser alocados na memória virtual do processo, não no pool.

Quando você terminar de usar as credenciais retornadas, libere a memória usada pelas credenciais chamando a função [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                   |
| parâmetro<br/>                   | <dl> <dt>SSPI. h (incluir Security. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Nomes Unicode e ANSI<br/>   | **AcquireCredentialsHandleW** (Unicode) e **AcquireCredentialsHandleA** (ANSI)<br/>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (negociar)**](acceptsecuritycontext--negotiate.md)
</dt> <dt>

[**InitializeSecurityContext (negociar)**](initializesecuritycontext--negotiate.md)
</dt> <dt>

[**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
