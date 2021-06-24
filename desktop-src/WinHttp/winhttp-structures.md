---
description: Este tópico identifica as estruturas que o WinHTTP usa.
ms.assetid: e1567393-162e-48d4-8e6b-7620e351136c
title: Estruturas WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9d6f0cdbb467e916b1a6ac54b90491cbee9efdb
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587980"
---
# <a name="winhttp-structures"></a><span data-ttu-id="69529-103">Estruturas WinHTTP</span><span class="sxs-lookup"><span data-stu-id="69529-103">WinHTTP structures</span></span>

<span data-ttu-id="69529-104">O WinHTTP usa as seguintes estruturas:</span><span class="sxs-lookup"><span data-stu-id="69529-104">WinHTTP uses the following structures:</span></span>

<dl> <dt>

[<span data-ttu-id="69529-105">**HTTP_VERSION_INFO**</span><span class="sxs-lookup"><span data-stu-id="69529-105">**HTTP_VERSION_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info)
</dt> <dd>

<span data-ttu-id="69529-106">Contém a versão HTTP global.</span><span class="sxs-lookup"><span data-stu-id="69529-106">Contains the global HTTP version.</span></span>

</dd> <dt>

[<span data-ttu-id="69529-107">**URL_COMPONENTS**</span><span class="sxs-lookup"><span data-stu-id="69529-107">**URL_COMPONENTS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-url_components)
</dt> <dd>

<span data-ttu-id="69529-108">Contém as partes constituintes de uma URL.</span><span class="sxs-lookup"><span data-stu-id="69529-108">Contains the constituent parts of a URL.</span></span> <span data-ttu-id="69529-109">Essa estrutura é usada com as funções [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) e [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) .</span><span class="sxs-lookup"><span data-stu-id="69529-109">This structure is used with the [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) functions.</span></span>

</dd> <dt>

[<span data-ttu-id="69529-110">**WINHTTP_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="69529-110">**WINHTTP_ASYNC_RESULT**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_async_result)
</dt> <dd>

<span data-ttu-id="69529-111">Contém o resultado de uma chamada para uma função assíncrona.</span><span class="sxs-lookup"><span data-stu-id="69529-111">Contains the result of a call to an asynchronous function.</span></span> <span data-ttu-id="69529-112">Essa estrutura é usada com o protótipo de [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) .</span><span class="sxs-lookup"><span data-stu-id="69529-112">This structure is used with the [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) prototype.</span></span>

</dd> <dt>

[<span data-ttu-id="69529-113">**WINHTTP_AUTOPROXY_OPTIONS**</span><span class="sxs-lookup"><span data-stu-id="69529-113">**WINHTTP_AUTOPROXY_OPTIONS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)
</dt> <dd>

