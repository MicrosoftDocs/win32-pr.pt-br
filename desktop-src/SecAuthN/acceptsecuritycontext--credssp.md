---
description: Permite que o componente de servidor de um aplicativo de transporte estabeleça um contexto de segurança entre o servidor e um cliente remoto.
ms.assetid: a53f733e-b646-4431-b021-a2c446308849
title: Função AcceptSecurityContext (CredSSP)
ms.topic: article
ms.date: 07/25/2019
ms.openlocfilehash: df4c87274c3a19d9e4a028cde813801688ce1927d1a0b89dbe3a7e8633ce8b57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141689"
---
# <a name="acceptsecuritycontext-credssp-function"></a>Função AcceptSecurityContext (CredSSP)

A **função AcceptSecurityContext (CredSSP)** permite que o componente de servidor de um aplicativo de transporte estabeleça um contexto de segurança entre o servidor e um cliente remoto. O cliente remoto chama a [**função InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) para iniciar o processo de estabelecimento de um contexto de segurança. O servidor pode exigir um ou mais tokens de resposta do cliente remoto para concluir o estabelecimento do contexto de segurança.

## <a name="syntax"></a>Sintaxe

```C++
SECURITY_STATUS SEC_ENTRY AcceptSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_opt_    PSecBufferDesc pInput,
  _In_        unsigned long  fContextReq,
  _In_        unsigned long  TargetDataRep,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Inout_opt_ PSecBufferDesc pOutput,
  _Out_       unsigned long  *pfContextAttr,
  _Out_opt_   PTimeStamp     ptsExpiry
);
```

## <a name="parameters"></a>Parâmetros

*phCredential* \[ in, opcional\]

Um handle para as credenciais do servidor. Para recuperar esse identificador, o servidor chama a função [**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md) com o conjunto de sinalizadores SECPKG \_ CRED INBOUND ou \_ SECPKG \_ CRED \_ BOTH.

*phContext* \[ in, opcional\]

Um ponteiro para uma [estrutura CtxtHandle.](sspi-handles.md) Na primeira chamada para **AcceptSecurityContext (CredSSP),** esse ponteiro é **NULL.** Em chamadas subsequentes, *phContext* especifica o contexto parcialmente formado retornado no parâmetro *phNewContext* pela primeira chamada.

*pInput* \[ in, opcional\]

Um ponteiro para uma [**estrutura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) gerada por uma chamada do cliente para [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md). A estrutura contém o descritor de buffer de entrada.

O primeiro buffer deve ser do **tipo SECBUFFER \_ TOKEN** e conter o token de segurança recebido do cliente. O segundo buffer deve ser do **tipo SECBUFFER \_ EMPTY.**

*fContextReq* \[ Em\]

Sinalizadores de bits que especificam os atributos exigidos pelo servidor para estabelecer o contexto. Os sinalizadores de bit podem ser combinados usando operações **OR** bit a bit. Esse parâmetro pode ser um ou mais dos valores a seguir.

| Valor                          | Significado                                                                                                                                                                                                        |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ASC \_ REQ \_ ALLOCATE \_ MEMORY** | O CredSSP (Provedor de Suporte de Segurança de Credencial) alocará buffers de saída. Quando terminar de usar os buffers de saída, livre-os chamando a [**função FreeContextBuffer.**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) |
| **CONEXÃO ASC \_ REQ \_**       | O contexto de segurança não manipulará mensagens de formatação.                                                                                                                                                      |
| **ASC \_ REQ \_ DELEGATE**         | O servidor tem permissão para representar o cliente. Ignore esse sinalizador para delegação restrita.                                                         |
| **ERRO ESTENDIDO DO ASC \_ REQ \_ \_**  | Quando ocorrerem erros, a parte remota será notificada.                                                                                                                                                          |
| **ASC \_ REQ \_ REPLAY \_ DETECT**   | Detectar pacotes replayed.                                                                                                                                                                                       |
| **ASC \_ REQ \_ SEQUENCE \_ DETECT** | Detectar mensagens recebidas fora de sequência.                                                                                                                                                                      |
| **FLUXO DE REQ DO ASC \_ \_**           | Dar suporte a uma conexão orientada a fluxo.                                                                                                                                                                          |

