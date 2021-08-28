---
description: Permite que o componente de servidor de um aplicativo de transporte estabeleça um contexto de segurança entre o servidor e um cliente remoto que está usando Digest.
ms.assetid: 017683e3-b21a-4e97-9232-582ac7dbd5b2
title: Função AcceptSecurityContext (Digest) (Sspi.h)
ms.topic: article
ms.date: 07/25/2019
ms.openlocfilehash: ec6ad11e754124f56f5852b4e0b0a0347f1bb099
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628708"
---
# <a name="acceptsecuritycontext-digest-function"></a>Função AcceptSecurityContext (Digest)

A **função AcceptSecurityContext (Digest)** permite que o componente [](../secgloss/s-gly.md) de servidor de um aplicativo de transporte estabeleça um contexto de segurança entre o servidor e um cliente remoto. O cliente remoto usa a [**função InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) para iniciar o processo de estabelecimento de um contexto de segurança. O servidor pode exigir um ou mais tokens de resposta do cliente remoto para concluir o estabelecimento do contexto de segurança.

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

*phCredential* \[ in, opcional\]
</dt> <dd>

Um handle para as credenciais do servidor. O servidor chama [**a função AcquireCredentialsHandle (Digest)**](acquirecredentialshandle--digest.md) com o sinalizador SECPKG \_ CRED INBOUND ou SECPKG CRED BOTH definido para recuperar esse \_ \_ \_ identificador.

</dd> <dt>

*phContext* \[ in, out, opcional\]
</dt> <dd>

Um ponteiro para uma [estrutura CtxtHandle.](sspi-handles.md) Na primeira chamada para **AcceptSecurityContext (Digest),** esse ponteiro é **NULL.** Em chamadas subsequentes, *phContext* é o handle para o contexto parcialmente formado que foi retornado no parâmetro *phNewContext* pela primeira chamada.

</dd> <dt>

*pInput* \[ in, opcional\]
</dt> <dd>

Um ponteiro para uma [**estrutura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) gerada por uma chamada do cliente para [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) que contém o descritor de buffer de entrada.

A tabela a seguir mostra a configuração de buffer para Digest HTTP. O primeiro buffer deve ser do tipo **SECBUFFER \_ TOKEN** e o restante deve ser do tipo **SECBUFFER \_ PKG \_ PARAMS**. O SASL requer apenas o buffer zero.



| Tipo \# de buffer/buffer                                                                                                                                                                                                 | Significado                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> <dt> **TOKEN \_ SECBUFFER**</dt> </dl>                                        | Vazio para a primeira chamada e a resposta de desafio recebida do cliente para a segunda chamada.<br/>                                                             |
| <span id="1"></span><dl> <dt>**1**</dt> <dt> **SECBUFFER \_ PKG \_ PARAMS**</dt> </dl>                                  | Método. Os caracteres são formato de linha de transmissão da linha de solicitação. Caracteres de byte único ASCII dos EUA.<br/>                                                                |
| <span id="2"></span><dl> <dt>**2**</dt> <dt> **\_ \_ PARAMS DE PKG DO SECBUFFER**</dt> </dl>                                  | Reservado.<br/>                                                                                                                                                     |
| <span id="3"></span><dl> <dt>**3**</dt> <dt> **\_ \_ PARAMS DE PKG DO SECBUFFER**</dt> </dl>                                  | HEntity. Representação hexadecimal de H(entity-body). Caracteres de byte único ASCII dos EUA.<br/>                                                                       |
| <span id="4"></span><dl> <dt>**4**</dt> <dt> **\_ \_ PARAMS DE PKG DO SECBUFFER**</dt> </dl>                                  | Reino. Cadeia de caracteres de realm para o desafio. Cadeia de caracteres Unicode que deve ser representável no ASCII dos EUA.<br/>                                                                 |
| <span id="5"></span><dl> <dt>**5**</dt> <dt> **SECBUFFER \_ CHANNEL \_ BINDINGS** \| **SECBUFFER \_ READONLY**</dt> </dl> | Contém o valor do token de associação de canal.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para esse valor.<br/> |



 

</dd> <dt>

*fContextReq* \[ Em\]
</dt> <dd>

