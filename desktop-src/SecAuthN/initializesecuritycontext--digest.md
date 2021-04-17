---
description: Inicia o lado do cliente, [*contexto de segurança*](../secgloss/s-gly.md) de saída de um identificador de credencial usando a [*delegação restrita*](../secgloss/s-gly.md)de resumo.
ms.assetid: 4b482dcc-3878-4bc6-85e4-229a1726cecc
title: Função InitializeSecurityContext (Digest) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: cd5d99f4caef41523ee879abe086659de1889254
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790431"
---
# <a name="initializesecuritycontext-digest-function"></a>Função InitializeSecurityContext (Digest)

A função **InitializeSecurityContext (Digest)** inicia o lado do cliente, [*contexto de segurança*](../secgloss/s-gly.md) de saída de um identificador de credencial. A função é usada para criar um [*contexto de segurança*](../secgloss/s-gly.md) entre o aplicativo cliente e um par remoto. **InitializeSecurityContext (Digest)** retorna um token que o cliente deve passar para o par remoto, que o par, por sua vez, envia para a implementação de segurança local por meio da chamada de [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) . O token gerado deve ser considerado opaco por todos os chamadores.

Normalmente, a função **InitializeSecurityContext (Digest)** é chamada em um loop até que um [*contexto de segurança*](../secgloss/s-gly.md) suficiente seja estabelecido.

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS SEC_Entry InitializeSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_opt_    SEC_CHAR       *pszTargetName,
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

*phCredential* \[ em, opcional\]
</dt> <dd>

Um identificador para as credenciais retornadas por [**falha AcquireCredentialsHandle (Digest)**](acquirecredentialshandle--digest.md). Esse identificador é usado para criar o [*contexto de segurança*](../secgloss/s-gly.md). A função **InitializeSecurityContext (Digest)** requer pelo menos credenciais de saída.

</dd> <dt>

