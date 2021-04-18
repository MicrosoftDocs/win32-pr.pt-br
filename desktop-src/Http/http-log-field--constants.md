---
title: Constantes de HTTP_LOG_FIELD_ (http. h)
description: Defina os campos no log W3C e nos logs de erros.
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
ms.openlocfilehash: b9ab05a9126cb5ffb81b65a460e6a9d671c268bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753300"
---
# <a name="http_log_field_-constants"></a>\_Constantes de \_ campo de log http \_

As constantes de **\_ \_ campo \_ de log http** definem os campos no log W3C e os logs de erros.

Essas constantes são usadas na estrutura [**de \_ \_ informações de log http**](/windows/desktop/api/Http/ns-http-http_logging_info) .

<dl> <dt>

<span id="HTTP_LOG_FIELD_DATE"></span><span id="http_log_field_date"></span>**\_data do \_ campo de log http \_**
</dt> <dd> <dl> <dt>



A data em que a atividade ocorreu.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_TIME"></span><span id="http_log_field_time"></span>**\_tempo do \_ campo de log http \_**
</dt> <dd> <dl> <dt>



A hora, em UTC (tempo Universal Coordenado), na qual a atividade ocorreu.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_CLIENT_IP"></span><span id="http_log_field_client_ip"></span>**\_IP do \_ cliente do campo de log http \_ \_**
</dt> <dd> <dl> <dt>



Endereço IP do cliente que fez a solicitação.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_USER_NAME"></span><span id="http_log_field_user_name"></span>**\_nome de \_ usuário do campo de log http \_ \_**
</dt> <dd> <dl> <dt>



O nome do usuário autenticado que acessou seu servidor. Os usuários anônimos são indicados por um hífen.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SITE_NAME"></span><span id="http_log_field_site_name"></span>**\_nome do \_ site do campo de log http \_ \_**
</dt> <dd> <dl> <dt>



O nome do site no qual a entrada do arquivo de log foi gerada.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_COMPUTER_NAME"></span><span id="_http_log_field_computer_name"></span>**Http \_ \_nome do \_ computador \_ do campo de log**
</dt> <dd> <dl> <dt>



O nome do computador no qual a entrada do arquivo de log foi gerada.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SERVER_IP"></span><span id="http_log_field_server_ip"></span>**\_ \_ \_ IP do servidor de campo de log http \_**
</dt> <dd> <dl> <dt>



O endereço IP do servidor no qual a entrada do arquivo de log foi gerada.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_METHOD"></span><span id="http_log_field_method"></span>**\_método de \_ campo de log http \_**
</dt> <dd> <dl> <dt>



A ação solicitada, por exemplo, um método Get.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_URI_STEM"></span><span id="_http_log_field_uri_stem"></span>**Http \_ \_ \_ \_ tronco URI do campo de log**
</dt> <dd> <dl> <dt>



O destino da ação, por exemplo, Default.htm.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_URI_QUERY"></span><span id="http_log_field_uri_query"></span>**\_consulta de \_ URI de campo de log http \_ \_**
</dt> <dd> <dl> <dt>



A consulta, se houver, que o cliente estava tentando executar. Um URI (Resource Identifier Universal) consulta é necessário apenas para páginas dinâmico.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_STATUS"></span><span id="http_log_field_status"></span>**\_status do \_ campo de log http \_**
</dt> <dd> <dl> <dt>



O código de status HTTP.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_WIN32_STATUS"></span><span id="http_log_field_win32_status"></span>**\_Status do \_ Win32 do campo de log http \_ \_**
</dt> <dd> <dl> <dt>



O código de status do Windows.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_BYTES_SENT"></span><span id="http_log_field_bytes_sent"></span>**\_bytes de campo de log http \_ \_ \_ enviados**
</dt> <dd> <dl> <dt>



O número, em bytes, enviado pelo servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_BYTES_RECV"></span><span id="http_log_field_bytes_recv"></span>**\_bytes de campo de log http \_ \_ \_ recv**
</dt> <dd> <dl> <dt>



O número, em bytes, recebido pelo servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_TIME_TAKEN"></span><span id="http_log_field_time_taken"></span>**\_tempo de campo de log http \_ \_ \_ retirado**
</dt> <dd> <dl> <dt>



O tempo, em milissegundos, da ação.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SERVER_PORT"></span><span id="http_log_field_server_port"></span>**\_ \_ \_ porta do servidor de campo de log http \_**
</dt> <dd> <dl> <dt>



O número da porta do servidor que está configurado para o serviço.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_USER_AGENT"></span><span id="_http_log_field_user_agent"></span>**Http \_ \_agente do \_ usuário \_ do campo de log**
</dt> <dd> <dl> <dt>



O aplicativo usado pelo cliente.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_COOKIE"></span><span id="http_log_field_cookie"></span>**\_cookie de \_ campo de log http \_**
</dt> <dd> <dl> <dt>



O conteúdo do cookie enviado ou recebido, se houver.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_REFERER"></span><span id="http_log_field_referer"></span>**\_ \_ referenciador de campo de log http \_**
</dt> <dd> <dl> <dt>



O site que o usuário visitou pela última vez. Esse site fornece um link para o site atual.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_VERSION"></span><span id="http_log_field_version"></span>**\_versão do \_ campo de log http \_**
</dt> <dd> <dl> <dt>



A versão do protocolo HTTP que o cliente usou.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_HOST"></span><span id="http_log_field_host"></span>**\_host de \_ campo de log http \_**
</dt> <dd> <dl> <dt>



O nome do cabeçalho de host, se houver.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SUB_STATUS"></span><span id="http_log_field_sub_status"></span>**substatus de \_ campo de log http \_ \_ \_**
</dt> <dd> <dl> <dt>



O código de erro de substatus.


</dt> </dl> </dd> </dl>

As constantes a seguir são usadas para o log de erros HTTP.

<dl> <dt>

<span id="HTTP_LOG_FIELD_CLIENT_PORT"></span><span id="http_log_field_client_port"></span>**\_porta do \_ cliente do campo de log http \_ \_**
</dt> <dd> <dl> <dt>



O número da porta do cliente a partir da qual a solicitação é recebida. Este campo de log só é usado para log de erros.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_URI"></span><span id="http_log_field_uri"></span>**\_URI do \_ campo de log http \_**
</dt> <dd> <dl> <dt>



O URI recebido na solicitação, incluindo a parte de consulta. Este campo de log só é usado para log de erros.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SITE_ID"></span><span id="http_log_field_site_id"></span>**\_ID do \_ site do campo de log http \_ \_**
</dt> <dd> <dl> <dt>



A ID numérica específica do aplicativo do grupo de URLs na qual a solicitação é roteada. Este campo de log só é usado para log de erros.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_REASON"></span><span id="http_log_field_reason"></span>**\_motivo do \_ campo de log http \_**
</dt> <dd> <dl> <dt>



A frase do motivo do erro. Este campo de log só é usado para log de erros.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_QUEUE_NAME"></span><span id="http_log_field_queue_name"></span>**\_nome da \_ fila do campo de log http \_ \_**
</dt> <dd> <dl> <dt>



O nome da fila de solicitações para a qual a solicitação é expedida. Este campo de log só é usado para log de erros.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_STREAMID"></span><span id="http_log_field_streamid"></span>**\_campo de log http \_ \_ streamid**
</dt> <dd> <dl> <dt>



A ID do fluxo.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>Http. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes da API do servidor HTTP versão 2,0](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**\_informações de log http \_**](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





