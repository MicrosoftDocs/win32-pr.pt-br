---
description: Os valores de erro identificados neste tópico são retornados por GetLastError quando uma das funções do Microsoft Windows HTTP Services (WinHTTP) falha.
ms.assetid: c8a863cd-d36c-4ec8-ac49-0b714a5e4cc2
title: Mensagens de erro (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eccdc8be4b1e7c3cc7f9a03403c2f8778ddd19b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828946"
---
# <a name="error-messages-winhttph"></a>Mensagens de erro (WinHTTP. h)

Os valores de erro listados abaixo são retornados por [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando uma das funções do Microsoft Windows http Services (WinHTTP) falha, e também são retornadas nos 16 bits inferiores do [**HRESULT**](../com/structure-of-com-error-codes.md) Error retornado do objeto [**WinHttpRequest**](winhttprequest.md) .

Os valores de erro cujos nomes começam com "ERROR \_ WinHTTP \_ " são específicos para as funções de WinHTTP. As funções WinHTTP também retornam mensagens de erro do Windows, quando apropriado.

<dl> <dt>

<span id="ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR"></span><span id="error_winhttp_auto_proxy_service_error"></span>**ERRO \_ WinHTTP erro de \_ \_ serviço de proxy automático \_ \_**
</dt> <dd> <dl> <dt>

12178
</dt> <dt>



Retornado por [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) quando um proxy para a URL especificada não pode ser localizado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_AUTODETECTION_FAILED"></span><span id="error_winhttp_autodetection_failed"></span>**ERRO de detecção automática de \_ WinHTTP \_ \_ falhou**
</dt> <dd> <dl> <dt>

12180
</dt> <dt>



Retornado por [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) se o WinHTTP não puder descobrir a URL do Arquivo PAC (configuração automática de proxy).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_winhttp_bad_auto_proxy_script"></span>**ERRO \_ WinHTTP \_ - \_ \_ script de proxy automático insatisfatório \_**
</dt> <dd> <dl> <dt>

12166
</dt> <dt>



Ocorreu um erro ao executar o código de script no arquivo PAC (configuração automática de proxy).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_OPEN"></span><span id="error_winhttp_cannot_call_after_open"></span>**ERRO \_ WinHTTP \_ não pode \_ chamar \_ após \_ abrir**
</dt> <dd> <dl> <dt>

12103
</dt> <dt>



Retornado pelo objeto [**HttpRequest**](winhttprequest.md) se uma opção especificada não puder ser solicitada depois que o método [**Open**](iwinhttprequest-open.md) tiver sido chamado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_SEND"></span><span id="error_winhttp_cannot_call_after_send"></span>**ERRO \_ WinHTTP \_ não pode \_ chamar \_ após \_ envio**
</dt> <dd> <dl> <dt>

12102
</dt> <dt>



Retornado pelo objeto [**HttpRequest**](winhttprequest.md) se uma operação solicitada não puder ser executada Depois de chamar o método [**Send**](iwinhttprequest-send.md) .


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_OPEN"></span><span id="error_winhttp_cannot_call_before_open"></span>**ERRO \_ WinHTTP \_ não pode \_ chamar \_ antes de \_ abrir**
</dt> <dd> <dl> <dt>

12100
</dt> <dt>



Retornado pelo objeto [**HttpRequest**](winhttprequest.md) se uma operação solicitada não puder ser executada antes de chamar o método [**Open**](iwinhttprequest-open.md) .


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_SEND"></span><span id="error_winhttp_cannot_call_before_send"></span>**ERRO \_ WinHTTP \_ não pode \_ chamar \_ antes de \_ Enviar**
</dt> <dd> <dl> <dt>

12101
</dt> <dt>



Retornado pelo objeto [**HttpRequest**](winhttprequest.md) se uma operação solicitada não puder ser executada antes de chamar o método [**Send**](iwinhttprequest-send.md) .


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CONNECT"></span><span id="error_winhttp_cannot_connect"></span>**ERRO \_ WinHTTP \_ não pode \_ conectar**
</dt> <dd> <dl> <dt>

12029
</dt> <dt>



Retornado se a conexão com o servidor falhou.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERRO \_ de \_ certificado de autenticação de cliente WinHTTP \_ \_ \_ necessário**
</dt> <dd> <dl> <dt>



O servidor requer autenticação de cliente SSL. O aplicativo recupera a lista de emissores de certificado chamando [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) com a opção **WinHTTP lista de \_ emissor de \_ \_ certificado de \_ \_ cliente** . Para obter mais informações, consulte **a \_ opção \_ WinHTTP \_ \_ \_ lista de emissor de certificado de cliente** .

Se o servidor solicitar o certificado de cliente, mas não precisar dele, o aplicativo poderá chamar [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) alternadamente com a opção **WinHTTP de contexto de \_ \_ \_ certificado \_ de cliente** . Nesse caso, o aplicativo especifica a macro WINHTTP \_ no \_ \_ contexto de certificado do cliente \_ no parâmetro *lpBuffer* de **WinHttpSetOption**. Para obter mais informações, consulte opção **WinHTTP de contexto de certificado de \_ \_ cliente \_ \_ de opção** .

**Windows Server 2003 com SP1 e Windows XP com SP2:** Não há suporte para esse erro.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_access_private_key"></span>**ERRO \_ WinHTTP \_ Client \_ CERT \_ sem \_ acesso \_ à \_ chave privada**
</dt> <dd> <dl> <dt>



O aplicativo não tem os privilégios necessários para acessar a chave privada associada ao certificado do cliente.

**Windows Server 2003 com SP1 e Windows XP com SP2:** Não há suporte para esse erro.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_CERT_NO_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_private_key"></span>**ERRO \_ WinHTTP \_ Client \_ CERT \_ sem \_ \_ chave privada**
</dt> <dd> <dl> <dt>



O contexto do certificado de cliente SSL não tem uma chave privada associada a ele. O certificado do cliente pode ter sido importado para o computador sem a chave privada.

**Windows Server 2003 com SP1 e Windows XP com SP2:** Não há suporte para esse erro.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CHUNKED_ENCODING_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_chunked_encoding_header_size_overflow"></span>**ERRO \_ WinHTTP de \_ tamanho do cabeçalho de codificação em partes \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

12183
</dt> <dt>



Retornado por [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) quando uma condição de estouro é encontrada no curso da análise de codificação em bloco.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERRO \_ de \_ certificado de autenticação de cliente WinHTTP \_ \_ \_ necessário**
</dt> <dd> <dl> <dt>

12044
</dt> <dt>



Retornado por [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) quando o servidor solicita autenticação de cliente.

**Windows Server 2003 com SP1 e Windows XP com SP2:** Não há suporte para esse erro.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CONNECTION_ERROR"></span><span id="error_winhttp_connection_error"></span>**erro \_ de \_ conexão de WinHTTP \_**
</dt> <dd> <dl> <dt>

12030
</dt> <dt>



A conexão com o servidor foi redefinida ou encerrada ou um protocolo SSL incompatível foi encontrado. Por exemplo, o WinHTTP versão 5,1 não oferece suporte a SSL2, a menos que o cliente o habilite especificamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_ALREADY_EXISTS"></span><span id="error_winhttp_header_already_exists"></span>**o \_ cabeçalho WinHTTP de erro \_ \_ já \_ existe**
</dt> <dd> <dl> <dt>

12155
</dt> <dt>



Substituí Não é mais usado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_COUNT_EXCEEDED"></span><span id="error_winhttp_header_count_exceeded"></span>**ERRO \_ de \_ contagem de cabeçalho WinHTTP \_ \_ excedida**
</dt> <dd> <dl> <dt>

12181
</dt> <dt>



Retornado por [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) quando um número maior de cabeçalhos estava presente em uma resposta do que o WinHTTP poderia receber.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_NOT_FOUND"></span><span id="error_winhttp_header_not_found"></span>**ERRO \_ de \_ cabeçalho WinHTTP \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

12150
</dt> <dt>



O cabeçalho solicitado não pode ser localizado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_header_size_overflow"></span>**ERRO \_ de \_ \_ estouro no tamanho do cabeçalho WinHTTP \_**
</dt> <dd> <dl> <dt>

12182
</dt> <dt>



Retornado por [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) quando o tamanho dos cabeçalhos recebidos excede o limite para o identificador de solicitação.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INCORRECT_HANDLE_STATE"></span><span id="error_winhttp_incorrect_handle_state"></span>**ERRO \_ WinHTTP \_ \_ estado de identificador incorreto \_**
</dt> <dd> <dl> <dt>

12019
</dt> <dt>



A operação solicitada não pode ser executada porque o identificador fornecido não está no estado correto.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INCORRECT_HANDLE_TYPE"></span><span id="error_winhttp_incorrect_handle_type"></span>**ERRO \_ WinHTTP \_ \_ tipo de identificador incorreto \_**
</dt> <dd> <dl> <dt>

12018
</dt> <dt>



O tipo de identificador fornecido está incorreto para esta operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INTERNAL_ERROR"></span><span id="error_winhttp_internal_error"></span>**erro \_ interno de WinHTTP \_ \_**
</dt> <dd> <dl> <dt>

12004
</dt> <dt>



Ocorreu um erro interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_OPTION"></span><span id="error_winhttp_invalid_option"></span>**ERRO \_ WinHTTP \_ opção inválida \_**
</dt> <dd> <dl> <dt>

12009
</dt> <dt>



Uma solicitação para [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) ou [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) especificou um valor de opção inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_QUERY_REQUEST"></span><span id="error_winhttp_invalid_query_request"></span>**ERRO \_ WinHTTP \_ \_ solicitação de consulta inválida \_**
</dt> <dd> <dl> <dt>

12154
</dt> <dt>



Substituí Não é mais usado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_SERVER_RESPONSE"></span><span id="error_winhttp_invalid_server_response"></span>**ERRO \_ WinHTTP \_ \_ resposta de servidor inválida \_**
</dt> <dd> <dl> <dt>

12152
</dt> <dt>



Não é possível analisar a resposta do servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_URL"></span><span id="error_winhttp_invalid_url"></span>**ERRO \_ ao \_ WinHTTP \_ URL inválido**
</dt> <dd> <dl> <dt>

12005
</dt> <dt>



A URL não é válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_LOGIN_FAILURE"></span><span id="error_winhttp_login_failure"></span>**ERRO \_ de \_ falha de logon WinHTTP \_**
</dt> <dd> <dl> <dt>

12015
</dt> <dt>



Falha na tentativa de logon. Quando esse erro é encontrado, o identificador de solicitação deve ser fechado com [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle). Um novo identificador de solicitação deve ser criado antes de tentar novamente a função que produziu esse erro originalmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_NAME_NOT_RESOLVED"></span><span id="error_winhttp_name_not_resolved"></span>**ERRO \_ WinHTTP \_ nome \_ não \_ resolvido**
</dt> <dd> <dl> <dt>

12007
</dt> <dt>



O nome do servidor não pode ser resolvido.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_NOT_INITIALIZED"></span><span id="error_winhttp_not_initialized"></span>**ERRO \_ WinHTTP \_ não \_ inicializado**
</dt> <dd> <dl> <dt>

12172
</dt> <dt>



Substituí Não é mais usado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OPERATION_CANCELLED"></span><span id="error_winhttp_operation_cancelled"></span>**ERRO \_ de \_ operação WinHTTP \_ cancelada**
</dt> <dd> <dl> <dt>

12017
</dt> <dt>



A operação foi cancelada, geralmente porque o identificador no qual a solicitação estava operando foi fechado antes da operação ser concluída.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OPTION_NOT_SETTABLE"></span><span id="error_winhttp_option_not_settable"></span>**ERRO \_ de \_ opção WinHTTP \_ não \_ configurável**
</dt> <dd> <dl> <dt>

12011
</dt> <dt>



A opção solicitada não pode ser definida, somente consultada.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OUT_OF_HANDLES"></span><span id="error_winhttp_out_of_handles"></span>**ERRO \_ WinHTTP \_ fora \_ de \_ identificadores**
</dt> <dd> <dl> <dt>

12001
</dt> <dt>



Substituí Não é mais usado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_REDIRECT_FAILED"></span><span id="error_winhttp_redirect_failed"></span>**ERRO \_ \_ ao redirecionar WinHTTP \_**
</dt> <dd> <dl> <dt>

12156
</dt> <dt>



Falha no redirecionamento porque o esquema foi alterado ou todas as tentativas feitas para redirecionamento falharam (o padrão é cinco tentativas).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_RESEND_REQUEST"></span><span id="error_winhttp_resend_request"></span>**ERRO \_ de \_ solicitação de reenvio de WinHTTP \_**
</dt> <dd> <dl> <dt>

12032
</dt> <dt>



A função WinHTTP falhou. A função desejada pode ser repetida no mesmo identificador de solicitação.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW"></span><span id="error_winhttp_response_drain_overflow"></span>**ERRO \_ de \_ \_ estouro de esgotamento de resposta de WinHTTP \_**
</dt> <dd> <dl> <dt>

12184
</dt> <dt>



Retornado quando uma resposta de entrada excede um limite de tamanho de WinHTTP interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SCRIPT_EXECUTION_ERROR"></span><span id="error_winhttp_script_execution_error"></span>**erro \_ de \_ \_ erro de execução de script WinHTTP \_**
</dt> <dd> <dl> <dt>

12177
</dt> <dt>



Foi encontrado um erro ao executar um script.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_CN_INVALID"></span><span id="error_winhttp_secure_cert_cn_invalid"></span>**ERRO \_ WinHTTP \_ Secure \_ CERT \_ CN \_ inválido**
</dt> <dd> <dl> <dt>

12038
</dt> <dt>



Retornado quando um nome CN do certificado não corresponde ao valor transmitido (equivalente a um erro de **certificado \_ E \_ CN \_ sem \_ correspondência** ).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_DATE_INVALID"></span><span id="error_winhttp_secure_cert_date_invalid"></span>**ERRO \_ WinHTTP \_ Secure \_ CERT \_ Date \_ inválido**
</dt> <dd> <dl> <dt>

12037
</dt> <dt>



Indica que um certificado necessário não está dentro de seu período de validade ao verificar em relação ao relógio do sistema atual ou ao carimbo de data/hora no arquivo assinado, ou que os períodos de validade da cadeia de certificação não são aninhados corretamente (equivalente a um **certificado \_ e \_ expirado** ou a um erro **\_ e \_ VALIDITYPERIODNESTING** ).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_REV_FAILED"></span><span id="error_winhttp_secure_cert_rev_failed"></span>**ERRO \_ WinHTTP \_ Secure \_ CERT \_ rev \_ falhou**
</dt> <dd> <dl> <dt>

12057
</dt> <dt>



Indica que a revogação não pode ser verificada porque o servidor de revogação estava offline (equivalente a **criptografada \_ E \_ revogação \_ offline**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_REVOKED"></span><span id="error_winhttp_secure_cert_revoked"></span>**ERRO \_ WinHTTP \_ Secure \_ CERT \_ revogado**
</dt> <dd> <dl> <dt>

12170
</dt> <dt>



Indica que um certificado foi revogado (equivalente a cript. **\_ E \_ revogado**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_WRONG_USAGE"></span><span id="error_winhttp_secure_cert_wrong_usage"></span>**ERRO \_ WinHTTP \_ - \_ \_ uso errado de certificado seguro \_**
</dt> <dd> <dl> <dt>

12179
</dt> <dt>



Indica que um certificado não é válido para o uso solicitado (equivalente ao **certificado \_ E \_ \_ uso incorreto**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CHANNEL_ERROR"></span><span id="error_winhttp_secure_channel_error"></span>**erro de erro de \_ \_ canal seguro de WinHTTP \_ \_**
</dt> <dd> <dl> <dt>

12157
</dt> <dt>



Indica que ocorreu um erro ao fazer com um canal seguro (equivalente a códigos de erro que começam com "SEC \_ e \_ " e "s \_ I \_ " listados no arquivo de cabeçalho "Winerror. h").


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_FAILURE"></span><span id="error_winhttp_secure_failure"></span>**ERRO de \_ falha de WinHTTP \_ seguro \_**
</dt> <dd> <dl> <dt>

12175
</dt> <dt>



Um ou mais erros foram encontrados no certificado de protocolo SSL (SSL) enviado pelo servidor. Para determinar que tipo de erro foi encontrado, verifique se há uma notificação de [**\_ \_ \_ \_ falha segura de status de retorno de chamada do WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) em uma função de retorno de chamada de status. Para obter mais informações, [**consulte \_ retorno de \_ chamada de status do WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_INVALID_CA"></span><span id="error_winhttp_secure_invalid_ca"></span>**ERRO \_ WinHTTP \_ Secure \_ AC inválida \_**
</dt> <dd> <dl> <dt>

12045
</dt> <dt>



Indica que uma cadeia de certificados foi processada, mas terminada em um certificado raiz que não é confiável pelo provedor de confiança (equivalente a **CERT \_ E \_ UNTRUSTEDROOT**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_INVALID_CERT"></span><span id="error_winhttp_secure_invalid_cert"></span>**ERRO \_ WinHTTP \_ Secure \_ \_ CERT inválido**
</dt> <dd> <dl> <dt>

12169
</dt> <dt>



Indica que um certificado é inválido (equivalente a erros como a **\_ \_ função CERT e**, **CERT \_ e \_ PATHLENCONST**, **CERT \_ e \_ Critical**, CERT e **\_ \_ propósito**, **CERT \_ e \_ ISSUERCHAINING**, **CERT \_ e \_** **\_ \_ encadeado e CERT**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SHUTDOWN"></span><span id="error_winhttp_shutdown"></span>**ERRO \_ de \_ desligamento de WinHTTP**
</dt> <dd> <dl> <dt>

12012
</dt> <dt>



O suporte à função WinHTTP está sendo desligado ou descarregado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_TIMEOUT"></span><span id="error_winhttp_timeout"></span>**ERRO de \_ WinHTTP \_ Timeout**
</dt> <dd> <dl> <dt>

12002
</dt> <dt>



O tempo limite da solicitação foi atingido.

Esse erro pode ser retornado como resultado do comportamento de tempo limite de TCP/IP, independentemente dos valores de tempo limite definidos nos serviços HTTP do Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_winhttp_unable_to_download_script"></span>**ERRO \_ WinHTTP \_ não é possível \_ \_ baixar o \_ script**
</dt> <dd> <dl> <dt>

12167
</dt> <dt>



Não é possível baixar o arquivo PAC. Por exemplo, o servidor referenciado pela URL de PAC pode não ter sido acessado ou o servidor retornou uma resposta 404 não encontrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNHANDLED_SCRIPT_TYPE"></span><span id="error_winhttp_unhandled_script_type"></span>**ERRO \_ WinHTTP \_ tipo de script sem tratamento \_ \_**
</dt> <dd> <dl> <dt>

12176
</dt> <dt>



Não há suporte para o tipo de script.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNRECOGNIZED_SCHEME"></span><span id="error_winhttp_unrecognized_scheme"></span>**ERRO \_ WinHTTP \_ esquema não reconhecido \_**
</dt> <dd> <dl> <dt>

12006
</dt> <dt>



A URL especificou um esquema diferente de "http:" ou "https:".


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERRO \_ de \_ memória insuficiente \_**
</dt> <dd> <dl> <dt>



Não havia memória suficiente disponível para concluir a operação solicitada.

**Cabeçalho:** Declarado em Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERRO \_ de \_ buffer insuficiente**
</dt> <dd> <dl> <dt>



O tamanho, em bytes, do buffer fornecido a uma função era insuficiente para conter os dados retornados. Para obter mais informações, consulte a função específica.

**Cabeçalho:** Declarado em Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**\_identificador inválido do erro \_**
</dt> <dd> <dl> <dt>



O identificador passado para a API (interface de programação de aplicativo) foi invalidado ou fechado.

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


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERRO \_ sem \_ suporte**
</dt> <dd> <dl> <dt>



A pilha de protocolos necessária não está carregada e o aplicativo não pode iniciar o WinSock.

**Cabeçalho:** Declarado em Winerror. h


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]<br/>            |
| Servidor mínimo com suporte<br/> | Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]<br/>         |
| Redistribuível<br/>          | WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.<br/> |
| parâmetro<br/>                   | <dl> <dt>WinHTTP. h</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Versões do WinHTTP](winhttp-versions.md)
</dt> </dl>

 

