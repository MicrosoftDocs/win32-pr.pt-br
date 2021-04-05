---
title: Mensagens de erro (Wininet. h)
description: As funções WinINet retornam códigos de erro quando apropriado. Os erros a seguir são específicos para as funções do WinINet.
ms.assetid: 338bf65f-ebe5-4434-8407-9ab2a4c8d381
topic_type:
- apiref
api_name:
- ERROR_FTP_DROPPED
- ERROR_FTP_NO_PASSIVE_MODE
- ERROR_FTP_TRANSFER_IN_PROGRESS
- ERROR_GOPHER_ATTRIBUTE_NOT_FOUND
- ERROR_GOPHER_DATA_ERROR
- ERROR_GOPHER_END_OF_DATA
- ERROR_GOPHER_INCORRECT_LOCATOR_TYPE
- ERROR_GOPHER_INVALID_LOCATOR
- ERROR_GOPHER_NOT_FILE
- ERROR_GOPHER_NOT_GOPHER_PLUS
- ERROR_GOPHER_PROTOCOL_ERROR
- ERROR_GOPHER_UNKNOWN_LOCATOR
- ERROR_HTTP_COOKIE_DECLINED
- ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION
- ERROR_HTTP_DOWNLEVEL_SERVER
- ERROR_HTTP_HEADER_ALREADY_EXISTS
- ERROR_HTTP_HEADER_NOT_FOUND
- ERROR_HTTP_INVALID_HEADER
- ERROR_HTTP_INVALID_QUERY_REQUEST
- ERROR_HTTP_INVALID_SERVER_RESPONSE
- ERROR_HTTP_NOT_REDIRECTED
- ERROR_HTTP_REDIRECT_FAILED
- ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION
- ERROR_INTERNET_ASYNC_THREAD_FAILED
- ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT
- ERROR_INTERNET_BAD_OPTION_LENGTH
- ERROR_INTERNET_BAD_REGISTRY_PARAMETER
- ERROR_INTERNET_CANNOT_CONNECT
- ERROR_INTERNET_CHG_POST_IS_NON_SECURE
- ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED
- ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP
- ERROR_INTERNET_CONNECTION_ABORTED
- ERROR_INTERNET_CONNECTION_RESET
- ERROR_INTERNET_DECODING_FAILED
- ERROR_INTERNET_DIALOG_PENDING
- ERROR_INTERNET_DISCONNECTED
- ERROR_INTERNET_EXTENDED_ERROR
- ERROR_INTERNET_FAILED_DUETOSECURITYCHECK
- ERROR_INTERNET_FORCE_RETRY
- ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED
- ERROR_INTERNET_HANDLE_EXISTS
- ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR
- ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR
- ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR
- ERROR_INTERNET_INCORRECT_FORMAT
- ERROR_INTERNET_INCORRECT_HANDLE_STATE
- ERROR_INTERNET_INCORRECT_HANDLE_TYPE
- ERROR_INTERNET_INCORRECT_PASSWORD
- ERROR_INTERNET_INCORRECT_USER_NAME
- ERROR_INTERNET_INSERT_CDROM
- ERROR_INTERNET_INTERNAL_ERROR
- ERROR_INTERNET_INVALID_CA
- ERROR_INTERNET_INVALID_OPERATION
- ERROR_INTERNET_INVALID_OPTION
- ERROR_INTERNET_INVALID_PROXY_REQUEST
- ERROR_INTERNET_INVALID_URL
- ERROR_INTERNET_ITEM_NOT_FOUND
- ERROR_INTERNET_LOGIN_FAILURE
- ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY
- ERROR_INTERNET_MIXED_SECURITY
- ERROR_INTERNET_NAME_NOT_RESOLVED
- ERROR_INTERNET_NEED_MSN_SSPI_PKG
- ERROR_INTERNET_NEED_UI
- ERROR_INTERNET_NO_CALLBACK
- ERROR_INTERNET_NO_CONTEXT
- ERROR_INTERNET_NO_DIRECT_ACCESS
- ERROR_INTERNET_NOT_INITIALIZED
- ERROR_INTERNET_NOT_PROXY_REQUEST
- ERROR_INTERNET_OPERATION_CANCELLED
- ERROR_INTERNET_OPTION_NOT_SETTABLE
- ERROR_INTERNET_OUT_OF_HANDLES
- ERROR_INTERNET_POST_IS_NON_SECURE
- ERROR_INTERNET_PROTOCOL_NOT_FOUND
- ERROR_INTERNET_PROXY_SERVER_UNREACHABLE
- ERROR_INTERNET_REDIRECT_SCHEME_CHANGE
- ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND
- ERROR_INTERNET_REQUEST_PENDING
- ERROR_INTERNET_RETRY_DIALOG
- ERROR_INTERNET_SEC_CERT_CN_INVALID
- ERROR_INTERNET_SEC_CERT_DATE_INVALID
- ERROR_INTERNET_SEC_CERT_ERRORS
- ERROR_INTERNET_SEC_CERT_NO_REV
- ERROR_INTERNET_SEC_CERT_REV_FAILED
- ERROR_INTERNET_SEC_CERT_REVOKED
- ERROR_INTERNET_SEC_INVALID_CERT
- ERROR_INTERNET_SECURITY_CHANNEL_ERROR
- ERROR_INTERNET_SERVER_UNREACHABLE
- ERROR_INTERNET_SHUTDOWN
- ERROR_INTERNET_TCPIP_NOT_INSTALLED
- ERROR_INTERNET_TIMEOUT
- ERROR_INTERNET_UNABLE_TO_CACHE_FILE
- ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT
- ERROR_INTERNET_UNRECOGNIZED_SCHEME
- ERROR_INVALID_HANDLE
- ERROR_MORE_DATA
- ERROR_NO_MORE_FILES
- ERROR_NO_MORE_ITEMS
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43fcaba7f0404ad002d2a94ac8291c95b0f7440
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086482"
---
# <a name="error-messages-winineth"></a>Mensagens de erro (Wininet. h)