*phContext* \[ em, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura [CtxtHandle](sspi-handles.md) . Na primeira chamada para **InitializeSecurityContext (Digest)**, esse ponteiro é **nulo**. Na segunda chamada, esse parâmetro é um ponteiro para o identificador para o contexto formado parcialmente retornado no parâmetro *phNewContext* pela primeira chamada.

Esse parâmetro é opcional e pode ser definido como **nulo**.

</dd> <dt>

*pszTargetName* \[ em, opcional\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que identifica exclusivamente o URI do recurso solicitado. A cadeia de caracteres deve ser composta de caracteres permitidos em um URI e deve ser representável pelo conjunto de códigos ASCII dos EUA. A codificação percentual pode ser usada para representar caracteres fora do conjunto de códigos ASCII dos EUA.

</dd> <dt>

*fContextReq* \[ no\]
</dt> <dd>

Sinalizadores de bits que indicam solicitações para o contexto. Nem todos os pacotes podem dar suporte a todos os requisitos. Os sinalizadores usados para esse parâmetro são prefixados com o \_ req \_ do ISC, por exemplo, delegado de req do ISC \_ \_ . Esse parâmetro pode ser um ou mais dos seguintes sinalizadores de atributos.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Valor</th><th>Significado</th></tr></thead><tbody><tr class="odd"><td><span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl> <dt><strong>ISC_REQ_ALLOCATE_MEMORY</strong></dt> </dl></td><td>O [*pacote de segurança*](../secgloss/s-gly.md) aloca buffers de saída para você. Quando você terminar de usar os buffers de saída, libere-os chamando a função [<strong>FreeContextBuffer</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-FreeContextBuffer).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_CONFIDENTIALITY"></span><span id="isc_req_confidentiality"></span><dl> <dt><strong>ISC_REQ_CONFIDENTIALITY</strong></dt> </dl></td><td>Criptografe mensagens usando a função [<strong>EncryptMessage</strong>] (EncryptMessage--General.MD).<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl> <dt><strong>ISC_REQ_EXTENDED_ERROR</strong></dt> </dl></td><td>Quando ocorrerem erros, a parte remota será notificada.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_HTTP"></span><span id="isc_req_http"></span><dl> <dt><strong>ISC_REQ_HTTP</strong></dt> </dl></td><td>Use Digest para HTTP. Omita esse sinalizador para usar Digest como um mecanismo SASL.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_INTEGRITY"></span><span id="isc_req_integrity"></span><dl> <dt><strong>ISC_REQ_INTEGRITY</strong></dt> </dl></td><td>Assine mensagens e verifique as assinaturas usando as funções [<strong>EncryptMessage</strong>] (EncryptMessage--General.MD) e [<strong>MakeSignature</strong>] (MakeSignature.MD).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl> <dt><strong>ISC_REQ_MUTUAL_AUTH</strong></dt> </dl></td><td>A política de autenticação mútua do serviço será satisfeita.<br/><blockquote>[!Caution]<br />
Isso não significa necessariamente que a autenticação mútua seja executada, apenas que a política de autenticação do serviço seja satisfeita. Para garantir que a autenticação mútua seja executada, chame a função [<strong>QueryContextAttributes (Digest)</strong>] (QueryContextAttributes--Digest.MD).</blockquote><br/></td></tr><tr class="odd"><td><span id="ISC_REQ_REPLAY_DETECT"></span><span id="isc_req_replay_detect"></span><dl> <dt><strong>ISC_REQ_REPLAY_DETECT</strong></dt> </dl></td><td>Detectar as mensagens reproduzidas que foram codificadas usando as funções [<strong>EncryptMessage</strong>] (EncryptMessage--General.MD) ou [<strong>MakeSignature</strong>] (MakeSignature.MD).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl> <dt><strong>ISC_REQ_SEQUENCE_DETECT</strong></dt> </dl></td><td>Detecte mensagens recebidas fora de sequência.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl> <dt><strong>ISC_REQ_STREAM</strong></dt> </dl></td><td>Suporte a uma conexão orientada a fluxo.<br/></td></tr></tbody></table>



 

Os atributos solicitados podem não ter suporte do cliente. Para obter mais informações, consulte o parâmetro *pfContextAttr* .

Para obter descrições adicionais dos vários atributos, consulte [requisitos de contexto](context-requirements.md).

</dd> <dt>

*Reserved1* \[ no\]
</dt> <dd>

Esse parâmetro é reservado e deve ser definido como zero.

</dd> <dt>

*TargetDataRep* \[ no\]
</dt> <dd>

Esse parâmetro não é usado com Digest. Defina-o como zero.

</dd> <dt>

*pInput* \[ em, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) que contém ponteiros para os buffers fornecidos como entrada para o pacote. A menos que o contexto do cliente tenha sido iniciado pelo servidor, o valor desse parâmetro deve ser **nulo** na primeira chamada para a função. Nas chamadas subsequentes para a função ou quando o contexto do cliente foi iniciado pelo servidor, o valor desse parâmetro é um ponteiro para um buffer alocado com memória suficiente para conter o token retornado pelo computador remoto.

Para obter informações sobre a configuração de buffer, consulte [buffers de entrada para a resposta de desafio de resumo](input-buffers-for-the-digest-challenge-response.md).

</dd> <dt>

*Reserved2* \[ no\]
</dt> <dd>

Esse parâmetro é reservado e deve ser definido como zero.

</dd> <dt>

*phNewContext* \[ entrada, saída, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura [CtxtHandle](sspi-handles.md) . Na primeira chamada para **InitializeSecurityContext (Digest)**, esse ponteiro recebe o novo identificador de contexto. Na segunda chamada, *phNewContext* pode ser o mesmo que o identificador especificado no parâmetro *phContext* .

</dd> <dt>

*pOutput* \[ entrada, saída, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) que contém ponteiros para a estrutura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que recebe os dados de saída. Se um buffer tiver sido digitado como s \_ ReadWrite na entrada, ele estará lá na saída. O sistema alocará um buffer para o token de segurança, se solicitado (por meio da ISC, \_ \_ aloque a \_ memória) e preencherá o endereço no descritor de buffer para o token de segurança.

Esse parâmetro recebe a resposta de desafio que deve ser enviada ao servidor.

</dd> <dt>

*pfContextAttr* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável para receber um conjunto de sinalizadores de bits que indicam os [*atributos*](../secgloss/a-gly.md#_security_attribute_gly) do contexto estabelecido. Para obter uma descrição dos vários atributos, consulte [requisitos de contexto](context-requirements.md).

Os sinalizadores usados para esse parâmetro são prefixados com ISC \_ RET, como o delegado da ISC \_ RET \_ . Para obter uma lista de valores válidos, consulte o parâmetro *fContextReq* .

Não verifique os atributos relacionados à segurança até que a chamada de função final seja retornada com êxito. Os sinalizadores de atributo que não estão relacionados à segurança, como o \_ \_ sinalizador de memória alocada de ASC RET \_ , podem ser verificados antes do retorno final.

> [!Note]  
> Determinados atributos de contexto podem ser alterados durante a negociação com um par remoto.

 

</dd> <dt>

*ptsExpiry* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura de [**carimbo de data/**](timestamp.md) hora que recebe o tempo de expiração do contexto.

Não há tempo de expiração para Microsoft Digest s ou credenciais do [*contexto de segurança*](../secgloss/s-gly.md)do SSP.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, a função retornará um dos códigos de êxito a seguir.



| Código de retorno                                                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**s \_ E \_ OK**</dt> </dl>                      | O [*contexto de segurança*](../secgloss/s-gly.md) foi inicializado com êxito. Não há necessidade de outra chamada de [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) . Se a função retornar um token de saída, ou seja, se o \_ token SECBUFFER em *pOutput* for de comprimento diferente de zero, esse token deverá ser enviado ao servidor.<br/> |
| <dl> <dt>**s \_ I \_ concluir \_ e \_ continuar**</dt> </dl> | O cliente deve chamar [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) e, em seguida, passar a saída para o servidor. Em seguida, o cliente aguarda um token retornado e o passa, em outra chamada, para [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md).<br/>                                                                                                                                  |
| <dl> <dt>**s \_ \_ conclusão \_ necessária**</dt> </dl>        | O cliente deve concluir a compilação da mensagem e, em seguida, chamar a função [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) .<br/>                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**s \_ I \_ continuar \_ necessário**</dt> </dl>        | O cliente deve enviar o token de saída para o servidor e aguardar um token de retorno. O token retornado é passado em outra chamada para [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md). O token de saída pode estar vazio.<br/>                                                                                                                                                       |
| <dl> <dt>**s \_ \_ credenciais incompletas \_**</dt> </dl> | Use com Schannel. O servidor solicitou a autenticação do cliente e as credenciais fornecidas não incluem um certificado ou o certificado não foi emitido por uma autoridade de certificação (CA) confiável pelo servidor. Para obter mais informações, consulte Comentários.<br/>                                            |



 

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

A função **InitializeSecurityContext (Digest)** é usada por um cliente para inicializar um contexto de saída.

Para um [*contexto de segurança*](../secgloss/s-gly.md)de dois lados, a sequência de chamada é a seguinte:

1.  O cliente chama a função com *phContext* definido como **NULL** e preenche o descritor de buffer com a mensagem de entrada.
2.  O [*pacote de segurança*](../secgloss/s-gly.md) examina os parâmetros e constrói um token opaco, colocando-o no elemento token na matriz de buffer. Se o parâmetro *fContextReq* incluir o sinalizador de alocação de memória de req do ISC \_ \_ \_ , o [*pacote de segurança*](../secgloss/s-gly.md) alocará a memória e retornará o ponteiro no elemento token.
3.  O cliente envia o token retornado no buffer *pOutput* para o servidor de destino. Em seguida, o servidor passa o token como um argumento de entrada em uma chamada para a função [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) .
4.  [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) pode retornar um token, que o servidor envia para o cliente para uma segunda chamada para **InitializeSecurityContext (Digest)** se a primeira chamada for retornada \_ , eu \_ continuaria \_ necessário.

Para os s de [*contexto de segurança*](../secgloss/s-gly.md)de vários trechos, como autenticação mútua, a sequência de chamada é a seguinte:

1.  O cliente chama a função conforme descrito anteriormente, mas o pacote retorna a s \_ e eu \_ continue o \_ código de sucesso necessário.
2.  O cliente envia o token de saída para o servidor e aguarda a resposta do servidor.
3.  Após o recebimento da resposta do servidor, o cliente chama **InitializeSecurityContext (Digest)** novamente, com *phContext* definido para o identificador que foi retornado da última chamada. O token recebido do servidor é fornecido no parâmetro *pInput* .

Se o servidor tiver respondido com êxito, o [*pacote de segurança*](../secgloss/s-gly.md) retornará s \_ e \_ OK e uma sessão segura será estabelecida.

Se a função retornar uma das respostas de erro, a resposta do servidor não será aceita e a sessão não será estabelecida.

Se a função retornar s, \_ eu \_ continuaria \_ necessária, a conclusão da SEC \_ \_ \_ necessária ou SEC \_ que \_ concluí \_ e \_ continuaria, as etapas 2 e 3 serão repetidas.

Para inicializar um [*contexto de segurança*](../secgloss/s-gly.md), mais de uma chamada para essa função pode ser necessária, dependendo do mecanismo de autenticação subjacente, bem como das opções especificadas no parâmetro *fContextReq* .

Os parâmetros *fContextReq* e *pfContextAttributes* são bitmasks que representam vários atributos de contexto. Para obter uma descrição dos vários atributos, consulte [requisitos de contexto](context-requirements.md). O parâmetro *pfContextAttributes* é válido em qualquer retorno bem-sucedido, mas somente no retorno bem-sucedido final, você deve examinar os sinalizadores que pertencem aos aspectos de segurança do contexto. Os retornos intermediários podem definir, por exemplo, o \_ \_ sinalizador de memória alocada do ISC RET \_ .

Se o sinalizador de uso de credenciais do ISC \_ req. \_ \_ \_ for definido, o [*pacote de segurança*](../secgloss/s-gly.md) deverá procurar um tipo de buffer de parâmetros de \_ pacote SECBUFFER \_ no buffer de entrada *pInput* . Essa não é uma solução genérica, mas permite um emparelhamento forte do [*pacote de segurança*](../secgloss/s-gly.md) e do aplicativo quando apropriado.

Se o \_ cliente da ISC \_ alocar \_ memória foi especificada, o chamador deverá liberar a memória chamando a função [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .

Por exemplo, o token de entrada pode ser o desafio de um Gerenciador de LAN. Nesse caso, o token de saída seria a resposta criptografada em NTLM para o desafio.

A ação que o cliente leva depende do código de retorno dessa função. Se o código de retorno for s \_ E \_ OK, não haverá uma segunda chamada **InitializeSecurityContext (Digest)** e nenhuma resposta do servidor será esperada. Se o código de retorno for \_ s \_ , eu continuaria \_ necessário, o cliente espera um token em resposta do servidor e o passa em uma segunda chamada para **InitializeSecurityContext (Digest)**. A SEC \_ que \_ Concluo o \_ código de retorno necessário indica que o cliente deve concluir a compilação da mensagem e chamar a função [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) . A SEC \_ que eu \_ concluo \_ e \_ continue o código incorpora essas duas ações.

Se **InitializeSecurityContext (Digest)** retornar êxito na primeira chamada (ou somente), o chamador deverá eventualmente chamar a função [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) no identificador retornado, mesmo se a chamada falhar em um segmento posterior da troca de autenticação.

O cliente pode chamar **InitializeSecurityContext (Digest)** novamente depois que ele for concluído com êxito. Isso indica ao [*pacote de segurança*](../secgloss/s-gly.md) que uma reautenticação é desejada.

Os chamadores de modo kernel têm as seguintes diferenças: o nome de destino é uma cadeia de caracteres [*Unicode*](../secgloss/u-gly.md) que deve ser alocada na memória virtual usando o [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc); Ele não deve ser alocado do pool. Os buffers passados e fornecidos em *pInput* e *pOutput* devem estar na memória virtual, não no pool.

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

[**AcceptSecurityContext (resumo)**](acceptsecuritycontext--digest.md)
</dt> <dt>

[**Falha AcquireCredentialsHandle (resumo)**](acquirecredentialshandle--digest.md)
</dt> <dt>

[**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)
</dt> <dt>

[**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)
</dt> <dt>

[**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
