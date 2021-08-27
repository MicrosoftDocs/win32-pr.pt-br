---
description: Inicia o contexto de [](../secgloss/s-gly.md) segurança de saída do lado do cliente de um handle de credencial usando a delegação restrita de Kerberos [](../secgloss/s-gly.md).
ms.assetid: b5c968dc-9343-44ed-acbc-a89c58c14e4a
title: Função InitializeSecurityContext (Kerberos) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 8c558174c168b17b67c9c08b1aee92e6dc10161f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470531"
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




| Valor | Significado | 
|-------|---------|
| <span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl><dt><strong>ISC_REQ_ALLOCATE_MEMORY</strong></dt></dl> | O [*pacote de segurança*](../secgloss/s-gly.md) aloca buffers de saída para você. Quando terminar de usar os buffers de saída, livre-os chamando a [<strong>função FreeContextBuffer.</strong>](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)<br /> | 
| <span id="ISC_REQ_CONFIDENTIALITY"></span><span id="isc_req_confidentiality"></span><dl><dt><strong>ISC_REQ_CONFIDENTIALITY</strong></dt></dl> | Criptografe mensagens usando a [<strong>função EncryptMessage.</strong>](encryptmessage--general.md)<br /> | 
| <span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl><dt><strong>ISC_REQ_CONNECTION</strong></dt></dl> | O [*contexto de segurança*](../secgloss/s-gly.md) não manipulará mensagens de formatação. Esse valor é o padrão.<br /> | 
| <span id="ISC_REQ_DELEGATE"></span><span id="isc_req_delegate"></span><dl><dt><strong>ISC_REQ_DELEGATE</strong></dt></dl> | O servidor pode usar o contexto para autenticar em outros servidores como o cliente. O ISC_REQ_MUTUAL_AUTH sinalizador deve ser definido para que esse sinalizador funcione. Válido para Kerberos. Ignore esse sinalizador para [*delegação restrita.*](../secgloss/c-gly.md)<br /> | 
| <span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl><dt><strong>ISC_REQ_EXTENDED_ERROR</strong></dt></dl> | Quando ocorrerem erros, a parte remota será notificada.<br /> | 
| <span id="ISC_REQ_INTEGRITY"></span><span id="isc_req_integrity"></span><dl><dt><strong>ISC_REQ_INTEGRITY</strong></dt></dl> | Assine mensagens e verifique as assinaturas usando as [<strong>funções EncryptMessage</strong>](encryptmessage--general.md) [<strong>e MakeSignature.</strong>](makesignature.md)<br /> | 
| <span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl><dt><strong>ISC_REQ_MUTUAL_AUTH</strong></dt></dl> | A política de autenticação mútua do serviço será atendida.<br /><blockquote>[!Caution]<br />Isso não significa necessariamente que a autenticação mútua seja executada, apenas que a política de autenticação do serviço é atendida. Para garantir que a autenticação mútua seja executada, chame a [<strong>função QueryContextAttributes (Kerberos).</strong>](querycontextattributes--kerberos.md)</blockquote><br /> | 
| <span id="ISC_REQ_NO_INTEGRITY"></span><span id="isc_req_no_integrity"></span><dl><dt><strong>ISC_REQ_NO_INTEGRITY</strong></dt></dl> | Se esse sinalizador for definido, o <strong>sinalizador ISC_REQ_INTEGRITY</strong> será ignorado.<br /> | 
| <span id="ISC_REQ_REPLAY_DETECT"></span><span id="isc_req_replay_detect"></span><dl><dt><strong>ISC_REQ_REPLAY_DETECT</strong></dt></dl> | Detecte mensagens reprodução que foram codificadas usando as funções [<strong>EncryptMessage</strong>](encryptmessage--general.md) ou [<strong>MakeSignature.</strong>](makesignature.md)<br /> | 
| <span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl><dt><strong>ISC_REQ_SEQUENCE_DETECT</strong></dt></dl> | Detectar mensagens recebidas fora de sequência.<br /> | 
| <span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl><dt><strong>ISC_REQ_STREAM</strong></dt></dl> | Dar suporte a uma conexão orientada a fluxo.<br /> | 
| <span id="ISC_REQ_USE_SESSION_KEY"></span><span id="isc_req_use_session_key"></span><dl><dt><strong>ISC_REQ_USE_SESSION_KEY</strong></dt></dl> | Uma nova [*chave de sessão*](../secgloss/s-gly.md) deve ser negociada.<br /> | 




 

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
| <dl> <dt>**SEC \_ E \_ OK**</dt> </dl>                      | O [*contexto de segurança*](../secgloss/s-gly.md) foi inicializado com êxito. Não há necessidade de outra [**chamada InitializeSecurityContext (Kerberos).**](initializesecuritycontext--kerberos.md) Se a função retornar um token de saída, ou seja, se o \_ token SECBUFFER em *pOutput* for de comprimento diferente de zero, esse token deverá ser enviado ao servidor.<br/> |
| <dl> <dt>**s \_ I \_ concluir \_ e \_ continuar**</dt> </dl> | O cliente deve chamar [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) e, em seguida, passar a saída para o servidor. Em seguida, o cliente aguarda um token retornado e o passa, em outra chamada, para [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md).<br/>                                                                                                                                  |
| <dl> <dt>**s \_ \_ conclusão \_ necessária**</dt> </dl>        | O cliente deve concluir a compilação da mensagem e, em seguida, chamar a função [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) .<br/>                                                                                                                                                                                                                                                                                           |
| <dl> <dt>**s \_ I \_ continuar \_ necessário**</dt> </dl>        | O cliente deve enviar o token de saída para o servidor e aguardar um token de retorno. O token retornado é passado em outra chamada para [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md). O token de saída pode estar vazio.<br/>                                                                                                                                                       |
| <dl> <dt>**s \_ \_ credenciais incompletas \_**</dt> </dl> | Use com Schannel. O servidor solicitou a autenticação do cliente e as credenciais fornecidas não incluem um certificado ou o certificado não foi emitido por uma autoridade de certificação (CA) confiável pelo servidor. Para obter mais informações, consulte Comentários.<br/>                                                |



 

