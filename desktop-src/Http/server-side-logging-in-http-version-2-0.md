---
title: Log de Server-Side
description: O registro em log do lado do servidor está disponível em um grupo de URLs ou sessão de servidor.
ms.assetid: e1fcd87f-382a-42bf-b53f-1e1cb1dbbfc5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b76548b296bcdbd343e4e259e0cf3c87537ef5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822806"
---
# <a name="server-side-logging"></a><span data-ttu-id="d69f3-103">Log de Server-Side</span><span class="sxs-lookup"><span data-stu-id="d69f3-103">Server-Side Logging</span></span>

<span data-ttu-id="d69f3-104">O registro em log do lado do servidor está disponível em um grupo de URLs ou sessão de servidor.</span><span class="sxs-lookup"><span data-stu-id="d69f3-104">Server-side logging is available on a URL group or server session.</span></span> <span data-ttu-id="d69f3-105">Quando o log está habilitado em uma sessão de servidor, ele funciona como uma forma centralizada de registro em log para todos os grupos de URLs na sessão do servidor.</span><span class="sxs-lookup"><span data-stu-id="d69f3-105">When logging is enabled on a server session, it functions as centralized form of logging for all the URL groups under the server session.</span></span> <span data-ttu-id="d69f3-106">Quando o log está habilitado em um grupo de URLs, o log é executado somente em solicitações que são roteadas para o grupo de URLs.</span><span class="sxs-lookup"><span data-stu-id="d69f3-106">When logging is enabled on a URL group, logging is performed only on requests that are routed to the URL Group.</span></span> <span data-ttu-id="d69f3-107">Os seguintes tipos de registro em log são suportados pela API do servidor HTTP:</span><span class="sxs-lookup"><span data-stu-id="d69f3-107">The following types of logging are supported by the HTTP Server API:</span></span>

-   <span data-ttu-id="d69f3-108">[Log W3C](w3c-logging.md): disponível na sessão do servidor e no grupo de URLs.</span><span class="sxs-lookup"><span data-stu-id="d69f3-108">[W3C logging](w3c-logging.md): Available on the server session and URL group.</span></span>
-   <span data-ttu-id="d69f3-109">[Log do NCSA](ncsa-logging.md): disponível no grupo de URLs.</span><span class="sxs-lookup"><span data-stu-id="d69f3-109">[NCSA logging](ncsa-logging.md): Available on the URL group.</span></span>
-   <span data-ttu-id="d69f3-110">[Log do IIS](iis-logging.md): disponível no grupo de URLs.</span><span class="sxs-lookup"><span data-stu-id="d69f3-110">[IIS logging](iis-logging.md): Available on the URL group.</span></span>
-   <span data-ttu-id="d69f3-111">[Log binário centralizado](centralized-binary-logging.md): disponível na sessão do servidor.</span><span class="sxs-lookup"><span data-stu-id="d69f3-111">[Centralized binary logging](centralized-binary-logging.md): Available on the server session.</span></span>

<span data-ttu-id="d69f3-112">Para aproveitar o recurso de log HTTP, o aplicativo habilita e configura um tipo de log na sessão de servidor ou no grupo de URLs.</span><span class="sxs-lookup"><span data-stu-id="d69f3-112">To take advantage of the HTTP logging feature, the application enables and configures one type of logging on the server session or URL group.</span></span> <span data-ttu-id="d69f3-113">Para obter mais informações, consulte [Configurando e habilitando o log do servidor](configuring-and-enabling-server-side-logging.md)</span><span class="sxs-lookup"><span data-stu-id="d69f3-113">For more information, see [Configuring and Enabling Server Side Logging](configuring-and-enabling-server-side-logging.md)</span></span>

 

 




