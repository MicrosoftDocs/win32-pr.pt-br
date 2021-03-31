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
# <a name="about-wininet"></a>Sobre o WinINet

> [!NOTE]
> Para contêineres de aplicativos, desde que o Windows 10, versão 1709, HTTP/2 (consulte [RFC7540](https://tools.ietf.org/html/rfc7540)) esteja ativado por padrão.

A API (interface de programação de aplicativo) do Windows Internet (WinINet) permite que seu aplicativo interaja com protocolos FTP e HTTP para acessar recursos da Internet. À medida que os padrões evoluem, essas funções manipulam as alterações nos protocolos subjacentes, permitindo que eles mantenham o comportamento consistente.

**Windows XP e Windows Server 2003 R2 e anteriores:** Também habilitou aplicativos para interagir com o Gopher.

Para obter mais informações, consulte:

-   [WinINet versus WinHTTP](wininet-vs-winhttp.md)
-   [Identificadores de HINTERNET](appendix-a-hinternet-handles.md)
-   [Suporte para IP versão 6](ip-version-6-support.md)
-   [Codificação de conteúdo \_](content-encoding.md)
-   [Cache](caching.md)
-   [Funções comuns](common-functions.md)
-   [Sessões de FTP](ftp-sessions.md)
-   [Sessões HTTP](http-sessions.md)
-   [Cookies HTTP](http-cookies.md)
-   [Operação assíncrona](asynchronous-operation.md)
-   [Manipulando a autenticação](handling-authentication.md)
-   [Manipulando localizadores de recursos uniformes](handling-uniform-resource-locators.md)
-   [Diretriz de segurança \_](security-guidelines.md)

## <a name="internet-protocols"></a>Protocolos de Internet

Os dois protocolos de Internet primários são FTP e HTTP. Para obter mais informações sobre esses protocolos, consulte os documentos de RFC (solicitação de comentários) para FTP e HTTP:

-   [RFC 959](https://www.ietf.org/rfc/rfc0959.txt), *protocolo FTP (FTP)*.
-   [RFC 1945](ftp://ftp.isi.edu/in-notes/rfc1945.txt), *protocolo de transferência de hipertexto-HTTP/1.0*.
-   [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), *protocolo de transferência de hipertexto-HTTP/1.1*.

> [!NOTE]  
> (Esses recursos podem não estar disponíveis em alguns idiomas e países.)

**Windows XP e Windows Server 2003 R2 e anteriores:** O protocolo Gopher também tinha suporte. Consulte [RFC 1436](https://www.ietf.org/rfc/rfc1436.txt), *o protocolo Gopher da Internet*.
