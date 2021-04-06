---
description: Habilita o componente de servidor de um aplicativo de transporte para estabelecer um [*contexto de segurança*](../secgloss/s-gly.md) entre o servidor e um cliente remoto.
ms.assetid: eaa15fed-4438-4e43-9be3-aa100ca453c7
title: Função AcceptSecurityContext (geral) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 41b3220e9304f63e1a6ac4f77b609e3cbbac8741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828696"
---
# <a name="acceptsecuritycontext-general-function"></a>Função AcceptSecurityContext (geral)

A função **AcceptSecurityContext (geral)** permite que o componente de servidor de um aplicativo de transporte estabeleça um [*contexto de segurança*](../secgloss/s-gly.md) entre o servidor e um cliente remoto. O cliente remoto usa a função [**InitializeSecurityContext (geral)**](initializesecuritycontext--general.md) para iniciar o processo de estabelecimento de um [*contexto de segurança*](../secgloss/s-gly.md). O servidor pode exigir um ou mais tokens de resposta do cliente remoto para concluir o estabelecimento do [*contexto de segurança*](../secgloss/s-gly.md).

Para obter informações sobre como usar essa função com um SSP ( [*provedor de suporte de segurança*](../secgloss/s-gly.md) ) específico, consulte os tópicos a seguir.



| Tópico                                                                          | Descrição                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md)     | Permite que o componente de servidor de um aplicativo de transporte estabeleça um [*contexto de segurança*](../secgloss/s-gly.md) entre o servidor e um cliente remoto usando o Credential Security Support Provider (CredSSP).<br/> |
| [**AcceptSecurityContext (resumo)**](acceptsecuritycontext--digest.md)       | Habilita o componente de servidor de um aplicativo de transporte para estabelecer um [*contexto de segurança*](../secgloss/s-gly.md) entre o servidor e um cliente remoto que está usando o Digest.<br/>                                                                                                                  |
| [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md)   | Permite que o componente de servidor de um aplicativo de transporte estabeleça um [*contexto de segurança*](../secgloss/s-gly.md) entre o servidor e um cliente remoto que esteja usando o Kerberos.<br/>                                                                                                                |
| [**AcceptSecurityContext (negociar)**](acceptsecuritycontext--negotiate.md) | Habilita o componente de servidor de um aplicativo de transporte para estabelecer um [*contexto de segurança*](../secgloss/s-gly.md) entre o servidor e um cliente remoto que está usando Negotiate.<br/>                                                                                                               |
| [**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md)           | Habilita o componente de servidor de um aplicativo de transporte para estabelecer um [*contexto de segurança*](../secgloss/s-gly.md) entre o servidor e um cliente remoto que está usando NTLM.<br/>                                                                                                                    |
| [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md)   | Habilita o componente de servidor de um aplicativo de transporte para estabelecer um [*contexto de segurança*](../secgloss/s-gly.md) entre o servidor e um cliente remoto que está usando Schannel.<br/>                                                                                                                |



 

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
  _Out_opt_   PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*phCredential* \[ em, opcional\]
</dt> <dd>

Um identificador para as credenciais do servidor. O servidor chama a função [**falha AcquireCredentialsHandle (geral)**](acquirecredentialshandle--general.md) com o sinalizador de \_ entrada de credenciais SECPKG \_ ou SECPKG \_ cred \_ Ambos definido para recuperar esse identificador.

</dd> <dt>

*phContext* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para uma estrutura [CtxtHandle](sspi-handles.md) . Na primeira chamada para **AcceptSecurityContext (geral)**, esse ponteiro é **nulo**. Nas chamadas subsequentes, *phContext* é o identificador para o contexto parcialmente formado que foi retornado no parâmetro *phNewContext* pela primeira chamada.

</dd> <dt>

*pInput* \[ em, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) gerada por uma chamada de cliente para [**InitializeSecurityContext (geral)**](initializesecuritycontext--general.md) que contém o descritor de buffer de entrada.

