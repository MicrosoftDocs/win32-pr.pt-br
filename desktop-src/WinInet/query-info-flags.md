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
# <a name="query-info-flags-winineth"></a><span data-ttu-id="44f60-103">Sinalizadores de informações de consulta (Wininet. h)</span><span class="sxs-lookup"><span data-stu-id="44f60-103">Query Info Flags (Wininet.h)</span></span>

<span data-ttu-id="44f60-104">As listas a seguir contêm os atributos e os modificadores usados por [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) e [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="44f60-104">The following lists contain the attributes and modifiers used by [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) and [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85)).</span></span>

<span data-ttu-id="44f60-105">Os sinalizadores de atributo são usados por [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (ou [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) para indicar quais dados recuperar.</span><span class="sxs-lookup"><span data-stu-id="44f60-105">The attribute flags are used by [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (or [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) to indicate what data to retrieve.</span></span> <span data-ttu-id="44f60-106">A maioria dos sinalizadores de atributo mapeia diretamente para um cabeçalho HTTP específico.</span><span class="sxs-lookup"><span data-stu-id="44f60-106">Most of the attribute flags map directly to a specific HTTP header.</span></span> <span data-ttu-id="44f60-107">Também há alguns sinalizadores especiais, como [ \_ \_ \_ cabeçalhos brutos de consulta http](/windows), que não estão relacionados a um cabeçalho específico.</span><span class="sxs-lookup"><span data-stu-id="44f60-107">There are also some special flags, such as [HTTP\_QUERY\_RAW\_HEADERS](/windows), that are not related to a specific header.</span></span>

<dl> <dt>

<span data-ttu-id="44f60-108"><span id="HTTP_QUERY_ACCEPT"></span><span id="http_query_accept"></span>**\_aceitação de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-108"><span id="HTTP_QUERY_ACCEPT"></span><span id="http_query_accept"></span>**HTTP\_QUERY\_ACCEPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-109">24</span><span class="sxs-lookup"><span data-stu-id="44f60-109">24</span></span>
</dt> <dt>



<span data-ttu-id="44f60-110">Recupera os tipos de mídia aceitáveis para a resposta.</span><span class="sxs-lookup"><span data-stu-id="44f60-110">Retrieves the acceptable media types for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-111"><span id="HTTP_QUERY_ACCEPT_CHARSET"></span><span id="http_query_accept_charset"></span>**conjunto \_ de \_ caracteres de aceitação de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-111"><span id="HTTP_QUERY_ACCEPT_CHARSET"></span><span id="http_query_accept_charset"></span>**HTTP\_QUERY\_ACCEPT\_CHARSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-112">25</span><span class="sxs-lookup"><span data-stu-id="44f60-112">25</span></span>
</dt> <dt>



<span data-ttu-id="44f60-113">Recupera os conjuntos de caracteres aceitáveis para a resposta.</span><span class="sxs-lookup"><span data-stu-id="44f60-113">Retrieves the acceptable character sets for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-114"><span id="HTTP_QUERY_ACCEPT_ENCODING"></span><span id="http_query_accept_encoding"></span>**\_codificação de \_ aceitação de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-114"><span id="HTTP_QUERY_ACCEPT_ENCODING"></span><span id="http_query_accept_encoding"></span>**HTTP\_QUERY\_ACCEPT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-115">26</span><span class="sxs-lookup"><span data-stu-id="44f60-115">26</span></span>
</dt> <dt>



<span data-ttu-id="44f60-116">Recupera os valores de codificação de conteúdo aceitáveis para a resposta.</span><span class="sxs-lookup"><span data-stu-id="44f60-116">Retrieves the acceptable content-coding values for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-117"><span id="HTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="http_query_accept_language"></span>**\_linguagem de \_ aceitação de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-117"><span id="HTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="http_query_accept_language"></span>**HTTP\_QUERY\_ACCEPT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-118">27</span><span class="sxs-lookup"><span data-stu-id="44f60-118">27</span></span>
</dt> <dt>



<span data-ttu-id="44f60-119">Recupera os idiomas naturais aceitáveis para a resposta.</span><span class="sxs-lookup"><span data-stu-id="44f60-119">Retrieves the acceptable natural languages for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-120"><span id="HTTP_QUERY_ACCEPT_RANGES"></span><span id="http_query_accept_ranges"></span>**\_intervalos de \_ aceitação de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-120"><span id="HTTP_QUERY_ACCEPT_RANGES"></span><span id="http_query_accept_ranges"></span>**HTTP\_QUERY\_ACCEPT\_RANGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-121">42</span><span class="sxs-lookup"><span data-stu-id="44f60-121">42</span></span>
</dt> <dt>



<span data-ttu-id="44f60-122">Recupera os tipos de solicitações de intervalo que são aceitas para um recurso.</span><span class="sxs-lookup"><span data-stu-id="44f60-122">Retrieves the types of range requests that are accepted for a resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-123"><span id="HTTP_QUERY_AGE"></span><span id="http_query_age"></span>**\_duração da consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-123"><span id="HTTP_QUERY_AGE"></span><span id="http_query_age"></span>**HTTP\_QUERY\_AGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-124">48</span><span class="sxs-lookup"><span data-stu-id="44f60-124">48</span></span>
</dt> <dt>



<span data-ttu-id="44f60-125">Recupera o campo de cabeçalho resposta etária, que contém a estimativa do remetente do período desde que a resposta foi gerada no servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="44f60-125">Retrieves the Age response-header field, which contains the sender's estimate of the amount of time since the response was generated at the origin server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-126"><span id="HTTP_QUERY_ALLOW"></span><span id="http_query_allow"></span>**\_permissão de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-126"><span id="HTTP_QUERY_ALLOW"></span><span id="http_query_allow"></span>**HTTP\_QUERY\_ALLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-127">7</span><span class="sxs-lookup"><span data-stu-id="44f60-127">7</span></span>
</dt> <dt>



<span data-ttu-id="44f60-128">Recebe os verbos HTTP com suporte do servidor.</span><span class="sxs-lookup"><span data-stu-id="44f60-128">Receives the HTTP verbs supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-129"><span id="HTTP_QUERY_AUTHORIZATION"></span><span id="http_query_authorization"></span>**\_autorização de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-129"><span id="HTTP_QUERY_AUTHORIZATION"></span><span id="http_query_authorization"></span>**HTTP\_QUERY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-130">28</span><span class="sxs-lookup"><span data-stu-id="44f60-130">28</span></span>
</dt> <dt>



<span data-ttu-id="44f60-131">Recupera as credenciais de autorização usadas para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="44f60-131">Retrieves the authorization credentials used for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-132"><span id="HTTP_QUERY_CACHE_CONTROL"></span><span id="http_query_cache_control"></span>**\_controle de \_ cache de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-132"><span id="HTTP_QUERY_CACHE_CONTROL"></span><span id="http_query_cache_control"></span>**HTTP\_QUERY\_CACHE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-133">49</span><span class="sxs-lookup"><span data-stu-id="44f60-133">49</span></span>
</dt> <dt>



<span data-ttu-id="44f60-134">Recupera as diretivas de controle de cache.</span><span class="sxs-lookup"><span data-stu-id="44f60-134">Retrieves the cache control directives.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-135"><span id="HTTP_QUERY_CONNECTION"></span><span id="http_query_connection"></span>**\_conexão de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-135"><span id="HTTP_QUERY_CONNECTION"></span><span id="http_query_connection"></span>**HTTP\_QUERY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-136">23</span><span class="sxs-lookup"><span data-stu-id="44f60-136">23</span></span>
</dt> <dt>



<span data-ttu-id="44f60-137">Recupera as opções especificadas para uma conexão específica e não deve ser comunicada por proxies em outras conexões.</span><span class="sxs-lookup"><span data-stu-id="44f60-137">Retrieves any options that are specified for a particular connection and must not be communicated by proxies over further connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-138"><span id="HTTP_QUERY_CONTENT_BASE"></span><span id="http_query_content_base"></span>**\_base de \_ conteúdo de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-138"><span id="HTTP_QUERY_CONTENT_BASE"></span><span id="http_query_content_base"></span>**HTTP\_QUERY\_CONTENT\_BASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-139">50</span><span class="sxs-lookup"><span data-stu-id="44f60-139">50</span></span>
</dt> <dt>



<span data-ttu-id="44f60-140">Recupera o URI de base (Uniform Resource Identifier) para resolver URLs relativas na entidade.</span><span class="sxs-lookup"><span data-stu-id="44f60-140">Retrieves the base URI (Uniform Resource Identifier) for resolving relative URLs within the entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-141"><span id="HTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="http_query_content_description"></span>**\_Descrição do \_ conteúdo da consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-141"><span id="HTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="http_query_content_description"></span>**HTTP\_QUERY\_CONTENT\_DESCRIPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-142">4</span><span class="sxs-lookup"><span data-stu-id="44f60-142">4</span></span>
</dt> <dt>



<span data-ttu-id="44f60-143">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="44f60-143">Obsolete.</span></span> <span data-ttu-id="44f60-144">Mantido somente para compatibilidade de aplicativos herdados.</span><span class="sxs-lookup"><span data-stu-id="44f60-144">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-145"><span id="HTTP_QUERY_CONTENT_DISPOSITION"></span><span id="http_query_content_disposition"></span>**\_disposição de \_ conteúdo de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-145"><span id="HTTP_QUERY_CONTENT_DISPOSITION"></span><span id="http_query_content_disposition"></span>**HTTP\_QUERY\_CONTENT\_DISPOSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-146">47</span><span class="sxs-lookup"><span data-stu-id="44f60-146">47</span></span>
</dt> <dt>



<span data-ttu-id="44f60-147">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="44f60-147">Obsolete.</span></span> <span data-ttu-id="44f60-148">Mantido somente para compatibilidade de aplicativos herdados.</span><span class="sxs-lookup"><span data-stu-id="44f60-148">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-149"><span id="HTTP_QUERY_CONTENT_ENCODING"></span><span id="http_query_content_encoding"></span>**\_codificação de \_ conteúdo de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-149"><span id="HTTP_QUERY_CONTENT_ENCODING"></span><span id="http_query_content_encoding"></span>**HTTP\_QUERY\_CONTENT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-150">29</span><span class="sxs-lookup"><span data-stu-id="44f60-150">29</span></span>
</dt> <dt>



<span data-ttu-id="44f60-151">Recupera as codificações de conteúdo adicionais que foram aplicadas a todo o recurso.</span><span class="sxs-lookup"><span data-stu-id="44f60-151">Retrieves any additional content codings that have been applied to the entire resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-152"><span id="HTTP_QUERY_CONTENT_ID"></span><span id="http_query_content_id"></span>**\_ID do \_ conteúdo da consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-152"><span id="HTTP_QUERY_CONTENT_ID"></span><span id="http_query_content_id"></span>**HTTP\_QUERY\_CONTENT\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-153">3</span><span class="sxs-lookup"><span data-stu-id="44f60-153">3</span></span>
</dt> <dt>



<span data-ttu-id="44f60-154">Recupera a identificação do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="44f60-154">Retrieves the content identification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-155"><span id="HTTP_QUERY_CONTENT_LANGUAGE"></span><span id="http_query_content_language"></span>**\_linguagem de \_ conteúdo de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-155"><span id="HTTP_QUERY_CONTENT_LANGUAGE"></span><span id="http_query_content_language"></span>**HTTP\_QUERY\_CONTENT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-156">6</span><span class="sxs-lookup"><span data-stu-id="44f60-156">6</span></span>
</dt> <dt>



<span data-ttu-id="44f60-157">Recupera o idioma no qual o conteúdo está.</span><span class="sxs-lookup"><span data-stu-id="44f60-157">Retrieves the language that the content is in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-158"><span id="HTTP_QUERY_CONTENT_LENGTH"></span><span id="http_query_content_length"></span>**\_comprimento do \_ conteúdo da consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-158"><span id="HTTP_QUERY_CONTENT_LENGTH"></span><span id="http_query_content_length"></span>**HTTP\_QUERY\_CONTENT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-159">5</span><span class="sxs-lookup"><span data-stu-id="44f60-159">5</span></span>
</dt> <dt>



<span data-ttu-id="44f60-160">Recupera o tamanho do recurso, em bytes.</span><span class="sxs-lookup"><span data-stu-id="44f60-160">Retrieves the size of the resource, in bytes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-161"><span id="HTTP_QUERY_CONTENT_LOCATION"></span><span id="http_query_content_location"></span>**\_local do \_ conteúdo da consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-161"><span id="HTTP_QUERY_CONTENT_LOCATION"></span><span id="http_query_content_location"></span>**HTTP\_QUERY\_CONTENT\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-162">51</span><span class="sxs-lookup"><span data-stu-id="44f60-162">51</span></span>
</dt> <dt>



<span data-ttu-id="44f60-163">Recupera o local do recurso para a entidade incluída na mensagem.</span><span class="sxs-lookup"><span data-stu-id="44f60-163">Retrieves the resource location for the entity enclosed in the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-164"><span id="HTTP_QUERY_CONTENT_MD5"></span><span id="http_query_content_md5"></span>**\_MD5 de \_ conteúdo de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-164"><span id="HTTP_QUERY_CONTENT_MD5"></span><span id="http_query_content_md5"></span>**HTTP\_QUERY\_CONTENT\_MD5**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-165">52</span><span class="sxs-lookup"><span data-stu-id="44f60-165">52</span></span>
</dt> <dt>



<span data-ttu-id="44f60-166">Recupera um resumo MD5 do corpo da entidade com a finalidade de fornecer um MIC (verificação de integridade de mensagem) de ponta a ponta para o corpo da entidade.</span><span class="sxs-lookup"><span data-stu-id="44f60-166">Retrieves an MD5 digest of the entity-body for the purpose of providing an end-to-end message integrity check (MIC) for the entity-body.</span></span> <span data-ttu-id="44f60-167">Para obter mais informações, consulte RFC1864, o campo cabeçalho Content-MD5, em [https://ftp.isi.edu/in-notes/rfc1864.txt](https://tools.ietf.org/html/rfc1864) .</span><span class="sxs-lookup"><span data-stu-id="44f60-167">For more information, see RFC1864, The Content-MD5 Header Field, at [https://ftp.isi.edu/in-notes/rfc1864.txt](https://tools.ietf.org/html/rfc1864).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-168"><span id="HTTP_QUERY_CONTENT_RANGE"></span><span id="http_query_content_range"></span>**\_intervalo de \_ conteúdo de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-168"><span id="HTTP_QUERY_CONTENT_RANGE"></span><span id="http_query_content_range"></span>**HTTP\_QUERY\_CONTENT\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-169">53</span><span class="sxs-lookup"><span data-stu-id="44f60-169">53</span></span>
</dt> <dt>



<span data-ttu-id="44f60-170">Recupera o local no corpo da entidade completa em que o corpo da entidade parcial deve ser inserido e o tamanho total do corpo da entidade completa.</span><span class="sxs-lookup"><span data-stu-id="44f60-170">Retrieves the location in the full entity-body where the partial entity-body should be inserted and the total size of the full entity-body.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-171"><span id="HTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="http_query_content_transfer_encoding"></span>**\_codificação de \_ transferência de conteúdo de consulta http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-171"><span id="HTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="http_query_content_transfer_encoding"></span>**HTTP\_QUERY\_CONTENT\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-172">2</span><span class="sxs-lookup"><span data-stu-id="44f60-172">2</span></span>
</dt> <dt>



<span data-ttu-id="44f60-173">Recebe a codificação de conteúdo adicional que foi aplicada ao recurso.</span><span class="sxs-lookup"><span data-stu-id="44f60-173">Receives the additional content coding that has been applied to the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-174"><span id="HTTP_QUERY_CONTENT_TYPE"></span><span id="http_query_content_type"></span>**\_tipo de \_ conteúdo de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-174"><span id="HTTP_QUERY_CONTENT_TYPE"></span><span id="http_query_content_type"></span>**HTTP\_QUERY\_CONTENT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-175">1</span><span class="sxs-lookup"><span data-stu-id="44f60-175">1</span></span>
</dt> <dt>



<span data-ttu-id="44f60-176">Recebe o tipo de conteúdo do recurso (como texto/HTML).</span><span class="sxs-lookup"><span data-stu-id="44f60-176">Receives the content type of the resource (such as text/html).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-177"><span id="HTTP_QUERY_COOKIE"></span><span id="http_query_cookie"></span>**\_cookie de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-177"><span id="HTTP_QUERY_COOKIE"></span><span id="http_query_cookie"></span>**HTTP\_QUERY\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-178">44</span><span class="sxs-lookup"><span data-stu-id="44f60-178">44</span></span>
</dt> <dt>



<span data-ttu-id="44f60-179">Recupera todos os cookies associados à solicitação.</span><span class="sxs-lookup"><span data-stu-id="44f60-179">Retrieves any cookies associated with the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-180"><span id="HTTP_QUERY_COST"></span><span id="http_query_cost"></span>**\_custo da consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-180"><span id="HTTP_QUERY_COST"></span><span id="http_query_cost"></span>**HTTP\_QUERY\_COST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-181">15</span><span class="sxs-lookup"><span data-stu-id="44f60-181">15</span></span>
</dt> <dt>



<span data-ttu-id="44f60-182">Não tem mais suporte.</span><span class="sxs-lookup"><span data-stu-id="44f60-182">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-183"><span id="HTTP_QUERY_CUSTOM"></span><span id="http_query_custom"></span>**\_personalizado de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-183"><span id="HTTP_QUERY_CUSTOM"></span><span id="http_query_custom"></span>**HTTP\_QUERY\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-184">65535</span><span class="sxs-lookup"><span data-stu-id="44f60-184">65535</span></span>
</dt> <dt>



<span data-ttu-id="44f60-185">Faz com que o [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) procure o nome do cabeçalho especificado em *lpvBuffer* e armazene os dados do cabeçalho em *lpvBuffer*.</span><span class="sxs-lookup"><span data-stu-id="44f60-185">Causes [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) to search for the header name specified in *lpvBuffer* and store the header data in *lpvBuffer*.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-186"><span id="HTTP_QUERY_DATE"></span><span id="http_query_date"></span>**\_data da consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-186"><span id="HTTP_QUERY_DATE"></span><span id="http_query_date"></span>**HTTP\_QUERY\_DATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-187">9</span><span class="sxs-lookup"><span data-stu-id="44f60-187">9</span></span>
</dt> <dt>



<span data-ttu-id="44f60-188">Recebe a data e a hora em que a mensagem foi originada.</span><span class="sxs-lookup"><span data-stu-id="44f60-188">Receives the date and time at which the message was originated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-189"><span id="HTTP_QUERY_DERIVED_FROM"></span><span id="http_query_derived_from"></span>**\_consulta http \_ derivada \_ de**</span><span class="sxs-lookup"><span data-stu-id="44f60-189"><span id="HTTP_QUERY_DERIVED_FROM"></span><span id="http_query_derived_from"></span>**HTTP\_QUERY\_DERIVED\_FROM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-190">14</span><span class="sxs-lookup"><span data-stu-id="44f60-190">14</span></span>
</dt> <dt>



<span data-ttu-id="44f60-191">Não tem mais suporte.</span><span class="sxs-lookup"><span data-stu-id="44f60-191">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-192"><span id="HTTP_QUERY_ECHO_HEADERS"></span><span id="http_query_echo_headers"></span>**\_cabeçalhos de \_ eco de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-192"><span id="HTTP_QUERY_ECHO_HEADERS"></span><span id="http_query_echo_headers"></span>**HTTP\_QUERY\_ECHO\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-193">73</span><span class="sxs-lookup"><span data-stu-id="44f60-193">73</span></span>
</dt> <dt>



<span data-ttu-id="44f60-194">Não implementado atualmente.</span><span class="sxs-lookup"><span data-stu-id="44f60-194">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-195"><span id="HTTP_QUERY_ECHO_HEADERS_CRLF"></span><span id="http_query_echo_headers_crlf"></span>**\_cabeçalhos de eco de consulta http \_ \_ \_ CRLF**</span><span class="sxs-lookup"><span data-stu-id="44f60-195"><span id="HTTP_QUERY_ECHO_HEADERS_CRLF"></span><span id="http_query_echo_headers_crlf"></span>**HTTP\_QUERY\_ECHO\_HEADERS\_CRLF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-196">74</span><span class="sxs-lookup"><span data-stu-id="44f60-196">74</span></span>
</dt> <dt>



<span data-ttu-id="44f60-197">Não implementado atualmente.</span><span class="sxs-lookup"><span data-stu-id="44f60-197">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-198"><span id="HTTP_QUERY_ECHO_REPLY"></span><span id="http_query_echo_reply"></span>**\_resposta de \_ eco de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-198"><span id="HTTP_QUERY_ECHO_REPLY"></span><span id="http_query_echo_reply"></span>**HTTP\_QUERY\_ECHO\_REPLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-199">72</span><span class="sxs-lookup"><span data-stu-id="44f60-199">72</span></span>
</dt> <dt>



<span data-ttu-id="44f60-200">Não implementado atualmente.</span><span class="sxs-lookup"><span data-stu-id="44f60-200">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-201"><span id="HTTP_QUERY_ECHO_REQUEST"></span><span id="http_query_echo_request"></span>**\_solicitação de \_ eco de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-201"><span id="HTTP_QUERY_ECHO_REQUEST"></span><span id="http_query_echo_request"></span>**HTTP\_QUERY\_ECHO\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-202">71</span><span class="sxs-lookup"><span data-stu-id="44f60-202">71</span></span>
</dt> <dt>



<span data-ttu-id="44f60-203">Não implementado atualmente.</span><span class="sxs-lookup"><span data-stu-id="44f60-203">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-204"><span id="HTTP_QUERY_ETAG"></span><span id="http_query_etag"></span>**\_ETag de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-204"><span id="HTTP_QUERY_ETAG"></span><span id="http_query_etag"></span>**HTTP\_QUERY\_ETAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-205">54</span><span class="sxs-lookup"><span data-stu-id="44f60-205">54</span></span>
</dt> <dt>



<span data-ttu-id="44f60-206">Recupera a marca de entidade para a entidade associada.</span><span class="sxs-lookup"><span data-stu-id="44f60-206">Retrieves the entity tag for the associated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-207"><span id="HTTP_QUERY_EXPECT"></span><span id="http_query_expect"></span>**\_espera de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-207"><span id="HTTP_QUERY_EXPECT"></span><span id="http_query_expect"></span>**HTTP\_QUERY\_EXPECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-208">68</span><span class="sxs-lookup"><span data-stu-id="44f60-208">68</span></span>
</dt> <dt>



<span data-ttu-id="44f60-209">Recupera o cabeçalho esperado, que indica se o aplicativo cliente deve esperar respostas da série 100.</span><span class="sxs-lookup"><span data-stu-id="44f60-209">Retrieves the Expect header, which indicates whether the client application should expect 100 series responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-210"><span id="HTTP_QUERY_EXPIRES"></span><span id="http_query_expires"></span>**a \_ consulta http \_ expira**</span><span class="sxs-lookup"><span data-stu-id="44f60-210"><span id="HTTP_QUERY_EXPIRES"></span><span id="http_query_expires"></span>**HTTP\_QUERY\_EXPIRES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-211">10</span><span class="sxs-lookup"><span data-stu-id="44f60-211">10</span></span>
</dt> <dt>



<span data-ttu-id="44f60-212">Recebe a data e a hora após as quais o recurso deve ser considerado desatualizado.</span><span class="sxs-lookup"><span data-stu-id="44f60-212">Receives the date and time after which the resource should be considered outdated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-213"><span id="HTTP_QUERY_FORWARDED"></span><span id="http_query_forwarded"></span>**\_consulta http \_ encaminhada**</span><span class="sxs-lookup"><span data-stu-id="44f60-213"><span id="HTTP_QUERY_FORWARDED"></span><span id="http_query_forwarded"></span>**HTTP\_QUERY\_FORWARDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-214">30</span><span class="sxs-lookup"><span data-stu-id="44f60-214">30</span></span>
</dt> <dt>



<span data-ttu-id="44f60-215">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="44f60-215">Obsolete.</span></span> <span data-ttu-id="44f60-216">Mantido somente para compatibilidade de aplicativos herdados.</span><span class="sxs-lookup"><span data-stu-id="44f60-216">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-217"><span id="HTTP_QUERY_FROM"></span><span id="http_query_from"></span>**\_consulta http \_ de**</span><span class="sxs-lookup"><span data-stu-id="44f60-217"><span id="HTTP_QUERY_FROM"></span><span id="http_query_from"></span>**HTTP\_QUERY\_FROM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-218">31</span><span class="sxs-lookup"><span data-stu-id="44f60-218">31</span></span>
</dt> <dt>



<span data-ttu-id="44f60-219">Recupera o endereço de email do usuário humano que controla o agente do usuário solicitante se o cabeçalho de for fornecido.</span><span class="sxs-lookup"><span data-stu-id="44f60-219">Retrieves the email address for the human user who controls the requesting user agent if the From header is given.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-220"><span id="HTTP_QUERY_HOST"></span><span id="http_query_host"></span>**\_host de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-220"><span id="HTTP_QUERY_HOST"></span><span id="http_query_host"></span>**HTTP\_QUERY\_HOST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-221">55</span><span class="sxs-lookup"><span data-stu-id="44f60-221">55</span></span>
</dt> <dt>



<span data-ttu-id="44f60-222">Recupera o host da Internet e o número da porta do recurso que está sendo solicitado.</span><span class="sxs-lookup"><span data-stu-id="44f60-222">Retrieves the Internet host and port number of the resource being requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-223"><span id="HTTP_QUERY_IF_MATCH"></span><span id="http_query_if_match"></span>**\_consulta http \_ se \_ corresponder**</span><span class="sxs-lookup"><span data-stu-id="44f60-223"><span id="HTTP_QUERY_IF_MATCH"></span><span id="http_query_if_match"></span>**HTTP\_QUERY\_IF\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-224">56</span><span class="sxs-lookup"><span data-stu-id="44f60-224">56</span></span>
</dt> <dt>



<span data-ttu-id="44f60-225">Recupera o conteúdo do campo If-Match cabeçalho de solicitação.</span><span class="sxs-lookup"><span data-stu-id="44f60-225">Retrieves the contents of the If-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-226"><span id="HTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="http_query_if_modified_since"></span>**\_consulta http \_ se \_ modificada \_ desde**</span><span class="sxs-lookup"><span data-stu-id="44f60-226"><span id="HTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="http_query_if_modified_since"></span>**HTTP\_QUERY\_IF\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-227">32</span><span class="sxs-lookup"><span data-stu-id="44f60-227">32</span></span>
</dt> <dt>



<span data-ttu-id="44f60-228">Recupera o conteúdo do cabeçalho If-Modified-Since.</span><span class="sxs-lookup"><span data-stu-id="44f60-228">Retrieves the contents of the If-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-229"><span id="HTTP_QUERY_IF_NONE_MATCH"></span><span id="http_query_if_none_match"></span>**\_consulta http \_ se \_ nenhuma \_ correspondência**</span><span class="sxs-lookup"><span data-stu-id="44f60-229"><span id="HTTP_QUERY_IF_NONE_MATCH"></span><span id="http_query_if_none_match"></span>**HTTP\_QUERY\_IF\_NONE\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-230">57</span><span class="sxs-lookup"><span data-stu-id="44f60-230">57</span></span>
</dt> <dt>



<span data-ttu-id="44f60-231">Recupera o conteúdo do campo de cabeçalho de solicitação If-None-Match.</span><span class="sxs-lookup"><span data-stu-id="44f60-231">Retrieves the contents of the If-None-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-232"><span id="HTTP_QUERY_IF_RANGE"></span><span id="http_query_if_range"></span>**\_consulta http \_ se o \_ intervalo**</span><span class="sxs-lookup"><span data-stu-id="44f60-232"><span id="HTTP_QUERY_IF_RANGE"></span><span id="http_query_if_range"></span>**HTTP\_QUERY\_IF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-233">58</span><span class="sxs-lookup"><span data-stu-id="44f60-233">58</span></span>
</dt> <dt>



<span data-ttu-id="44f60-234">Recupera o conteúdo do campo If-Range cabeçalho de solicitação.</span><span class="sxs-lookup"><span data-stu-id="44f60-234">Retrieves the contents of the If-Range request-header field.</span></span> <span data-ttu-id="44f60-235">Esse cabeçalho permite que o aplicativo cliente Verifique se a entidade relacionada a uma cópia parcial da entidade no cache de aplicativo do cliente não foi atualizada.</span><span class="sxs-lookup"><span data-stu-id="44f60-235">This header enables the client application to verify that the entity related to a partial copy of the entity in the client application cache has not been updated.</span></span> <span data-ttu-id="44f60-236">Se a entidade não tiver sido atualizada, envie as partes que o aplicativo cliente está faltando.</span><span class="sxs-lookup"><span data-stu-id="44f60-236">If the entity has not been updated, send the parts that the client application is missing.</span></span> <span data-ttu-id="44f60-237">Se a entidade tiver sido atualizada, envie toda a entidade atualizada.</span><span class="sxs-lookup"><span data-stu-id="44f60-237">If the entity has been updated, send the entire updated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-238"><span id="HTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="http_query_if_unmodified_since"></span>**\_consulta http \_ se não for \_ modificado \_ desde**</span><span class="sxs-lookup"><span data-stu-id="44f60-238"><span id="HTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="http_query_if_unmodified_since"></span>**HTTP\_QUERY\_IF\_UNMODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-239">59</span><span class="sxs-lookup"><span data-stu-id="44f60-239">59</span></span>
</dt> <dt>



<span data-ttu-id="44f60-240">Recupera o conteúdo do campo de cabeçalho de solicitação se-não modificado-desde.</span><span class="sxs-lookup"><span data-stu-id="44f60-240">Retrieves the contents of the If-Unmodified-Since request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-241"><span id="HTTP_QUERY_LAST_MODIFIED"></span><span id="http_query_last_modified"></span>**\_consulta http \_ modificada pela última vez \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-241"><span id="HTTP_QUERY_LAST_MODIFIED"></span><span id="http_query_last_modified"></span>**HTTP\_QUERY\_LAST\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-242">11</span><span class="sxs-lookup"><span data-stu-id="44f60-242">11</span></span>
</dt> <dt>



<span data-ttu-id="44f60-243">Recebe a data e a hora em que o servidor acredita que o recurso foi modificado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="44f60-243">Receives the date and time at which the server believes the resource was last modified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-244"><span id="HTTP_QUERY_LINK"></span><span id="http_query_link"></span>**\_link de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-244"><span id="HTTP_QUERY_LINK"></span><span id="http_query_link"></span>**HTTP\_QUERY\_LINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-245">16</span><span class="sxs-lookup"><span data-stu-id="44f60-245">16</span></span>
</dt> <dt>



<span data-ttu-id="44f60-246">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="44f60-246">Obsolete.</span></span> <span data-ttu-id="44f60-247">Mantido somente para compatibilidade de aplicativos herdados.</span><span class="sxs-lookup"><span data-stu-id="44f60-247">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-248"><span id="HTTP_QUERY_LOCATION"></span><span id="http_query_location"></span>**\_local da consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-248"><span id="HTTP_QUERY_LOCATION"></span><span id="http_query_location"></span>**HTTP\_QUERY\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-249">33</span><span class="sxs-lookup"><span data-stu-id="44f60-249">33</span></span>
</dt> <dt>



<span data-ttu-id="44f60-250">Recupera o Uniform Resource Identifier absoluto (URI) usado em um cabeçalho de resposta de local.</span><span class="sxs-lookup"><span data-stu-id="44f60-250">Retrieves the absolute Uniform Resource Identifier (URI) used in a Location response-header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-251"><span id="HTTP_QUERY_MAX"></span><span id="http_query_max"></span>**\_máximo de consultas http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-251"><span id="HTTP_QUERY_MAX"></span><span id="http_query_max"></span>**HTTP\_QUERY\_MAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-252">78</span><span class="sxs-lookup"><span data-stu-id="44f60-252">78</span></span>
</dt> <dt>



<span data-ttu-id="44f60-253">Não é um sinalizador de consulta.</span><span class="sxs-lookup"><span data-stu-id="44f60-253">Not a query flag.</span></span> <span data-ttu-id="44f60-254">Indica o valor máximo de um \_ valor de consulta http \_ \* .</span><span class="sxs-lookup"><span data-stu-id="44f60-254">Indicates the maximum value of an HTTP\_QUERY\_\* value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-255"><span id="HTTP_QUERY_MAX_FORWARDS"></span><span id="http_query_max_forwards"></span>**\_ \_ encaminhamentos máximos de consultas http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-255"><span id="HTTP_QUERY_MAX_FORWARDS"></span><span id="http_query_max_forwards"></span>**HTTP\_QUERY\_MAX\_FORWARDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-256">60</span><span class="sxs-lookup"><span data-stu-id="44f60-256">60</span></span>
</dt> <dt>



<span data-ttu-id="44f60-257">Recupera o número de proxies ou gateways que podem encaminhar a solicitação para o próximo servidor de entrada.</span><span class="sxs-lookup"><span data-stu-id="44f60-257">Retrieves the number of proxies or gateways that can forward the request to the next inbound server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-258"><span id="HTTP_QUERY_MESSAGE_ID"></span><span id="http_query_message_id"></span>**\_ID da \_ mensagem de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-258"><span id="HTTP_QUERY_MESSAGE_ID"></span><span id="http_query_message_id"></span>**HTTP\_QUERY\_MESSAGE\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-259">12</span><span class="sxs-lookup"><span data-stu-id="44f60-259">12</span></span>
</dt> <dt>



<span data-ttu-id="44f60-260">Não tem mais suporte.</span><span class="sxs-lookup"><span data-stu-id="44f60-260">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-261"><span id="HTTP_QUERY_MIME_VERSION"></span><span id="http_query_mime_version"></span>**\_versão de \_ MIME de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-261"><span id="HTTP_QUERY_MIME_VERSION"></span><span id="http_query_mime_version"></span>**HTTP\_QUERY\_MIME\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-262">0</span><span class="sxs-lookup"><span data-stu-id="44f60-262">0</span></span>
</dt> <dt>



<span data-ttu-id="44f60-263">Recebe a versão do protocolo MIME que foi usado para construir a mensagem.</span><span class="sxs-lookup"><span data-stu-id="44f60-263">Receives the version of the MIME protocol that was used to construct the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-264"><span id="HTTP_QUERY_ORIG_URI"></span><span id="http_query_orig_uri"></span>**\_URI de \_ orig de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-264"><span id="HTTP_QUERY_ORIG_URI"></span><span id="http_query_orig_uri"></span>**HTTP\_QUERY\_ORIG\_URI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-265">34</span><span class="sxs-lookup"><span data-stu-id="44f60-265">34</span></span>
</dt> <dt>



<span data-ttu-id="44f60-266">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="44f60-266">Obsolete.</span></span> <span data-ttu-id="44f60-267">Mantido somente para compatibilidade de aplicativos herdados.</span><span class="sxs-lookup"><span data-stu-id="44f60-267">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-268"><span id="HTTP_QUERY_PRAGMA"></span><span id="http_query_pragma"></span>**\_pragma da consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-268"><span id="HTTP_QUERY_PRAGMA"></span><span id="http_query_pragma"></span>**HTTP\_QUERY\_PRAGMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-269">17</span><span class="sxs-lookup"><span data-stu-id="44f60-269">17</span></span>
</dt> <dt>



<span data-ttu-id="44f60-270">Recebe as diretivas específicas de implementação que podem se aplicar a qualquer destinatário ao longo da cadeia de solicitação/resposta.</span><span class="sxs-lookup"><span data-stu-id="44f60-270">Receives the implementation-specific directives that might apply to any recipient along the request/response chain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-271"><span id="HTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="http_query_proxy_authenticate"></span>**\_autenticação de \_ proxy de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-271"><span id="HTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="http_query_proxy_authenticate"></span>**HTTP\_QUERY\_PROXY\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-272">41</span><span class="sxs-lookup"><span data-stu-id="44f60-272">41</span></span>
</dt> <dt>



<span data-ttu-id="44f60-273">Recupera o esquema de autenticação e o realm retornado pelo proxy.</span><span class="sxs-lookup"><span data-stu-id="44f60-273">Retrieves the authentication scheme and realm returned by the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-274"><span id="HTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="http_query_proxy_authorization"></span>**\_autorização de \_ proxy de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-274"><span id="HTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="http_query_proxy_authorization"></span>**HTTP\_QUERY\_PROXY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-275">61</span><span class="sxs-lookup"><span data-stu-id="44f60-275">61</span></span>
</dt> <dt>



<span data-ttu-id="44f60-276">Recupera o cabeçalho que é usado para identificar o usuário para um proxy que requer autenticação.</span><span class="sxs-lookup"><span data-stu-id="44f60-276">Retrieves the header that is used to identify the user to a proxy that requires authentication.</span></span> <span data-ttu-id="44f60-277">Esse cabeçalho só pode ser recuperado antes que a solicitação seja enviada ao servidor.</span><span class="sxs-lookup"><span data-stu-id="44f60-277">This header can only be retrieved before the request is sent to the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-278"><span id="HTTP_QUERY_PROXY_CONNECTION"></span><span id="http_query_proxy_connection"></span>**\_conexão de \_ proxy de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-278"><span id="HTTP_QUERY_PROXY_CONNECTION"></span><span id="http_query_proxy_connection"></span>**HTTP\_QUERY\_PROXY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-279">69</span><span class="sxs-lookup"><span data-stu-id="44f60-279">69</span></span>
</dt> <dt>



<span data-ttu-id="44f60-280">Recupera o cabeçalho Proxy-Connection.</span><span class="sxs-lookup"><span data-stu-id="44f60-280">Retrieves the Proxy-Connection header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-281"><span id="HTTP_QUERY_PUBLIC"></span><span id="http_query_public"></span>**\_público de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-281"><span id="HTTP_QUERY_PUBLIC"></span><span id="http_query_public"></span>**HTTP\_QUERY\_PUBLIC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-282">8</span><span class="sxs-lookup"><span data-stu-id="44f60-282">8</span></span>
</dt> <dt>



<span data-ttu-id="44f60-283">Recebe os métodos disponíveis neste servidor.</span><span class="sxs-lookup"><span data-stu-id="44f60-283">Receives methods available at this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-284"><span id="HTTP_QUERY_RANGE"></span><span id="http_query_range"></span>**\_intervalo de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-284"><span id="HTTP_QUERY_RANGE"></span><span id="http_query_range"></span>**HTTP\_QUERY\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-285">62</span><span class="sxs-lookup"><span data-stu-id="44f60-285">62</span></span>
</dt> <dt>



<span data-ttu-id="44f60-286">Recupera o intervalo de bytes de uma entidade.</span><span class="sxs-lookup"><span data-stu-id="44f60-286">Retrieves the byte range of an entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-287"><span id="HTTP_QUERY_RAW_HEADERS"></span><span id="http_query_raw_headers"></span>**\_ \_ cabeçalhos brutos de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-287"><span id="HTTP_QUERY_RAW_HEADERS"></span><span id="http_query_raw_headers"></span>**HTTP\_QUERY\_RAW\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-288">21</span><span class="sxs-lookup"><span data-stu-id="44f60-288">21</span></span>
</dt> <dt>



<span data-ttu-id="44f60-289">Recebe todos os cabeçalhos retornados pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="44f60-289">Receives all the headers returned by the server.</span></span> <span data-ttu-id="44f60-290">Cada cabeçalho é encerrado por " \\ 0".</span><span class="sxs-lookup"><span data-stu-id="44f60-290">Each header is terminated by "\\0".</span></span> <span data-ttu-id="44f60-291">Um " \\ 0" adicional encerra a lista de cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="44f60-291">An additional "\\0" terminates the list of headers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-292"><span id="HTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="http_query_raw_headers_crlf"></span>**\_ \_ cabeçalhos brutos de consulta http \_ \_ CRLF**</span><span class="sxs-lookup"><span data-stu-id="44f60-292"><span id="HTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="http_query_raw_headers_crlf"></span>**HTTP\_QUERY\_RAW\_HEADERS\_CRLF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-293">22</span><span class="sxs-lookup"><span data-stu-id="44f60-293">22</span></span>
</dt> <dt>



<span data-ttu-id="44f60-294">Recebe todos os cabeçalhos retornados pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="44f60-294">Receives all the headers returned by the server.</span></span> <span data-ttu-id="44f60-295">Cada cabeçalho é separado por uma sequência de CR/LF (retorno de carro/alimentação de linha).</span><span class="sxs-lookup"><span data-stu-id="44f60-295">Each header is separated by a carriage return/line feed (CR/LF) sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-296"><span id="HTTP_QUERY_REFERER"></span><span id="http_query_referer"></span>**\_referenciador de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-296"><span id="HTTP_QUERY_REFERER"></span><span id="http_query_referer"></span>**HTTP\_QUERY\_REFERER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-297">35</span><span class="sxs-lookup"><span data-stu-id="44f60-297">35</span></span>
</dt> <dt>



<span data-ttu-id="44f60-298">Recebe o Uniform Resource Identifier (URI) do recurso em que o URI solicitado foi obtido.</span><span class="sxs-lookup"><span data-stu-id="44f60-298">Receives the Uniform Resource Identifier (URI) of the resource where the requested URI was obtained.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-299"><span id="HTTP_QUERY_REFRESH"></span><span id="http_query_refresh"></span>**\_atualização de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-299"><span id="HTTP_QUERY_REFRESH"></span><span id="http_query_refresh"></span>**HTTP\_QUERY\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-300">46</span><span class="sxs-lookup"><span data-stu-id="44f60-300">46</span></span>
</dt> <dt>



<span data-ttu-id="44f60-301">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="44f60-301">Obsolete.</span></span> <span data-ttu-id="44f60-302">Mantido somente para compatibilidade de aplicativos herdados.</span><span class="sxs-lookup"><span data-stu-id="44f60-302">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-303"><span id="HTTP_QUERY_REQUEST_METHOD"></span><span id="http_query_request_method"></span>**\_método de \_ solicitação de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-303"><span id="HTTP_QUERY_REQUEST_METHOD"></span><span id="http_query_request_method"></span>**HTTP\_QUERY\_REQUEST\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-304">45</span><span class="sxs-lookup"><span data-stu-id="44f60-304">45</span></span>
</dt> <dt>



<span data-ttu-id="44f60-305">Recebe o verbo HTTP que está sendo usado na solicitação, normalmente GET ou POST.</span><span class="sxs-lookup"><span data-stu-id="44f60-305">Receives the HTTP verb that is being used in the request, typically GET or POST.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-306"><span id="HTTP_QUERY_RETRY_AFTER"></span><span id="http_query_retry_after"></span>**\_repetição de consulta http \_ \_ após**</span><span class="sxs-lookup"><span data-stu-id="44f60-306"><span id="HTTP_QUERY_RETRY_AFTER"></span><span id="http_query_retry_after"></span>**HTTP\_QUERY\_RETRY\_AFTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-307">36</span><span class="sxs-lookup"><span data-stu-id="44f60-307">36</span></span>
</dt> <dt>



<span data-ttu-id="44f60-308">Recupera a quantidade de tempo que o serviço deve estar indisponível.</span><span class="sxs-lookup"><span data-stu-id="44f60-308">Retrieves the amount of time the service is expected to be unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-309"><span id="HTTP_QUERY_SERVER"></span><span id="http_query_server"></span>**\_servidor de consultas http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-309"><span id="HTTP_QUERY_SERVER"></span><span id="http_query_server"></span>**HTTP\_QUERY\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-310">37</span><span class="sxs-lookup"><span data-stu-id="44f60-310">37</span></span>
</dt> <dt>



<span data-ttu-id="44f60-311">Recupera dados sobre o software usado pelo servidor de origem para lidar com a solicitação.</span><span class="sxs-lookup"><span data-stu-id="44f60-311">Retrieves data about the software used by the origin server to handle the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-312"><span id="HTTP_QUERY_SET_COOKIE"></span><span id="http_query_set_cookie"></span>**\_cookie de \_ conjunto de consultas http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-312"><span id="HTTP_QUERY_SET_COOKIE"></span><span id="http_query_set_cookie"></span>**HTTP\_QUERY\_SET\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-313">43</span><span class="sxs-lookup"><span data-stu-id="44f60-313">43</span></span>
</dt> <dt>



<span data-ttu-id="44f60-314">Recebe o valor do conjunto de cookies para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="44f60-314">Receives the value of the cookie set for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-315"><span id="HTTP_QUERY_STATUS_CODE"></span><span id="http_query_status_code"></span>**\_código de \_ status de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-315"><span id="HTTP_QUERY_STATUS_CODE"></span><span id="http_query_status_code"></span>**HTTP\_QUERY\_STATUS\_CODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-316">19</span><span class="sxs-lookup"><span data-stu-id="44f60-316">19</span></span>
</dt> <dt>



<span data-ttu-id="44f60-317">Recebe o código de status retornado pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="44f60-317">Receives the status code returned by the server.</span></span> <span data-ttu-id="44f60-318">Para obter mais informações e uma lista de valores possíveis, consulte [**códigos de status http**](http-status-codes.md).</span><span class="sxs-lookup"><span data-stu-id="44f60-318">For more information and a list of possible values, see [**HTTP Status Codes**](http-status-codes.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-319"><span id="HTTP_QUERY_STATUS_TEXT"></span><span id="http_query_status_text"></span>**\_texto de \_ status da consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-319"><span id="HTTP_QUERY_STATUS_TEXT"></span><span id="http_query_status_text"></span>**HTTP\_QUERY\_STATUS\_TEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-320">20</span><span class="sxs-lookup"><span data-stu-id="44f60-320">20</span></span>
</dt> <dt>



<span data-ttu-id="44f60-321">Recebe qualquer texto adicional retornado pelo servidor na linha de resposta.</span><span class="sxs-lookup"><span data-stu-id="44f60-321">Receives any additional text returned by the server on the response line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-322"><span id="HTTP_QUERY_TITLE"></span><span id="http_query_title"></span>**\_título da consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-322"><span id="HTTP_QUERY_TITLE"></span><span id="http_query_title"></span>**HTTP\_QUERY\_TITLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-323">38</span><span class="sxs-lookup"><span data-stu-id="44f60-323">38</span></span>
</dt> <dt>



<span data-ttu-id="44f60-324">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="44f60-324">Obsolete.</span></span> <span data-ttu-id="44f60-325">Mantido somente para compatibilidade de aplicativos herdados.</span><span class="sxs-lookup"><span data-stu-id="44f60-325">Maintained for legacy application compatibility only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-326"><span id="HTTP_QUERY_TRANSFER_ENCODING"></span><span id="http_query_transfer_encoding"></span>**\_codificação de \_ transferência de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-326"><span id="HTTP_QUERY_TRANSFER_ENCODING"></span><span id="http_query_transfer_encoding"></span>**HTTP\_QUERY\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-327">63</span><span class="sxs-lookup"><span data-stu-id="44f60-327">63</span></span>
</dt> <dt>



<span data-ttu-id="44f60-328">Recupera o tipo de transformação que foi aplicado ao corpo da mensagem para que possa ser transferido com segurança entre o remetente e o destinatário.</span><span class="sxs-lookup"><span data-stu-id="44f60-328">Retrieves the type of transformation that has been applied to the message body so it can be safely transferred between the sender and recipient.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-329"><span id="HTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="http_query_unless_modified_since"></span>**\_consulta http \_ a menos que seja \_ modificado \_ desde**</span><span class="sxs-lookup"><span data-stu-id="44f60-329"><span id="HTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="http_query_unless_modified_since"></span>**HTTP\_QUERY\_UNLESS\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-330">70</span><span class="sxs-lookup"><span data-stu-id="44f60-330">70</span></span>
</dt> <dt>



<span data-ttu-id="44f60-331">Recupera o cabeçalho, a menos que-Modified-Since.</span><span class="sxs-lookup"><span data-stu-id="44f60-331">Retrieves the Unless-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-332"><span id="HTTP_QUERY_UPGRADE"></span><span id="http_query_upgrade"></span>**\_atualização de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-332"><span id="HTTP_QUERY_UPGRADE"></span><span id="http_query_upgrade"></span>**HTTP\_QUERY\_UPGRADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-333">64</span><span class="sxs-lookup"><span data-stu-id="44f60-333">64</span></span>
</dt> <dt>



<span data-ttu-id="44f60-334">Recupera os protocolos de comunicação adicionais que são suportados pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="44f60-334">Retrieves the additional communication protocols that are supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-335"><span id="HTTP_QUERY_URI"></span><span id="http_query_uri"></span>**\_URI de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-335"><span id="HTTP_QUERY_URI"></span><span id="http_query_uri"></span>**HTTP\_QUERY\_URI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-336">13</span><span class="sxs-lookup"><span data-stu-id="44f60-336">13</span></span>
</dt> <dt>



<span data-ttu-id="44f60-337">Recebe alguns ou todos os URIs (identificadores de recursos uniformes) pelos quais o recurso de solicitação-URI pode ser identificado.</span><span class="sxs-lookup"><span data-stu-id="44f60-337">Receives some or all of the Uniform Resource Identifiers (URIs) by which the Request-URI resource can be identified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-338"><span id="HTTP_QUERY_USER_AGENT"></span><span id="http_query_user_agent"></span>**\_agente do \_ usuário de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-338"><span id="HTTP_QUERY_USER_AGENT"></span><span id="http_query_user_agent"></span>**HTTP\_QUERY\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-339">39</span><span class="sxs-lookup"><span data-stu-id="44f60-339">39</span></span>
</dt> <dt>



<span data-ttu-id="44f60-340">Recupera dados sobre o agente do usuário que fez a solicitação.</span><span class="sxs-lookup"><span data-stu-id="44f60-340">Retrieves data about the user agent that made the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-341"><span id="HTTP_QUERY_VARY"></span><span id="http_query_vary"></span>**a \_ consulta http \_ varia**</span><span class="sxs-lookup"><span data-stu-id="44f60-341"><span id="HTTP_QUERY_VARY"></span><span id="http_query_vary"></span>**HTTP\_QUERY\_VARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-342">65</span><span class="sxs-lookup"><span data-stu-id="44f60-342">65</span></span>
</dt> <dt>



<span data-ttu-id="44f60-343">Recupera o cabeçalho que indica que a entidade foi selecionada a partir de várias representações disponíveis da resposta usando a negociação controlada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="44f60-343">Retrieves the header that indicates that the entity was selected from a number of available representations of the response using server-driven negotiation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-344"><span id="HTTP_QUERY_VERSION"></span><span id="http_query_version"></span>**\_versão da consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-344"><span id="HTTP_QUERY_VERSION"></span><span id="http_query_version"></span>**HTTP\_QUERY\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-345">18</span><span class="sxs-lookup"><span data-stu-id="44f60-345">18</span></span>
</dt> <dt>



<span data-ttu-id="44f60-346">Recebe o último código de resposta retornado pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="44f60-346">Receives the last response code returned by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-347"><span id="HTTP_QUERY_VIA"></span><span id="http_query_via"></span>**\_consulta http \_ via**</span><span class="sxs-lookup"><span data-stu-id="44f60-347"><span id="HTTP_QUERY_VIA"></span><span id="http_query_via"></span>**HTTP\_QUERY\_VIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-348">66</span><span class="sxs-lookup"><span data-stu-id="44f60-348">66</span></span>
</dt> <dt>



<span data-ttu-id="44f60-349">Recupera os protocolos intermediários e os destinatários entre o agente do usuário e o servidor em solicitações e entre o servidor de origem e o cliente em respostas.</span><span class="sxs-lookup"><span data-stu-id="44f60-349">Retrieves the intermediate protocols and recipients between the user agent and the server on requests, and between the origin server and the client on responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-350"><span id="HTTP_QUERY_WARNING"></span><span id="http_query_warning"></span>**\_aviso de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-350"><span id="HTTP_QUERY_WARNING"></span><span id="http_query_warning"></span>**HTTP\_QUERY\_WARNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-351">67</span><span class="sxs-lookup"><span data-stu-id="44f60-351">67</span></span>
</dt> <dt>



<span data-ttu-id="44f60-352">Recupera dados adicionais sobre o status de uma resposta que pode não ser refletida pelo código de status de resposta.</span><span class="sxs-lookup"><span data-stu-id="44f60-352">Retrieves additional data about the status of a response that might not be reflected by the response status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-353"><span id="HTTP_QUERY_WWW_AUTHENTICATE"></span><span id="http_query_www_authenticate"></span>**\_consulta http \_ www \_ Authenticate**</span><span class="sxs-lookup"><span data-stu-id="44f60-353"><span id="HTTP_QUERY_WWW_AUTHENTICATE"></span><span id="http_query_www_authenticate"></span>**HTTP\_QUERY\_WWW\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-354">40</span><span class="sxs-lookup"><span data-stu-id="44f60-354">40</span></span>
</dt> <dt>



<span data-ttu-id="44f60-355">Recupera o esquema de autenticação e o realm retornado pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="44f60-355">Retrieves the authentication scheme and realm returned by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-356"><span id="HTTP_QUERY_X_CONTENT_TYPE_OPTIONS"></span><span id="http_query_x_content_type_options"></span>**\_Opções de \_ \_ tipo de \_ conteúdo \_ de consulta http X**</span><span class="sxs-lookup"><span data-stu-id="44f60-356"><span id="HTTP_QUERY_X_CONTENT_TYPE_OPTIONS"></span><span id="http_query_x_content_type_options"></span>**HTTP\_QUERY\_X\_CONTENT\_TYPE\_OPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-357">79</span><span class="sxs-lookup"><span data-stu-id="44f60-357">79</span></span>
</dt> <dt>



<span data-ttu-id="44f60-358">Recupera o valor do cabeçalho X-Content-Type-Options.</span><span class="sxs-lookup"><span data-stu-id="44f60-358">Retrieves the X-Content-Type-Options header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-359"><span id="HTTP_QUERY_P3P"></span><span id="http_query_p3p"></span>**\_P3P de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-359"><span id="HTTP_QUERY_P3P"></span><span id="http_query_p3p"></span>**HTTP\_QUERY\_P3P**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-360">80</span><span class="sxs-lookup"><span data-stu-id="44f60-360">80</span></span>
</dt> <dt>



<span data-ttu-id="44f60-361">Recupera o valor do cabeçalho P3P.</span><span class="sxs-lookup"><span data-stu-id="44f60-361">Retrieves the P3P header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-362"><span id="HTTP_QUERY_X_P2P_PEERDIST"></span><span id="http_query_x_p2p_peerdist"></span>**\_Consulta http \_ X \_ P2P \_ PEERDIST**</span><span class="sxs-lookup"><span data-stu-id="44f60-362"><span id="HTTP_QUERY_X_P2P_PEERDIST"></span><span id="http_query_x_p2p_peerdist"></span>**HTTP\_QUERY\_X\_P2P\_PEERDIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-363">81</span><span class="sxs-lookup"><span data-stu-id="44f60-363">81</span></span>
</dt> <dt>



<span data-ttu-id="44f60-364">Recupera o valor do cabeçalho X-P2P-PeerDist.</span><span class="sxs-lookup"><span data-stu-id="44f60-364">Retrieves the X-P2P-PeerDist header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-365"><span id="HTTP_QUERY_TRANSLATE"></span><span id="http_query_translate"></span>**\_conversão de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-365"><span id="HTTP_QUERY_TRANSLATE"></span><span id="http_query_translate"></span>**HTTP\_QUERY\_TRANSLATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-366">82</span><span class="sxs-lookup"><span data-stu-id="44f60-366">82</span></span>
</dt> <dt>



<span data-ttu-id="44f60-367">Recupera o valor do cabeçalho de conversão.</span><span class="sxs-lookup"><span data-stu-id="44f60-367">Retrieves the translate header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-368"><span id="HTTP_QUERY_X_UA_COMPATIBLE"></span><span id="http_query_x_ua_compatible"></span>**\_consulta http \_ X \_ UA \_ compatível**</span><span class="sxs-lookup"><span data-stu-id="44f60-368"><span id="HTTP_QUERY_X_UA_COMPATIBLE"></span><span id="http_query_x_ua_compatible"></span>**HTTP\_QUERY\_X\_UA\_COMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-369">83</span><span class="sxs-lookup"><span data-stu-id="44f60-369">83</span></span>
</dt> <dt>



<span data-ttu-id="44f60-370">Recupera o valor de cabeçalho compatível com X-UA.</span><span class="sxs-lookup"><span data-stu-id="44f60-370">Retrieves the X-UA-Compatible header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-371"><span id="HTTP_QUERY_DEFAULT_STYLE"></span><span id="http_query_default_style"></span>**\_ \_ estilo padrão de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-371"><span id="HTTP_QUERY_DEFAULT_STYLE"></span><span id="http_query_default_style"></span>**HTTP\_QUERY\_DEFAULT\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-372">84</span><span class="sxs-lookup"><span data-stu-id="44f60-372">84</span></span>
</dt> <dt>



<span data-ttu-id="44f60-373">Recupera o valor do cabeçalho de Default-Style.</span><span class="sxs-lookup"><span data-stu-id="44f60-373">Retrieves the Default-Style header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-374"><span id="HTTP_QUERY_X_FRAME_OPTIONS"></span><span id="http_query_x_frame_options"></span>**\_Opções de \_ \_ quadros X de consulta \_ http**</span><span class="sxs-lookup"><span data-stu-id="44f60-374"><span id="HTTP_QUERY_X_FRAME_OPTIONS"></span><span id="http_query_x_frame_options"></span>**HTTP\_QUERY\_X\_FRAME\_OPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-375">85</span><span class="sxs-lookup"><span data-stu-id="44f60-375">85</span></span>
</dt> <dt>



<span data-ttu-id="44f60-376">Recupera o valor do cabeçalho X-Frame-Options.</span><span class="sxs-lookup"><span data-stu-id="44f60-376">Retrieves the X-Frame-Options header value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-377"><span id="HTTP_QUERY_X_XSS_PROTECTION"></span><span id="http_query_x_xss_protection"></span>**proteção HTTP de \_ consulta \_ X \_ XSS \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-377"><span id="HTTP_QUERY_X_XSS_PROTECTION"></span><span id="http_query_x_xss_protection"></span>**HTTP\_QUERY\_X\_XSS\_PROTECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-378">86</span><span class="sxs-lookup"><span data-stu-id="44f60-378">86</span></span>
</dt> <dt>



<span data-ttu-id="44f60-379">Recupera o valor do cabeçalho X-XSS-Protection.</span><span class="sxs-lookup"><span data-stu-id="44f60-379">Retrieves the X-XSS-Protection header value.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="44f60-380">Os sinalizadores modificadores são usados em conjunto com um sinalizador de atributo para modificar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="44f60-380">The modifier flags are used in conjunction with an attribute flag to modify the request.</span></span> <span data-ttu-id="44f60-381">Os sinalizadores de modificador modificam o formato dos dados retornados ou indicam onde [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (ou [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) devem Pesquisar os dados.</span><span class="sxs-lookup"><span data-stu-id="44f60-381">Modifier flags either modify the format of the data returned or indicate where [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (or [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) should search for the data.</span></span>

<dl> <dt>

<span data-ttu-id="44f60-382"><span id="HTTP_QUERY_FLAG_COALESCE"></span><span id="http_query_flag_coalesce"></span>**\_União de \_ sinalizador de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-382"><span id="HTTP_QUERY_FLAG_COALESCE"></span><span id="http_query_flag_coalesce"></span>**HTTP\_QUERY\_FLAG\_COALESCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-383">0x10000000</span><span class="sxs-lookup"><span data-stu-id="44f60-383">0x10000000</span></span>
</dt> <dt>



<span data-ttu-id="44f60-384">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="44f60-384">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-385"><span id="HTTP_QUERY_FLAG_NUMBER"></span><span id="http_query_flag_number"></span>**\_número do \_ sinalizador de consulta http \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-385"><span id="HTTP_QUERY_FLAG_NUMBER"></span><span id="http_query_flag_number"></span>**HTTP\_QUERY\_FLAG\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-386">0x20000000</span><span class="sxs-lookup"><span data-stu-id="44f60-386">0x20000000</span></span>
</dt> <dt>



<span data-ttu-id="44f60-387">Retorna os dados como um número de 32 bits para cabeçalhos cujo valor é um número, como o código de status.</span><span class="sxs-lookup"><span data-stu-id="44f60-387">Returns the data as a 32-bit number for headers whose value is a number, such as the status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-388"><span id="HTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="http_query_flag_request_headers"></span>**\_cabeçalhos de \_ solicitação do sinalizador de consulta http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="44f60-388"><span id="HTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="http_query_flag_request_headers"></span>**HTTP\_QUERY\_FLAG\_REQUEST\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-389">0x80000000</span><span class="sxs-lookup"><span data-stu-id="44f60-389">0x80000000</span></span>
</dt> <dt>



<span data-ttu-id="44f60-390">Consulta somente cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="44f60-390">Queries request headers only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44f60-391"><span id="HTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="http_query_flag_systemtime"></span>**\_sinalizador de consulta http \_ \_ SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="44f60-391"><span id="HTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="http_query_flag_systemtime"></span>**HTTP\_QUERY\_FLAG\_SYSTEMTIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44f60-392">0x40000000</span><span class="sxs-lookup"><span data-stu-id="44f60-392">0x40000000</span></span>
</dt> <dt>



<span data-ttu-id="44f60-393">Retorna o valor do cabeçalho como uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , que não exige que o aplicativo analise os dados.</span><span class="sxs-lookup"><span data-stu-id="44f60-393">Returns the header value as a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure, which does not require the application to parse the data.</span></span> <span data-ttu-id="44f60-394">Use para cabeçalhos cujo valor é uma cadeia de caracteres de data/hora, como "hora da última modificação".</span><span class="sxs-lookup"><span data-stu-id="44f60-394">Use for headers whose value is a date/time string, such as "Last-Modified-Time".</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44f60-395">Comentários</span><span class="sxs-lookup"><span data-stu-id="44f60-395">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="44f60-396">O WinINet não oferece suporte a implementações de servidor.</span><span class="sxs-lookup"><span data-stu-id="44f60-396">WinINet does not support server implementations.</span></span> <span data-ttu-id="44f60-397">Além disso, ele não deve ser usado de um serviço.</span><span class="sxs-lookup"><span data-stu-id="44f60-397">In addition, it should not be used from a service.</span></span> <span data-ttu-id="44f60-398">Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="44f60-398">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="44f60-399">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44f60-399">Requirements</span></span>



| <span data-ttu-id="44f60-400">Requisito</span><span class="sxs-lookup"><span data-stu-id="44f60-400">Requirement</span></span> | <span data-ttu-id="44f60-401">Valor</span><span class="sxs-lookup"><span data-stu-id="44f60-401">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="44f60-402">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44f60-402">Minimum supported client</span></span><br/> | <span data-ttu-id="44f60-403">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="44f60-403">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="44f60-404">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44f60-404">Minimum supported server</span></span><br/> | <span data-ttu-id="44f60-405">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="44f60-405">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="44f60-406">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="44f60-406">Header</span></span><br/>                   | <dl> <span data-ttu-id="44f60-407"><dt>WinInet. h</dt></span><span class="sxs-lookup"><span data-stu-id="44f60-407"><dt>Wininet.h</dt></span></span> </dl> |



 