Se a função falhar, a função retornará um dos códigos de erro a seguir.



| Código de retorno                                                                                                          | Descrição                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**s \_ E \_ memória insuficiente \_**</dt> </dl>          | Não há memória suficiente disponível para concluir a ação solicitada.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**s \_ E \_ \_ erro interno**</dt> </dl>               | Ocorreu um erro que não foi mapeado para um código de erro SSPI.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>**s \_ E \_ \_ identificador inválido**</dt> </dl>               | O identificador passado para a função não é válido.<br/>                                                                                                                                                                                                                                          |
| <dl> <dt>**s \_ E \_ \_ token inválido**</dt> </dl>                | O erro ocorre devido a um token de entrada malformado, como um token corrompido em trânsito, um token de tamanho incorreto ou um token passado para a [*delegação restrita*](../secgloss/s-gly.md)errada. Passar um token para o pacote incorreto pode acontecer se o cliente e o servidor não negociarem a [*delegação restrita*](../secgloss/s-gly.md)adequada.<br/> |
| <dl> <dt>**s \_ E \_ logon \_ negado**</dt> </dl>                 | Falha no logon.<br/>                                                                                                                                                                                                                                                                        |
| <dl> <dt>**s \_ E \_ nenhuma \_ autoridade de autenticação \_**</dt> </dl> | Nenhuma autoridade pode ser contatada para autenticação. O nome de domínio da parte de autenticação pode estar errado, o domínio pode estar inacessível ou pode ter havido uma falha de relação de confiança.<br/>                                                                                  |
| <dl> <dt>**s \_ E \_ sem \_ credenciais**</dt> </dl>               | Não há credenciais disponíveis na [*delegação restrita*](../secgloss/s-gly.md).<br/>                                                                                                                                                  |
| <dl> <dt>**s \_ E \_ destino \_ desconhecidos**</dt> </dl>               | O destino não foi reconhecido.<br/>                                                                                                                                                                                                                                                           |
| <dl> <dt>**s \_ E \_ função sem suporte \_**</dt> </dl>         | Um sinalizador de atributo de contexto inválido ( \_ \_ delegado req do ISC ou \_ \_ prompt de solicitação \_ do ISC para \_ credenciais) foi especificado no parâmetro *fContextReq* .<br/>                                                                                                                                            |
| <dl> <dt>**\_principal s E \_ entidade de segurança incorreta \_**</dt> </dl>              | A entidade de segurança que recebeu a solicitação de autenticação não é a mesma passada para o parâmetro *pszTargetName* . Isso indica uma falha na autenticação mútua.<br/>                                                                                                          |



 

## <a name="remarks"></a>Comentários

O chamador é responsável por determinar se os atributos de contexto final são suficientes. Se, por exemplo, a confidencialidade for solicitada, mas não puder ser estabelecida, alguns aplicativos poderão optar por desligar a conexão imediatamente.

Se os atributos do [*contexto de segurança*](../secgloss/s-gly.md) não forem suficientes, o cliente deverá liberar o contexto parcialmente criado chamando a função [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) .

A função **InitializeSecurityContext (Kerberos)** é usada por um cliente para inicializar um contexto de saída.

Para um [*contexto de segurança*](../secgloss/s-gly.md)de dois lados, a sequência de chamada é a seguinte:

