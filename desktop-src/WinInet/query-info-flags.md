---
title: Sinalizadores de informações de consulta (Wininet.h)
description: As listas a seguir contêm os atributos e modificadores usados por HttpQueryInfo e QueryInfo.
ms.assetid: b1613193-ae03-411e-bf05-de42f471cd8c
topic_type:
- apiref
api_name:
- HTTP_QUERY_ACCEPT
- HTTP_QUERY_ACCEPT_CHARSET
- HTTP_QUERY_ACCEPT_ENCODING
- HTTP_QUERY_ACCEPT_LANGUAGE
- HTTP_QUERY_ACCEPT_RANGES
- HTTP_QUERY_AGE
- HTTP_QUERY_ALLOW
- HTTP_QUERY_AUTHORIZATION
- HTTP_QUERY_CACHE_CONTROL
- HTTP_QUERY_CONNECTION
- HTTP_QUERY_CONTENT_BASE
- HTTP_QUERY_CONTENT_DESCRIPTION
- HTTP_QUERY_CONTENT_DISPOSITION
- HTTP_QUERY_CONTENT_ENCODING
- HTTP_QUERY_CONTENT_ID
- HTTP_QUERY_CONTENT_LANGUAGE
- HTTP_QUERY_CONTENT_LENGTH
- HTTP_QUERY_CONTENT_LOCATION
- HTTP_QUERY_CONTENT_MD5
- HTTP_QUERY_CONTENT_RANGE
- HTTP_QUERY_CONTENT_TRANSFER_ENCODING
- HTTP_QUERY_CONTENT_TYPE
- HTTP_QUERY_COOKIE
- HTTP_QUERY_COST
- HTTP_QUERY_CUSTOM
- HTTP_QUERY_DATE
- HTTP_QUERY_DERIVED_FROM
- HTTP_QUERY_ECHO_HEADERS
- HTTP_QUERY_ECHO_HEADERS_CRLF
- HTTP_QUERY_ECHO_REPLY
- HTTP_QUERY_ECHO_REQUEST
- HTTP_QUERY_ETAG
- HTTP_QUERY_EXPECT
- HTTP_QUERY_EXPIRES
- HTTP_QUERY_FORWARDED
- HTTP_QUERY_FROM
- HTTP_QUERY_HOST
- HTTP_QUERY_IF_MATCH
- HTTP_QUERY_IF_MODIFIED_SINCE
- HTTP_QUERY_IF_NONE_MATCH
- HTTP_QUERY_IF_RANGE
- HTTP_QUERY_IF_UNMODIFIED_SINCE
- HTTP_QUERY_LAST_MODIFIED
- HTTP_QUERY_LINK
- HTTP_QUERY_LOCATION
- HTTP_QUERY_MAX
- HTTP_QUERY_MAX_FORWARDS
- HTTP_QUERY_MESSAGE_ID
- HTTP_QUERY_MIME_VERSION
- HTTP_QUERY_ORIG_URI
- HTTP_QUERY_PRAGMA
- HTTP_QUERY_PROXY_AUTHENTICATE
- HTTP_QUERY_PROXY_AUTHORIZATION
- HTTP_QUERY_PROXY_CONNECTION
- HTTP_QUERY_PUBLIC
- HTTP_QUERY_RANGE
- HTTP_QUERY_RAW_HEADERS
- HTTP_QUERY_RAW_HEADERS_CRLF
- HTTP_QUERY_REFERER
- HTTP_QUERY_REFRESH
- HTTP_QUERY_REQUEST_METHOD
- HTTP_QUERY_RETRY_AFTER
- HTTP_QUERY_SERVER
- HTTP_QUERY_SET_COOKIE
- HTTP_QUERY_STATUS_CODE
- HTTP_QUERY_STATUS_TEXT
- HTTP_QUERY_TITLE
- HTTP_QUERY_TRANSFER_ENCODING
- HTTP_QUERY_UNLESS_MODIFIED_SINCE
- HTTP_QUERY_UPGRADE
- HTTP_QUERY_URI
- HTTP_QUERY_USER_AGENT
- HTTP_QUERY_VARY
- HTTP_QUERY_VERSION
- HTTP_QUERY_VIA
- HTTP_QUERY_WARNING
- HTTP_QUERY_WWW_AUTHENTICATE
- HTTP_QUERY_X_CONTENT_TYPE_OPTIONS
- HTTP_QUERY_P3P
- HTTP_QUERY_X_P2P_PEERDIST
- HTTP_QUERY_TRANSLATE
- HTTP_QUERY_X_UA_COMPATIBLE
- HTTP_QUERY_DEFAULT_STYLE
- HTTP_QUERY_X_FRAME_OPTIONS
- HTTP_QUERY_X_XSS_PROTECTION
- HTTP_QUERY_FLAG_COALESCE
- HTTP_QUERY_FLAG_NUMBER
- HTTP_QUERY_FLAG_REQUEST_HEADERS
- HTTP_QUERY_FLAG_SYSTEMTIME
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fb2e52a30aa10161963f215e9045db006a82fee482a67947017d20372cefbdb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955546"
---
# <a name="query-info-flags-winineth"></a>Sinalizadores de informações de consulta (Wininet.h)

