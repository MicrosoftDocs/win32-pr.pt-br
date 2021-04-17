---
description: Permite que o componente de servidor de um aplicativo de transporte estabeleça um contexto de segurança entre o servidor e um cliente remoto.
ms.assetid: a53f733e-b646-4431-b021-a2c446308849
title: Função AcceptSecurityContext (CredSSP)
ms.topic: article
ms.date: 07/25/2019
ms.openlocfilehash: 681e03ea15729cc8726d63551e8b7b0a2b39ecac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790427"
---
# <a name="acceptsecuritycontext-credssp-function"></a>Função AcceptSecurityContext (CredSSP)

A função **AcceptSecurityContext (CredSSP)** permite que o componente de servidor de um aplicativo de transporte estabeleça um contexto de segurança entre o servidor e um cliente remoto. O cliente remoto chama a função [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) para iniciar o processo de estabelecimento de um contexto de segurança. O servidor pode exigir um ou mais tokens de resposta do cliente remoto para concluir o estabelecimento do contexto de segurança.

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

*phCredential* \[ em, opcional\]

Um identificador para as credenciais do servidor. Para recuperar esse identificador, o servidor chama a função [**falha AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md) com o sinalizador de \_ entrada SECPKG cred \_ ou SECPKG \_ creds \_ .

*phContext* \[ em, opcional\]

Um ponteiro para uma estrutura [CtxtHandle](sspi-handles.md) . Na primeira chamada para **AcceptSecurityContext (CredSSP)**, esse ponteiro é **nulo**. Nas chamadas subsequentes, *phContext* especifica o contexto parcialmente formado retornado no parâmetro *phNewContext* pela primeira chamada.

*pInput* \[ em, opcional\]

Um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) gerada por uma chamada de cliente para [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md). A estrutura contém o descritor de buffer de entrada.

O primeiro buffer deve ser do tipo **\_ token SECBUFFER** e conter o token de segurança recebido do cliente. O segundo buffer deve ser do tipo **SECBUFFER \_ vazio**.

*fContextReq* \[ no\]

– Sinalizadores de bits que especificam os atributos exigidos pelo servidor para estabelecer o contexto. Os sinalizadores de bits podem ser combinados usando operações de bit-a-**ou** . Esse parâmetro pode ser um ou mais dos valores a seguir.

| Valor                          | Significado                                                                                                                                                                                                        |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **memória de alocação do ASC \_ req \_ \_** | O CredSSP (provedor de suporte à segurança de credencial) alocará buffers de saída. Quando você terminar de usar os buffers de saída, libere-os chamando a função [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) . |
| **\_conexão de req. asc \_**       | O contexto de segurança não tratará mensagens de formatação.                                                                                                                                                      |
| **\_delegado de req ASC \_**         | O servidor tem permissão para representar o cliente. Ignore este sinalizador para delegação restrita.                                                         |
| **\_ \_ erro estendido de req. asc \_**  | Quando ocorrerem erros, a parte remota será notificada.                                                                                                                                                          |
| **\_detecção de \_ Replay de req do ASC \_**   | Detectar pacotes reproduzidos.                                                                                                                                                                                       |
| **\_detecção de \_ sequência de req do ASC \_** | Detecte mensagens recebidas fora de sequência.                                                                                                                                                                      |
| **\_fluxo de req. asc \_**           | Suporte a uma conexão orientada a fluxo.                                                                                                                                                                          |

Para possíveis sinalizadores de atributo e seus significados, consulte [requisitos de contexto](context-requirements.md). Os sinalizadores usados para esse parâmetro são prefixados com o ASC \_ req, por exemplo, o \_ delegado de req ASC \_ .

Os atributos solicitados podem não ter suporte do cliente. Para obter mais informações, consulte o parâmetro *pfContextAttr* .

*TargetDataRep* \[ no\]

A representação de dados, como ordenação de bytes, no destino. Esse parâmetro pode ser **segurança \_ nativa \_ DREP** ou segurança de **\_ rede \_ DREP**.

*phNewContext* \[ entrada, saída, opcional\]

Um ponteiro para uma estrutura [CtxtHandle](sspi-handles.md) . Na primeira chamada para **AcceptSecurityContext (CredSSP)**, esse ponteiro recebe o novo identificador de contexto. Nas chamadas subsequentes, *phNewContext* pode ser o mesmo que o identificador especificado no parâmetro *phContext* .

*pOutput* \[ entrada, saída, opcional\]

Um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) que contém o descritor de buffer de saída. Esse buffer é enviado ao cliente para entrada em chamadas adicionais para [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md). Um buffer de saída pode ser gerado mesmo que a função retorne s \_ E \_ OK. Qualquer buffer gerado deve ser enviado de volta para o aplicativo cliente.

Na saída, esse buffer recebe um token para o contexto de segurança. O token deve ser enviado ao cliente. A função também pode retornar um buffer do tipo SECBUFFER \_ extra.

*pfContextAttr* \[ fora\]

Um ponteiro para um conjunto de sinalizadores de bit que indicam os atributos do contexto estabelecido. Para obter uma descrição dos vários atributos, consulte [requisitos de contexto](context-requirements.md). Os sinalizadores usados para esse parâmetro são prefixados com ASC \_ RET, por exemplo, o delegado de ASC \_ RET \_ .

Não verifique os atributos relacionados à segurança até que a chamada de função final seja retornada com êxito. Os sinalizadores de atributo não relacionados à segurança, como o \_ \_ sinalizador de memória alocada de ASC RET \_ , podem ser verificados antes do retorno final.

*ptsExpiry* \[ out, opcional\]

Um ponteiro para uma estrutura de [**carimbo de data/**](timestamp.md) hora que recebe o tempo de expiração do contexto. É recomendável que o pacote de segurança sempre retorne esse valor na hora local.

> [!Note]  
> Até a última chamada do processo de autenticação, o tempo de expiração do contexto pode estar incorreto, pois mais informações serão fornecidas durante os estágios posteriores da negociação. Portanto, *ptsTimeStamp* deve ser **nulo** até a última chamada para a função.

## <a name="return-value"></a>Retornar valor

Essa função retorna um dos valores a seguir.

| Código/valor de retorno                                   | Descrição                                                                                                                                                                 |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SEC_E_INCOMPLETE_MESSAGE <br/> 0x80090318L          | A função foi bem-sucedida. Os dados no buffer de entrada estão incompletos. O aplicativo deve ler dados adicionais do cliente e chamar [<strong>AcceptSecurityContext (CredSSP)</strong>](acceptsecuritycontext--credssp.md) novamente. |
| SEC_E_INSUFFICIENT_MEMORY <br/> 0x80090300L         | A função falhou. Não há memória suficiente disponível para concluir a ação solicitada.                                                                                 |
| SEC_E_INTERNAL_ERROR <br/> 0x80090304L              | A função falhou. Ocorreu um erro que não foi mapeado para um código de erro SSPI.                                                                                              |
| SEC_E_INVALID_HANDLE <br/> 0x80100003L              | A função falhou. O identificador passado para a função não é válido.                                                                                                        |
| SEC_E_INVALID_TOKEN <br/> 0x80090308L               | A função falhou. O token passado para a função não é válido.                                                                                                         |
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
| Cliente mínimo com suporte | \[Somente aplicativos da área de trabalho do Windows Vista\]       |
| Servidor mínimo com suporte | \[Somente aplicativos da área de trabalho do Windows Server 2008\] |
| parâmetro                   | SSPI. h (incluir Security. h)               |
| Biblioteca                  | Secur32. lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Confira também

- [Funções SSPI](authentication-functions.md#sspi-functions)
- [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
- [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md)
