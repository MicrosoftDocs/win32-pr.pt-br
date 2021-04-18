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
# <a name="http_log_field_-constants"></a><span data-ttu-id="fb500-103">\_Constantes de \_ campo de log http \_</span><span class="sxs-lookup"><span data-stu-id="fb500-103">HTTP\_LOG\_FIELD\_ Constants</span></span>

<span data-ttu-id="fb500-104">As constantes de **\_ \_ campo \_ de log http** definem os campos no log W3C e os logs de erros.</span><span class="sxs-lookup"><span data-stu-id="fb500-104">The **HTTP\_LOG\_FIELD\_** constants define the fields in the W3C log and the error logs.</span></span>

<span data-ttu-id="fb500-105">Essas constantes são usadas na estrutura [**de \_ \_ informações de log http**](/windows/desktop/api/Http/ns-http-http_logging_info) .</span><span class="sxs-lookup"><span data-stu-id="fb500-105">These constants are used in the [**HTTP\_LOGGING\_INFO**](/windows/desktop/api/Http/ns-http-http_logging_info) structure.</span></span>

<dl> <dt>

<span data-ttu-id="fb500-106"><span id="HTTP_LOG_FIELD_DATE"></span><span id="http_log_field_date"></span>**\_data do \_ campo de log http \_**</span><span class="sxs-lookup"><span data-stu-id="fb500-106"><span id="HTTP_LOG_FIELD_DATE"></span><span id="http_log_field_date"></span>**HTTP\_LOG\_FIELD\_DATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-107">A data em que a atividade ocorreu.</span><span class="sxs-lookup"><span data-stu-id="fb500-107">The date on which the activity occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb500-108"><span id="HTTP_LOG_FIELD_TIME"></span><span id="http_log_field_time"></span>**\_tempo do \_ campo de log http \_**</span><span class="sxs-lookup"><span data-stu-id="fb500-108"><span id="HTTP_LOG_FIELD_TIME"></span><span id="http_log_field_time"></span>**HTTP\_LOG\_FIELD\_TIME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-109">A hora, em UTC (tempo Universal Coordenado), na qual a atividade ocorreu.</span><span class="sxs-lookup"><span data-stu-id="fb500-109">The time, in coordinated universal time (UTC), at which the activity occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb500-110"><span id="HTTP_LOG_FIELD_CLIENT_IP"></span><span id="http_log_field_client_ip"></span>**\_IP do \_ cliente do campo de log http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fb500-110"><span id="HTTP_LOG_FIELD_CLIENT_IP"></span><span id="http_log_field_client_ip"></span>**HTTP\_LOG\_FIELD\_CLIENT\_IP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-111">Endereço IP do cliente que fez a solicitação.</span><span class="sxs-lookup"><span data-stu-id="fb500-111">The IP address of the client that made the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb500-112"><span id="HTTP_LOG_FIELD_USER_NAME"></span><span id="http_log_field_user_name"></span>**\_nome de \_ usuário do campo de log http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fb500-112"><span id="HTTP_LOG_FIELD_USER_NAME"></span><span id="http_log_field_user_name"></span>**HTTP\_LOG\_FIELD\_USER\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-113">O nome do usuário autenticado que acessou seu servidor.</span><span class="sxs-lookup"><span data-stu-id="fb500-113">The name of the authenticated user who accessed your server.</span></span> <span data-ttu-id="fb500-114">Os usuários anônimos são indicados por um hífen.</span><span class="sxs-lookup"><span data-stu-id="fb500-114">Anonymous users are indicated by a hyphen.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb500-115"><span id="HTTP_LOG_FIELD_SITE_NAME"></span><span id="http_log_field_site_name"></span>**\_nome do \_ site do campo de log http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fb500-115"><span id="HTTP_LOG_FIELD_SITE_NAME"></span><span id="http_log_field_site_name"></span>**HTTP\_LOG\_FIELD\_SITE\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-116">O nome do site no qual a entrada do arquivo de log foi gerada.</span><span class="sxs-lookup"><span data-stu-id="fb500-116">The name of the site on which the log file entry was generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb500-117"><span id="_HTTP_LOG_FIELD_COMPUTER_NAME"></span><span id="_http_log_field_computer_name"></span>**Http \_ \_nome do \_ computador \_ do campo de log**</span><span class="sxs-lookup"><span data-stu-id="fb500-117"><span id="_HTTP_LOG_FIELD_COMPUTER_NAME"></span><span id="_http_log_field_computer_name"></span> **HTTP\_LOG\_FIELD\_COMPUTER\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-118">O nome do computador no qual a entrada do arquivo de log foi gerada.</span><span class="sxs-lookup"><span data-stu-id="fb500-118">The name of the computer on which the log file entry was generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb500-119"><span id="HTTP_LOG_FIELD_SERVER_IP"></span><span id="http_log_field_server_ip"></span>**\_ \_ \_ IP do servidor de campo de log http \_**</span><span class="sxs-lookup"><span data-stu-id="fb500-119"><span id="HTTP_LOG_FIELD_SERVER_IP"></span><span id="http_log_field_server_ip"></span>**HTTP\_LOG\_FIELD\_SERVER\_IP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-120">O endereço IP do servidor no qual a entrada do arquivo de log foi gerada.</span><span class="sxs-lookup"><span data-stu-id="fb500-120">The IP address of the server on which the log file entry was generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb500-121"><span id="HTTP_LOG_FIELD_METHOD"></span><span id="http_log_field_method"></span>**\_método de \_ campo de log http \_**</span><span class="sxs-lookup"><span data-stu-id="fb500-121"><span id="HTTP_LOG_FIELD_METHOD"></span><span id="http_log_field_method"></span>**HTTP\_LOG\_FIELD\_METHOD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-122">A ação solicitada, por exemplo, um método Get.</span><span class="sxs-lookup"><span data-stu-id="fb500-122">The requested action, for example, a get method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb500-123"><span id="_HTTP_LOG_FIELD_URI_STEM"></span><span id="_http_log_field_uri_stem"></span>**Http \_ \_ \_ \_ tronco URI do campo de log**</span><span class="sxs-lookup"><span data-stu-id="fb500-123"><span id="_HTTP_LOG_FIELD_URI_STEM"></span><span id="_http_log_field_uri_stem"></span> **HTTP\_LOG\_FIELD\_URI\_STEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-124">O destino da ação, por exemplo, Default.htm.</span><span class="sxs-lookup"><span data-stu-id="fb500-124">The target of the action, for example, Default.htm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb500-125"><span id="HTTP_LOG_FIELD_URI_QUERY"></span><span id="http_log_field_uri_query"></span>**\_consulta de \_ URI de campo de log http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fb500-125"><span id="HTTP_LOG_FIELD_URI_QUERY"></span><span id="http_log_field_uri_query"></span>**HTTP\_LOG\_FIELD\_URI\_QUERY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-126">A consulta, se houver, que o cliente estava tentando executar.</span><span class="sxs-lookup"><span data-stu-id="fb500-126">The query, if any, that the client was trying to perform.</span></span> <span data-ttu-id="fb500-127">Um URI (Resource Identifier Universal) consulta é necessário apenas para páginas dinâmico.</span><span class="sxs-lookup"><span data-stu-id="fb500-127">A Universal Resource Identifier (URI) query is necessary only for dynamic pages.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb500-128"><span id="HTTP_LOG_FIELD_STATUS"></span><span id="http_log_field_status"></span>**\_status do \_ campo de log http \_**</span><span class="sxs-lookup"><span data-stu-id="fb500-128"><span id="HTTP_LOG_FIELD_STATUS"></span><span id="http_log_field_status"></span>**HTTP\_LOG\_FIELD\_STATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-129">O código de status HTTP.</span><span class="sxs-lookup"><span data-stu-id="fb500-129">The HTTP status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb500-130"><span id="HTTP_LOG_FIELD_WIN32_STATUS"></span><span id="http_log_field_win32_status"></span>**\_Status do \_ Win32 do campo de log http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fb500-130"><span id="HTTP_LOG_FIELD_WIN32_STATUS"></span><span id="http_log_field_win32_status"></span>**HTTP\_LOG\_FIELD\_WIN32\_STATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-131">O código de status do Windows.</span><span class="sxs-lookup"><span data-stu-id="fb500-131">The Windows status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb500-132"><span id="HTTP_LOG_FIELD_BYTES_SENT"></span><span id="http_log_field_bytes_sent"></span>**\_bytes de campo de log http \_ \_ \_ enviados**</span><span class="sxs-lookup"><span data-stu-id="fb500-132"><span id="HTTP_LOG_FIELD_BYTES_SENT"></span><span id="http_log_field_bytes_sent"></span>**HTTP\_LOG\_FIELD\_BYTES\_SENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-133">O número, em bytes, enviado pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="fb500-133">The number, in bytes, sent by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb500-134"><span id="HTTP_LOG_FIELD_BYTES_RECV"></span><span id="http_log_field_bytes_recv"></span>**\_bytes de campo de log http \_ \_ \_ recv**</span><span class="sxs-lookup"><span data-stu-id="fb500-134"><span id="HTTP_LOG_FIELD_BYTES_RECV"></span><span id="http_log_field_bytes_recv"></span>**HTTP\_LOG\_FIELD\_BYTES\_RECV**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-135">O número, em bytes, recebido pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="fb500-135">The number, in bytes, received by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb500-136"><span id="HTTP_LOG_FIELD_TIME_TAKEN"></span><span id="http_log_field_time_taken"></span>**\_tempo de campo de log http \_ \_ \_ retirado**</span><span class="sxs-lookup"><span data-stu-id="fb500-136"><span id="HTTP_LOG_FIELD_TIME_TAKEN"></span><span id="http_log_field_time_taken"></span>**HTTP\_LOG\_FIELD\_TIME\_TAKEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-137">O tempo, em milissegundos, da ação.</span><span class="sxs-lookup"><span data-stu-id="fb500-137">The time, in milliseconds, of the action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb500-138"><span id="HTTP_LOG_FIELD_SERVER_PORT"></span><span id="http_log_field_server_port"></span>**\_ \_ \_ porta do servidor de campo de log http \_**</span><span class="sxs-lookup"><span data-stu-id="fb500-138"><span id="HTTP_LOG_FIELD_SERVER_PORT"></span><span id="http_log_field_server_port"></span>**HTTP\_LOG\_FIELD\_SERVER\_PORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-139">O número da porta do servidor que está configurado para o serviço.</span><span class="sxs-lookup"><span data-stu-id="fb500-139">The server port number that is configured for the service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb500-140"><span id="_HTTP_LOG_FIELD_USER_AGENT"></span><span id="_http_log_field_user_agent"></span>**Http \_ \_agente do \_ usuário \_ do campo de log**</span><span class="sxs-lookup"><span data-stu-id="fb500-140"><span id="_HTTP_LOG_FIELD_USER_AGENT"></span><span id="_http_log_field_user_agent"></span> **HTTP\_LOG\_FIELD\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-141">O aplicativo usado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="fb500-141">The application that the client used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb500-142"><span id="HTTP_LOG_FIELD_COOKIE"></span><span id="http_log_field_cookie"></span>**\_cookie de \_ campo de log http \_**</span><span class="sxs-lookup"><span data-stu-id="fb500-142"><span id="HTTP_LOG_FIELD_COOKIE"></span><span id="http_log_field_cookie"></span>**HTTP\_LOG\_FIELD\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-143">O conteúdo do cookie enviado ou recebido, se houver.</span><span class="sxs-lookup"><span data-stu-id="fb500-143">The content of the cookie sent or received, if any.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb500-144"><span id="HTTP_LOG_FIELD_REFERER"></span><span id="http_log_field_referer"></span>**\_ \_ referenciador de campo de log http \_**</span><span class="sxs-lookup"><span data-stu-id="fb500-144"><span id="HTTP_LOG_FIELD_REFERER"></span><span id="http_log_field_referer"></span>**HTTP\_LOG\_FIELD\_REFERER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-145">O site que o usuário visitou pela última vez.</span><span class="sxs-lookup"><span data-stu-id="fb500-145">The site that the user last visited.</span></span> <span data-ttu-id="fb500-146">Esse site fornece um link para o site atual.</span><span class="sxs-lookup"><span data-stu-id="fb500-146">This site provided a link to the current site.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb500-147"><span id="HTTP_LOG_FIELD_VERSION"></span><span id="http_log_field_version"></span>**\_versão do \_ campo de log http \_**</span><span class="sxs-lookup"><span data-stu-id="fb500-147"><span id="HTTP_LOG_FIELD_VERSION"></span><span id="http_log_field_version"></span>**HTTP\_LOG\_FIELD\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-148">A versão do protocolo HTTP que o cliente usou.</span><span class="sxs-lookup"><span data-stu-id="fb500-148">The HTTP protocol version that the client used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb500-149"><span id="HTTP_LOG_FIELD_HOST"></span><span id="http_log_field_host"></span>**\_host de \_ campo de log http \_**</span><span class="sxs-lookup"><span data-stu-id="fb500-149"><span id="HTTP_LOG_FIELD_HOST"></span><span id="http_log_field_host"></span>**HTTP\_LOG\_FIELD\_HOST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-150">O nome do cabeçalho de host, se houver.</span><span class="sxs-lookup"><span data-stu-id="fb500-150">The host header name, if any.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb500-151"><span id="HTTP_LOG_FIELD_SUB_STATUS"></span><span id="http_log_field_sub_status"></span>**substatus de \_ campo de log http \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fb500-151"><span id="HTTP_LOG_FIELD_SUB_STATUS"></span><span id="http_log_field_sub_status"></span>**HTTP\_LOG\_FIELD\_SUB\_STATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-152">O código de erro de substatus.</span><span class="sxs-lookup"><span data-stu-id="fb500-152">The substatus error code.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="fb500-153">As constantes a seguir são usadas para o log de erros HTTP.</span><span class="sxs-lookup"><span data-stu-id="fb500-153">The following constants are used for HTTP error logging.</span></span>