Para possíveis sinalizadores de atributo e seus significados, consulte [Requisitos de contexto.](context-requirements.md) Sinalizadores usados para esse parâmetro são prefixados com ASC \_ REQ, por exemplo, ASC \_ REQ \_ DELEGATE.

Os atributos solicitados podem não ser suportados pelo cliente. Para obter mais informações, consulte o *parâmetro pfContextAttr.*

*TargetDataRep* \[ Em\]

A representação de dados, como ordenação de byte, no destino. Esse parâmetro pode ser **SECURITY \_ NATIVE \_ DREP** ou **SECURITY NETWORK \_ \_ DREP**.

*phNewContext* \[ in, out, opcional\]

Um ponteiro para uma [estrutura CtxtHandle.](sspi-handles.md) Na primeira chamada para **AcceptSecurityContext (CredSSP),** esse ponteiro recebe o novo indicador de contexto. Em chamadas subsequentes, *phNewContext* pode ser o mesmo que o handle especificado no *parâmetro phContext.*

*pOutput* \[ in, out, opcional\]

Um ponteiro para uma [**estrutura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) que contém o descritor de buffer de saída. Esse buffer é enviado ao cliente para entrada em chamadas adicionais para [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md). Um buffer de saída pode ser gerado mesmo que a função retorne SEC \_ E \_ OK. Qualquer buffer gerado deve ser enviado de volta para o aplicativo cliente.

Na saída, esse buffer recebe um token para o contexto de segurança. O token deve ser enviado ao cliente. A função também pode retornar um buffer do tipo SECBUFFER \_ EXTRA.

*pfContextAttr* \[ out\]

Um ponteiro para um conjunto de sinalizadores de bits que indicam os atributos do contexto estabelecido. Para ver uma descrição dos vários atributos, confira [Requisitos de contexto.](context-requirements.md) Os sinalizadores usados para esse parâmetro são prefixados com ASC \_ RET, por exemplo, ASC \_ RET \_ DELEGATE.

Não verifique se há atributos relacionados à segurança até que a chamada de função final retorne com êxito. Sinalizadores de atributo não relacionados à segurança, como o sinalizador ASC \_ RET ALLOCATED MEMORY, podem ser verificados \_ antes do retorno \_ final.

*ptsExpiry* \[ out, opcional\]

Um ponteiro para uma [**estrutura TimeStamp**](timestamp.md) que recebe a hora de expiração do contexto. Recomendamos que o pacote de segurança sempre retorne esse valor no horário local.

> [!Note]  
> Até a última chamada do processo de autenticação, o tempo de expiração do contexto pode estar incorreto porque mais informações serão fornecidas durante os estágios posteriores da negociação. Portanto, *ptsTimeStamp* deve ser **NULL** até a última chamada para a função.

## <a name="return-value"></a>Valor retornado

Essa função retorna um dos valores a seguir.

