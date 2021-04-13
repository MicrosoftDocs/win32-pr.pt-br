---
title: Códigos de status HTTP (Wininet. h)
description: A tabela a seguir contém as constantes e os valores correspondentes para os códigos de status HTTP retornados pelos servidores na Internet.
ms.assetid: 28a5e889-c8f3-4996-a1ca-c48866fa59d7
topic_type:
- apiref
api_name:
- HTTP_STATUS_CONTINUE
- HTTP_STATUS_SWITCH_PROTOCOLS
- HTTP_STATUS_OK
- HTTP_STATUS_CREATED
- HTTP_STATUS_ACCEPTED
- HTTP_STATUS_PARTIAL
- HTTP_STATUS_NO_CONTENT
- HTTP_STATUS_RESET_CONTENT
- HTTP_STATUS_PARTIAL_CONTENT
- HTTP_STATUS_AMBIGUOUS
- HTTP_STATUS_MOVED
- HTTP_STATUS_REDIRECT
- HTTP_STATUS_REDIRECT_METHOD
- HTTP_STATUS_NOT_MODIFIED
- HTTP_STATUS_USE_PROXY
- HTTP_STATUS_REDIRECT_KEEP_VERB
- HTTP_STATUS_BAD_REQUEST
- HTTP_STATUS_DENIED
- HTTP_STATUS_PAYMENT_REQ
- HTTP_STATUS_FORBIDDEN
- HTTP_STATUS_NOT_FOUND
- HTTP_STATUS_BAD_METHOD
- HTTP_STATUS_NONE_ACCEPTABLE
- HTTP_STATUS_PROXY_AUTH_REQ
- HTTP_STATUS_REQUEST_TIMEOUT
- HTTP_STATUS_CONFLICT
- HTTP_STATUS_GONE
- HTTP_STATUS_LENGTH_REQUIRED
- HTTP_STATUS_PRECOND_FAILED
- HTTP_STATUS_REQUEST_TOO_LARGE
- HTTP_STATUS_URI_TOO_LONG
- HTTP_STATUS_UNSUPPORTED_MEDIA
- HTTP_STATUS_RETRY_WITH
- HTTP_STATUS_SERVER_ERROR
- HTTP_STATUS_NOT_SUPPORTED
- HTTP_STATUS_BAD_GATEWAY
- HTTP_STATUS_SERVICE_UNAVAIL
- HTTP_STATUS_GATEWAY_TIMEOUT
- HTTP_STATUS_VERSION_NOT_SUP
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6933617b0488e059c029dd783af238a3ddbb3ecb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369899"
---
# <a name="http-status-codes-winineth"></a><span data-ttu-id="fb1bf-103">Códigos de status HTTP (Wininet. h)</span><span class="sxs-lookup"><span data-stu-id="fb1bf-103">HTTP Status Codes (Wininet.h)</span></span>

<span data-ttu-id="fb1bf-104">A tabela a seguir contém as constantes e os valores correspondentes para os códigos de status HTTP retornados pelos servidores na Internet.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-104">The following table contains the constants and corresponding values for the HTTP status codes returned by servers on the Internet.</span></span>

<dl> <dt>

