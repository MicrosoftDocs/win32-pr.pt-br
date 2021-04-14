---
description: Esta seção descreve como usar a API C/C++ para o Microsoft Windows HTTP Services (WinHTTP) e a interface COM exposta pelo objeto WinHttpRequest.
ms.assetid: 16178bb8-5e95-46a5-825a-880edc402445
title: Usando o WinHTTP
ms.topic: article
ms.date: 07/22/2020
ms.openlocfilehash: cda0a7772b88dfd9c03675c522f4b7504ea00b06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461129"
---
# <a name="using-winhttp"></a><span data-ttu-id="4ddb3-103">Usando o WinHTTP</span><span class="sxs-lookup"><span data-stu-id="4ddb3-103">Using WinHTTP</span></span>

<span data-ttu-id="4ddb3-104">Esta seção descreve como usar a API C/C++ para o Microsoft Windows HTTP Services (WinHTTP) e a interface COM exposta pelo objeto **WinHttpRequest** .</span><span class="sxs-lookup"><span data-stu-id="4ddb3-104">This section describes how to use both the C/C++ API for Microsoft Windows HTTP Services (WinHTTP) and the COM interface exposed by the **WinHttpRequest** Object.</span></span> <span data-ttu-id="4ddb3-105">Consulte [escolhendo uma interface WinHTTP](choosing-a-winhttp-interface.md) para uma comparação dessas interfaces.</span><span class="sxs-lookup"><span data-stu-id="4ddb3-105">See [Choosing a WinHTTP Interface](choosing-a-winhttp-interface.md) for a comparison of these interfaces.</span></span> <span data-ttu-id="4ddb3-106">Ele também descreve como usar as ferramentas administrativas incluídas com o WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="4ddb3-106">It also describes how to use the administrative tools included with WinHTTP.</span></span>

## <a name="how-to-topics"></a><span data-ttu-id="4ddb3-107">Tópicos de instruções</span><span class="sxs-lookup"><span data-stu-id="4ddb3-107">How-To Topics</span></span>

[<span data-ttu-id="4ddb3-108">Usando a API do WinHTTP C/C++</span><span class="sxs-lookup"><span data-stu-id="4ddb3-108">Using the WinHTTP C/C++ API</span></span>](using-the-winhttp-c-c---api.md)

-   [<span data-ttu-id="4ddb3-109">Visão geral das sessões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="4ddb3-109">WinHTTP Sessions Overview</span></span>](winhttp-sessions-overview.md)
-   [<span data-ttu-id="4ddb3-110">HINTERNET identificadores no WinHTTP</span><span class="sxs-lookup"><span data-stu-id="4ddb3-110">HINTERNET Handles in WinHTTP</span></span>](hinternet-handles-in-winhttp.md)
-   [<span data-ttu-id="4ddb3-111">URLs (Uniform Resource Locators) no WinHTTP</span><span class="sxs-lookup"><span data-stu-id="4ddb3-111">Uniform Resource Locators (URLs) in WinHTTP</span></span>](uniform-resource-locators--urls--in-winhttp.md)
-   [<span data-ttu-id="4ddb3-112">Autenticação no WinHTTP</span><span class="sxs-lookup"><span data-stu-id="4ddb3-112">Authentication in WinHTTP</span></span>](authentication-in-winhttp.md)
-   [<span data-ttu-id="4ddb3-113">Autenticação do Passport no WinHTTP</span><span class="sxs-lookup"><span data-stu-id="4ddb3-113">Passport Authentication in WinHTTP</span></span>](passport-authentication-in-winhttp.md)
-   [<span data-ttu-id="4ddb3-114">SSL no WinHTTP</span><span class="sxs-lookup"><span data-stu-id="4ddb3-114">SSL in WinHTTP</span></span>](ssl-in-winhttp.md)
-   [<span data-ttu-id="4ddb3-115">Usando o WinHTTP como um assembly lado a lado</span><span class="sxs-lookup"><span data-stu-id="4ddb3-115">Using WinHTTP as a Side-by-side Assembly</span></span>](using-winhttp-as-a-side-by-side-assembly.md)
-   [<span data-ttu-id="4ddb3-116">Tratamento de cookies no WinHTTP</span><span class="sxs-lookup"><span data-stu-id="4ddb3-116">Cookie Handling in WinHTTP</span></span>](cookie-handling-in-winhttp.md)
-   [<span data-ttu-id="4ddb3-117">Tratamento de erro no WinHTTP</span><span class="sxs-lookup"><span data-stu-id="4ddb3-117">Error Handling in WinHTTP</span></span>](error-handling-in-winhttp.md)
-   [<span data-ttu-id="4ddb3-118">Suporte ao WinHTTP AutoProxy</span><span class="sxs-lookup"><span data-stu-id="4ddb3-118">WinHTTP AutoProxy Support</span></span>](winhttp-autoproxy-support.md)

[<span data-ttu-id="4ddb3-119">Usando o objeto COM WinHttpRequest</span><span class="sxs-lookup"><span data-stu-id="4ddb3-119">Using the WinHttpRequest COM Object</span></span>](using-the-winhttprequest-com-object.md)

-   [<span data-ttu-id="4ddb3-120">Recuperando dados usando script</span><span class="sxs-lookup"><span data-stu-id="4ddb3-120">Retrieving Data Using Script</span></span>](retrieving-data-using-script.md)
-   [<span data-ttu-id="4ddb3-121">Autenticação usando script</span><span class="sxs-lookup"><span data-stu-id="4ddb3-121">Authentication Using Script</span></span>](authentication-using-script.md)

[<span data-ttu-id="4ddb3-122">Usando as ferramentas do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="4ddb3-122">Using WinHTTP Tools</span></span>](using-winhttp-tools.md)

-   [<span data-ttu-id="4ddb3-123">WinHttpCfg.exe, uma ferramenta de configuração de certificado</span><span class="sxs-lookup"><span data-stu-id="4ddb3-123">WinHttpCfg.exe, a Certificate Configuration Tool</span></span>](winhttpcertcfg-exe--a-certificate-configuration-tool.md)
-   [<span data-ttu-id="4ddb3-124">ProxyCfg.exe, uma ferramenta de configuração de proxy</span><span class="sxs-lookup"><span data-stu-id="4ddb3-124">ProxyCfg.exe, a Proxy Configuration Tool</span></span>](proxycfg-exe--a-proxy-configuration-tool.md)
-   [<span data-ttu-id="4ddb3-125">WinHttpTraceCfg, uma ferramenta de configuração de rastreamento</span><span class="sxs-lookup"><span data-stu-id="4ddb3-125">WinHttpTraceCfg, a Trace Configuration Tool</span></span>](winhttptracecfg-exe--a-trace-configuration-tool.md)

 

 



