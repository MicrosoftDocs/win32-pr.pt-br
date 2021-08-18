---
description: Inicia o contexto de [](../secgloss/s-gly.md) segurança de saída do lado do cliente de um handle de credencial usando a delegação restrita de Kerberos [](../secgloss/s-gly.md).
ms.assetid: b5c968dc-9343-44ed-acbc-a89c58c14e4a
title: Função InitializeSecurityContext (Kerberos) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: f2a88fd930e58be418afa9d508adf9cda73912a8c0c5ea6731c06af5ec41a997
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482596"
---
# <a name="initializesecuritycontext-kerberos-function"></a>Função InitializeSecurityContext (Kerberos)

A **função InitializeSecurityContext (Kerberos)** inicia o contexto de segurança de saída do lado do cliente [*de*](../secgloss/s-gly.md) um handle de credencial. A função é usada para criar um contexto [*de segurança*](../secgloss/s-gly.md) entre o aplicativo cliente e um par remoto. **InitializeSecurityContext (Kerberos)** retorna um token que o cliente deve passar para o par remoto, que o par, por sua vez, envia para a implementação de segurança local por meio da chamada [**AcceptSecurityContext (Kerberos).**](acceptsecuritycontext--kerberos.md) O token gerado deve ser considerado opaco por todos os chamadores.

Normalmente, a **função InitializeSecurityContext (Kerberos)** é chamada em um loop até que um contexto de [*segurança suficiente*](../secgloss/s-gly.md) seja estabelecido.

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS SEC_Entry InitializeSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_        SEC_CHAR       *pszTargetName,
  _In_        ULONG          fContextReq,
  _In_        ULONG          Reserved1,
  _In_        ULONG          TargetDataRep,
  _In_opt_    PSecBufferDesc pInput,
  _In_        ULONG          Reserved2,
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

Um identificador para as credenciais retornadas [**por AcquireCredentialsHandle (Kerberos)**](acquirecredentialshandle--kerberos.md). Esse handle é usado para criar o contexto [*de segurança*](../secgloss/s-gly.md). A **função InitializeSecurityContext (Kerberos)** requer pelo menos credenciais de SAÍDA.

</dd> <dt>

*phContext* \[ in, opcional\]
</dt> <dd>

Um ponteiro para uma [estrutura CtxtHandle.](sspi-handles.md) Na primeira chamada para **InitializeSecurityContext (Kerberos),** esse ponteiro é **NULL.** Na segunda chamada, esse parâmetro é um ponteiro para o ponteiro para o contexto parcialmente formado retornado no parâmetro *phNewContext* pela primeira chamada.

</dd> <dt>

*pszTargetName* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que indica o SPN (nome da entidade de serviço) ou o contexto [*de*](../secgloss/s-gly.md) segurança do servidor de destino.

Use um nome de destino totalmente qualificado porque não há suporte para nomes curtos entre florestas.

</dd> <dt>

*fContextReq* \[ Em\]
</dt> <dd>

