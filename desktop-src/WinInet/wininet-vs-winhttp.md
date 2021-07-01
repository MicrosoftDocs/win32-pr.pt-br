---
title: WinINet versus WinHTTP
description: Saiba como escolher entre o WinInet e o WinHTTP. Leia uma comparação dos recursos e examine os tópicos relacionados.
ms.assetid: 77386b54-2c86-4a30-8c4c-88d5f15313d7
keywords:
- WinINet versus WinHTTP
ms.topic: article
ms.date: 02/22/2019
ms.openlocfilehash: 8ced80dd048559fee483e8cf121918eed75fc462
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118791"
---
# <a name="wininet-vs-winhttp"></a>WinINet versus WinHTTP

Com algumas exceções, o [WinInet](portal.md) é um superconjunto do [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page). Ao selecionar entre os dois, você deve usar o WinINet, a menos que você planeje executar dentro de um processo de serviço ou de serviço que exija a representação e o isolamento da sessão.

## <a name="comparison-of-features"></a>Comparação de recursos

| Recurso | WinINet | WinHTTP |
|-|-|-|
| **Cache de credenciais** Permite que todos os aplicativos internos no Windows Internet Explorer obtenham credenciais automaticamente. Ele também permite que um aplicativo em execução fora do Internet Explorer solicite/especifique as credenciais para o servidor somente uma vez. A partir de então, as solicitações são automáticas. | sim | não |
| **Solicitação de credencial** Fornece uma API que permite que o código de chamada solicite as credenciais ao usuário. | sim | não |
| **FTP** | sim | não |
| **Suporte de AutoDiscagem/RAS** Essa é a funcionalidade herdada. Em vez disso, use o [acesso remoto](/windows/desktop/RRAS/portal) . | sim | não |
| **Zonas** Integração automática com as zonas de segurança do Internet Explorer. | sim | não |
| **Suporte do IDNA** Suporte integrado para IDNA RFC/Punycode. | sim | sim |
| **APIs do jar do cookie** Há suporte para cookies persistentes e não persistentes. Qualquer aplicativo ou script pode usar isso para ver os mesmos cookies que o navegador. | sim | não |
| **Suporte do modo protegido do IE** | sim | não |
| **Suporte à descompactação** Suporte para esquema de compactação Gzip e deflate. | sim | sim |
| **Suporte a carregamento em partes** O código do cliente deve executar o agrupamento. | não | sim |
| **Suporte a SOCKS v4** Não inclui V4A ou v5. | sim | não |
| **Envio e recebimento bidirecional** | não | não |
| **E/s sobreposta** | não | não |
| **Suporte a esquema de arquivo** Útil para scripts de proxy com um esquema de arquivo. | sim | não |
| **InternetOpenUrl** Código simplificado para abrir uma URL. | sim | não |
| **Suporte a serviços** Pode ser executado de um serviço ou de uma conta de serviço. | não | sim |
| **Isolamento de sessão** Sessões separadas não afetam uma à outra. | não | sim |
| **Representação** Dá suporte para chamada enquanto o thread está representando um usuário diferente. | não | sim |

## <a name="related-topics"></a>Tópicos relacionados

* [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
* [WinINet](/windows/desktop/WinInet/about-wininet)