---
description: Permite que o componente de servidor [](../secgloss/s-gly.md) de um aplicativo de transporte estabeleça um contexto de segurança entre o servidor e um cliente remoto que está usando Negotiate.
ms.assetid: aaec6fee-df6b-4033-8ece-73ecd1799653
title: Função AcceptSecurityContext (Negotiate) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 13aa91545e5301e10a1f9d36e93e2d4995c15253
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628686"
---
# <a name="acceptsecuritycontext-negotiate-function"></a>Função AcceptSecurityContext (Negotiate)

A **função AcceptSecurityContext (Negotiate)** permite que o componente [](../secgloss/s-gly.md) de servidor de um aplicativo de transporte estabeleça um contexto de segurança entre o servidor e um cliente remoto. O cliente remoto usa a [**função InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) para iniciar o processo de estabelecimento de um [*contexto de segurança*](../secgloss/s-gly.md). O servidor pode exigir um ou mais tokens de resposta do cliente remoto para concluir o estabelecimento do [*contexto de segurança*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS SEC_Entry AcceptSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _Inout_opt_ PCtxtHandle    phContext,
  _In_opt_    PSecBufferDesc pInput,
  _In_        ULONG          fContextReq,
  _In_        ULONG          TargetDataRep,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Inout_opt_ PSecBufferDesc pOutput,
  _Out_       PULONG         pfContextAttr,
  _Out_opt_   PTimeStamp     ptsTimeStamp
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*phCredential* \[ in, opcional\]
</dt> <dd>

Um handle para as credenciais do servidor. O servidor chama [**a função AcquireCredentialsHandle (Negotiate)**](acquirecredentialshandle--negotiate.md) com o sinalizador SECPKG \_ CRED INBOUND ou SECPKG CRED BOTH definido para recuperar esse \_ \_ \_ identificador.

</dd> <dt>

*phContext* \[ in, out, opcional\]
</dt> <dd>

Um ponteiro para uma [estrutura CtxtHandle.](sspi-handles.md) Na primeira chamada para **AcceptSecurityContext (Negotiate),** esse ponteiro é **NULL.** Em chamadas subsequentes, *phContext* é o handle para o contexto parcialmente formado que foi retornado no parâmetro *phNewContext* pela primeira chamada.

</dd> <dt>

*pInput* \[ in, opcional\]
</dt> <dd>

Um ponteiro para uma [**estrutura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) gerada por uma chamada do cliente para [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) que contém o descritor de buffer de entrada.

As informações de associação de canal podem ser especificadas passando uma estrutura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) do tipo **SECBUFFER \_ CHANNEL \_ BINDINGS,** além dos buffers gerados pela chamada para a função [**InitializeSecurityContext (Geral).**](initializesecuritycontext--general.md) As informações de associação de canal para o buffer de associação de canal podem ser obtidas chamando a função [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) no contexto Schannel que o cliente usou para autenticar.

</dd> <dt>

*fContextReq* \[ Em\]
</dt> <dd>

Sinalizadores de bits que especificam os atributos exigidos pelo servidor para estabelecer o contexto. Os sinalizadores de bit podem ser combinados usando operações **OR** bit a bit. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                         | Significado                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASC_REQ_CONFIDENTIALITY"></span><span id="asc_req_confidentiality"></span><dl> <dt>**CONFIDENCIALIDADE DO ASC \_ REQ \_**</dt> </dl>  | Criptografar e descriptografar mensagens.<br/>                                                                                                                                                                                   |
| <span id="ASC_REQ_CONNECTION"></span><span id="asc_req_connection"></span><dl> <dt>**CONEXÃO ASC \_ REQ \_**</dt> </dl>                 | O [*contexto de segurança*](../secgloss/s-gly.md) não manipulará mensagens de formatação.<br/>                                                                                                                                                       |
| <span id="ASC_REQ_DELEGATE"></span><span id="asc_req_delegate"></span><dl> <dt>**ASC \_ REQ \_ DELEGATE**</dt> </dl>                       | O servidor tem permissão para representar o cliente. Válido para Kerberos. Ignore esse sinalizador para [*delegação restrita.*](../secgloss/c-gly.md)<br/> |
| <span id="ASC_REQ_EXTENDED_ERROR"></span><span id="asc_req_extended_error"></span><dl> <dt>**ERRO ESTENDIDO DO ASC \_ REQ \_ \_**</dt> </dl>    | Quando ocorrerem erros, a parte remota será notificada.<br/>                                                                                                                                                           |
| <span id="ASC_REQ_INTEGRITY"></span><span id="asc_req_integrity"></span><dl> <dt>**INTEGRIDADE DA \_ ASC REQ \_**</dt> </dl>                    | Assinar mensagens e verificar assinaturas.<br/>                                                                                                                                                                            |
| <span id="ASC_REQ_REPLAY_DETECT"></span><span id="asc_req_replay_detect"></span><dl> <dt>**ASC \_ REQ \_ REPLAY \_ DETECT**</dt> </dl>       | Detectar pacotes replayed.<br/>                                                                                                                                                                                        |
| <span id="ASC_REQ_SEQUENCE_DETECT"></span><span id="asc_req_sequence_detect"></span><dl> <dt>**ASC \_ REQ \_ SEQUENCE \_ DETECT**</dt> </dl> | Detectar mensagens recebidas fora de sequência.<br/>                                                                                                                                                                       |



 