<span data-ttu-id="fb1bf-105"><span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**STATUS do HTTP \_ \_ continuar**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-105"><span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-106">100</span><span class="sxs-lookup"><span data-stu-id="fb1bf-106">100</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-107">A solicitação pode ser continuada.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-107">The request can be continued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-108"><span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**\_protocolos de \_ comutação de status http \_**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-108"><span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**HTTP\_STATUS\_SWITCH\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-109">101</span><span class="sxs-lookup"><span data-stu-id="fb1bf-109">101</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-110">O servidor alternou protocolos em um cabeçalho de atualização.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-110">The server has switched protocols in an upgrade header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-111"><span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**STATUS do HTTP \_ \_ OK**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-111"><span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**HTTP\_STATUS\_OK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-112">200</span><span class="sxs-lookup"><span data-stu-id="fb1bf-112">200</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-113">A solicitação foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-113">The request completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-114"><span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**STATUS do HTTP \_ \_ criado**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-114"><span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**HTTP\_STATUS\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-115">201</span><span class="sxs-lookup"><span data-stu-id="fb1bf-115">201</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-116">A solicitação foi atendida e resultou na criação de um novo recurso.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-116">The request has been fulfilled and resulted in the creation of a new resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-117"><span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**\_status http \_ aceito**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-117"><span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**HTTP\_STATUS\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-118">202</span><span class="sxs-lookup"><span data-stu-id="fb1bf-118">202</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-119">A solicitação foi aceita para processamento, mas o processamento não foi concluído.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-119">The request has been accepted for processing, but the processing has not been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-120"><span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**STATUS do HTTP \_ \_ parcial**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-120"><span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**HTTP\_STATUS\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-121">203</span><span class="sxs-lookup"><span data-stu-id="fb1bf-121">203</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-122">As informações meta retornadas no cabeçalho da entidade não são o conjunto definitivo disponível do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-122">The returned meta information in the entity-header is not the definitive set available from the origin server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-123"><span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**STATUS do HTTP \_ \_ sem \_ conteúdo**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-123"><span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**HTTP\_STATUS\_NO\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-124">204</span><span class="sxs-lookup"><span data-stu-id="fb1bf-124">204</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-125">O servidor atendeu à solicitação, mas não há nenhuma informação nova a ser enviada de volta.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-125">The server has fulfilled the request, but there is no new information to send back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-126"><span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**\_conteúdo de \_ redefinição de status http \_**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-126"><span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**HTTP\_STATUS\_RESET\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-127">205</span><span class="sxs-lookup"><span data-stu-id="fb1bf-127">205</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-128">A solicitação foi concluída e o programa cliente deve redefinir a exibição de documento que fez com que a solicitação fosse enviada para permitir que o usuário inicie facilmente outra ação de entrada.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-128">The request has been completed, and the client program should reset the document view that caused the request to be sent to allow the user to easily initiate another input action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-129"><span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**\_ \_ conteúdo parcial do status http \_**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-129"><span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**HTTP\_STATUS\_PARTIAL\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-130">206</span><span class="sxs-lookup"><span data-stu-id="fb1bf-130">206</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-131">O servidor atendeu à solicitação GET parcial para o recurso.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-131">The server has fulfilled the partial GET request for the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-132"><span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**\_status http \_ ambíguo**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-132"><span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**HTTP\_STATUS\_AMBIGUOUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-133">300</span><span class="sxs-lookup"><span data-stu-id="fb1bf-133">300</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-134">O servidor não pôde decidir o que retornar.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-134">The server couldn't decide what to return.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-135"><span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**STATUS do HTTP \_ \_ movido**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-135"><span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**HTTP\_STATUS\_MOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-136">301</span><span class="sxs-lookup"><span data-stu-id="fb1bf-136">301</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-137">O recurso solicitado foi atribuído a um novo URI permanente (Uniform Resource Identifier) e todas as referências futuras a esse recurso devem ser feitas usando um dos URIs retornados.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-137">The requested resource has been assigned to a new permanent URI (Uniform Resource Identifier), and any future references to this resource should be done using one of the returned URIs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-138"><span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**\_redirecionamento de status http \_**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-138"><span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**HTTP\_STATUS\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-139">302</span><span class="sxs-lookup"><span data-stu-id="fb1bf-139">302</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-140">O recurso solicitado reside temporariamente em um URI diferente (Uniform Resource Identifier).</span><span class="sxs-lookup"><span data-stu-id="fb1bf-140">The requested resource resides temporarily under a different URI (Uniform Resource Identifier).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-141"><span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**\_método de \_ redirecionamento de status http \_**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-141"><span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**HTTP\_STATUS\_REDIRECT\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-142">303</span><span class="sxs-lookup"><span data-stu-id="fb1bf-142">303</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-143">A resposta à solicitação pode ser encontrada em um URI diferente (Uniform Resource Identifier) e deve ser recuperada usando um verbo HTTP GET nesse recurso.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-143">The response to the request can be found under a different URI (Uniform Resource Identifier) and should be retrieved using a GET HTTP verb on that resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-144"><span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**\_status http \_ não \_ modificado**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-144"><span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**HTTP\_STATUS\_NOT\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-145">304</span><span class="sxs-lookup"><span data-stu-id="fb1bf-145">304</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-146">O recurso solicitado não foi modificado.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-146">The requested resource has not been modified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-147"><span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**\_proxy de \_ uso de status http \_**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-147"><span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**HTTP\_STATUS\_USE\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-148">305</span><span class="sxs-lookup"><span data-stu-id="fb1bf-148">305</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-149">O recurso solicitado deve ser acessado por meio do proxy fornecido pelo campo local.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-149">The requested resource must be accessed through the proxy given by the location field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-150"><span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**\_verbo de \_ redirecionamento de status http \_ Keep \_**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-150"><span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**HTTP\_STATUS\_REDIRECT\_KEEP\_VERB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-151">307</span><span class="sxs-lookup"><span data-stu-id="fb1bf-151">307</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-152">A solicitação redirecionada mantém o mesmo verbo HTTP.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-152">The redirected request keeps the same HTTP verb.</span></span> <span data-ttu-id="fb1bf-153">Comportamento de HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-153">HTTP/1.1 behavior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-154"><span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**\_ \_ solicitação inadequada de status http \_**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-154"><span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**HTTP\_STATUS\_BAD\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-155">400</span><span class="sxs-lookup"><span data-stu-id="fb1bf-155">400</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-156">A solicitação não pôde ser processada pelo servidor devido à sintaxe inválida.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-156">The request could not be processed by the server due to invalid syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-157"><span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**STATUS do HTTP \_ \_ negado**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-157"><span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**HTTP\_STATUS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-158">401</span><span class="sxs-lookup"><span data-stu-id="fb1bf-158">401</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-159">O recurso solicitado requer a autenticação do usuário.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-159">The requested resource requires user authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-160"><span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**Req. de \_ pagamento de status http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-160"><span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**HTTP\_STATUS\_PAYMENT\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-161">402</span><span class="sxs-lookup"><span data-stu-id="fb1bf-161">402</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-162">Não implementado atualmente no protocolo HTTP.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-162">Not currently implemented in the HTTP protocol.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-163"><span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**STATUS de HTTP \_ \_ proibido**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-163"><span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**HTTP\_STATUS\_FORBIDDEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-164">403</span><span class="sxs-lookup"><span data-stu-id="fb1bf-164">403</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-165">O servidor entendeu a solicitação, mas está se recusando a atendê-la.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-165">The server understood the request, but is refusing to fulfill it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-166"><span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**\_status http \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-166"><span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**HTTP\_STATUS\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-167">404</span><span class="sxs-lookup"><span data-stu-id="fb1bf-167">404</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-168">O servidor não encontrou nada correspondente ao URI solicitado (Uniform Resource Identifier).</span><span class="sxs-lookup"><span data-stu-id="fb1bf-168">The server has not found anything matching the requested URI (Uniform Resource Identifier).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-169"><span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**\_ \_ método inadequado de status http \_**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-169"><span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**HTTP\_STATUS\_BAD\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-170">405</span><span class="sxs-lookup"><span data-stu-id="fb1bf-170">405</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-171">O verbo HTTP usado não é permitido.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-171">The HTTP verb used is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-172"><span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**\_status http \_ nenhum \_ aceitável**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-172"><span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**HTTP\_STATUS\_NONE\_ACCEPTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-173">406</span><span class="sxs-lookup"><span data-stu-id="fb1bf-173">406</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-174">Nenhuma resposta aceitável para o cliente foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-174">No responses acceptable to the client were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-175"><span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**Req. de autenticação de proxy de \_ status http \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-175"><span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**HTTP\_STATUS\_PROXY\_AUTH\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-176">407</span><span class="sxs-lookup"><span data-stu-id="fb1bf-176">407</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-177">Autenticação de proxy necessária.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-177">Proxy authentication required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-178"><span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**\_ \_ tempo limite de solicitação de status http \_**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-178"><span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**HTTP\_STATUS\_REQUEST\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-179">408</span><span class="sxs-lookup"><span data-stu-id="fb1bf-179">408</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-180">O servidor atingiu o tempo limite ao aguardar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-180">The server timed out waiting for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-181"><span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**\_conflito de status http \_**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-181"><span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**HTTP\_STATUS\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-182">409</span><span class="sxs-lookup"><span data-stu-id="fb1bf-182">409</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-183">A solicitação não pôde ser concluída devido a um conflito com o estado atual do recurso.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-183">The request could not be completed due to a conflict with the current state of the resource.</span></span> <span data-ttu-id="fb1bf-184">O usuário deve enviar novamente com mais informações.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-184">The user should resubmit with more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-185"><span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**\_status http \_ ausente**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-185"><span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**HTTP\_STATUS\_GONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-186">410</span><span class="sxs-lookup"><span data-stu-id="fb1bf-186">410</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-187">O recurso solicitado não está mais disponível no servidor e nenhum endereço de encaminhamento é conhecido.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-187">The requested resource is no longer available at the server, and no forwarding address is known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-188"><span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**\_comprimento de status http \_ \_ necessário**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-188"><span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**HTTP\_STATUS\_LENGTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-189">411</span><span class="sxs-lookup"><span data-stu-id="fb1bf-189">411</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-190">O servidor se recusa a aceitar a solicitação sem um comprimento de conteúdo definido.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-190">The server refuses to accept the request without a defined content length.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-191"><span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**\_falha de \_ PRECOND de status http \_**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-191"><span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**HTTP\_STATUS\_PRECOND\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-192">412</span><span class="sxs-lookup"><span data-stu-id="fb1bf-192">412</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-193">A pré-condição fornecida em um ou mais dos campos de cabeçalho da solicitação foi avaliada como falsa quando foi testada no servidor.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-193">The precondition given in one or more of the request header fields evaluated to false when it was tested on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-194"><span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**\_solicitação de status http \_ \_ muito \_ grande**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-194"><span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**HTTP\_STATUS\_REQUEST\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-195">413</span><span class="sxs-lookup"><span data-stu-id="fb1bf-195">413</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-196">O servidor está se recusando a processar uma solicitação porque a entidade de solicitação é maior do que o servidor está disposto ou pode processar.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-196">The server is refusing to process a request because the request entity is larger than the server is willing or able to process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-197"><span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**\_URI de status http \_ \_ muito \_ longo**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-197"><span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**HTTP\_STATUS\_URI\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-198">414</span><span class="sxs-lookup"><span data-stu-id="fb1bf-198">414</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-199">O servidor está se recusando a atender à solicitação porque o URI de solicitação (Uniform Resource Identifier) é maior do que o servidor está disposto a interpretar.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-199">The server is refusing to service the request because the request URI (Uniform Resource Identifier) is longer than the server is willing to interpret.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-200"><span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**\_mídia de status http \_ sem suporte \_**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-200"><span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**HTTP\_STATUS\_UNSUPPORTED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-201">415</span><span class="sxs-lookup"><span data-stu-id="fb1bf-201">415</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-202">O servidor está se recusando a atender à solicitação porque a entidade da solicitação está em um formato não suportado pelo recurso solicitado para o método solicitado.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-202">The server is refusing to service the request because the entity of the request is in a format not supported by the requested resource for the requested method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-203"><span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**\_ \_ repetição de status http \_ com**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-203"><span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**HTTP\_STATUS\_RETRY\_WITH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-204">449</span><span class="sxs-lookup"><span data-stu-id="fb1bf-204">449</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-205">A solicitação deve ser repetida após a ação apropriada.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-205">The request should be retried after doing the appropriate action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-206"><span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**\_ \_ erro do servidor de status http \_**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-206"><span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**HTTP\_STATUS\_SERVER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-207">500</span><span class="sxs-lookup"><span data-stu-id="fb1bf-207">500</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-208">O servidor encontrou uma condição inesperada que o impediu de atender à solicitação.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-208">The server encountered an unexpected condition that prevented it from fulfilling the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-209"><span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**\_status http \_ sem \_ suporte**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-209"><span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**HTTP\_STATUS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-210">501</span><span class="sxs-lookup"><span data-stu-id="fb1bf-210">501</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-211">O servidor não oferece suporte à funcionalidade necessária para atender à solicitação.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-211">The server does not support the functionality required to fulfill the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-212"><span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**\_ \_ Gateway insatisfatório de status http \_**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-212"><span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**HTTP\_STATUS\_BAD\_GATEWAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-213">502</span><span class="sxs-lookup"><span data-stu-id="fb1bf-213">502</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-214">O servidor, ao atuar como gateway ou proxy, recebeu uma resposta inválida do servidor upstream acessado na tentativa de atender à solicitação.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-214">The server, while acting as a gateway or proxy, received an invalid response from the upstream server it accessed in attempting to fulfill the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-215"><span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**serviço de status HTTP não \_ \_ \_ disp.**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-215"><span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**HTTP\_STATUS\_SERVICE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-216">503</span><span class="sxs-lookup"><span data-stu-id="fb1bf-216">503</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-217">O serviço está temporariamente sobrecarregado.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-217">The service is temporarily overloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-218"><span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**\_ \_ tempo limite do gateway de status http \_**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-218"><span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**HTTP\_STATUS\_GATEWAY\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-219">504</span><span class="sxs-lookup"><span data-stu-id="fb1bf-219">504</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-220">A solicitação atingiu o tempo limite ao aguardar um gateway.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-220">The request was timed out waiting for a gateway.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb1bf-221"><span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**\_versão de status http \_ \_ não \_ sup**</span><span class="sxs-lookup"><span data-stu-id="fb1bf-221"><span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**HTTP\_STATUS\_VERSION\_NOT\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1bf-222">505</span><span class="sxs-lookup"><span data-stu-id="fb1bf-222">505</span></span>
</dt> <dt>