As listas a seguir contêm os atributos e modificadores usados [**por HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) e [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85)).

Os sinalizadores de atributo são usados [**por HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (ou [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) para indicar quais dados recuperar. A maioria dos sinalizadores de atributo é mapeada diretamente para um cabeçalho HTTP específico. Também há alguns sinalizadores especiais, como CABEÇALHOS BRUTOS DE CONSULTA HTTP, que não estão relacionados a um cabeçalho específico. [ \_ \_ \_ ](/windows)

<dl> <dt>

<span id="HTTP_QUERY_ACCEPT"></span><span id="http_query_accept"></span>**HTTP \_ QUERY \_ ACCEPT**
</dt> <dd> <dl> <dt>

24
</dt> <dt>



Recupera os tipos de mídia aceitáveis para a resposta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_CHARSET"></span><span id="http_query_accept_charset"></span>**CHARSET \_ DE ACEITAÇÃO DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

25
</dt> <dt>



Recupera os conjuntos de caracteres aceitáveis para a resposta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_ENCODING"></span><span id="http_query_accept_encoding"></span>**\_CODIFICAÇÃO \_ HTTP QUERY ACCEPT \_**
</dt> <dd> <dl> <dt>

26
</dt> <dt>



Recupera os valores aceitáveis de codificação de conteúdo para a resposta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="http_query_accept_language"></span>**LINGUAGEM \_ HTTP QUERY \_ \_ ACCEPT**
</dt> <dd> <dl> <dt>

27
</dt> <dt>



Recupera os idiomas naturais aceitáveis para a resposta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_RANGES"></span><span id="http_query_accept_ranges"></span>**INTERVALOS \_ DE \_ ACEITAÇÃO DE \_ CONSULTA HTTP**
</dt> <dd> <dl> <dt>

42
</dt> <dt>



Recupera os tipos de solicitações de intervalo que são aceitas para um recurso.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_AGE"></span><span id="http_query_age"></span>**IDADE \_ DA CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

48
</dt> <dt>



Recupera o campo idade response-header, que contém a estimativa do remetente da quantidade de tempo desde que a resposta foi gerada no servidor de origem.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ALLOW"></span><span id="http_query_allow"></span>**PERMITIR \_ CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

7
</dt> <dt>



Recebe os verbos HTTP com suporte pelo servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_AUTHORIZATION"></span><span id="http_query_authorization"></span>**AUTORIZAÇÃO \_ DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

28
</dt> <dt>



Recupera as credenciais de autorização usadas para uma solicitação.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CACHE_CONTROL"></span><span id="http_query_cache_control"></span>**CONTROLE \_ DE CACHE DE \_ CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

49
</dt> <dt>



Recupera as diretivas de controle de cache.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONNECTION"></span><span id="http_query_connection"></span>**CONEXÃO \_ DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

23
</dt> <dt>



Recupera todas as opções especificadas para uma conexão específica e não devem ser comunicadas por proxies em conexões posteriores.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_BASE"></span><span id="http_query_content_base"></span>**BASE \_ DE CONTEÚDO DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

50
</dt> <dt>



Recupera o URI base (Uniform Resource Identifier) para resolver URLs relativas dentro da entidade.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="http_query_content_description"></span>**DESCRIÇÃO \_ DO CONTEÚDO \_ DA CONSULTA HTTP \_**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Obsoleto. Mantido apenas para compatibilidade de aplicativo herdado.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_DISPOSITION"></span><span id="http_query_content_disposition"></span>**DISPOSIÇÃO \_ DO CONTEÚDO DA \_ CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

47
</dt> <dt>



Obsoleto. Mantido apenas para compatibilidade de aplicativo herdado.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_ENCODING"></span><span id="http_query_content_encoding"></span>**CODIFICAÇÃO \_ DE \_ CONTEÚDO \_ DE CONSULTA HTTP**
</dt> <dd> <dl> <dt>

29
</dt> <dt>



Recupera as codificações de conteúdo adicionais que foram aplicadas a todo o recurso.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_ID"></span><span id="http_query_content_id"></span>**\_ID DE CONTEÚDO \_ DA \_ CONSULTA HTTP**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Recupera a identificação do conteúdo.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LANGUAGE"></span><span id="http_query_content_language"></span>**LINGUAGEM \_ DE CONTEÚDO DE \_ CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

6
</dt> <dt>



Recupera o idioma em que o conteúdo está.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LENGTH"></span><span id="http_query_content_length"></span>**TAMANHO \_ DO CONTEÚDO DA \_ CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Recupera o tamanho do recurso, em bytes.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LOCATION"></span><span id="http_query_content_location"></span>**LOCAL \_ DO CONTEÚDO DA \_ CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

51
</dt> <dt>



Recupera o local do recurso para a entidade delimitada na mensagem.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_MD5"></span><span id="http_query_content_md5"></span>**HTTP \_ QUERY \_ CONTENT \_ MD5**
</dt> <dd> <dl> <dt>

52
</dt> <dt>



Recupera um resumo MD5 do corpo da entidade com a finalidade de fornecer uma MIC (verificação de integridade de mensagem de ponta a ponta) para o corpo da entidade. Para obter mais informações, consulte RFC1864, o campo de título Content-MD5, em [https://ftp.isi.edu/in-notes/rfc1864.txt](https://tools.ietf.org/html/rfc1864) .


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_RANGE"></span><span id="http_query_content_range"></span>**INTERVALO \_ DE CONTEÚDO DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

53
</dt> <dt>



Recupera o local no corpo da entidade completo em que o corpo parcial da entidade deve ser inserido e o tamanho total do corpo da entidade completo.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="http_query_content_transfer_encoding"></span>**CODIFICAÇÃO \_ DE TRANSFERÊNCIA DE CONTEÚDO \_ \_ \_ DE CONSULTA HTTP**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Recebe a codificação de conteúdo adicional que foi aplicada ao recurso.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_TYPE"></span><span id="http_query_content_type"></span>**TIPO \_ DE CONTEÚDO DE \_ CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Recebe o tipo de conteúdo do recurso (como text/html).


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_COOKIE"></span><span id="http_query_cookie"></span>**COOKIE \_ DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

44
</dt> <dt>



Recupera todos os cookies associados à solicitação.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_COST"></span><span id="http_query_cost"></span>**CUSTO \_ DA CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

15
</dt> <dt>



Não tem mais suporte.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CUSTOM"></span><span id="http_query_custom"></span>**HTTP \_ QUERY \_ CUSTOM**
</dt> <dd> <dl> <dt>

65535
</dt> <dt>



Faz [**com que HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) pesquise o nome do cabeçalho especificado em *lpvBuffer* e armazene os dados de cabeçalho em *lpvBuffer*.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DATE"></span><span id="http_query_date"></span>**DATA \_ DA CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

9
</dt> <dt>



Recebe a data e a hora em que a mensagem foi originada.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DERIVED_FROM"></span><span id="http_query_derived_from"></span>**CONSULTA HTTP \_ \_ DERIVADA \_ DE**
</dt> <dd> <dl> <dt>

14
</dt> <dt>



Não tem mais suporte.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_HEADERS"></span><span id="http_query_echo_headers"></span>**CABEÇALHOS \_ DE \_ ECO DE \_ CONSULTA HTTP**
</dt> <dd> <dl> <dt>

73
</dt> <dt>



Não implementado atualmente.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_HEADERS_CRLF"></span><span id="http_query_echo_headers_crlf"></span>**CABEÇALHOS DE ECO DE CONSULTA HTTP \_ \_ \_ \_ CRLF**
</dt> <dd> <dl> <dt>

74
</dt> <dt>



Não implementado atualmente.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_REPLY"></span><span id="http_query_echo_reply"></span>**RESPOSTA \_ DE ECO DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

72
</dt> <dt>



Não implementado atualmente.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_REQUEST"></span><span id="http_query_echo_request"></span>**SOLICITAÇÃO \_ DE ECO DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

71
</dt> <dt>



Não implementado atualmente.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ETAG"></span><span id="http_query_etag"></span>**ETAG \_ DE \_ CONSULTA HTTP**
</dt> <dd> <dl> <dt>

54
</dt> <dt>



Recupera a marca de entidade para a entidade associada.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_EXPECT"></span><span id="http_query_expect"></span>**HTTP \_ QUERY \_ EXPECT**
</dt> <dd> <dl> <dt>

68
</dt> <dt>



Recupera o header Expect, que indica se o aplicativo cliente deve esperar respostas da série 100.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_EXPIRES"></span><span id="http_query_expires"></span>**A CONSULTA HTTP \_ \_ EXPIRA**
</dt> <dd> <dl> <dt>

10
</dt> <dt>



Recebe a data e a hora após as quais o recurso deve ser considerado desatualizado.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FORWARDED"></span><span id="http_query_forwarded"></span>**CONSULTA HTTP \_ \_ ENCAMINHADA**
</dt> <dd> <dl> <dt>

30
</dt> <dt>



Obsoleto. Mantido apenas para compatibilidade de aplicativo herdado.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FROM"></span><span id="http_query_from"></span>**CONSULTA HTTP \_ \_ DE**
</dt> <dd> <dl> <dt>

31
</dt> <dt>



Recupera o endereço de email para o usuário humano que controla o agente de usuário solicitante se o header From for determinado.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_HOST"></span><span id="http_query_host"></span>**HOST \_ DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

55
</dt> <dt>



Recupera o host da Internet e o número da porta do recurso que está sendo solicitado.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_MATCH"></span><span id="http_query_if_match"></span>**CONSULTA HTTP \_ \_ SE \_ CORRESPONDER**
</dt> <dd> <dl> <dt>

56
</dt> <dt>



Recupera o conteúdo do campo If-Match de solicitação.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="http_query_if_modified_since"></span>**CONSULTA \_ HTTP, \_ SE MODIFICADA \_ DESDE \_ ENTÃO**
</dt> <dd> <dl> <dt>

32
</dt> <dt>



Recupera o conteúdo do header If-Modified-Since.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_NONE_MATCH"></span><span id="http_query_if_none_match"></span>**CONSULTA HTTP \_ SE \_ NENHUM \_ \_ CORRESPONDER**
</dt> <dd> <dl> <dt>

57
</dt> <dt>



Recupera o conteúdo do campo de header de solicitação If-None-Match.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_RANGE"></span><span id="http_query_if_range"></span>**CONSULTA HTTP \_ SE \_ \_ INTERVALO**
</dt> <dd> <dl> <dt>

58
</dt> <dt>



Recupera o conteúdo do campo If-Range de solicitação. Esse header permite que o aplicativo cliente verifique se a entidade relacionada a uma cópia parcial da entidade no cache do aplicativo cliente não foi atualizada. Se a entidade não tiver sido atualizada, envie as partes que o aplicativo cliente está ausente. Se a entidade tiver sido atualizada, envie toda a entidade atualizada.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="http_query_if_unmodified_since"></span>**CONSULTA \_ HTTP SE NÃO FOR \_ \_ MODIFICADA \_ DESDE**
</dt> <dd> <dl> <dt>

59
</dt> <dt>



Recupera o conteúdo do campo de header de solicitação If-Unmodified-Since.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LAST_MODIFIED"></span><span id="http_query_last_modified"></span>**CONSULTA HTTP \_ \_ ÚLTIMA \_ MODIFICAÇÃO**
</dt> <dd> <dl> <dt>

11
</dt> <dt>



Recebe a data e a hora em que o servidor acredita que o recurso foi modificado pela última vez.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LINK"></span><span id="http_query_link"></span>**\_LINK DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

16
</dt> <dt>



Obsoleto. Mantido apenas para compatibilidade de aplicativo herdado.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LOCATION"></span><span id="http_query_location"></span>**LOCAL \_ DA CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

33
</dt> <dt>



Recupera o URI (Uniform Resource Identifier absoluto) usado em um header de resposta Local.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MAX"></span><span id="http_query_max"></span>**HTTP \_ QUERY \_ MAX**
</dt> <dd> <dl> <dt>

78
</dt> <dt>



Não é um sinalizador de consulta. Indica o valor máximo de um valor \_ DE CONSULTA \_ \* HTTP.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MAX_FORWARDS"></span><span id="http_query_max_forwards"></span>**\_ENCAMINHAMENTOS \_ \_ MÁXIMOS DE CONSULTA HTTP**
</dt> <dd> <dl> <dt>

60
</dt> <dt>



Recupera o número de proxies ou gateways que podem encaminhar a solicitação para o próximo servidor de entrada.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MESSAGE_ID"></span><span id="http_query_message_id"></span>**\_ID DA \_ MENSAGEM DE \_ CONSULTA HTTP**
</dt> <dd> <dl> <dt>

12
</dt> <dt>



Não tem mais suporte.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MIME_VERSION"></span><span id="http_query_mime_version"></span>**VERSÃO \_ \_ MIME DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Recebe a versão do protocolo MIME que foi usado para construir a mensagem.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ORIG_URI"></span><span id="http_query_orig_uri"></span>**\_ \_ URI ORIG DE CONSULTA HTTP \_**
</dt> <dd> <dl> <dt>

34
</dt> <dt>



Obsoleto. Mantido apenas para compatibilidade de aplicativo herdado.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PRAGMA"></span><span id="http_query_pragma"></span>**\_PRAGMA DE CONSULTA HTTP \_**
</dt> <dd> <dl> <dt>

17
</dt> <dt>



Recebe as diretivas específicas da implementação que podem ser aplicadas a qualquer destinatário ao longo da cadeia de solicitação/resposta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="http_query_proxy_authenticate"></span>**AUTENTICAÇÃO \_ DE PROXY DE \_ \_ CONSULTA HTTP**
</dt> <dd> <dl> <dt>

41
</dt> <dt>



Recupera o esquema de autenticação e o realm retornados pelo proxy.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="http_query_proxy_authorization"></span>**AUTORIZAÇÃO \_ DE PROXY DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

61
</dt> <dt>



Recupera o header usado para identificar o usuário para um proxy que requer autenticação. Esse header só pode ser recuperado antes que a solicitação seja enviada ao servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_CONNECTION"></span><span id="http_query_proxy_connection"></span>**CONEXÃO \_ DE PROXY DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

69
</dt> <dt>



Recupera o Proxy-Connection de dados.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PUBLIC"></span><span id="http_query_public"></span>**HTTP \_ QUERY \_ PUBLIC**
</dt> <dd> <dl> <dt>

8
</dt> <dt>



Recebe métodos disponíveis neste servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RANGE"></span><span id="http_query_range"></span>**INTERVALO \_ DE CONSULTAS \_ HTTP**
</dt> <dd> <dl> <dt>

62
</dt> <dt>



Recupera o intervalo de byte de uma entidade.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RAW_HEADERS"></span><span id="http_query_raw_headers"></span>**CABEÇALHOS \_ BRUTOS \_ DE CONSULTA HTTP \_**
</dt> <dd> <dl> <dt>

21
</dt> <dt>



Recebe todos os headers retornados pelo servidor. Cada header é encerrado por \\ "0". Um \\ "0" adicional encerra a lista de headers.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="http_query_raw_headers_crlf"></span>**\_CRLF \_ DE CABEÇALHOS \_ BRUTOS DE \_ CONSULTA HTTP**
</dt> <dd> <dl> <dt>

22
</dt> <dt>



Recebe todos os headers retornados pelo servidor. Cada header é separado por uma sequência cr/lf (retorno de carro/alimentação de linha).


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REFERER"></span><span id="http_query_referer"></span>**REFERÊNCIA \_ DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

35
</dt> <dt>



Recebe o Uniform Resource Identifier (URI) do recurso em que o URI solicitado foi obtido.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REFRESH"></span><span id="http_query_refresh"></span>**ATUALIZAÇÃO \_ DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

46
</dt> <dt>



Obsoleto. Mantido apenas para compatibilidade de aplicativo herdado.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REQUEST_METHOD"></span><span id="http_query_request_method"></span>**MÉTODO \_ DE SOLICITAÇÃO \_ DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

45
</dt> <dt>



Recebe o verbo HTTP que está sendo usado na solicitação, normalmente GET ou POST.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RETRY_AFTER"></span><span id="http_query_retry_after"></span>**HTTP \_ QUERY \_ RETRY \_ AFTER**
</dt> <dd> <dl> <dt>

36
</dt> <dt>



Recupera a quantidade de tempo que o serviço deve ficar indisponível.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_SERVER"></span><span id="http_query_server"></span>**SERVIDOR \_ DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

37
</dt> <dt>



Recupera dados sobre o software usado pelo servidor de origem para lidar com a solicitação.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_SET_COOKIE"></span><span id="http_query_set_cookie"></span>**HTTP \_ QUERY \_ SET \_ COOKIE**
</dt> <dd> <dl> <dt>

43
</dt> <dt>



Recebe o valor do conjunto de cookies para a solicitação.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_STATUS_CODE"></span><span id="http_query_status_code"></span>**CÓDIGO DE \_ STATUS DA CONSULTA HTTP \_ \_**
</dt> <dd> <dl> <dt>

19
</dt> <dt>



Recebe o código de status retornado pelo servidor. Para obter mais informações e uma lista de valores possíveis, consulte [**Códigos de status HTTP**](http-status-codes.md).


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_STATUS_TEXT"></span><span id="http_query_status_text"></span>**TEXTO DE STATUS DA CONSULTA HTTP \_ \_ \_**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



Recebe qualquer texto adicional retornado pelo servidor na linha de resposta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TITLE"></span><span id="http_query_title"></span>**TÍTULO \_ DA CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

38
</dt> <dt>



Obsoleto. Mantido apenas para compatibilidade de aplicativo herdado.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TRANSFER_ENCODING"></span><span id="http_query_transfer_encoding"></span>**CODIFICAÇÃO \_ DE \_ TRANSFERÊNCIA DE CONSULTA HTTP \_**
</dt> <dd> <dl> <dt>

63
</dt> <dt>



Recupera o tipo de transformação que foi aplicado ao corpo da mensagem para que ela possa ser transferida com segurança entre o remetente e o destinatário.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="http_query_unless_modified_since"></span>**CONSULTA \_ HTTP, A \_ MENOS QUE TENHA SIDO MODIFICADA \_ \_ DESDE**
</dt> <dd> <dl> <dt>

70
</dt> <dt>



Recupera o header Unless-Modified-Since.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_UPGRADE"></span><span id="http_query_upgrade"></span>**ATUALIZAÇÃO \_ DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

64
</dt> <dt>



Recupera os protocolos de comunicação adicionais com suporte pelo servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_URI"></span><span id="http_query_uri"></span>**\_URI DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

13
</dt> <dt>



Recebe alguns ou todos os URIs (Uniform Resource Identifiers) pelos quais o recurso Request-URI pode ser identificado.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_USER_AGENT"></span><span id="http_query_user_agent"></span>**AGENTE \_ DO USUÁRIO DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

39
</dt> <dt>



Recupera dados sobre o agente do usuário que fez a solicitação.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VARY"></span><span id="http_query_vary"></span>**A CONSULTA HTTP \_ \_ VARIA**
</dt> <dd> <dl> <dt>

65
</dt> <dt>



Recupera o header que indica que a entidade foi selecionada de várias representações disponíveis da resposta usando a negociação controlada pelo servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VERSION"></span><span id="http_query_version"></span>**VERSÃO \_ DA CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

18
</dt> <dt>



Recebe o último código de resposta retornado pelo servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VIA"></span><span id="http_query_via"></span>**CONSULTA HTTP \_ \_ VIA**
</dt> <dd> <dl> <dt>

66
</dt> <dt>



Recupera os protocolos intermediários e destinatários entre o agente do usuário e o servidor em solicitações e entre o servidor de origem e o cliente nas respostas.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_WARNING"></span><span id="http_query_warning"></span>**AVISO \_ DE CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

67
</dt> <dt>



Recupera dados adicionais sobre o status de uma resposta que podem não ser refletidos pelo código de status da resposta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_WWW_AUTHENTICATE"></span><span id="http_query_www_authenticate"></span>**HTTP \_ QUERY \_ WWW \_ AUTHENTICATE**
</dt> <dd> <dl> <dt>

40
</dt> <dt>



Recupera o esquema de autenticação e o realm retornados pelo servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_CONTENT_TYPE_OPTIONS"></span><span id="http_query_x_content_type_options"></span>**OPÇÕES \_ DE TIPO DE CONTEÚDO HTTP \_ \_ \_ QUERY X \_**
</dt> <dd> <dl> <dt>

79
</dt> <dt>



Recupera o valor do título X-Content-Type-Options.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_P3P"></span><span id="http_query_p3p"></span>**CONSULTA HTTP \_ \_ P3P**
</dt> <dd> <dl> <dt>

80
</dt> <dt>



Recupera o valor do header P3P.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_P2P_PEERDIST"></span><span id="http_query_x_p2p_peerdist"></span>**HTTP \_ QUERY \_ X \_ P2P \_ PEERDIST**
</dt> <dd> <dl> <dt>

81
</dt> <dt>



Recupera o valor do header X-P2P-PeerDist.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TRANSLATE"></span><span id="http_query_translate"></span>**HTTP \_ QUERY \_ TRANSLATE**
</dt> <dd> <dl> <dt>

82
</dt> <dt>



Recupera o valor do header de tradução.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_UA_COMPATIBLE"></span><span id="http_query_x_ua_compatible"></span>**HTTP \_ QUERY \_ X \_ UA \_ COMPATIBLE**
</dt> <dd> <dl> <dt>

83
</dt> <dt>



Recupera o valor de header compatível com X-UA.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DEFAULT_STYLE"></span><span id="http_query_default_style"></span>**ESTILO \_ PADRÃO DA CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

84
</dt> <dt>



Recupera o valor Default-Style do usuário.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_FRAME_OPTIONS"></span><span id="http_query_x_frame_options"></span>**OPÇÕES \_ DE QUADRO X \_ DA CONSULTA HTTP \_ \_**
</dt> <dd> <dl> <dt>

85
</dt> <dt>



Recupera o valor do header X-Frame-Options.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_XSS_PROTECTION"></span><span id="http_query_x_xss_protection"></span>**CONSULTA HTTP \_ \_ X PROTEÇÃO \_ XSS \_**
</dt> <dd> <dl> <dt>

86
</dt> <dt>



Recupera o valor do header X-XSS-Protection.


</dt> </dl> </dd> </dl>

Os sinalizadores modificador são usados em conjunto com um sinalizador de atributo para modificar a solicitação. Os sinalizadores modificador modificam o formato dos dados retornados ou indicam onde [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (ou [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) deve pesquisar os dados.

<dl> <dt>

<span id="HTTP_QUERY_FLAG_COALESCE"></span><span id="http_query_flag_coalesce"></span>**\_ \_ \_ COALESCE DO SINALIZADOR DE CONSULTA HTTP**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



Não implementado.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_NUMBER"></span><span id="http_query_flag_number"></span>**NÚMERO \_ DO SINALIZADOR DE CONSULTA \_ \_ HTTP**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Retorna os dados como um número de 32 bits para os headers cujo valor é um número, como o código de status.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="http_query_flag_request_headers"></span>**CABEÇALHOS \_ DE SOLICITAÇÃO \_ DO SINALIZADOR DE \_ CONSULTA \_ HTTP**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



Somente os headers de solicitação de consultas.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="http_query_flag_systemtime"></span>**SYSTEMTIME \_ DO SINALIZADOR DE \_ \_ CONSULTA HTTP**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Retorna o valor do header como uma [**estrutura SYSTEMTIME,**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que não exige que o aplicativo analisar os dados. Use para os headers cujo valor é uma cadeia de caracteres de data/hora, como "Hora da Última Modificação".


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

> [!Note]  
> O WinINet não dá suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o WinHTTP (Microsoft Windows HTTP Services).](/windows/desktop/WinHttp/winhttp-start-page)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Wininet.h</dt> </dl> |



 