Sinalizadores de bits que especificam os atributos exigidos pelo servidor para estabelecer o contexto. Os sinalizadores de bit podem ser combinados usando operações **OR** bit a bit. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                                                          | Significado                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASC_REQ_ALLOCATE_MEMORY"></span><span id="asc_req_allocate_memory"></span><dl> <dt>**ASC \_ REQ \_ ALLOCATE \_ MEMORY**</dt> </dl>                                                  | Digest aloca buffers de saída para você. Quando terminar de usar os buffers de saída, livre-os chamando a [**função FreeContextBuffer.**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)<br/>                                                                                                                                                                                                                                      |
| <span id="ASC_REQ_ALLOW_MISSING_BINDINGS"></span><span id="asc_req_allow_missing_bindings"></span><dl> <dt>**ASC \_ REQ \_ \_ PERMITEM \_ VINCULAÇÕES AUSENTES**</dt> </dl>                            | Indica que Digest não requer vinculações de canal para canais internos e externos. Esse valor é usado para compatibilidade com backward quando o suporte para associação de canal de ponto de extremidade não é conhecido.<br/> Esse valor é mutuamente exclusivo com **ASC \_ REQ \_ PROXY \_ BINDINGS**.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para esse valor.<br/> <br/> |
| <span id="ASC_REQ_CONFIDENTIALITY"></span><span id="asc_req_confidentiality"></span><dl> <dt>**CONFIDENCIALIDADE DO ASC \_ REQ \_**</dt> </dl>                                                   | Criptografar e descriptografar mensagens. <br/> O SSP digest dá suporte a esse sinalizador somente para SASL.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="ASC_REQ_PROXY_BINDINGS"></span><span id="asc_req_proxy_bindings"></span><dl> <dt>**ASC \_ REQ \_ PROXY \_ BINDINGS**</dt> </dl>                                                     | Indica que Digest requer associação de canal.<br/> Esse valor é mutuamente exclusivo com **ASC \_ REQ \_ ALLOW MISSING \_ \_ BINDINGS**.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para esse valor.<br/> <br/>                                                                                                                                         |
| <span id="ASC_REQ_CONNECTION"></span><span id="asc_req_connection"></span><dl> <dt>**CONEXÃO ASC \_ REQ \_**</dt> </dl>                                                                  | O [*contexto de segurança*](../secgloss/s-gly.md) não manipulará mensagens de formatação.<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="ASC_REQ_EXTENDED_ERROR"></span><span id="asc_req_extended_error"></span><dl> <dt>**ERRO ESTENDIDO DO ASC \_ REQ \_ \_**</dt> </dl>                                                     | Quando ocorrerem erros, a parte remota será notificada.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <span id="ASC_REQ_HTTP__0x10000000_"></span><span id="asc_req_http__0x10000000_"></span><span id="ASC_REQ_HTTP__0X10000000_"></span><dl> <dt>**HTTP DO ASC \_ REQ \_ (0x10000000)**</dt> </dl> | Use Digest para HTTP. Omita esse sinalizador para usar Digest como um mecanismo SASL.<br/>                                                                                                                                                                                                                                                                                                                                          |
| <span id="ASC_REQ_INTEGRITY"></span><span id="asc_req_integrity"></span><dl> <dt>**INTEGRIDADE DA \_ ASC REQ \_**</dt> </dl>                                                                     | Assinar mensagens e verificar assinaturas.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="ASC_REQ_REPLAY_DETECT"></span><span id="asc_req_replay_detect"></span><dl> <dt>**ASC \_ REQ \_ REPLAY \_ DETECT**</dt> </dl>                                                        | Detectar pacotes replayed.<br/>                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="ASC_REQ_SEQUENCE_DETECT"></span><span id="asc_req_sequence_detect"></span><dl> <dt>**ASC \_ REQ \_ SEQUENCE \_ DETECT**</dt> </dl>                                                  | Detectar mensagens recebidas fora de sequência.<br/>                                                                                                                                                                                                                                                                                                                                                                        |



 

Para possíveis sinalizadores de atributo e seus significados, consulte [Requisitos de contexto.](context-requirements.md) Sinalizadores usados para esse parâmetro são prefixados com ASC \_ REQ, por exemplo, ASC \_ REQ \_ DELEGATE.

Os atributos solicitados podem não ser suportados pelo cliente. Para obter mais informações, consulte o *parâmetro pfContextAttr.*

</dd> <dt>

*TargetDataRep* \[ Em\]
</dt> <dd>

A representação de dados, como ordenação de byte, no destino. Esse parâmetro pode ser SECURITY \_ NATIVE \_ DREP ou SECURITY \_ NETWORK \_ DREP.

Esse parâmetro não é usado com Digest SSP. Ao usar o Digest SSP, especifique zero para esse parâmetro.

</dd> <dt>

*phNewContext* \[ in, out, opcional\]
</dt> <dd>