Sinalizadores de bits que indicam solicitações para o contexto. Nem todos os pacotes podem dar suporte a todos os requisitos. Sinalizadores usados para esse parâmetro são prefixados com ISC \_ REQ \_ , por exemplo, ISC \_ REQ \_ DELEGATE. Esse parâmetro pode ser um ou mais dos sinalizadores de atributos a seguir.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Valor</th><th>Significado</th></tr></thead><tbody><tr class="odd"><td><span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl> <dt><strong>ISC_REQ_ALLOCATE_MEMORY</strong></dt> </dl></td><td>O [*pacote de segurança*](../secgloss/s-gly.md) aloca buffers de saída para você. Quando terminar de usar os buffers de saída, livre-os chamando a função [<strong>FreeContextBuffer</strong>](/windows/win32/api/sspi/nf-sspi-freecontextbuffer).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_CONFIDENTIALITY"></span><span id="isc_req_confidentiality"></span><dl> <dt><strong>ISC_REQ_CONFIDENTIALITY</strong></dt> </dl></td><td>Criptografe mensagens usando a função [<strong>EncryptMessage</strong>](encryptmessage--general.md).<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl> <dt><strong>ISC_REQ_CONNECTION</strong></dt> </dl></td><td>O [*contexto de segurança*](../secgloss/s-gly.md) não manipulará mensagens de formatação. Esse valor é o padrão.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_DELEGATE"></span><span id="isc_req_delegate"></span><dl> <dt><strong>ISC_REQ_DELEGATE</strong></dt> </dl></td><td>O servidor pode usar o contexto para autenticar em outros servidores como o cliente. O ISC_REQ_MUTUAL_AUTH sinalizador deve ser definido para que esse sinalizador funcione. Válido para Kerberos. Ignore esse sinalizador para [*delegação restrita.*](../secgloss/c-gly.md)<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl> <dt><strong>ISC_REQ_EXTENDED_ERROR</strong></dt> </dl></td><td>Quando ocorrerem erros, a parte remota será notificada.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_INTEGRITY"></span><span id="isc_req_integrity"></span><dl> <dt><strong>ISC_REQ_INTEGRITY</strong></dt> </dl></td><td>Assine mensagens e verifique assinaturas usando as funções [<strong>EncryptMessage</strong>](encryptmessage--general.md) e [<strong>MakeSignature</strong>](makesignature.md).<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl> <dt><strong>ISC_REQ_MUTUAL_AUTH</strong></dt> </dl></td><td>A política de autenticação mútua do serviço será atendida.<br/><blockquote>[!Caution]<br />
Isso não significa necessariamente que a autenticação mútua seja executada, apenas que a política de autenticação do serviço é atendida. Para garantir que a autenticação mútua seja executada, chame a função [<strong>QueryContextAttributes (Kerberos)</strong>](querycontextattributes--kerberos.md).</blockquote><br/></td></tr><tr class="even"><td><span id="ISC_REQ_NO_INTEGRITY"></span><span id="isc_req_no_integrity"></span><dl> <dt><strong>ISC_REQ_NO_INTEGRITY</strong></dt> </dl></td><td>Se esse sinalizador for definido, o <strong>sinalizador ISC_REQ_INTEGRITY</strong> será ignorado.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_REPLAY_DETECT"></span><span id="isc_req_replay_detect"></span><dl> <dt><strong>ISC_REQ_REPLAY_DETECT</strong></dt> </dl></td><td>Detecte mensagens reprodução codificadas usando as funções [<strong>EncryptMessage</strong>](encryptmessage--general.md) ou [<strong>MakeSignature</strong>](makesignature.md).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl> <dt><strong>ISC_REQ_SEQUENCE_DETECT</strong></dt> </dl></td><td>Detectar mensagens recebidas fora de sequência.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl> <dt><strong>ISC_REQ_STREAM</strong></dt> </dl></td><td>Dar suporte a uma conexão orientada a fluxo.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_USE_SESSION_KEY"></span><span id="isc_req_use_session_key"></span><dl> <dt><strong>ISC_REQ_USE_SESSION_KEY</strong></dt> </dl></td><td>Uma nova [*chave de sessão*](../secgloss/s-gly.md) deve ser negociada.<br/></td></tr></tbody></table>



 

Os atributos solicitados podem não ser suportados pelo cliente. Para obter mais informações, consulte o *parâmetro pfContextAttr.*

Para saber mais sobre os vários atributos, confira [Requisitos de contexto.](context-requirements.md)

</dd> <dt>

*Reservado1* \[ Em\]
</dt> <dd>

Esse parâmetro é reservado e deve ser definido como zero.

</dd> <dt>

*TargetDataRep* \[ Em\]
</dt> <dd>

A representação de dados, como ordenação de byte, no destino. Esse parâmetro pode ser SECURITY \_ NATIVE \_ DREP ou SECURITY \_ NETWORK \_ DREP.

</dd> <dt>

*pInput* \[ in, opcional\]
</dt> <dd>

Um ponteiro para uma [**estrutura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) que contém ponteiros para os buffers fornecidos como entrada para o pacote. A menos que o contexto do cliente tenha sido iniciado pelo servidor, o valor desse parâmetro deve ser **NULL** na primeira chamada para a função. Em chamadas subsequentes para a função ou quando o contexto do cliente foi iniciado pelo servidor, o valor desse parâmetro é um ponteiro para um buffer alocado com memória suficiente para manter o token retornado pelo computador remoto.

</dd> <dt>

*Reservado2* \[ Em\]
</dt> <dd>

Esse parâmetro é reservado e deve ser definido como zero.

</dd> <dt>

*phNewContext* \[ in, out, opcional\]
</dt> <dd>