As funções WinINet retornam códigos de erro quando apropriado. Os erros a seguir são específicos para as funções do WinINet.

<dl> <dt>

<span id="ERROR_FTP_DROPPED"></span><span id="error_ftp_dropped"></span>**ERRO \_ FTP \_ ignorado**
</dt> <dd> <dl> <dt>

12111
</dt> <dt>



A operação de FTP não foi concluída porque a sessão foi anulada.


</dt> </dl> </dd> <dt>

<span id="ERROR_FTP_NO_PASSIVE_MODE"></span><span id="error_ftp_no_passive_mode"></span>**ERRO \_ FTP \_ sem \_ \_ modo passivo**
</dt> <dd> <dl> <dt>

12112
</dt> <dt>



O modo passivo não está disponível no servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_FTP_TRANSFER_IN_PROGRESS"></span><span id="error_ftp_transfer_in_progress"></span>**ERRO \_ \_ na transferência \_ de FTP em \_ andamento**
</dt> <dd> <dl> <dt>

12110
</dt> <dt>



A operação solicitada não pode ser feita no identificador de sessão de FTP porque uma operação já está em andamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_ATTRIBUTE_NOT_FOUND"></span><span id="error_gopher_attribute_not_found"></span>**ERRO \_ de \_ atributo Gopher \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

12137
</dt> <dt>



Não foi possível localizar o atributo solicitado.

> [!Note]  
> Somente Windows XP e Windows Server 2003 R2 e versões anteriores.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_DATA_ERROR"></span><span id="error_gopher_data_error"></span>**ERRO de erro de \_ \_ dados Gopher \_**
</dt> <dd> <dl> <dt>

12132
</dt> <dt>



Foi detectado um erro ao receber dados do servidor gopher.

> [!Note]  
> Somente Windows XP e Windows Server 2003 R2 e versões anteriores.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_END_OF_DATA"></span><span id="error_gopher_end_of_data"></span>**ERRO \_ \_ de fim \_ de \_ dados do Gopher**
</dt> <dd> <dl> <dt>

12133
</dt> <dt>



O fim dos dados foi atingido.

> [!Note]  
> Somente Windows XP e Windows Server 2003 R2 e versões anteriores.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_INCORRECT_LOCATOR_TYPE"></span><span id="error_gopher_incorrect_locator_type"></span>**ERRO \_ do \_ \_ tipo de localizador incorreto do Gopher \_**
</dt> <dd> <dl> <dt>

12135
</dt> <dt>



O tipo do localizador não está correto para esta operação.

> [!Note]  
> Somente Windows XP e Windows Server 2003 R2 e versões anteriores.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_INVALID_LOCATOR"></span><span id="error_gopher_invalid_locator"></span>**ERRO \_ Gopher \_ inválido no \_ localizador**
</dt> <dd> <dl> <dt>

12134
</dt> <dt>



O localizador fornecido não é válido.