Um ponteiro para uma [estrutura CtxtHandle.](sspi-handles.md) Na primeira chamada para **AcceptSecurityContext (Digest),** esse ponteiro recebe o novo indicador de contexto. Em chamadas subsequentes, *phNewContext* pode ser o mesmo que o handle especificado no *parâmetro phContext.*

</dd> <dt>

*pOutput* \[ in, out, opcional\]
</dt> <dd>

Um ponteiro para uma [**estrutura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) que contém o descritor de buffer de saída. Esse buffer é enviado ao cliente para entrada em chamadas adicionais para [**InitializeSecurityContext (Digest).**](initializesecuritycontext--digest.md) Um buffer de saída pode ser gerado mesmo que a função retorne SEC \_ E \_ OK. Qualquer buffer gerado deve ser enviado de volta para o aplicativo cliente.

</dd> <dt>

*pfContextAttr* \[ out\]
</dt> <dd>

Um ponteiro para uma variável que recebe um conjunto de sinalizadores de bits que indicam os atributos do contexto estabelecido. Para ver uma descrição dos vários atributos, confira [Requisitos de contexto.](context-requirements.md) Os sinalizadores usados para esse parâmetro são prefixados com ASC \_ RET, por exemplo, ASC \_ RET \_ DELEGATE.

Não verifique se há atributos relacionados à segurança até que a chamada de função final retorne com êxito. Sinalizadores de atributo não relacionados à segurança, como o sinalizador ASC \_ RET ALLOCATED MEMORY, podem ser verificados \_ antes do retorno \_ final.

</dd> <dt>