Um ponteiro para uma [estrutura CtxtHandle.](sspi-handles.md) Na primeira chamada para **InitializeSecurityContext (Kerberos),** esse ponteiro recebe o novo indicador de contexto. Na segunda chamada, *phNewContext* pode ser o mesmo que o handle especificado no *parâmetro phContext.*

</dd> <dt>

*pOutput* \[ in, out, opcional\]
</dt> <dd>

Um ponteiro para uma [**estrutura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) que contém ponteiros para a estrutura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que recebe os dados de saída. Se um buffer tiver sido digitado como SEC \_ READWRITE na entrada, ele estará lá na saída. O sistema alocará um buffer para o token de segurança se solicitado (por meio de ISC \_ REQ ALLOCATE MEMORY) e preencherá o endereço no descritor de buffer para o \_ \_ token de segurança.

</dd> <dt>

*pfContextAttr* \[ out\]
</dt> <dd>

Um ponteiro para uma variável para receber um conjunto de sinalizadores de bits que indicam os [*atributos*](../secgloss/a-gly.md#_security_attribute_gly) do contexto estabelecido. Para ver uma descrição dos vários atributos, confira [Requisitos de contexto.](context-requirements.md)

Sinalizadores usados para esse parâmetro são prefixados com ISC \_ RET, como ISC \_ RET \_ DELEGATE. Para ver uma lista de valores válidos, consulte o *parâmetro fContextReq.*

Não verifique se há atributos relacionados à segurança até que a chamada de função final retorne com êxito. Sinalizadores de atributo que não estão relacionados à segurança, como o sinalizador ASC \_ RET ALLOCATED MEMORY, podem ser verificados \_ antes do retorno \_ final.

> [!Note]  
> Atributos de contexto específicos podem mudar durante a negociação com um par remoto.

 

</dd> <dt>

*ptsExpiry* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma [**estrutura TimeStamp**](timestamp.md) que recebe a hora de expiração do contexto. Recomendamos que o [*pacote de segurança*](../secgloss/s-gly.md) sempre retorne esse valor no horário local. Como esse parâmetro é opcional, **NULL** deve ser passado para clientes de curta duração.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, a função retornará um dos códigos de êxito a seguir.



| Código de retorno                                                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ OK**</dt> </dl>                      | O [*contexto de segurança*](../secgloss/s-gly.md) foi inicializado com êxito. Não há necessidade de outra [**chamada InitializeSecurityContext (Kerberos).**](initializesecuritycontext--kerberos.md) Se a função retornar um token de saída, ou seja, se o TOKEN SECBUFFER em pOutput for de comprimento diferente de zero, esse token deverá ser \_ enviado para o servidor. <br/> |
| <dl> <dt>**SEC \_ I \_ COMPLETE \_ AND \_ CONTINUE**</dt> </dl> | O cliente deve chamar [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) e, em seguida, passar a saída para o servidor. Em seguida, o cliente aguarda um token retornado e passa-o, em outra chamada, para [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md).<br/>                                                                                                                                  |
| <dl> <dt>**SE EU \_ \_ CONCLUIR \_ NECESSÁRIO**</dt> </dl>        | O cliente deve concluir a criação da mensagem e, em seguida, chamar a [**função CompleteAuthToken.**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)<br/>                                                                                                                                                                                                                                                                                           |
| <dl> <dt>**SE EU \_ \_ CONTINUAR \_ NECESSÁRIO**</dt> </dl>        | O cliente deve enviar o token de saída para o servidor e aguardar um token de retorno. O token retornado é passado em outra chamada para [**InitializeSecurityContext (Kerberos).**](initializesecuritycontext--kerberos.md) O token de saída pode estar vazio.<br/>                                                                                                                                                       |
| <dl> <dt>**SEG \_ I \_ CREDENCIAIS \_ INCOMPLETAS**</dt> </dl> | Use com schannel. O servidor solicitou autenticação de cliente e as credenciais fornecidas não incluem um certificado ou o certificado não foi emitido por uma AC (autoridade de certificação) confiável pelo servidor. Para obter mais informações, consulte Comentários.<br/>                                                |



 

Se a função falhar, a função retornará um dos códigos de erro a seguir.



| Código de retorno                                                                                                          | Descrição                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ E \_ MEMÓRIA \_ INSUFICIENTE**</dt> </dl>          | Não há memória suficiente disponível para concluir a ação solicitada.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**ERRO \_ INTERNO DO SEC E \_ \_**</dt> </dl>               | Ocorreu um erro que não mapeou para um código de erro SSPI.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>**SEC \_ E \_ INVALID \_ HANDLE**</dt> </dl>               | O alça passado para a função não é válido.<br/>                                                                                                                                                                                                                                          |
| <dl> <dt>**SEC \_ E \_ TOKEN \_ INVÁLIDO**</dt> </dl>                | O erro ocorre devido a um token de entrada [*malformado,*](../secgloss/s-gly.md)como um token corrompido em trânsito, um token de tamanho incorreto ou um token passado para a delegação restrita incorreta. Passar um token para o pacote errado poderá acontecer se o cliente e o servidor não negociarem a [*delegação restrita adequada.*](../secgloss/s-gly.md)<br/> |
| <dl> <dt>**LOGON \_ DO SEC E \_ \_ NEGADO**</dt> </dl>                 | Falha no logon.<br/>                                                                                                                                                                                                                                                                        |
| <dl> <dt>**SEC \_ E \_ NO \_ AUTHENTICATING \_ AUTHORITY**</dt> </dl> | Nenhuma autoridade pode ser contata para autenticação. O nome de domínio da parte de autenticação pode estar errado, o domínio pode estar inacessível ou pode ter sido uma falha de relação de confiança.<br/>                                                                                  |
| <dl> <dt>**SEC \_ E \_ NO \_ CREDENTIALS**</dt> </dl>               | Nenhuma credencial está disponível na [*delegação restrita*](../secgloss/s-gly.md).<br/>                                                                                                                                                  |
| <dl> <dt>**SEC \_ E \_ TARGET \_ UNKNOWN**</dt> </dl>               | O destino não foi reconhecido.<br/>                                                                                                                                                                                                                                                           |
| <dl> <dt>**FUNÇÃO \_ SEC E SEM \_ \_ SUPORTE**</dt> </dl>         | Um sinalizador de atributo de contexto que não é válido (ISC REQ DELEGATE ou ISC REQ PROMPT FOR CREDS) foi especificado no \_ \_ parâmetro \_ \_ \_ \_ *fContextReq.*<br/>                                                                                                                                            |
| <dl> <dt>**SEC \_ E ENTIDADE DE ENTIDADE \_ \_ ERRADA**</dt> </dl>              | A entidade de serviço que recebeu a solicitação de autenticação não é a mesma que a passada para o *parâmetro pszTargetName.* Isso indica uma falha na autenticação mútua.<br/>                                                                                                          |



 

## <a name="remarks"></a>Comentários

O chamador é responsável por determinar se os atributos de contexto finais são suficientes. Se, por exemplo, a confidencialidade tiver sido solicitada, mas não puder ser estabelecida, alguns aplicativos poderão optar por desligar a conexão imediatamente.

Se os atributos do contexto [*de segurança não*](../secgloss/s-gly.md) são suficientes, o cliente deve liberar o contexto parcialmente criado chamando a função [**DeleteSecurityContext.**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)

A **função InitializeSecurityContext (Kerberos)** é usada por um cliente para inicializar um contexto de saída.

Para um contexto de segurança [*de duas fases,*](../secgloss/s-gly.md)a sequência de chamada é a seguinte:

1.  O cliente chama a função com *phContext* definido como **NULL** e preenche o descritor de buffer com a mensagem de entrada.
2.  O [*pacote de*](../secgloss/s-gly.md) segurança examina os parâmetros e constrói um token opaco, colocando-o no elemento TOKEN na matriz de buffer. Se o *parâmetro fContextReq* incluir o sinalizador ISC \_ REQ ALLOCATE MEMORY, o pacote de segurança alocará a memória e retornará o ponteiro no \_ \_ elemento TOKEN. [](../secgloss/s-gly.md)
3.  O cliente envia o token retornado no buffer *pOutput* para o servidor de destino. Em seguida, o servidor passa o token como um argumento de entrada em uma chamada para a função [**AcceptSecurityContext (Kerberos).**](acceptsecuritycontext--kerberos.md)
4.  [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) pode retornar um token, que o servidor envia ao cliente para uma segunda chamada para **InitializeSecurityContext (Kerberos)** se a primeira chamada retornar SEC \_ I CONTINUE \_ \_ NEEDED.

Para contextos de [*segurança de várias*](../secgloss/s-gly.md)etapas, como autenticação mútua, a sequência de chamada é a seguinte:

1.  O cliente chama a função conforme descrito anteriormente, mas o pacote retorna o código de \_ êxito I CONTINUE NEEDED da \_ \_ SEC.
2.  O cliente envia o token de saída para o servidor e aguarda a resposta do servidor.
3.  Após o recebimento da resposta do servidor, o cliente chama **InitializeSecurityContext (Kerberos)** novamente, com *phContext* definido como o alça que foi retornado da última chamada. O token recebido do servidor é fornecido no *parâmetro pInput.*

Se o servidor tiver respondido com êxito, o [*pacote de segurança*](../secgloss/s-gly.md) retornará SEC E OK e uma sessão segura será \_ \_ estabelecida.

Se a função retornar uma das respostas de erro, a resposta do servidor não será aceita e a sessão não será estabelecida.

Se a função retornar SEC I CONTINUE NEEDED, SEC I COMPLETE NEEDED ou SEC I COMPLETE AND CONTINUE, as etapas \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 2 e 3 serão repetidas.

Para inicializar um contexto de [*segurança,*](../secgloss/s-gly.md)mais de uma chamada para essa função pode ser necessária, dependendo do mecanismo de autenticação subjacente, bem como das opções especificadas no parâmetro *fContextReq.*

Os *parâmetros fContextReq* e *pfContextAttributes* são bitmasks que representam vários atributos de contexto. Para ver uma descrição dos vários atributos, confira [Requisitos de contexto.](context-requirements.md) O *parâmetro pfContextAttributes* é válido em qualquer retorno bem-sucedido, mas somente no retorno final bem-sucedido você deve examinar os sinalizadores que pertencem aos aspectos de segurança do contexto. Os retornos intermediários podem definir, por exemplo, o sinalizador ISC \_ RET \_ ALLOCATED \_ MEMORY.

Se o sinalizador ISC REQ USE SUPPLIED CREDS estiver definido, o pacote de segurança deverá procurar um tipo de \_ \_ buffer \_ \_ SECBUFFER PKG PARAMS [](../secgloss/s-gly.md) no buffer de entrada \_ \_ *pInput.* Essa não é uma solução genérica, mas permite [](../secgloss/s-gly.md) um emparelhamento forte de aplicativo e pacote de segurança quando apropriado.

Se ISC REQ ALLOCATE MEMORY tiver sido especificado, o chamador deverá liberar a memória chamando a \_ \_ função \_ [**FreeContextBuffer.**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)

Por exemplo, o token de entrada pode ser o desafio de um Gerente de LAN. Nesse caso, o token de saída seria a resposta criptografada por NTLM para o desafio.

A ação que o cliente toma depende do código de retorno dessa função. Se o código de retorno for SEC E OK, não haverá nenhuma segunda chamada \_ \_ **InitializeSecurityContext (Kerberos)** e nenhuma resposta do servidor será esperada. Se o código de retorno for SEC I CONTINUE NEEDED, o cliente esperará um token em resposta do servidor e o passará em uma segunda chamada para \_ \_ \_ **InitializeSecurityContext (Kerberos).** O código de retorno SEC I COMPLETE NEEDED indica que o cliente deve concluir a criação da mensagem e \_ \_ chamar a função \_ [**CompleteAuthToken.**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) O código \_ SEC I COMPLETE AND CONTINUE incorpora essas duas \_ \_ \_ ações.

Se **InitializeSecurityContext (Kerberos)** retornar êxito na primeira chamada (ou somente) , o chamador deverá eventualmente chamar a função [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) no alça retornado, mesmo que a chamada falhe em um trecho posterior da troca de autenticação.

O cliente pode chamar **InitializeSecurityContext (Kerberos)** novamente após a conclusão bem-sucedida. Isso indica ao pacote [*de segurança*](../secgloss/s-gly.md) que uma reauttenticação é procurada.

Os chamadores de modo kernel têm as seguintes diferenças: o nome de destino é uma cadeia de caracteres [*Unicode*](../secgloss/u-gly.md) que deve ser alocada na memória virtual usando [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc); ele não deve ser alocado do pool. Buffers passados e fornecidos em *pInput* e *pOutput* devem estar na memória virtual, não no pool.

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

[**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[**AcquireCredentialsHandle (Kerberos)**](acquirecredentialshandle--kerberos.md)
</dt> <dt>

[**Completeauthtoken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)
</dt> <dt>

[**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**Freecontextbuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)
</dt> <dt>

[**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
