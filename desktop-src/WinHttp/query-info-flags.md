---
description: Esses atributos e modificadores são usados por WinHttpQueryHeaders.
ms.assetid: c26dac1d-9a75-440a-a0ef-a2029f138f3b
title: Sinalizadores de Informações de Consulta (Winhttp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b3d8a7f95f0e093f175901e4bed30f4055a04b8
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396621"
---
# <a name="query-info-flags-winhttph"></a><span data-ttu-id="52420-103">Sinalizadores de Informações de Consulta (Winhttp.h)</span><span class="sxs-lookup"><span data-stu-id="52420-103">Query Info Flags (Winhttp.h)</span></span>

<span data-ttu-id="52420-104">Esses atributos e modificadores são usados [**por WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span><span class="sxs-lookup"><span data-stu-id="52420-104">These attributes and modifiers are used by [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>

<span data-ttu-id="52420-105">Os sinalizadores de atributo são usados [**por WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) para indicar quais informações recuperar.</span><span class="sxs-lookup"><span data-stu-id="52420-105">The attribute flags are used by [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) to indicate what information to retrieve.</span></span> <span data-ttu-id="52420-106">A maioria dos sinalizadores de atributo é mapeada diretamente para um cabeçalho HTTP específico.</span><span class="sxs-lookup"><span data-stu-id="52420-106">Most of the attribute flags map directly to a specific HTTP header.</span></span> <span data-ttu-id="52420-107">Também há alguns sinalizadores especiais, como OS HEADERS BRUTOS DE CONSULTA \_ WINHTTP, que não estão relacionados \_ \_ a um título específico.</span><span class="sxs-lookup"><span data-stu-id="52420-107">There are also some special flags, such as WINHTTP\_QUERY\_RAW\_HEADERS, that are not related to a specific header.</span></span>

<dl> <dt>

<span data-ttu-id="52420-108"><span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**WINHTTP \_ QUERY \_ ACCEPT**</span><span class="sxs-lookup"><span data-stu-id="52420-108"><span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**WINHTTP\_QUERY\_ACCEPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-109">Recupera os tipos de mídia aceitáveis para a resposta.</span><span class="sxs-lookup"><span data-stu-id="52420-109">Retrieves the acceptable media types for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-110"><span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**WINHTTP \_ QUERY \_ ACCEPT \_ CHARSET**</span><span class="sxs-lookup"><span data-stu-id="52420-110"><span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**WINHTTP\_QUERY\_ACCEPT\_CHARSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-111">Recupera os conjuntos de caracteres aceitáveis para a resposta.</span><span class="sxs-lookup"><span data-stu-id="52420-111">Retrieves the acceptable character sets for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-112"><span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**CODIFICAÇÃO WINHTTP \_ QUERY \_ ACCEPT \_**</span><span class="sxs-lookup"><span data-stu-id="52420-112"><span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**WINHTTP\_QUERY\_ACCEPT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-113">Recupera os valores aceitáveis de codificação de conteúdo para a resposta.</span><span class="sxs-lookup"><span data-stu-id="52420-113">Retrieves the acceptable content-coding values for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-114"><span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**WINHTTP \_ QUERY \_ ACCEPT \_ LANGUAGE**</span><span class="sxs-lookup"><span data-stu-id="52420-114"><span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**WINHTTP\_QUERY\_ACCEPT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-115">Recupera os idiomas naturais aceitáveis para a resposta.</span><span class="sxs-lookup"><span data-stu-id="52420-115">Retrieves the acceptable natural languages for the response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-116"><span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**INTERVALOS DE ACEITAÇÃO \_ DE \_ CONSULTA WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-116"><span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**WINHTTP\_QUERY\_ACCEPT\_RANGES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-117">Recupera os tipos de solicitações de intervalo que são aceitas para um recurso.</span><span class="sxs-lookup"><span data-stu-id="52420-117">Retrieves the types of range requests that are accepted for a resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-118"><span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**IDADE DA CONSULTA WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="52420-118"><span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**WINHTTP\_QUERY\_AGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-119">Recupera o campo idade response-header, que contém a estimativa do remetente da quantidade de tempo desde que a resposta foi gerada no servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="52420-119">Retrieves the Age response-header field, which contains the sender's estimate of the amount of time since the response was generated at the originating server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-120"><span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**WINHTTP \_ QUERY \_ ALLOW**</span><span class="sxs-lookup"><span data-stu-id="52420-120"><span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**WINHTTP\_QUERY\_ALLOW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-121">Recebe os [**verbos HTTP com**](glossary.md) suporte pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="52420-121">Receives the [**HTTP verbs**](glossary.md) supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-122"><span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**INFORMAÇÕES DE \_ AUTENTICAÇÃO DE CONSULTA WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="52420-122"><span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**WINHTTP\_QUERY\_AUTHENTICATION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-123">Recupera o Authentication-Info de dados.</span><span class="sxs-lookup"><span data-stu-id="52420-123">Retrieves the Authentication-Info header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-124"><span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**AUTORIZAÇÃO DE CONSULTA WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="52420-124"><span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**WINHTTP\_QUERY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-125">Recupera as credenciais de autorização usadas para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="52420-125">Retrieves the authorization credentials used for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-126"><span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**CONTROLE DE CACHE DE CONSULTA WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="52420-126"><span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**WINHTTP\_QUERY\_CACHE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-127">Recupera as diretivas de controle de cache.</span><span class="sxs-lookup"><span data-stu-id="52420-127">Retrieves the cache control directives.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-128"><span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**CONEXÃO DE CONSULTA \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="52420-128"><span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**WINHTTP\_QUERY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-129">Recupera todas as opções especificadas para uma conexão específica e não devem ser comunicadas por proxies em conexões posteriores.</span><span class="sxs-lookup"><span data-stu-id="52420-129">Retrieves any options that are specified for a particular connection and must not be communicated by proxies over further connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-130"><span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**BASE DE CONTEÚDO DE CONSULTA WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="52420-130"><span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**WINHTTP\_QUERY\_CONTENT\_BASE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-131">Recupera o URI (Uniform Resource Identifier base) para resolver URLs relativas dentro da entidade.</span><span class="sxs-lookup"><span data-stu-id="52420-131">Retrieves the base Uniform Resource Identifier (URI) to resolve relative URLs within the entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-132"><span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**DESCRIÇÃO DO CONTEÚDO DA CONSULTA WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="52420-132"><span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**WINHTTP\_QUERY\_CONTENT\_DESCRIPTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-133">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="52420-133">Obsolete.</span></span> <span data-ttu-id="52420-134">Mantido para compatibilidade de aplicativo herdado.</span><span class="sxs-lookup"><span data-stu-id="52420-134">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-135"><span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**DISPOSIÇÃO DO CONTEÚDO DA CONSULTA WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="52420-135"><span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**WINHTTP\_QUERY\_CONTENT\_DISPOSITION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-136">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="52420-136">Obsolete.</span></span> <span data-ttu-id="52420-137">Mantido para compatibilidade de aplicativo herdado.</span><span class="sxs-lookup"><span data-stu-id="52420-137">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-138"><span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**CODIFICAÇÃO DE CONTEÚDO \_ \_ DE CONSULTA WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-138"><span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**WINHTTP\_QUERY\_CONTENT\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-139">Recupera a codificação de conteúdo adicional que foi aplicada a todo o recurso.</span><span class="sxs-lookup"><span data-stu-id="52420-139">Retrieves additional content coding that has been applied to the entire resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-140"><span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**ID DE CONTEÚDO DA CONSULTA WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="52420-140"><span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**WINHTTP\_QUERY\_CONTENT\_ID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-141">Recupera a identificação do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="52420-141">Retrieves the content identification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-142"><span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**LINGUAGEM DE CONTEÚDO DE CONSULTA WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="52420-142"><span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**WINHTTP\_QUERY\_CONTENT\_LANGUAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-143">Recupera o idioma em que o conteúdo é gravado.</span><span class="sxs-lookup"><span data-stu-id="52420-143">Retrieves the language that the content is written in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-144"><span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**TAMANHO DO CONTEÚDO DA CONSULTA WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="52420-144"><span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**WINHTTP\_QUERY\_CONTENT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-145">Recupera o tamanho do recurso, em bytes.</span><span class="sxs-lookup"><span data-stu-id="52420-145">Retrieves the size of the resource, in bytes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-146"><span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**LOCAL DO CONTEÚDO DA CONSULTA WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="52420-146"><span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**WINHTTP\_QUERY\_CONTENT\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-147">Recupera o local do recurso para a entidade delimitada na mensagem.</span><span class="sxs-lookup"><span data-stu-id="52420-147">Retrieves the resource location for the entity enclosed in the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-148"><span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**WINHTTP \_ QUERY \_ CONTENT \_ MD5**</span><span class="sxs-lookup"><span data-stu-id="52420-148"><span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**WINHTTP\_QUERY\_CONTENT\_MD5**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-149">Recupera um resumo MD5 do corpo da entidade com a finalidade de fornecer uma verificação de integridade da mensagem de ponta a ponta para o corpo da entidade.</span><span class="sxs-lookup"><span data-stu-id="52420-149">Retrieves an MD5 digest of the entity body for the purpose of providing an end-to-end message integrity check for the entity body.</span></span> <span data-ttu-id="52420-150">Para obter mais informações, [consulte RFC 1864](https://www.ietf.org/rfc/rfc1864.txt).</span><span class="sxs-lookup"><span data-stu-id="52420-150">For more information, see [RFC 1864](https://www.ietf.org/rfc/rfc1864.txt).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-151"><span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**INTERVALO DE CONTEÚDO DE CONSULTA WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="52420-151"><span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**WINHTTP\_QUERY\_CONTENT\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-152">Recupera o local no corpo completo da entidade em que o corpo parcial da entidade deve ser inserido e o tamanho total do corpo da entidade completo.</span><span class="sxs-lookup"><span data-stu-id="52420-152">Retrieves the location in the full entity body where the partial entity body should be inserted and the total size of the full entity body.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-153"><span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**CODIFICAÇÃO DE TRANSFERÊNCIA DE \_ \_ CONTEÚDO DE \_ CONSULTA \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="52420-153"><span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**WINHTTP\_QUERY\_CONTENT\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-154">Recupera uma transformação de codificação aplicável a um corpo da entidade.</span><span class="sxs-lookup"><span data-stu-id="52420-154">Retrieves an encoding transformation applicable to an entity-body.</span></span> <span data-ttu-id="52420-155">Ele pode já ter sido aplicado, pode precisar ser aplicado ou pode ser opcionalmente aplicável.</span><span class="sxs-lookup"><span data-stu-id="52420-155">It may already have been applied, may need to be applied, or may be optionally applicable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-156"><span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**TIPO DE CONTEÚDO DE CONSULTA WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="52420-156"><span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**WINHTTP\_QUERY\_CONTENT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-157">Recebe o tipo de conteúdo do recurso, como texto ou html.</span><span class="sxs-lookup"><span data-stu-id="52420-157">Receives the content type of the resource, such as text or html.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-158"><span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**COOKIE DE CONSULTA WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="52420-158"><span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**WINHTTP\_QUERY\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-159">Recupera todos os cookies associados à solicitação.</span><span class="sxs-lookup"><span data-stu-id="52420-159">Retrieves any cookies associated with the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-160"><span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**CUSTO DA CONSULTA WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="52420-160"><span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**WINHTTP\_QUERY\_COST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-161">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="52420-161">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-162"><span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**WINHTTP \_ QUERY \_ CUSTOM**</span><span class="sxs-lookup"><span data-stu-id="52420-162"><span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**WINHTTP\_QUERY\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-163">Faz [**com que WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) pesquise o nome do título especificado no parâmetro *pwszName* e armazene as informações de título *em lpBuffer*.</span><span class="sxs-lookup"><span data-stu-id="52420-163">Causes [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) to search for the header name specified in the *pwszName* parameter and store the header information in *lpBuffer*.</span></span> <span data-ttu-id="52420-164">Um aplicativo pode usar **WINHTTP \_ OPTION RECEIVE RESPONSE \_ \_ \_ TIMEOUT** para limitar o tempo máximo que essa consulta aguarda para que todos os títulos sejam recebidos.</span><span class="sxs-lookup"><span data-stu-id="52420-164">An application can use **WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT** to limit the maximum time this query waits for all headers to be received.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-165"><span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**WINHTTP \_ QUERY \_ DATE**</span><span class="sxs-lookup"><span data-stu-id="52420-165"><span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**WINHTTP\_QUERY\_DATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-166">Recebe a data e a hora em que a mensagem foi originada.</span><span class="sxs-lookup"><span data-stu-id="52420-166">Receives the date and time at which the message was originated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-167"><span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**CONSULTA WINHTTP \_ \_ DERIVADA \_ DE**</span><span class="sxs-lookup"><span data-stu-id="52420-167"><span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**WINHTTP\_QUERY\_DERIVED\_FROM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-168">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="52420-168">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-169"><span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**WINHTTP \_ QUERY \_ ETAG**</span><span class="sxs-lookup"><span data-stu-id="52420-169"><span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**WINHTTP\_QUERY\_ETAG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-170">Recupera a marca de entidade para a entidade associada.</span><span class="sxs-lookup"><span data-stu-id="52420-170">Retrieves the entity tag for the associated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-171"><span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**WINHTTP \_ QUERY \_ EXPECT**</span><span class="sxs-lookup"><span data-stu-id="52420-171"><span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**WINHTTP\_QUERY\_EXPECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-172">Recupera o header Expect, que indica se o aplicativo cliente deve esperar respostas da série 100.</span><span class="sxs-lookup"><span data-stu-id="52420-172">Retrieves the Expect header, which indicates whether the client application should expect 100 series responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-173"><span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**A CONSULTA WINHTTP \_ \_ EXPIRA**</span><span class="sxs-lookup"><span data-stu-id="52420-173"><span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**WINHTTP\_QUERY\_EXPIRES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-174">Recebe a data e a hora após as quais o recurso deve ser considerado desatualizado.</span><span class="sxs-lookup"><span data-stu-id="52420-174">Receives the date and time after which the resource should be considered outdated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-175"><span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**CONSULTA WINHTTP \_ \_ ENCAMINHADA**</span><span class="sxs-lookup"><span data-stu-id="52420-175"><span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**WINHTTP\_QUERY\_FORWARDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-176">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="52420-176">Obsolete.</span></span> <span data-ttu-id="52420-177">Mantido para compatibilidade de aplicativo herdado.</span><span class="sxs-lookup"><span data-stu-id="52420-177">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-178"><span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**CONSULTA WINHTTP \_ \_ DE**</span><span class="sxs-lookup"><span data-stu-id="52420-178"><span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**WINHTTP\_QUERY\_FROM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-179">Recupera o endereço de email para o usuário que controla o agente de [*usuário solicitante*](glossary.md) se o header From for dado.</span><span class="sxs-lookup"><span data-stu-id="52420-179">Retrieves the e-mail address for the user who controls the requesting [*user agent*](glossary.md) if the From header is given.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-180"><span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**HOST DE CONSULTA WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="52420-180"><span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**WINHTTP\_QUERY\_HOST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-181">Recupera o host da Internet e o número da porta do recurso que está sendo solicitado.</span><span class="sxs-lookup"><span data-stu-id="52420-181">Retrieves the Internet host and port number of the resource being requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-182"><span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**WINHTTP \_ QUERY \_ IF \_ MATCH**</span><span class="sxs-lookup"><span data-stu-id="52420-182"><span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**WINHTTP\_QUERY\_IF\_MATCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-183">Recupera o conteúdo do campo If-Match de solicitação.</span><span class="sxs-lookup"><span data-stu-id="52420-183">Retrieves the contents of the If-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-184"><span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**CONSULTA WINHTTP \_ SE \_ MODIFICADA DESDE \_ \_ ENTÃO**</span><span class="sxs-lookup"><span data-stu-id="52420-184"><span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**WINHTTP\_QUERY\_IF\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-185">Recupera o conteúdo do header If-Modified-Since.</span><span class="sxs-lookup"><span data-stu-id="52420-185">Retrieves the contents of the If-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-186"><span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**CONSULTA WINHTTP \_ \_ SE NENHUM \_ \_ CORRESPONDER**</span><span class="sxs-lookup"><span data-stu-id="52420-186"><span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**WINHTTP\_QUERY\_IF\_NONE\_MATCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-187">Recupera o conteúdo do campo de header de solicitação If-None-Match.</span><span class="sxs-lookup"><span data-stu-id="52420-187">Retrieves the contents of the If-None-Match request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-188"><span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**CONSULTA WINHTTP \_ SE \_ \_ INTERVALO**</span><span class="sxs-lookup"><span data-stu-id="52420-188"><span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**WINHTTP\_QUERY\_IF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-189">Recupera o conteúdo do campo If-Range de solicitação.</span><span class="sxs-lookup"><span data-stu-id="52420-189">Retrieves the contents of the If-Range request-header field.</span></span> <span data-ttu-id="52420-190">Esse header permite que o aplicativo cliente verifique se a entidade relacionada a uma cópia parcial da entidade no cache do aplicativo cliente não foi atualizada.</span><span class="sxs-lookup"><span data-stu-id="52420-190">This header allows the client application to check if the entity related to a partial copy of the entity in the client application's cache has not been updated.</span></span> <span data-ttu-id="52420-191">Se a entidade não tiver sido atualizada, envie as partes que o aplicativo cliente está ausente.</span><span class="sxs-lookup"><span data-stu-id="52420-191">If the entity has not been updated, send the parts that the client application is missing.</span></span> <span data-ttu-id="52420-192">Se a entidade tiver sido atualizada, envie toda a entidade atualizada.</span><span class="sxs-lookup"><span data-stu-id="52420-192">If the entity has been updated, send the entire updated entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-193"><span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**CONSULTA WINHTTP \_ \_ SE NÃO FOR \_ MODIFICADA DESDE \_ ENTÃO**</span><span class="sxs-lookup"><span data-stu-id="52420-193"><span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**WINHTTP\_QUERY\_IF\_UNMODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-194">Recupera o conteúdo do campo de header de solicitação If-Unmodified-Since.</span><span class="sxs-lookup"><span data-stu-id="52420-194">Retrieves the contents of the If-Unmodified-Since request-header field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-195"><span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**LINK DE CONSULTA \_ WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-195"><span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**WINHTTP\_QUERY\_LINK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-196">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="52420-196">Obsolete.</span></span> <span data-ttu-id="52420-197">Mantido para compatibilidade de aplicativo herdado.</span><span class="sxs-lookup"><span data-stu-id="52420-197">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-198"><span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**CONSULTA WINHTTP \_ ÚLTIMA \_ \_ MODIFICAÇÃO**</span><span class="sxs-lookup"><span data-stu-id="52420-198"><span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**WINHTTP\_QUERY\_LAST\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-199">Recebe a data e a hora em que o recurso foi modificado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="52420-199">Receives the date and time at which the resource was last modified.</span></span> <span data-ttu-id="52420-200">A data e a hora são determinadas pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="52420-200">The date and time are determined by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-201"><span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**\_local da consulta WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-201"><span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**WINHTTP\_QUERY\_LOCATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-202">Recupera o URI absoluto usado em um cabeçalho de resposta de local.</span><span class="sxs-lookup"><span data-stu-id="52420-202">Retrieves the absolute URI used in a Location response-header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-203"><span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**consulta de WINHTTP \_ \_ Max**</span><span class="sxs-lookup"><span data-stu-id="52420-203"><span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**WINHTTP\_QUERY\_MAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-204">Indica o valor máximo de um \_ valor de consulta WinHTTP \_ \* .</span><span class="sxs-lookup"><span data-stu-id="52420-204">Indicates the maximum value of a WINHTTP\_QUERY\_\* value.</span></span> <span data-ttu-id="52420-205">Não é um sinalizador de consulta.</span><span class="sxs-lookup"><span data-stu-id="52420-205">Not a query flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-206"><span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**\_ \_ encaminhamentos máximos de consulta WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-206"><span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**WINHTTP\_QUERY\_MAX\_FORWARDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-207">Recupera o número de proxies ou gateways que podem encaminhar a solicitação para o próximo servidor de entrada.</span><span class="sxs-lookup"><span data-stu-id="52420-207">Retrieves the number of proxies or gateways that can forward the request to the next inbound server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-208"><span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**\_ID da \_ mensagem de consulta WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-208"><span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**WINHTTP\_QUERY\_MESSAGE\_ID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-209">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="52420-209">Not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-210"><span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**\_versão de \_ MIME da consulta WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-210"><span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**WINHTTP\_QUERY\_MIME\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-211">Recebe a versão do protocolo MIME (Multipurpose Internet Mail Extensions) usado para construir a mensagem.</span><span class="sxs-lookup"><span data-stu-id="52420-211">Receives the version of the Multipurpose Internet Mail Extensions (MIME) protocol that was used to construct the message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-212"><span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**\_URI de \_ orig de consulta de WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-212"><span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**WINHTTP\_QUERY\_ORIG\_URI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-213">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="52420-213">Obsolete.</span></span> <span data-ttu-id="52420-214">Mantido para compatibilidade de aplicativos herdados.</span><span class="sxs-lookup"><span data-stu-id="52420-214">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-215"><span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**\_pragma da consulta WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-215"><span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**WINHTTP\_QUERY\_PRAGMA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-216">Recebe as diretivas específicas de implementação que podem se aplicar a qualquer destinatário ao longo da cadeia de solicitação/resposta.</span><span class="sxs-lookup"><span data-stu-id="52420-216">Receives the implementation-specific directives that might apply to any recipient along the request/response chain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-217"><span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**\_autenticação de \_ proxy de consulta WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-217"><span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**WINHTTP\_QUERY\_PROXY\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-218">Recupera o esquema de autenticação e o realm retornado pelo proxy.</span><span class="sxs-lookup"><span data-stu-id="52420-218">Retrieves the authentication scheme and realm returned by the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-219"><span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**\_autorização de \_ proxy de consulta WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-219"><span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**WINHTTP\_QUERY\_PROXY\_AUTHORIZATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-220">Recupera o cabeçalho que é usado para identificar o usuário para um proxy que requer autenticação.</span><span class="sxs-lookup"><span data-stu-id="52420-220">Retrieves the header that is used to identify the user to a proxy that requires authentication.</span></span> <span data-ttu-id="52420-221">Esse cabeçalho só pode ser recuperado antes que a solicitação seja enviada ao servidor.</span><span class="sxs-lookup"><span data-stu-id="52420-221">This header can only be retrieved before the request is sent to the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-222"><span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**\_conexão de \_ proxy de consulta WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-222"><span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**WINHTTP\_QUERY\_PROXY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-223">Recupera o cabeçalho Proxy-Connection.</span><span class="sxs-lookup"><span data-stu-id="52420-223">Retrieves the Proxy-Connection header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-224"><span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**\_ \_ suporte ao proxy de consulta WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-224"><span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**WINHTTP\_QUERY\_PROXY\_SUPPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-225">Recupera o cabeçalho Proxy-Support.</span><span class="sxs-lookup"><span data-stu-id="52420-225">Retrieves the Proxy-Support header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-226"><span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**consulta de WINHTTP \_ \_ pública**</span><span class="sxs-lookup"><span data-stu-id="52420-226"><span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**WINHTTP\_QUERY\_PUBLIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-227">Recebe verbos HTTP disponíveis neste servidor.</span><span class="sxs-lookup"><span data-stu-id="52420-227">Receives HTTP verbs available at this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-228"><span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**\_intervalo de consulta WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-228"><span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**WINHTTP\_QUERY\_RANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-229">Recupera o intervalo de bytes de uma entidade.</span><span class="sxs-lookup"><span data-stu-id="52420-229">Retrieves the byte range of an entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-230"><span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**\_ \_ cabeçalhos brutos de consulta WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-230"><span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**WINHTTP\_QUERY\_RAW\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-231">Recebe todos os cabeçalhos retornados pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="52420-231">Receives all the headers returned by the server.</span></span> <span data-ttu-id="52420-232">Cada cabeçalho é encerrado por " \\ 0".</span><span class="sxs-lookup"><span data-stu-id="52420-232">Each header is terminated by "\\0".</span></span> <span data-ttu-id="52420-233">Um " \\ 0" adicional encerra a lista de cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="52420-233">An additional "\\0" terminates the list of headers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-234"><span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**\_CRLF de \_ cabeçalhos brutos de consulta \_ WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-234"><span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**WINHTTP\_QUERY\_RAW\_HEADERS\_CRLF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-235">Recebe todos os cabeçalhos retornados pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="52420-235">Receives all the headers returned by the server.</span></span> <span data-ttu-id="52420-236">Cada cabeçalho é separado por uma sequência de CR/LF (retorno de carro/alimentação de linha).</span><span class="sxs-lookup"><span data-stu-id="52420-236">Each header is separated by a carriage return/line feed (CR/LF) sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-237"><span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**\_referenciador de consulta de WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-237"><span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**WINHTTP\_QUERY\_REFERER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-238">Recebe o URI do recurso em que o URI solicitado foi obtido.</span><span class="sxs-lookup"><span data-stu-id="52420-238">Receives the URI of the resource where the requested URI was obtained.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-239"><span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**\_atualização de consulta WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-239"><span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**WINHTTP\_QUERY\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-240">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="52420-240">Obsolete.</span></span> <span data-ttu-id="52420-241">Mantido para compatibilidade de aplicativos herdados.</span><span class="sxs-lookup"><span data-stu-id="52420-241">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-242"><span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**\_método de \_ solicitação de consulta WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-242"><span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**WINHTTP\_QUERY\_REQUEST\_METHOD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-243">Recebe o verbo HTTP que está sendo usado na solicitação, normalmente GET ou POST.</span><span class="sxs-lookup"><span data-stu-id="52420-243">Receives the HTTP verb that is being used in the request, typically GET or POST.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-244"><span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**\_repetir consulta de WinHTTP \_ \_ após**</span><span class="sxs-lookup"><span data-stu-id="52420-244"><span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**WINHTTP\_QUERY\_RETRY\_AFTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-245">Recupera a quantidade de tempo que o serviço deve estar indisponível.</span><span class="sxs-lookup"><span data-stu-id="52420-245">Retrieves the amount of time the service is expected to be unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-246"><span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**\_servidor de consulta WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-246"><span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**WINHTTP\_QUERY\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-247">Recupera informações sobre o software usado pelo servidor de origem para lidar com a solicitação.</span><span class="sxs-lookup"><span data-stu-id="52420-247">Retrieves information about the software used by the originating server to handle the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-248"><span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**\_cookie do \_ conjunto de consultas do WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-248"><span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**WINHTTP\_QUERY\_SET\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-249">Recebe o valor do conjunto de cookies para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="52420-249">Receives the value of the cookie set for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-250"><span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**\_código de \_ status de consulta WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-250"><span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**WINHTTP\_QUERY\_STATUS\_CODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-251">Recebe o código de status retornado pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="52420-251">Receives the status code returned by the server.</span></span> <span data-ttu-id="52420-252">Para obter uma lista de valores possíveis, consulte [**códigos de status http**](http-status-codes.md).</span><span class="sxs-lookup"><span data-stu-id="52420-252">For a list of possible values, see [**HTTP Status Codes**](http-status-codes.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-253"><span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**\_texto de \_ status da consulta WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-253"><span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**WINHTTP\_QUERY\_STATUS\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-254">Recebe texto adicional retornado pelo servidor na linha de resposta.</span><span class="sxs-lookup"><span data-stu-id="52420-254">Receives additional text returned by the server on the response line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-255"><span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**\_título da consulta WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-255"><span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**WINHTTP\_QUERY\_TITLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-256">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="52420-256">Obsolete.</span></span> <span data-ttu-id="52420-257">Mantido para compatibilidade de aplicativos herdados.</span><span class="sxs-lookup"><span data-stu-id="52420-257">Maintained for legacy application compatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-258"><span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**\_codificação de \_ transferência de consulta WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-258"><span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**WINHTTP\_QUERY\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-259">Recupera o tipo de transformação que foi aplicado ao corpo da mensagem para que possa ser transferido com segurança entre o remetente e o destinatário.</span><span class="sxs-lookup"><span data-stu-id="52420-259">Retrieves the type of transformation that has been applied to the message body so it can be safely transferred between the sender and recipient.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-260"><span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**\_consulta WinHTTP \_ , a menos que seja \_ modificado \_ desde**</span><span class="sxs-lookup"><span data-stu-id="52420-260"><span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**WINHTTP\_QUERY\_UNLESS\_MODIFIED\_SINCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-261">Recupera o cabeçalho, a menos que-Modified-Since.</span><span class="sxs-lookup"><span data-stu-id="52420-261">Retrieves the Unless-Modified-Since header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-262"><span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**\_atualização de consulta de WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-262"><span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**WINHTTP\_QUERY\_UPGRADE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-263">Recupera os protocolos de comunicação adicionais que são suportados pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="52420-263">Retrieves the additional communication protocols that are supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-264"><span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**\_URI de consulta WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-264"><span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**WINHTTP\_QUERY\_URI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-265">Recebe parte ou todo o URI pelo qual o recurso de solicitação-URI pode ser identificado.</span><span class="sxs-lookup"><span data-stu-id="52420-265">Receives some or all of the URI by which the Request-URI resource can be identified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-266"><span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**\_agente do \_ usuário de consulta WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-266"><span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**WINHTTP\_QUERY\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-267">Recupera informações sobre o agente do usuário que fez a solicitação.</span><span class="sxs-lookup"><span data-stu-id="52420-267">Retrieves information about the user agent that made the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-268"><span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**a \_ consulta WinHTTP \_ varia**</span><span class="sxs-lookup"><span data-stu-id="52420-268"><span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**WINHTTP\_QUERY\_VARY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-269">Recupera o cabeçalho que indica que a entidade foi selecionada a partir de várias representações disponíveis da resposta usando a negociação controlada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="52420-269">Retrieves the header that indicates that the entity was selected from a number of available representations of the response using server-driven negotiation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-270"><span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**\_versão de consulta WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-270"><span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**WINHTTP\_QUERY\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-271">Recupera a versão HTTP que está presente na linha de status.</span><span class="sxs-lookup"><span data-stu-id="52420-271">Retrieves the HTTP version that is present in the status line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-272"><span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**\_consulta WinHTTP \_ via**</span><span class="sxs-lookup"><span data-stu-id="52420-272"><span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**WINHTTP\_QUERY\_VIA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-273">Recupera os protocolos intermediários e os destinatários entre o agente do usuário e o servidor em solicitações e entre o servidor de origem e o cliente em respostas.</span><span class="sxs-lookup"><span data-stu-id="52420-273">Retrieves the intermediate protocols and recipients between the user agent and the server on requests, and between the origin server and the client on responses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-274"><span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**\_aviso de consulta WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-274"><span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**WINHTTP\_QUERY\_WARNING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-275">Recupera informações adicionais sobre o status de uma resposta que pode não ser refletida pelo código de status de resposta.</span><span class="sxs-lookup"><span data-stu-id="52420-275">Retrieves additional information about the status of a response that might not be reflected by the response status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-276"><span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**\_consulta WinHTTP \_ www \_ Authenticate**</span><span class="sxs-lookup"><span data-stu-id="52420-276"><span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**WINHTTP\_QUERY\_WWW\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-277">Recupera o esquema de autenticação e o realm retornado pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="52420-277">Retrieves the authentication scheme and realm returned by the server.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="52420-278">Os sinalizadores modificadores são usados em conjunto com um sinalizador de atributo para modificar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="52420-278">The modifier flags are used in conjunction with an attribute flag to modify the request.</span></span> <span data-ttu-id="52420-279">Os sinalizadores de modificador modificam o formato dos dados retornados ou indicam onde a função [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) deve pesquisar as informações.</span><span class="sxs-lookup"><span data-stu-id="52420-279">Modifier flags either modify the format of the data returned or indicate where the [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) function should search for the information.</span></span>

<dl> <dt>

<span data-ttu-id="52420-280"><span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**\_número do \_ sinalizador de consulta WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-280"><span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**WINHTTP\_QUERY\_FLAG\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-281">Retorna os dados como um número de 32 bits para cabeçalhos cujo valor é um número, como o código de status.</span><span class="sxs-lookup"><span data-stu-id="52420-281">Returns the data as a 32-bit number for headers whose value is a number, such as the status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-282"><span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**\_cabeçalhos de \_ solicitação de sinalizador de consulta WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="52420-282"><span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**WINHTTP\_QUERY\_FLAG\_REQUEST\_HEADERS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-283">Consulta somente cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="52420-283">Queries request headers only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52420-284"><span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**sinalizador de consulta de WINHTTP \_ \_ \_ SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="52420-284"><span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**WINHTTP\_QUERY\_FLAG\_SYSTEMTIME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52420-285">Retorna o valor do cabeçalho como uma estrutura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) , que não exige que o aplicativo analise os dados.</span><span class="sxs-lookup"><span data-stu-id="52420-285">Returns the header value as a [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure, which does not require the application to parse the data.</span></span> <span data-ttu-id="52420-286">Use para cabeçalhos cujo valor é uma cadeia de caracteres de data/hora, como "hora da última modificação".</span><span class="sxs-lookup"><span data-stu-id="52420-286">Use for headers whose value is a date/time string, such as "Last-Modified-Time".</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="52420-287"><span id="WINHTTP_QUERY_FLAG_TRAILERS"></span><span id="winhttp_query_flag_trailers"></span>**\_marcadores de \_ sinalizador de consulta WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="52420-287"><span id="WINHTTP_QUERY_FLAG_TRAILERS"></span><span id="winhttp_query_flag_trailers"></span>**WINHTTP\_QUERY\_FLAG\_TRAILERS**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="52420-288">Consulta os trailers de resposta.</span><span class="sxs-lookup"><span data-stu-id="52420-288">Queries response trailers.</span></span> <span data-ttu-id="52420-289">Antes de consultar os trailers de resposta, você deve chamar [**WinHttpReadData**](/windows/win32/api/Winhttp/nf-winhttp-winhttpreaddata) até que ele retorne 0 bytes lidos.</span><span class="sxs-lookup"><span data-stu-id="52420-289">Prior to querying response trailers, you must call [**WinHttpReadData**](/windows/win32/api/Winhttp/nf-winhttp-winhttpreaddata) until it returns 0 bytes read.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="52420-290"><span id="WINHTTP_QUERY_FLAG_WIRE_ENCODING"></span><span id="winhttp_query_flag_wire_encoding"></span>**\_codificação de \_ transmissão de sinalizador de consulta WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="52420-290"><span id="WINHTTP_QUERY_FLAG_WIRE_ENCODING"></span><span id="winhttp_query_flag_wire_encoding"></span>**WINHTTP\_QUERY\_FLAG\_WIRE\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="52420-291">Por padrão, o [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) executa uma conversão de Unicode antes de retornar o cabeçalho que foi consultado.</span><span class="sxs-lookup"><span data-stu-id="52420-291">By default, [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) performs a Unicode conversion before returning the header that was queried.</span></span> <span data-ttu-id="52420-292">Se esse sinalizador for definido, o WinHttp retornará o cabeçalho ao chamador sem executar essa conversão.</span><span class="sxs-lookup"><span data-stu-id="52420-292">If this flag is set, WinHttp returns the header to the caller without performing this conversion.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="52420-293">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52420-293">Requirements</span></span>

| <span data-ttu-id="52420-294">Requisito</span><span class="sxs-lookup"><span data-stu-id="52420-294">Requirement</span></span> | <span data-ttu-id="52420-295">Valor</span><span class="sxs-lookup"><span data-stu-id="52420-295">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="52420-296">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52420-296">Minimum supported client</span></span> | <span data-ttu-id="52420-297">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="52420-297">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span>      |
| <span data-ttu-id="52420-298">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52420-298">Minimum supported server</span></span> | <span data-ttu-id="52420-299">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="52420-299">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span>   |
| <span data-ttu-id="52420-300">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="52420-300">Header</span></span>                   | <dl> <span data-ttu-id="52420-301"><dt>WinHTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="52420-301"><dt>Winhttp.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="52420-302">Confira também</span><span class="sxs-lookup"><span data-stu-id="52420-302">See also</span></span>

* [<span data-ttu-id="52420-303">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="52420-303">WinHTTP Versions</span></span>](winhttp-versions.md)