> [!Note]  
> Somente Windows XP e Windows Server 2003 R2 e versões anteriores.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_NOT_FILE"></span><span id="error_gopher_not_file"></span>**ERRO \_ Gopher \_ não \_ arquivo**
</dt> <dd> <dl> <dt>

12131
</dt> <dt>



A solicitação deve ser feita para um localizador de arquivo.

> [!Note]  
> Somente Windows XP e Windows Server 2003 R2 e versões anteriores.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_NOT_GOPHER_PLUS"></span><span id="error_gopher_not_gopher_plus"></span>**ERRO \_ Gopher \_ não \_ Gopher \_ Plus**
</dt> <dd> <dl> <dt>

12136
</dt> <dt>



A operação solicitada pode ser feita somente em um servidor Gopher + ou com um localizador que especifica uma operação do Gopher +.

> [!Note]  
> Somente Windows XP e Windows Server 2003 R2 e versões anteriores.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_PROTOCOL_ERROR"></span><span id="error_gopher_protocol_error"></span>**ERRO de erro de \_ \_ protocolo Gopher \_**
</dt> <dd> <dl> <dt>

12130
</dt> <dt>



Foi detectado um erro ao analisar os dados retornados do servidor gopher.

> [!Note]  
> Somente Windows XP e Windows Server 2003 R2 e versões anteriores.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_UNKNOWN_LOCATOR"></span><span id="error_gopher_unknown_locator"></span>**ERRO \_ de \_ localizador desconhecido do Gopher \_**
</dt> <dd> <dl> <dt>

12138
</dt> <dt>



O tipo de localizador é desconhecido.

> [!Note]  
> Somente Windows XP e Windows Server 2003 R2 e versões anteriores.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_COOKIE_DECLINED"></span><span id="error_http_cookie_declined"></span>**ERRO \_ de \_ Cookie http \_ recusado**
</dt> <dd> <dl> <dt>

12162
</dt> <dt>



O cookie HTTP foi recusado pelo servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION"></span><span id="error_http_cookie_needs_confirmation"></span>**ERRO \_ o \_ Cookie http \_ precisa de \_ confirmação**
</dt> <dd> <dl> <dt>

12161
</dt> <dt>



O cookie HTTP requer confirmação.

> [!Note]  
> Somente Windows Vista e Windows Server 2008 e versões anteriores.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_DOWNLEVEL_SERVER"></span><span id="error_http_downlevel_server"></span>**ERRO \_ de \_ servidor de nível inferior http \_**
</dt> <dd> <dl> <dt>

12151
</dt> <dt>



O servidor não retornou nenhum cabeçalho.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_HEADER_ALREADY_EXISTS"></span><span id="error_http_header_already_exists"></span>**o \_ cabeçalho HTTP do erro \_ \_ já \_ existe**
</dt> <dd> <dl> <dt>

12155
</dt> <dt>



Não foi possível adicionar o cabeçalho porque ele já existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_HEADER_NOT_FOUND"></span><span id="error_http_header_not_found"></span>**\_cabeçalho HTTP de erro \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

12150
</dt> <dt>



Não foi possível localizar o cabeçalho solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_INVALID_HEADER"></span><span id="error_http_invalid_header"></span>**ERRO \_ de \_ cabeçalho http inválido \_**
</dt> <dd> <dl> <dt>

12153
</dt> <dt>



O cabeçalho fornecido é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_INVALID_QUERY_REQUEST"></span><span id="error_http_invalid_query_request"></span>**ERRO \_ de \_ \_ solicitação de consulta http inválida \_**
</dt> <dd> <dl> <dt>

12154
</dt> <dt>



A solicitação feita ao [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) é inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_INVALID_SERVER_RESPONSE"></span><span id="error_http_invalid_server_response"></span>**ERRO \_ de \_ resposta inválida \_ do servidor http \_**
</dt> <dd> <dl> <dt>

12152
</dt> <dt>



Não foi possível analisar a resposta do servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_NOT_REDIRECTED"></span><span id="error_http_not_redirected"></span>**ERRO \_ http \_ não \_ Redirecionado**
</dt> <dd> <dl> <dt>

12160
</dt> <dt>



A solicitação HTTP não foi redirecionada.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_REDIRECT_FAILED"></span><span id="error_http_redirect_failed"></span>**ERRO \_ \_ ao redirecionar http \_**
</dt> <dd> <dl> <dt>

12156
</dt> <dt>



Falha no redirecionamento porque o esquema foi alterado (por exemplo, HTTP para FTP) ou todas as tentativas feitas para redirecionar falharam (o padrão é cinco tentativas).


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION"></span><span id="error_http_redirect_needs_confirmation"></span>**ERRO \_ de \_ confirmação de redirecionamento http \_ necessário \_**
</dt> <dd> <dl> <dt>

