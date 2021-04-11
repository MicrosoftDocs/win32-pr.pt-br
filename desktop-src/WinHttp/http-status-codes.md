---
description: Essas constantes e valores correspondentes indicam códigos de status HTTP retornados por servidores na Internet.
ms.assetid: 3de6a35d-41e9-4fce-ab92-e970c7c07e55
title: Códigos de status HTTP (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcf4103cdc382bd5ab0d582fe99212083e2780ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170198"
---
# <a name="http-status-codes-winhttph"></a><span data-ttu-id="e8514-103">Códigos de status HTTP (WinHTTP. h)</span><span class="sxs-lookup"><span data-stu-id="e8514-103">HTTP Status Codes (Winhttp.h)</span></span>

<span data-ttu-id="e8514-104">Essas constantes e valores correspondentes indicam códigos de status HTTP retornados por servidores na Internet.</span><span class="sxs-lookup"><span data-stu-id="e8514-104">These constants and corresponding values indicate HTTP status codes returned by servers on the Internet.</span></span>

<dl> <dt>

<span data-ttu-id="e8514-105"><span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**STATUS do HTTP \_ \_ continuar**</span><span class="sxs-lookup"><span data-stu-id="e8514-105"><span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-106">100</span><span class="sxs-lookup"><span data-stu-id="e8514-106">100</span></span>
</dt> <dt>



<span data-ttu-id="e8514-107">A solicitação pode ser continuada.</span><span class="sxs-lookup"><span data-stu-id="e8514-107">The request can be continued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-108"><span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**\_protocolos de \_ comutação de status http \_**</span><span class="sxs-lookup"><span data-stu-id="e8514-108"><span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**HTTP\_STATUS\_SWITCH\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-109">101</span><span class="sxs-lookup"><span data-stu-id="e8514-109">101</span></span>
</dt> <dt>



<span data-ttu-id="e8514-110">O servidor alternou protocolos em um cabeçalho de atualização.</span><span class="sxs-lookup"><span data-stu-id="e8514-110">The server has switched protocols in an upgrade header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-111"><span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**STATUS do HTTP \_ \_ OK**</span><span class="sxs-lookup"><span data-stu-id="e8514-111"><span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**HTTP\_STATUS\_OK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-112">200</span><span class="sxs-lookup"><span data-stu-id="e8514-112">200</span></span>
</dt> <dt>



<span data-ttu-id="e8514-113">A solicitação foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="e8514-113">The request completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-114"><span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**STATUS do HTTP \_ \_ criado**</span><span class="sxs-lookup"><span data-stu-id="e8514-114"><span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**HTTP\_STATUS\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-115">201</span><span class="sxs-lookup"><span data-stu-id="e8514-115">201</span></span>
</dt> <dt>



<span data-ttu-id="e8514-116">A solicitação foi atendida e resultou na criação de um novo recurso.</span><span class="sxs-lookup"><span data-stu-id="e8514-116">The request has been fulfilled and resulted in the creation of a new resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-117"><span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**\_status http \_ aceito**</span><span class="sxs-lookup"><span data-stu-id="e8514-117"><span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**HTTP\_STATUS\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-118">202</span><span class="sxs-lookup"><span data-stu-id="e8514-118">202</span></span>
</dt> <dt>



<span data-ttu-id="e8514-119">A solicitação foi aceita para processamento, mas o processamento não foi concluído.</span><span class="sxs-lookup"><span data-stu-id="e8514-119">The request has been accepted for processing, but the processing has not been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-120"><span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**STATUS do HTTP \_ \_ parcial**</span><span class="sxs-lookup"><span data-stu-id="e8514-120"><span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**HTTP\_STATUS\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-121">203</span><span class="sxs-lookup"><span data-stu-id="e8514-121">203</span></span>
</dt> <dt>



<span data-ttu-id="e8514-122">As informações meta retornadas no cabeçalho da entidade não são o conjunto definitivo disponível do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="e8514-122">The returned meta information in the entity-header is not the definitive set available from the originating server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-123"><span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**STATUS do HTTP \_ \_ sem \_ conteúdo**</span><span class="sxs-lookup"><span data-stu-id="e8514-123"><span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**HTTP\_STATUS\_NO\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-124">204</span><span class="sxs-lookup"><span data-stu-id="e8514-124">204</span></span>
</dt> <dt>



<span data-ttu-id="e8514-125">O servidor atendeu à solicitação, mas não há nenhuma informação nova a ser enviada de volta.</span><span class="sxs-lookup"><span data-stu-id="e8514-125">The server has fulfilled the request, but there is no new information to send back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-126"><span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**\_conteúdo de \_ redefinição de status http \_**</span><span class="sxs-lookup"><span data-stu-id="e8514-126"><span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**HTTP\_STATUS\_RESET\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-127">205</span><span class="sxs-lookup"><span data-stu-id="e8514-127">205</span></span>
</dt> <dt>



<span data-ttu-id="e8514-128">A solicitação foi concluída e o programa cliente deve redefinir a exibição de documento que fez com que a solicitação fosse enviada para permitir que o usuário inicie facilmente outra ação de entrada.</span><span class="sxs-lookup"><span data-stu-id="e8514-128">The request has been completed, and the client program should reset the document view that caused the request to be sent to allow the user to easily initiate another input action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-129"><span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**\_ \_ conteúdo parcial do status http \_**</span><span class="sxs-lookup"><span data-stu-id="e8514-129"><span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**HTTP\_STATUS\_PARTIAL\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-130">206</span><span class="sxs-lookup"><span data-stu-id="e8514-130">206</span></span>
</dt> <dt>



<span data-ttu-id="e8514-131">O servidor atendeu à solicitação GET parcial para o recurso.</span><span class="sxs-lookup"><span data-stu-id="e8514-131">The server has fulfilled the partial GET request for the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-132"><span id="HTTP_STATUS_WEBDAV_MULTI_STATUS"></span><span id="http_status_webdav_multi_status"></span>**\_status http \_ \_ vários \_ status do WebDAV**</span><span class="sxs-lookup"><span data-stu-id="e8514-132"><span id="HTTP_STATUS_WEBDAV_MULTI_STATUS"></span><span id="http_status_webdav_multi_status"></span>**HTTP\_STATUS\_WEBDAV\_MULTI\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-133">207</span><span class="sxs-lookup"><span data-stu-id="e8514-133">207</span></span>
</dt> <dt>



<span data-ttu-id="e8514-134">Durante uma World Wide Web operação de criação e controle de versão distribuída (WebDAV), isso indica vários códigos de status para uma única resposta.</span><span class="sxs-lookup"><span data-stu-id="e8514-134">During a World Wide Web Distributed Authoring and Versioning (WebDAV) operation, this indicates multiple status codes for a single response.</span></span> <span data-ttu-id="e8514-135">O corpo da resposta contém linguagem XML (XML) que descreve os códigos de status.</span><span class="sxs-lookup"><span data-stu-id="e8514-135">The response body contains Extensible Markup Language (XML) that describes the status codes.</span></span> <span data-ttu-id="e8514-136">Para obter mais informações, consulte [extensões http para criação distribuída](../webdav/webdav-portal.md).</span><span class="sxs-lookup"><span data-stu-id="e8514-136">For more information, see [HTTP Extensions for Distributed Authoring](../webdav/webdav-portal.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-137"><span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**\_status http \_ ambíguo**</span><span class="sxs-lookup"><span data-stu-id="e8514-137"><span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**HTTP\_STATUS\_AMBIGUOUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-138">300</span><span class="sxs-lookup"><span data-stu-id="e8514-138">300</span></span>
</dt> <dt>



<span data-ttu-id="e8514-139">O recurso solicitado está disponível em um ou mais locais.</span><span class="sxs-lookup"><span data-stu-id="e8514-139">The requested resource is available at one or more locations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-140"><span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**STATUS do HTTP \_ \_ movido**</span><span class="sxs-lookup"><span data-stu-id="e8514-140"><span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**HTTP\_STATUS\_MOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-141">301</span><span class="sxs-lookup"><span data-stu-id="e8514-141">301</span></span>
</dt> <dt>



<span data-ttu-id="e8514-142">O recurso solicitado foi atribuído a um novo Uniform Resource Identifier permanente (URI) e todas as referências futuras a esse recurso devem ser feitas usando um dos URIs retornados.</span><span class="sxs-lookup"><span data-stu-id="e8514-142">The requested resource has been assigned to a new permanent Uniform Resource Identifier (URI), and any future references to this resource should be done using one of the returned URIs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-143"><span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**\_redirecionamento de status http \_**</span><span class="sxs-lookup"><span data-stu-id="e8514-143"><span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**HTTP\_STATUS\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-144">302</span><span class="sxs-lookup"><span data-stu-id="e8514-144">302</span></span>
</dt> <dt>



<span data-ttu-id="e8514-145">O recurso solicitado reside temporariamente em um URI diferente.</span><span class="sxs-lookup"><span data-stu-id="e8514-145">The requested resource resides temporarily under a different URI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-146"><span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**\_método de \_ redirecionamento de status http \_**</span><span class="sxs-lookup"><span data-stu-id="e8514-146"><span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**HTTP\_STATUS\_REDIRECT\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-147">303</span><span class="sxs-lookup"><span data-stu-id="e8514-147">303</span></span>
</dt> <dt>



<span data-ttu-id="e8514-148">A resposta à solicitação pode ser encontrada em um URI diferente e deve ser recuperada usando um [*verbo http*](glossary.md) Get nesse recurso.</span><span class="sxs-lookup"><span data-stu-id="e8514-148">The response to the request can be found under a different URI and should be retrieved using a GET [*HTTP verb*](glossary.md) on that resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-149"><span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**\_status http \_ não \_ modificado**</span><span class="sxs-lookup"><span data-stu-id="e8514-149"><span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**HTTP\_STATUS\_NOT\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-150">304</span><span class="sxs-lookup"><span data-stu-id="e8514-150">304</span></span>
</dt> <dt>



<span data-ttu-id="e8514-151">O recurso solicitado não foi modificado.</span><span class="sxs-lookup"><span data-stu-id="e8514-151">The requested resource has not been modified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-152"><span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**\_proxy de \_ uso de status http \_**</span><span class="sxs-lookup"><span data-stu-id="e8514-152"><span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**HTTP\_STATUS\_USE\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-153">305</span><span class="sxs-lookup"><span data-stu-id="e8514-153">305</span></span>
</dt> <dt>



<span data-ttu-id="e8514-154">O recurso solicitado deve ser acessado por meio do proxy fornecido pelo campo local.</span><span class="sxs-lookup"><span data-stu-id="e8514-154">The requested resource must be accessed through the proxy given by the location field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-155"><span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**\_verbo de \_ redirecionamento de status http \_ Keep \_**</span><span class="sxs-lookup"><span data-stu-id="e8514-155"><span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**HTTP\_STATUS\_REDIRECT\_KEEP\_VERB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-156">307</span><span class="sxs-lookup"><span data-stu-id="e8514-156">307</span></span>
</dt> <dt>



<span data-ttu-id="e8514-157">A solicitação redirecionada mantém o mesmo [*verbo http*](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="e8514-157">The redirected request keeps the same [*HTTP verb*](glossary.md).</span></span> <span data-ttu-id="e8514-158">Comportamento de HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="e8514-158">HTTP/1.1 behavior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-159"><span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**\_ \_ solicitação inadequada de status http \_**</span><span class="sxs-lookup"><span data-stu-id="e8514-159"><span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**HTTP\_STATUS\_BAD\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-160">400</span><span class="sxs-lookup"><span data-stu-id="e8514-160">400</span></span>
</dt> <dt>



<span data-ttu-id="e8514-161">A solicitação não pôde ser processada pelo servidor devido à sintaxe inválida.</span><span class="sxs-lookup"><span data-stu-id="e8514-161">The request could not be processed by the server due to invalid syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-162"><span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**STATUS do HTTP \_ \_ negado**</span><span class="sxs-lookup"><span data-stu-id="e8514-162"><span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**HTTP\_STATUS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-163">401</span><span class="sxs-lookup"><span data-stu-id="e8514-163">401</span></span>
</dt> <dt>



<span data-ttu-id="e8514-164">O recurso solicitado requer a autenticação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e8514-164">The requested resource requires user authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-165"><span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**Req. de \_ pagamento de status http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e8514-165"><span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**HTTP\_STATUS\_PAYMENT\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-166">402</span><span class="sxs-lookup"><span data-stu-id="e8514-166">402</span></span>
</dt> <dt>



<span data-ttu-id="e8514-167">Não implementado no protocolo HTTP.</span><span class="sxs-lookup"><span data-stu-id="e8514-167">Not implemented in the HTTP protocol.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-168"><span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**STATUS de HTTP \_ \_ proibido**</span><span class="sxs-lookup"><span data-stu-id="e8514-168"><span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**HTTP\_STATUS\_FORBIDDEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-169">403</span><span class="sxs-lookup"><span data-stu-id="e8514-169">403</span></span>
</dt> <dt>



<span data-ttu-id="e8514-170">O servidor entendeu a solicitação, mas não pode atendê-la.</span><span class="sxs-lookup"><span data-stu-id="e8514-170">The server understood the request, but cannot fulfill it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-171"><span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**\_status http \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="e8514-171"><span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**HTTP\_STATUS\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-172">404</span><span class="sxs-lookup"><span data-stu-id="e8514-172">404</span></span>
</dt> <dt>



<span data-ttu-id="e8514-173">O servidor não encontrou nada que corresponda ao URI solicitado.</span><span class="sxs-lookup"><span data-stu-id="e8514-173">The server has not found anything that matches the requested URI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-174"><span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**\_ \_ método inadequado de status http \_**</span><span class="sxs-lookup"><span data-stu-id="e8514-174"><span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**HTTP\_STATUS\_BAD\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-175">405</span><span class="sxs-lookup"><span data-stu-id="e8514-175">405</span></span>
</dt> <dt>



<span data-ttu-id="e8514-176">O [*verbo http*](glossary.md) usado não é permitido.</span><span class="sxs-lookup"><span data-stu-id="e8514-176">The [*HTTP verb*](glossary.md) used is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-177"><span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**\_status http \_ nenhum \_ aceitável**</span><span class="sxs-lookup"><span data-stu-id="e8514-177"><span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**HTTP\_STATUS\_NONE\_ACCEPTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-178">406</span><span class="sxs-lookup"><span data-stu-id="e8514-178">406</span></span>
</dt> <dt>



<span data-ttu-id="e8514-179">Nenhuma resposta aceitável para o cliente foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="e8514-179">No responses acceptable to the client were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-180"><span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**Req. de autenticação de proxy de \_ status http \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e8514-180"><span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**HTTP\_STATUS\_PROXY\_AUTH\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-181">407</span><span class="sxs-lookup"><span data-stu-id="e8514-181">407</span></span>
</dt> <dt>



<span data-ttu-id="e8514-182">Autenticação de proxy necessária.</span><span class="sxs-lookup"><span data-stu-id="e8514-182">Proxy authentication required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-183"><span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**\_ \_ tempo limite de solicitação de status http \_**</span><span class="sxs-lookup"><span data-stu-id="e8514-183"><span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**HTTP\_STATUS\_REQUEST\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-184">408</span><span class="sxs-lookup"><span data-stu-id="e8514-184">408</span></span>
</dt> <dt>



<span data-ttu-id="e8514-185">O servidor atingiu o tempo limite ao aguardar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="e8514-185">The server timed out waiting for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-186"><span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**\_conflito de status http \_**</span><span class="sxs-lookup"><span data-stu-id="e8514-186"><span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**HTTP\_STATUS\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-187">409</span><span class="sxs-lookup"><span data-stu-id="e8514-187">409</span></span>
</dt> <dt>



<span data-ttu-id="e8514-188">A solicitação não pôde ser concluída devido a um conflito com o estado atual do recurso.</span><span class="sxs-lookup"><span data-stu-id="e8514-188">The request could not be completed due to a conflict with the current state of the resource.</span></span> <span data-ttu-id="e8514-189">O usuário deve enviar novamente com mais informações.</span><span class="sxs-lookup"><span data-stu-id="e8514-189">The user should resubmit with more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-190"><span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**\_status http \_ ausente**</span><span class="sxs-lookup"><span data-stu-id="e8514-190"><span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**HTTP\_STATUS\_GONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-191">410</span><span class="sxs-lookup"><span data-stu-id="e8514-191">410</span></span>
</dt> <dt>



<span data-ttu-id="e8514-192">O recurso solicitado não está mais disponível no servidor e nenhum endereço de encaminhamento é conhecido.</span><span class="sxs-lookup"><span data-stu-id="e8514-192">The requested resource is no longer available at the server, and no forwarding address is known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-193"><span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**\_comprimento de status http \_ \_ necessário**</span><span class="sxs-lookup"><span data-stu-id="e8514-193"><span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**HTTP\_STATUS\_LENGTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-194">411</span><span class="sxs-lookup"><span data-stu-id="e8514-194">411</span></span>
</dt> <dt>



<span data-ttu-id="e8514-195">O servidor não pode aceitar a solicitação sem um comprimento de conteúdo definido.</span><span class="sxs-lookup"><span data-stu-id="e8514-195">The server cannot accept the request without a defined content length.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-196"><span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**\_falha de \_ PRECOND de status http \_**</span><span class="sxs-lookup"><span data-stu-id="e8514-196"><span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**HTTP\_STATUS\_PRECOND\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-197">412</span><span class="sxs-lookup"><span data-stu-id="e8514-197">412</span></span>
</dt> <dt>



<span data-ttu-id="e8514-198">A pré-condição fornecida em um ou mais dos campos de cabeçalho da solicitação foi avaliada como falsa quando foi testada no servidor.</span><span class="sxs-lookup"><span data-stu-id="e8514-198">The precondition given in one or more of the request header fields evaluated to false when it was tested on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-199"><span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**\_solicitação de status http \_ \_ muito \_ grande**</span><span class="sxs-lookup"><span data-stu-id="e8514-199"><span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**HTTP\_STATUS\_REQUEST\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-200">413</span><span class="sxs-lookup"><span data-stu-id="e8514-200">413</span></span>
</dt> <dt>



<span data-ttu-id="e8514-201">O servidor não pode processar a solicitação porque a entidade de solicitação é maior do que o servidor é capaz de processar.</span><span class="sxs-lookup"><span data-stu-id="e8514-201">The server cannot process the request because the request entity is larger than the server is able to process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-202"><span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**\_URI de status http \_ \_ muito \_ longo**</span><span class="sxs-lookup"><span data-stu-id="e8514-202"><span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**HTTP\_STATUS\_URI\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-203">414</span><span class="sxs-lookup"><span data-stu-id="e8514-203">414</span></span>
</dt> <dt>



<span data-ttu-id="e8514-204">O servidor não pode atender à solicitação porque o URI da solicitação é maior do que o servidor pode interpretar.</span><span class="sxs-lookup"><span data-stu-id="e8514-204">The server cannot service the request because the request URI is longer than the server can interpret.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-205"><span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**\_mídia de status http \_ sem suporte \_**</span><span class="sxs-lookup"><span data-stu-id="e8514-205"><span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**HTTP\_STATUS\_UNSUPPORTED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-206">415</span><span class="sxs-lookup"><span data-stu-id="e8514-206">415</span></span>
</dt> <dt>



<span data-ttu-id="e8514-207">O servidor não pode atender à solicitação porque a entidade da solicitação está em um formato sem suporte pelo recurso solicitado para o método solicitado.</span><span class="sxs-lookup"><span data-stu-id="e8514-207">The server cannot service the request because the entity of the request is in a format not supported by the requested resource for the requested method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-208"><span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**\_ \_ repetição de status http \_ com**</span><span class="sxs-lookup"><span data-stu-id="e8514-208"><span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**HTTP\_STATUS\_RETRY\_WITH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-209">449</span><span class="sxs-lookup"><span data-stu-id="e8514-209">449</span></span>
</dt> <dt>



<span data-ttu-id="e8514-210">A solicitação deve ser repetida após a ação apropriada.</span><span class="sxs-lookup"><span data-stu-id="e8514-210">The request should be retried after doing the appropriate action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-211"><span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**\_ \_ erro do servidor de status http \_**</span><span class="sxs-lookup"><span data-stu-id="e8514-211"><span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**HTTP\_STATUS\_SERVER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-212">500</span><span class="sxs-lookup"><span data-stu-id="e8514-212">500</span></span>
</dt> <dt>



<span data-ttu-id="e8514-213">O servidor encontrou uma condição inesperada que o impediu de atender à solicitação.</span><span class="sxs-lookup"><span data-stu-id="e8514-213">The server encountered an unexpected condition that prevented it from fulfilling the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-214"><span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**\_status http \_ sem \_ suporte**</span><span class="sxs-lookup"><span data-stu-id="e8514-214"><span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**HTTP\_STATUS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-215">501</span><span class="sxs-lookup"><span data-stu-id="e8514-215">501</span></span>
</dt> <dt>



<span data-ttu-id="e8514-216">O servidor não oferece suporte à funcionalidade necessária para atender à solicitação.</span><span class="sxs-lookup"><span data-stu-id="e8514-216">The server does not support the functionality required to fulfill the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-217"><span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**\_ \_ Gateway insatisfatório de status http \_**</span><span class="sxs-lookup"><span data-stu-id="e8514-217"><span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**HTTP\_STATUS\_BAD\_GATEWAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-218">502</span><span class="sxs-lookup"><span data-stu-id="e8514-218">502</span></span>
</dt> <dt>



<span data-ttu-id="e8514-219">O servidor, ao atuar como gateway ou proxy, recebeu uma resposta inválida do servidor upstream acessado na tentativa de atender à solicitação.</span><span class="sxs-lookup"><span data-stu-id="e8514-219">The server, while acting as a gateway or proxy, received an invalid response from the upstream server it accessed in attempting to fulfill the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-220"><span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**serviço de status HTTP não \_ \_ \_ disp.**</span><span class="sxs-lookup"><span data-stu-id="e8514-220"><span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**HTTP\_STATUS\_SERVICE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-221">503</span><span class="sxs-lookup"><span data-stu-id="e8514-221">503</span></span>
</dt> <dt>



<span data-ttu-id="e8514-222">O serviço está temporariamente sobrecarregado.</span><span class="sxs-lookup"><span data-stu-id="e8514-222">The service is temporarily overloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-223"><span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**\_ \_ tempo limite do gateway de status http \_**</span><span class="sxs-lookup"><span data-stu-id="e8514-223"><span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**HTTP\_STATUS\_GATEWAY\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-224">504</span><span class="sxs-lookup"><span data-stu-id="e8514-224">504</span></span>
</dt> <dt>



<span data-ttu-id="e8514-225">A solicitação atingiu o tempo limite ao aguardar um gateway.</span><span class="sxs-lookup"><span data-stu-id="e8514-225">The request was timed out waiting for a gateway.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8514-226"><span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**\_versão de status http \_ \_ não \_ sup**</span><span class="sxs-lookup"><span data-stu-id="e8514-226"><span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**HTTP\_STATUS\_VERSION\_NOT\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8514-227">505</span><span class="sxs-lookup"><span data-stu-id="e8514-227">505</span></span>
</dt> <dt>



<span data-ttu-id="e8514-228">O servidor não oferece suporte à versão do protocolo HTTP que foi usada na mensagem de solicitação.</span><span class="sxs-lookup"><span data-stu-id="e8514-228">The server does not support the HTTP protocol version that was used in the request message.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8514-229">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8514-229">Requirements</span></span>



| <span data-ttu-id="e8514-230">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8514-230">Requirement</span></span> | <span data-ttu-id="e8514-231">Valor</span><span class="sxs-lookup"><span data-stu-id="e8514-231">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e8514-232">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8514-232">Minimum supported client</span></span><br/> | <span data-ttu-id="e8514-233">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="e8514-233">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="e8514-234">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8514-234">Minimum supported server</span></span><br/> | <span data-ttu-id="e8514-235">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="e8514-235">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>   |
| <span data-ttu-id="e8514-236">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e8514-236">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8514-237"><dt>WinHTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8514-237"><dt>Winhttp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8514-238">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8514-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8514-239">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="e8514-239">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

