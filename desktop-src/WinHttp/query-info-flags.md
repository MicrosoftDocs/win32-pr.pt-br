---
description: Esses atributos e modificadores são usados pelo WinHttpQueryHeaders.
ms.assetid: c26dac1d-9a75-440a-a0ef-a2029f138f3b
title: Sinalizadores de informações de consulta (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9ffc8f4ba4a947fe6fb277617c99460c43ffb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011239"
---
# <a name="query-info-flags-winhttph"></a>Sinalizadores de informações de consulta (WinHTTP. h)

Esses atributos e modificadores são usados pelo [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).

Os sinalizadores de atributo são usados pelo [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) para indicar quais informações recuperar. A maioria dos sinalizadores de atributo mapeia diretamente para um cabeçalho HTTP específico. Também há alguns sinalizadores especiais, como \_ \_ cabeçalhos brutos de consulta WinHTTP \_ , que não estão relacionados a um cabeçalho específico.

<dl> <dt>

<span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**\_aceitação de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera os tipos de mídia aceitáveis para a resposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**conjunto \_ de \_ caracteres de aceitação de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera os conjuntos de caracteres aceitáveis para a resposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**\_codificação de \_ aceitação de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera os valores de codificação de conteúdo aceitáveis para a resposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**\_linguagem de \_ aceitação de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera os idiomas naturais aceitáveis para a resposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**\_intervalos de \_ aceitação de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera os tipos de solicitações de intervalo que são aceitas para um recurso.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**\_idade de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera o campo de cabeçalho resposta etária, que contém a estimativa do remetente do período desde que a resposta foi gerada no servidor de origem.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**\_permissão de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recebe o [*verbo http*](glossary.md)s com suporte do servidor.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**\_informações de \_ autenticação de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera o cabeçalho Authentication-Info.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**\_autorização de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera as credenciais de autorização usadas para uma solicitação.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**\_controle de \_ cache de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera as diretivas de controle de cache.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**\_conexão de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera as opções especificadas para uma conexão específica e não deve ser comunicada por proxies em outras conexões.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**\_base de \_ conteúdo de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera o Uniform Resource Identifier de base (URI) para resolver URLs relativas na entidade.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**\_Descrição do \_ conteúdo da consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Obsoleto. Mantido para compatibilidade de aplicativos herdados.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**\_disposição de \_ conteúdo de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Obsoleto. Mantido para compatibilidade de aplicativos herdados.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**\_codificação de \_ conteúdo de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera a codificação de conteúdo adicional que foi aplicada a todo o recurso.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**\_ID de \_ conteúdo de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera a identificação do conteúdo.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**\_linguagem de \_ conteúdo de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera o idioma no qual o conteúdo é gravado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**\_comprimento do \_ conteúdo da consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera o tamanho do recurso, em bytes.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**\_local do \_ conteúdo da consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera o local do recurso para a entidade incluída na mensagem.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**\_MD5 de \_ conteúdo de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera um resumo MD5 do corpo da entidade com a finalidade de fornecer uma verificação de integridade de mensagem de ponta a ponta para o corpo da entidade. Para obter mais informações, consulte [RFC 1864](https://www.ietf.org/rfc/rfc1864.txt).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**\_intervalo de \_ conteúdo de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera o local no corpo da entidade completa em que o corpo da entidade parcial deve ser inserido e o tamanho total do corpo da entidade completa.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**\_codificação de \_ transferência de conteúdo de consulta WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera uma transformação de codificação aplicável a um corpo de entidade. Talvez ele já tenha sido aplicado, talvez precise ser aplicado ou pode ser opcionalmente aplicável.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**\_tipo de \_ conteúdo de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recebe o tipo de conteúdo do recurso, como texto ou HTML.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**\_cookie de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera todos os cookies associados à solicitação.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**\_custo da consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Não há suporte.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**consulta de WINHTTP \_ \_ personalizada**
</dt> <dd> <dl> <dt>



Faz com que o [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) procure o nome do cabeçalho especificado no parâmetro *pwszName* e armazene as informações do cabeçalho em *lpBuffer*. Um aplicativo pode usar **o \_ \_ \_ \_ tempo limite de resposta de recebimento da opção WinHTTP** para limitar o tempo máximo que essa consulta aguarda para que todos os cabeçalhos sejam recebidos.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**\_data da consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recebe a data e a hora em que a mensagem foi originada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**\_consulta WinHTTP \_ derivada \_ de**
</dt> <dd> <dl> <dt>



Não há suporte.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**\_ETag de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera a marca de entidade para a entidade associada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**\_espera de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera o cabeçalho esperado, que indica se o aplicativo cliente deve esperar respostas da série 100.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**a \_ consulta WinHTTP \_ expira**
</dt> <dd> <dl> <dt>



Recebe a data e a hora após as quais o recurso deve ser considerado desatualizado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**\_consulta WinHTTP \_ encaminhada**
</dt> <dd> <dl> <dt>



Obsoleto. Mantido para compatibilidade de aplicativos herdados.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**\_consulta \_ de WinHTTP de**
</dt> <dd> <dl> <dt>



Recupera o endereço de email do usuário que controla o [*agente do usuário*](glossary.md) solicitante se o cabeçalho de for fornecido.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**\_host de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera o host da Internet e o número da porta do recurso que está sendo solicitado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**\_consulta WinHTTP \_ se \_ corresponder**
</dt> <dd> <dl> <dt>



Recupera o conteúdo do campo If-Match cabeçalho de solicitação.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**\_consulta WinHTTP \_ se \_ modificada \_ desde**
</dt> <dd> <dl> <dt>



Recupera o conteúdo do cabeçalho If-Modified-Since.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**\_consulta WinHTTP \_ se \_ nenhuma \_ correspondência**
</dt> <dd> <dl> <dt>



Recupera o conteúdo do campo de cabeçalho de solicitação If-None-Match.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**consulta de WINHTTP \_ \_ se \_ intervalo**
</dt> <dd> <dl> <dt>



Recupera o conteúdo do campo If-Range cabeçalho de solicitação. Esse cabeçalho permite que o aplicativo cliente Verifique se a entidade relacionada a uma cópia parcial da entidade no cache do aplicativo cliente não foi atualizada. Se a entidade não tiver sido atualizada, envie as partes que o aplicativo cliente está faltando. Se a entidade tiver sido atualizada, envie toda a entidade atualizada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**\_consulta WinHTTP \_ se não for \_ modificado \_ desde**
</dt> <dd> <dl> <dt>



Recupera o conteúdo do campo de cabeçalho de solicitação se-não modificado-desde.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**\_link de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Obsoleto. Mantido para compatibilidade de aplicativos herdados.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**\_consulta WinHTTP \_ modificada pela última vez \_**
</dt> <dd> <dl> <dt>



Recebe a data e a hora da última modificação do recurso. A data e a hora são determinadas pelo servidor.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**\_local da consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera o URI absoluto usado em um cabeçalho de resposta de local.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**consulta de WINHTTP \_ \_ Max**
</dt> <dd> <dl> <dt>



Indica o valor máximo de um \_ valor de consulta WinHTTP \_ \* . Não é um sinalizador de consulta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**\_ \_ encaminhamentos máximos de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera o número de proxies ou gateways que podem encaminhar a solicitação para o próximo servidor de entrada.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**\_ID da \_ mensagem de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Não há suporte.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**\_versão de \_ MIME da consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recebe a versão do protocolo MIME (Multipurpose Internet Mail Extensions) usado para construir a mensagem.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**\_URI de \_ orig de consulta de WinHTTP \_**
</dt> <dd> <dl> <dt>



Obsoleto. Mantido para compatibilidade de aplicativos herdados.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**\_pragma da consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recebe as diretivas específicas de implementação que podem se aplicar a qualquer destinatário ao longo da cadeia de solicitação/resposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**\_autenticação de \_ proxy de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera o esquema de autenticação e o realm retornado pelo proxy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**\_autorização de \_ proxy de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera o cabeçalho que é usado para identificar o usuário para um proxy que requer autenticação. Esse cabeçalho só pode ser recuperado antes que a solicitação seja enviada ao servidor.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**\_conexão de \_ proxy de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera o cabeçalho Proxy-Connection.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**\_ \_ suporte ao proxy de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera o cabeçalho Proxy-Support.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**consulta de WINHTTP \_ \_ pública**
</dt> <dd> <dl> <dt>



Recebe verbos HTTP disponíveis neste servidor.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**\_intervalo de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera o intervalo de bytes de uma entidade.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**\_ \_ cabeçalhos brutos de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recebe todos os cabeçalhos retornados pelo servidor. Cada cabeçalho é encerrado por " \\ 0". Um " \\ 0" adicional encerra a lista de cabeçalhos.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**\_CRLF de \_ cabeçalhos brutos de consulta \_ WinHTTP \_**
</dt> <dd> <dl> <dt>



Recebe todos os cabeçalhos retornados pelo servidor. Cada cabeçalho é separado por uma sequência de CR/LF (retorno de carro/alimentação de linha).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**\_referenciador de consulta de WinHTTP \_**
</dt> <dd> <dl> <dt>



Recebe o URI do recurso em que o URI solicitado foi obtido.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**\_atualização de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Obsoleto. Mantido para compatibilidade de aplicativos herdados.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**\_método de \_ solicitação de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recebe o verbo HTTP que está sendo usado na solicitação, normalmente GET ou POST.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**\_repetir consulta de WinHTTP \_ \_ após**
</dt> <dd> <dl> <dt>



Recupera a quantidade de tempo que o serviço deve estar indisponível.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**\_servidor de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera informações sobre o software usado pelo servidor de origem para lidar com a solicitação.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**\_cookie do \_ conjunto de consultas do WinHTTP \_**
</dt> <dd> <dl> <dt>



Recebe o valor do conjunto de cookies para a solicitação.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**\_código de \_ status de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recebe o código de status retornado pelo servidor. Para obter uma lista de valores possíveis, consulte [**códigos de status http**](http-status-codes.md).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**\_texto de \_ status da consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recebe texto adicional retornado pelo servidor na linha de resposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**\_título da consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Obsoleto. Mantido para compatibilidade de aplicativos herdados.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**\_codificação de \_ transferência de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera o tipo de transformação que foi aplicado ao corpo da mensagem para que possa ser transferido com segurança entre o remetente e o destinatário.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**\_consulta WinHTTP \_ , a menos que seja \_ modificado \_ desde**
</dt> <dd> <dl> <dt>



Recupera o cabeçalho, a menos que-Modified-Since.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**\_atualização de consulta de WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera os protocolos de comunicação adicionais que são suportados pelo servidor.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**\_URI de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recebe parte ou todo o URI pelo qual o recurso de solicitação-URI pode ser identificado.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**\_agente do \_ usuário de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera informações sobre o agente do usuário que fez a solicitação.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**a \_ consulta WinHTTP \_ varia**
</dt> <dd> <dl> <dt>



Recupera o cabeçalho que indica que a entidade foi selecionada a partir de várias representações disponíveis da resposta usando a negociação controlada pelo servidor.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**\_versão de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera a versão HTTP que está presente na linha de status.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**\_consulta WinHTTP \_ via**
</dt> <dd> <dl> <dt>



Recupera os protocolos intermediários e os destinatários entre o agente do usuário e o servidor em solicitações e entre o servidor de origem e o cliente em respostas.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**\_aviso de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera informações adicionais sobre o status de uma resposta que pode não ser refletida pelo código de status de resposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**\_consulta WinHTTP \_ www \_ Authenticate**
</dt> <dd> <dl> <dt>



Recupera o esquema de autenticação e o realm retornado pelo servidor.


</dt> </dl> </dd> </dl>

Os sinalizadores modificadores são usados em conjunto com um sinalizador de atributo para modificar a solicitação. Os sinalizadores de modificador modificam o formato dos dados retornados ou indicam onde a função [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) deve pesquisar as informações.

<dl> <dt>

<span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**\_número do \_ sinalizador de consulta WinHTTP \_**
</dt> <dd> <dl> <dt>



Retorna os dados como um número de 32 bits para cabeçalhos cujo valor é um número, como o código de status.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**\_cabeçalhos de \_ solicitação de sinalizador de consulta WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Consulta somente cabeçalhos de solicitação.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**sinalizador de consulta de WINHTTP \_ \_ \_ SYSTEMTIME**
</dt> <dd> <dl> <dt>



Retorna o valor do cabeçalho como uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , que não exige que o aplicativo analise os dados. Use para cabeçalhos cujo valor é uma cadeia de caracteres de data/hora, como "hora da última modificação".


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]<br/>      |
| Servidor mínimo com suporte<br/> | Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]<br/>   |
| parâmetro<br/>                   | <dl> <dt>WinHTTP. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Versões do WinHTTP](winhttp-versions.md)
</dt> </dl>

 

