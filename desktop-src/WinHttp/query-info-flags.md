---
description: Esses atributos e modificadores são usados por WinHttpQueryHeaders.
ms.assetid: c26dac1d-9a75-440a-a0ef-a2029f138f3b
title: Sinalizadores de Informações de Consulta (Winhttp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c66fd75ad1258123c3047dee4cafa4e57cb4dadd6675eb02deaa307085acbd55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051954"
---
# <a name="query-info-flags-winhttph"></a>Sinalizadores de Informações de Consulta (Winhttp.h)

Esses atributos e modificadores são usados [**por WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders).

Os sinalizadores de atributo são usados [**por WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) para indicar quais informações recuperar. A maioria dos sinalizadores de atributo é mapeada diretamente para um cabeçalho HTTP específico. Também há alguns sinalizadores especiais, como OS HEADERS BRUTOS DE CONSULTA \_ WINHTTP, que não estão relacionados \_ \_ a um título específico.

<dl> <dt>

<span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**WINHTTP \_ QUERY \_ ACCEPT**
</dt> <dd> <dl> <dt>



Recupera os tipos de mídia aceitáveis para a resposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**WINHTTP \_ QUERY \_ ACCEPT \_ CHARSET**
</dt> <dd> <dl> <dt>



Recupera os conjuntos de caracteres aceitáveis para a resposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**CODIFICAÇÃO WINHTTP \_ QUERY \_ ACCEPT \_**
</dt> <dd> <dl> <dt>



Recupera os valores aceitáveis de codificação de conteúdo para a resposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**WINHTTP \_ QUERY \_ ACCEPT \_ LANGUAGE**
</dt> <dd> <dl> <dt>



Recupera os idiomas naturais aceitáveis para a resposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**INTERVALOS DE ACEITAÇÃO DE CONSULTA WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera os tipos de solicitações de intervalo que são aceitas para um recurso.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**IDADE DA CONSULTA WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera o campo idade response-header, que contém a estimativa do remetente da quantidade de tempo desde que a resposta foi gerada no servidor de origem.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**WINHTTP \_ QUERY \_ ALLOW**
</dt> <dd> <dl> <dt>



Recebe os [**verbos HTTP com**](glossary.md) suporte pelo servidor.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**INFORMAÇÕES DE \_ AUTENTICAÇÃO DE CONSULTA WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera o Authentication-Info de dados.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**AUTORIZAÇÃO DE CONSULTA WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera as credenciais de autorização usadas para uma solicitação.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**CONTROLE DE CACHE DE CONSULTA WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera as diretivas de controle de cache.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**CONEXÃO DE CONSULTA \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera todas as opções especificadas para uma conexão específica e não devem ser comunicadas por proxies em conexões posteriores.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**BASE DE CONTEÚDO DE CONSULTA WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera o URI (Uniform Resource Identifier base) para resolver URLs relativas dentro da entidade.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**DESCRIÇÃO DO CONTEÚDO DA CONSULTA WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Obsoleto. Mantido para compatibilidade de aplicativo herdado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**DISPOSIÇÃO DO CONTEÚDO DA CONSULTA WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Obsoleto. Mantido para compatibilidade de aplicativo herdado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**CODIFICAÇÃO DE CONTEÚDO \_ \_ DE CONSULTA WINHTTP \_**
</dt> <dd> <dl> <dt>



Recupera a codificação de conteúdo adicional que foi aplicada a todo o recurso.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**ID DE CONTEÚDO DA CONSULTA WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera a identificação do conteúdo.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**LINGUAGEM DE CONTEÚDO DE CONSULTA WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera o idioma em que o conteúdo é gravado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**COMPRIMENTO DO CONTEÚDO DA CONSULTA WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera o tamanho do recurso, em bytes.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**LOCAL DO CONTEÚDO DA CONSULTA WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera o local do recurso para a entidade delimitada na mensagem.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**WINHTTP \_ QUERY \_ CONTENT \_ MD5**
</dt> <dd> <dl> <dt>



Recupera um resumo MD5 do corpo da entidade com a finalidade de fornecer uma verificação de integridade da mensagem de ponta a ponta para o corpo da entidade. Para obter mais informações, [consulte RFC 1864](https://www.ietf.org/rfc/rfc1864.txt).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**INTERVALO DE CONTEÚDO DE CONSULTA WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera o local no corpo completo da entidade em que o corpo parcial da entidade deve ser inserido e o tamanho total do corpo da entidade completo.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**CODIFICAÇÃO DE TRANSFERÊNCIA DE \_ \_ CONTEÚDO DE \_ CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera uma transformação de codificação aplicável a um corpo da entidade. Ele pode já ter sido aplicado, pode precisar ser aplicado ou pode ser opcionalmente aplicável.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**TIPO DE CONTEÚDO DE CONSULTA WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recebe o tipo de conteúdo do recurso, como texto ou html.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**COOKIE DE CONSULTA WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera todos os cookies associados à solicitação.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**CUSTO DA CONSULTA WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Sem suporte.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**WINHTTP \_ QUERY \_ CUSTOM**
</dt> <dd> <dl> <dt>



Faz [**com que WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) pesquise o nome do título especificado no parâmetro *pwszName* e armazene as informações de título *em lpBuffer*. Um aplicativo pode usar **WINHTTP \_ OPTION RECEIVE RESPONSE \_ \_ \_ TIMEOUT** para limitar o tempo máximo que essa consulta aguarda para que todos os títulos sejam recebidos.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**WINHTTP \_ QUERY \_ DATE**
</dt> <dd> <dl> <dt>



Recebe a data e a hora em que a mensagem foi originada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**CONSULTA WINHTTP \_ \_ DERIVADA \_ DE**
</dt> <dd> <dl> <dt>



Sem suporte.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**WINHTTP \_ QUERY \_ ETAG**
</dt> <dd> <dl> <dt>



Recupera a marca de entidade para a entidade associada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**WINHTTP \_ QUERY \_ EXPECT**
</dt> <dd> <dl> <dt>



Recupera o header Expect, que indica se o aplicativo cliente deve esperar respostas da série 100.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**A CONSULTA WINHTTP \_ \_ EXPIRA**
</dt> <dd> <dl> <dt>



Recebe a data e a hora após as quais o recurso deve ser considerado desatualizado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**CONSULTA WINHTTP \_ \_ ENCAMINHADA**
</dt> <dd> <dl> <dt>



Obsoleto. Mantido para compatibilidade de aplicativo herdado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**CONSULTA WINHTTP \_ \_ DE**
</dt> <dd> <dl> <dt>



Recupera o endereço de email para o usuário que controla o agente de [*usuário solicitante*](glossary.md) se o header From for dado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**HOST DE CONSULTA WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera o host da Internet e o número da porta do recurso que está sendo solicitado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**WINHTTP \_ QUERY \_ IF \_ MATCH**
</dt> <dd> <dl> <dt>



Recupera o conteúdo do campo If-Match de solicitação.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**CONSULTA WINHTTP \_ SE \_ MODIFICADA DESDE \_ \_ ENTÃO**
</dt> <dd> <dl> <dt>



Recupera o conteúdo do header If-Modified-Since.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**CONSULTA WINHTTP \_ \_ SE NENHUM \_ \_ CORRESPONDER**
</dt> <dd> <dl> <dt>



Recupera o conteúdo do campo de header de solicitação If-None-Match.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**CONSULTA WINHTTP \_ SE \_ \_ INTERVALO**
</dt> <dd> <dl> <dt>



Recupera o conteúdo do campo If-Range de solicitação. Esse header permite que o aplicativo cliente verifique se a entidade relacionada a uma cópia parcial da entidade no cache do aplicativo cliente não foi atualizada. Se a entidade não tiver sido atualizada, envie as partes que o aplicativo cliente está ausente. Se a entidade tiver sido atualizada, envie toda a entidade atualizada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**CONSULTA WINHTTP \_ \_ SE NÃO FOR \_ MODIFICADA DESDE \_ ENTÃO**
</dt> <dd> <dl> <dt>



Recupera o conteúdo do campo de header de solicitação If-Unmodified-Since.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**LINK DE CONSULTA \_ WINHTTP \_**
</dt> <dd> <dl> <dt>



Obsoleto. Mantido para compatibilidade de aplicativo herdado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**CONSULTA WINHTTP \_ ÚLTIMA \_ \_ MODIFICAÇÃO**
</dt> <dd> <dl> <dt>



Recebe a data e a hora em que o recurso foi modificado pela última vez. A data e a hora são determinadas pelo servidor.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**LOCAL DA CONSULTA WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera o URI absoluto usado em um header de resposta local.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**WINHTTP \_ QUERY \_ MAX**
</dt> <dd> <dl> <dt>



Indica o valor máximo de um valor WINHTTP \_ \_ \* QUERY. Não é um sinalizador de consulta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**ENCAMINHAMENTOS \_ MÁXIMOS DE CONSULTA \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera o número de proxies ou gateways que podem encaminhar a solicitação para o próximo servidor de entrada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**ID DA MENSAGEM \_ \_ DE CONSULTA WINHTTP \_**
</dt> <dd> <dl> <dt>



Sem suporte.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**WINHTTP \_ QUERY \_ MIME \_ VERSION**
</dt> <dd> <dl> <dt>



Recebe a versão do protocolo MIME (Multipurpose Internet Mail Extensions) que foi usado para construir a mensagem.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**WINHTTP \_ QUERY \_ ORIG \_ URI**
</dt> <dd> <dl> <dt>



Obsoleto. Mantido para compatibilidade de aplicativo herdado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**PRAGMA DE \_ CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recebe as diretivas específicas da implementação que podem ser aplicadas a qualquer destinatário ao longo da cadeia de solicitação/resposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**AUTENTICAÇÃO DO PROXY DE CONSULTA WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera o esquema de autenticação e o realm retornados pelo proxy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**AUTORIZAÇÃO DE PROXY DE CONSULTA WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera o header usado para identificar o usuário para um proxy que requer autenticação. Esse header só pode ser recuperado antes que a solicitação seja enviada ao servidor.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**CONEXÃO DE PROXY DE CONSULTA WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera o Proxy-Connection de dados.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**SUPORTE A PROXY DE CONSULTA WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera o Proxy-Support de dados.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**WINHTTP \_ QUERY \_ PUBLIC**
</dt> <dd> <dl> <dt>



Recebe verbos HTTP disponíveis neste servidor.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**INTERVALO DE CONSULTAS \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera o intervalo de byte de uma entidade.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**HEADERS \_ BRUTOS DE \_ CONSULTA WINHTTP \_**
</dt> <dd> <dl> <dt>



Recebe todos os headers retornados pelo servidor. Cada header é encerrado por \\ "0". Um \\ "0" adicional encerra a lista de headers.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**\_CRLF DE \_ TÍTULOS BRUTOS DE CONSULTA \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recebe todos os headers retornados pelo servidor. Cada header é separado por uma sequência cr/lf (retorno de carro/alimentação de linha).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**REFERÊNCIA DE CONSULTA WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recebe o URI do recurso em que o URI solicitado foi obtido.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**ATUALIZAÇÃO DE CONSULTA \_ WINHTTP \_**
</dt> <dd> <dl> <dt>



Obsoleto. Mantido para compatibilidade de aplicativo herdado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**MÉTODO DE \_ SOLICITAÇÃO DE CONSULTA WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recebe o verbo HTTP que está sendo usado na solicitação, normalmente GET ou POST.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**TENTATIVA DE CONSULTA WINHTTP \_ \_ \_ APÓS**
</dt> <dd> <dl> <dt>



Recupera a quantidade de tempo que o serviço deve ficar indisponível.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**SERVIDOR DE CONSULTA \_ WINHTTP \_**
</dt> <dd> <dl> <dt>



Recupera informações sobre o software usado pelo servidor de origem para manipular a solicitação.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**COOKIE DO CONJUNTO DE CONSULTAS WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recebe o valor do conjunto de cookies para a solicitação.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**CÓDIGO DE STATUS DA CONSULTA WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recebe o código de status retornado pelo servidor. Para ver uma lista de valores possíveis, consulte [**Códigos de status HTTP.**](http-status-codes.md)


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**TEXTO DE STATUS DA CONSULTA WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recebe texto adicional retornado pelo servidor na linha de resposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**TÍTULO DA CONSULTA WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Obsoleto. Mantido para compatibilidade de aplicativo herdado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**CODIFICAÇÃO DE TRANSFERÊNCIA \_ \_ DE CONSULTA WINHTTP \_**
</dt> <dd> <dl> <dt>



Recupera o tipo de transformação que foi aplicado ao corpo da mensagem para que ela possa ser transferida com segurança entre o remetente e o destinatário.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**CONSULTA WINHTTP, \_ A MENOS QUE MODIFICADA \_ \_ \_ DESDE**
</dt> <dd> <dl> <dt>



Recupera o header Unless-Modified-Since.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**ATUALIZAÇÃO DE CONSULTA \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera os protocolos de comunicação adicionais com suporte pelo servidor.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**URI DE CONSULTA WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recebe algum ou todo o URI pelo qual o recurso Request-URI pode ser identificado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**AGENTE DO USUÁRIO DE CONSULTA WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera informações sobre o agente do usuário que fez a solicitação.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**A CONSULTA WINHTTP \_ \_ VARIA**
</dt> <dd> <dl> <dt>



Recupera o header que indica que a entidade foi selecionada de várias representações disponíveis da resposta usando a negociação controlada pelo servidor.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**VERSÃO DA \_ CONSULTA WINHTTP \_**
</dt> <dd> <dl> <dt>



Recupera a versão HTTP que está presente na linha de status.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**CONSULTA WINHTTP \_ \_ VIA**
</dt> <dd> <dl> <dt>



Recupera os protocolos intermediários e destinatários entre o agente do usuário e o servidor em solicitações e entre o servidor de origem e o cliente nas respostas.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**AVISO DE CONSULTA \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera informações adicionais sobre o status de uma resposta que pode não ser refletida pelo código de status da resposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**WINHTTP \_ QUERY \_ WWW \_ AUTHENTICATE**
</dt> <dd> <dl> <dt>



Recupera o esquema de autenticação e o realm retornados pelo servidor.


</dt> </dl> </dd> </dl>

Os sinalizadores modificador são usados em conjunto com um sinalizador de atributo para modificar a solicitação. Os sinalizadores modificadores modificam o formato dos dados retornados ou indicam onde a [**função WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) deve pesquisar as informações.

<dl> <dt>

<span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**NÚMERO DO SINALIZADOR DE CONSULTA WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Retorna os dados como um número de 32 bits para os headers cujo valor é um número, como o código de status.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**HEADERS DE \_ SOLICITAÇÃO DO SINALIZADOR \_ DE CONSULTA \_ WINHTTP \_**
</dt> <dd> <dl> <dt>



Somente os headers de solicitação de consultas.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**SYSTEMTIME DO \_ SINALIZADOR \_ DE CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>



Retorna o valor do header como uma [**estrutura SYSTEMTIME,**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) que não exige que o aplicativo analisar os dados. Use para os headers cujo valor é uma cadeia de caracteres de data/hora, como "Hora da Última Modificação".


</dt> </dl> </dd> </dl>

<span id="WINHTTP_QUERY_FLAG_TRAILERS"></span><span id="winhttp_query_flag_trailers"></span>**TRAILERS DO \_ SINALIZADOR \_ DE CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>


Consultas responderam a trailers. Antes de consultar os trailers de resposta, você deve chamar [**WinHttpReadData**](/windows/win32/api/Winhttp/nf-winhttp-winhttpreaddata) até que ele retorne 0 bytes lidos.


</dt> </dl> </dd> </dl>

<span id="WINHTTP_QUERY_FLAG_WIRE_ENCODING"></span><span id="winhttp_query_flag_wire_encoding"></span>**CODIFICAÇÃO DE TRANSMISSÃO DO SINALIZADOR \_ \_ DE \_ CONSULTA \_ WINHTTP**
</dt> <dd> <dl> <dt>


Por padrão, [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) executa uma conversão Unicode antes de retornar o título consultado. Se esse sinalizador for definido, WinHttp retornará o título para o chamador sem executar essa conversão.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows XP, Windows 2000 Professional somente com aplicativos da área de trabalho SP3 \[\]      |
| Servidor mínimo com suporte | Windows Server 2003, Windows 2000 Server somente com aplicativos da área de trabalho SP3 \[\]   |
| Cabeçalho                   | <dl> <dt>WinHTTP. h</dt> </dl> |

## <a name="see-also"></a>Confira também

* [Versões do WinHTTP](winhttp-versions.md)
