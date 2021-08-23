---
description: Um provedor de rede é uma DLL que permite que Windows sistema operacional interaja com outros tipos de redes, como a Novell. Ele é um cliente do driver Windows WNet.
ms.assetid: d316f159-4fe3-4b78-9efc-177906875918
title: API do Provedor de Rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 359104da668ee3dbe63efa538b58f224f93f52575ed20992fced0e10517fe5f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921322"
---
# <a name="network-provider-api"></a>API do Provedor de Rede

Um provedor de rede é uma DLL que permite que Windows sistema operacional interaja com outros tipos de redes, como a Novell. Ele é um cliente do driver Windows WNet. Um provedor de rede implementa ações específicas de rede, como fazer uma conexão, e expõe uma interface comum para Windows. Essa interface é chamada de API do Provedor de Rede e consiste em funções implementadas pelo provedor de rede. Você pode criar uma DLL de provedor de rede para dar suporte a novos protocolos de rede.

Como cada rede expõe uma interface comum por meio de seu provedor, Windows pode interagir com vários tipos de redes sem saber os detalhes de implementação específicos da rede.

A [*MPR*](../secgloss/m-gly.md) (Roteador Múltiplo Provedor) lida com a comunicação com todos os vários provedores de rede no sistema e apresenta uma rede integrada ao usuário.

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

[Credenciais API de Gerenciamento](credential-management-api.md)
</dt> <dt>

[Conexão API de Notificação](connection-notification-api.md)
</dt> </dl>

 

 
