---
description: Um provedor de rede é uma DLL que dá suporte a um protocolo de rede específico.
ms.assetid: ebd47c1b-f427-4fa1-a2ec-1e73be297bef
title: Provedores de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5443ec7366b0f7ad74037f868e1ca4a93dbd913d0c13fda46c7b9fdabd0e0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786594"
---
# <a name="network-providers"></a>Provedores de rede

Um provedor de rede é uma DLL que dá suporte a um protocolo de rede específico. Ele também implementa a [API do provedor de rede](network-provider-api.md). isso permite que ele interaja com o sistema operacional Windows para receber solicitações de rede padrão, como solicitações de conexão ou desconexão. Para lidar com essas solicitações, o provedor de rede chama a API específica da rede apropriada ao protocolo de rede que o provedor de rede suporta. Em outras palavras, o provedor de rede encapsula a funcionalidade específica da rede em uma DLL, que expõe uma interface padrão para Windows.

usando provedores de rede, Windows pode dar suporte a vários tipos diferentes de protocolos de rede sem precisar saber os detalhes específicos da rede de cada rede. Isso é essencial porque novos protocolos de rede estão sendo desenvolvidos o tempo todo. Com os provedores de rede, o suporte a um novo protocolo simplesmente requer a criação e a instalação de um novo provedor de rede.

Para obter informações sobre as funções e estruturas do provedor de rede, consulte os seguintes tópicos:

-   [Funções de provedor de rede](authentication-functions.md)
-   [Estruturas de provedor de rede](authentication-structures.md)

 

 



