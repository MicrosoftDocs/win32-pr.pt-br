---
title: WinINet vs. WinHTTP
description: Saiba como escolher entre WinInet e WinHTTP. Leia uma comparação de recursos e revise os tópicos relacionados.
ms.assetid: 77386b54-2c86-4a30-8c4c-88d5f15313d7
keywords:
- WinINet vs. WinHTTP
ms.topic: article
ms.date: 02/22/2019
ms.openlocfilehash: 20bd0ced1d0ea897dba05680258cae4a2b1a248b204824ded7d2ec5be30ff00b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899086"
---
# <a name="wininet-vs-winhttp"></a>WinINet vs. WinHTTP

Com algumas exceções, [WinINet](portal.md) é um superconjunto de [WinHTTP.](/windows/desktop/WinHttp/winhttp-start-page) Ao selecionar entre os dois, você deve usar o WinINet, a menos que planeje executar em um processo de serviço ou de serviço que exija representação e isolamento de sessão.

## <a name="comparison-of-features"></a>Comparação de recursos

| Recurso | Wininet | WinHTTP |
|-|-|-|
| **Cache de credenciais** Permite que todos os aplicativos integrados no Windows Internet Explorer recebam credenciais automaticamente. Ele também permite que um aplicativo em execução fora do Internet Explorer prompt/especifique as credenciais para o servidor apenas uma vez. A partir daí, as solicitações são automáticas. | sim | não |
| **Solicitação de credencial** Fornece uma API que permite que o código de chamada solicitar credenciais ao usuário. | sim | não |
| **FTP** | sim | não |
| **Suporte a RAS/Autodial** Essa é a funcionalidade herdado. Em [vez disso, use o Acesso](/windows/desktop/RRAS/portal) Remoto. | sim | não |
| **Zonas** Integração automática com Internet Explorer de segurança. | sim | não |
| **Suporte à IDNA** Suporte integrado para o IDNA RFC/Punycode. | sim | sim |
| **APIs jar de cookie** Há suporte para cookies persistentes e não persistentes. Qualquer aplicativo ou script pode usar isso para ver os mesmos cookies que o navegador. | sim | não |
| **Suporte ao IE do modo protegido** | sim | não |
| **Suporte à descompactação** Suporte para esquema de compactação gzip e deflate. | sim | sim |
| **Suporte a Upload em partes** O código do cliente deve executar o em partes. | não | sim |
| **Suporte a SOCKS v4** Não inclui v4a ou v5. | sim | não |
| **Envio e recebimento bidirecional** | não | não |
| **E/S sobressalvada** | não | não |
| **Suporte ao esquema de arquivos** Útil para scripts de proxy com um esquema de arquivo. | sim | não |
| **InternetOpenUrl** Código simplificado para abrir uma URL. | sim | não |
| **Suporte a serviços** Pode ser executado de um serviço ou de uma conta de serviço. | não | sim |
| **Isolamento de sessão** As sessões separadas não se impactam entre si. | não | sim |
| **Representação** Dá suporte a ser chamado enquanto o thread está representando um usuário diferente. | não | sim |

## <a name="related-topics"></a>Tópicos relacionados

* [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
* [Wininet](/windows/desktop/WinInet/about-wininet)