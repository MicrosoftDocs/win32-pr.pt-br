---
title: Recursos da API do servidor HTTP
description: Este tópico tem suporte e recursos sem suporte da API do servidor HTTP.
ms.assetid: 448fe5a5-e79f-4c3a-aa76-94cff988f24f
keywords:
- Recursos da API do servidor HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d5f529811b08999d6e1cfffa99fc85288ec471
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292668"
---
# <a name="http-server-api-features"></a><span data-ttu-id="a26b6-104">Recursos da API do servidor HTTP</span><span class="sxs-lookup"><span data-stu-id="a26b6-104">HTTP Server API Features</span></span>

<span data-ttu-id="a26b6-105">As listas a seguir descrevem os recursos com e sem suporte da API do servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="a26b6-105">The following lists describe supported and unsupported features of the HTTP Server API.</span></span>

## <a name="features-supported"></a><span data-ttu-id="a26b6-106">Recursos com suporte</span><span class="sxs-lookup"><span data-stu-id="a26b6-106">Features Supported</span></span>

<span data-ttu-id="a26b6-107">O HTTP dá suporte aos seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="a26b6-107">HTTP supports the following features:</span></span>

-   <span data-ttu-id="a26b6-108">Funcionalidade de servidor HTTP v 1.0 e v 1.1.</span><span class="sxs-lookup"><span data-stu-id="a26b6-108">HTTP v1.0 and v1.1 server functionality.</span></span>
-   <span data-ttu-id="a26b6-109">Protocolo SSL 3,0 (SSL) com suporte para certificados de cliente e de servidor.</span><span class="sxs-lookup"><span data-stu-id="a26b6-109">Secure Sockets Layer 3.0 (SSL) with support for client and server certificates.</span></span>
-   <span data-ttu-id="a26b6-110">Cache de fragmentos de dados para uso em respostas subsequentes.</span><span class="sxs-lookup"><span data-stu-id="a26b6-110">Caching of data fragments for use in subsequent responses.</span></span>
-   <span data-ttu-id="a26b6-111">Suporte para IPv6 e endereçamento IPv4.</span><span class="sxs-lookup"><span data-stu-id="a26b6-111">Support for IPv6 and IPv4 addressing.</span></span>
-   <span data-ttu-id="a26b6-112">Reservas de namespace de URL para segurança de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a26b6-112">URL namespace reservations for application security.</span></span>
-   <span data-ttu-id="a26b6-113">Identificadores verdadeiros para todos os objetos.</span><span class="sxs-lookup"><span data-stu-id="a26b6-113">True handles for all objects.</span></span>
-   <span data-ttu-id="a26b6-114">Modelos de e/s síncronos e assíncronos.</span><span class="sxs-lookup"><span data-stu-id="a26b6-114">Synchronous and asynchronous I/O models.</span></span>
-   <span data-ttu-id="a26b6-115">Suporte para WOW64 em computadores executados em Windows de 64 bits a partir do Windows Server 2003 com Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a26b6-115">Support for WOW64 on computers running on 64-bit Windows starting with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="features-not-supported"></a><span data-ttu-id="a26b6-116">Recursos sem suporte</span><span class="sxs-lookup"><span data-stu-id="a26b6-116">Features Not Supported</span></span>

<span data-ttu-id="a26b6-117">A API do servidor HTTP não oferece suporte para a seguinte funcionalidade:</span><span class="sxs-lookup"><span data-stu-id="a26b6-117">The HTTP Server API does not support the following functionality:</span></span>

-   <span data-ttu-id="a26b6-118">A API do servidor HTTP não executa a autenticação de cliente ou de servidor com base no conteúdo dos cabeçalhos de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="a26b6-118">The HTTP Server API does not perform client or server authentication based on the contents of the HTTP request headers.</span></span> <span data-ttu-id="a26b6-119">Qualquer autenticação necessária deve ser implementada pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a26b6-119">Any required authentication must be implemented by the application.</span></span>
-   <span data-ttu-id="a26b6-120">O WOW64 em computadores que executam o Windows de 64 bits não tem suporte no Windows Server 2003 e no Windows XP com Service Pack 2 (SP2) e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="a26b6-120">WOW64 on computers running on 64-bit Windows is not supported on Windows Server 2003, and Windows XP with Service Pack 2 (SP2) and earlier.</span></span>
-   <span data-ttu-id="a26b6-121">A API do servidor HTTP não dá suporte ao log de solicitações e respostas HTTP.</span><span class="sxs-lookup"><span data-stu-id="a26b6-121">The HTTP Server API does not support logging HTTP requests and responses.</span></span>
-   <span data-ttu-id="a26b6-122">A API do servidor HTTP não faz a parte das respostas HTTP de saída.</span><span class="sxs-lookup"><span data-stu-id="a26b6-122">The HTTP Server API does not chunk outgoing HTTP responses.</span></span> <span data-ttu-id="a26b6-123">O aplicativo deve implementar o agrupamento de respostas, se necessário.</span><span class="sxs-lookup"><span data-stu-id="a26b6-123">The application must implement response chunking if required.</span></span>

 

 




