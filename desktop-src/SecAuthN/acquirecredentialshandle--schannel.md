---
description: Adquire um lidar com credenciais preexistência de uma entidade de segurança que está usando o Schannel.
ms.assetid: 0f006670-a1e5-47ed-baf5-ed55bd42b468
title: Função AcquireCredentialsHandle (Schannel) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: d2fb9812817e27576667f7fa0ff5312eea8cea41743cbfc9e5b03267f837011f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101436"
---
# <a name="acquirecredentialshandle-schannel-function"></a>Função AcquireCredentialsHandle (Schannel)

A **função AcquireCredentialsHandle (Schannel)** adquire um identificador para credenciais preexistente de uma entidade [*de segurança*](../secgloss/s-gly.md). Esse handle é exigido pelas funções [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) e [**AcceptSecurityContext (Schannel).**](acceptsecuritycontext--schannel.md) Elas podem ser credenciais preexistência, que são *estabelecidas* por meio de um logon do sistema que não está descrito aqui, ou o chamador pode fornecer credenciais alternativas.

> [!Note]  
> Isso não é um "logoff na rede" e não implica na coleta de credenciais.

 

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS SEC_Entry AcquireCredentialsHandle(
  _In_opt_  SEC_CHAR       *pszPrincipal,
  _In_      SEC_CHAR       *pszPackage,
  _In_      ULONG          fCredentialUse,
  _In_opt_  PLUID          pvLogonID,
  _In_opt_  PVOID          pAuthData,
  _In_opt_  SEC_GET_KEY_FN pGetKeyFn,
  _In_opt_  PVOID          pvGetKeyArgument,
  _Out_     PCredHandle    phCredential,
  _Out_opt_ PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszPrincipal* \[ in, opcional\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome da entidade de serviço cujas credenciais o alça fará referência.

Ao usar o SSP Schannel, esse parâmetro não é usado e deve ser definido como **NULL.**

> [!Note]  
> Se o processo que solicita o handle não tiver acesso às credenciais, a função retornará um erro. Uma cadeia de caracteres nula indica que o processo requer um alçamento para as credenciais do usuário em cujo contexto [*de segurança*](../secgloss/s-gly.md) ele está sendo executado.

 

</dd> <dt>

*pszPackage* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do [*pacote*](../secgloss/s-gly.md) de segurança com o qual essas credenciais serão usadas. Esse é um [*nome de pacote*](../secgloss/s-gly.md) de segurança retornado no membro **Name** de uma estrutura [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) retornada pela [**função EnumerateSecurityPackages.**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) Depois que um contexto é estabelecido, [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) pode ser chamado com *ulAttribute definido* como SECPKG ATTR PACKAGE INFO para retornar informações sobre o pacote de segurança em \_ \_ \_ [](../secgloss/s-gly.md) uso.

Ao usar o SSP Schannel, de definido esse parâmetro como NOME DO \_ UNISP.

</dd> <dt>

*fCredentialUse* \[ Em\]
</dt> <dd>

Um sinalizador que indica como essas credenciais serão usadas. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <dt>**ENTRADA CRED SECPKG \_ \_**</dt> </dl>    | Validar uma credencial de servidor de entrada. As credenciais de entrada podem ser validadas usando uma autoridade de autenticação quando [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) ou [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) é chamado. Se essa autoridade não estiver disponível, a função falhará e retornará SEC \_ E \_ NO \_ AUTHENTICATING \_ AUTHORITY. A validação é específica do pacote.<br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <dt>**SAÍDA DE CRED SECPKG \_ \_**</dt> </dl> | Permitir uma credencial de cliente local para preparar um token de saída.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*pvLogonID* \[ in, opcional\]
</dt> <dd>

Um ponteiro para um LUID [*(identificador*](../secgloss/l-gly.md) exclusivo local) que identifica o usuário. Esse parâmetro é fornecido para processos do sistema de arquivos, como redirecionadores de rede. Este parâmetro pode ser **NULL**.

Ao usar o SSP Schannel, esse parâmetro não é usado e deve ser definido como **NULL.**

</dd> <dt>

*pAuthData* \[ in, opcional\]
</dt> <dd>

Um ponteiro para dados específicos do pacote. Esse parâmetro pode ser **NULL,** que indica que as credenciais padrão para esse pacote [*de segurança*](../secgloss/s-gly.md) devem ser usadas. Para usar as credenciais fornecidas, passe uma estrutura DE IDENTIDADE DE [**\_ \_ AUTH \_ WINNT**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) DO WINNT da SEC que inclua essas credenciais nesse parâmetro. O tempo de executar RPC passa o que foi fornecido em [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).

Ao usar o SSP Schannel, especifique uma estrutura [**SCH_CREDENTIALS**](/windows/win32/api/schannel/ns-schannel-sch_credentials) que indica o protocolo a ser usado e as configurações para vários recursos de canal personalizáveis.

</dd> <dt>

*pGetKeyFn* \[ in, opcional\]
</dt> <dd>

Esse parâmetro não é usado e deve ser definido como **NULL.**

</dd> <dt>

*pvGetKeyArgument* \[ in, opcional\]
</dt> <dd>

Esse parâmetro não é usado e deve ser definido como **NULL.**

</dd> <dt>

*phCredential* \[ out\]
</dt> <dd>

Um ponteiro para uma [estrutura CredHandle](sspi-handles.md) para receber o alça de credencial.

</dd> <dt>

*ptsExpiry* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma [**estrutura TimeStamp**](timestamp.md) que recebe a hora em que as credenciais retornadas expiram. O valor retornado nesta estrutura **TimeStamp** depende da [*delegação restrita*](../secgloss/s-gly.md). O [*pacote de segurança*](../secgloss/s-gly.md) deve retornar esse valor em hora local.

Ao usar o SSP Schannel, esse parâmetro é opcional. Quando a credencial a ser usada para autenticação é um certificado, esse parâmetro recebe o tempo de expiração desse certificado. Se nenhum certificado tiver sido fornecido, um valor de tempo máximo será retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, a função retornará SEC \_ E \_ OK.

Se a função falhar, ela retornará um dos códigos de erro a seguir.



| Código de retorno                                                                                                 | Descrição                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ E \_ MEMÓRIA \_ INSUFICIENTE**</dt> </dl> | Não há memória suficiente disponível para concluir a ação solicitada.<br/>                                                                  |
| <dl> <dt>**ERRO \_ INTERNO DO SEC E \_ \_**</dt> </dl>      | Ocorreu um erro que não mapeou para um código de erro SSPI.<br/>                                                                               |
| <dl> <dt>**SEC \_ E \_ NO \_ CREDENTIALS**</dt> </dl>      | Nenhuma credencial está disponível na [*delegação restrita*](../secgloss/s-gly.md).<br/> |
| <dl> <dt>**SEC \_ E \_ NOT \_ OWNER**</dt> </dl>           | O chamador da função não tem as credenciais necessárias.<br/>                                                                     |
| <dl> <dt>**SEC \_ E \_ SECPKG \_ NÃO \_ ENCONTRADO**</dt> </dl>   | O pacote de [*segurança solicitado*](../secgloss/s-gly.md) não existe.<br/>                                                                                          |
| <dl> <dt>**S \_ E \_ CREDENCIAIS \_ DESCONHECIDAS**</dt> </dl> | As credenciais fornecidas ao pacote não foram reconhecidas.<br/>                                                                            |



 

## <a name="remarks"></a>Comentários

A **função AcquireCredentialsHandle (Schannel)** retorna um identificador para as credenciais de uma entidade de serviço, como um usuário ou cliente, conforme usado por uma delegação restrita [*específica.*](../secgloss/s-gly.md) Esse pode ser o lidar com credenciais preexistência ou a função pode criar um novo conjunto de credenciais e devolvê-lo. Esse handle pode ser usado em chamadas subsequentes para as funções [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) e [**InitializeSecurityContext (Schannel).**](initializesecuritycontext--schannel.md)

Em geral, **AcquireCredentialsHandle (Schannel)** não permite que um processo obtenha um identificador para as credenciais de outros usuários conectados ao mesmo computador. No entanto, um chamador com ES privilégio TCB NAME tem a opção de especificar o \_ \_ LUID (identificador de [*logon)*](../secgloss/l-gly.md) [](../secgloss/s-gly.md) de qualquer token de sessão de logon existente para obter um identificador para as credenciais dessa sessão. Normalmente, isso é usado por módulos de modo kernel que devem agir em nome de um usuário conectado.

Um pacote pode chamar a função em *pGetKeyFn* fornecida pelo transporte em tempo de executar RPC. Se o transporte não dá suporte à noção de retorno de chamada para recuperar credenciais, esse parâmetro deve ser **NULL.**

Para chamadores de modo kernel, as seguintes diferenças devem ser notadas:

-   Os dois parâmetros de cadeia de caracteres devem ser [*cadeias de caracteres Unicode.*](../secgloss/u-gly.md)
-   Os valores de buffer devem ser alocados na memória virtual do processo, não no pool.

Quando terminar de usar as credenciais retornadas, livre a memória usada pelas credenciais chamando a [**função FreeCredentialsHandle.**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                   |
| Cabeçalho<br/>                   | <dl> <dt>Sspi.h (inclua Security.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Nomes Unicode e ANSI<br/>   | **AcquireCredentialsHandleW** (Unicode) e **AcquireCredentialsHandleA** (ANSI)<br/>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md)
</dt> <dt>

[**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

[**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md)
</dt> <dt>

[**SCH_CREDENTIALS**](/windows/win32/api/schannel/ns-schannel-sch_credentials)
</dt> <dt>

[**Funções SSPI**](authentication-functions.md#sspi-functions)
</dt> <dt>
 

 
