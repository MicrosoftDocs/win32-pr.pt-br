---
description: A função falha AcquireCredentialsHandle (CredSSP) adquire um identificador para credenciais preexistentes de uma entidade de segurança.
ms.assetid: 3b73decf-75d4-4bc4-b7ca-5f16aaadff29
title: Função AcquireCredentialsHandle (CredSSP)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 22ab5b4f9696e266e6d07b3085cafe10384e8b6b266c9e20672021fa04e97998
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101476"
---
# <a name="acquirecredentialshandle-credssp-function"></a>Função AcquireCredentialsHandle (CredSSP)

A função **falha AcquireCredentialsHandle (CredSSP)** adquire um identificador para credenciais preexistentes de uma entidade de segurança. Esse identificador é exigido pelas funções [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) e [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) . Elas podem ser *credenciais* preexistentes, que são estabelecidas por meio de um logon do sistema que não está descrito aqui, ou o chamador pode fornecer credenciais alternativas.

> [!Note]  
> Isso não é um "logon na rede" e não implica a coleta de credenciais.

## <a name="syntax"></a>Sintaxe

```C++
SECURITY_STATUS SEC_ENTRY AcquireCredentialsHandle(
  _In_opt_   SEC_CHAR       *pszPrincipal,
  _In_       SEC_CHAR       *pszPackage,
  _In_       unsigned long  fCredentialUse,
  _In_opt_   void           *pvLogonID,
  _In_opt_   void           *pAuthData,
  _In_opt_   SEC_GET_KEY_FN pGetKeyFn,
  _Reserved_ void           *pvGetKeyArgument,
  _Out_      PCredHandle    phCredential,
  _Out_opt_  PTimeStamp     ptsExpiry
);
```

## <a name="parameters"></a>Parâmetros

*pszPrincipal* \[ em, opcional\]

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome da entidade de segurança cujas credenciais serão referenciadas pelo identificador.

> [!Note]  
> Se o processo que solicita o identificador não tiver acesso às credenciais, a função retornará um erro. Uma cadeia de caracteres nula indica que o processo requer um identificador para as credenciais do usuário em cujo contexto de segurança está sendo executado.

*pszPackage* \[ no\]

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do pacote de segurança com o qual essas credenciais serão usadas. Esse é um nome de pacote de segurança retornado no membro **Name** de uma estrutura [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) retornada pela função [**EnumerateSecurityPackages**](/windows/win32/api/sspi/nf-sspi-enumeratesecuritypackagesa) . Depois que um contexto é estabelecido, [**QueryContextAttributes (CredSSP)**](querycontextattributes--credssp.md) pode ser chamado com *UlAttribute* definido como **SECPKG \_ \_ \_ informações do pacote attr** para retornar informações sobre o pacote de segurança em uso.

*fCredentialUse* \[ no\]

Um sinalizador que indica como essas credenciais serão usadas. Esse parâmetro pode usar um dos valores a seguir.

| Valor                                                                                                                                                                                                                                        | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_entrada de credenciais SECPKG \_**<br/>0x1  | Valide uma credencial de servidor de entrada. As credenciais de entrada podem ser validadas usando uma autoridade de autenticação quando [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) ou [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) é chamado. Se essa autoridade não estiver disponível, a função falhará e retornará **s \_ e \_ nenhuma \_ \_ autoridade de autenticação**. A validação é específica do pacote |
| **\_saída de credenciais SECPKG \_**<br/>0x0 | Permitir que uma credencial de cliente local Prepare um token de saída. |

*pvLogonId* \[ em, opcional\]