12168
</dt> <dt>



O redirecionamento requer confirmação do usuário.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_ASYNC_THREAD_FAILED"></span><span id="error_internet_async_thread_failed"></span>**ERRO \_ \_ thread assíncrono da Internet \_ \_ com falha**
</dt> <dd> <dl> <dt>

12047
</dt> <dt>



O aplicativo não pôde iniciar um thread assíncrono.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_internet_bad_auto_proxy_script"></span>**ERRO \_ de \_ \_ script de \_ proxy \_ automático de Internet inválido**
</dt> <dd> <dl> <dt>

12166
</dt> <dt>



Ocorreu um erro no script de configuração de proxy automático.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_BAD_OPTION_LENGTH"></span><span id="error_internet_bad_option_length"></span>**ERRO \_ de \_ \_ comprimento de opção inadequado da Internet \_**
</dt> <dd> <dl> <dt>

12010
</dt> <dt>



O comprimento de uma opção fornecida para [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) ou [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) está incorreto para o tipo de opção especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_BAD_REGISTRY_PARAMETER"></span><span id="error_internet_bad_registry_parameter"></span>**ERRO \_ de \_ \_ parâmetro de registro insatisfatório na Internet \_**
</dt> <dd> <dl> <dt>

12022
</dt> <dt>



Um valor de registro necessário foi localizado, mas é um tipo incorreto ou tem um valor inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CANNOT_CONNECT"></span><span id="error_internet_cannot_connect"></span>**ERRO a \_ Internet \_ não pode \_ se conectar**
</dt> <dd> <dl> <dt>

12029
</dt> <dt>



Falha na tentativa de conexão com o servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CHG_POST_IS_NON_SECURE"></span><span id="error_internet_chg_post_is_non_secure"></span>**ERRO o \_ Internet \_ CHG post não \_ \_ é \_ \_ seguro**
</dt> <dd> <dl> <dt>

12042
</dt> <dt>



O aplicativo está postando e tentando alterar várias linhas de texto em um servidor que não é seguro.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_internet_client_auth_cert_needed"></span>**ERRO \_ de \_ certificado de autenticação de cliente de Internet \_ \_ \_ necessário**
</dt> <dd> <dl> <dt>

12044
</dt> <dt>



O servidor está solicitando a autenticação do cliente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP"></span><span id="error_internet_client_auth_not_setup"></span>**ERRO \_ autenticação do cliente da Internet \_ \_ \_ não \_ configurada**
</dt> <dd> <dl> <dt>

12046
</dt> <dt>



A autorização do cliente não está configurada neste computador.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CONNECTION_ABORTED"></span><span id="error_internet_connection_aborted"></span>**ERRO \_ de \_ conexão com a Internet \_ abortado**
</dt> <dd> <dl> <dt>

12030
</dt> <dt>



A conexão com o servidor foi encerrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CONNECTION_RESET"></span><span id="error_internet_connection_reset"></span>**ERRO \_ de \_ redefinição de conexão com a Internet \_**
</dt> <dd> <dl> <dt>

12031
</dt> <dt>



A conexão com o servidor foi redefinida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_DECODING_FAILED"></span><span id="error_internet_decoding_failed"></span>**ERRO \_ de \_ decodificação de Internet \_ com falha**
</dt> <dd> <dl> <dt>

12175
</dt> <dt>



O WinINet não pôde executar a decodificação de conteúdo na resposta. Para obter mais informações, consulte o tópico [**codificação de conteúdo**](content-encoding.md) .


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_DIALOG_PENDING"></span><span id="error_internet_dialog_pending"></span>**diálogo de Internet de erro \_ \_ \_ pendente**
</dt> <dd> <dl> <dt>

12049
</dt> <dt>



Outro thread tem uma caixa de diálogo de senha em andamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_DISCONNECTED"></span><span id="error_internet_disconnected"></span>**ERRO de \_ Internet \_ desconectado**
</dt> <dd> <dl> <dt>

12163
</dt> <dt>



A conexão com a Internet foi perdida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_EXTENDED_ERROR"></span><span id="error_internet_extended_error"></span>**erro \_ \_ estendido pela Internet \_**
</dt> <dd> <dl> <dt>

12003
</dt> <dt>



