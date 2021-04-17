---
description: Inicia o lado do cliente, contexto de segurança de saída de um identificador de credencial.
ms.assetid: f3d8c07b-db28-4f26-ba29-8733fc95bdb5
title: Função InitializeSecurityContext (CredSSP) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: aa359fc0cedf96f43d93cfb7d962035453328759
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812132"
---
# <a name="initializesecuritycontext-credssp-function"></a>Função InitializeSecurityContext (CredSSP)

A função **InitializeSecurityContext (CredSSP)** inicia o contexto de segurança de saída do lado do cliente de um identificador de credencial. A função cria um contexto de segurança entre o aplicativo cliente e um par remoto. **InitializeSecurityContext (CredSSP)** retorna um token que o cliente deve passar para o par remoto; o par, por sua vez, envia esse token para a implementação de segurança local por meio da chamada [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) . O token gerado deve ser considerado opaco por todos os chamadores.

Normalmente, a função **InitializeSecurityContext (CredSSP)** é chamada em um loop até que um contexto de segurança suficiente seja estabelecido.

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS SEC_ENTRY InitializeSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_opt_    SEC_CHAR       *pszTargetName,
  _In_        unsigned long  fContextReq,
  _Reserved_  unsigned long  Reserved1,
  _In_        unsigned long  TargetDataRep,
  _Inout_opt_ PSecBufferDesc pInput,
  _In_        unsigned long  Reserved2,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Out_opt_   PSecBufferDesc pOutput,
  _Out_       unsigned long  *pfContextAttr,
  _Out_opt_   PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*phCredential* \[ em, opcional\]
</dt> <dd>

Um identificador para as credenciais retornadas por [**falha AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md). Esse identificador é usado para criar o contexto de segurança. A função **InitializeSecurityContext (CredSSP)** requer pelo menos credenciais de saída.

</dd> <dt>