Ao usar o SSP do Schannel, o primeiro buffer deve ser do tipo \_ token SECBUFFER e conter o token de segurança recebido do cliente. O segundo buffer deve ser do tipo SECBUFFER \_ vazio.

Ao usar os SSPs Negotiate, Kerberos ou NTLM, as informações de associação de canal podem ser especificadas passando uma estrutura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) do **tipo \_ \_ associações de canal SecBuffer** , além dos buffers gerados pela chamada para a função [**InitializeSecurityContext (geral)**](initializesecuritycontext--general.md) . As informações de associação de canal para o buffer de associação de canal podem ser obtidas chamando a função [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) no contexto Schannel que o cliente usou para autenticar.

</dd> <dt>

*fContextReq* \[ no\]
</dt> <dd>

Sinalizadores de bits que especificam os atributos exigidos pelo servidor para estabelecer o contexto. Os sinalizadores de bits podem ser combinados usando operações de bit-a-**ou** . Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                                                          | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASC_REQ_ALLOCATE_MEMORY"></span><span id="asc_req_allocate_memory"></span><dl> <dt>**memória de alocação do ASC \_ req \_ \_**</dt> </dl>                                                  | Digest e Schannel alocarão buffers de saída para você. Quando você terminar de usar os buffers de saída, libere-os chamando a função [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .<br/>                                                                                                                                                                                                                                                                                |
| <span id="ASC_REQ_ALLOW_MISSING_BINDINGS"></span><span id="asc_req_allow_missing_bindings"></span><dl> <dt>**o \_ ASC \_ req \_ permite \_ associações ausentes**</dt> </dl>                            | Indica que o resumo não requer associações de canal para canais internos e externos. Esse valor é usado para compatibilidade com versões anteriores quando o suporte para associação de canal de ponto de extremidade não é conhecido.<br/> Esse valor é mutuamente exclusivo com as **\_ associações de \_ proxy \_ do ASC req**.<br/> Esse valor tem suporte apenas pelo SSP de resumo.<br/> **Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Não há suporte para esse valor.<br/> <br/> |
| <span id="ASC_REQ_CONFIDENTIALITY"></span><span id="asc_req_confidentiality"></span><dl> <dt>**\_confidencialidade de req. asc \_**</dt> </dl>                                                   | Criptografar e descriptografar mensagens. <br/> O SSP de resumo dá suporte a este sinalizador somente para SASL.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="ASC_REQ_CONNECTION"></span><span id="asc_req_connection"></span><dl> <dt>**\_conexão de req. asc \_**</dt> </dl>                                                                  | O [*contexto de segurança*](../secgloss/s-gly.md) não tratará mensagens de formatação.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="ASC_REQ_DELEGATE"></span><span id="asc_req_delegate"></span><dl> <dt>**\_delegado de req ASC \_**</dt> </dl>                                                                        | O servidor tem permissão para representar o cliente. Válido para Kerberos. Ignore este sinalizador para [*delegação restrita*](../secgloss/c-gly.md).<br/>                                                                                                                                                                                                                                                             |
| <span id="ASC_REQ_EXTENDED_ERROR"></span><span id="asc_req_extended_error"></span><dl> <dt>**\_ \_ erro estendido de req. asc \_**</dt> </dl>                                                     | Quando ocorrerem erros, a parte remota será notificada.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ASC_REQ_HTTP__0x10000000_"></span><span id="asc_req_http__0x10000000_"></span><span id="ASC_REQ_HTTP__0X10000000_"></span><dl> <dt>**\_ \_ 0X10000000 (ASC req http)**</dt> </dl> | Use Digest para HTTP. Omita esse sinalizador para usar Digest como um mecanismo SASL.<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="ASC_REQ_INTEGRITY"></span><span id="asc_req_integrity"></span><dl> <dt>**\_integridade de req ASC \_**</dt> </dl>                                                                     | Assinar mensagens e verificar assinaturas.<br/> O Schannel não dá suporte a esse sinalizador.<br/>                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="ASC_REQ_MUTUAL_AUTH"></span><span id="asc_req_mutual_auth"></span><dl> <dt>**\_ \_ autenticação mútua de req. asc \_**</dt> </dl>                                                              | O cliente é necessário para fornecer um certificado a ser usado para autenticação de cliente.<br/> Esse sinalizador tem suporte apenas pelo Schannel.<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="ASC_REQ_PROXY_BINDINGS"></span><span id="asc_req_proxy_bindings"></span><dl> <dt>**\_associações de \_ proxy de req. asc \_**</dt> </dl>                                                     | Indica que o resumo requer Associação de canal.<br/> Esse valor é mutuamente exclusivo com o **ASC \_ req \_ permitir \_ \_ associações ausentes**.<br/> Esse valor tem suporte apenas pelo SSP de resumo.<br/> **Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Não há suporte para esse valor.<br/> <br/>                                                                                                                                         |
| <span id="ASC_REQ_REPLAY_DETECT"></span><span id="asc_req_replay_detect"></span><dl> <dt>**\_detecção de \_ Replay de req do ASC \_**</dt> </dl>                                                        | Detectar pacotes reproduzidos.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ASC_REQ_SEQUENCE_DETECT"></span><span id="asc_req_sequence_detect"></span><dl> <dt>**\_detecção de \_ sequência de req do ASC \_**</dt> </dl>                                                  | Detecte mensagens recebidas fora de sequência.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="ASC_REQ_STREAM"></span><span id="asc_req_stream"></span><dl> <dt>**\_fluxo de req. asc \_**</dt> </dl>                                                                              | Suporte a uma conexão orientada a fluxo.<br/> Esse sinalizador tem suporte apenas pelo Schannel.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |



 

