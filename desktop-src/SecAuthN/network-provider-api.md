---
description: Um provedor de rede é uma DLL que permite que o sistema operacional Windows interaja com outros tipos de redes, como Novell. É um cliente do driver WNet do Windows.
ms.assetid: d316f159-4fe3-4b78-9efc-177906875918
title: API do provedor de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc68184f60639a603614cbaf71631a2521012cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752539"
---
# <a name="network-provider-api"></a>API do provedor de rede

Um provedor de rede é uma DLL que permite que o sistema operacional Windows interaja com outros tipos de redes, como Novell. É um cliente do driver WNet do Windows. Um provedor de rede implementa ações específicas de rede, como fazer uma conexão, e expõe uma interface comum ao Windows. Essa interface é chamada de API do provedor de rede e consiste em funções implementadas pelo provedor de rede. Você pode criar uma DLL de provedor de rede para dar suporte a novos protocolos de rede.

Como cada rede expõe uma interface comum por meio de seu provedor, o Windows pode interagir com vários tipos de redes sem conhecer seus detalhes de implementação específicos da rede.

O [*roteador do provedor múltiplo*](../secgloss/m-gly.md) (MPR) trata da comunicação com todos os vários provedores de rede no sistema e apresenta uma rede integrada ao usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Provedores de rede](network-providers.md)
</dt> <dt>

[Gerenciador de Credenciais](credential-manager.md)
</dt> <dt>

[Roteador de vários provedores](multiple-provider-router.md)
</dt> <dt>

[Funções implementadas por provedores de rede](functions-implemented-by-network-providers.md)
</dt> <dt>

[API de gerenciamento de credenciais](credential-management-api.md)
</dt> <dt>

[API de notificação de conexão](connection-notification-api.md)
</dt> </dl>

 

 