<span data-ttu-id="fb1bf-223">O servidor não dá suporte a, ou recusa-se a oferecer suporte à versão do protocolo HTTP que foi usada na mensagem de solicitação.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-223">The server does not support, or refuses to support, the HTTP protocol version that was used in the request message.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb1bf-224">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb1bf-224">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fb1bf-225">O WinINet não oferece suporte a implementações de servidor.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-225">WinINet does not support server implementations.</span></span> <span data-ttu-id="fb1bf-226">Além disso, ele não deve ser usado de um serviço.</span><span class="sxs-lookup"><span data-stu-id="fb1bf-226">In addition, it should not be used from a service.</span></span> <span data-ttu-id="fb1bf-227">Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="fb1bf-227">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fb1bf-228">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb1bf-228">Requirements</span></span>



| <span data-ttu-id="fb1bf-229">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb1bf-229">Requirement</span></span> | <span data-ttu-id="fb1bf-230">Valor</span><span class="sxs-lookup"><span data-stu-id="fb1bf-230">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fb1bf-231">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb1bf-231">Minimum supported client</span></span><br/> | <span data-ttu-id="fb1bf-232">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fb1bf-232">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="fb1bf-233">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb1bf-233">Minimum supported server</span></span><br/> | <span data-ttu-id="fb1bf-234">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fb1bf-234">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fb1bf-235">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fb1bf-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb1bf-236"><dt>WinInet. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb1bf-236"><dt>Wininet.h</dt></span></span> </dl> |



 