Para possíveis sinalizadores de atributo e seus significados, consulte [requisitos de contexto](context-requirements.md). Os sinalizadores usados para esse parâmetro são prefixados com o ASC \_ req, por exemplo, o \_ delegado de req ASC \_ .

Os atributos solicitados podem não ter suporte do cliente. Para obter mais informações, consulte o parâmetro *pfContextAttr* .

</dd> <dt>

*TargetDataRep* \[ no\]
</dt> <dd>

A representação de dados, como ordenação de bytes, no destino. Esse parâmetro pode ser segurança \_ nativa \_ DREP ou segurança de \_ rede \_ DREP.

Esse parâmetro não é usado com SSPs Schannel ou Digest. Ao usar os SSPs Schannel ou Digest, especifique zero para esse parâmetro.

</dd> <dt>

*phNewContext* \[ entrada, saída, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura [CtxtHandle](sspi-handles.md) . Na primeira chamada para **AcceptSecurityContext (geral)**, esse ponteiro recebe o novo identificador de contexto. Nas chamadas subsequentes, *phNewContext* pode ser o mesmo que o identificador especificado no parâmetro *phContext* .

</dd> <dt>

*pOutput* \[ entrada, saída, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) que contém o descritor de buffer de saída. Esse buffer é enviado ao cliente para entrada em chamadas adicionais para [**InitializeSecurityContext (geral)**](initializesecuritycontext--general.md). Um buffer de saída pode ser gerado mesmo que a função retorne s \_ E \_ OK. Qualquer buffer gerado deve ser enviado de volta para o aplicativo cliente.

Ao usar Schannel, na saída, esse buffer recebe um token para o [*contexto de segurança*](../secgloss/s-gly.md). O token deve ser enviado ao cliente. A função também pode retornar um buffer do tipo SECBUFFER \_ extra. Além disso, o chamador deve passar um buffer do tipo **\_ alerta de SECBUFFER**. Na saída, se um alerta for gerado, esse buffer conterá informações sobre esse alerta e a função falhará.

</dd> <dt>

*pfContextAttr* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe um conjunto de sinalizadores de bits que indicam os atributos do contexto estabelecido. Para obter uma descrição dos vários atributos, consulte [requisitos de contexto](context-requirements.md). Os sinalizadores usados para esse parâmetro são prefixados com ASC \_ RET, por exemplo, o delegado de ASC \_ RET \_ .

Não verifique os atributos relacionados à segurança até que a chamada de função final seja retornada com êxito. Os sinalizadores de atributo não relacionados à segurança, como o \_ \_ sinalizador de memória alocada de ASC RET \_ , podem ser verificados antes do retorno final.

</dd> <dt>

*ptsTimeStamp* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura de [**carimbo de data/**](timestamp.md) hora que recebe o tempo de expiração do contexto. É recomendável que o [*pacote de segurança*](../secgloss/s-gly.md) sempre retorne esse valor na hora local.

Esse parâmetro é definido como um tempo máximo de constante. Não há tempo de expiração para as credenciais ou s de [*contexto de segurança*](../secgloss/s-gly.md)Digest ou ao usar o SSP de resumo.

Isso é opcional ao usar o SSP do Schannel. Quando a parte remota forneceu um certificado a ser usado para autenticação, esse parâmetro recebe o tempo de expiração para esse certificado. Se nenhum certificado tiver sido fornecido, um valor de tempo máximo será retornado.

> [!Note]  
> Até a última chamada do processo de autenticação, o tempo de expiração do contexto pode estar incorreto, pois mais informações serão fornecidas durante os estágios posteriores da negociação. Portanto, *ptsTimeStamp* deve ser **nulo** até a última chamada para a função.

 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função retorna um dos valores a seguir.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Código/valor de retorno</th><th>Description</th></tr></thead><tbody><tr class="odd"><td><dl> <dt><strong>SEC_E_BAD_BINDINGS</strong></dt> <dt>0x80090346L</dt> </dl></td><td>A função falhou. A política de associação de canal não foi satisfeita.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INCOMPLETE_MESSAGE</strong></dt> <dt>0x80090318L</dt> </dl></td><td>A função foi bem-sucedida. Os dados no buffer de entrada estão incompletos. O aplicativo deve ler dados adicionais do cliente e chamar [<strong>AcceptSecurityContext (General)</strong>] (AcceptSecurityContext--General.MD) novamente.<br/> Esse valor pode ser retornado ao usar o SSP do Schannel. Para obter mais informações sobre esse valor de retorno, consulte [<strong>AcceptSecurityContext (Schannel)</strong>] (AcceptSecurityContext--Schannel.MD).<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INSUFFICIENT_MEMORY</strong></dt> <dt>0x80090300L</dt> </dl></td><td>A função falhou. Não há memória suficiente disponível para concluir a ação solicitada.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INTERNAL_ERROR</strong></dt> <dt>0x80090304L</dt> </dl></td><td>A função falhou. Ocorreu um erro que não foi mapeado para um código de erro SSPI.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INVALID_HANDLE</strong></dt> <dt>0x80100003L</dt> </dl></td><td>A função falhou. O identificador passado para a função não é válido.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INVALID_TOKEN</strong></dt> <dt>0x80090308L</dt> </dl></td><td>A função falhou. O token passado para a função não é válido.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_LOGON_DENIED</strong></dt> <dt>0x8009030CL</dt> </dl></td><td>Falha no logon.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_NO_AUTHENTICATING_AUTHORITY</strong></dt> <dt>0x80090311L</dt> </dl></td><td>A função falhou. Nenhuma autoridade pode ser contatada para autenticação. Isso pode ser devido às seguintes condições:<br/><ul><li>O nome de domínio da parte de autenticação está incorreto.</li><li>O domínio não está disponível.</li><li>Falha na relação de confiança.</li></ul></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_NO_CREDENTIALS</strong></dt> <dt>0x8009030EL</dt> </dl></td><td>A função falhou. O identificador de credenciais especificado no parâmetro <em>phCredential</em> não é válido. Esse valor pode ser retornado ao usar o SSP Digest ou Schannel.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_OK</strong></dt> <dt>0x00000000l</dt> </dl></td><td>A função foi bem-sucedida. O [*contexto de segurança*](../secgloss/s-gly.md) recebido do cliente foi aceito. Se um token de saída foi gerado pela função, ele deve ser enviado para o processo do cliente.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_SECURITY_QOS_FAILED</strong></dt> <dt>0x80090332L</dt> </dl></td><td>A função falhou. Um sinalizador de atributo de contexto inválido foi especificado no parâmetro <em>fContextReq</em> . Esse valor pode ser retornado ao usar o SSP de resumo.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_UNSUPPORTED_FUNCTION</strong></dt> <dt>0x80090302L</dt> </dl></td><td>A função falhou. Um sinalizador de atributo de contexto que não é válido (ASC_REQ_DELEGATE ou ASC_REQ_PROMPT_FOR_CREDS) foi especificado no parâmetro <em>fContextReq</em> . Esse valor pode ser retornado ao usar o SSP do Schannel.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_COMPLETE_AND_CONTINUE</strong></dt> <dt>0x00090314L</dt> </dl></td><td>A função foi bem-sucedida. O servidor deve chamar [<strong>CompleteAuthToken</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-CompleteAuthToken) e passar o token de saída para o cliente. Em seguida, o servidor aguarda um token de retorno do cliente e, em seguida, faz outra chamada para [<strong>AcceptSecurityContext (geral)</strong>] (AcceptSecurityContext--General.MD). <br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_COMPLETE_NEEDED</strong></dt> <dt>0x00090313L</dt> </dl></td><td>A função foi bem-sucedida. O servidor deve concluir a compilação da mensagem do cliente e, em seguida, chamar a função [<strong>CompleteAuthToken</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-CompleteAuthToken).<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_CONTINUE_NEEDED</strong></dt> <dt>0x00090312L</dt> </dl></td><td>A função foi bem-sucedida. O servidor deve enviar o token de saída para o cliente e aguardar um token retornado. O token retornado deve ser passado em <em>pInput</em> para outra chamada para [<strong>AcceptSecurityContext (General)</strong>] (AcceptSecurityContext--General.MD).<br/></td></tr><tr class="even"><td><dl> <dt><strong>STATUS_LOGON_FAILURE</strong></dt> <dt>0xC000006DL</dt> </dl></td><td>A função falhou. A função [<strong>AcceptSecurityContext (General)</strong>] (AcceptSecurityContext--General.MD) foi chamada depois que o contexto especificado foi estabelecido. Esse valor pode ser retornado ao usar o SSP de resumo.<br/></td></tr></tbody></table>



 

## <a name="remarks"></a>Comentários

A função **AcceptSecurityContext (geral)** é a contraparte do servidor para a função [**InitializeSecurityContext (geral)**](initializesecuritycontext--general.md) .

Quando o servidor recebe uma solicitação de um cliente, o servidor usa o parâmetro *fContextReq* para especificar o que é necessário para a sessão. Dessa maneira, um servidor pode especificar que os clientes devem ser capazes de usar uma sessão confidencial ou com verificação de [*integridade*](../secgloss/i-gly.md), e pode rejeitar clientes que não podem atender a essa demanda. Como alternativa, um servidor pode não exigir nada e tudo o que o cliente pode fornecer ou exigir é retornado no parâmetro *pfContextAttr* .

Para um pacote que dá suporte à autenticação de vários trechos, como a autenticação mútua, a sequência de chamada é a seguinte:

1.  O cliente transmite um token para o servidor.
2.  O servidor chama **AcceptSecurityContext (geral)** na primeira vez, o que gera um token de resposta que é enviado para o cliente.
3.  O cliente recebe o token e o passa para [**InitializeSecurityContext (geral)**](initializesecuritycontext--general.md). Se **InitializeSecurityContext (geral)** retornar s \_ e \_ OK, a autenticação mútua foi concluída e uma sessão segura pode começar. Se **InitializeSecurityContext (geral)** retornar um código de erro, a negociação de autenticação mútua terminará. Caso contrário, o token de segurança retornado por **InitializeSecurityContext (geral)** é enviado ao cliente e as etapas 2 e 3 são repetidas.

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

[**InitializeSecurityContext (geral)**](initializesecuritycontext--general.md)
</dt> </dl>

 

 