Um erro estendido foi retornado do servidor. Normalmente, é uma cadeia de caracteres ou um buffer que contém uma mensagem de erro detalhada. Chame [**InternetGetLastResponseInfo**](/windows/desktop/api/Wininet/nf-wininet-internetgetlastresponseinfoa) para recuperar o texto do erro.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_FAILED_DUETOSECURITYCHECK"></span><span id="error_internet_failed_duetosecuritycheck"></span>**ERRO \_ de \_ falha na Internet \_ DUETOSECURITYCHECK**
</dt> <dd> <dl> <dt>

12171
</dt> <dt>



A função falhou devido a uma verificação de segurança.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_FORCE_RETRY"></span><span id="error_internet_force_retry"></span>**ERRO de \_ repetição de Internet \_ Force \_**
</dt> <dd> <dl> <dt>

12032
</dt> <dt>



A função precisa refazer a solicitação.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED"></span><span id="error_internet_fortezza_login_needed"></span>**ERRO \_ de \_ logon do Internet Fortezza \_ \_ necessário**
</dt> <dd> <dl> <dt>

12054
</dt> <dt>



O recurso solicitado requer autenticação Fortezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HANDLE_EXISTS"></span><span id="error_internet_handle_exists"></span>**ERRO \_ o \_ identificador da Internet \_ existe**
</dt> <dd> <dl> <dt>

12036
</dt> <dt>



A solicitação falhou porque o identificador já existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR"></span><span id="error_internet_http_to_https_on_redir"></span>**ERRO \_ \_ de http \_ da Internet para \_ https \_ no \_ REDIR**
</dt> <dd> <dl> <dt>

12039
</dt> <dt>



O aplicativo está mudando de um não SSL para uma conexão SSL devido a um redirecionamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR"></span><span id="error_internet_https_http_submit_redir"></span>**ERRO \_ de \_ \_ envio de http https \_ de Internet \_**
</dt> <dd> <dl> <dt>

12052
</dt> <dt>



Os dados que estão sendo enviados para uma conexão SSL estão sendo redirecionados para uma conexão não SSL.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR"></span><span id="error_internet_https_to_http_on_redir"></span>**ERRO de \_ Internet \_ https \_ para \_ http \_ em \_ REDIR**
</dt> <dd> <dl> <dt>

12040
</dt> <dt>



O aplicativo está mudando de um SSL para uma conexão não SSL devido a um redirecionamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_FORMAT"></span><span id="error_internet_incorrect_format"></span>**ERRO \_ de \_ formato incorreto da Internet \_**
</dt> <dd> <dl> <dt>

12027
</dt> <dt>



O formato da solicitação é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_HANDLE_STATE"></span><span id="error_internet_incorrect_handle_state"></span>**ERRO \_ no \_ \_ estado do identificador incorreto da Internet \_**
</dt> <dd> <dl> <dt>

12019
</dt> <dt>



A operação solicitada não pode ser executada porque o identificador fornecido não está no estado correto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_HANDLE_TYPE"></span><span id="error_internet_incorrect_handle_type"></span>**ERRO \_ de \_ \_ tipo de identificador incorreto da Internet \_**
</dt> <dd> <dl> <dt>

12018
</dt> <dt>



O tipo de identificador fornecido está incorreto para esta operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_PASSWORD"></span><span id="error_internet_incorrect_password"></span>**ERRO \_ de \_ senha incorreta na Internet \_**
</dt> <dd> <dl> <dt>

12014
</dt> <dt>



A solicitação para se conectar e fazer logon em um servidor FTP não pôde ser concluída porque a senha fornecida está incorreta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_USER_NAME"></span><span id="error_internet_incorrect_user_name"></span>**ERRO \_ de \_ \_ nome de usuário incorreto da Internet \_**
</dt> <dd> <dl> <dt>

12013
</dt> <dt>



A solicitação para se conectar e fazer logon em um servidor FTP não pôde ser concluída porque o nome de usuário fornecido está incorreto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INSERT_CDROM"></span><span id="error_internet_insert_cdrom"></span>**ERRO \_ ao \_ Inserir \_ CD-ROM**
</dt> <dd> <dl> <dt>

12053
</dt> <dt>



A solicitação exige que um CD-ROM seja inserido na unidade de CD-ROM para localizar o recurso solicitado.

> [!Note]  
> Somente Windows Vista e Windows Server 2008 e versões anteriores.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INTERNAL_ERROR"></span><span id="error_internet_internal_error"></span>**erro \_ interno da Internet de erro \_ \_**
</dt> <dd> <dl> <dt>

12004
</dt> <dt>



Ocorreu um erro interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_CA"></span><span id="error_internet_invalid_ca"></span>**ERRO \_ de \_ AC inválida \_ da Internet**
</dt> <dd> <dl> <dt>