Um ponteiro para um [*identificador local exclusivo*](../secgloss/l-gly.md#_security_locally_unique_identifier_gly) (LUID) que identifica o usuário. Esse parâmetro é fornecido para processos do sistema de arquivos, como redirecionadores de rede. Este parâmetro pode ser **NULL**.

*pAuthData* \[ em, opcional\]

Um ponteiro para uma estrutura de [**\_ credenciais CREDSSP**](/windows/win32/api/credssp/ns-credssp-credssp_cred) que especifica os dados de autenticação para os pacotes Schannel e Negotiate.

*pGetKeyFn* \[ em, opcional\]

Reservado. Esse parâmetro não é usado e deve ser definido como **nulo**.

*pvGetKeyArgument* \[ em, opcional\]

Reservado. Esse parâmetro deve ser definido como **nulo**.

*phCredential* \[ fora\]

Um ponteiro para a estrutura [CredHandle](sspi-handles.md) que receberá o identificador de credencial.

*ptsExpiry* \[ out, opcional\]

Um ponteiro para uma estrutura de [**carimbo de data/**](timestamp.md) hora que recebe a hora em que as credenciais retornadas expiram. O valor de estrutura recebido depende do pacote de segurança, que deve especificar o valor na hora local.

## <a name="return-value"></a>Valor retornado

Se a função for bem sucedido, retornará **s \_ E \_ OK**.

Se a função falhar, ela retornará um dos seguintes códigos de erro.

| Código de retorno                      | Descrição                                                              |
|----------------------------------|--------------------------------------------------------------------------|
| **s \_ E \_ memória insuficiente \_** | Memória insuficiente disponível para concluir a ação solicitada. |
| **s \_ E \_ \_ erro interno**      | Ocorreu um erro que não foi mapeado para um código de erro SSPI.                |
| **s \_ E \_ sem \_ credenciais**      | Não há credenciais disponíveis no pacote de segurança.                    |
| **s \_ E \_ não \_ proprietário**           | O chamador da função não tem as credenciais necessárias.      |
| **s \_ E \_ SECPKG \_ não \_ encontrados**   | O pacote de segurança solicitado não existe.                           |
| **s \_ E \_ credenciais desconhecidas \_** | As credenciais fornecidas para o pacote não foram reconhecidas.             |

## <a name="remarks"></a>Comentários

A função **falha AcquireCredentialsHandle (CredSSP)** retorna um identificador para as credenciais de uma entidade, como um usuário ou cliente, conforme usado por um pacote de segurança específico. A função pode retornar o identificador para credenciais preexistentes ou credenciais recém-criadas e retorná-la. Esse identificador pode ser usado em chamadas subsequentes para as funções [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) e [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) .

Em geral, **falha AcquireCredentialsHandle (CredSSP)** não fornece as credenciais de outros usuários conectados ao mesmo computador. no entanto, um chamador \_ com \_ [*privilégio*](../secgloss/p-gly.md#_security_privilege_gly) de nome ES TCB pode obter as credenciais de uma sessão de logon existente especificando o [*identificador de logon*](../secgloss/l-gly.md#_security_logon_identifier_gly) (LUID) dessa sessão. Normalmente, isso é usado por módulos de modo kernel que devem agir em nome de um usuário conectado.

Um pacote pode chamar a função no *pGetKeyFn* fornecido pelo transporte de tempo de execução RPC. Se o transporte não oferecer suporte à noção de retorno de chamada para recuperar credenciais, esse parâmetro deverá ser **nulo**.

Para chamadores de modo kernel, as seguintes diferenças devem ser observadas:

- Os dois parâmetros String devem ser cadeias de caracteres [*Unicode*](../secgloss/u-gly.md#_security_unicode_gly) .
- Os valores do buffer devem ser alocados na memória virtual do processo, não no pool.

Quando você terminar de usar as credenciais retornadas, libere a memória usada pelas credenciais chamando a função [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows \[Somente aplicativos da área de trabalho do vista\]                                              |
| Servidor mínimo com suporte | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]                                        |
| Cabeçalho                   | SSPI. h (incluir Security. h)                                                      |
| Biblioteca                  | Secur32. lib                                                                      |
| DLL                      | Secur32.dll                                                                      |
| Nomes Unicode e ANSI   | **AcquireCredentialsHandleW** (Unicode) e **AcquireCredentialsHandleA** (ANSI) |

## <a name="see-also"></a>Confira também

- [Funções SSPI](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md)
- [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md)
- [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