<span data-ttu-id="69529-114">Usado para indicar à função [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) se é para especificar a URL do Arquivo PAC (configuração automática de proxy) ou para localizar automaticamente a URL com consultas DHCP ou DNS na rede.</span><span class="sxs-lookup"><span data-stu-id="69529-114">Used to indicate to the [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function whether to specify the URL of the Proxy Auto-Configuration (PAC) file or to automatically locate the URL with DHCP or DNS queries to the network.</span></span>

</dd> <dt>

[<span data-ttu-id="69529-115">**WINHTTP_CERTIFICATE_INFO**</span><span class="sxs-lookup"><span data-stu-id="69529-115">**WINHTTP_CERTIFICATE_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info)
</dt> <dd>

<span data-ttu-id="69529-116">Contém informações de certificado retornadas do servidor.</span><span class="sxs-lookup"><span data-stu-id="69529-116">Contains certificate information returned from the server.</span></span> <span data-ttu-id="69529-117">Essa estrutura é usada pela função [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) .</span><span class="sxs-lookup"><span data-stu-id="69529-117">This structure is used by the [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) function.</span></span>

</dd> <dt>

[<span data-ttu-id="69529-118">**WINHTTP_CONNECTION_GROUP**</span><span class="sxs-lookup"><span data-stu-id="69529-118">**WINHTTP_CONNECTION_GROUP**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_connection_group)
</dt> <dd>

<span data-ttu-id="69529-119">Representa um grupo de conexões.</span><span class="sxs-lookup"><span data-stu-id="69529-119">Represents a connection group.</span></span>

</dd> <dt>

[<span data-ttu-id="69529-120">**WINHTTP_CONNECTION_INFO**</span><span class="sxs-lookup"><span data-stu-id="69529-120">**WINHTTP_CONNECTION_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info)
</dt> <dd>

<span data-ttu-id="69529-121">Contém o endereço IP de origem e de destino da solicitação que gerou a resposta.</span><span class="sxs-lookup"><span data-stu-id="69529-121">Contains the source and destination IP address of the request that generated the response.</span></span>

</dd> <dt>

[<span data-ttu-id="69529-122">**WINHTTP_CREDS**</span><span class="sxs-lookup"><span data-stu-id="69529-122">**WINHTTP_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds)
</dt> <dd>

<span data-ttu-id="69529-123">Contém informações de credenciais de usuário usadas para autenticação de servidor e proxy.</span><span class="sxs-lookup"><span data-stu-id="69529-123">Contains user credential information used for server and proxy authentication.</span></span>

> [!Note]
> <span data-ttu-id="69529-124">Esta estrutura foi preterida.</span><span class="sxs-lookup"><span data-stu-id="69529-124">This structure has been deprecated.</span></span> <span data-ttu-id="69529-125">Em vez disso, o uso da estrutura de [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) é recomendado.</span><span class="sxs-lookup"><span data-stu-id="69529-125">Instead, the use of the [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure is recommended.</span></span>

</dd> <dt>

[<span data-ttu-id="69529-126">**WINHTTP_CREDS_EX**</span><span class="sxs-lookup"><span data-stu-id="69529-126">**WINHTTP_CREDS_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex)
</dt> <dd>

<span data-ttu-id="69529-127">Contém informações de credenciais de usuário usadas para autenticação de servidor e proxy.</span><span class="sxs-lookup"><span data-stu-id="69529-127">Contains user credential information used for server and proxy authentication.</span></span>

</dd> <dt>

[<span data-ttu-id="69529-128">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span><span class="sxs-lookup"><span data-stu-id="69529-128">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config)
</dt> <dd>

<span data-ttu-id="69529-129">Contém as informações de configuração de proxy do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="69529-129">Contains the Internet Explorer proxy configuration information.</span></span>

</dd> <dt>

[<span data-ttu-id="69529-130">**WINHTTP_HOST_CONNECTION_GROUP**</span><span class="sxs-lookup"><span data-stu-id="69529-130">**WINHTTP_HOST_CONNECTION_GROUP**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_host_connection_group)
</dt> <dd>

<span data-ttu-id="69529-131">Representa uma coleção de grupos de conexão.</span><span class="sxs-lookup"><span data-stu-id="69529-131">Represents a collection of connection groups.</span></span>

</dd> <dt>

[<span data-ttu-id="69529-132">**WINHTTP_MATCH_CONNECTION_GUID**</span><span class="sxs-lookup"><span data-stu-id="69529-132">**WINHTTP_MATCH_CONNECTION_GUID**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_match_connection_group)
</dt> <dd>

<span data-ttu-id="69529-133">Representa o GUID de uma conexão, para fins de correspondência de conexão.</span><span class="sxs-lookup"><span data-stu-id="69529-133">Represents the GUID of a connection, for purposes of connection-matching.</span></span>

</dd> <dt>

[<span data-ttu-id="69529-134">**WINHTTP_PROXY_INFO**</span><span class="sxs-lookup"><span data-stu-id="69529-134">**WINHTTP_PROXY_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)
</dt> <dd>

<span data-ttu-id="69529-135">Contém a sessão ou a configuração de proxy padrão.</span><span class="sxs-lookup"><span data-stu-id="69529-135">Contains the session or default proxy configuration.</span></span>

</dd> <dt>

[<span data-ttu-id="69529-136">**WINHTTP_PROXY_RESULT**</span><span class="sxs-lookup"><span data-stu-id="69529-136">**WINHTTP_PROXY_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result)
</dt> <dd>

<span data-ttu-id="69529-137">Uma coleção de entradas de resultados de proxy fornecidas pelo [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span><span class="sxs-lookup"><span data-stu-id="69529-137">A collection of proxy result entries provided by [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="69529-138">**WINHTTP_PROXY_RESULT_ENTRY**</span><span class="sxs-lookup"><span data-stu-id="69529-138">**WINHTTP_PROXY_RESULT_ENTRY**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> <dd>

<span data-ttu-id="69529-139">Uma entrada de resultado de uma chamada para [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span><span class="sxs-lookup"><span data-stu-id="69529-139">A result entry from a call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="69529-140">**WINHTTP_QUERY_CONNECTION_GROUP_RESULT**</span><span class="sxs-lookup"><span data-stu-id="69529-140">**WINHTTP_QUERY_CONNECTION_GROUP_RESULT**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_query_connection_group_result)
</dt> <dd>

<span data-ttu-id="69529-141">Representa uma descrição do estado atual das conexões do WinHttp.</span><span class="sxs-lookup"><span data-stu-id="69529-141">Represents a description of the current state of WinHttp's connections.</span></span>

</dd> <dt>

[<span data-ttu-id="69529-142">**WINHTTP_REQUEST_STATS**</span><span class="sxs-lookup"><span data-stu-id="69529-142">**WINHTTP_REQUEST_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats)
</dt> <dd>

<span data-ttu-id="69529-143">Contém estatísticas para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="69529-143">Contains statistics for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="69529-144">**WINHTTP_REQUEST_TIMES**</span><span class="sxs-lookup"><span data-stu-id="69529-144">**WINHTTP_REQUEST_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times)
</dt> <dd>

<span data-ttu-id="69529-145">Contém informações de tempo para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="69529-145">Contains timing information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="69529-146">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="69529-146">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info)
</dt> <dd>

<span data-ttu-id="69529-147">Contém a conexão SChannel e as informações de codificação para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="69529-147">Contains SChannel connection and cipher information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="69529-148">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="69529-148">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_async_result)
</dt> <dd>

<span data-ttu-id="69529-149">Status de resultado de uma operação WebSocket.</span><span class="sxs-lookup"><span data-stu-id="69529-149">Result status of a WebSocket operation.</span></span>

</dd> <dt>

[<span data-ttu-id="69529-150">**WINHTTP_WEB_SOCKET_STATUS**</span><span class="sxs-lookup"><span data-stu-id="69529-150">**WINHTTP_WEB_SOCKET_STATUS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_status)
</dt> <dd>

<span data-ttu-id="69529-151">Status de uma operação WebSocket.</span><span class="sxs-lookup"><span data-stu-id="69529-151">Status of a WebSocket operation.</span></span>

</dd> </dl>
