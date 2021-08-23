---
title: HTTP_LOG_FIELD_ constantes (Http.h)
description: Defina os campos no log do W3C e nos logs de erro.
ms.assetid: 44307d5a-f413-4ee9-9f9c-586c824d5493
topic_type:
- apiref
api_name:
- HTTP_LOG_FIELD_DATE
- HTTP_LOG_FIELD_TIME
- HTTP_LOG_FIELD_CLIENT_IP
- HTTP_LOG_FIELD_USER_NAME
- HTTP_LOG_FIELD_SITE_NAME
- HTTP_LOG_FIELD_COMPUTER_NAME
- HTTP_LOG_FIELD_SERVER_IP
- HTTP_LOG_FIELD_METHOD
- HTTP_LOG_FIELD_URI_STEM
- HTTP_LOG_FIELD_URI_QUERY
- HTTP_LOG_FIELD_STATUS
- HTTP_LOG_FIELD_WIN32_STATUS
- HTTP_LOG_FIELD_BYTES_SENT
- HTTP_LOG_FIELD_BYTES_RECV
- HTTP_LOG_FIELD_TIME_TAKEN
- HTTP_LOG_FIELD_SERVER_PORT
- HTTP_LOG_FIELD_USER_AGENT
- HTTP_LOG_FIELD_COOKIE
- HTTP_LOG_FIELD_REFERER
- HTTP_LOG_FIELD_VERSION
- HTTP_LOG_FIELD_HOST
- HTTP_LOG_FIELD_SUB_STATUS
- HTTP_LOG_FIELD_CLIENT_PORT
- HTTP_LOG_FIELD_URI
- HTTP_LOG_FIELD_SITE_ID
- HTTP_LOG_FIELD_REASON
- HTTP_LOG_FIELD_QUEUE_NAME
- HTTP_LOG_FIELD_STREAMID
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 616caaed9829c7f926f95f8982033457e1835a6beccfcad8313f6624d68195db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950825"
---
# <a name="http_log_field_-constants"></a>Constantes \_ DE \_ CAMPO DE LOG HTTP \_

As **constantes \_ HTTP LOG \_ FIELD \_** definem os campos no log do W3C e nos logs de erro.

Essas constantes são usadas na estrutura [**HTTP \_ LOGGING \_ INFO.**](/windows/desktop/api/Http/ns-http-http_logging_info)

<dl> <dt>

<span id="HTTP_LOG_FIELD_DATE"></span><span id="http_log_field_date"></span>**DATA DO \_ CAMPO DE LOG \_ \_ HTTP**
</dt> <dd> <dl> <dt>



A data em que a atividade ocorreu.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_TIME"></span><span id="http_log_field_time"></span>**HORA DO \_ CAMPO DE LOG \_ \_ HTTP**
</dt> <dd> <dl> <dt>



A hora, em UTC (tempo universal coordenado), em que a atividade ocorreu.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_CLIENT_IP"></span><span id="http_log_field_client_ip"></span>**IP \_ DO CLIENTE DO CAMPO DE LOG \_ \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Endereço IP do cliente que fez a solicitação.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_USER_NAME"></span><span id="http_log_field_user_name"></span>**NOME \_ DE USUÁRIO DO CAMPO \_ \_ DE LOG \_ HTTP**
</dt> <dd> <dl> <dt>



O nome do usuário autenticado que acessou o servidor. Os usuários anônimos são indicados por um hífen.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SITE_NAME"></span><span id="http_log_field_site_name"></span>**NOME \_ DO SITE DO CAMPO \_ \_ DE LOG \_ HTTP**
</dt> <dd> <dl> <dt>



O nome do site no qual a entrada do arquivo de log foi gerada.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_COMPUTER_NAME"></span><span id="_http_log_field_computer_name"></span>**HTTP \_ NOME \_ DO COMPUTADOR DO CAMPO DE \_ \_ LOG**
</dt> <dd> <dl> <dt>



O nome do computador no qual a entrada do arquivo de log foi gerada.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SERVER_IP"></span><span id="http_log_field_server_ip"></span>**IP \_ DO SERVIDOR DE CAMPO DE LOG \_ \_ \_ HTTP**
</dt> <dd> <dl> <dt>



O endereço IP do servidor no qual a entrada do arquivo de log foi gerada.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_METHOD"></span><span id="http_log_field_method"></span>**MÉTODO DE \_ CAMPO DE LOG \_ \_ HTTP**
</dt> <dd> <dl> <dt>



A ação solicitada, por exemplo, um método get.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_URI_STEM"></span><span id="_http_log_field_uri_stem"></span>**HTTP \_ STEM \_ DO URI DO CAMPO \_ DE \_ LOG**
</dt> <dd> <dl> <dt>



O destino da ação, por exemplo, Default.htm.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_URI_QUERY"></span><span id="http_log_field_uri_query"></span>**CONSULTA \_ DE \_ URI DO \_ CAMPO \_ DE LOG HTTP**
</dt> <dd> <dl> <dt>



