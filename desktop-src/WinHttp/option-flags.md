---
Description: Os seguintes sinalizadores de opção têm suporte de WinHttpQueryOption e WinHttpSetOption.
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: Sinalizadores de opção (WinHTTP. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: 91a9506225c53893990d4dcdc534293daa6c8e00
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262057"
---
# <a name="option-flags"></a>Sinalizadores de opção

Os seguintes sinalizadores de opção têm suporte de [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) e [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).

<dl> <dt>

<span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**\_opção WinHTTP \_ garantindo \_ \_ \_ retornos de chamada sem bloqueio**
</dt> <dd> <dl> <dt>



O padrão é FALSE. Se definido como TRUE, o WinHTTP não garantirá o progresso se os retornos de chamada de status forem bloqueados pelo aplicativo cliente.

O aplicativo cliente deve tomar cuidado especial para executar operações mínimas no retorno de chamada sem bloqueio, retornando o mais rápido possível e, em particular, não deve esperar por nenhuma chamada de WinHTTP subsequente. Se não seguir essas diretrizes, provavelmente haverá um impacto negativo no desempenho ou um possível travamento do aplicativo. Se usado da maneira prescrita, essa opção pode melhorar o desempenho.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**política de WINHTTP da \_ opção de \_ logon automático \_**
</dt> <dd> <dl> <dt>



Define um valor inteiro longo sem sinal que especifica a [política de logon automática](authentication-in-winhttp.md) com um dos valores a seguir.

| Termo | Descrição |
|-|-|
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>nível de segurança do WINHTTP \_ AUTOlogonn \_ \_ \_ alto | As credenciais padrão não são usadas. Observe que esse sinalizador só terá efeito se você especificar o servidor pelo nome real do computador. Ele não entrará em vigor, se você especificar o servidor por "localhost" ou endereço IP. |
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>nível de segurança do WINHTTP com \_ \_ acesso automático \_ \_ reduzido | Um logon autenticado usando as credenciais padrão é executado para todas as solicitações. |
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>nível de segurança do WINHTTP com \_ logon automático \_ \_ \_ médio | Um logon autenticado usando as credenciais padrão é executado somente para solicitações na intranet local. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**retorno de chamada de \_ opção WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera o ponteiro para a função de retorno de chamada definida com [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**\_contexto de \_ certificado de cliente de opção WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Define o contexto de certificado do cliente. Se um aplicativo receber [**o \_ certificado de autenticação de cliente WinHTTP de erro \_ \_ \_ \_ necessário**](error-messages.md), ele deverá chamar [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) para fornecer um certificado antes de repetir a solicitação. Como parte do processamento dessa opção, o WinHttp chama [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) no contexto de certificado fornecido pelo chamador para que o contexto do certificado possa ser liberado independentemente pelo chamador.

> [!Note]
> O aplicativo não deve tentar fechar o repositório de certificados com o \_ sinalizador de \_ sinalizador de força de armazenamento de fechamento de certificado \_ \_ na chamada para [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) no repositório de certificados do qual o contexto de certificado foi recuperado. Pode ocorrer uma violação de acesso.

Quando o servidor solicita um certificado de cliente, o [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)ou o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) retorna um erro WinHTTP erro de [**certificado de \_ \_ \_ autenticação de \_ \_ cliente**](error-messages.md) . Se o servidor solicitar o certificado, mas não o exigir, o aplicativo poderá especificar essa opção para indicar que ele não tem um certificado. O servidor pode escolher outro esquema de autenticação ou permitir acesso anônimo ao servidor. O aplicativo fornece a macro de **contexto de \_ \_ \_ certificado \_ de cliente do WinHTTP** no parâmetro *lpBuffer* de [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , conforme mostrado no exemplo de código a seguir.

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

Se o servidor exigir um certificado de cliente, ele poderá enviar um código de status HTTP 403 em resposta. Para obter mais informações, consulte **a \_ opção \_ WinHTTP \_ \_ \_ lista de emissor de certificado de cliente** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**\_opção WinHTTP \_ \_ lista de emissor de certificado de cliente \_ \_**
</dt> <dd> <dl> <dt>



Recupera uma [**estrutura SecPkgContext \_ IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) quando o erro de [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) ou [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) é um **erro \_ WinHTTP \_ Client \_ auth \_ CERT \_ necessário**. A lista emissor na estrutura contém uma lista de autoridades de certificação aceitáveis (CA) do servidor. O aplicativo cliente pode filtrar a lista de autoridades de certificação para recuperar o certificado do cliente para autenticação SSL.

Como alternativa, se o servidor solicitar o certificado do cliente, mas não precisar dele, o aplicativo poderá chamar [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) com a opção **WinHTTP de contexto de \_ \_ \_ certificado \_ de cliente** . Para obter mais informações, consulte opção **WinHTTP de contexto de certificado de \_ \_ cliente \_ \_ de opção** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**página de código da \_ opção WinHTTP \_**
</dt> <dd> <dl> <dt>



Define a [*página de código*](glossary.md) usada para processar a URL (ou seja, a cadeia de caracteres de consulta). O padrão é UTF8.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**\_opção WinHTTP \_ Configurar \_ autenticação do Passport \_**
</dt> <dd> <dl> <dt>



Define um valor inteiro longo sem sinal que especifica se a [autenticação do Passport na autenticação do WinHTTP](passport-authentication-in-winhttp.md) está habilitada. O valor pode ser um dos seguintes:

| Termo | Descrição |
|-|-|
| <span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP \_ desabilitar \_ autenticação do Passport \_ | A autenticação Microsoft Passport está desabilitada. Esse é o padrão. |
| <span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP \_ desabilitar \_ o \_ keyring do Passport | O token de telefone do Passport está desabilitado. Esse é o padrão. |
| <span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP \_ habilitar \_ autenticação do Passport \_ | A autenticação do Passport está habilitada. |
| <span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP \_ habilitar \_ o \_ token de toque do Passport | O token de telefone do Passport está habilitado. |

</dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**\_ \_ novas tentativas de conexão de opção WinHTTP \_**
</dt> <dd> <dl> <dt>



Define ou recupera um valor inteiro longo sem sinal que contém o número de tentativas de timesWinHTTP para se conectar a um host. O Microsoft Windows HTTP Services (WinHTTP) só tenta uma vez por endereço IP (Internet Protocol). Por exemplo, se você tentar se conectar a um host de hospedagem múltipla que tem 10 endereços IP e **a \_ opção WinHTTP as \_ \_ repetições de conexão** estiver definida como 7, o WinHTTP tentará se conectar somente com o primeiro endereço IP sete. Dado o mesmo conjunto de 10 endereços IP, se **a \_ opção WinHTTP \_ conectar \_ repetições** estiver definida como 20, o WinHTTP tentará cada uma das 10 somente uma vez. Se uma tentativa de conexão ainda falhar após o número especificado de tentativas ou se o tempo limite de conexão expirar antes de então, a solicitação será cancelada. O valor padrão para **as \_ \_ \_ repetições de conexão de opção de WinHTTP** é cinco tentativas.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**\_ \_ tempo limite de conexão da opção WinHTTP \_**
</dt> <dd> <dl> <dt>



Define ou recupera um valor inteiro longo sem sinal que contém o valor de tempo limite, em milissegundos. Definir essa opção como infinito (0xFFFFFFFF) desabilitará esse temporizador.

Se uma solicitação de conexão TCP demorar mais do que esse valor de tempo limite, a solicitação será cancelada. O tempo limite padrão é de 60 segundos. Quando você está tentando se conectar a vários endereços IP para um único host (um host de hospedagem múltipla), o tempo limite é para cada conexão individual.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**\_informações de \_ conexão da opção WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera o endereço IP de origem e de destino e a porta da solicitação que gerou a resposta quando [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) retorna. O aplicativo chama [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) com a opção de **\_ informações de \_ conexão \_ da opção WinHTTP** e fornece a estrutura de [**informações de \_ conexão \_ WinHTTP**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) no parâmetro *lpBuffer* . Para obter mais informações, **consulte \_ \_ informações de conexão do WinHTTP**.

**Windows Server 2003 com SP1 e Windows XP com SP2:** Este sinalizador é obsoleto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**\_V0 de \_ Estatísticas de conexão da opção WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera o [**struct \_ \_ V0 de informações de TCP**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) para a conexão subjacente usada pela solicitação. A estrutura retornada pode conter estatísticas de solicitações anteriores enviadas pela mesma conexão.

> [!Note]
> Esta opção foi substituída por **WinHTTP \_ Option \_ Connection \_ stats \_ v1**.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**\_Estatísticas de conexão da opção WinHTTP \_ \_ \_ v1**
</dt> <dd> <dl> <dt>



Recupera a estrutura de [**informações do TCP \_ \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) para a conexão subjacente usada pela solicitação. A estrutura retornada pode conter estatísticas de solicitações anteriores enviadas pela mesma conexão.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**\_valor de \_ contexto da opção WinHTTP \_**
</dt> <dd> <dl> <dt>



Define ou recupera um **\_ PTR de DWORD** que contém um ponteiro para o valor de contexto associado a esse identificador [HINTERNET](hinternet-handles-in-winhttp.md) . O valor armazenado no buffer é usado e o sinalizador de opção de **\_ valor de \_ contexto \_ de opção WinHTTP** recebe um novo valor.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**\_DEScompactação da opção WinHTTP \_**
</dt> <dd> <dl> <dt>



Define um DWORD de sinalizadores que determinam se o WinHTTP irá descompactar automaticamente os corpos de resposta com codificações de conteúdo compactadas. O WinHTTP também definirá um cabeçalho de Accept-Encoding apropriado, substituindo qualquer um fornecido pelo chamador. Os valores com suporte são:

| Termo | Descrição |
|-|-|
| <span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>\_sinalizador de DEScompactação de WinHTTP \_ \_ gzip | Descompactar conteúdo-codificação: respostas gzip. |
| <span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>\_sinalizador de DEScompactação WinHTTP \_ \_ deflate | Descompactar conteúdo-codificação: reinflar respostas. |
| <span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>\_sinalizador de DEScompactação de WinHTTP \_ \_ All | Descompacte as respostas com qualquer codificação de conteúdo com suporte. |

Por padrão, o WinHTTP fornecerá respostas compactadas ao chamador sem modificações.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**RECURSO DESABILITAR OPÇÃO WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Define um valor inteiro longo sem sinal que especifica quais recursos estão desabilitados com um ou mais dos sinalizadores a seguir. Esteja ciente de que esse recurso só deve ser passado para [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) em alças de solicitação depois que o handle de solicitação é criado com [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)e antes que a solicitação seja enviada com [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).

| Termo | Descrição |
|-|-|
| <span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>DESABILITAR AUTENTICAÇÃO DO WINHTTP \_ \_ | A autenticação automática está desabilitada. |
| <span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>DESABILITAR COOKIES WINHTTP \_ \_ | A adição automática de headers de cookie às solicitações está desabilitada. Além disso, os cookies retornados não são adicionados automaticamente ao banco de dados de cookie. Desabilitar cookies pode resultar em baixo desempenho para autenticação do Passport. |
| <span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP \_ DISABLE \_ KEEP \_ ALIVE | Desabilita a semântica keep alive para a conexão. A semântica keep alive é necessária para MSN, NTLM e outros tipos de autenticação. |
| <span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>DESABILITAR \_ REDIRECIONAMENTOS DO WINHTTP \_ | O redirecionamento automático é desabilitado ao enviar solicitações [**com WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) Se o redirecionamento automático estiver desabilitado, um aplicativo deverá registrar uma função de retorno de chamada para que a autenticação do Passport seja bem-sucedida. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**OPÇÃO WINHTTP \_ \_ DESABILITAR \_ \_ FALLBACK DE \_ PROTOCOLO SEGURO**
</dt> <dd> <dl> <dt>



Impede que o WinHTTP repetir uma conexão com uma versão inferior do protocolo de segurança quando a negociação de protocolo inicial falhar.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**OPÇÃO WINHTTP \_ \_ DESABILITAR \_ FILA DE \_ FLUXO**
</dt> <dd> <dl> <dt>



Permite que novas solicitações abram uma conexão HTTP/2 adicional quando o limite máximo de fluxo simultâneo for atingido, em vez de aguardar o próximo fluxo disponível em uma conexão existente.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**RECURSO \_ HABILITAR OPÇÃO WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Define um valor inteiro longo sem sinal que especifica os recursos atualmente habilitados. Pode ser um dos valores a seguir.

| Termo | Descrição |
|-|-|
| <span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ ENABLE \_ SSL \_ REVERT \_ IMPERSONATION | Se habilitada, o WinHTTP reverte temporariamente a representação do cliente durante as operações de autenticação de certificado SSL. Esse valor pode ser definido somente no alça de sessão. |
| <span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP \_ \_ HABILITAR \_ REVOGAÇÃO DE SSL | Se habilitada, o WinHTTP permite a revogação de SSL. Esse valor pode ser definido somente no alça de solicitação. |


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**OPÇÃO WINHTTP \_ \_ HABILITAR \_ PROTOCOLO HTTP \_**
</dt> <dd> <dl> <dt>



Define uma máscara de bits DWORD de versões HTTP avançadas aceitáveis. Os valores possíveis são:

| Termo | Descrição |
|-|-|
| <span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>SINALIZADOR DE PROTOCOLO WINHTTP \_ \_ \_ HTTP2 (0x1) | Habilita HTTP/2 para a solicitação. |
| Nenhum (0x0) | Restringe a solicitação a HTTP/1.1 e anterior. |

As versões herdadas do HTTP (1.1 e anteriores) não podem ser desabilitadas usando essa opção. O padrão é 0x0.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**OPÇÃO WINHTTP \_ ENABLE \_ \_ HTTP2 \_ PLUS CLIENT \_ \_ CERT**
</dt> <dd> <dl> <dt>


Essa opção pode ser definida em um handle de sessão WinHttp para permitir que o WinHttp use o contexto de certificado do cliente fornecido pelo chamador quando HTTP/2 estiver sendo usado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**OPÇÃO WINHTTP \_ \_ ENABLETRACING**
</dt> <dd> <dl> <dt>



Define um **valor BOOL** que especifica se o rastreamento está habilitado no momento. Para obter mais informações sobre o recurso de rastreamento no WinHTTP, consulte [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md). Essa opção só pode ser definida em um handle  **HINTERNET NULL.**


</dt> </dl> </dd>

<dt>

<span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**CODIFICAR EXTRA DA OPÇÃO WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Habilita a codificação de porcentagem de URL para caminho e cadeia de caracteres de consulta.

Como alternativa, você pode codificar por porcentagem antes de chamar WinHttp.

</dt> </dl> </dd>

<dt>

<span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**WINHTTP \_ OPTION \_ EXPIRE \_ CONNECTION**
</dt> <dd> <dl> <dt>



Essa opção só pode ser definida em um handle de solicitação que ainda esteja ativo (envio ou recebimento). Definir essa opção dirá ao WinHttp para parar de atender às solicitações na conexão associada ao handle de solicitação passado. A conexão será fechada depois que o lidar com a solicitação com a qual essa opção é chamada for concluída. Essa opção não tem parâmetros.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**ERRO ESTENDIDO DA OPÇÃO WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera um valor inteiro longo sem sinal que contém um código de erro do Microsoft Windows Sockets mapeado para as mensagens de erro ERROR WINHTTP retornadas pela última vez neste \_ \_ \* contexto de thread. Você pode passar **NULL** como o valor do handle.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**CREDS DE \_ \_ PROXY GLOBAL DA \_ OPÇÃO WINHTTP \_**
</dt> <dd> <dl> <dt>



Leva um ponteiro para uma [**estrutura WINHTTP \_ CREDS \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) com o *parâmetro de função hInternet* definido como **NULL.** Essa opção requer a chave do Registro **HKLM \\ Software Microsoft Windows \\ \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp.** Se essa chave do Registro não estiver definida, WinHTTP retornará o **erro \_ ERRO WINHTTP \_ INVALID \_ OPTION**. Essa chave do Registro não está presente por padrão. Quando estiver definido, o WinINet enviará credenciais para WinHTTP. Sempre que o WinHttp receber um desafio de autenticação e se não houver credenciais definidas no alçamento atual, ele usará as credenciais fornecidas pelo WinINet. Para compartilhar credenciais de servidor, além de credenciais de proxy, os usuários precisam definir **WINHTTP \_ OPTION USE GLOBAL SERVER \_ \_ \_ \_ CREDENTIALS** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**CREDS DE SERVIDOR GLOBAL DA OPÇÃO WINHTTP \_ \_ \_ \_**
</dt> <dd> <dl> <dt>



Leva um ponteiro para uma [**estrutura WINHTTP \_ CREDS \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) com o *parâmetro de função hInternet* definido como **NULL.** Essa opção requer a chave do Registro **HKLM \\ Software Microsoft Windows \\ \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp.** Se essa chave do Registro não estiver definida, WinHTTP retornará o **erro \_ ERRO WINHTTP \_ INVALID \_ OPTION**. Essa chave do Registro não está presente por padrão. Quando estiver definido, o WinINet enviará credenciais para WinHTTP. Sempre que o WinHttp receber um desafio de autenticação e se não houver credenciais definidas no alçamento atual, ele usará as credenciais fornecidas pelo WinINet. Para compartilhar credenciais de servidor, além de credenciais de proxy, os usuários precisam definir **WINHTTP \_ OPTION USE GLOBAL SERVER \_ \_ \_ \_ CREDENTIALS** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**TIPO DE \_ IDENTIFICADOR DE OPÇÃO WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera um valor inteiro longo sem sinal que contém o tipo do identificador [HINTERNET](hinternet-handles-in-winhttp.md) passado. O valor de retorno pode ser um dos seguintes:

| Termo | Descrição |
|-|-|
| <span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>TIPO DE IDENTIFICADOR WINHTTP \_ \_ \_ CONNECT | O handle é um alça de conexão. |
| <span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>SOLICITAÇÃO DE TIPO \_ DE \_ IDENTIFICADOR WINHTTP \_ | O handle é um alça de solicitação. |
| <span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>SESSÃO DE TIPO \_ DE \_ IDENTIFICADOR WINHTTP \_ | O handle é um alça de sessão. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**WINHTTP \_ OPTION \_ HTTP \_ PROTOCOL \_ REQUIRED**
</dt> <dd> <dl> <dt>



Impede que versões de protocolo diferentes daquelas habilitadas por **WINHTTP \_ OPTION ENABLE HTTP \_ \_ \_ PROTOCOL** seja usada para a solicitação.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**WINHTTP \_ OPTION \_ HTTP \_ PROTOCOL \_ USED**
</dt> <dd> <dl> <dt>



Obtém um DWORD que indica qual versão HTTP avançada foi usada em uma determinada solicitação. Para ver uma lista de valores possíveis, consulte **WINHTTP \_ OPTION ENABLE HTTP \_ \_ \_ PROTOCOL**.



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**WINHTTP \_ OPTION \_ HTTP \_ VERSION**
</dt> <dd> <dl> <dt>



Define ou recupera uma estrutura [**HTTP \_ VERSION \_ INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) que contém a versão HTTP com suporte. Essa é uma opção em todo o processo; use **NULL** para o handle.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**WINHTTP \_ OPTION \_ HTTP2 \_ KEEPALIVE**
</dt> <dd> <dl> <dt>


Essa opção pode ser definida em um alça de sessão para que o WinHttp use quadros PING HTTP/2 como um mecanismo keepalive. Os chamadores especificam um tempo máximo em milissegundos e, depois que não houver nenhuma atividade em uma conexão para esse período de tempo de tempo, o WinHttp começará a enviar quadros PING HTTP/2. Os chamadores não podem definir um valor de tempo acima de 5.000 milissegundos.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**\_Opção WinHTTP \_ HTTP2 \_ mais \_ codificação de transferência \_**
</dt> <dd> <dl> <dt>


Essa opção pode ser definida em um identificador de solicitação WinHttp para controlar como o WinHttp se comporta quando uma resposta HTTP/2 contém um cabeçalho "transferência-codificação". Nesse caso, o WinHttp retornará um erro se essa opção for definida como **false**.


</dt> </dl> </dd> <dt>


<span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**\_opção WinHTTP \_ ignorar \_ \_ revogação de certificado \_ offline**
</dt> <dd> <dl> <dt>



Permite conexões seguras para usar certificados de segurança para os quais a lista de certificados revogados não pôde ser baixada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**\_Opção WinHTTP \_ IPv6 \_ Fast \_ FALLBACK**
</dt> <dd> <dl> <dt>



Habilita o fallback rápido IPv6 (mais feliz olhos) para a conexão. Esse comportamento é semelhante ao comportamento feliz olhos descrito na [RFC 6555](https://tools.ietf.org/html/rfc6555) para melhorar os tempos de conexão em redes em que o IPv6 não é confiável.
- Se os endereços IPv6 e IPv4 forem resolvidos para um determinado host, o WinHttp será iniciado conectando-se ao primeiro endereço IPv6 resolvido com um tempo limite curto (300 MS).
- Se essa conexão falhar, o WinHttp tentará se conectar ao primeiro endereço IPv4 resolvido com o tempo limite padrão.
- Se a segunda conexão falhar, o WinHttp tentará novamente o primeiro endereço IPv6 resolvido com o tempo limite padrão.
- Se a terceira conexão falhar, o WinHttp reverterá para o comportamento padrão de todos os endereços restantes, tentando uma conexão com cada um com o tempo limite padrão até que uma conexão seja estabelecida ou nenhum endereço permaneça.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**a \_ opção WinHTTP \_ é uma resposta de \_ conexão de proxy \_ \_**
</dt> <dd> <dl> <dt>



Obtém se uma resposta de conexão de retorno de proxy pode ou não ser recuperada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**Opção de WINHTTP \_ \_ Max \_ Conns \_ por \_ servidor de 1 \_ 0 \_**
</dt> <dd> <dl> <dt>



Define ou recupera um valor inteiro longo sem sinal que contém o número máximo de conexões permitidas por servidor HTTP/1.0. O valor padrão é **infinito**.

**Windows Vista com SP1 e Windows Server 2008:** Este sinalizador é obsoleto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**opção de WINHTTP \_ \_ Max \_ Conns \_ por \_ servidor**
</dt> <dd> <dl> <dt>



Define ou recupera um valor inteiro longo sem sinal que contém o número máximo de conexões permitidas por servidor. O valor padrão é **infinito**.

Quando essa opção é definida como zero, o WinHTTP define o limite no número de conexões como 2.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**opção WINHTTP máx. de \_ \_ \_ \_ redirecionamentos automáticos de http \_**
</dt> <dd> <dl> <dt>



Define o número máximo de redirecionamentos que o WinHTTP segue; o padrão é 10. Esse limite impede que sites não autorizados façam a pausa do cliente WinHTTP após um grande número de redirecionamentos.

**Windows XP com SP1 e windows 2000 com SP3:** Este sinalizador é obsoleto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**\_máximo de \_ status HTTP da opção WinHTTP \_ \_ \_ continuar**
</dt> <dd> <dl> <dt>



O número máximo de respostas de código de status 100-199 informativas ignoradas antes de retornar o código de status final para o cliente WinHTTP. Os códigos de status informativos 100-199 podem ser enviados pelo servidor antes do código de status final e são descritos na especificação para HTTP/1.1 (para obter mais informações, consulte [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)). O padrão é 10.

**Windows XP com SP1 e windows 2000 com SP3:** Este sinalizador é obsoleto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**\_tamanho de \_ \_ dreno de resposta máx da opção \_ WinHTTP \_**
</dt> <dd> <dl> <dt>



Um limite na quantidade de dados drenados de respostas para reutilizar uma conexão, especificada em bytes. O padrão é 1MB.

**Windows XP com SP1 e windows 2000 com SP3:** Este sinalizador é obsoleto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**\_ \_ tamanho máximo do \_ cabeçalho de resposta da \_ opção WinHTTP \_**
</dt> <dd> <dl> <dt>



Um conjunto associado no tamanho máximo da parte do cabeçalho da resposta do servidor, especificado em bytes. Essa ligação protege o cliente de um servidor não autorizado tentando paralisar o cliente enviando uma resposta com uma quantidade infinita de dados de cabeçalho. O valor padrão é 64 KB.

**Windows XP com SP1 e windows 2000 com SP3:** Este sinalizador é obsoleto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**\_ \_ identificador pai da opção WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera o identificador pai para esse identificador.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**opção WINHTTP de \_ \_ \_ texto de comarcação do Passport \_**
</dt> <dd> <dl> <dt>



Recupera uma cadeia de caracteres que contém o texto de [*comarcação*](glossary.md) fornecido pelo servidor de logon do Passport. Essa opção deve ser recuperada imediatamente após o servidor de logon responder com um código de status 401. Um aplicativo deve passar um tamanho de buffer, em bytes, que seja grande o suficiente para manter a cadeia de caracteres retornada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**\_URL de \_ \_ comarcação do passaporte da opção WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera uma cadeia de caracteres que contém uma URL para um gráfico de [*comarcação*](glossary.md) fornecido pelo servidor de logon do Passport. Essa opção deve ser recuperada imediatamente após o servidor de logon responder com um código de status 401. Um aplicativo deve passar um tamanho de buffer, em bytes, que seja grande o suficiente para manter a cadeia de caracteres retornada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**\_opção WinHTTP \_ URL de retorno do Passport \_ \_**
</dt> <dd> <dl> <dt>



Define uma opção somente leitura em um identificador de solicitação que recupera a URL de retorno do Passport.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**opção WINHTTP sair do \_ \_ Passport \_ \_**
</dt> <dd> <dl> <dt>



Define a opção em um identificador de sessão para sair de quaisquer logons do Passport. Um aplicativo deve passar na URL de retorno do Passport que foi recuperada com a **\_ opção WinHTTP URL de \_ \_ retorno \_ do Passport**. Todos os cookies relacionados à URL de retorno são apagados.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**\_senha da opção WinHTTP \_**
</dt> <dd> <dl> <dt>



Define ou recupera um valor de cadeia de caracteres que contém a senha associada a um identificador de solicitação.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**\_proxy de opção WinHTTP \_**
</dt> <dd> <dl> <dt>



Define ou recupera uma estrutura de [**\_ \_ informações de proxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) que contém os dados de proxy em um identificador de sessão existente ou identificador de solicitação. Ao recuperar dados de proxy, um aplicativo deve liberar as cadeias de caracteres **lpszProxy** e **lpszProxyBypass** contidas nessa estrutura (se elas não forem **nulas**) usando a função [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) . Um aplicativo pode consultar os dados do proxy global (o proxy padrão) passando um identificador **nulo** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**\_senha do \_ proxy da opção WinHTTP \_**
</dt> <dd> <dl> <dt>



Define ou recupera um valor de cadeia de caracteres que contém a senha usada para acessar o proxy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**SPN de proxy de opção de WINHTTP \_ \_ \_ \_ usado**
</dt> <dd> <dl> <dt>



Obtém o nome da entidade de segurança do servidor proxy que o WinHTTP forneceu ao SSPI durante a autenticação. Esse valor de cadeia de caracteres é usefor passando para [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) após uma falha de autenticação.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**\_nome de \_ usuário do proxy de opção WinHTTP \_**
</dt> <dd> <dl> <dt>



Define ou recupera um valor de cadeia de caracteres que contém o nome de usuário usado para acessar o proxy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**\_tamanho do \_ buffer de leitura da opção WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Esta opção foi preterida; Ele não tem nenhum efeito.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**a \_ opção \_ WinHTTP \_ recebe \_ resposta de conexão proxy \_**
</dt> <dd> <dl> <dt>



Define se a entidade de resposta de proxy pode ou não ser recuperada. Essa opção está desabilitada por padrão.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**a \_ opção \_ WinHTTP \_ recebe \_ tempo limite de resposta**
</dt> <dd> <dl> <dt>



Define ou recupera um valor inteiro longo sem sinal que contém o valor de tempo limite, em milissegundos, para aguardar a recepção de todos os cabeçalhos de resposta a uma solicitação. Se o WinHTTP não receber todos os cabeçalhos dentro desse período de tempo limite, a solicitação será cancelada. O valor de tempo limite padrão é 90 segundos.

Esse tempo limite é verificado somente quando os dados são recebidos do soquete. Como resultado, quando o tempo limite expira, o aplicativo cliente não é notificado até que mais dados cheguem do servidor. Se nenhum dado chega do servidor, o atraso entre a expiração do tempo limite e a notificação do aplicativo cliente pode ser tão grande quanto o valor de tempo limite definido usando o parâmetro *dwReceiveTimeout* da função [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**\_ \_ tempo limite de recebimento da opção WinHTTP \_**
</dt> <dd> <dl> <dt>



Define ou recupera um valor inteiro longo sem sinal que contém o valor de tempo limite, em milissegundos, para receber uma resposta parcial a uma solicitação ou ler alguns dados. Se a resposta demorar mais do que esse valor de tempo limite, a solicitação será cancelada. O valor do tempo limite padrão é de 30 segundos.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**\_política de \_ redirecionamento de opção WinHTTP \_**
</dt> <dd> <dl> <dt>



Define o comportamento do WinHTTP em relação ao tratamento de um código de status de redirecionamento HTTP 30 vezes. Essa opção pode ser definida em uma sessão ou identificador de solicitação para um dos seguintes valores:

| Termo | Descrição |
|-|-|
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>\_política de \_ redirecionamento de opção de WinHTTP \_ \_ sempre | Todos os redirecionamentos são seguidos automaticamente. |
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>\_ \_ a política de redirecionamento de opção WinHTTP não \_ \_ permite \_ https \_ para \_ http | Todos os redirecionamentos são seguidos, exceto aqueles que se originam de uma URL segura (https) para uma URL não segura (http). Essa é a configuração padrão. |
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>\_política de \_ redirecionamento de opção WinHTTP \_ \_ nunca | Redirecionamentos nunca são seguidos. O status de 30 vezes é retornado para o aplicativo. |


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**a \_ opção WinHTTP \_ rejeita \_ USERPWD \_ na \_ URL**
</dt> <dd> <dl> <dt>



Rejeita URLs que contêm um nome de usuário e senha. Essa opção também rejeita URLs que contêm a semântica de *nome de usuário: senha* , mesmo que nenhum nome de usuário ou senha seja especificado. Por exemplo, " u:p@hostname ", " :@hostname ", " u:@hostname " e " :p@hostname " todos seriam sinalizados como inválidos. Se uma URL inválida for passada para a função, ela retornará o [erro \_ WinHTTP \_ Invalid \_ URL](error-messages.md). Essa opção é desativada por padrão.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**\_prioridade de \_ solicitação de opção de WinHTTP \_**
</dt> <dd> <dl> <dt>



Esta opção foi preterida; Ele não tem nenhum efeito.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**\_Estatísticas de \_ solicitação de opção de WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera estatísticas para a solicitação.  Para obter uma lista das estatísticas disponíveis, consulte [**\_ \_ Estatísticas de solicitação do WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**\_tempos de \_ solicitação de opção de WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera informações de tempo para a solicitação. Para obter uma lista dos intervalos disponíveis, confira [**\_ \_ tempos de solicitação do WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**a \_ opção \_ WinHTTP \_ requer \_ fim de fluxo**
</dt> <dd> <dl> <dt>


Essa opção informa ao WinHttp para ignorar cabeçalhos de resposta de "comprimento de conteúdo" e continuar recebendo em um fluxo até que o sinalizador de END_STREAM seja recebido.



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**\_ \_ nome do host de resolução de opção WinHTTP \_**
</dt> <dd> <dl> <dt>


Essa opção pode ser definida em um identificador de solicitação WinHttp antes de ser enviada. Se definido, o WinHttp usará a cadeia de caracteres fornecida pelo chamador como o nome do host para a resolução DNS.



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**\_opção WinHTTP \_ resolver \_ tempo limite**
</dt> <dd> <dl> <dt>



Define ou recupera um valor inteiro longo sem sinal que contém o valor de tempo limite, em milissegundos, para resolver um nome de host. O valor de tempo limite padrão é **infinito**. Se um valor não padrão for especificado, haverá uma sobrecarga de uma criação de thread por resolução de nomes.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**\_protocolos de \_ segurança de opção WinHTTP \_**
</dt> <dd> <dl> <dt>



Define um valor inteiro longo sem sinal que especifica quais protocolos seguros são aceitáveis. Por padrão, somente SSL3 e TLS1 são habilitados no Windows 7 e no Windows 8. Por padrão, somente SSL3, TLS 1.0, TLS 1.1 e TLS 1.2 estão habilitados no Windows 8.1 e no Windows 10. O valor pode ser uma combinação de um ou mais dos valores a seguir.

| Termo | Descrição |
|-|-|
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>\_sinalizador WinHTTP \_ - \_ \_ todos os protocolos seguros | Os protocolos protocolo SSL (SSL) 2,0, SSL 3,0 e protocolo TLS 1,0 podem ser usados. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>\_Sinalizador WinHTTP \_ \_ SSL2 protocolo \_ seguro | O protocolo SSL 2,0 pode ser usado. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>\_Sinalizador WinHTTP \_ \_ SSL3 protocolo \_ seguro | O protocolo SSL 3,0 pode ser usado. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>\_Sinalizador WinHTTP \_ \_ TLS1 protocolo \_ seguro | O protocolo TLS 1,0 pode ser usado. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>Sinalizador WINHTTP de \_ \_ protocolo de segurança \_ \_ TLS1 \_ 1 | O protocolo TLS 1,1 pode ser usado. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>Sinalizador WINHTTP de \_ \_ protocolo de segurança \_ \_ TLS1 \_ 2 | O protocolo TLS 1,2 pode ser usado. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**\_estrutura do \_ certificado de segurança da opção WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera o certificado para um servidor SSL/TLS na estrutura [**de \_ \_ informações do certificado WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) . O aplicativo deve liberar os membros **lpszSubjectInfo** e **lpszIssuerInfo** com [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**\_sinalizadores de \_ segurança da opção WinHTTP \_**
</dt> <dd> <dl> <dt>



Define ou recupera um valor inteiro longo sem sinal que contém os sinalizadores de segurança para um identificador. Pode ser uma combinação desses valores:

| Termo | Descrição |
|-|-|
| <span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>sinalizador de segurança \_ \_ ignorar \_ certificado \_ CN \_ inválido |Permite um nome comum inválido em um certificado; ou seja, o nome do servidor especificado pelo aplicativo não corresponde ao nome comum no certificado. Se esse sinalizador for definido, o aplicativo não receberá um retorno de chamada do **sinalizador de status de retorno de chamada do WinHTTP \_ \_ \_ \_ \_ CN \_ inválido** . |
| <span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>sinalizador de segurança \_ \_ ignorar \_ data de certificado \_ \_ inválida |Permite uma data de certificado inválida, ou seja, um certificado expirado ou ainda não efetivo. Se esse sinalizador for definido, o aplicativo não receberá um retorno de chamada de **certificado de sinalizador de status de retorno de chamada de \_ \_ \_ \_ \_ dados \_ inválido** . |
| <span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>sinalizador de segurança \_ \_ ignorar \_ \_ AC desconhecida | Permite uma autoridade de certificação inválida. Se esse sinalizador for definido, o aplicativo não receberá um sinalizador de status de retorno de chamada do WinHTTP com retorno de chamada de **\_ \_ \_ \_ \_ AC inválido** . |
| <span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>sinalizador de segurança \_ \_ ignorar \_ \_ uso incorreto do certificado \_ | Permite que a identidade de um servidor seja estabelecida com um certificado que não seja de servidor (por exemplo, um certificado de cliente). |
| <span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>sinalizador de segurança \_ \_ ignorar \_ \_ assinatura fraca | Permite que uma assinatura fraca seja ignorada.<br/>Esse sinalizador está disponível na atualização cumulativa para cada sistema operacional, começando com o Windows 7 e o Windows Server 2008 R2. |
| <span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>sinalizador de segurança \_ \_ seguro | Usa transferências seguras. Isso só é retornado em uma chamada para [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption). |
| <span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>\_ \_ nível médio do sinalizador de segurança \_ | Usa a criptografia média (56 bits). Isso só é retornado em uma chamada para [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption). |
| <span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>\_ \_ forte força do sinalizador de segurança \_ | Usa criptografia forte (128 bits). Isso só é retornado em uma chamada para [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption). |
| <span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>intensidade de sinalizador de segurança \_ \_ \_ fraca | Usa criptografia fraca (40 bits). Isso só é retornado em uma chamada para [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption). |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**\_informações de \_ segurança da opção WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera a conexão SChannel e as informações de codificação para uma solicitação.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**chave de segurança de bit de bits de opção de WINHTTP \_ \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera um valor inteiro longo sem sinal que contém a intensidade de codificação da chave de criptografia. Um número maior indica criptografia de intensidade de codificação mais forte.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**\_ \_ tempo limite de envio da opção WinHTTP \_**
</dt> <dd> <dl> <dt>



Define ou recupera um valor inteiro longo sem sinal que contém o valor de tempo limite, em milissegundos, para enviar uma solicitação ou gravar alguns dados. Se o envio da solicitação demorar mais do que o tempo limite, a operação enviar será cancelada. O tempo limite padrão é de 30 segundos.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**\_CBT de \_ servidor de opção WinHTTP \_**
</dt> <dd> <dl> <dt>



Obtém um ponteiro para a estrutura de [**\_ associações SecPkgContext**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) que especifica um token de associação de canal (CBT).

Um token de associação de canal é uma propriedade de um canal de transporte seguro e é usado para associar um canal de autenticação ao canal de transporte seguro. Esse token só pode ser obtido por essa opção depois que uma conexão SSL é estabelecida.

> [!Note]
> Passar essa opção e um valor **nulo** para *lpBuffer* para [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) retornará \_ o buffer insuficiente de erro \_ e o tamanho de byte necessário para o buffer no parâmetro *lpdwBufferLength* . Esse valor de tamanho de buffer retornado pode ser passado em uma chamada subsequente para consulta para o token de associação de canal. Essas etapas são necessárias ao manipular \_ \_ a solicitação de status de retorno de chamada WinHTTP \_ se você quiser modificar cabeçalhos de solicitação com base no token de associação de canal. Observe que o Windows XP e o vista não dão suporte à modificação de cabeçalhos de solicitação durante esse retorno de chamada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**\_contexto da \_ cadeia de certificados do servidor de opção WinHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera o contexto da cadeia de certificação do servidor. **WinHTTP \_ O \_ \_ contexto de \_ cadeia \_ de certificados de servidor de opção** pode ser passado para obter um ponteiro duplicado para o **\_ \_ contexto da cadeia** de certificados para uma cadeia de certificados de servidor recebida durante uma conexão SSL negociada. O cliente deve chamar [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) no ponteiro de contexto PCCERT retornado \_ que é preenchido no buffer.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**\_contexto de \_ certificado de servidor de opção WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera o contexto de certificação do servidor. **WinHTTP \_ O \_ \_ \_ contexto de certificado de servidor de opção** pode ser passado para obter um ponteiro DUPLICAdo para o [**contexto**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) de certificado para um certificado de servidor recebido durante uma conexão SSL negociada. O cliente deve chamar [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) no ponteiro de contexto PCCERT retornado \_ que é preenchido no buffer.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**\_SPN de servidor de opção WinHTTP \_ \_ \_ usado**
</dt> <dd> <dl> <dt>



Obtém o nome principal do servidor do servidor que o WinHTTP forneceu ao SSPI durante a autenticação. Esse valor de cadeia de caracteres pode ser passado para [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) após uma falha de autenticação.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**\_SPN da opção WinHTTP \_**
</dt> <dd> <dl> <dt>



Inclui ou remove o número da porta do servidor quando o SPN (nome da entidade de serviço) é criado para Kerberos ou negociar autenticação Kerberos. Esse sinalizador é um dos seguintes valores:

| Termo | Descrição |
|-|-|
| <span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP \_ desabilitar \_ \_ porta do servidor SPN \_ | Remove o número da porta do servidor. |
| <span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>\_ \_ \_ porta do servidor SPN habilitar WinHTTP \_ | Inclui o número da porta do servidor. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**\_código de \_ erro de fluxo de opção WinHTTP \_ \_**
</dt> <dd> <dl> <dt>


Essa opção pode ser consultada em um identificador de solicitação WinHttp e retornará o código de erro indicado por um quadro de RST_STREAM recebido em um fluxo HTTP.



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**\_opção WinHTTP \_ TCP \_ Fast \_ aberta**
</dt> <dd> <dl> <dt>



Habilita o TCP Fast Open para a conexão.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**\_opção WinHTTP \_ TCP \_ KeepAlive**
</dt> <dd> <dl> <dt>



Essa opção pode ser definida em um identificador de sessão do WinHttp para habilitar o comportamento Keep-Alive TCP no soquete subjacente. Usa um struct [**TCP \_ KeepAlive**](/windows/win32/winsock/sio-keepalive-vals) .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**\_ \_ Início falso de TLS da opção WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Habilita o início falso do TLS para a conexão.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**\_opção WinHTTP \_ protocolo TLS de \_ \_ FALLBACK inseguro \_**
</dt> <dd> <dl> <dt>



Essa opção pode ser definida em um identificador de sessão do WinHttp para controlar se o fallback para TLS 1,0 será permitido se houver uma falha de handshake de TLS com uma versão de protocolo mais nova.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**\_evento de \_ notificação de descarregamento da opção WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Assume um evento que será definido quando o último retorno de chamada for concluído para uma sessão específica. Esse sinalizador deve ser usado em um identificador de sessão. O evento não pode ser fechado até que tenha sido definido pelo WinHTTP.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**\_opção WinHTTP \_ análise de \_ cabeçalho não seguro \_**
</dt> <dd> <dl> <dt>



Essa opção é reservada para uso interno e não deve ser chamada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**\_opção \_ de WinHTTP atualizar para o \_ \_ soquete da Web \_**
</dt> <dd> <dl> <dt>



Instrui a pilha para iniciar um processo de handshake do WebSocket com [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). Essa opção não usa parâmetros.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**\_URL da opção WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera um valor de cadeia de caracteres que contém a URL completa de um recurso baixado. Se a URL original contiver dados adicionais, como cadeias de caracteres de pesquisa ou âncoras, ou se a chamada tiver sido redirecionada, a URL retornada será diferente da original. O aplicativo deve passar um buffer, dimensionado em bytes, que é grande o suficiente para manter a URL retornada em caracteres largos.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**\_opção WinHTTP \_ usar \_ \_ credenciais do servidor global \_**
</dt> <dd> <dl> <dt>



Usa um **bool** e pode ser definido apenas como um identificador de sessão. Ele só se propagará para os identificadores criados a partir do identificador de sessão depois que a opção tiver sido definida. Se **for true**, essa opção fará com que o último recurso use as credenciais do servidor global que foram enviadas do Wininet. O padrão para essa opção é **false**. Essa opção requer a chave do registro **HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings! ShareCredsWithWinHttp**. Essa chave do registro não está presente por padrão. Quando definido, o WinINet enviará as credenciais para o WinHTTP. Sempre que o WinHttp obtiver um desafio de autenticação e se não houver nenhuma credencial definida no identificador atual, ele usará as credenciais fornecidas pelo WinINet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**\_agente do \_ usuário da opção WinHTTP \_**
</dt> <dd> <dl> <dt>



Define ou recupera a cadeia de caracteres do [*agente do usuário*](glossary.md) nos identificadores fornecidos pelo [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) e usado em funções [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) subsequentes, desde que ele não seja substituído por um cabeçalho adicionado por [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) ou **WinHttpSendRequest**. Ao recuperar um agente do usuário, o aplicativo deve passar um buffer, dimensionado em bytes, que é grande o suficiente para manter a URL retornada em caracteres largos. Ao definir o agente do usuário, o tamanho do buffer é o comprimento da cadeia de caracteres, em valores, mais o terminador **nulo** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**nome de usuário da \_ opção WinHTTP \_**
</dt> <dd> <dl> <dt>



Define ou recupera uma cadeia de caracteres que contém o nome de usuário.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**\_ \_ \_ \_ tempo limite de fechamento de soquete da Web de opção WinHTTP \_**
</dt> <dd> <dl> <dt>



Define o tempo, em milissegundos, que [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) deve aguardar para concluir o handshake de fechamento. O padrão é 10 segundos.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**\_intervalo de \_ KeepAlive de soquete da Web de opção WinHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Define o intervalo, em milissegundos, para enviar um pacote Keep-Alive pela conexão. O intervalo padrão é 30000 (30 segundos). O intervalo mínimo é 15000 (15 segundos). Usar [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) para definir um valor inferior a 15000 retornará com um **\_ \_ parâmetro de erro inválido**.

> [!Note]
> O valor padrão para **a \_ opção \_ WinHTTP \_ \_ \_ intervalo de KeepAlive do soquete da Web** é lido em **HKLM: \\ software \\ Microsoft \\ WebSocket \\ KeepaliveInterval**. Se um valor não for definido, o valor padrão de 30000 será usado. Não é possível ter um intervalo de KeepAlive inferior a 15000 milissegundos.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**\_opção WinHTTP \_ \_ tamanho do \_ buffer de recebimento de soquete da \_ Web \_**
</dt> <dd> <dl> <dt>



Define ou recupera um DWORD que especifica o tamanho do buffer de recebimento a ser usado em conexões WebSocket.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**\_opção WinHTTP \_ \_ tamanho do \_ buffer de envio de soquete da \_ Web \_**
</dt> <dd> <dl> <dt>



Define ou recupera um DWORD que especifica o tamanho do buffer de envio a ser usado em conexões WebSocket.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**\_opção WinHTTP \_ \_ contagem de threads de trabalho \_**
</dt> <dd> <dl> <dt>



Define um valor inteiro longo sem sinal que especifica o número de threads de trabalho que o pool de threads deve usar para conclusões assíncronas. O valor padrão dessa opção é zero, que especifica que o número de threads de trabalho é igual ao número de CPUs no sistema. Essa opção só pode ser definida em um identificador [HINTERNET](hinternet-handles-in-winhttp.md) **nulo** antes que uma operação assíncrona tenha ocorrido.   Essa opção só pode ser definida uma vez.

**Windows Server 2008 R2 e Windows 7:** Este sinalizador é obsoleto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**\_tamanho do \_ buffer de gravação da opção WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Esta opção foi preterida; Ele não tem nenhum efeito.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

A tabela a seguir lista os sinalizadores de opção especificando em quais identificadores eles podem atuar, se eles podem ser consultados e definidos e o tipo de dados usado. Um "X" indica que o sinalizador de opção é válido para uso com a função ou o identificador, enquanto um "-" especifica que o sinalizador de opção é inválido.

A tentativa de definir ou consultar um sinalizador de opção em uma versão do Windows em que não tem suporte resultará na **\_ \_ \_ opção erro WinHTTP inválido**.

| Sinalizador de opção e tipo de dados | Identificador de sessão | Identificador de solicitação | Opção de consulta | Opção Set | Versão mínima do Windows |
|-|-|-|-|-|-|
| \_opção WinHTTP \_ garantindo \_ \_ \_ retornos de chamada sem bloqueio<br/>**BOOL** | X | \- | \- | X | \- |
| política de WINHTTP da \_ opção de \_ logon automático \_<br/>**DWORD** | \- | X | \- | X | \- |
| retorno de chamada de \_ opção WinHTTP \_<br/>**LPVOID** | X | X | X | X | \- |
| \_contexto de \_ certificado de cliente de opção WinHTTP \_ \_<br/>[**contexto do certificado \_**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | X | \- | X | Windows Vista |
| LISTA DO EMISSOR DO CERTIFICADO \_ \_ DO \_ CLIENTE \_ \_ WINHTTP OPTION<br/>[**IssuerListInfoEx de SecPkgContext \_**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | X | X | \- | Windows Vista |
| PÁGINA DE CÓDIGO DA OPÇÃO WINHTTP \_ \_<br/>**DWORD** | X | \- | \- | X | \- |
| OPÇÃO WINHTTP \_ \_ CONFIGURAR O PASSPORT \_ \_ AUTH<br/>**DWORD** | X | \- | \- | X | \- |
| WINHTTP \_ OPTION \_ CONNECT \_ RETRIES<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP \_ OPTION \_ CONNECT \_ TIMEOUT<br/>**DWORD** | X | X | X | X | \- |
| INFORMAÇÕES DE CONEXÃO DA OPÇÃO WINHTTP \_ \_ \_<br/>[**INFORMAÇÕES DE CONEXÃO \_ \_ WINHTTP**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | X | X | \- | \- |
| ESTATÍSTICAS DE CONEXÃO DA OPÇÃO WINHTTP \_ \_ \_ \_ V0<br/>[**TCP \_ INFO \_ v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | X | X | \- | Windows 10 versão 1903 |
| ESTATÍSTICAS DE CONEXÃO DA OPÇÃO WINHTTP \_ \_ \_ \_ V1<br/>[**TCP \_ INFO \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | X | X | \- | Windows 10 versão 2004 |
| VALOR DE CONTEXTO DA OPÇÃO WINHTTP \_ \_ \_<br/>**DWORD \_ PTR** | X | X | X | X | \- |
| DESCOMPACTAÇÃO DA OPÇÃO WINHTTP \_ \_<br/>**DWORD** | X | X | \- | X | Windows 8.1 |
| RECURSO DESABILITAR OPÇÃO WINHTTP \_ \_ \_<br/>**DWORD** | \- | X | \- | X | \- |
| OPÇÃO WINHTTP \_ \_ DESABILITAR \_ \_ FALLBACK DE \_ PROTOCOLO SEGURO<br/>**Bool** | X | \- | \- | X | Windows 10 versão 1903 |
| OPÇÃO WINHTTP \_ \_ DESABILITAR \_ FILA DE \_ FLUXO<br/>**Bool** | X | X | \- | X | Windows 10 versão 1809 |
| RECURSO \_ HABILITAR OPÇÃO WINHTTP \_ \_<br/>**DWORD** | \* | \* | \- | X | \- |
| OPÇÃO WINHTTP \_ \_ HABILITAR \_ PROTOCOLO HTTP \_<br/>**DWORD** | X | X | \- | X | Windows 10, versão 1607 |
| OPÇÃO WINHTTP \_ \_ HABILITAR \_ HTTP2 \_ MAIS CONTEXTO DE CERTIFICADO DO \_ \_ \_ CLIENTE<br/>**Bool** | X | \- | \- | X | Windows 10 versão 21H1 |
| OPÇÃO WINHTTP \_ \_ ENABLETRACING<br/>**DWORD** | \- | \- | X | X | \- |
| CODIFICAR EXTRA DA OPÇÃO WINHTTP \_ \_ \_<br/>**Bool** | X | X | \- | X | Windows 10 versão 1803 |
| WINHTTP \_ OPTION \_ EXPIRE \_ CONNECTION<br/>N/D | \- | X | \- | X | Windows 10 versão 1903 |
| ERRO ESTENDIDO DA OPÇÃO WINHTTP \_ \_ \_<br/>**DWORD** | X | X | X | \- | \- |
| CREDS DE \_ \_ PROXY GLOBAL DA \_ OPÇÃO WINHTTP \_<br/>[**WINHTTP \_ CREDS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | X | X | \- | X | \- |
| CREDS DE SERVIDOR GLOBAL DA OPÇÃO WINHTTP \_ \_ \_ \_<br/>[**WINHTTP \_ CREDS \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | X | X | \- | X | \- |
| TIPO DE \_ IDENTIFICADOR DE OPÇÃO WINHTTP \_ \_<br/>**DWORD** | X | X | X | \- | \- |
| WINHTTP \_ OPTION \_ HTTP \_ PROTOCOL \_ REQUIRED<br/>**Bool** | X | X | \- | X | Windows 10 versão 1903 |
| WINHTTP \_ OPTION \_ HTTP \_ PROTOCOL \_ USED<br/>**DWORD** | \- | X | X | \- | Windows 10, versão 1607 |
| WINHTTP \_ OPTION \_ HTTP \_ VERSION<br/>[**INFORMAÇÕES \_ DE VERSÃO \_ HTTP**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | X | X | X | X | \- |
| WINHTTP \_ OPTION \_ HTTP2 \_ KEEPALIVE<br/>**DWORD** | X | \- | \- | X | Windows 10 versão 21H1 |
| WINHTTP \_ OPTION \_ HTTP2 \_ PLUS \_ TRANSFER \_ ENCODING<br/>**Bool** | X | X | \- | X | Windows 10 versão 21H1 |
| OPÇÃO WINHTTP \_ \_ IGNORAR \_ \_ REVOGAÇÃO DE CERTIFICADO \_ OFFLINE<br/>**Bool** | \- | X | \- | X | Windows 10 versão 2004 |
| FALLBACK RÁPIDO \_ \_ DE IPV6 \_ DA OPÇÃO WINHTTP \_<br/>**Bool** | X | \- | \- | X | Windows 10 versão 1903 |
| A OPÇÃO \_ WINHTTP É PROXY CONNECT \_ \_ \_ \_ RESPONSE<br/>**Bool** | X | X | X | \- | \- |
| WINHTTP \_ OPTION \_ MAX \_ CONNS \_ PER \_ 1 \_ 0 \_ SERVER<br/>**DWORD** | X | \- | X | X | \- |
| OPÇÃO WINHTTP \_ \_ MAX \_ CONNS POR \_ \_ SERVIDOR<br/>**DWORD** | X | \- | X | X | \- |
| REDIRECIONAMENTOS \_ AUTOMÁTICOS \_ DE HTTP MÁXIMO DA \_ \_ \_ OPÇÃO WINHTTP<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP \_ OPTION \_ MAX \_ HTTP \_ STATUS \_ CONTINUE<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP \_ OPTION \_ MAX \_ RESPONSE \_ DRAIN \_ SIZE<br/>**DWORD** | X | X | X | X | \- |
| TAMANHO MÁXIMO \_ DO \_ \_ \_ HEADER DE RESPOSTA DA \_ OPÇÃO WINHTTP<br/>**DWORD** | X | X | X | X | \- |
| WINHTTP \_ OPTION \_ PARENT \_ HANDLE<br/>[Hinternet](hinternet-handles-in-winhttp.md) | X | X | X | \- | \- |
| WINHTTP \_ OPTION \_ PASSPORT \_ COBRANDING \_ TEXT<br/>**LPWSTR** | \- | X | X | \- | \- |
| \_URL de \_ \_ comarcação do passaporte da opção WinHTTP \_<br/>**LPWSTR** | \- | X | X | \- | \- |
| \_opção WinHTTP \_ URL de retorno do Passport \_ \_<br/>**LPVOID** | \- | X | X | \- | \- |
| opção WINHTTP sair do \_ \_ Passport \_ \_<br/>**LPVOID** | X | \- | \- | X | \- |
| \_senha da opção WinHTTP \_<br/>**LPWSTR** | \- | X | X | X | \- |
| \_proxy de opção WinHTTP \_<br/>[**\_informações de proxy WinHTTP \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | X | X | X | X | \- |
| \_senha do \_ proxy da opção WinHTTP \_<br/>**LPWSTR** | \- | X | X | X | \- |
| SPN de proxy de opção de WINHTTP \_ \_ \_ \_ usado<br/>**LPWSTR** | \- | X | X | \- | \- |
| \_nome de \_ usuário do proxy de opção WinHTTP \_<br/>**LPWSTR** | \- | X | X | X | \- |
| \_tamanho do \_ buffer de leitura da opção WinHTTP \_ \_<br/>**DWORD** | \- | X | X | X | \- |
| a \_ opção \_ WinHTTP \_ recebe \_ resposta de conexão proxy \_<br/>**BOOL** | X | X | \- | X | \- |
| a \_ opção \_ WinHTTP \_ recebe \_ tempo limite de resposta<br/>**DWORD** | X | X | X | X | \- |
| \_ \_ tempo limite de recebimento da opção WinHTTP \_<br/>**DWORD** | X | X | X | X | \- |
| \_política de \_ redirecionamento de opção WinHTTP \_<br/>**DWORD** | X | X | X | X | \- |
| a \_ opção WinHTTP \_ rejeita \_ USERPWD \_ na \_ URL<br/>**BOOL** | \- | X | \- | X | \- |
| \_prioridade de \_ solicitação de opção de WinHTTP \_<br/>**DWORD** | \- | X | X | X | \- |
| \_Estatísticas de \_ solicitação de opção de WinHTTP \_<br/>[**\_Estatísticas de solicitação de WinHTTP \_**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | X | X | \- | Windows 10 versão 1903 |
| \_tempos de \_ solicitação de opção de WinHTTP \_<br/>[**\_tempos de solicitação WinHTTP \_**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | X | X | \- | Windows 10 versão 1903 |
| a \_ opção \_ WinHTTP \_ requer \_ fim de fluxo<br/>**BOOL** | X | X | \- | X | Windows 10 versão 21H1 |
| \_ \_ nome do host de resolução de opção WinHTTP \_<br/>**LPWSTR** | \- | X | \- | X | Windows 10 versão 21H1 |
| \_opção WinHTTP \_ resolver \_ tempo limite<br/>**DWORD** | X | X | X | X | \- |
| PROTOCOLOS SEGUROS DA OPÇÃO WINHTTP \_ \_ \_<br/>**DWORD** | X | \- | \- | X | \- |
| STRUCT DO CERTIFICADO \_ \_ DE SEGURANÇA DA \_ OPÇÃO WINHTTP \_<br/>[**INFORMAÇÕES DE CERTIFICADO WINHTTP \_ \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | X | X | \- | \- |
| SINALIZADORES DE SEGURANÇA DA OPÇÃO WINHTTP \_ \_ \_<br/>**DWORD** | \- | X | X | X | \- |
| INFORMAÇÕES DE SEGURANÇA DA OPÇÃO WINHTTP \_ \_ \_<br/>[**WINHTTP_SECURITY_INFO**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | X | X | \- | Windows 10 versão 2004 |
| BITNESS \_ DA CHAVE \_ DE SEGURANÇA DA \_ \_ OPÇÃO WINHTTP<br/>**DWORD** | \- | X | X | \- | \- |
| WINHTTP \_ OPTION \_ SEND \_ TIMEOUT<br/>**DWORD** | X | X | X | X | \- |
| CBT DO \_ SERVIDOR DE OPÇÕES \_ \_ WINHTTP<br/>[**Vinculações SecPkgContext \_**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\* | \- | X | X | \- | \- |
| CONTEXTO DA CADEIA DE \_ \_ CERTIFICADOS \_ DO SERVIDOR WINHTTP OPTION \_ \_<br/>[**CERT_CHAIN_CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | X | X | \- | Windows 10 versão 2004 |
| CONTEXTO DE CERTIFICADO \_ DO \_ SERVIDOR WINHTTP OPTION \_ \_<br/>[**CONTEXTO DO CERTIFICADO**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | X | X | \- | \- |
| SPN DO \_ SERVIDOR DE OPÇÕES \_ \_ WINHTTP \_ USADO<br/>**Lpwstr** | \- | X | X | \- | \- |
| SPN DA \_ OPÇÃO \_ WINHTTP<br/>**DWORD** | \- | X | \- | X | \- |
| CÓDIGO DE ERRO DE FLUXO DE OPÇÃO WINHTTP \_ \_ \_ \_<br/>**DWORD** | \- | X | X | \- | Windows 10 versão 21H1 |
| WINHTTP \_ OPTION \_ TCP \_ FAST \_ OPEN<br/>**Bool** | X | \- | \- | X | Windows 10 versão 2004 |
| WINHTTP \_ OPTION \_ TCP \_ KEEPALIVE<br/>[**tcp \_ keepalive**](/windows/win32/winsock/sio-keepalive-vals) | X | \- | \- | X | Windows 10 versão 2004 |
| WINHTTP \_ OPTION \_ TLS \_ FALSE \_ START<br/>**Bool** | X | \- | \- | X | Windows 10 versão 2004 |
| FALLBACK INSEGURO DO \_ \_ PROTOCOLO TLS \_ \_ DA OPÇÃO WINHTTP \_<br/>**Bool** | X | \- | \- | X | Windows 10 versão 21H1 |
| EVENTO DE \_ NOTIFICAÇÃO \_ DE DESCARREGAMENTO DE OPÇÃO \_ \_ WINHTTP<br/>[Hinternet](hinternet-handles-in-winhttp.md) | X | \- | \- | X | \- |
| ANÁLISE DE TÍTULO NÃO SEGURO DA OPÇÃO WINHTTP \_ \_ \_ \_<br/>**DWORD** | \- | X | \- | X | \- |
| ATUALIZAÇÃO DA OPÇÃO WINHTTP \_ \_ PARA O \_ \_ SOQUETE DA \_ WEB<br/>N/D | \- | X | \- | X | \- |
| URL DA OPÇÃO \_ WINHTTP \_<br/>**Lpwstr** | \- | X | X | \- | \- |
| OPÇÃO WINHTTP \_ \_ USAR CREDENCIAIS DE \_ \_ SERVIDOR GLOBAL \_<br/>**Bool** | X | X | \- | X | \- |
| AGENTE DO USUÁRIO DA OPÇÃO WINHTTP \_ \_ \_<br/>**Lpwstr** | X | \- | X | X | \- |
| NOME DE USUÁRIO DA OPÇÃO WINHTTP \_ \_<br/>**Lpwstr** | \- | X | X | X | \- |
| WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ CLOSE \_ TIMEOUT<br/>**DWORD** | \- | \- | X | X | \- |
| WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ KEEPALIVE \_ INTERVAL<br/>**DWORD** | \- | \- | X | X | \- |
| WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ RECEIVE \_ BUFFER \_ SIZE<br/>**DWORD** | X | X | X | X | Windows 8.1 |
| WINHTTP \_ OPTION \_ WEB \_ SOCKET \_ SEND \_ BUFFER \_ SIZE<br/>**DWORD** | X | X | X | X | Windows 8.1 |
| CONTAGEM DE \_ \_ THREADS DE TRABALHO DA OPÇÃO \_ WINHTTP \_<br/>**DWORD** | \- | \- | \- | X | \- |
| TAMANHO DO \_ BUFFER DE GRAVAÇÃO DA OPÇÃO WINHTTP \_ \_ \_<br/>**DWORD** | \- | X | X | X | \- |

> [!Note]
> Para Windows XP e Windows 2000, consulte [Requisitos de tempo de executar](winhttp-start-page.md).

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------------------------|---------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows XP, Windows 2000 Professional somente com aplicativos da área de trabalho SP3 \[\]            |
| Servidor mínimo com suporte | Windows Server 2003, Windows 2000 Server somente com aplicativos da área de trabalho SP3 \[\]         |
| Redistribuível          | WinHTTP 5.0 e Internet Explorer 5.01 ou posterior no Windows XP e Windows 2000. |
| Cabeçalho                   | Winhttp.h                                                                       |

## <a name="see-also"></a>Confira também

[Versões do WinHTTP](winhttp-versions.md)
