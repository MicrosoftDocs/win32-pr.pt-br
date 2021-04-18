---
title: Sinalizadores de informações de consulta (Wininet. h)
description: As listas a seguir contêm os atributos e os modificadores usados por HttpQueryInfo e QueryInfo.
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
ms.openlocfilehash: 5f3a6166c59e158d041e730d2198f6e1b066a8b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760996"
---
# <a name="query-info-flags-winineth"></a>Sinalizadores de informações de consulta (Wininet. h)

As listas a seguir contêm os atributos e os modificadores usados por [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) e [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85)).

Os sinalizadores de atributo são usados por [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (ou [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) para indicar quais dados recuperar. A maioria dos sinalizadores de atributo mapeia diretamente para um cabeçalho HTTP específico. Também há alguns sinalizadores especiais, como [ \_ \_ \_ cabeçalhos brutos de consulta http](/windows), que não estão relacionados a um cabeçalho específico.

<dl> <dt>

<span id="HTTP_QUERY_ACCEPT"></span><span id="http_query_accept"></span>**\_aceitação de consulta http \_**
</dt> <dd> <dl> <dt>

24
</dt> <dt>



Recupera os tipos de mídia aceitáveis para a resposta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_CHARSET"></span><span id="http_query_accept_charset"></span>**conjunto \_ de \_ caracteres de aceitação de consulta http \_**
</dt> <dd> <dl> <dt>

25
</dt> <dt>



Recupera os conjuntos de caracteres aceitáveis para a resposta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_ENCODING"></span><span id="http_query_accept_encoding"></span>**\_codificação de \_ aceitação de consulta http \_**
</dt> <dd> <dl> <dt>

26
</dt> <dt>



Recupera os valores de codificação de conteúdo aceitáveis para a resposta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="http_query_accept_language"></span>**\_linguagem de \_ aceitação de consulta http \_**
</dt> <dd> <dl> <dt>

27
</dt> <dt>



Recupera os idiomas naturais aceitáveis para a resposta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_RANGES"></span><span id="http_query_accept_ranges"></span>**\_intervalos de \_ aceitação de consulta http \_**
</dt> <dd> <dl> <dt>

42
</dt> <dt>



Recupera os tipos de solicitações de intervalo que são aceitas para um recurso.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_AGE"></span><span id="http_query_age"></span>**\_duração da consulta http \_**
</dt> <dd> <dl> <dt>

48
</dt> <dt>



Recupera o campo de cabeçalho resposta etária, que contém a estimativa do remetente do período desde que a resposta foi gerada no servidor de origem.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ALLOW"></span><span id="http_query_allow"></span>**\_permissão de consulta http \_**
</dt> <dd> <dl> <dt>

7
</dt> <dt>



Recebe os verbos HTTP com suporte do servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_AUTHORIZATION"></span><span id="http_query_authorization"></span>**\_autorização de consulta http \_**
</dt> <dd> <dl> <dt>

28
</dt> <dt>



Recupera as credenciais de autorização usadas para uma solicitação.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CACHE_CONTROL"></span><span id="http_query_cache_control"></span>**\_controle de \_ cache de consulta http \_**
</dt> <dd> <dl> <dt>

49
</dt> <dt>



Recupera as diretivas de controle de cache.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONNECTION"></span><span id="http_query_connection"></span>**\_conexão de consulta http \_**
</dt> <dd> <dl> <dt>

23
</dt> <dt>



Recupera as opções especificadas para uma conexão específica e não deve ser comunicada por proxies em outras conexões.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_BASE"></span><span id="http_query_content_base"></span>**\_base de \_ conteúdo de consulta http \_**
</dt> <dd> <dl> <dt>

50
</dt> <dt>



Recupera o URI de base (Uniform Resource Identifier) para resolver URLs relativas na entidade.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="http_query_content_description"></span>**\_Descrição do \_ conteúdo da consulta http \_**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Obsoleto. Mantido somente para compatibilidade de aplicativos herdados.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_DISPOSITION"></span><span id="http_query_content_disposition"></span>**\_disposição de \_ conteúdo de consulta http \_**
</dt> <dd> <dl> <dt>

47
</dt> <dt>



Obsoleto. Mantido somente para compatibilidade de aplicativos herdados.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_ENCODING"></span><span id="http_query_content_encoding"></span>**\_codificação de \_ conteúdo de consulta http \_**
</dt> <dd> <dl> <dt>

29
</dt> <dt>



Recupera as codificações de conteúdo adicionais que foram aplicadas a todo o recurso.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_ID"></span><span id="http_query_content_id"></span>**\_ID do \_ conteúdo da consulta http \_**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Recupera a identificação do conteúdo.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LANGUAGE"></span><span id="http_query_content_language"></span>**\_linguagem de \_ conteúdo de consulta http \_**
</dt> <dd> <dl> <dt>

6
</dt> <dt>



Recupera o idioma no qual o conteúdo está.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LENGTH"></span><span id="http_query_content_length"></span>**\_comprimento do \_ conteúdo da consulta http \_**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Recupera o tamanho do recurso, em bytes.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LOCATION"></span><span id="http_query_content_location"></span>**\_local do \_ conteúdo da consulta http \_**
</dt> <dd> <dl> <dt>

51
</dt> <dt>



Recupera o local do recurso para a entidade incluída na mensagem.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_MD5"></span><span id="http_query_content_md5"></span>**\_MD5 de \_ conteúdo de consulta http \_**
</dt> <dd> <dl> <dt>

52
</dt> <dt>



Recupera um resumo MD5 do corpo da entidade com a finalidade de fornecer um MIC (verificação de integridade de mensagem) de ponta a ponta para o corpo da entidade. Para obter mais informações, consulte RFC1864, o campo cabeçalho Content-MD5, em [https://ftp.isi.edu/in-notes/rfc1864.txt](https://tools.ietf.org/html/rfc1864) .


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_RANGE"></span><span id="http_query_content_range"></span>**\_intervalo de \_ conteúdo de consulta http \_**
</dt> <dd> <dl> <dt>

53
</dt> <dt>



Recupera o local no corpo da entidade completa em que o corpo da entidade parcial deve ser inserido e o tamanho total do corpo da entidade completa.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="http_query_content_transfer_encoding"></span>**\_codificação de \_ transferência de conteúdo de consulta http \_ \_**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Recebe a codificação de conteúdo adicional que foi aplicada ao recurso.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_TYPE"></span><span id="http_query_content_type"></span>**\_tipo de \_ conteúdo de consulta http \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Recebe o tipo de conteúdo do recurso (como texto/HTML).


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_COOKIE"></span><span id="http_query_cookie"></span>**\_cookie de consulta http \_**
</dt> <dd> <dl> <dt>

44
</dt> <dt>



Recupera todos os cookies associados à solicitação.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_COST"></span><span id="http_query_cost"></span>**\_custo da consulta http \_**
</dt> <dd> <dl> <dt>

15
</dt> <dt>



Não tem mais suporte.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CUSTOM"></span><span id="http_query_custom"></span>**\_personalizado de consulta http \_**
</dt> <dd> <dl> <dt>

65535
</dt> <dt>



Faz com que o [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) procure o nome do cabeçalho especificado em *lpvBuffer* e armazene os dados do cabeçalho em *lpvBuffer*.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DATE"></span><span id="http_query_date"></span>**\_data da consulta http \_**
</dt> <dd> <dl> <dt>

9
</dt> <dt>



Recebe a data e a hora em que a mensagem foi originada.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DERIVED_FROM"></span><span id="http_query_derived_from"></span>**\_consulta http \_ derivada \_ de**
</dt> <dd> <dl> <dt>

14
</dt> <dt>



Não tem mais suporte.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_HEADERS"></span><span id="http_query_echo_headers"></span>**\_cabeçalhos de \_ eco de consulta http \_**
</dt> <dd> <dl> <dt>

73
</dt> <dt>



Não implementado atualmente.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_HEADERS_CRLF"></span><span id="http_query_echo_headers_crlf"></span>**\_cabeçalhos de eco de consulta http \_ \_ \_ CRLF**
</dt> <dd> <dl> <dt>

74
</dt> <dt>



Não implementado atualmente.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_REPLY"></span><span id="http_query_echo_reply"></span>**\_resposta de \_ eco de consulta http \_**
</dt> <dd> <dl> <dt>

72
</dt> <dt>



Não implementado atualmente.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_REQUEST"></span><span id="http_query_echo_request"></span>**\_solicitação de \_ eco de consulta http \_**
</dt> <dd> <dl> <dt>

71
</dt> <dt>



Não implementado atualmente.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ETAG"></span><span id="http_query_etag"></span>**\_ETag de consulta http \_**
</dt> <dd> <dl> <dt>

54
</dt> <dt>



Recupera a marca de entidade para a entidade associada.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_EXPECT"></span><span id="http_query_expect"></span>**\_espera de consulta http \_**
</dt> <dd> <dl> <dt>

68
</dt> <dt>



Recupera o cabeçalho esperado, que indica se o aplicativo cliente deve esperar respostas da série 100.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_EXPIRES"></span><span id="http_query_expires"></span>**a \_ consulta http \_ expira**
</dt> <dd> <dl> <dt>

10
</dt> <dt>



Recebe a data e a hora após as quais o recurso deve ser considerado desatualizado.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FORWARDED"></span><span id="http_query_forwarded"></span>**\_consulta http \_ encaminhada**
</dt> <dd> <dl> <dt>

30
</dt> <dt>



Obsoleto. Mantido somente para compatibilidade de aplicativos herdados.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FROM"></span><span id="http_query_from"></span>**\_consulta http \_ de**
</dt> <dd> <dl> <dt>

31
</dt> <dt>



Recupera o endereço de email do usuário humano que controla o agente do usuário solicitante se o cabeçalho de for fornecido.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_HOST"></span><span id="http_query_host"></span>**\_host de consulta http \_**
</dt> <dd> <dl> <dt>

55
</dt> <dt>



Recupera o host da Internet e o número da porta do recurso que está sendo solicitado.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_MATCH"></span><span id="http_query_if_match"></span>**\_consulta http \_ se \_ corresponder**
</dt> <dd> <dl> <dt>

56
</dt> <dt>



Recupera o conteúdo do campo If-Match cabeçalho de solicitação.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="http_query_if_modified_since"></span>**\_consulta http \_ se \_ modificada \_ desde**
</dt> <dd> <dl> <dt>

32
</dt> <dt>



Recupera o conteúdo do cabeçalho If-Modified-Since.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_NONE_MATCH"></span><span id="http_query_if_none_match"></span>**\_consulta http \_ se \_ nenhuma \_ correspondência**
</dt> <dd> <dl> <dt>

57
</dt> <dt>



Recupera o conteúdo do campo de cabeçalho de solicitação If-None-Match.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_RANGE"></span><span id="http_query_if_range"></span>**\_consulta http \_ se o \_ intervalo**
</dt> <dd> <dl> <dt>

58
</dt> <dt>



Recupera o conteúdo do campo If-Range cabeçalho de solicitação. Esse cabeçalho permite que o aplicativo cliente Verifique se a entidade relacionada a uma cópia parcial da entidade no cache de aplicativo do cliente não foi atualizada. Se a entidade não tiver sido atualizada, envie as partes que o aplicativo cliente está faltando. Se a entidade tiver sido atualizada, envie toda a entidade atualizada.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="http_query_if_unmodified_since"></span>**\_consulta http \_ se não for \_ modificado \_ desde**
</dt> <dd> <dl> <dt>

59
</dt> <dt>



Recupera o conteúdo do campo de cabeçalho de solicitação se-não modificado-desde.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LAST_MODIFIED"></span><span id="http_query_last_modified"></span>**\_consulta http \_ modificada pela última vez \_**
</dt> <dd> <dl> <dt>

11
</dt> <dt>



Recebe a data e a hora em que o servidor acredita que o recurso foi modificado pela última vez.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LINK"></span><span id="http_query_link"></span>**\_link de consulta http \_**
</dt> <dd> <dl> <dt>

16
</dt> <dt>



Obsoleto. Mantido somente para compatibilidade de aplicativos herdados.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LOCATION"></span><span id="http_query_location"></span>**\_local da consulta http \_**
</dt> <dd> <dl> <dt>

33
</dt> <dt>



Recupera o Uniform Resource Identifier absoluto (URI) usado em um cabeçalho de resposta de local.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MAX"></span><span id="http_query_max"></span>**\_máximo de consultas http \_**
</dt> <dd> <dl> <dt>

78
</dt> <dt>



Não é um sinalizador de consulta. Indica o valor máximo de um \_ valor de consulta http \_ \* .


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MAX_FORWARDS"></span><span id="http_query_max_forwards"></span>**\_ \_ encaminhamentos máximos de consultas http \_**
</dt> <dd> <dl> <dt>

60
</dt> <dt>



Recupera o número de proxies ou gateways que podem encaminhar a solicitação para o próximo servidor de entrada.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MESSAGE_ID"></span><span id="http_query_message_id"></span>**\_ID da \_ mensagem de consulta http \_**
</dt> <dd> <dl> <dt>

12
</dt> <dt>



Não tem mais suporte.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MIME_VERSION"></span><span id="http_query_mime_version"></span>**\_versão de \_ MIME de consulta http \_**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Recebe a versão do protocolo MIME que foi usado para construir a mensagem.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ORIG_URI"></span><span id="http_query_orig_uri"></span>**\_URI de \_ orig de consulta http \_**
</dt> <dd> <dl> <dt>

34
</dt> <dt>



Obsoleto. Mantido somente para compatibilidade de aplicativos herdados.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PRAGMA"></span><span id="http_query_pragma"></span>**\_pragma da consulta http \_**
</dt> <dd> <dl> <dt>

17
</dt> <dt>



Recebe as diretivas específicas de implementação que podem se aplicar a qualquer destinatário ao longo da cadeia de solicitação/resposta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="http_query_proxy_authenticate"></span>**\_autenticação de \_ proxy de consulta http \_**
</dt> <dd> <dl> <dt>

41
</dt> <dt>



Recupera o esquema de autenticação e o realm retornado pelo proxy.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="http_query_proxy_authorization"></span>**\_autorização de \_ proxy de consulta http \_**
</dt> <dd> <dl> <dt>

61
</dt> <dt>



Recupera o cabeçalho que é usado para identificar o usuário para um proxy que requer autenticação. Esse cabeçalho só pode ser recuperado antes que a solicitação seja enviada ao servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_CONNECTION"></span><span id="http_query_proxy_connection"></span>**\_conexão de \_ proxy de consulta http \_**
</dt> <dd> <dl> <dt>

69
</dt> <dt>



Recupera o cabeçalho Proxy-Connection.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PUBLIC"></span><span id="http_query_public"></span>**\_público de consulta http \_**
</dt> <dd> <dl> <dt>

8
</dt> <dt>



Recebe os métodos disponíveis neste servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RANGE"></span><span id="http_query_range"></span>**\_intervalo de consulta http \_**
</dt> <dd> <dl> <dt>

62
</dt> <dt>



Recupera o intervalo de bytes de uma entidade.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RAW_HEADERS"></span><span id="http_query_raw_headers"></span>**\_ \_ cabeçalhos brutos de consulta http \_**
</dt> <dd> <dl> <dt>

21
</dt> <dt>



Recebe todos os cabeçalhos retornados pelo servidor. Cada cabeçalho é encerrado por " \\ 0". Um " \\ 0" adicional encerra a lista de cabeçalhos.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="http_query_raw_headers_crlf"></span>**\_ \_ cabeçalhos brutos de consulta http \_ \_ CRLF**
</dt> <dd> <dl> <dt>

22
</dt> <dt>



Recebe todos os cabeçalhos retornados pelo servidor. Cada cabeçalho é separado por uma sequência de CR/LF (retorno de carro/alimentação de linha).


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REFERER"></span><span id="http_query_referer"></span>**\_referenciador de consulta http \_**
</dt> <dd> <dl> <dt>

35
</dt> <dt>



Recebe o Uniform Resource Identifier (URI) do recurso em que o URI solicitado foi obtido.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REFRESH"></span><span id="http_query_refresh"></span>**\_atualização de consulta http \_**
</dt> <dd> <dl> <dt>

46
</dt> <dt>



Obsoleto. Mantido somente para compatibilidade de aplicativos herdados.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REQUEST_METHOD"></span><span id="http_query_request_method"></span>**\_método de \_ solicitação de consulta http \_**
</dt> <dd> <dl> <dt>

45
</dt> <dt>



Recebe o verbo HTTP que está sendo usado na solicitação, normalmente GET ou POST.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RETRY_AFTER"></span><span id="http_query_retry_after"></span>**\_repetição de consulta http \_ \_ após**
</dt> <dd> <dl> <dt>

36
</dt> <dt>



Recupera a quantidade de tempo que o serviço deve estar indisponível.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_SERVER"></span><span id="http_query_server"></span>**\_servidor de consultas http \_**
</dt> <dd> <dl> <dt>

37
</dt> <dt>



Recupera dados sobre o software usado pelo servidor de origem para lidar com a solicitação.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_SET_COOKIE"></span><span id="http_query_set_cookie"></span>**\_cookie de \_ conjunto de consultas http \_**
</dt> <dd> <dl> <dt>

43
</dt> <dt>



Recebe o valor do conjunto de cookies para a solicitação.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_STATUS_CODE"></span><span id="http_query_status_code"></span>**\_código de \_ status de consulta http \_**
</dt> <dd> <dl> <dt>

19
</dt> <dt>



Recebe o código de status retornado pelo servidor. Para obter mais informações e uma lista de valores possíveis, consulte [**códigos de status http**](http-status-codes.md).


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_STATUS_TEXT"></span><span id="http_query_status_text"></span>**\_texto de \_ status da consulta http \_**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



Recebe qualquer texto adicional retornado pelo servidor na linha de resposta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TITLE"></span><span id="http_query_title"></span>**\_título da consulta http \_**
</dt> <dd> <dl> <dt>

38
</dt> <dt>



Obsoleto. Mantido somente para compatibilidade de aplicativos herdados.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TRANSFER_ENCODING"></span><span id="http_query_transfer_encoding"></span>**\_codificação de \_ transferência de consulta http \_**
</dt> <dd> <dl> <dt>

63
</dt> <dt>



Recupera o tipo de transformação que foi aplicado ao corpo da mensagem para que possa ser transferido com segurança entre o remetente e o destinatário.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="http_query_unless_modified_since"></span>**\_consulta http \_ a menos que seja \_ modificado \_ desde**
</dt> <dd> <dl> <dt>

70
</dt> <dt>



Recupera o cabeçalho, a menos que-Modified-Since.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_UPGRADE"></span><span id="http_query_upgrade"></span>**\_atualização de consulta http \_**
</dt> <dd> <dl> <dt>

64
</dt> <dt>



Recupera os protocolos de comunicação adicionais que são suportados pelo servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_URI"></span><span id="http_query_uri"></span>**\_URI de consulta http \_**
</dt> <dd> <dl> <dt>

13
</dt> <dt>



Recebe alguns ou todos os URIs (identificadores de recursos uniformes) pelos quais o recurso de solicitação-URI pode ser identificado.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_USER_AGENT"></span><span id="http_query_user_agent"></span>**\_agente do \_ usuário de consulta http \_**
</dt> <dd> <dl> <dt>

39
</dt> <dt>



Recupera dados sobre o agente do usuário que fez a solicitação.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VARY"></span><span id="http_query_vary"></span>**a \_ consulta http \_ varia**
</dt> <dd> <dl> <dt>

65
</dt> <dt>



Recupera o cabeçalho que indica que a entidade foi selecionada a partir de várias representações disponíveis da resposta usando a negociação controlada pelo servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VERSION"></span><span id="http_query_version"></span>**\_versão da consulta http \_**
</dt> <dd> <dl> <dt>

18
</dt> <dt>



Recebe o último código de resposta retornado pelo servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VIA"></span><span id="http_query_via"></span>**\_consulta http \_ via**
</dt> <dd> <dl> <dt>

66
</dt> <dt>



Recupera os protocolos intermediários e os destinatários entre o agente do usuário e o servidor em solicitações e entre o servidor de origem e o cliente em respostas.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_WARNING"></span><span id="http_query_warning"></span>**\_aviso de consulta http \_**
</dt> <dd> <dl> <dt>

67
</dt> <dt>



Recupera dados adicionais sobre o status de uma resposta que pode não ser refletida pelo código de status de resposta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_WWW_AUTHENTICATE"></span><span id="http_query_www_authenticate"></span>**\_consulta http \_ www \_ Authenticate**
</dt> <dd> <dl> <dt>

40
</dt> <dt>



Recupera o esquema de autenticação e o realm retornado pelo servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_CONTENT_TYPE_OPTIONS"></span><span id="http_query_x_content_type_options"></span>**\_Opções de \_ \_ tipo de \_ conteúdo \_ de consulta http X**
</dt> <dd> <dl> <dt>

79
</dt> <dt>



Recupera o valor do cabeçalho X-Content-Type-Options.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_P3P"></span><span id="http_query_p3p"></span>**\_P3P de consulta http \_**
</dt> <dd> <dl> <dt>

80
</dt> <dt>



Recupera o valor do cabeçalho P3P.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_P2P_PEERDIST"></span><span id="http_query_x_p2p_peerdist"></span>**\_Consulta http \_ X \_ P2P \_ PEERDIST**
</dt> <dd> <dl> <dt>

81
</dt> <dt>



Recupera o valor do cabeçalho X-P2P-PeerDist.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TRANSLATE"></span><span id="http_query_translate"></span>**\_conversão de consulta http \_**
</dt> <dd> <dl> <dt>

82
</dt> <dt>



Recupera o valor do cabeçalho de conversão.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_UA_COMPATIBLE"></span><span id="http_query_x_ua_compatible"></span>**\_consulta http \_ X \_ UA \_ compatível**
</dt> <dd> <dl> <dt>

83
</dt> <dt>



Recupera o valor de cabeçalho compatível com X-UA.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DEFAULT_STYLE"></span><span id="http_query_default_style"></span>**\_ \_ estilo padrão de consulta http \_**
</dt> <dd> <dl> <dt>

84
</dt> <dt>



Recupera o valor do cabeçalho de Default-Style.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_FRAME_OPTIONS"></span><span id="http_query_x_frame_options"></span>**\_Opções de \_ \_ quadros X de consulta \_ http**
</dt> <dd> <dl> <dt>

85
</dt> <dt>



Recupera o valor do cabeçalho X-Frame-Options.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_XSS_PROTECTION"></span><span id="http_query_x_xss_protection"></span>**proteção HTTP de \_ consulta \_ X \_ XSS \_**
</dt> <dd> <dl> <dt>

86
</dt> <dt>



Recupera o valor do cabeçalho X-XSS-Protection.


</dt> </dl> </dd> </dl>

Os sinalizadores modificadores são usados em conjunto com um sinalizador de atributo para modificar a solicitação. Os sinalizadores de modificador modificam o formato dos dados retornados ou indicam onde [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (ou [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) devem Pesquisar os dados.

<dl> <dt>

<span id="HTTP_QUERY_FLAG_COALESCE"></span><span id="http_query_flag_coalesce"></span>**\_União de \_ sinalizador de consulta http \_**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



Não implementado.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_NUMBER"></span><span id="http_query_flag_number"></span>**\_número do \_ sinalizador de consulta http \_**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Retorna os dados como um número de 32 bits para cabeçalhos cujo valor é um número, como o código de status.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="http_query_flag_request_headers"></span>**\_cabeçalhos de \_ solicitação do sinalizador de consulta http \_ \_**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



Consulta somente cabeçalhos de solicitação.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="http_query_flag_systemtime"></span>**\_sinalizador de consulta http \_ \_ SYSTEMTIME**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Retorna o valor do cabeçalho como uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , que não exige que o aplicativo analise os dados. Use para cabeçalhos cujo valor é uma cadeia de caracteres de data/hora, como "hora da última modificação".


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



 

