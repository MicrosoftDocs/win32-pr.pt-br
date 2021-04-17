---
description: O Microsoft Windows HTTP Services (WinHTTP) fornece uma interface de alto nível com suporte de servidor para os protocolos de Internet HTTP/2 e 1,1.
ms.assetid: 8337f699-3ec0-4397-acc2-6dc813f7542d
title: Sobre o WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 150c829410a1601a3ede7f115f4594276af7fead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784052"
---
# <a name="about-winhttp"></a>Sobre o WinHTTP

> [!NOTE]
> Para contêineres de aplicativos e serviços do sistema desde que o Windows 10, versão 1709, HTTP/2 (consulte [RFC7540](https://tools.ietf.org/html/rfc7540)) esteja ativado por padrão.

O Microsoft Windows HTTP Services (WinHTTP) fornece uma interface de alto nível com suporte de servidor para os protocolos de Internet HTTP/2 e 1,1. O WinHTTP foi projetado para ser usado principalmente em cenários baseados em servidor por aplicativos de servidor que se comunicam com servidores HTTP.

O [WinInet](/windows/desktop/WinInet/portal) foi projetado como uma plataforma de cliente http para aplicativos de área de trabalho interativa. O WinINet exibe uma interface do usuário para algumas operações, como coletar credenciais do usuário. No entanto, o WinHTTP manipula essas operações de forma programática. Aplicativos de servidor que exigem serviços de cliente HTTP devem usar WinHTTP em vez de WinINet. Para obter mais informações, consulte [portando aplicativos WinInet para WinHTTP](porting-wininet-applications-to-winhttp.md).

O WinHTTP também foi projetado para uso em serviços do sistema e aplicativos cliente baseados em HTTP. No entanto, aplicativos de usuário único que exigem funcionalidade de protocolo FTP, persistência de cookie, cache, tratamento automático de caixa de diálogo de credencial, compatibilidade do Internet Explorer ou suporte a plataformas de nível inferior devem considerar o uso do [WinInet](/windows/desktop/WinInet/portal).

Essa interface pode ser acessada do C/C++ usando a API (interface de programação de aplicativo) do WinHTTP ou usando as interfaces [**IWinHttpRequest**](iwinhttprequest-interface.md) e [**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md) . O WinHTTP também pode ser acessado do script e do Microsoft Visual Basic por meio do objeto WinHTTP. Para obter mais informações e descrições das funções individuais, consulte a referência das funções do WinHTTP para o idioma específico.

A partir do Windows 8, o WinHTTP fornece APIs para habilitar conexões usando o [protocolo WebSocket](https://tools.ietf.org/html/rfc6455)l, como [**WinHttpWebSocketSend**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend) e [**WinHttpWebSocketReceive**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive).

> [!Caution]  
> O WinHTTP não é reentrante, exceto durante o retorno de chamada de conclusão assíncrona. Ou seja, enquanto um thread tem uma chamada pendente para uma das funções do WinHTTP, como WinHttpSendRequest, WinHttpReceiveResponse, WinHttpQueryDataAvailable, WinHttpSendData ou WinHttpWriteData, ele nunca deve chamar o WinHTTP uma segunda vez até que a primeira chamada seja concluída. Um cenário sob o qual uma segunda chamada pode ocorrer é o seguinte: se um aplicativo enfileirar uma APC (chamada de procedimento assíncrono) para o thread que chama o WinHTTP e se o WinHTTP executar uma espera de alerta internamente, a APC poderá ser executada. Se a rotina da APC ocorrer também chamar o WinHTTP, ela reinserirá a API do WinHTTP e o estado interno do WinHTTP poderá ser corrompido.

## <a name="winhttp-51-features"></a>Recursos do WinHTTP 5,1

Os seguintes recursos foram adicionados na versão 5,1 do WinHTTP:

-   Suporte a IPv6.
-   Recursos de AutoProxy.
-   Protocolo HTTP/1.0, incluindo suporte para conexões Keep Alive (persistentes) e cookies de sessão.
-   Suporte para transferência em partes de HTTP/1.1 para respostas HTTP.
-   Pool de Keep-Alive de conexões anônimas entre sessões.
-   Funcionalidade de protocolo SSL (SSL), incluindo certificados de cliente. Os protocolos SSL com suporte incluem o seguinte: SSL 2,0, SSL 3,0 e TLS (Transport Layer Security) 1,0.
-   Suporte para autenticação de servidor e proxy, incluindo suporte integrado para Microsoft Passport 1,4 e o pacote Negotiate/ [Kerberos](../com/kerberos-v5-protocol.md) .
-   Manipulação automática de redirecionamentos, a menos que suprimido.
-   Interface programável, além da API.
-   Utilitário de rastreamento para ajudar a solucionar problemas.

Não há suporte para vários recursos do [WinInet](/windows/desktop/WinInet/portal) no WinHTTP, incluindo cache de URL e cookies persistentes, AutoProxy, discagem automática, suporte offline e protocolo FTP (FTP).

Para obter mais informações sobre as alterações introduzidas na versão 5,1, consulte [What ' s New in WinHTTP 5,1](what-s-new-in-winhttp-5-1.md).

## <a name="getting-started-with-winhttp"></a>Introdução com WinHTTP

Para obter mais informações sobre o WinHTTP, consulte os tópicos a seguir.

* O [WinInet versus o WinHTTP](/windows/desktop/wininet/wininet-vs-winhttp) compara as duas tecnologias para acessar o http.
* [As versões WinHTTP](winhttp-versions.md) descrevem o histórico de versão do WinHTTP.
* [O que há de novo no winhttp 5,1](what-s-new-in-winhttp-5-1.md) descreve as alterações e os novos recursos no WinHTTP 5,1.
* A [terminologia de rede](network-terminology.md) descreve os conceitos úteis e a terminologia relacionada à rede em geral e o protocolo http em particular.
* A [escolha de uma interface WinHTTP](choosing-a-winhttp-interface.md) descreve a API C/C++ e a interface com para WinHTTP.
* As [considerações de segurança do WinHTTP](winhttp-security-considerations.md) descrevem os problemas de segurança que devem ser considerados ao usar o WinHTTP.
* [Portar aplicativos WinInet para o WinHTTP](porting-wininet-applications-to-winhttp.md) descreve como modificar seus aplicativos [WinInet](/windows/desktop/WinInet/portal) existentes para usar a API do WinHTTP.
