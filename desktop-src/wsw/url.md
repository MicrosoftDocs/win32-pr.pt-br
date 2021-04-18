---
title: Url
description: Os elementos da API da URL do WWSAPI fornecem mecanismos para dividir e cancelar a saída de URLs em partes de componente e para escapar e combinar partes de componentes de volta em uma URL.
ms.assetid: 2904fee0-d92b-4054-8ad9-51c409756f33
keywords:
- Serviços Web de URL para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8511bf755f80f124071f658a65249243dc2f2af
ms.sourcegitcommit: 6f8c895f4d43c4463f6f33fa8014c5de413ece1f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/20/2020
ms.locfileid: "105813618"
---
# <a name="url"></a><span data-ttu-id="a4bfe-106">Url</span><span class="sxs-lookup"><span data-stu-id="a4bfe-106">Url</span></span>

<span data-ttu-id="a4bfe-107">Os elementos da API da URL do WWSAPI fornecem mecanismos para dividir e cancelar a saída de URLs em partes de componente e para escapar e combinar partes de componentes de volta em uma URL.</span><span class="sxs-lookup"><span data-stu-id="a4bfe-107">The WWSAPI URL API elements provide mechanisms to split and unescape URLs into component parts, and to escape and combine component parts back into a URL.</span></span>

-   <span data-ttu-id="a4bfe-108">Para dividir e cancelar a saída de URLs em partes de componente, use a função [**WsDecodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl) .</span><span class="sxs-lookup"><span data-stu-id="a4bfe-108">To split and unescape URLs into component parts, use the [**WsDecodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl) function.</span></span>
-   <span data-ttu-id="a4bfe-109">Para escapar e combinar partes componentes de volta em uma URL, use a função [**WsEncodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl) .</span><span class="sxs-lookup"><span data-stu-id="a4bfe-109">To escape and combine component parts back into a URL, use the [**WsEncodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl) function.</span></span>
-   <span data-ttu-id="a4bfe-110">Para combinar URLs relativas com uma URL base absoluta formando uma URL absoluta, use a função [**WsCombineUrl**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl) .</span><span class="sxs-lookup"><span data-stu-id="a4bfe-110">To combine relative URLs with an absolute base URL forming an absolute URL, use the [**WsCombineUrl**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl) function.</span></span>

<span data-ttu-id="a4bfe-111">As seguintes enumerações fazem parte da URL:</span><span class="sxs-lookup"><span data-stu-id="a4bfe-111">The following enumerations are part of the URL:</span></span>

-   [<span data-ttu-id="a4bfe-112">**\_sinalizadores de URL do WS \_**</span><span class="sxs-lookup"><span data-stu-id="a4bfe-112">**WS\_URL\_FLAGS**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_xml_writer_encoding_type)
-   [<span data-ttu-id="a4bfe-113">**\_tipo de \_ esquema de URL do WS \_**</span><span class="sxs-lookup"><span data-stu-id="a4bfe-113">**WS\_URL\_SCHEME\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_url_scheme_type)

<span data-ttu-id="a4bfe-114">As funções a seguir fazem parte da URL:</span><span class="sxs-lookup"><span data-stu-id="a4bfe-114">The following functions are part of the URL:</span></span>

-   [<span data-ttu-id="a4bfe-115">**WsCombineUrl**</span><span class="sxs-lookup"><span data-stu-id="a4bfe-115">**WsCombineUrl**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscombineurl)
-   [<span data-ttu-id="a4bfe-116">**WsDecodeUrl**</span><span class="sxs-lookup"><span data-stu-id="a4bfe-116">**WsDecodeUrl**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl)
-   [<span data-ttu-id="a4bfe-117">**WsEncodeUrl**</span><span class="sxs-lookup"><span data-stu-id="a4bfe-117">**WsEncodeUrl**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl)

<span data-ttu-id="a4bfe-118">As seguintes estruturas fazem parte da URL:</span><span class="sxs-lookup"><span data-stu-id="a4bfe-118">The following structures are part of the URL:</span></span>

-   [<span data-ttu-id="a4bfe-119">**\_URL WS https \_**</span><span class="sxs-lookup"><span data-stu-id="a4bfe-119">**WS\_HTTPS\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_https_url)
-   [<span data-ttu-id="a4bfe-120">**\_URL http do WS \_**</span><span class="sxs-lookup"><span data-stu-id="a4bfe-120">**WS\_HTTP\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_url)
-   [<span data-ttu-id="a4bfe-121">**\_URL do NETPIPE WS \_**</span><span class="sxs-lookup"><span data-stu-id="a4bfe-121">**WS\_NETPIPE\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [<span data-ttu-id="a4bfe-122">**URL do WS \_ NETTCP \_**</span><span class="sxs-lookup"><span data-stu-id="a4bfe-122">**WS\_NETTCP\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_nettcp_url)
-   [<span data-ttu-id="a4bfe-123">**URL do WS \_ SOAPUDP \_**</span><span class="sxs-lookup"><span data-stu-id="a4bfe-123">**WS\_SOAPUDP\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_soapudp_url)
-   [<span data-ttu-id="a4bfe-124">**URL do WS \_**</span><span class="sxs-lookup"><span data-stu-id="a4bfe-124">**WS\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_url)

 

 