Para possíveis sinalizadores de atributo e seus significados, consulte [Requisitos de contexto.](context-requirements.md) Sinalizadores usados para esse parâmetro são prefixados com ASC \_ REQ, por exemplo, ASC \_ REQ \_ DELEGATE.

Os atributos solicitados podem não ser suportados pelo cliente. Para obter mais informações, consulte o *parâmetro pfContextAttr.*

</dd> <dt>

*TargetDataRep* \[ Em\]
</dt> <dd>

A representação de dados, como ordenação de byte, no destino. Esse parâmetro pode ser SECURITY \_ NATIVE \_ DREP ou SECURITY \_ NETWORK \_ DREP.

</dd> <dt>

*phNewContext* \[ in, out, opcional\]
</dt> <dd>

Um ponteiro para uma [estrutura CtxtHandle.](sspi-handles.md) Na primeira chamada para **AcceptSecurityContext (Negotiate),** esse ponteiro recebe o novo indicador de contexto. Em chamadas subsequentes, *phNewContext* pode ser o mesmo que o handle especificado no *parâmetro phContext.*

</dd> <dt>

*pOutput* \[ in, out, opcional\]
</dt> <dd>

Um ponteiro para uma [**estrutura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) que contém o descritor de buffer de saída. Esse buffer é enviado ao cliente para entrada em chamadas adicionais para [**InitializeSecurityContext (Negotiate).**](initializesecuritycontext--negotiate.md) Um buffer de saída pode ser gerado mesmo que a função retorne SEC \_ E \_ OK. Qualquer buffer gerado deve ser enviado de volta para o aplicativo cliente.

</dd> <dt>

*pfContextAttr* \[ out\]
</dt> <dd>

Um ponteiro para uma variável que recebe um conjunto de sinalizadores de bits que indicam os atributos do contexto estabelecido. Para ver uma descrição dos vários atributos, confira [Requisitos de contexto.](context-requirements.md) Os sinalizadores usados para esse parâmetro são prefixados com ASC \_ RET, por exemplo, ASC \_ RET \_ DELEGATE.

Não verifique se há atributos relacionados à segurança até que a chamada de função final retorne com êxito. Sinalizadores de atributo não relacionados à segurança, como o sinalizador ASC \_ RET ALLOCATED MEMORY, podem ser verificados \_ antes do retorno \_ final.

</dd> <dt>

*ptsTimeStamp* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma [**estrutura TimeStamp**](timestamp.md) que recebe a hora de expiração do contexto. Recomendamos que o [*pacote de segurança*](../secgloss/s-gly.md) sempre retorne esse valor no horário local.

> [!Note]  
> Até a última chamada do processo de autenticação, o tempo de expiração do contexto pode estar incorreto porque mais informações serão fornecidas durante os estágios posteriores da negociação. Portanto, *ptsTimeStamp* deve ser **NULL** até a última chamada para a função.

 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa função retorna um dos valores a seguir.