12045
</dt> <dt>



A função não está familiarizada com a autoridade de certificação que gerou o certificado do servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_OPERATION"></span><span id="error_internet_invalid_operation"></span>**ERRO \_ de \_ operação inválida na Internet \_**
</dt> <dd> <dl> <dt>

12016
</dt> <dt>



A operação solicitada é inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_OPTION"></span><span id="error_internet_invalid_option"></span>**ERRO de \_ opção de Internet \_ inválida \_**
</dt> <dd> <dl> <dt>

12009
</dt> <dt>



Uma solicitação para [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) ou [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) especificou um valor de opção inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_PROXY_REQUEST"></span><span id="error_internet_invalid_proxy_request"></span>**ERRO \_ na \_ \_ solicitação de proxy inválida da Internet \_**
</dt> <dd> <dl> <dt>

12033
</dt> <dt>



A solicitação para o proxy era inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_URL"></span><span id="error_internet_invalid_url"></span>**\_ \_ URL inválida da Internet de erro \_**
</dt> <dd> <dl> <dt>

12005
</dt> <dt>



A URL é inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_ITEM_NOT_FOUND"></span><span id="error_internet_item_not_found"></span>**ITEM de Internet de erro \_ \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

12028
</dt> <dt>



Não foi possível localizar o item solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_LOGIN_FAILURE"></span><span id="error_internet_login_failure"></span>**ERRO \_ de \_ logon \_ na Internet**
</dt> <dd> <dl> <dt>

12015
</dt> <dt>



A solicitação para se conectar e fazer logon em um servidor FTP falhou.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="error_internet_login_failure_display_entity_body"></span>**ERRO \_ de \_ logon \_ na Internet falha ao \_ Exibir o \_ corpo da entidade \_**
</dt> <dd> <dl> <dt>

12174
</dt> <dt>



O cabeçalho do Resumo de MS-Logoff foi retornado do site. Esse cabeçalho instrui especificamente o pacote de resumo para limpar as credenciais do Realm associado. Esse erro será retornado somente se a opção de [ \_ falha de logon máscara de erro da Internet exibir o \_ \_ \_ \_ \_ \_ corpo da entidade](option-flags.md) tiver sido definida; caso contrário, será retornada uma falha de **\_ \_ logon \_ na Internet** .


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_MIXED_SECURITY"></span><span id="error_internet_mixed_security"></span>**ERRO \_ de \_ segurança mista na Internet \_**
</dt> <dd> <dl> <dt>

12041
</dt> <dt>



O conteúdo não é totalmente seguro. Parte do conteúdo visualizado pode ter vindo de servidores não seguros.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NAME_NOT_RESOLVED"></span><span id="error_internet_name_not_resolved"></span>**ERRO \_ nome da Internet \_ \_ não \_ resolvido**
</dt> <dd> <dl> <dt>

12007
</dt> <dt>



Não foi possível resolver o nome do servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NEED_MSN_SSPI_PKG"></span><span id="error_internet_need_msn_sspi_pkg"></span>**ERRO a \_ Internet \_ precisa do \_ \_ pacote SSPI do MSN \_**
</dt> <dd> <dl> <dt>

12173
</dt> <dt>



Não implementado atualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NEED_UI"></span><span id="error_internet_need_ui"></span>**ERRO \_ na \_ \_ interface do usuário da Internet**
</dt> <dd> <dl> <dt>

12034
</dt> <dt>



Uma interface do usuário ou outra operação de bloqueio foi solicitada.

> [!Note]  
> Somente Windows Vista e Windows Server 2008 e versões anteriores.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NO_CALLBACK"></span><span id="error_internet_no_callback"></span>**ERRO de \_ Internet \_ sem retorno de \_ chamada**
</dt> <dd> <dl> <dt>

12025
</dt> <dt>



Uma solicitação assíncrona não pôde ser feita porque uma função de retorno de chamada não foi definida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NO_CONTEXT"></span><span id="error_internet_no_context"></span>**ERRO de \_ Internet \_ sem \_ contexto**
</dt> <dd> <dl> <dt>

12024
</dt> <dt>



Uma solicitação assíncrona não pôde ser feita porque um valor de contexto zero foi fornecido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NO_DIRECT_ACCESS"></span><span id="error_internet_no_direct_access"></span>**ERRO \_ de \_ Internet \_ sem \_ acesso direto**
</dt> <dd> <dl> <dt>

12023
</dt> <dt>



