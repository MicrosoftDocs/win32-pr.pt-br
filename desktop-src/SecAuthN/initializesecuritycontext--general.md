---
description: Inicia o lado do cliente, [*contexto de segurança*](../secgloss/s-gly.md) de saída de um identificador de credencial.
ms.assetid: 21d965d4-3c03-4e29-a70d-4538c5c366b0
title: Função InitializeSecurityContext (geral) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: f67832ae3593e893d56e9a3d772b635ef2aac327d6e997dafb152682da569ae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015916"
---
# <a name="initializesecuritycontext-general-function"></a>Função InitializeSecurityContext (geral)

A função **InitializeSecurityContext (geral)** inicia o lado do cliente, [*contexto de segurança*](../secgloss/s-gly.md) de saída de um identificador de credencial. A função é usada para criar um [*contexto de segurança*](../secgloss/s-gly.md) entre o aplicativo cliente e um par remoto. **InitializeSecurityContext (geral)** retorna um token que o cliente deve passar para o par remoto, que o par, por sua vez, envia para a implementação de segurança local por meio da chamada [**AcceptSecurityContext (geral)**](acceptsecuritycontext--general.md) . O token gerado deve ser considerado opaco por todos os chamadores.

Normalmente, a função **InitializeSecurityContext (geral)** é chamada em um loop até que um [*contexto de segurança*](../secgloss/s-gly.md) suficiente seja estabelecido.

Para obter informações sobre como usar essa função com um SSP ( [*provedor de suporte de segurança*](../secgloss/s-gly.md) ) específico, consulte os tópicos a seguir.



| Tópico                                                                                  | Descrição                                                                                                                                |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md)     | Inicia o lado do cliente, [*contexto de segurança*](../secgloss/s-gly.md) de saída de um identificador de credencial usando o [*pacote de segurança*](../secgloss/s-gly.md)do Credential Security Support Provider (CredSSP).  
| [**InitializeSecurityContext (resumo)**](initializesecuritycontext--digest.md)       | Inicia o lado do cliente, [*contexto de segurança*](../secgloss/s-gly.md) de saída de um identificador de credencial usando o [*pacote de segurança*](../secgloss/s-gly.md)Digest.                        |
| [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md)   | Inicia o lado do cliente, [*contexto de segurança*](../secgloss/s-gly.md) de saída de um identificador de credencial usando o [*pacote de segurança*](../secgloss/s-gly.md)do Kerberos.                      |
| [**InitializeSecurityContext (negociar)**](initializesecuritycontext--negotiate.md) | Inicia o lado do cliente, [*contexto de segurança*](../secgloss/s-gly.md) de saída de um identificador de credencial usando o [*pacote de segurança*](../secgloss/s-gly.md)Negotiate.                     |
| [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md)           | Inicia o lado do cliente, [*contexto de segurança*](../secgloss/s-gly.md) de saída de um identificador de credencial usando o [*pacote de segurança*](../secgloss/s-gly.md)NTLM.                          |
| [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md)   | Inicia o lado do cliente, [*contexto de segurança*](../secgloss/s-gly.md) de saída de um identificador de credencial usando o [*pacote de segurança*](../secgloss/s-gly.md)Schannel.                      |



 

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

Um identificador para as credenciais retornadas por [**falha AcquireCredentialsHandle (geral)**](acquirecredentialshandle--general.md). Esse identificador é usado para criar o [*contexto de segurança*](../secgloss/s-gly.md). A função **InitializeSecurityContext (geral)** requer pelo menos credenciais de saída.

</dd> <dt>

