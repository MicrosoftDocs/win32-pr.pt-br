---
description: Permite que o componente de servidor de um aplicativo de transporte estabeleça um [*contexto de segurança*](../secgloss/s-gly.md) entre o servidor e um cliente remoto que esteja usando o Kerberos.
ms.assetid: 838eaaa7-6fce-4ed1-bd69-6e76a804c67b
title: Função AcceptSecurityContext (Kerberos) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 2c379aa0f111e24d534bb14746df4b0e7cbbc9c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812418"
---
# <a name="acceptsecuritycontext-kerberos-function"></a>Função AcceptSecurityContext (Kerberos)

A função **AcceptSecurityContext (Kerberos)** permite que o componente de servidor de um aplicativo de transporte estabeleça um [*contexto de segurança*](../secgloss/s-gly.md) entre o servidor e um cliente remoto. O cliente remoto usa a função [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) para iniciar o processo de estabelecimento de um [*contexto de segurança*](../secgloss/s-gly.md). O servidor pode exigir um ou mais tokens de resposta do cliente remoto para concluir o estabelecimento do [*contexto de segurança*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS SEC_Entry AcceptSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_opt_    PSecBufferDesc pInput,
  _In_        ULONG          fContextReq,
  _In_        ULONG          TargetDataRep,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Inout_opt_ PSecBufferDesc pOutput,
  _Out_       PULONG         pfContextAttr,
  _Out_opt_   PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*phCredential* \[ em, opcional\]
</dt> <dd>

Um identificador para as credenciais do servidor. O servidor chama a função [**falha AcquireCredentialsHandle (Kerberos)**](acquirecredentialshandle--kerberos.md) com o sinalizador de \_ entrada de credenciais SECPKG \_ ou SECPKG \_ cred \_ both definido para recuperar esse identificador.

</dd> <dt>

*phContext* \[ entrada, saída, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura [CtxtHandle](sspi-handles.md) . Na primeira chamada para **AcceptSecurityContext (Kerberos)**, esse ponteiro é **nulo**. Nas chamadas subsequentes, *phContext* é o identificador para o contexto parcialmente formado que foi retornado no parâmetro *phNewContext* pela primeira chamada.

</dd> <dt>

*pInput* \[ em, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) gerada por uma chamada de cliente para [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) que contém o descritor de buffer de entrada.

As informações de associação de canal podem ser especificadas passando uma estrutura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) do **tipo \_ \_ associações de canal SecBuffer** , além dos buffers gerados pela chamada para a função [**InitializeSecurityContext (geral)**](initializesecuritycontext--general.md) . As informações de associação de canal para o buffer de associação de canal podem ser obtidas chamando a função [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) no contexto Schannel que o cliente usou para autenticar.

</dd> <dt>

*fContextReq* \[ no\]
</dt> <dd>

Sinalizadores de bits que especificam os atributos exigidos pelo servidor para estabelecer o contexto. Os sinalizadores de bits podem ser combinados usando operações de bit-a-**ou** . Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                         | Significado                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASC_REQ_CONFIDENTIALITY"></span><span id="asc_req_confidentiality"></span><dl> <dt>**\_confidencialidade de req. asc \_**</dt> </dl>  | Criptografar e descriptografar mensagens.<br/>                                                                                                                                                                                   |
| <span id="ASC_REQ_CONNECTION"></span><span id="asc_req_connection"></span><dl> <dt>**\_conexão de req. asc \_**</dt> </dl>                 | O [*contexto de segurança*](../secgloss/s-gly.md) não tratará mensagens de formatação.<br/>                                                                                                                                                       |
| <span id="ASC_REQ_DELEGATE"></span><span id="asc_req_delegate"></span><dl> <dt>**\_delegado de req ASC \_**</dt> </dl>                       | O servidor tem permissão para representar o cliente. Válido para Kerberos. Ignore este sinalizador para [*delegação restrita*](../secgloss/c-gly.md).<br/> |
| <span id="ASC_REQ_EXTENDED_ERROR"></span><span id="asc_req_extended_error"></span><dl> <dt>**\_ \_ erro estendido de req. asc \_**</dt> </dl>    | Quando ocorrerem erros, a parte remota será notificada.<br/>                                                                                                                                                           |
| <span id="ASC_REQ_INTEGRITY"></span><span id="asc_req_integrity"></span><dl> <dt>**\_integridade de req ASC \_**</dt> </dl>                    | Assinar mensagens e verificar assinaturas.<br/>                                                                                                                                                                            |
| <span id="ASC_REQ_REPLAY_DETECT"></span><span id="asc_req_replay_detect"></span><dl> <dt>**\_detecção de \_ Replay de req do ASC \_**</dt> </dl>       | Detectar pacotes reproduzidos.<br/>                                                                                                                                                                                        |
| <span id="ASC_REQ_SEQUENCE_DETECT"></span><span id="asc_req_sequence_detect"></span><dl> <dt>**\_detecção de \_ sequência de req do ASC \_**</dt> </dl> | Detecte mensagens recebidas fora de sequência.<br/>                                                                                                                                                                       |



 

Para possíveis sinalizadores de atributo e seus significados, consulte [requisitos de contexto](context-requirements.md). Os sinalizadores usados para esse parâmetro são prefixados com o ASC \_ req, por exemplo, o \_ delegado de req ASC \_ .

Os atributos solicitados podem não ter suporte do cliente. Para obter mais informações, consulte o parâmetro *pfContextAttr* .

</dd> <dt>

*TargetDataRep* \[ no\]
</dt> <dd>

A representação de dados, como ordenação de bytes, no destino. Esse parâmetro pode ser segurança \_ nativa \_ DREP ou segurança de \_ rede \_ DREP.

</dd> <dt>

*phNewContext* \[ entrada, saída, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura [CtxtHandle](sspi-handles.md) . Na primeira chamada para **AcceptSecurityContext (Kerberos)**, esse ponteiro recebe o novo identificador de contexto. Nas chamadas subsequentes, *phNewContext* pode ser o mesmo que o identificador especificado no parâmetro *phContext* .

</dd> <dt>

*pOutput* \[ entrada, saída, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) que contém o descritor de buffer de saída. Esse buffer é enviado ao cliente para entrada em chamadas adicionais para [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md). Um buffer de saída pode ser gerado mesmo que a função retorne s \_ E \_ OK. Qualquer buffer gerado deve ser enviado de volta para o aplicativo cliente.

</dd> <dt>

*pfContextAttr* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe um conjunto de sinalizadores de bits que indicam os atributos do contexto estabelecido. Para obter uma descrição dos vários atributos, consulte [requisitos de contexto](context-requirements.md). Os sinalizadores usados para esse parâmetro são prefixados com ASC \_ RET, por exemplo, o delegado de ASC \_ RET \_ .

Não verifique os atributos relacionados à segurança até que a chamada de função final seja retornada com êxito. Os sinalizadores de atributo não relacionados à segurança, como o \_ \_ sinalizador de memória alocada de ASC RET \_ , podem ser verificados antes do retorno final.

</dd> <dt>

*ptsTimeStamp* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura de [**carimbo de data/**](timestamp.md) hora que recebe o tempo de expiração do contexto. É recomendável que o [*pacote de segurança*](../secgloss/s-gly.md) sempre retorne esse valor na hora local.

> [!Note]  
> Até a última chamada do processo de autenticação, o tempo de expiração do contexto pode estar incorreto, pois mais informações serão fornecidas durante os estágios posteriores da negociação. Portanto, *ptsTimeStamp* deve ser **nulo** até a última chamada para a função.

 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função retorna um dos valores a seguir.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Código/valor de retorno</th><th>Descrição</th></tr></thead><tbody><tr class="odd"><td><dl> <dt><strong>SEC_E_INSUFFICIENT_MEMORY</strong></dt> <dt>0x80090300L</dt> </dl></td><td>A função falhou. Não há memória suficiente disponível para concluir a ação solicitada.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INTERNAL_ERROR</strong></dt> <dt>0x80090304L</dt> </dl></td><td>A função falhou. Ocorreu um erro que não foi mapeado para um código de erro SSPI.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INVALID_HANDLE</strong></dt> <dt>0x80100003L</dt> </dl></td><td>A função falhou. O identificador passado para a função não é válido.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INVALID_TOKEN</strong></dt> <dt>0x80090308L</dt> </dl></td><td>A função falhou. O token passado para a função não é válido.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_LOGON_DENIED</strong></dt> <dt>0x8009030CL</dt> </dl></td><td>Falha no logon.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_NO_AUTHENTICATING_AUTHORITY</strong></dt> <dt>0x80090311L</dt> </dl></td><td>A função falhou. Nenhuma autoridade pode ser contatada para autenticação. Isso pode ser devido às seguintes condições:<br/><ul><li>O nome de domínio da parte de autenticação está incorreto.</li><li>O domínio não está disponível.</li><li>Falha na relação de confiança.</li></ul></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_OK</strong></dt> <dt>0x00000000l</dt> </dl></td><td>A função foi bem-sucedida. O [*contexto de segurança*](../secgloss/s-gly.md) recebido do cliente foi aceito. Se um token de saída foi gerado pela função, ele deve ser enviado para o processo do cliente.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_UNSUPPORTED_FUNCTION</strong></dt> <dt>0x80090302L</dt> </dl></td><td>A função falhou. Um sinalizador de atributo de contexto que não é válido (ASC_REQ_DELEGATE ou ASC_REQ_PROMPT_FOR_CREDS) foi especificado no parâmetro <em>fContextReq</em> . Esse valor pode ser retornado ao usar o SSP do Schannel.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_COMPLETE_AND_CONTINUE</strong></dt> <dt>0x00090314L</dt> </dl></td><td>A função foi bem-sucedida. O servidor deve chamar [<strong>CompleteAuthToken</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-CompleteAuthToken) e passar o token de saída para o cliente. Em seguida, o servidor aguarda um token de retorno do cliente e, em seguida, faz outra chamada para [<strong>AcceptSecurityContext (Kerberos)</strong>] (AcceptSecurityContext--Kerberos.MD).<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_COMPLETE_NEEDED</strong></dt> <dt>0x00090313L</dt> </dl></td><td>A função foi bem-sucedida. O servidor deve concluir a compilação da mensagem do cliente e, em seguida, chamar a função [<strong>CompleteAuthToken</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-CompleteAuthToken).<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_CONTINUE_NEEDED</strong></dt> <dt>0x00090312L</dt> </dl></td><td>A função foi bem-sucedida. O servidor deve enviar o token de saída para o cliente e aguardar um token retornado. O token retornado deve ser passado em <em>pInput</em> para outra chamada para [<strong>AcceptSecurityContext (Kerberos)</strong>] (AcceptSecurityContext--Kerberos.MD).<br/></td></tr></tbody></table>



 

## <a name="remarks"></a>Comentários

A função **AcceptSecurityContext (Kerberos)** é a contraparte do servidor para a função [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) .

Quando o servidor recebe uma solicitação de um cliente, o servidor usa o parâmetro *fContextReq* para especificar o que é necessário para a sessão. Dessa maneira, um servidor pode especificar que os clientes devem ser capazes de usar uma sessão confidencial ou com verificação de [*integridade*](../secgloss/i-gly.md), e pode rejeitar clientes que não podem atender a essa demanda. Como alternativa, um servidor pode não exigir nada e tudo o que o cliente pode fornecer ou exigir é retornado no parâmetro *pfContextAttr* .

Para um pacote que dá suporte à autenticação de vários trechos, como a autenticação mútua, a sequência de chamada é a seguinte:

1.  O cliente transmite um token para o servidor.
2.  O servidor chama **AcceptSecurityContext (Kerberos)** pela primeira vez, o que gera um token de resposta que é enviado para o cliente.
3.  O cliente recebe o token e o passa para [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md). Se **InitializeSecurityContext (Kerberos)** retornar s \_ e \_ OK, a autenticação mútua foi concluída e uma sessão segura pode começar. Se **InitializeSecurityContext (Kerberos)** retornar um código de erro, a negociação de autenticação mútua terminará. Caso contrário, o token de segurança retornado por **InitializeSecurityContext (Kerberos)** é enviado ao cliente e as etapas 2 e 3 são repetidas.

Os parâmetros *fContextReq* e *pfContextAttr* são bitmasks que representam vários atributos de contexto. Para obter uma descrição dos vários atributos, consulte [requisitos de contexto](context-requirements.md).

> [!Note]  
> O parâmetro *pfContextAttr* é válido em qualquer retorno bem-sucedido, mas somente no retorno bem-sucedido final, você deve examinar os sinalizadores referentes aos aspectos de segurança do contexto. Os retornos intermediários podem definir, por exemplo, o \_ \_ sinalizador de memória alocada do ISC RET \_ .

 

O chamador é responsável por determinar se os atributos de contexto final são suficientes. Se, por exemplo, a confidencialidade (criptografia) tiver sido solicitada, mas não puder ser estabelecida, alguns aplicativos poderão optar por desligar a conexão imediatamente. Se o [*contexto de segurança*](../secgloss/s-gly.md) não puder ser estabelecido, o servidor deverá liberar o contexto parcialmente criado chamando a função [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) . Para obter informações sobre quando chamar a função **DeleteSecurityContext** , consulte **DeleteSecurityContext**.

Depois que o [*contexto de segurança*](../secgloss/s-gly.md) tiver sido estabelecido, o aplicativo de servidor poderá usar a função [**QuerySecurityContextToken**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) para recuperar um identificador para a conta de usuário para a qual o certificado de cliente foi mapeado. Além disso, o servidor pode usar a função [**ImpersonateSecurityContext**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) para representar o usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                   |
| parâmetro<br/>                   | <dl> <dt>SSPI. h (incluir Security. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md)
</dt> </dl>

 

 
