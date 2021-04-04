---
title: Sobre o WinINet
description: A API (interface de programação de aplicativo) do Windows Internet (WinINet) permite que seu aplicativo interaja com protocolos FTP e HTTP para acessar recursos da Internet.
ms.assetid: 0a06f2af-957a-4dff-a8cc-187370181b5c
keywords:
- Sobre o WinINet WinINet
- WinINet WinINet, sobre
- WinINet WinINet, página inicial
- Windows Internet WinINet
- Internet, Windows Internet WinINet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4513e5c3912a483fd4dbef96f452c5712717c8a5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103917028"
---
# <a name="about-wininet"></a><span data-ttu-id="aba98-108">Sobre o WinINet</span><span class="sxs-lookup"><span data-stu-id="aba98-108">About WinINet</span></span>

> [!NOTE]
> <span data-ttu-id="aba98-109">Para contêineres de aplicativos, desde que o Windows 10, versão 1709, HTTP/2 (consulte [RFC7540](https://tools.ietf.org/html/rfc7540)) esteja ativado por padrão.</span><span class="sxs-lookup"><span data-stu-id="aba98-109">For app containers since Windows 10, version 1709, HTTP/2 (see [RFC7540](https://tools.ietf.org/html/rfc7540)) is on by default.</span></span>

<span data-ttu-id="aba98-110">A API (interface de programação de aplicativo) do Windows Internet (WinINet) permite que seu aplicativo interaja com protocolos FTP e HTTP para acessar recursos da Internet.</span><span class="sxs-lookup"><span data-stu-id="aba98-110">The Windows Internet (WinINet) application programming interface (API) enables your application to interact with FTP and HTTP protocols to access Internet resources.</span></span> <span data-ttu-id="aba98-111">À medida que os padrões evoluem, essas funções manipulam as alterações nos protocolos subjacentes, permitindo que eles mantenham o comportamento consistente.</span><span class="sxs-lookup"><span data-stu-id="aba98-111">As standards evolve, these functions handle the changes in underlying protocols, enabling them to maintain consistent behavior.</span></span>

<span data-ttu-id="aba98-112">**Windows XP e Windows Server 2003 R2 e anteriores:** Também habilitou aplicativos para interagir com o Gopher.</span><span class="sxs-lookup"><span data-stu-id="aba98-112">**Windows XP and Windows Server 2003 R2 and earlier:** Also enabled applications to interact with Gopher.</span></span>

<span data-ttu-id="aba98-113">Para obter mais informações, consulte:</span><span class="sxs-lookup"><span data-stu-id="aba98-113">For more information, see:</span></span>

-   [<span data-ttu-id="aba98-114">WinINet versus WinHTTP</span><span class="sxs-lookup"><span data-stu-id="aba98-114">WinINet vs. WinHTTP</span></span>](wininet-vs-winhttp.md)
-   [<span data-ttu-id="aba98-115">Identificadores de HINTERNET</span><span class="sxs-lookup"><span data-stu-id="aba98-115">HINTERNET Handles</span></span>](appendix-a-hinternet-handles.md)
-   [<span data-ttu-id="aba98-116">Suporte para IP versão 6</span><span class="sxs-lookup"><span data-stu-id="aba98-116">IP Version 6 Support</span></span>](ip-version-6-support.md)
-   [<span data-ttu-id="aba98-117">Codificação de conteúdo \_</span><span class="sxs-lookup"><span data-stu-id="aba98-117">Content\_Encoding</span></span>](content-encoding.md)
-   [<span data-ttu-id="aba98-118">Cache</span><span class="sxs-lookup"><span data-stu-id="aba98-118">Caching</span></span>](caching.md)
-   [<span data-ttu-id="aba98-119">Funções comuns</span><span class="sxs-lookup"><span data-stu-id="aba98-119">Common Functions</span></span>](common-functions.md)
-   [<span data-ttu-id="aba98-120">Sessões de FTP</span><span class="sxs-lookup"><span data-stu-id="aba98-120">FTP Sessions</span></span>](ftp-sessions.md)
-   [<span data-ttu-id="aba98-121">Sessões HTTP</span><span class="sxs-lookup"><span data-stu-id="aba98-121">HTTP Sessions</span></span>](http-sessions.md)
-   [<span data-ttu-id="aba98-122">Cookies HTTP</span><span class="sxs-lookup"><span data-stu-id="aba98-122">HTTP Cookies</span></span>](http-cookies.md)
-   [<span data-ttu-id="aba98-123">Operação assíncrona</span><span class="sxs-lookup"><span data-stu-id="aba98-123">Asynchronous Operation</span></span>](asynchronous-operation.md)
-   [<span data-ttu-id="aba98-124">Manipulando a autenticação</span><span class="sxs-lookup"><span data-stu-id="aba98-124">Handling Authentication</span></span>](handling-authentication.md)
-   [<span data-ttu-id="aba98-125">Manipulando localizadores de recursos uniformes</span><span class="sxs-lookup"><span data-stu-id="aba98-125">Handling Uniform Resource Locators</span></span>](handling-uniform-resource-locators.md)
-   [<span data-ttu-id="aba98-126">Diretriz de segurança \_</span><span class="sxs-lookup"><span data-stu-id="aba98-126">Security\_Guideline</span></span>](security-guidelines.md)

## <a name="internet-protocols"></a><span data-ttu-id="aba98-127">Protocolos de Internet</span><span class="sxs-lookup"><span data-stu-id="aba98-127">Internet Protocols</span></span>

<span data-ttu-id="aba98-128">Os dois protocolos de Internet primários são FTP e HTTP.</span><span class="sxs-lookup"><span data-stu-id="aba98-128">The two primary Internet protocols are FTP and HTTP.</span></span> <span data-ttu-id="aba98-129">Para obter mais informações sobre esses protocolos, consulte os documentos de RFC (solicitação de comentários) para FTP e HTTP:</span><span class="sxs-lookup"><span data-stu-id="aba98-129">For more information about these protocols, see the Request For Comments (RFC) documents for FTP and HTTP:</span></span>

-   <span data-ttu-id="aba98-130">[RFC 959](https://www.ietf.org/rfc/rfc0959.txt), *protocolo FTP (FTP)*.</span><span class="sxs-lookup"><span data-stu-id="aba98-130">[RFC 959](https://www.ietf.org/rfc/rfc0959.txt), *File Transfer Protocol (FTP)*.</span></span>
-   <span data-ttu-id="aba98-131">[RFC 1945](ftp://ftp.isi.edu/in-notes/rfc1945.txt), *protocolo de transferência de hipertexto-HTTP/1.0*.</span><span class="sxs-lookup"><span data-stu-id="aba98-131">[RFC 1945](ftp://ftp.isi.edu/in-notes/rfc1945.txt), *Hypertext Transfer Protocol - HTTP/1.0*.</span></span>
-   <span data-ttu-id="aba98-132">[RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), *protocolo de transferência de hipertexto-HTTP/1.1*.</span><span class="sxs-lookup"><span data-stu-id="aba98-132">[RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), *Hypertext Transfer Protocol - HTTP/1.1*.</span></span>

> [!NOTE]  
> <span data-ttu-id="aba98-133">(Esses recursos podem não estar disponíveis em alguns idiomas e países.)</span><span class="sxs-lookup"><span data-stu-id="aba98-133">(These resources may not be available in some languages and countries.)</span></span>

<span data-ttu-id="aba98-134">**Windows XP e Windows Server 2003 R2 e anteriores:** O protocolo Gopher também tinha suporte.</span><span class="sxs-lookup"><span data-stu-id="aba98-134">**Windows XP and Windows Server 2003 R2 and earlier:** The Gopher protocol was also supported.</span></span> <span data-ttu-id="aba98-135">Consulte [RFC 1436](https://www.ietf.org/rfc/rfc1436.txt), *o protocolo Gopher da Internet*.</span><span class="sxs-lookup"><span data-stu-id="aba98-135">See [RFC 1436](https://www.ietf.org/rfc/rfc1436.txt), *The Internet Gopher Protocol*.</span></span>