| Valor/código de retorno                                   | Descrição                                                                                                                                                                 |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SEC_E_INCOMPLETE_MESSAGE <br/> 0x80090318L          | A função foi bem-sucedida. Os dados no buffer de entrada estão incompletos. O aplicativo deve ler dados adicionais do cliente e chamar [<strong>AcceptSecurityContext (CredSSP)</strong>](acceptsecuritycontext--credssp.md) novamente. |
| SEC_E_INSUFFICIENT_MEMORY <br/> 0x80090300L         | Falha na função. Não há memória suficiente disponível para concluir a ação solicitada.                                                                                 |
| SEC_E_INTERNAL_ERROR <br/> 0x80090304L              | Falha na função. Ocorreu um erro que não mapeou para um código de erro SSPI.                                                                                              |
| SEC_E_INVALID_HANDLE <br/> 0x80100003L              | Falha na função. O alça passado para a função não é válido.                                                                                                        |
| SEC_E_INVALID_TOKEN <br/> 0x80090308L               | Falha na função. O token passado para a função não é válido.                                                                                                         |
| SEC_E_LOGON_DENIED <br/> 0x8009030CL                | Falha no logon.                                                                                                                                                           |
| SEC_E_NO_AUTHENTICATING_AUTHORITY <br/> 0x80090311L | A função falhou. Nenhuma autoridade pode ser contatada para autenticação. Isso pode ser devido às seguintes condições:<br/><ul><li>O nome de domínio da parte de autenticação está incorreto.</li><li>O domínio não está disponível.</li><li>Falha na relação de confiança. |
| SEC_E_NO_CREDENTIALS <br/>0x8009030EL               | A função falhou. O identificador de credenciais especificado no parâmetro *phCredential* não é válido.                            |
| SEC_E_OK <br/> 0x00000000l                          | A função foi bem-sucedida. O contexto de segurança recebido do cliente foi aceito. Se a função gerou um token de saída, o token deve ser enviado ao processo do cliente. |
| SEC_E_UNSUPPORTED_FUNCTION <br/> 0x80090302L        | A função falhou. O parâmetro *fContextReq* especificou um sinalizador de atributo de contexto (ASC_REQ_DELEGATE ou ASC_REQ_PROMPT_FOR_CREDS) que não era válido.                       |
| SEC_I_COMPLETE_AND_CONTINUE <br/> 0x00090314L       | A função foi bem-sucedida. O servidor deve chamar [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) e passar o token de saída para o cliente. O servidor deve aguardar um token de retorno do cliente antes de fazer outra chamada para [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md). |
| SEC_I_COMPLETE_NEEDED <br/> 0x00090313L             | A função foi bem-sucedida. O servidor deve concluir a compilação da mensagem do cliente antes de chamar [ **CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)                             |
| SEC_I_CONTINUE_NEEDED <br/> 0x00090312L             | A função foi bem-sucedida. O servidor deve enviar o token de saída para o cliente e aguardar um token retornado. O token retornado deve ser passado em *pInput* para outra chamada para [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md).


## <a name="remarks"></a>Comentários

A função **AcceptSecurityContext (CredSSP)** é a contraparte do servidor para a função [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) .

Quando o servidor recebe uma solicitação de um cliente, ele usa o parâmetro *fContextReq* para especificar o que é necessário para a sessão. Dessa maneira, um servidor pode exigir que os clientes sejam capazes de usar uma sessão confidencial ou com verificação de [*integridade*](../secgloss/i-gly.md); Ele pode rejeitar clientes que não atendem a essa demanda. Como alternativa, um servidor pode não exigir nada; o que o cliente requer ou pode fornecer é retornado no parâmetro *pfContextAttr* .

Os parâmetros *fContextReq* e *pfContextAttr* são bitmasks que representam vários atributos de contexto. Para obter uma descrição dos vários atributos, consulte [requisitos de contexto](context-requirements.md).

> [!Note]  
> Embora o parâmetro *pfContextAttr* seja válido em qualquer retorno bem-sucedido, você deve examinar os sinalizadores referentes aos aspectos de segurança do contexto somente no retorno bem-sucedido final. Os retornos intermediários podem definir, por exemplo, o \_ \_ sinalizador de memória alocada do ISC RET \_ .

O chamador é responsável por determinar se os atributos de contexto final são suficientes. Por exemplo, se a confidencialidade (criptografia) foi solicitada, mas não pôde ser estabelecida, alguns aplicativos podem optar por desligar a conexão imediatamente. Se o contexto de segurança não puder ser estabelecido, o servidor deverá liberar o contexto parcialmente criado chamando a função [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) . Para obter informações sobre quando chamar a função **DeleteSecurityContext** , consulte **DeleteSecurityContext**.

Depois que o contexto de segurança tiver sido estabelecido, o aplicativo de servidor poderá usar a função [**QuerySecurityContextToken**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) para recuperar um identificador para a conta de usuário para a qual o certificado de cliente foi mapeado. Além disso, o servidor pode usar a função [**ImpersonateSecurityContext**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) para representar o usuário.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------------------------|-------------------------------------------|
| Cliente mínimo com suporte | \[somente aplicativos da área de trabalho do Windows Vista\]       |
| Servidor mínimo com suporte | Windows \[Somente aplicativos da área de trabalho do servidor 2008\] |
| Cabeçalho                   | SSPI. h (incluir Security. h)               |
| Biblioteca                  | Secur32. lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Confira também

- [Funções SSPI](authentication-functions.md#sspi-functions)
- [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
- [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md)
