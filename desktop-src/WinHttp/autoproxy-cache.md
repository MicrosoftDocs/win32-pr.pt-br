---
description: Cache de AutoProxy
ms.assetid: 087104e8-ab38-4ba4-be70-23a5ea2bb130
title: Cache de AutoProxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0492bec116bad8a82da0e961cf6d851d27c787
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105808259"
---
# <a name="autoproxy-cache"></a>Cache de AutoProxy

A função [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) executa a pesquisa de AutoProxy em uma base por solicitação para a URL especificada. Se vários proxies forem retornados, os aplicativos cliente devem testar cada proxy antes de enviar a solicitação (para obter mais informações, consulte a seção [somente um servidor proxy tem suporte no momento](autoproxy-issues-in-winhttp.md) em problemas de AutoProxy no WinHTTP). As informações neste tópico se aplicam a chamadas para **WinHttpGetProxyForUrl** quando o cliente especifica a descoberta de proxy automática.

[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) opcionalmente localiza a URL de AutoProxy e baixa o script de AutoProxy desse site. O WinHttp usa o script AutoProxy para localizar os servidores proxy. A URL do AutoProxy e o script de AutoProxy são armazenados em cache para a sessão especificada. Somente uma URL e um script de AutoProxy são armazenados em cache para cada sessão. Normalmente, o script e a URL de AutoProxy são armazenados em cache até que o endereço IP associado ao computador seja alterado. Se um novo endereço IP for detectado durante uma chamada para **WinHttpGetProxyForUrl**, a chamada tentará localizar uma nova URL e um script de AutoProxy e armazenar em cache os resultados. Somente um usuário deve ser permitido por sessão, para que os dados armazenados em cache não sejam compartilhados com outros usuários no computador. Para obter mais informações, consulte [visão geral das sessões do WinHTTP](winhttp-sessions-overview.md).

Se o serviço fora do processo estiver ativo quando [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) for chamado, a URL e o script do AutoProxy armazenados em cache estarão disponíveis para todo o computador. No entanto, se o serviço fora do processo for usado e o sinalizador **fAutoLogonIfChallenged** na estrutura *pAutoProxyOptions* for true, a URL e o script do AutoProxy não serão armazenados em cache. Portanto, chamar **WinHttpGetProxyForUrl** com o membro **FAutoLogonIfChallenged** definido como **true** resulta em operações de sobrecarga adicionais que podem afetar o desempenho. As etapas a seguir podem ser usadas para melhorar o desempenho.

**Para melhorar o desempenho**

1.  Chame [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) com o parâmetro fAutoLogonIfChallenged definido como **false**. A URL e o script do AutoProxy são armazenados em cache para chamadas futuras para **WinHttpGetProxyForUrl**.
2.  Se a etapa 1 falhar, com **erro de \_ \_ \_ falha de logon WinHTTP**, chame [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) com o membro **fAutoLogonIfChallenged** definido como **true**.

 

 



