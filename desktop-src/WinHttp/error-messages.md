---
description: Os valores de erro identificados neste tópico são retornados por GetLastError quando uma das funções do Microsoft Windows HTTP Services (WinHTTP) falha.
ms.assetid: c8a863cd-d36c-4ec8-ac49-0b714a5e4cc2
title: Mensagens de erro (Winhttp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d83fa1859f071b0fc0e651235deea51626f55b8a45cdb2a3ea8736a57317741
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744712"
---
# <a name="error-messages-winhttph"></a>Mensagens de erro (Winhttp.h)

Os valores de erro listados abaixo são retornados por [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando uma das funções do Microsoft Windows HTTP Services (WinHTTP) falha e também é retornada nos 16 bits inferiores do [**erro HRESULT**](../com/structure-of-com-error-codes.md) retorna do objeto [**WinHttpRequest.**](winhttprequest.md)

Os valores de erro cujos nomes começam com "ERROR \_ WINHTTP" \_ são específicos para as funções WinHTTP. As funções WinHTTP também retornam Windows mensagens de erro quando apropriado.

<dl> <dt>

<span id="ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR"></span><span id="error_winhttp_auto_proxy_service_error"></span>**ERRO \_ ERRO DO SERVIÇO DE \_ PROXY AUTOMÁTICO WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>

12178
</dt> <dt>



Retornado por [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) quando não é possível localizar um proxy para a URL especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_AUTODETECTION_FAILED"></span><span id="error_winhttp_autodetection_failed"></span>**ERRO \_ FALHA NA \_ AUTODETECTION WINHTTP \_**
</dt> <dd> <dl> <dt>

12180
</dt> <dt>



Retornado por [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) se o WinHTTP não conseguir descobrir a URL do arquivo PAC (Configuração Automática de Proxy).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_winhttp_bad_auto_proxy_script"></span>**ERRO \_ SCRIPT DE PROXY AUTOMÁTICO \_ WINHTTP \_ \_ \_ RUIM**
</dt> <dd> <dl> <dt>

12166
</dt> <dt>



Ocorreu um erro ao executar o código de script no arquivo PAC (Configuração Automática de Proxy).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_OPEN"></span><span id="error_winhttp_cannot_call_after_open"></span>**ERRO \_ WINHTTP \_ NÃO PODE CHAMAR APÓS \_ \_ \_ ABRIR**
</dt> <dd> <dl> <dt>

12103
</dt> <dt>



Retornado pelo objeto [**HttpRequest**](winhttprequest.md) se uma opção especificada não puder ser solicitada depois que [**o método Open**](iwinhttprequest-open.md) tiver sido chamado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_SEND"></span><span id="error_winhttp_cannot_call_after_send"></span>**ERRO \_ WINHTTP \_ NÃO PODE CHAMAR APÓS O \_ \_ \_ ENVIO**
</dt> <dd> <dl> <dt>

12102
</dt> <dt>



Retornado pelo objeto [**HttpRequest**](winhttprequest.md) se uma operação solicitada não puder ser executada depois de chamar o [**método**](iwinhttprequest-send.md) Send.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_OPEN"></span><span id="error_winhttp_cannot_call_before_open"></span>**ERRO \_ WINHTTP \_ NÃO PODE CHAMAR ANTES DE \_ \_ \_ ABRIR**
</dt> <dd> <dl> <dt>

12100
</dt> <dt>



Retornado pelo objeto [**HttpRequest**](winhttprequest.md) se uma operação solicitada não puder ser executada antes de chamar o [**método**](iwinhttprequest-open.md) Open.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_SEND"></span><span id="error_winhttp_cannot_call_before_send"></span>**ERRO \_ WINHTTP \_ NÃO PODE CHAMAR ANTES DE \_ \_ \_ ENVIAR**
</dt> <dd> <dl> <dt>

12101
</dt> <dt>



Retornado pelo objeto [**HttpRequest**](winhttprequest.md) se uma operação solicitada não puder ser executada antes de chamar o [**método**](iwinhttprequest-send.md) Send.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CONNECT"></span><span id="error_winhttp_cannot_connect"></span>**ERRO \_ WINHTTP \_ NÃO PODE SE \_ CONECTAR**
</dt> <dd> <dl> <dt>

12029
</dt> <dt>



Retornado se a conexão com o servidor falhou.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERRO \_ WINHTTP \_ CLIENT \_ AUTH \_ CERT \_ NEEDED**
</dt> <dd> <dl> <dt>



O servidor requer autenticação de cliente SSL. O aplicativo recupera a lista de emissores de certificado chamando [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) com a **opção WINHTTP \_ OPTION CLIENT CERT \_ \_ \_ ISSUER \_ LIST.** Para obter mais informações, consulte a **opção WINHTTP \_ OPTION CLIENT CERT \_ \_ \_ ISSUER \_ LIST.**

Se o servidor solicitar o certificado do cliente, mas não o exigir, o aplicativo poderá, como alternativa, chamar [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) com a **opção WINHTTP \_ OPTION CLIENT CERT \_ \_ \_ CONTEXT.** Nesse caso, o aplicativo especifica a macro CONTEXTO WINHTTP NO CLIENT CERT no parâmetro \_ \_ \_ \_ *lpBuffer* de **WinHttpSetOption**. Para obter mais informações, consulte a opção CONTEXTO DE CERTIFICADO DO CLIENTE **\_ WINHTTP OPTION. \_ \_ \_**

**Windows Server 2003 com SP1 e Windows XP com SP2:** Não há suporte para esse erro.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_access_private_key"></span>**ERRO \_ CERTIFICADO DO CLIENTE WINHTTP SEM CHAVE PRIVADA DE \_ \_ \_ \_ \_ \_ ACESSO**
</dt> <dd> <dl> <dt>



O aplicativo não tem os privilégios necessários para acessar a chave privada associada ao certificado do cliente.

**Windows Server 2003 com SP1 e Windows XP com SP2:** Não há suporte para esse erro.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_CERT_NO_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_private_key"></span>**ERRO \_ CERTIFICADO DO CLIENTE WINHTTP SEM CHAVE \_ \_ \_ \_ \_ PRIVADA**
</dt> <dd> <dl> <dt>



O contexto para o certificado do cliente SSL não tem uma chave privada associada a ele. O certificado do cliente pode ter sido importado para o computador sem a chave privada.

**Windows Server 2003 com SP1 e Windows XP com SP2:** Não há suporte para esse erro.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CHUNKED_ENCODING_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_chunked_encoding_header_size_overflow"></span>**ERRO ESTOURO DE TAMANHO DO TÍTULO DE CODIFICAÇÃO EM PARTES \_ \_ \_ \_ \_ DO \_ WINHTTP**
</dt> <dd> <dl> <dt>

12183
</dt> <dt>



Retornado por [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) quando uma condição de estouro é encontrada no decorrer da análise da codificação em partes.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERRO \_ WINHTTP \_ CLIENT \_ AUTH \_ CERT \_ NEEDED**
</dt> <dd> <dl> <dt>

12044
</dt> <dt>



Retornado por [**WinHttpReceiveResponse quando o**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) servidor solicita autenticação de cliente.

**Windows Server 2003 com SP1 e Windows XP com SP2:** Não há suporte para esse erro.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CONNECTION_ERROR"></span><span id="error_winhttp_connection_error"></span>**ERRO \_ DE CONEXÃO WINHTTP \_ \_**
</dt> <dd> <dl> <dt>

12030
</dt> <dt>



A conexão com o servidor foi redefinida ou encerrada ou um protocolo SSL incompatível foi encontrado. Por exemplo, o WinHTTP versão 5.1 não dá suporte ao SSL2, a menos que o cliente o habilita especificamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_ALREADY_EXISTS"></span><span id="error_winhttp_header_already_exists"></span>**O \_ ERRO O HEADER WINHTTP \_ JÁ \_ \_ EXISTE**
</dt> <dd> <dl> <dt>

12155
</dt> <dt>



Obsoleto; não é mais usado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_COUNT_EXCEEDED"></span><span id="error_winhttp_header_count_exceeded"></span>**ERRO \_ CONTAGEM DE \_ HEADER WINHTTP \_ \_ EXCEDIDA**
</dt> <dd> <dl> <dt>

12181
</dt> <dt>



Retornado por [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) quando um número maior de títulos estava presente em uma resposta do que o WinHTTP poderia receber.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_NOT_FOUND"></span><span id="error_winhttp_header_not_found"></span>**ERRO \_ O HEADER WINHTTP \_ NÃO \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

12150
</dt> <dt>



O header solicitado não pode ser localizado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_header_size_overflow"></span>**ERRO \_ ESTOURO DE TAMANHO \_ DO TÍTULO \_ WINHTTP \_**
</dt> <dd> <dl> <dt>

12182
</dt> <dt>



Retornado por [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) quando o tamanho dos títulos recebidos excede o limite para o alça de solicitação.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INCORRECT_HANDLE_STATE"></span><span id="error_winhttp_incorrect_handle_state"></span>**ERRO \_ WINHTTP \_ ESTADO INCORRETO DO \_ \_ HANDLE**
</dt> <dd> <dl> <dt>

12019
</dt> <dt>



A operação solicitada não pode ser executada porque o handle fornecido não está no estado correto.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INCORRECT_HANDLE_TYPE"></span><span id="error_winhttp_incorrect_handle_type"></span>**ERRO \_ TIPO DE \_ IDENTIFICADOR INCORRETO WINHTTP \_ \_**
</dt> <dd> <dl> <dt>

12018
</dt> <dt>



O tipo de identificador fornecido está incorreto para essa operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INTERNAL_ERROR"></span><span id="error_winhttp_internal_error"></span>**ERRO \_ WINHTTP \_ INTERNAL \_ ERROR**
</dt> <dd> <dl> <dt>

12004
</dt> <dt>



Ocorreu um erro interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_OPTION"></span><span id="error_winhttp_invalid_option"></span>**ERRO \_ WINHTTP \_ OPÇÃO \_ INVÁLIDA**
</dt> <dd> <dl> <dt>

12009
</dt> <dt>



Uma solicitação [**para WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) ou [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) especificou um valor de opção inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_QUERY_REQUEST"></span><span id="error_winhttp_invalid_query_request"></span>**ERRO \_ SOLICITAÇÃO DE CONSULTA INVÁLIDA WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>

12154
</dt> <dt>



Obsoleto; não é mais usado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_SERVER_RESPONSE"></span><span id="error_winhttp_invalid_server_response"></span>**ERRO \_ WINHTTP \_ RESPOSTA DE SERVIDOR \_ \_ INVÁLIDA**
</dt> <dd> <dl> <dt>

12152
</dt> <dt>



A resposta do servidor não pode ser analisado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_URL"></span><span id="error_winhttp_invalid_url"></span>**ERRO \_ URL INVÁLIDA DE WINHTTP \_ \_**
</dt> <dd> <dl> <dt>

12005
</dt> <dt>



A URL não é válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_LOGIN_FAILURE"></span><span id="error_winhttp_login_failure"></span>**ERRO \_ FALHA DE LOGON DO WINHTTP \_ \_**
</dt> <dd> <dl> <dt>

12015
</dt> <dt>



Falha na tentativa de logon. Quando esse erro é encontrado, o handle de solicitação deve ser fechado com [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle). Um novo alça de solicitação deve ser criado antes de tentar novamente a função que originalmente produziu esse erro.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_NAME_NOT_RESOLVED"></span><span id="error_winhttp_name_not_resolved"></span>**ERRO \_ NOME WINHTTP \_ NÃO \_ \_ RESOLVIDO**
</dt> <dd> <dl> <dt>

12007
</dt> <dt>



O nome do servidor não pode ser resolvido.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_NOT_INITIALIZED"></span><span id="error_winhttp_not_initialized"></span>**ERRO \_ WINHTTP \_ NÃO \_ INICIALIZADO**
</dt> <dd> <dl> <dt>

12172
</dt> <dt>



Obsoleto; não é mais usado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OPERATION_CANCELLED"></span><span id="error_winhttp_operation_cancelled"></span>**ERRO \_ OPERAÇÃO WINHTTP \_ \_ CANCELADA**
</dt> <dd> <dl> <dt>

12017
</dt> <dt>



A operação foi cancelada, geralmente porque o handle no qual a solicitação estava operando foi fechado antes da conclusão da operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OPTION_NOT_SETTABLE"></span><span id="error_winhttp_option_not_settable"></span>**ERRO \_ OPÇÃO WINHTTP \_ NÃO \_ \_ SETTABLE**
</dt> <dd> <dl> <dt>

12011
</dt> <dt>



A opção solicitada não pode ser definida, apenas consultada.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OUT_OF_HANDLES"></span><span id="error_winhttp_out_of_handles"></span>**ERRO \_ WINHTTP \_ FORA DOS \_ \_ ALÇAS**
</dt> <dd> <dl> <dt>

12001
</dt> <dt>



Obsoleto; não é mais usado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_REDIRECT_FAILED"></span><span id="error_winhttp_redirect_failed"></span>**ERRO \_ FALHA NO REDIRECIONAMENTO DE WINHTTP \_ \_**
</dt> <dd> <dl> <dt>

12156
</dt> <dt>



Falha no redirecionamento porque o esquema foi alterado ou todas as tentativas feitas para redirecionamento falharam (o padrão é cinco tentativas).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_RESEND_REQUEST"></span><span id="error_winhttp_resend_request"></span>**ERRO \_ WINHTTP \_ RESEND \_ REQUEST**
</dt> <dd> <dl> <dt>

12032
</dt> <dt>



Falha na função WinHTTP. A função desejada pode ser recuperada no mesmo handle de solicitação.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW"></span><span id="error_winhttp_response_drain_overflow"></span>**ERRO \_ WINHTTP \_ RESPONSE DRAIN \_ \_ OVERFLOW**
</dt> <dd> <dl> <dt>

12184
</dt> <dt>



Retornado quando uma resposta de entrada excede um limite de tamanho winHTTP interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SCRIPT_EXECUTION_ERROR"></span><span id="error_winhttp_script_execution_error"></span>**ERRO \_ DE EXECUÇÃO DE SCRIPT WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>

12177
</dt> <dt>



Foi encontrado um erro durante a execução de um script.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_CN_INVALID"></span><span id="error_winhttp_secure_cert_cn_invalid"></span>**ERRO \_ WINHTTP \_ SECURE CERT CN \_ \_ \_ INVÁLIDO**
</dt> <dd> <dl> <dt>

12038
</dt> <dt>



Retornado quando um nome CN do certificado não corresponde ao valor passado (equivalente a **um erro CERT E CN NO \_ \_ \_ \_ MATCH).**


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_DATE_INVALID"></span><span id="error_winhttp_secure_cert_date_invalid"></span>**ERRO \_ WINHTTP \_ SECURE CERT DATE \_ \_ \_ INVALID**
</dt> <dd> <dl> <dt>

12037
</dt> <dt>



Indica que um certificado necessário não está dentro de seu período de validade ao verificar em relação ao relógio do sistema atual ou ao timestamp no arquivo assinado ou que os períodos de validade da cadeia de certificação não são aninhados corretamente (equivalente a **um erro CERT E \_ \_ EXPIRED** ou **CERT E \_ \_ VALIDITYPERIODNESTING).**


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_REV_FAILED"></span><span id="error_winhttp_secure_cert_rev_failed"></span>**ERRO \_ FALHA NA REV DO CERTIFICADO DO WINHTTP \_ \_ \_ \_ SECURE**
</dt> <dd> <dl> <dt>

12057
</dt> <dt>



Indica que a revogação não pode ser verificada porque o servidor de revogação estava offline (equivalente a **CRYPT \_ E \_ REVOCATION \_ OFFLINE).**


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_REVOKED"></span><span id="error_winhttp_secure_cert_revoked"></span>**ERRO \_ WINHTTP \_ SECURE CERT \_ \_ REVOGADO**
</dt> <dd> <dl> <dt>

12170
</dt> <dt>



Indica que um certificado foi revogado (equivalente a **CRYPT \_ E \_ REVOKED).**


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_WRONG_USAGE"></span><span id="error_winhttp_secure_cert_wrong_usage"></span>**ERRO \_ USO ERRADO DO CERTIFICADO \_ \_ WINHTTP SECURE \_ \_ CERT**
</dt> <dd> <dl> <dt>

12179
</dt> <dt>



Indica que um certificado não é válido para o uso solicitado (equivalente a **CERT \_ E WRONG \_ \_ USAGE**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CHANNEL_ERROR"></span><span id="error_winhttp_secure_channel_error"></span>**ERRO \_ WINHTTP \_ SECURE CHANNEL \_ \_ ERROR**
</dt> <dd> <dl> <dt>

12157
</dt> <dt>



Indica que ocorreu um erro relacionado a um canal seguro (equivalente a códigos de erro que começam com "SEC E" e "SEC I" listados no arquivo de título \_ \_ \_ \_ "winerror.h").


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_FAILURE"></span><span id="error_winhttp_secure_failure"></span>**ERRO \_ WINHTTP \_ SECURE \_ FAILURE**
</dt> <dd> <dl> <dt>

12175
</dt> <dt>



Um ou mais erros foram encontrados no certificado protocolo SSL (SSL) enviado pelo servidor. Para determinar qual tipo de erro foi encontrado, verifique se há uma notificação [**WINHTTP \_ CALLBACK \_ STATUS SECURE \_ \_ FAILURE**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) em uma função de retorno de chamada de status. Para obter mais informações, consulte [**WINHTTP \_ STATUS \_ CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_INVALID_CA"></span><span id="error_winhttp_secure_invalid_ca"></span>**ERRO \_ WINHTTP \_ SECURE INVALID \_ \_ CA**
</dt> <dd> <dl> <dt>

12045
</dt> <dt>



Indica que uma cadeia de certificados foi processada, mas encerrada em um certificado raiz que não é confiável para o provedor de confiança (equivalente a **CERT \_ E \_ UNTRUSTEDROOT**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_INVALID_CERT"></span><span id="error_winhttp_secure_invalid_cert"></span>**ERRO \_ WINHTTP \_ SECURE CERTIFICADO \_ \_ INVÁLIDO**
</dt> <dd> <dl> <dt>

12169
</dt> <dt>



Indica que um certificado é inválido (equivalente a erros como **CERT \_ E \_ ROLE,** **CERT E \_ \_ PATHLENCONST,** **CERT E \_ \_ CRITICAL,** **CERT E \_ \_ PURPOSE**, **CERT E \_ \_ ISSUERC LTDING,** **CERT E \_ \_ MALFORMED** **e CERT E \_ \_ CHAINING).**


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SHUTDOWN"></span><span id="error_winhttp_shutdown"></span>**ERRO \_ WINHTTP \_ SHUTDOWN**
</dt> <dd> <dl> <dt>

12012
</dt> <dt>



O suporte à função WinHTTP está sendo desligado ou descarregado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_TIMEOUT"></span><span id="error_winhttp_timeout"></span>**ERRO \_ WINHTTP \_ TIMEOUT**
</dt> <dd> <dl> <dt>

12002
</dt> <dt>



O tempo limite da solicitação foi atingido.

Esse erro pode ser retornado como resultado do comportamento de tempo-out de TCP/IP, independentemente dos valores de tempo-Windows HTTP Services.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_winhttp_unable_to_download_script"></span>**ERRO \_ WINHTTP \_ NÃO É POSSÍVEL BAIXAR O \_ \_ \_ SCRIPT**
</dt> <dd> <dl> <dt>

12167
</dt> <dt>



O arquivo PAC não pode ser baixado. Por exemplo, o servidor referenciado pela URL do PAC pode não ter sido acessível ou o servidor retornou uma resposta 404 NOT FOUND.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNHANDLED_SCRIPT_TYPE"></span><span id="error_winhttp_unhandled_script_type"></span>**ERRO \_ TIPO DE SCRIPT WINHTTP SEM \_ \_ \_ IDENTIFICADOR**
</dt> <dd> <dl> <dt>

12176
</dt> <dt>



Não há suporte para o tipo de script.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNRECOGNIZED_SCHEME"></span><span id="error_winhttp_unrecognized_scheme"></span>**ERRO \_ WINHTTP \_ ESQUEMA NÃO RECOGNIZADO \_**
</dt> <dd> <dl> <dt>

12006
</dt> <dt>



A URL especificou um esquema diferente de "http:" ou "https:".


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERRO \_ SEM \_ MEMÓRIA \_ SUFICIENTE**
</dt> <dd> <dl> <dt>



Não havia memória suficiente disponível para concluir a operação solicitada.

**Header:** Declarado em Winerror.h


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERRO \_ BUFFER \_ INSUFICIENTE**
</dt> <dd> <dl> <dt>



O tamanho, em bytes, do buffer fornecido a uma função era insuficiente para conter os dados retornados. Para obter mais informações, consulte a função específica.

**Header:** Declarado em Winerror.h


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR \_ INVALID \_ HANDLE**
</dt> <dd> <dl> <dt>



O handle passado para a API (interface de programação de aplicativo) foi invalidado ou fechado.

**Header:** Declarado em Winerror.h


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERRO \_ NÃO HÁ MAIS \_ \_ ARQUIVOS**
</dt> <dd> <dl> <dt>



Não foram encontrados mais arquivos.

**Header:** Declarado em Winerror.h


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERRO \_ NÃO HÁ MAIS \_ \_ ITENS**
</dt> <dd> <dl> <dt>



Nenhum outro item foi encontrado.

**Header:** Declarado em Winerror.h


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERRO \_ SEM \_ SUPORTE**
</dt> <dd> <dl> <dt>



A pilha de protocolo necessária não é carregada e o aplicativo não pode iniciar o WinSock.

**Header:** Declarado em Winerror.h


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Para Windows XP e Windows 2000, consulte [](winhttp-start-page.md) a seção Requisitos de tempo de executar da página inicial do WinHttp.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP, Windows 2000 Professional somente com aplicativos da área de trabalho SP3 \[\]<br/>            |
| Servidor mínimo com suporte<br/> | Windows Server 2003, Windows 2000 Server com somente aplicativos da área de trabalho SP3 \[\]<br/>         |
| Redistribuível<br/>          | WinHTTP 5.0 e Internet Explorer 5.01 ou posterior no Windows XP e Windows 2000.<br/> |
| Cabeçalho<br/>                   | <dl> <dt>Winhttp.h</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Versões do WinHTTP](winhttp-versions.md)
</dt> </dl>

 