*phContext* \[ em, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura [CtxtHandle](sspi-handles.md) . Na primeira chamada para **InitializeSecurityContext (CredSSP)**, esse ponteiro é **nulo**. Na segunda chamada, esse parâmetro é um ponteiro para o identificador para o contexto formado parcialmente retornado no parâmetro *phNewContext* pela primeira chamada.

Na primeira chamada para **InitializeSecurityContext (CredSSP)**, especifique **NULL**. Em chamadas futuras, especifique o token recebido no parâmetro *phNewContext* após a primeira chamada para essa função.

</dd> <dt>

*pTargetName* \[ em, opcional\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que identifica exclusivamente o servidor de destino. O Schannel usa esse valor para verificar o certificado do servidor. O Schannel também usa esse valor para localizar a sessão no cache da sessão ao restabelecer uma conexão. A sessão armazenada em cache será usada somente se todas as condições a seguir forem atendidas:

-   O nome de destino é o mesmo.
-   A entrada do cache não expirou.
-   O processo do aplicativo que chama a função é o mesmo.
-   A sessão de logon é a mesma.
-   O identificador de credencial é o mesmo.

</dd> <dt>

*fContextReq* \[ no\]
</dt> <dd>

Sinalizadores de bits que indicam solicitações para o contexto. Nem todos os pacotes podem dar suporte a todos os requisitos. Os sinalizadores usados para esse parâmetro são prefixados com o \_ req \_ do ISC, por exemplo, delegado de req do ISC \_ \_ .

Esse parâmetro pode ser um ou mais dos seguintes sinalizadores de atributos.



| Valor                                                                                                                                                                                                                                                                            | Significado                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl> <dt>**ISC \_ REQ \_ alocar \_ memória**</dt> <dt>0x100</dt> </dl>                         | O pacote de segurança aloca buffers de saída para o chamador. Quando você terminar de usar os buffers de saída, libere-os chamando a função [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .<br/>                                                        |
| <span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl> <dt>**ISC \_ 0x800 de \_ conexão req**</dt> . <dt></dt> </dl>                                         | O contexto de segurança não tratará mensagens de formatação.<br/>                                                                                                                                                                                               |
| <span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl> <dt>**ISC \_ 0x4000 \_ de \_ erro ESTENDIdo req**</dt> . <dt></dt> </dl>                           | Quando ocorrerem erros, a parte remota será notificada.<br/>                                                                                                                                                                                                   |
| <span id="ISC_REQ_MANUAL_CRED_VALIDATION"></span><span id="isc_req_manual_cred_validation"></span><dl> <dt>**ISC \_ 0x80000 \_ de \_ \_ validação de credenciais de req manual**</dt> <dt></dt> </dl> | O CredSSP (provedor de suporte à segurança de credencial) não deve autenticar o servidor automaticamente. Esse sinalizador é sempre definido ao usar CredSSP.<br/>                                                                                                              |
| <span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl> <dt>**ISC \_ \_Seqüência \_**</dt> de solicitações de detecção de sequência de req <dt></dt> </dl>                           | Detecte mensagens recebidas fora de sequência.<br/>                                                                                                                                                                                                               |
| <span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl> <dt>**ISC \_ 0x8000 do \_ fluxo de req**</dt> . <dt></dt> </dl>                                                    | Suporte a uma conexão orientada a fluxo.<br/>                                                                                                                                                                                                                   |
| <span id="ISC_REQ_USE_SUPPLIED_CREDS"></span><span id="isc_req_use_supplied_creds"></span><dl> <dt>**ISC \_ REQ \_ usar \_ \_ creds fornecidas**</dt> <dt>0x80</dt> </dl>                | O CredSSP não deve tentar fornecer credenciais para o cliente automaticamente.<br/>                                                                                                                                                                            |
| <span id="ISC_REQ_DELEGATE"></span><span id="isc_req_delegate"></span><dl> <dt>**ISC \_ REQ \_ delegado**</dt> <dt>0x1</dt> </dl>                                                 | Indica que as credenciais do usuário devem ser delegadas ao servidor.<br/> Se esse sinalizador não for especificado, um conjunto vazio de credenciais será delegado ao servidor.<br/> **Windows Server 2008 e Windows Vista:** Esse sinalizador é necessário.<br/> |
| <span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl> <dt>**ISC \_ 0x2 \_ de \_ autenticação mútua do req**</dt> . <dt></dt> </dl>                                       | Indica que a autenticação do servidor não é necessária. As políticas de delegação ainda serão impostas se esse sinalizador não for especificado.<br/> **Windows Server 2008 e Windows Vista:** Esse sinalizador é ignorado.<br/>                                                 |



 

Os atributos solicitados podem não ter suporte do cliente. Para obter mais informações, consulte o parâmetro *pfContextAttr* .

Para obter descrições adicionais dos vários atributos, consulte [requisitos de contexto](context-requirements.md).

</dd> <dt>

*Reserved1* \[ no\]
</dt> <dd>

Reservado. Esse parâmetro deve ser definido como zero.

</dd> <dt>

*TargetDataRep* \[ no\]
</dt> <dd>

A representação de dados, como ordenação de bytes, no destino. Esse parâmetro pode ser **segurança \_ nativa \_ DREP** ou segurança de **\_ rede \_ DREP**.

</dd> <dt>

*pInput* \[ entrada, saída, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) que contém ponteiros para os buffers fornecidos como entrada para o pacote. A menos que o contexto do cliente tenha sido iniciado pelo servidor, o valor desse parâmetro deve ser **nulo** na primeira chamada para a função. Nas chamadas subsequentes para a função ou quando o contexto do cliente foi iniciado pelo servidor, o valor desse parâmetro é um ponteiro para um buffer alocado com memória suficiente para conter o token retornado pelo computador remoto.

Em chamadas para essa função após a chamada inicial, deve haver dois buffers. O primeiro tem o tipo de **\_ token SECBUFFER** e contém o token recebido do servidor. O segundo buffer tem o tipo **SECBUFFER \_ vazio**; defina os membros **pvBuffer** e **cbBuffer** como zero.

</dd> <dt>

*Reserved2* \[ no\]
</dt> <dd>

Reservado. Esse parâmetro deve ser definido como zero.

</dd> <dt>

*phNewContext* \[ entrada, saída, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura [CtxtHandle](sspi-handles.md) . Na primeira chamada para **InitializeSecurityContext (CredSSP)**, esse ponteiro recebe o novo identificador de contexto. Na segunda chamada, *phNewContext* pode ser o mesmo que o identificador especificado no parâmetro *phContext* .

Em chamadas após a primeira chamada, passe o identificador retornado aqui como o parâmetro *phContext* e especifique **NULL** para *phNewContext*.

</dd> <dt>

*pOutput* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . Essa estrutura, por sua vez, contém ponteiros para a estrutura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que recebe os dados de saída. Se um buffer tiver sido digitado como **s \_ ReadWrite** na entrada, ele estará lá na saída. O sistema alocará um buffer para o token de segurança, se solicitado (por meio da **ISC, \_ aloque a \_ \_ memória**) e preencherá o endereço no descritor de buffer para o token de segurança.

Se o sinalizador de **\_ \_ alocar \_ memória de req** . do ISC for especificado, o CredSSP alocará memória para o buffer e colocará as informações apropriadas no [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc).

</dd> <dt>

*pfContextAttr* \[ fora\]
</dt> <dd>

Um ponteiro para um conjunto de sinalizadores de bit que indicam os [*atributos*](../secgloss/a-gly.md#_security_attribute_gly) do contexto estabelecido. Para obter uma descrição dos vários atributos, consulte [requisitos de contexto](context-requirements.md).

Os sinalizadores usados para esse parâmetro são prefixados com ISC \_ RET, como o **\_ \_ delegado da ISC RET**. Para obter uma lista de valores válidos, consulte o parâmetro *fContextReq* .

Não verifique os atributos relacionados à segurança até que a chamada de função final seja retornada com êxito. Os sinalizadores de atributo que não estão relacionados à segurança, como o sinalizador de **\_ \_ \_ memória alocada de ASC RET** , podem ser verificados antes do retorno final.

> [!Note]  
> Determinados atributos de contexto podem ser alterados durante a negociação com um par remoto.

 

</dd> <dt>

*ptsExpiry* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura de [**carimbo de data/**](timestamp.md) hora que recebe o tempo de expiração do contexto. É recomendável que o pacote de segurança sempre retorne esse valor na hora local. Esse parâmetro é opcional e **NULL** deve ser passado para clientes de curta duração.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, ela retornará um dos códigos de êxito a seguir.



| Código de retorno                                                                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**s \_ E \_ mensagem incompleta \_**</dt> </dl>     | Os dados de toda a mensagem não foram lidos da transmissão.<br/> Quando esse valor é retornado, o buffer *pInput* contém uma estrutura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) com um membro **BufferType** de **SecBuffer \_ ausente**. O membro **cbBuffer** de **SecBuffer** especifica o número de bytes adicionais que a função deve ler do cliente antes que essa função tenha sucesso. Embora esse número nem sempre seja preciso, usá-lo pode ajudar a melhorar o desempenho, evitando várias chamadas para essa função.<br/> |
| <dl> <dt>**s \_ E \_ OK**</dt> </dl>                      | O contexto de segurança foi inicializado com êxito. Não há necessidade de outra chamada de [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) . Se a função retornar um token de saída, ou seja, se o **\_ token SECBUFFER** em *pOutput* for de comprimento diferente de zero, esse token deverá ser enviado ao servidor.<br/>                                                                                                   |
| <dl> <dt>**s \_ I \_ concluir \_ e \_ continuar**</dt> </dl> | O cliente deve chamar [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) e, em seguida, passar a saída para o servidor. Em seguida, o cliente aguarda um token retornado e o passa, em outra chamada, para [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md).<br/>                                                                                                                                                                                                                                            |
| <dl> <dt>**s \_ \_ conclusão \_ necessária**</dt> </dl>        | O cliente deve concluir a compilação da mensagem e, em seguida, chamar a função [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**s \_ I \_ continuar \_ necessário**</dt> </dl>        | O cliente deve enviar o token de saída para o servidor e aguardar um token de retorno. O cliente passa o token retornado em outra chamada para [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md). O token de saída pode estar vazio.<br/>                                                                                                                                                                                                                                                              |
| <dl> <dt>**s \_ \_ credenciais incompletas \_**</dt> </dl> | O servidor solicitou autenticação de cliente, mas as credenciais fornecidas não incluem um certificado ou o certificado não foi emitido por uma autoridade de certificação na qual o servidor confia. Para obter mais informações, consulte Comentários.<br/>                                                                                                                                                                              |



 

Se a função falhar, a função retornará um dos códigos de erro a seguir.



| Código de retorno                                                                                                          | Description                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**s \_ E \_ memória insuficiente \_**</dt> </dl>          | Não há memória suficiente disponível para concluir a ação solicitada.<br/>                                                                                                                                                                                                     |
| <dl> <dt>**s \_ E \_ \_ erro interno**</dt> </dl>               | Ocorreu um erro que não foi mapeado para um código de erro SSPI.<br/>                                                                                                                                                                                                                  |
| <dl> <dt>**s \_ E \_ \_ identificador inválido**</dt> </dl>               | O identificador passado para a função não é válido.<br/>                                                                                                                                                                                                                            |
| <dl> <dt>**s \_ E \_ \_ token inválido**</dt> </dl>                | O token de entrada está malformado. As possíveis causas incluem um token corrompido em trânsito, um token de tamanho incorreto e um token passado para o pacote de segurança errado. Essa última condição pode ocorrer se o cliente e o servidor não negociarem o pacote de segurança adequado.<br/> |
| <dl> <dt>**s \_ E \_ logon \_ negado**</dt> </dl>                 | Falha no logon.<br/>                                                                                                                                                                                                                                                          |
| <dl> <dt>**s \_ E \_ nenhuma \_ autoridade de autenticação \_**</dt> </dl> | Nenhuma autoridade pode ser contatada para autenticação. O nome de domínio da parte de autenticação pode estar errado, o domínio pode estar inacessível ou pode ter havido uma falha de relação de confiança.<br/>                                                                    |
| <dl> <dt>**s \_ E \_ sem \_ credenciais**</dt> </dl>               | Não há credenciais disponíveis no pacote de segurança.<br/>                                                                                                                                    |
| <dl> <dt>**s \_ E \_ destino \_ desconhecidos**</dt> </dl>               | O destino não foi reconhecido.<br/>                                                                                                                                                                                                                                             |
| <dl> <dt>**s \_ E \_ função sem suporte \_**</dt> </dl>         | O valor do parâmetro *fContextReq* não é válido. Um sinalizador necessário não foi especificado ou um sinalizador que não tem suporte pelo CredSSP foi especificado.<br/>                                                                                                                 |
| <dl> <dt>**\_principal s E \_ entidade de segurança incorreta \_**</dt> </dl>              | A entidade de segurança que recebeu a solicitação de autenticação não é a mesma passada para o parâmetro *pszTargetName* . Esse erro indica uma falha na autenticação mútua.<br/>                                                                                      |
| <dl> <dt>**\_política de \_ delegação s E \_**</dt> </dl>            | A política não dá suporte à delegação de credenciais para o servidor de destino.<br/>                                                                                                                                                                                                |
| <dl> <dt>**s \_ E \_ \_ somente NLTM da política \_**</dt> </dl>            | A delegação de credenciais para o servidor de destino não é permitida quando a autenticação mútua não é obtida.<br/>                                                                                                                                                                  |
| <dl> <dt>**s \_ E \_ \_ autenticação mútua \_ com falha**</dt> </dl>          | Falha na autenticação do servidor quando o \_ sinalizador de autenticação mútua de req do ISC \_ \_ é especificado no parâmetro *fContextReq* .<br/>                                                                                                                                                             |



 

## <a name="remarks"></a>Comentários

O chamador é responsável por determinar se os atributos de contexto final são suficientes. Se, por exemplo, a confidencialidade for solicitada, mas não puder ser estabelecida, alguns aplicativos poderão optar por desligar a conexão imediatamente.

Se os atributos do contexto de segurança não forem suficientes, o cliente deverá liberar o contexto parcialmente criado chamando a função [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) .

O cliente chama a função **InitializeSecurityContext (CredSSP)** para inicializar um contexto de saída.

Para um contexto de segurança de dois lados, a sequência de chamada é a seguinte:

1.  O cliente chama a função com *phContext* definido como **NULL** e preenche o descritor de buffer com a mensagem de entrada.
2.  O pacote de segurança examina os parâmetros e constrói um token opaco, colocando-o no elemento TOKEN na matriz de buffer. Se o parâmetro *fContextReq* incluir o sinalizador de **alocação de \_ \_ \_ memória de req do ISC** , o pacote de segurança alocará a memória e retornará o ponteiro no elemento token.
3.  O cliente envia o token retornado no buffer *pOutput* para o servidor de destino. Em seguida, o servidor passa o token como um argumento de entrada em uma chamada para a função [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) .
4.  [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) pode retornar um token. O servidor envia esse token para o cliente por meio de uma segunda chamada de **InitializeSecurityContext (CredSSP)** se a primeira chamada for retornada **\_ , eu \_ continuaria \_ necessário**.

Se o servidor tiver respondido com êxito, o pacote de segurança retornará **s \_ e \_ OK** e uma sessão segura será estabelecida.

Se a função retornar uma das respostas de erro, a resposta do servidor não será aceita e a sessão não será estabelecida.

Se a função retornar **s, \_ eu \_ continuaria \_ necessária**, a **conclusão da SEC \_ \_ \_ necessária** ou **SEC \_ que \_ concluí \_ e \_ continuaria**, as etapas 2 e 3 serão repetidas.

A inicialização de contexto de segurança pode exigir mais de uma chamada para essa função, dependendo do mecanismo de autenticação subjacente, bem como das opções especificadas no parâmetro *fContextReq* .

Os parâmetros *fContextReq* e *pfContextAttributes* são bitmasks que representam vários atributos de contexto. Para obter uma descrição dos vários atributos, consulte [requisitos de contexto](context-requirements.md). Embora o parâmetro *pfContextAttributes* seja válido em qualquer retorno bem-sucedido, você deve examinar os sinalizadores que pertencem aos aspectos de segurança do contexto somente no retorno bem-sucedido final. Os retornos intermediários podem definir, por exemplo, o sinalizador de **\_ \_ \_ memória alocada do ISC RET** .

Se o sinalizador de **\_ uso de \_ \_ \_ credenciais do ISC req** . for definido, o pacote de segurança deverá procurar um tipo de buffer de **\_ \_ parâmetros de pacote SECBUFFER** no buffer de entrada *pInput* . Embora essa não seja uma solução genérica, ela permite um forte emparelhamento de pacote de segurança e aplicativo quando apropriado.

Se o cliente da **ISC \_ \_ alocar \_ memória** foi especificada, o chamador deverá liberar a memória chamando a função [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .

Por exemplo, o token de entrada pode ser o desafio de um Gerenciador de LAN. Nesse caso, o token de saída seria a resposta criptografada em NTLM para o desafio.

A ação que o cliente leva depende do código de retorno dessa função. Se o código de retorno for **s \_ E \_ OK**, não haverá uma segunda chamada de **InitializeSecurityContext (CredSSP)** e nenhuma resposta do servidor será esperada. Se o código de retorno for **s, \_ eu \_ continuaria \_ necessário**, o cliente espera um token em resposta do servidor e o passa em uma segunda chamada para **InitializeSecurityContext (CredSSP)**. A **SEC \_ que \_ concluo \_** o código de retorno necessário indica que o cliente deve concluir a compilação da mensagem e chamar a função [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) . A **SEC \_ que eu \_ concluo \_ e \_ continue** o código incorpora essas duas ações.

Se **InitializeSecurityContext (CredSSP)** retornar êxito na primeira chamada (ou somente), o chamador deverá eventualmente chamar a função [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) no identificador retornado, mesmo se a chamada falhar em um segmento posterior da troca de autenticação.

O cliente pode chamar **InitializeSecurityContext (CredSSP)** novamente após a conclusão com êxito. Isso indica ao pacote de segurança que uma reautenticação é desejada.

Os chamadores de modo kernel têm as seguintes diferenças: o nome de destino é uma cadeia de caracteres [*Unicode*](../secgloss/u-gly.md#_security_unicode_gly) que deve ser alocada na memória virtual usando o [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc); Ele não deve ser alocado do pool. Os buffers passados e fornecidos em *pInput* e *pOutput* devem estar na memória virtual, não no pool.

Se a função retornar **as \_ \_ \_ credenciais s incompletas**, verifique se as credenciais de r passadas para a função [**falha AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md) especificou um certificado válido e confiável que o certificado deve ser um certificado de autenticação de cliente emitido por uma autoridade de certificação confiável pelo servidor. Para obter uma lista das CAs confiáveis pelo servidor, chame a função [**QueryContextAttributes (CredSSP)**](querycontextattributes--credssp.md) com o atributo **SECPKG da \_ \_ lista de emissores \_ \_** de atributos do.

Depois de receber um certificado de autenticação de uma autoridade de certificação que o servidor confia, o aplicativo cliente cria uma nova credencial. Ele faz isso chamando a função [**falha AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md) e, em seguida, chamando **InitializeSecurityContext (CredSSP)** novamente, especificando a nova credencial no parâmetro *phCredential* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                   |
| parâmetro<br/>                   | <dl> <dt>SSPI. h (incluir Security. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md)
</dt> <dt>

[**Falha AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md)
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

 

 