1.  O cliente chama a função com *phContext* definido como **NULL** e preenche o descritor de buffer com a mensagem de entrada.
2.  O [*pacote de segurança*](../secgloss/s-gly.md) examina os parâmetros e constrói um token opaco, colocando-o no elemento token na matriz de buffer. Se o parâmetro *fContextReq* incluir o sinalizador de alocação de memória de req do ISC \_ \_ \_ , o [*pacote de segurança*](../secgloss/s-gly.md) alocará a memória e retornará o ponteiro no elemento token.
3.  O cliente envia o token retornado no buffer *pOutput* para o servidor de destino. Em seguida, o servidor passa o token como um argumento de entrada em uma chamada para a função [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) .
4.  [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) pode retornar um token, que o servidor envia para o cliente para uma segunda chamada para **InitializeSecurityContext (Kerberos)** se a primeira chamada for retornada \_ , eu \_ continuaria \_ necessário.

Para os s de [*contexto de segurança*](../secgloss/s-gly.md)de vários trechos, como autenticação mútua, a sequência de chamada é a seguinte:

1.  O cliente chama a função conforme descrito anteriormente, mas o pacote retorna a s \_ e eu \_ continue o \_ código de sucesso necessário.
2.  O cliente envia o token de saída para o servidor e aguarda a resposta do servidor.
3.  Após o recebimento da resposta do servidor, o cliente chama **InitializeSecurityContext (Kerberos)** novamente, com *phContext* definido para o identificador que foi retornado da última chamada. O token recebido do servidor é fornecido no parâmetro *pInput* .

Se o servidor tiver respondido com êxito, o [*pacote de segurança*](../secgloss/s-gly.md) retornará s \_ e \_ OK e uma sessão segura será estabelecida.

Se a função retornar uma das respostas de erro, a resposta do servidor não será aceita e a sessão não será estabelecida.

Se a função retornar s, \_ eu \_ continuaria \_ necessária, a conclusão da SEC \_ \_ \_ necessária ou SEC \_ que \_ concluí \_ e \_ continuaria, as etapas 2 e 3 serão repetidas.

Para inicializar um [*contexto de segurança*](../secgloss/s-gly.md), mais de uma chamada para essa função pode ser necessária, dependendo do mecanismo de autenticação subjacente, bem como das opções especificadas no parâmetro *fContextReq* .

Os parâmetros *fContextReq* e *pfContextAttributes* são bitmasks que representam vários atributos de contexto. Para obter uma descrição dos vários atributos, consulte [requisitos de contexto](context-requirements.md). O parâmetro *pfContextAttributes* é válido em qualquer retorno bem-sucedido, mas somente no retorno bem-sucedido final, você deve examinar os sinalizadores que pertencem aos aspectos de segurança do contexto. Os retornos intermediários podem definir, por exemplo, o \_ \_ sinalizador de memória alocada do ISC RET \_ .

Se o sinalizador de uso de credenciais do ISC \_ req. \_ \_ \_ for definido, o [*pacote de segurança*](../secgloss/s-gly.md) deverá procurar um tipo de buffer de parâmetros de \_ pacote SECBUFFER \_ no buffer de entrada *pInput* . Essa não é uma solução genérica, mas permite um emparelhamento forte do [*pacote de segurança*](../secgloss/s-gly.md) e do aplicativo quando apropriado.

Se o \_ cliente da ISC \_ alocar \_ memória foi especificada, o chamador deverá liberar a memória chamando a função [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .

Por exemplo, o token de entrada pode ser o desafio de um Gerenciador de LAN. Nesse caso, o token de saída seria a resposta criptografada em NTLM para o desafio.

A ação que o cliente leva depende do código de retorno dessa função. Se o código de retorno for s \_ E \_ OK, não haverá uma segunda chamada de **InitializeSecurityContext (Kerberos)** e nenhuma resposta do servidor será esperada. Se o código de retorno for \_ s \_ , eu continuaria \_ necessário, o cliente espera um token em resposta do servidor e o passa em uma segunda chamada para **InitializeSecurityContext (Kerberos)**. A SEC \_ que \_ Concluo o \_ código de retorno necessário indica que o cliente deve concluir a compilação da mensagem e chamar a função [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) . A SEC \_ que eu \_ concluo \_ e \_ continue o código incorpora essas duas ações.

Se **InitializeSecurityContext (Kerberos)** retornar êxito na primeira chamada (ou somente), o chamador deverá eventualmente chamar a função [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) no identificador retornado, mesmo se a chamada falhar em um segmento posterior da troca de autenticação.

O cliente pode chamar **InitializeSecurityContext (Kerberos)** novamente depois que ele for concluído com êxito. Isso indica ao [*pacote de segurança*](../secgloss/s-gly.md) que uma reautenticação é desejada.

Os chamadores de modo kernel têm as seguintes diferenças: o nome de destino é uma cadeia de caracteres [*Unicode*](../secgloss/u-gly.md) que deve ser alocada na memória virtual usando o [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc); Ele não deve ser alocado do pool. Os buffers passados e fornecidos em *pInput* e *pOutput* devem estar na memória virtual, não no pool.

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

[**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[**Falha AcquireCredentialsHandle (Kerberos)**](acquirecredentialshandle--kerberos.md)
</dt> <dt>

[**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)
</dt> <dt>

[**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)
</dt> <dt>

[**Secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**Secbufferdesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
