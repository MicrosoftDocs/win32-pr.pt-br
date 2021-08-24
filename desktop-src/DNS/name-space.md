---
title: Namespace
description: Um namespace é um contexto no qual os nomes de todos os objetos devem ser resolvidos inequivocamente.
ms.assetid: 7731f6b5-1efa-43bc-bd31-9b5183ec90dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce9119b49cde888cb51f65e6e6b677fb364d640e1b78fe48c739b7c1206936d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692196"
---
# <a name="namespace"></a>Namespace

Um namespace é um contexto no qual os nomes de todos os objetos devem ser resolvidos inequivocamente. Por exemplo, a Internet é um único espaço de nome DNS, no qual todos os dispositivos de rede com um nome DNS podem ser resolvidos para um endereço específico (por exemplo, `www.microsoft.com` resolve para 207.46.131.13).

## <a name="flat-namespace"></a>Namespace simples

Um namespace pode ser simples ou hierárquico. Um namespace simples não dimensiona bem porque pode aumentar muito para que todos os nomes disponíveis sejam usados. Depois que um nome é usado mais de uma vez em um namespace, o namespace viola o requisito de resolução inequívoca.

## <a name="hierarchical-namespace"></a>Namespace hierárquico

Um namespace hierárquico é dividido em áreas diferentes, que podem ser pensados como subnamespaces. Cada área é seu próprio subnamespace no namespace geral. Portanto, cada objeto deve ter um nome exclusivo somente dentro de seu subnamespace para ter um nome com resolução inequívoca na hierarquia de namespace. Os namespaces hierárquicos, em seguida, podem ser dimensionados para redes extremamente grandes &mdash; à medida que você adiciona mais objetos ao espaço de nome geral, você precisa encontrar nomes exclusivos para eles dentro de apenas o subnamespace ao qual eles pertencem.

Todos os namespaces DNS são hierárquicos. Os subnamespaces no namespace hierárquico do DNS são chamados de *domínios*. O nome exclusivo de um computador em um domínio é chamado de *nome distinto relativo*. Computadores com o mesmo nome distinto relativo podem existir em diferentes subnamespaces (domínios) da hierarquia de namespace, pois eles podem ser totalmente resolvidos para um objeto exclusivo dentro de toda a hierarquia DNS, usando um FQDN (nome de domínio totalmente qualificado). Por exemplo, você poderia ter um servidor chamado *Server1* no domínio *widgets.Microsoft.com* (o namespace *widgets.Microsoft.com* ) e poderia ter *Server1* no namespace *gadgets.widgets.Microsoft.com* . Como estão em subnamespaces diferentes no namespace hierárquico, eles podem ser resolvidos para FQDNs diferentes &mdash; *server1.widgets.microsoft.com* e *Server1.gadgets.widgets.Microsoft.com*.