*ptsTimeStamp* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura de [**carimbo de data/**](timestamp.md) hora que recebe o tempo de expiração do contexto. É recomendável que o [*pacote de segurança*](../secgloss/s-gly.md) sempre retorne esse valor na hora local.

Esse parâmetro é definido como um tempo máximo de constante. Não há tempo de expiração para as credenciais ou s de [*contexto de segurança*](../secgloss/s-gly.md)Digest ou ao usar o SSP de resumo.

> [!Note]  
> Até a última chamada do processo de autenticação, o tempo de expiração do contexto pode estar incorreto, pois mais informações serão fornecidas durante os estágios posteriores da negociação. Portanto, *ptsTimeStamp* deve ser **nulo** até a última chamada para a função.

 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa função retorna um dos valores a seguir.



<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th>Código/valor de retorno</th><th>Descrição</th></tr></thead><tbody><tr class="odd"><td><dl> <dt><strong>SEC_E_INSUFFICIENT_MEMORY</strong></dt> <dt>0x80090300L</dt> </dl></td><td>A função falhou. Não há memória suficiente disponível para concluir a ação solicitada.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INTERNAL_ERROR</strong></dt> <dt>0x80090304L</dt> </dl></td><td>A função falhou. Ocorreu um erro que não foi mapeado para um código de erro SSPI.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INVALID_HANDLE</strong></dt> <dt>0x80100003L</dt> </dl></td><td>A função falhou. O identificador passado para a função não é válido.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INVALID_TOKEN</strong></dt> <dt>0x80090308L</dt> </dl></td><td>A função falhou. O token passado para a função não é válido.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_LOGON_DENIED</strong></dt> <dt>0x8009030CL</dt> </dl></td><td>Falha no logon.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_NO_AUTHENTICATING_AUTHORITY</strong></dt> <dt>0x80090311L</dt> </dl></td><td>A função falhou. Nenhuma autoridade pode ser contatada para autenticação. Isso pode ser devido às seguintes condições:<br/><ul><li>O nome de domínio da parte de autenticação está incorreto.</li><li>O domínio não está disponível.</li><li>Falha na relação de confiança.</li></ul></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_NO_CREDENTIALS</strong></dt> <dt>0x8009030EL</dt> </dl></td><td>A função falhou. O identificador de credenciais especificado no parâmetro <em>phCredential</em> não é válido.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_OK</strong></dt> <dt>0x00000000l</dt> </dl></td><td>A função foi bem-sucedida. O [*contexto de segurança*](../secgloss/s-gly.md) recebido do cliente foi aceito. Se um token de saída foi gerado pela função, ele deve ser enviado para o processo do cliente.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_SECURITY_QOS_FAILED</strong></dt> <dt>0x80090332L</dt> </dl></td><td>A função falhou. Um sinalizador de atributo de contexto inválido foi especificado no parâmetro <em>fContextReq</em> .<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_COMPLETE_AND_CONTINUE</strong></dt> <dt>0x00090314L</dt> </dl></td><td>A função foi bem-sucedida. O servidor deve chamar [<strong>CompleteAuthToken</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-CompleteAuthToken) e passar o token de saída para o cliente. Em seguida, o servidor aguarda um token de retorno do cliente e, em seguida, faz outra chamada para [<strong>AcceptSecurityContext (Digest)</strong>] (AcceptSecurityContext--Digest.MD).<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_COMPLETE_NEEDED</strong></dt> <dt>0x00090313L</dt> </dl></td><td>A função foi bem-sucedida. O servidor deve concluir a compilação da mensagem do cliente e, em seguida, chamar a função [<strong>CompleteAuthToken</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-CompleteAuthToken).<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_CONTINUE_NEEDED</strong></dt> <dt>0x00090312L</dt> </dl></td><td>A função foi bem-sucedida. O servidor deve enviar o token de saída para o cliente e aguardar um token retornado. O token retornado deve ser passado em <em>pInput</em> para outra chamada para [<strong>AcceptSecurityContext (Digest)</strong>] (AcceptSecurityContext--Digest.MD).<br/></td></tr><tr class="odd"><td><dl> <dt><strong>STATUS_LOGON_FAILURE</strong></dt> <dt>0xC000006DL</dt> </dl></td><td>A função falhou. A função [<strong>AcceptSecurityContext (Digest)</strong>] (AcceptSecurityContext--Digest.MD) foi chamada depois que o contexto especificado foi estabelecido.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_BAD_BINDINGS</strong></dt> <dt>0x80090346L</dt> </dl></td><td>A função falhou. A política de associação de canal não foi satisfeita.<br/></td></tr></tbody></table>



 

## <a name="remarks"></a>Comentários

A função **AcceptSecurityContext (Digest)** é a contraparte do servidor para a função [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) .

Quando o servidor recebe uma solicitação de um cliente, o servidor usa o parâmetro *fContextReq* para especificar o que é necessário para a sessão. Dessa maneira, um servidor pode especificar que os clientes devem ser capazes de usar uma sessão confidencial ou com verificação de [*integridade*](../secgloss/i-gly.md), e pode rejeitar clientes que não podem atender a essa demanda. Como alternativa, um servidor pode não exigir nada e tudo o que o cliente pode fornecer ou exigir é retornado no parâmetro *pfContextAttr* .

Para um pacote que dá suporte à autenticação de vários trechos, como a autenticação mútua, a sequência de chamada é a seguinte:

1.  O cliente transmite um token para o servidor.
2.  O servidor chama **AcceptSecurityContext (Digest)** pela primeira vez, o que gera um token de resposta que é enviado para o cliente.
3.  O cliente recebe o token e o passa para [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md). Se **InitializeSecurityContext (Digest)** retornar s \_ e \_ OK, a autenticação mútua foi concluída e uma sessão segura pode começar. Se **InitializeSecurityContext (Digest)** retornar um código de erro, a negociação de autenticação mútua terminará. Caso contrário, o token de segurança retornado por **InitializeSecurityContext (Digest)** é enviado ao cliente e as etapas 2 e 3 são repetidas.

Os parâmetros *fContextReq* e *pfContextAttr* são bitmasks que representam vários atributos de contexto. Para obter uma descrição dos vários atributos, consulte [requisitos de contexto](context-requirements.md).

> [!Note]  
> O parâmetro *pfContextAttr* é válido em qualquer retorno bem-sucedido, mas somente no retorno bem-sucedido final, você deve examinar os sinalizadores referentes aos aspectos de segurança do contexto. Os retornos intermediários podem definir, por exemplo, o \_ \_ sinalizador de memória alocada do ISC RET \_ .

 

O chamador é responsável por determinar se os atributos de contexto final são suficientes. Se, por exemplo, a confidencialidade (criptografia) tiver sido solicitada, mas não puder ser estabelecida, alguns aplicativos poderão optar por desligar a conexão imediatamente. Se o [*contexto de segurança*](../secgloss/s-gly.md) não puder ser estabelecido, o servidor deverá liberar o contexto parcialmente criado chamando a função [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) . Para obter informações sobre quando chamar a função **DeleteSecurityContext** , consulte **DeleteSecurityContext**.

Depois que o [*contexto de segurança*](../secgloss/s-gly.md) tiver sido estabelecido, o aplicativo de servidor poderá usar a função [**QuerySecurityContextToken**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) para recuperar um identificador para a conta de usuário para a qual o certificado de cliente foi mapeado. Além disso, o servidor pode usar a função [**ImpersonateSecurityContext**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) para representar o usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                   |
| Cabeçalho<br/>                   | <dl> <dt>SSPI. h (incluir Security. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**InitializeSecurityContext (resumo)**](initializesecuritycontext--digest.md)
</dt> </dl>

 

 
