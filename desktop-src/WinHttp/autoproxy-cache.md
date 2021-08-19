---
description: AutoProxy Cache
ms.assetid: 087104e8-ab38-4ba4-be70-23a5ea2bb130
title: AutoProxy Cache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d494f1491dd52484a893dbab601ed4870f03badf5f849dca413f9554a8493e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614176"
---
# <a name="autoproxy-cache"></a>AutoProxy Cache

A [**função WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) executa a procura automática por solicitação para a URL especificada. Se vários proxies são retornados, os aplicativos cliente devem testar cada proxy antes de enviar a solicitação (para obter mais informações, consulte a seção Only One Proxy Server is Atualmente [Supported](autoproxy-issues-in-winhttp.md) issues in AutoProxy Issues in WinHTTP). As informações neste tópico se aplica a chamadas para **WinHttpGetProxyForUrl** quando o cliente especifica a descoberta automática de proxy.

[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) opcionalmente localiza a URL de reprodução automática e baixa o script autoproxy desse site. O WinHttp usa o script de reprodução automática para localizar os servidores proxy. A URL de reprodução automática e o script autoproxy são armazenados em cache para a sessão especificada. Apenas uma URL autoproxy e script são armazenados em cache para cada sessão. Normalmente, o script autoproxy e a URL são armazenados em cache até que o endereço IP associado ao computador mude. Se um novo endereço IP for detectado durante uma chamada para **WinHttpGetProxyForUrl**, a chamada tentará localizar uma nova URL de reprodução automática e um script e armazenará os resultados em cache. Somente um usuário deve ser permitido por sessão, para que os dados armazenados em cache não sejam compartilhados com outros usuários no computador. Para obter mais informações, consulte [Visão geral das sessões do WinHTTP.](winhttp-sessions-overview.md)

Se o serviço fora do processo estiver ativo quando [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) for chamado, a URL autoproxy armazenada em cache e o script estarão disponíveis para todo o computador. No entanto, se o serviço fora do processo for usado e o sinalizador **fAutoLogonIfChallenged** na estrutura *pAutoProxyOptions* for true, a URL autoproxy e o script não serão armazenados em cache. Portanto, chamar **WinHttpGetProxyForUrl** com o membro **fAutoLogonIfChallenged** definido como **TRUE** resulta em operações de sobrecarga adicionais que podem afetar o desempenho. As etapas a seguir podem ser usadas para melhorar o desempenho.

**Para melhorar o desempenho**

1.  Chame [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) com o parâmetro fAutoLogonIfChallenged definido como **false.** A URL autoproxy e o script são armazenados em cache para chamadas futuras para **WinHttpGetProxyForUrl.**
2.  Se a Etapa 1 falhar, com **ERRO \_ WINHTTP \_ LOGIN \_ FAILURE**, chame [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) com **o membro fAutoLogonIfChallenged** definido como **TRUE.**

 

 