O acesso direto à rede não pode ser feito neste momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NOT_INITIALIZED"></span><span id="error_internet_not_initialized"></span>**ERRO na \_ Internet \_ não \_ inicializado**
</dt> <dd> <dl> <dt>

12172
</dt> <dt>



A inicialização da API do WinINet não ocorreu. Indica que uma função de nível superior, como [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), ainda não foi chamada.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NOT_PROXY_REQUEST"></span><span id="error_internet_not_proxy_request"></span>**ERRO \_ na \_ \_ solicitação de proxy \_ da Internet**
</dt> <dd> <dl> <dt>

12020
</dt> <dt>



A solicitação não pode ser feita por meio de um proxy.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_OPERATION_CANCELLED"></span><span id="error_internet_operation_cancelled"></span>**ERRO \_ na \_ operação de Internet \_ cancelada**
</dt> <dd> <dl> <dt>

12017
</dt> <dt>



A operação foi cancelada, geralmente porque o identificador no qual a solicitação estava operando foi fechado antes da operação ser concluída.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_OPTION_NOT_SETTABLE"></span><span id="error_internet_option_not_settable"></span>**ERRO \_ na \_ opção da Internet \_ não \_ configurável**
</dt> <dd> <dl> <dt>

12011
</dt> <dt>



A opção solicitada não pode ser definida, somente consultada.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_OUT_OF_HANDLES"></span><span id="error_internet_out_of_handles"></span>**ERRO \_ \_ de Internet fora \_ de \_ identificadores**
</dt> <dd> <dl> <dt>

12001
</dt> <dt>



Não foi possível gerar mais identificadores neste momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_POST_IS_NON_SECURE"></span><span id="error_internet_post_is_non_secure"></span>**ERRO \_ a \_ postagem na Internet \_ \_ não é \_ segura**
</dt> <dd> <dl> <dt>

12043
</dt> <dt>



O aplicativo está postando dados em um servidor que não é seguro.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_PROTOCOL_NOT_FOUND"></span><span id="error_internet_protocol_not_found"></span>**ERRO \_ de \_ protocolo de Internet \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

12008
</dt> <dt>



Não foi possível localizar o protocolo solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_PROXY_SERVER_UNREACHABLE"></span><span id="error_internet_proxy_server_unreachable"></span>**ERRO \_ de \_ servidor proxy da Internet \_ \_ inacessível**
</dt> <dd> <dl> <dt>

12165
</dt> <dt>



O servidor proxy designado não pode ser acessado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_REDIRECT_SCHEME_CHANGE"></span><span id="error_internet_redirect_scheme_change"></span>**ERRO \_ de \_ \_ alteração do esquema de redirecionamento da Internet \_**
</dt> <dd> <dl> <dt>

12048
</dt> <dt>



A função não pôde lidar com o redirecionamento, pois o esquema foi alterado (por exemplo, HTTP para FTP).


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND"></span><span id="error_internet_registry_value_not_found"></span>**ERRO \_ o \_ valor do registro da Internet \_ \_ não \_ foi encontrado**
</dt> <dd> <dl> <dt>

12021
</dt> <dt>



Um valor de registro necessário não pôde ser localizado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_REQUEST_PENDING"></span><span id="error_internet_request_pending"></span>**ERRO \_ de \_ solicitação de Internet \_ pendente**
</dt> <dd> <dl> <dt>

12026
</dt> <dt>



A operação necessária não pôde ser concluída porque uma ou mais solicitações estão pendentes.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_RETRY_DIALOG"></span><span id="error_internet_retry_dialog"></span>**\_diálogo de \_ repetição de Internet de erro \_**
</dt> <dd> <dl> <dt>

12050
</dt> <dt>



A caixa de diálogo deve ser repetida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_CN_INVALID"></span><span id="error_internet_sec_cert_cn_invalid"></span>**ERRO \_ CN do certificado da Internet \_ SEC \_ \_ \_ inválido**
</dt> <dd> <dl> <dt>

12038
</dt> <dt>



O nome comum do certificado SSL (campo nome do host) está incorreto por exemplo, se você inseriu www.server.com e o nome comum no certificado diz www.different.com.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_DATE_INVALID"></span><span id="error_internet_sec_cert_date_invalid"></span>**ERRO de data de CERT. de \_ Internet \_ \_ \_ \_ inválida**
</dt> <dd> <dl> <dt>

12037
</dt> <dt>



A data do certificado SSL que foi recebida do servidor é inadequada. O certificado expirou.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_ERRORS"></span><span id="error_internet_sec_cert_errors"></span>**\_erros de certificados da Internet \_ SEC \_ \_**
</dt> <dd> <dl> <dt>