A consulta, se alguma, que o cliente estava tentando executar. Um URI (Resource Identifier Universal) consulta é necessário apenas para páginas dinâmico.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_STATUS"></span><span id="http_log_field_status"></span>**STATUS \_ DO CAMPO DE LOG \_ \_ HTTP**
</dt> <dd> <dl> <dt>



O código de status HTTP.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_WIN32_STATUS"></span><span id="http_log_field_win32_status"></span>**STATUS \_ DO \_ \_ WIN32 DO CAMPO DE \_ LOG HTTP**
</dt> <dd> <dl> <dt>



O Windows de status.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_BYTES_SENT"></span><span id="http_log_field_bytes_sent"></span>**BYTES \_ DE CAMPO DE LOG HTTP \_ \_ \_ ENVIADOS**
</dt> <dd> <dl> <dt>



O número, em bytes, enviado pelo servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_BYTES_RECV"></span><span id="http_log_field_bytes_recv"></span>**RECV \_ DE BYTES DO CAMPO \_ \_ \_ DE LOG HTTP**
</dt> <dd> <dl> <dt>



O número, em bytes, recebido pelo servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_TIME_TAKEN"></span><span id="http_log_field_time_taken"></span>**TEMPO \_ DE USO DO CAMPO \_ \_ DE LOG \_ HTTP**
</dt> <dd> <dl> <dt>



O tempo, em milissegundos, da ação.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SERVER_PORT"></span><span id="http_log_field_server_port"></span>**PORTA \_ DO SERVIDOR DE CAMPO \_ \_ DE LOG \_ HTTP**
</dt> <dd> <dl> <dt>



O número da porta do servidor configurado para o serviço.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_USER_AGENT"></span><span id="_http_log_field_user_agent"></span>**HTTP \_ AGENTE \_ DE USUÁRIO DO CAMPO DE \_ \_ LOG**
</dt> <dd> <dl> <dt>



O aplicativo que o cliente usou.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_COOKIE"></span><span id="http_log_field_cookie"></span>**COOKIE DE \_ CAMPO DE LOG \_ \_ HTTP**
</dt> <dd> <dl> <dt>



O conteúdo do cookie enviado ou recebido, se for o caso.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_REFERER"></span><span id="http_log_field_referer"></span>**REFERENCIADOR \_ DE CAMPO DE LOG \_ \_ HTTP**
</dt> <dd> <dl> <dt>



O site que o usuário visitou pela última vez. Esse site fornece um link para o site atual.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_VERSION"></span><span id="http_log_field_version"></span>**VERSÃO \_ DO CAMPO DE LOG \_ \_ HTTP**
</dt> <dd> <dl> <dt>



A versão do protocolo HTTP que o cliente usou.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_HOST"></span><span id="http_log_field_host"></span>**HOST \_ DO CAMPO DE LOG \_ \_ HTTP**
</dt> <dd> <dl> <dt>



O nome do header do host, se for o caso.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SUB_STATUS"></span><span id="http_log_field_sub_status"></span>**SUB STATUS \_ DO CAMPO DE LOG \_ \_ \_ HTTP**
</dt> <dd> <dl> <dt>



O código de erro substatus.


</dt> </dl> </dd> </dl>

As constantes a seguir são usadas para o log de erros HTTP.

<dl> <dt>

<span id="HTTP_LOG_FIELD_CLIENT_PORT"></span><span id="http_log_field_client_port"></span>**PORTA \_ DO CLIENTE DO CAMPO \_ \_ DE LOG \_ HTTP**
</dt> <dd> <dl> <dt>



O número da porta do cliente do qual a solicitação é recebida. Esse campo de log só é usado para registro em log de erros.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_URI"></span><span id="http_log_field_uri"></span>**\_URI DO \_ CAMPO DE LOG \_ HTTP**
</dt> <dd> <dl> <dt>



O URI recebido na solicitação, incluindo a parte da consulta. Esse campo de log só é usado para registro em log de erros.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SITE_ID"></span><span id="http_log_field_site_id"></span>**\_ID DO \_ SITE DO \_ CAMPO \_ DE LOG HTTP**
</dt> <dd> <dl> <dt>



A ID numérica específica do aplicativo do Grupo de URL no qual a solicitação é roteada. Esse campo de log só é usado para registro em log de erros.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_REASON"></span><span id="http_log_field_reason"></span>**MOTIVO \_ DO CAMPO DE LOG \_ \_ HTTP**
</dt> <dd> <dl> <dt>



A frase de motivo do erro. Esse campo de log só é usado para registro em log de erros.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_QUEUE_NAME"></span><span id="http_log_field_queue_name"></span>**NOME \_ DA FILA DO CAMPO \_ \_ DE LOG \_ HTTP**
</dt> <dd> <dl> <dt>



O nome da fila de solicitações para a qual a solicitação é expedida. Esse campo de log só é usado para registro em log de erros.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_STREAMID"></span><span id="http_log_field_streamid"></span>**STREAMID \_ DO CAMPO DE LOG \_ \_ HTTP**
</dt> <dd> <dl> <dt>



A ID do fluxo.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                    |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                              |
| Cabeçalho<br/>                   | <dl> <dt>Http.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes da API do Servidor HTTP versão 2.0](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**INFORMAÇÕES DE \_ LOG \_ HTTP**](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





