---
title: Sobre a API do servidor HTTP
description: A API do servidor HTTP fornece aos desenvolvedores uma interface de nível baixo para o lado do servidor da funcionalidade HTTP, conforme definido no RFC 2616.
ms.assetid: 74ad3a1d-cde2-4849-a412-d9d4101eaf12
keywords:
- API do servidor HTTP, visão geral
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e00fcfe6527b77be32a849f00f62222396f42b5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104365644"
---
# <a name="about-http-server-api"></a><span data-ttu-id="538dc-104">Sobre a API do servidor HTTP</span><span class="sxs-lookup"><span data-stu-id="538dc-104">About HTTP Server API</span></span>

<span data-ttu-id="538dc-105">A API do servidor HTTP fornece aos desenvolvedores uma interface de nível baixo para o lado do servidor da funcionalidade HTTP, conforme definido no [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="538dc-105">The HTTP Server API provides developers with a low-level interface to the server side of the HTTP functionality as defined in [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span> <span data-ttu-id="538dc-106">A API permite que um aplicativo receba solicitações HTTP direcionadas às URLs e envie respostas HTTP.</span><span class="sxs-lookup"><span data-stu-id="538dc-106">The API enables an application to receive HTTP requests directed to URLs and send HTTP responses.</span></span> <span data-ttu-id="538dc-107">Para enviar respostas dinâmicas, as interfaces ISAPI ou ASP.NET são recomendadas.</span><span class="sxs-lookup"><span data-stu-id="538dc-107">For sending dynamic responses, the ISAPI or ASP.NET interfaces are recommended.</span></span>

<span data-ttu-id="538dc-108">A API do servidor HTTP permite que vários aplicativos coexistam em um sistema, compartilhando a mesma porta TCP (por exemplo, a porta 80 para HTTP ou a porta 443 para HTTPS) e atendendo partes diferentes do namespace da URL.</span><span class="sxs-lookup"><span data-stu-id="538dc-108">The HTTP Server API enables multiple applications to coexist on a system, sharing the same TCP port (for example, port 80 for HTTP or port 443 for HTTPS) and serving different parts of the URL namespace.</span></span>

<span data-ttu-id="538dc-109">A API do servidor HTTP requer conhecimento da linguagem de programação C e familiaridade com a programação da API do Windows.</span><span class="sxs-lookup"><span data-stu-id="538dc-109">The HTTP Server API requires knowledge of the C programming language and a familiarity with Windows API programming.</span></span> <span data-ttu-id="538dc-110">Os aplicativos que não exigem acesso de baixo nível ao HTTP devem usar a ISAPI do IIS ou as classes de .NET Framework para soluções baseadas em HTTP.</span><span class="sxs-lookup"><span data-stu-id="538dc-110">Applications that do not require low-level access to HTTP should use the IIS ISAPI or the .NET Framework classes for HTTP-based solutions.</span></span>

 

 




