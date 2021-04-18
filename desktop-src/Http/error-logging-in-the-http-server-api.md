---
title: Registro de erros na API de servidor HTTP
description: Alguns tipos de erros são tratados pela API do servidor HTTP em vez de serem passados de volta para um aplicativo para manipulação, porque a frequência desses erros poderia, de outra forma, inundar um log de eventos ou um manipulador de aplicativos.
ms.assetid: b919a718-e20b-4f34-a02e-bc028f8c32c7
keywords:
- API do servidor HTTP, log de erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d988d87a65c914625623c3f55d33a7f8cc9a4f94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105792532"
---
# <a name="error-logging-in-the-http-server-api"></a><span data-ttu-id="4aa44-104">Registro de erros na API de servidor HTTP</span><span class="sxs-lookup"><span data-stu-id="4aa44-104">Error Logging in the HTTP Server API</span></span>

<span data-ttu-id="4aa44-105">Alguns tipos de erros são tratados pela API do servidor HTTP em vez de serem passados de volta para um aplicativo para manipulação, porque a frequência desses erros poderia, de outra forma, inundar um log de eventos ou um manipulador de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="4aa44-105">Some kinds of errors are handled by the HTTP Server API rather than being passed back to an application for handling, because the frequency of such errors could otherwise flood an event log or application handler.</span></span>

<span data-ttu-id="4aa44-106">Os três tópicos a seguir descrevem os diferentes aspectos do log de erros da API do servidor HTTP:</span><span class="sxs-lookup"><span data-stu-id="4aa44-106">The following three topics describe the different aspects of the HTTP Server API error logging:</span></span>

-   <span data-ttu-id="4aa44-107">[Configuração](configuring-http-server-api-error-logging.md) do As configurações do registro controlam se a API do servidor HTTP registra erros, o tamanho máximo permitido de arquivos de log e onde os arquivos de log são salvos.</span><span class="sxs-lookup"><span data-stu-id="4aa44-107">[Configuration](configuring-http-server-api-error-logging.md) Registry settings control whether the HTTP Server API logs errors, the maximum allowable size of log files, and where log files are saved.</span></span>
-   <span data-ttu-id="4aa44-108">[Formato do arquivo de log](format-of-the-http-server-api-error-logs.md) A API do servidor HTTP cria arquivos de log que estão em conformidade com as convenções de arquivo de log World Wide Web Consortium (W3C) e podem ser analisadas usando ferramentas padrão.</span><span class="sxs-lookup"><span data-stu-id="4aa44-108">[Log File Format](format-of-the-http-server-api-error-logs.md) The HTTP Server API creates log files that comply with the World Wide Web Consortium (W3C) log file conventions, and can be parsed by using standard tools.</span></span> <span data-ttu-id="4aa44-109">No entanto, diferentemente dos arquivos de log do W3C, os arquivos de log da API do servidor HTTP não contêm nomes das colunas.</span><span class="sxs-lookup"><span data-stu-id="4aa44-109">However, unlike W3C log files, HTTP Server API log files do not contain names of the columns.</span></span>
-   <span data-ttu-id="4aa44-110">[Tipos de erros registrados](types-of-errors-logged-by-the-http-server-api.md) A API do servidor HTTP registra uma variedade de erros comuns.</span><span class="sxs-lookup"><span data-stu-id="4aa44-110">[Types of Errors Logged](types-of-errors-logged-by-the-http-server-api.md) The HTTP Server API logs a variety of common errors.</span></span>

 

 