*phContext* \[ em, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura [CtxtHandle](sspi-handles.md) . Na primeira chamada para **InitializeSecurityContext (geral)**, esse ponteiro é **nulo**. Na segunda chamada, esse parâmetro é um ponteiro para o identificador para o contexto formado parcialmente retornado no parâmetro *phNewContext* pela primeira chamada.

Esse parâmetro é opcional com o Microsoft Digest SSP e pode ser definido como **nulo**.

Ao usar o SSP do Schannel, na primeira chamada para **InitializeSecurityContext (geral)**, especifique **NULL**. Em chamadas futuras, especifique o token recebido no parâmetro *phNewContext* após a primeira chamada para essa função.

</dd> <dt>

*pTargetName* \[ em, opcional\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que indica o destino do contexto. O conteúdo da cadeia de caracteres é específico do [*pacote de segurança*](../secgloss/s-gly.md) , conforme descrito na tabela a seguir. Esta lista não é exaustiva. Os SSPs de sistema adicionais e os SSPs de terceiros podem ser adicionados a um sistema.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>SSP em uso</th><th>Significado</th></tr></thead><tbody><tr class="odd"><td><span id="Digest"></span><span id="digest"></span><span id="DIGEST"></span><dl> <dt><strong>Resumo</strong></dt><dt></dt> </dl></td><td>Cadeia de caracteres terminada em nulo que identifica exclusivamente o URI do recurso solicitado. A cadeia de caracteres deve ser composta de caracteres permitidos em um URI e deve ser representável pelo conjunto de códigos ASCII dos EUA. A codificação percentual pode ser usada para representar caracteres fora do conjunto de códigos ASCII dos EUA.<br/></td></tr><tr class="even"><td><span id="Kerberos_or_Negotiate"></span><span id="kerberos_or_negotiate"></span><span id="KERBEROS_OR_NEGOTIATE"></span><dl> <dt><strong>Kerberos ou Negotiate</strong></dt><dt></dt> </dl></td><td>SPN (nome da entidade de serviço) ou o [*contexto de segurança*](../secgloss/s-gly.md) do servidor de destino.<br/></td></tr><tr class="odd"><td><span id="NTLM"></span><span id="ntlm"></span><dl> <dt><strong>NTLM</strong></dt><dt></dt> </dl></td><td>SPN (nome da entidade de serviço) ou o [*contexto de segurança*](../secgloss/s-gly.md) do servidor de destino.<br/></td></tr><tr class="even"><td><span id="Schannel_SSL"></span><span id="schannel_ssl"></span><span id="SCHANNEL_SSL"></span><dl> <dt><strong>Schannel/SSL</strong></dt><dt></dt> </dl></td><td>Cadeia de caracteres terminada em nulo que identifica exclusivamente o servidor de destino. O Schannel usa esse valor para verificar o certificado do servidor. O Schannel também usa esse valor para localizar a sessão no cache da sessão ao restabelecer uma conexão. A sessão armazenada em cache será usada somente se todas as condições a seguir forem atendidas:<ul><li>O nome de destino é o mesmo.</li><li>A entrada do cache não expirou.</li><li>O processo do aplicativo que chama a função é o mesmo.</li><li>A sessão de logon é a mesma.</li><li>O identificador de credencial é o mesmo.</li></ul><br/></td></tr></tbody></table>



 

</dd> <dt>

*fContextReq* \[ no\]
</dt> <dd>

Sinalizadores de bits que indicam solicitações para o contexto. Nem todos os pacotes podem dar suporte a todos os requisitos. Os sinalizadores usados para esse parâmetro são prefixados com o \_ req \_ do ISC, por exemplo, delegado de req do ISC \_ \_ . Esse parâmetro pode ser um ou mais dos seguintes sinalizadores de atributos.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Valor</th><th>Significado</th></tr></thead><tbody><tr class="odd"><td><span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl> <dt><strong>ISC_REQ_ALLOCATE_MEMORY</strong></dt> </dl></td><td>O [*pacote de segurança*](../secgloss/s-gly.md) aloca buffers de saída para você. Quando você terminar de usar os buffers de saída, libere-os chamando a função [<strong>FreeContextBuffer</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-FreeContextBuffer).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_CONFIDENTIALITY"></span><span id="isc_req_confidentiality"></span><dl> <dt><strong>ISC_REQ_CONFIDENTIALITY</strong></dt> </dl></td><td>Criptografe mensagens usando a função [<strong>EncryptMessage</strong>] (EncryptMessage--General.MD).<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl> <dt><strong>ISC_REQ_CONNECTION</strong></dt> </dl></td><td>O [*contexto de segurança*](../secgloss/s-gly.md) não tratará mensagens de formatação. Esse valor é o padrão para os s de [*delegação restrita*](../secgloss/s-gly.md)de Kerberos, Negotiate e NTLM.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_DELEGATE"></span><span id="isc_req_delegate"></span><dl> <dt><strong>ISC_REQ_DELEGATE</strong></dt> </dl></td><td>O servidor pode usar o contexto para autenticar em outros servidores como o cliente. O sinalizador de ISC_REQ_MUTUAL_AUTH deve ser definido para que esse sinalizador funcione. Válido para Kerberos. Ignore este sinalizador para [*delegação restrita*](../secgloss/c-gly.md).<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl> <dt><strong>ISC_REQ_EXTENDED_ERROR</strong></dt> </dl></td><td>Quando ocorrerem erros, a parte remota será notificada.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_HTTP"></span><span id="isc_req_http"></span><dl> <dt><strong>ISC_REQ_HTTP</strong></dt> </dl></td><td>Use Digest para HTTP. Omita esse sinalizador para usar Digest como um mecanismo SASL.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_INTEGRITY"></span><span id="isc_req_integrity"></span><dl> <dt><strong>ISC_REQ_INTEGRITY</strong></dt> </dl></td><td>Assine mensagens e verifique as assinaturas usando as funções [<strong>EncryptMessage</strong>] (EncryptMessage--General.MD) e [<strong>MakeSignature</strong>] (MakeSignature.MD).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_MANUAL_CRED_VALIDATION"></span><span id="isc_req_manual_cred_validation"></span><dl> <dt><strong>ISC_REQ_MANUAL_CRED_VALIDATION</strong></dt> </dl></td><td>O Schannel não deve autenticar o servidor automaticamente.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl> <dt><strong>ISC_REQ_MUTUAL_AUTH</strong></dt> </dl></td><td>A política de autenticação mútua do serviço será satisfeita.<br/><blockquote>[!Caution]<br />
Isso não significa necessariamente que a autenticação mútua seja executada, apenas que a política de autenticação do serviço seja satisfeita. Para garantir que a autenticação mútua seja executada, chame a função [<strong>QueryContextAttributes (General)</strong>] (QueryContextAttributes--General.MD).</blockquote><br/></td></tr><tr class="even"><td><span id="ISC_REQ_NO_INTEGRITY"></span><span id="isc_req_no_integrity"></span><dl> <dt><strong>ISC_REQ_NO_INTEGRITY</strong></dt> </dl></td><td>Se esse sinalizador for definido, o sinalizador de <strong>ISC_REQ_INTEGRITY</strong> será ignorado.<br/> Esse valor só tem suporte pelos s de [*delegação restrita*](../secgloss/s-gly.md)e negociação Kerberos.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_REPLAY_DETECT"></span><span id="isc_req_replay_detect"></span><dl> <dt><strong>ISC_REQ_REPLAY_DETECT</strong></dt> </dl></td><td>Detectar as mensagens reproduzidas que foram codificadas usando as funções [<strong>EncryptMessage</strong>] (EncryptMessage--General.MD) ou [<strong>MakeSignature</strong>] (MakeSignature.MD).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl> <dt><strong>ISC_REQ_SEQUENCE_DETECT</strong></dt> </dl></td><td>Detecte mensagens recebidas fora de sequência.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl> <dt><strong>ISC_REQ_STREAM</strong></dt> </dl></td><td>Suporte a uma conexão orientada a fluxo.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_USE_SESSION_KEY"></span><span id="isc_req_use_session_key"></span><dl> <dt><strong>ISC_REQ_USE_SESSION_KEY</strong></dt> </dl></td><td>Uma nova [*chave de sessão*](../secgloss/s-gly.md) deve ser negociada.<br/> Esse valor só tem suporte pela [*delegação restrita*](../secgloss/s-gly.md)de Kerberos.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_USE_SUPPLIED_CREDS"></span><span id="isc_req_use_supplied_creds"></span><dl> <dt><strong>ISC_REQ_USE_SUPPLIED_CREDS</strong></dt> </dl></td><td>O Schannel não deve tentar fornecer credenciais para o cliente automaticamente.<br/></td></tr></tbody></table>



 

Os atributos solicitados podem não ter suporte do cliente. Para obter mais informações, consulte o parâmetro *pfContextAttr* .

Para obter descrições adicionais dos vários atributos, consulte [requisitos de contexto](context-requirements.md).

</dd> <dt>

*Reserved1* \[ no\]
</dt> <dd>

Esse parâmetro é reservado e deve ser definido como zero.

</dd> <dt>

*TargetDataRep* \[ no\]
</dt> <dd>

A representação de dados, como ordenação de bytes, no destino. Esse parâmetro pode ser segurança \_ nativa \_ DREP ou segurança de \_ rede \_ DREP.

Esse parâmetro não é usado com Digest ou Schannel. Defina-o como zero.

</dd> <dt>

*pInput* \[ em, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) que contém ponteiros para os buffers fornecidos como entrada para o pacote. A menos que o contexto do cliente tenha sido iniciado pelo servidor, o valor desse parâmetro deve ser **nulo** na primeira chamada para a função. Nas chamadas subsequentes para a função ou quando o contexto do cliente foi iniciado pelo servidor, o valor desse parâmetro é um ponteiro para um buffer alocado com memória suficiente para conter o token retornado pelo computador remoto.

</dd> <dt>

*Reserved2* \[ no\]
</dt> <dd>

Esse parâmetro é reservado e deve ser definido como zero.

</dd> <dt>

*phNewContext* \[ entrada, saída, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura [CtxtHandle](sspi-handles.md) . Na primeira chamada para **InitializeSecurityContext (geral)**, esse ponteiro recebe o novo identificador de contexto. Na segunda chamada, *phNewContext* pode ser o mesmo que o identificador especificado no parâmetro *phContext* .

Ao usar o SSP do Schannel, em chamadas após a primeira chamada, passe o identificador retornado aqui como o parâmetro *phContext* e especifique **NULL** para *phNewContext*.

</dd> <dt>

*pOutput* \[ entrada, saída, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) que contém ponteiros para a estrutura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que recebe os dados de saída. Se um buffer tiver sido digitado como s \_ ReadWrite na entrada, ele estará lá na saída. O sistema alocará um buffer para o token de segurança, se solicitado (por meio da ISC, \_ \_ aloque a \_ memória) e preencherá o endereço no descritor de buffer para o token de segurança.

Ao usar o Microsoft Digest SSP, esse parâmetro recebe a resposta de desafio que deve ser enviada ao servidor.

Ao usar o SSP do Schannel, se o \_ sinalizador de alocar memória do uso da ISC \_ \_ for especificado, o SSP do Schannel irá alocar memória para o buffer e colocar as informações apropriadas no [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc). Além disso, o chamador deve passar um buffer do tipo **\_ alerta de SECBUFFER**. Na saída, se um alerta for gerado, esse buffer conterá informações sobre esse alerta e a função falhará.

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

Um ponteiro para uma estrutura de [**carimbo de data/**](timestamp.md) hora que recebe o tempo de expiração do contexto. É recomendável que o [*pacote de segurança*](../secgloss/s-gly.md) sempre retorne esse valor na hora local. Esse parâmetro é opcional e **NULL** deve ser passado para clientes de curta duração.

Não há tempo de expiração para Microsoft Digest s ou credenciais do [*contexto de segurança*](../secgloss/s-gly.md)do SSP.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, a função retornará um dos códigos de êxito a seguir.



| Código de retorno                                                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**s \_ I \_ concluir \_ e \_ continuar**</dt> </dl> | O cliente deve chamar [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) e, em seguida, passar a saída para o servidor. Em seguida, o cliente aguarda um token retornado e o passa, em outra chamada, para [**InitializeSecurityContext (geral)**](initializesecuritycontext--general.md).<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**s \_ \_ conclusão \_ necessária**</dt> </dl>        | O cliente deve concluir a compilação da mensagem e, em seguida, chamar a função [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**s \_ I \_ continuar \_ necessário**</dt> </dl>        | O cliente deve enviar o token de saída para o servidor e aguardar um token de retorno. O token retornado é passado em outra chamada para [**InitializeSecurityContext (geral)**](initializesecuritycontext--general.md). O token de saída pode estar vazio.<br/>                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**s \_ \_ credenciais incompletas \_**</dt> </dl> | Use com Schannel. O servidor solicitou a autenticação do cliente e as credenciais fornecidas não incluem um certificado ou o certificado não foi emitido por uma autoridade de certificação confiável pelo servidor. Para obter mais informações, consulte Comentários.<br/>                                                                                                                                                                                              |
| <dl> <dt>**s \_ E \_ mensagem incompleta \_**</dt> </dl>     | Use com Schannel. Os dados de toda a mensagem não foram lidos da transmissão.<br/> Quando esse valor é retornado, o buffer *pInput* contém uma estrutura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) com um membro **BufferType** de **SecBuffer \_ ausente**. O membro **cbBuffer** de **SecBuffer** contém um valor que indica o número de bytes adicionais que a função deve ler do cliente antes que essa função tenha sucesso. Embora esse número nem sempre seja preciso, usá-lo pode ajudar a melhorar o desempenho, evitando várias chamadas para essa função.<br/> |
| <dl> <dt>**s \_ E \_ OK**</dt> </dl>                      | O [*contexto de segurança*](../secgloss/s-gly.md) foi inicializado com êxito. Não há necessidade de outra chamada de [**InitializeSecurityContext (geral)**](initializesecuritycontext--general.md) . Se a função retornar um token de saída, ou seja, se o \_ token SECBUFFER em *pOutput* for de comprimento diferente de zero, esse token deverá ser enviado ao servidor.<br/>                                                                                                                                                    |



 

Se a função falhar, a função retornará um dos códigos de erro a seguir.



| Código de retorno                                                                                                          | Descrição                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**s \_ E \_ memória insuficiente \_**</dt> </dl>          | Não há memória suficiente disponível para concluir a ação solicitada.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**s \_ E \_ \_ erro interno**</dt> </dl>               | Ocorreu um erro que não foi mapeado para um código de erro SSPI.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>**s \_ E \_ \_ identificador inválido**</dt> </dl>               | O identificador passado para a função não é válido.<br/>                                                                                                                                                                                                                                          |
| <dl> <dt>**s \_ E \_ \_ token inválido**</dt> </dl>                | O erro ocorre devido a um token de entrada malformado, como um token corrompido em trânsito, um token de tamanho incorreto ou um token passado para o [*pacote de segurança*](../secgloss/s-gly.md)errado. Passar um token para o pacote incorreto pode acontecer se o cliente e o servidor não negociarem o [*pacote de segurança*](../secgloss/s-gly.md)adequado.<br/> |
| <dl> <dt>**s \_ E \_ logon \_ negado**</dt> </dl>                 | Falha no logon.<br/>                                                                                                                                                                                                                                                                        |
| <dl> <dt>**s \_ E \_ nenhuma \_ autoridade de autenticação \_**</dt> </dl> | Nenhuma autoridade pode ser contatada para autenticação. O nome de domínio da parte de autenticação pode estar errado, o domínio pode estar inacessível ou pode ter havido uma falha de relação de confiança.<br/>                                                                                  |
| <dl> <dt>**s \_ E \_ sem \_ credenciais**</dt> </dl>               | Não há credenciais disponíveis no [*pacote de segurança*](../secgloss/s-gly.md).<br/>                                                                                                                                                  |
| <dl> <dt>**s \_ E \_ destino \_ desconhecidos**</dt> </dl>               | O destino não foi reconhecido.<br/>                                                                                                                                                                                                                                                           |
| <dl> <dt>**s \_ E \_ função sem suporte \_**</dt> </dl>         | Um sinalizador de atributo de contexto inválido ( \_ \_ delegado req do ISC ou \_ \_ prompt de solicitação \_ do ISC para \_ credenciais) foi especificado no parâmetro *fContextReq* .<br/>                                                                                                                                            |
| <dl> <dt>**\_principal s E \_ entidade de segurança incorreta \_**</dt> </dl>              | A entidade de segurança que recebeu a solicitação de autenticação não é a mesma passada para o parâmetro *pszTargetName* . Isso indica uma falha na autenticação mútua.<br/>                                                                                                          |



 

## <a name="remarks"></a>Comentários

O chamador é responsável por determinar se os atributos de contexto final são suficientes. Se, por exemplo, a confidencialidade for solicitada, mas não puder ser estabelecida, alguns aplicativos poderão optar por desligar a conexão imediatamente.

Se os atributos do [*contexto de segurança*](../secgloss/s-gly.md) não forem suficientes, o cliente deverá liberar o contexto parcialmente criado chamando a função [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) .

A função **InitializeSecurityContext (geral)** é usada por um cliente para inicializar um contexto de saída.

Para um [*contexto de segurança*](../secgloss/s-gly.md)de dois lados, a sequência de chamada é a seguinte:

1.  O cliente chama a função com *phContext* definido como **NULL** e preenche o descritor de buffer com a mensagem de entrada.
2.  O [*pacote de segurança*](../secgloss/s-gly.md) examina os parâmetros e constrói um token opaco, colocando-o no elemento token na matriz de buffer. Se o parâmetro *fContextReq* incluir o sinalizador de alocação de memória de req do ISC \_ \_ \_ , o [*pacote de segurança*](../secgloss/s-gly.md) alocará a memória e retornará o ponteiro no elemento token.
3.  O cliente envia o token retornado no buffer *pOutput* para o servidor de destino. Em seguida, o servidor passa o token como um argumento de entrada em uma chamada para a função [**AcceptSecurityContext (geral)**](acceptsecuritycontext--general.md) .
4.  [**AcceptSecurityContext (geral)**](acceptsecuritycontext--general.md) pode retornar um token, que o servidor envia para o cliente para uma segunda chamada para **InitializeSecurityContext (geral)** se a primeira chamada for retornada \_ , eu \_ continuaria \_ necessário.

Para os s de [*contexto de segurança*](../secgloss/s-gly.md)de vários trechos, como autenticação mútua, a sequência de chamada é a seguinte:

1.  O cliente chama a função conforme descrito anteriormente, mas o pacote retorna a s \_ e eu \_ continue o \_ código de sucesso necessário.
2.  O cliente envia o token de saída para o servidor e aguarda a resposta do servidor.
3.  Após o recebimento da resposta do servidor, o cliente chama **InitializeSecurityContext (geral)** novamente, com *phContext* definido para o identificador que foi retornado da última chamada. O token recebido do servidor é fornecido no parâmetro *pInput* .

Se o servidor tiver respondido com êxito, o [*pacote de segurança*](../secgloss/s-gly.md) retornará s \_ e \_ OK e uma sessão segura será estabelecida.

Se a função retornar uma das respostas de erro, a resposta do servidor não será aceita e a sessão não será estabelecida.

Se a função retornar s, \_ eu \_ continuaria \_ necessária, a conclusão da SEC \_ \_ \_ necessária ou SEC \_ que \_ concluí \_ e \_ continuaria, as etapas 2 e 3 serão repetidas.

Para inicializar um [*contexto de segurança*](../secgloss/s-gly.md), mais de uma chamada para essa função pode ser necessária, dependendo do mecanismo de autenticação subjacente, bem como das opções especificadas no parâmetro *fContextReq* .

Os parâmetros *fContextReq* e *pfContextAttributes* são bitmasks que representam vários atributos de contexto. Para obter uma descrição dos vários atributos, consulte [requisitos de contexto](context-requirements.md). O parâmetro *pfContextAttributes* é válido em qualquer retorno bem-sucedido, mas somente no retorno bem-sucedido final, você deve examinar os sinalizadores que pertencem aos aspectos de segurança do contexto. Os retornos intermediários podem definir, por exemplo, o \_ \_ sinalizador de memória alocada do ISC RET \_ .

Se o sinalizador de uso de credenciais do ISC \_ req. \_ \_ \_ for definido, o [*pacote de segurança*](../secgloss/s-gly.md) deverá procurar um tipo de buffer de parâmetros de \_ pacote SECBUFFER \_ no buffer de entrada *pInput* . Essa não é uma solução genérica, mas permite um emparelhamento forte do [*pacote de segurança*](../secgloss/s-gly.md) e do aplicativo quando apropriado.

Se o \_ cliente da ISC \_ alocar \_ memória foi especificada, o chamador deverá liberar a memória chamando a função [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .

Por exemplo, o token de entrada pode ser o desafio de um Gerenciador de LAN. Nesse caso, o token de saída seria a resposta criptografada em NTLM para o desafio.

A ação que o cliente leva depende do código de retorno dessa função. Se o código de retorno for s \_ E \_ OK, não haverá uma segunda chamada de **InitializeSecurityContext (geral)** e nenhuma resposta do servidor será esperada. Se o código de retorno for \_ s \_ , eu continuaria \_ necessário, o cliente espera um token em resposta do servidor e o passa em uma segunda chamada para **InitializeSecurityContext (geral)**. A SEC \_ que \_ Concluo o \_ código de retorno necessário indica que o cliente deve concluir a compilação da mensagem e chamar a função [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) . A SEC \_ que eu \_ concluo \_ e \_ continue o código incorpora essas duas ações.

Se **InitializeSecurityContext (geral)** retornar êxito na primeira chamada (ou somente), o chamador deverá eventualmente chamar a função [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) no identificador retornado, mesmo se a chamada falhar em um segmento posterior da troca de autenticação.

O cliente pode chamar **InitializeSecurityContext (geral)** novamente após a conclusão com êxito. Isso indica ao [*pacote de segurança*](../secgloss/s-gly.md) que uma reautenticação é desejada.

Os chamadores de modo kernel têm as seguintes diferenças: o nome de destino é uma cadeia de caracteres [*Unicode*](../secgloss/u-gly.md) que deve ser alocada na memória virtual usando o [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc); Ele não deve ser alocado do pool. Os buffers passados e fornecidos em *pInput* e *pOutput* devem estar na memória virtual, não no pool.

Ao usar o SSP do Schannel, se a função retornar \_ \_ as credenciais incompletas da SEC \_ , verifique se você especificou um certificado válido e confiável em suas credenciais. O certificado é especificado ao chamar a função [**falha AcquireCredentialsHandle (geral)**](acquirecredentialshandle--general.md) . O certificado deve ser um certificado de autenticação de cliente emitido por uma autoridade de certificação (CA) confiável pelo servidor. Para obter uma lista das CAs confiáveis pelo servidor, chame a função [**QueryContextAttributes (geral)**](querycontextattributes--general.md) e especifique o \_ \_ \_ atributo ex do emissor da lista de SECPKG attr \_ .

Ao usar o SSP do Schannel, depois que um aplicativo cliente recebe um certificado de autenticação de uma AC confiável pelo servidor, o aplicativo cria uma nova credencial chamando a função [**falha AcquireCredentialsHandle (geral)**](acquirecredentialshandle--general.md) e, em seguida, chamando **InitializeSecurityContext (geral)** novamente, especificando a nova credencial no parâmetro *phCredential* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                   |
| Cabeçalho<br/>                   | <dl> <dt>SSPI. h (incluir Security. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Nomes Unicode e ANSI<br/>   | **InitializeSecurityContextW** (Unicode) e **InitializeSecurityContextA** (ANSI)<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (geral)**](acceptsecuritycontext--general.md)
</dt> <dt>

[**Falha AcquireCredentialsHandle (geral)**](acquirecredentialshandle--general.md)
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

 

 
