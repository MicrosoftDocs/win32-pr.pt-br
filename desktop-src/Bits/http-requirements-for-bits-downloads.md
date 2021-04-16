---
title: Requisitos de HTTP para downloads de BITS
description: O BITS dá suporte a downloads e uploads de HTTP e HTTPS e requer que o servidor ofereça suporte ao protocolo HTTP/1.1.
ms.assetid: 35af422b-62e4-41fd-8890-579ccf016c83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d130ab3e527b62f34f48e6df4695bf75f63dcd2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453527"
---
# <a name="http-requirements-for-bits-downloads"></a><span data-ttu-id="82ee1-103">Requisitos de HTTP para downloads de BITS</span><span class="sxs-lookup"><span data-stu-id="82ee1-103">HTTP Requirements for BITS Downloads</span></span>

<span data-ttu-id="82ee1-104">O BITS dá suporte a downloads e uploads de HTTP e HTTPS e requer que o servidor ofereça suporte ao protocolo HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="82ee1-104">BITS supports HTTP and HTTPS downloads and uploads and requires that the server supports the HTTP/1.1 protocol.</span></span> <span data-ttu-id="82ee1-105">Para downloads, o método **Head** do servidor http deve retornar o tamanho do arquivo e seu método **Get** deve oferecer suporte aos cabeçalhos Content-Range e Content-Length.</span><span class="sxs-lookup"><span data-stu-id="82ee1-105">For downloads, the HTTP server's **Head** method must return the file size and its **Get** method must support the Content-Range and Content-Length headers.</span></span> <span data-ttu-id="82ee1-106">Como resultado, o BITS transfere apenas o conteúdo do arquivo estático e gera um erro se você tentar transferir conteúdo dinâmico, a menos que o script ASP, ISAPI ou CGI dê suporte aos cabeçalhos Content-Range e Content-Length.</span><span class="sxs-lookup"><span data-stu-id="82ee1-106">As a result, BITS only transfers static file content and generates an error if you try to transfer dynamic content, unless the ASP, ISAPI, or CGI script supports the Content-Range and Content-Length headers.</span></span>

<span data-ttu-id="82ee1-107">O BITS pode usar um servidor HTTP/1.0 contanto que atenda aos requisitos de método **Head** e **Get** .</span><span class="sxs-lookup"><span data-stu-id="82ee1-107">BITS can use an HTTP/1.0 server as long as it meets the **Head** and **Get** method requirements.</span></span>

<span data-ttu-id="82ee1-108">Para dar suporte ao download de intervalos de um arquivo, o servidor deve dar suporte aos seguintes requisitos:</span><span class="sxs-lookup"><span data-stu-id="82ee1-108">To support downloading ranges of a file, the server must support the following requirements:</span></span>

-   <span data-ttu-id="82ee1-109">Permitir que os cabeçalhos MIME incluam o intervalo de conteúdo padrão e os cabeçalhos de tipo de conteúdo, mais um máximo de 180 bytes de outros cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="82ee1-109">Allow MIME headers to include the standard Content-Range and Content-Type headers, plus a maximum of 180 bytes of other headers.</span></span>
-   <span data-ttu-id="82ee1-110">Permita um máximo de dois CR/LFs entre os cabeçalhos HTTP e a primeira cadeia de caracteres de limite.</span><span class="sxs-lookup"><span data-stu-id="82ee1-110">Allow a maximum of two CR/LFs between the HTTP headers and the first boundary string.</span></span>

 

 