12055
</dt> <dt>



O certificado SSL contém erros.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_NO_REV"></span><span id="error_internet_sec_cert_no_rev"></span>**ERRO na \_ Internet \_ s CERT. \_ \_ sem \_ Rev.**
</dt> <dd> <dl> <dt>

12056
</dt> <dt>



O certificado SSL não foi revogado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_REV_FAILED"></span><span id="error_internet_sec_cert_rev_failed"></span>**ERRO a Rev. de \_ certificado da Internet \_ SEC \_ \_ \_ falhou**
</dt> <dd> <dl> <dt>

12057
</dt> <dt>



Falha na revogação do certificado SSL.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_REVOKED"></span><span id="error_internet_sec_cert_revoked"></span>**ERRO na \_ Internet \_ SEC \_ CERT \_ revogado**
</dt> <dd> <dl> <dt>

12170
</dt> <dt>



O certificado SSL foi revogado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_INVALID_CERT"></span><span id="error_internet_sec_invalid_cert"></span>**ERRO na \_ Internet \_ SEC \_ inválida \_**
</dt> <dd> <dl> <dt>

12169
</dt> <dt>



O certificado SSL é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SECURITY_CHANNEL_ERROR"></span><span id="error_internet_security_channel_error"></span>**erro no erro de canal de segurança da \_ Internet \_ \_ \_**
</dt> <dd> <dl> <dt>

12157
</dt> <dt>



O aplicativo sofreu um erro interno ao carregar as bibliotecas SSL.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SERVER_UNREACHABLE"></span><span id="error_internet_server_unreachable"></span>**ERRO \_ de \_ servidor de Internet \_ inacessível**
</dt> <dd> <dl> <dt>

12164
</dt> <dt>



O site ou servidor indicado está inacessível.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SHUTDOWN"></span><span id="error_internet_shutdown"></span>**ERRO \_ de \_ desligamento da Internet**
</dt> <dd> <dl> <dt>

12012
</dt> <dt>



O suporte a WinINet está sendo desligado ou descarregado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_TCPIP_NOT_INSTALLED"></span><span id="error_internet_tcpip_not_installed"></span>**ERRO \_ tcpip de Internet \_ \_ não \_ instalado**
</dt> <dd> <dl> <dt>

12159
</dt> <dt>



A pilha de protocolos necessária não está carregada e o aplicativo não pode iniciar o WinSock.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_TIMEOUT"></span><span id="error_internet_timeout"></span>**\_tempo limite da Internet de erro \_**
</dt> <dd> <dl> <dt>

12002
</dt> <dt>



O tempo limite da solicitação foi atingido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_UNABLE_TO_CACHE_FILE"></span><span id="error_internet_unable_to_cache_file"></span>**ERRO \_ \_ na Internet não é possível \_ armazenar o \_ arquivo em cache \_**
</dt> <dd> <dl> <dt>

12158
</dt> <dt>



A função não pôde armazenar o arquivo em cache.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_internet_unable_to_download_script"></span>**ERRO \_ \_ na Internet não é possível \_ baixar o \_ \_ script**
</dt> <dd> <dl> <dt>

12167
</dt> <dt>



Não foi possível baixar o script de configuração de proxy automático. O sinalizador da INTERNET deve ter o \_ \_ sinalizador de solicitação de \_ cache \_ definido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_UNRECOGNIZED_SCHEME"></span><span id="error_internet_unrecognized_scheme"></span>**ERRO \_ de \_ esquema não reconhecido da Internet \_**
</dt> <dd> <dl> <dt>

12006
</dt> <dt>



O esquema de URL não pôde ser reconhecido ou não tem suporte.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**\_identificador inválido do erro \_**
</dt> <dd> <dl> <dt>



O identificador que foi passado para a API foi invalidado ou fechado.

**Cabeçalho:** Declarado em Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERRO de \_ mais \_ dados**
</dt> <dd> <dl> <dt>



Mais dados disponíveis.

**Cabeçalho:** Declarado em Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERRO \_ não há \_ mais \_ arquivos**
</dt> <dd> <dl> <dt>



Não foram encontrados mais arquivos.

**Cabeçalho:** Declarado em Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERRO \_ não há \_ mais \_ itens**
</dt> <dd> <dl> <dt>



Não foram encontrados mais itens.

**Cabeçalho:** Declarado em Winerror. h


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

> [!Note]  
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>WinInet. h</dt> </dl> |



 