<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th>Valor/código de retorno</th><th>Descrição</th></tr></thead><tbody><tr class="odd"><td><dl> <dt><strong>SEC_E_INSUFFICIENT_MEMORY</strong></dt> <dt>0x80090300L</dt> </dl></td><td>Falha na função. Não há memória suficiente disponível para concluir a ação solicitada.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INTERNAL_ERROR</strong></dt> <dt>0x80090304L</dt> </dl></td><td>Falha na função. Ocorreu um erro que não mapeou para um código de erro SSPI.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INVALID_HANDLE</strong></dt> <dt>0x80100003L</dt> </dl></td><td>Falha na função. O alça passado para a função não é válido.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INVALID_TOKEN</strong></dt> <dt>0x80090308L</dt> </dl></td><td>Falha na função. O token passado para a função não é válido.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_LOGON_DENIED</strong></dt> <dt>0x8009030CL</dt> </dl></td><td>Falha no logon.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_NO_AUTHENTICATING_AUTHORITY</strong></dt> <dt>0x80090311L</dt> </dl></td><td>Falha na função. Nenhuma autoridade pode ser contata para autenticação. Isso pode ser devido às seguintes condições:<br/><ul><li>O nome de domínio da parte de autenticação está incorreto.</li><li>O domínio não está disponível.</li><li>A relação de confiança falhou.</li></ul></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_OK</strong></dt> <dt>0x0000000L</dt> </dl></td><td>A função foi bem-sucedida. O [*contexto de*](../secgloss/s-gly.md) segurança recebido do cliente foi aceito. Se um token de saída tiver sido gerado pela função, ele deverá ser enviado para o processo do cliente.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_COMPLETE_AND_CONTINUE</strong></dt> <dt>0x00090314L</dt> </dl></td><td>A função foi bem-sucedida. O servidor deve chamar [<strong>CompleteAuthToken</strong>](/windows/win32/api/sspi/nf-sspi-completeauthtoken) e passar o token de saída para o cliente. Em seguida, o servidor aguarda um token de retorno do cliente e, em seguida, faz outra chamada para [<strong>AcceptSecurityContext (Negotiate)</strong>](acceptsecuritycontext--negotiate.md).<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_COMPLETE_NEEDED</strong></dt> <dt>0x00090313L</dt> </dl></td><td>A função foi bem-sucedida. O servidor deve concluir a criação da mensagem do cliente e chamar a função [<strong>CompleteAuthToken</strong>](/windows/win32/api/sspi/nf-sspi-completeauthtoken).<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_CONTINUE_NEEDED</strong></dt> <dt>0x00090312L</dt> </dl></td><td>A função foi bem-sucedida. O servidor deve enviar o token de saída para o cliente e aguardar um token retornado. O token retornado deve ser passado em <em>pInput</em> para outra chamada para [<strong>AcceptSecurityContext (Negotiate)</strong>](acceptsecuritycontext--negotiate.md).<br/></td></tr></tbody></table>



 

## <a name="remarks"></a>Comentários

A **função AcceptSecurityContext (Negotiate)** é o equivalente do servidor à [**função InitializeSecurityContext (Negotiate).**](initializesecuritycontext--negotiate.md)

Quando o servidor recebe uma solicitação de um cliente, o servidor usa o *parâmetro fContextReq* para especificar o que ele requer da sessão. Dessa forma, um servidor pode especificar que os clientes [](../secgloss/i-gly.md)devem ser capazes de usar uma sessão confidencial ou de integridade verificada e pode rejeitar clientes que não podem atender a essa demanda. Como alternativa, um servidor não pode exigir nada e o que o cliente puder fornecer ou exigir será retornado no *parâmetro pfContextAttr.*

Para um pacote que dá suporte à autenticação de várias etapas, como autenticação mútua, a sequência de chamada é a seguinte:

1.  O cliente transmite um token para o servidor.
2.  O servidor chama **AcceptSecurityContext (Negotiate)** pela primeira vez, o que gera um token de resposta que é enviado ao cliente.
3.  O cliente recebe o token e o passa para [**InitializeSecurityContext (Negotiate).**](initializesecuritycontext--negotiate.md) Se **InitializeSecurityContext (Negotiate)** retornar SEC E OK, a autenticação mútua será concluída e \_ uma sessão segura poderá \_ começar. Se **InitializeSecurityContext (Negotiate) retornar** um código de erro, a negociação de autenticação mútua terminará. Caso contrário, o token de segurança retornado por **InitializeSecurityContext (Negotiate)** será enviado ao cliente e as etapas 2 e 3 serão repetidas.

Os *parâmetros fContextReq* e *pfContextAttr* são bitmasks que representam vários atributos de contexto. Para ver uma descrição dos vários atributos, confira [Requisitos de contexto.](context-requirements.md)

> [!Note]  
> O *parâmetro pfContextAttr* é válido em qualquer retorno bem-sucedido, mas somente no retorno final bem-sucedido você deve examinar os sinalizadores pertencentes aos aspectos de segurança do contexto. Os retornos intermediários podem definir, por exemplo, o sinalizador ISC \_ RET \_ ALLOCATED \_ MEMORY.

 

O chamador é responsável por determinar se os atributos de contexto finais são suficientes. Se, por exemplo, a confidencialidade (criptografia) tiver sido solicitada, mas não puder ser estabelecida, alguns aplicativos poderão optar por desligar a conexão imediatamente. Se o [*contexto de segurança*](../secgloss/s-gly.md) não puder ser estabelecido, o servidor deverá liberar o contexto parcialmente criado chamando a função [**DeleteSecurityContext.**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) Para obter informações sobre quando chamar a **função DeleteSecurityContext,** consulte **DeleteSecurityContext**.

Depois que [*o*](../secgloss/s-gly.md) contexto de segurança tiver sido estabelecido, o aplicativo de servidor poderá usar a função [**QuerySecurityContextToken**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) para recuperar um handle para a conta de usuário para a qual o certificado do cliente foi mapeado. Além disso, o servidor pode usar a [**função ImpersonateSecurityContext**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) para representar o usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                   |
| Cabeçalho<br/>                   | <dl> <dt>Sspi.h (inclua Security.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md)
</dt> </dl>

 

 
