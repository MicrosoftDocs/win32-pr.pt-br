---
title: Estruturas da API do servidor HTTP versão 1,0
description: Estruturas da API do servidor HTTP versão 1,0
ms.assetid: e38f7a05-f966-4853-be3b-5cdbf224719e
keywords:
- Estruturas de API do servidor HTTP
- HTTP de estruturas, API de servidor HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67cdd426bbe9329e089352999acf5c0f79b6f94f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365971"
---
# <a name="http-server-api-version-10-structures"></a><span data-ttu-id="90e72-105">Estruturas da API do servidor HTTP versão 1,0</span><span class="sxs-lookup"><span data-stu-id="90e72-105">HTTP Server API Version 1.0 Structures</span></span>

<span data-ttu-id="90e72-106">A API do servidor HTTP fornece as seguintes estruturas:</span><span class="sxs-lookup"><span data-stu-id="90e72-106">The HTTP Server API provides the following structures:</span></span>

-   [<span data-ttu-id="90e72-107">**versão do HTTPAPI \_**</span><span class="sxs-lookup"><span data-stu-id="90e72-107">**HTTPAPI\_VERSION**</span></span>](/windows/desktop/api/Http/ns-http-httpapi_version)
-   [<span data-ttu-id="90e72-108">**\_intervalo de bytes http \_**</span><span class="sxs-lookup"><span data-stu-id="90e72-108">**HTTP\_BYTE\_RANGE**</span></span>](/windows/desktop/api/Http/ns-http-http_byte_range)
-   [<span data-ttu-id="90e72-109">**\_política de cache http \_**</span><span class="sxs-lookup"><span data-stu-id="90e72-109">**HTTP\_CACHE\_POLICY**</span></span>](/windows/desktop/api/Http/ns-http-http_cache_policy)
-   [<span data-ttu-id="90e72-110">**\_URL cooked \_ http**</span><span class="sxs-lookup"><span data-stu-id="90e72-110">**HTTP\_COOKED\_URL**</span></span>](/windows/desktop/api/Http/ns-http-http_cooked_url)
-   [<span data-ttu-id="90e72-111">**\_parte de dados http \_**</span><span class="sxs-lookup"><span data-stu-id="90e72-111">**HTTP\_DATA\_CHUNK**</span></span>](/windows/desktop/api/Http/ns-http-http_data_chunk)
-   [<span data-ttu-id="90e72-112">**\_cabeçalho conhecido \_ http**</span><span class="sxs-lookup"><span data-stu-id="90e72-112">**HTTP\_KNOWN\_HEADER**</span></span>](/windows/desktop/api/Http/ns-http-http_known_header)
-   <span data-ttu-id="90e72-113">[**\_solicitação http**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="90e72-113">[**HTTP\_REQUEST**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85))</span></span>
-   [<span data-ttu-id="90e72-114">**\_cabeçalhos de solicitação HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="90e72-114">**HTTP\_REQUEST\_HEADERS**</span></span>](/windows/desktop/api/Http/ns-http-http_request_headers)
-   [<span data-ttu-id="90e72-115">**\_resposta http**</span><span class="sxs-lookup"><span data-stu-id="90e72-115">**HTTP\_RESPONSE**</span></span>](http-response.md)
-   [<span data-ttu-id="90e72-116">**\_cabeçalhos de resposta http \_**</span><span class="sxs-lookup"><span data-stu-id="90e72-116">**HTTP\_RESPONSE\_HEADERS**</span></span>](/windows/desktop/api/Http/ns-http-http_response_headers)
-   [<span data-ttu-id="90e72-117">**\_parâmetro de \_ \_ escuta IP \_ de configuração de serviço http \_**</span><span class="sxs-lookup"><span data-stu-id="90e72-117">**HTTP\_SERVICE\_CONFIG\_IP\_LISTEN\_PARAM**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ip_listen_param)
-   [<span data-ttu-id="90e72-118">**\_consulta de \_ escuta de IP de configuração de serviço http \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="90e72-118">**HTTP\_SERVICE\_CONFIG\_IP\_LISTEN\_QUERY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ip_listen_query)
-   [<span data-ttu-id="90e72-119">**\_ \_ chave SSL de configuração do serviço http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="90e72-119">**HTTP\_SERVICE\_CONFIG\_SSL\_KEY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_key)
-   [<span data-ttu-id="90e72-120">**\_ \_ parâmetro SSL de configuração do serviço http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="90e72-120">**HTTP\_SERVICE\_CONFIG\_SSL\_PARAM**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_param)
-   [<span data-ttu-id="90e72-121">**\_ \_ consulta SSL de configuração do serviço http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="90e72-121">**HTTP\_SERVICE\_CONFIG\_SSL\_QUERY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_query)
-   [<span data-ttu-id="90e72-122">**\_conjunto de \_ SSL de configuração do serviço http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="90e72-122">**HTTP\_SERVICE\_CONFIG\_SSL\_SET**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_set)
-   [<span data-ttu-id="90e72-123">**\_ \_ \_ \_ chave SNI SSL de configuração de serviço http \_**</span><span class="sxs-lookup"><span data-stu-id="90e72-123">**HTTP\_SERVICE\_CONFIG\_SSL\_SNI\_KEY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_sni_key)
-   [<span data-ttu-id="90e72-124">**\_consulta do serviço http \_ config \_ SSL \_ SNI \_**</span><span class="sxs-lookup"><span data-stu-id="90e72-124">**HTTP\_SERVICE\_CONFIG\_SSL\_SNI\_QUERY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_sni_query)
-   [<span data-ttu-id="90e72-125">**\_conjunto de \_ \_ SNI SSL \_ de configuração de serviço http \_**</span><span class="sxs-lookup"><span data-stu-id="90e72-125">**HTTP\_SERVICE\_CONFIG\_SSL\_SNI\_SET**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_sni_set)
-   [<span data-ttu-id="90e72-126">**\_chave de \_ URLACL de configuração do serviço http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="90e72-126">**HTTP\_SERVICE\_CONFIG\_URLACL\_KEY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_key)
-   [<span data-ttu-id="90e72-127">**\_parâmetro de configuração do serviço http \_ \_ URLACL \_**</span><span class="sxs-lookup"><span data-stu-id="90e72-127">**HTTP\_SERVICE\_CONFIG\_URLACL\_PARAM**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_param)
-   [<span data-ttu-id="90e72-128">**\_consulta de configuração do serviço http \_ \_ URLACL \_**</span><span class="sxs-lookup"><span data-stu-id="90e72-128">**HTTP\_SERVICE\_CONFIG\_URLACL\_QUERY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_query)
-   [<span data-ttu-id="90e72-129">**\_conjunto de \_ URLACL de configuração de serviço http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="90e72-129">**HTTP\_SERVICE\_CONFIG\_URLACL\_SET**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_set)
-   [<span data-ttu-id="90e72-130">**\_informações de \_ certificado de cliente SSL \_ http \_**</span><span class="sxs-lookup"><span data-stu-id="90e72-130">**HTTP\_SSL\_CLIENT\_CERT\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_ssl_client_cert_info)
-   [<span data-ttu-id="90e72-131">**informações de HTTP \_ SSL \_**</span><span class="sxs-lookup"><span data-stu-id="90e72-131">**HTTP\_SSL\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_ssl_info)
-   [<span data-ttu-id="90e72-132">**\_endereço de transporte http \_**</span><span class="sxs-lookup"><span data-stu-id="90e72-132">**HTTP\_TRANSPORT\_ADDRESS**</span></span>](/windows/desktop/api/Http/ns-http-http_transport_address)
-   [<span data-ttu-id="90e72-133">**\_cabeçalho http desconhecido \_**</span><span class="sxs-lookup"><span data-stu-id="90e72-133">**HTTP\_UNKNOWN\_HEADER**</span></span>](/windows/desktop/api/Http/ns-http-http_unknown_header)
-   [<span data-ttu-id="90e72-134">**versão de HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="90e72-134">**HTTP\_VERSION**</span></span>](/windows/desktop/api/Http/ns-http-http_version)

## <a name="related-topics"></a><span data-ttu-id="90e72-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="90e72-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90e72-136">Funções da API do servidor HTTP versão 1,0</span><span class="sxs-lookup"><span data-stu-id="90e72-136">HTTP Server API Version 1.0 Functions</span></span>](http-server-api-version-1-0-functions.md)
</dt> </dl>

 

 