<dl> <dt>

<span data-ttu-id="fb500-154"><span id="HTTP_LOG_FIELD_CLIENT_PORT"></span><span id="http_log_field_client_port"></span>**\_porta do \_ cliente do campo de log http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fb500-154"><span id="HTTP_LOG_FIELD_CLIENT_PORT"></span><span id="http_log_field_client_port"></span>**HTTP\_LOG\_FIELD\_CLIENT\_PORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-155">O número da porta do cliente a partir da qual a solicitação é recebida.</span><span class="sxs-lookup"><span data-stu-id="fb500-155">The client port number from which the request is received.</span></span> <span data-ttu-id="fb500-156">Este campo de log só é usado para log de erros.</span><span class="sxs-lookup"><span data-stu-id="fb500-156">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb500-157"><span id="HTTP_LOG_FIELD_URI"></span><span id="http_log_field_uri"></span>**\_URI do \_ campo de log http \_**</span><span class="sxs-lookup"><span data-stu-id="fb500-157"><span id="HTTP_LOG_FIELD_URI"></span><span id="http_log_field_uri"></span>**HTTP\_LOG\_FIELD\_URI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-158">O URI recebido na solicitação, incluindo a parte de consulta.</span><span class="sxs-lookup"><span data-stu-id="fb500-158">The URI received in the request including the query portion.</span></span> <span data-ttu-id="fb500-159">Este campo de log só é usado para log de erros.</span><span class="sxs-lookup"><span data-stu-id="fb500-159">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb500-160"><span id="HTTP_LOG_FIELD_SITE_ID"></span><span id="http_log_field_site_id"></span>**\_ID do \_ site do campo de log http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fb500-160"><span id="HTTP_LOG_FIELD_SITE_ID"></span><span id="http_log_field_site_id"></span>**HTTP\_LOG\_FIELD\_SITE\_ID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-161">A ID numérica específica do aplicativo do grupo de URLs na qual a solicitação é roteada.</span><span class="sxs-lookup"><span data-stu-id="fb500-161">The application-specific numeric ID of the URL Group on which the request is routed.</span></span> <span data-ttu-id="fb500-162">Este campo de log só é usado para log de erros.</span><span class="sxs-lookup"><span data-stu-id="fb500-162">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb500-163"><span id="HTTP_LOG_FIELD_REASON"></span><span id="http_log_field_reason"></span>**\_motivo do \_ campo de log http \_**</span><span class="sxs-lookup"><span data-stu-id="fb500-163"><span id="HTTP_LOG_FIELD_REASON"></span><span id="http_log_field_reason"></span>**HTTP\_LOG\_FIELD\_REASON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-164">A frase do motivo do erro.</span><span class="sxs-lookup"><span data-stu-id="fb500-164">The error reason phrase.</span></span> <span data-ttu-id="fb500-165">Este campo de log só é usado para log de erros.</span><span class="sxs-lookup"><span data-stu-id="fb500-165">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb500-166"><span id="HTTP_LOG_FIELD_QUEUE_NAME"></span><span id="http_log_field_queue_name"></span>**\_nome da \_ fila do campo de log http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fb500-166"><span id="HTTP_LOG_FIELD_QUEUE_NAME"></span><span id="http_log_field_queue_name"></span>**HTTP\_LOG\_FIELD\_QUEUE\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-167">O nome da fila de solicitações para a qual a solicitação é expedida.</span><span class="sxs-lookup"><span data-stu-id="fb500-167">The name of the request queue to which the request is dispatched.</span></span> <span data-ttu-id="fb500-168">Este campo de log só é usado para log de erros.</span><span class="sxs-lookup"><span data-stu-id="fb500-168">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fb500-169"><span id="HTTP_LOG_FIELD_STREAMID"></span><span id="http_log_field_streamid"></span>**\_campo de log http \_ \_ streamid**</span><span class="sxs-lookup"><span data-stu-id="fb500-169"><span id="HTTP_LOG_FIELD_STREAMID"></span><span id="http_log_field_streamid"></span>**HTTP\_LOG\_FIELD\_STREAMID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fb500-170">A ID do fluxo.</span><span class="sxs-lookup"><span data-stu-id="fb500-170">The stream id.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fb500-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb500-171">Requirements</span></span>



| <span data-ttu-id="fb500-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb500-172">Requirement</span></span> | <span data-ttu-id="fb500-173">Valor</span><span class="sxs-lookup"><span data-stu-id="fb500-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fb500-174">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb500-174">Minimum supported client</span></span><br/> | <span data-ttu-id="fb500-175">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fb500-175">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fb500-176">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb500-176">Minimum supported server</span></span><br/> | <span data-ttu-id="fb500-177">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fb500-177">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fb500-178">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb500-178">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb500-179"><dt>Http. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb500-179"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb500-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb500-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb500-181">Constantes da API do servidor HTTP versão 2,0</span><span class="sxs-lookup"><span data-stu-id="fb500-181">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="fb500-182">**\_informações de log http \_**</span><span class="sxs-lookup"><span data-stu-id="fb500-182">**HTTP\_LOGGING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[<span data-ttu-id="fb500-183">**HttpSetUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="fb500-183">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[<span data-ttu-id="fb500-184">**HttpSetServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="fb500-184">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[<span data-ttu-id="fb500-185">**HttpQueryUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="fb500-185">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[<span data-ttu-id="fb500-186">**HttpQueryServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="fb500-186">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





