---
title: Propriedade de tempos limite do servidor
description: .
ms.assetid: 5525c226-3786-41c4-86a2-3e077682313d
keywords:
- Propriedade de tempos limite do servidor HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8356c1e0d0e9eea2e5db9bf43882f26f9d7e3ddb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364159"
---
# <a name="server-timeouts-property"></a>Propriedade de tempos limite do servidor

A API do servidor HTTP permite que os aplicativos definam os limites de tempo limite de conexão do servidor em uma sessão de servidor ou um grupo de URLs. A propriedade de tempos limite de HTTP é usada para definir todos os tempos limite em uma base específica do aplicativo. Os temporizadores **IdleConnection** e **HeaderWait** também podem ser configurados para toda a API do servidor http. Quando os temporizadores são configurados para toda a API do servidor HTTP, eles se aplicam a todos os aplicativos de API do servidor HTTP no computador e as configurações são mantidas quando o serviço é reiniciado.

Para obter mais informações sobre como configurar temporizadores, consulte [Configurando os tempos limite específicos do aplicativo](configuring-the-application-specific-timeouts.md).

Quando os temporizadores não estão configurados para um grupo de URLs ou sessão de servidor, as configurações padrão da API do servidor HTTP se aplicam.

A ordem de imposição de tempo limite é a seguinte:

1.  Os padrões de toda a API do servidor HTTP se aplicam a todos os aplicativos de API do servidor HTTP no computador.
2.  Os tempos limite da sessão do servidor substituem as configurações de toda a API do servidor HTTP, quando definidas.
3.  As configurações do grupo de URLs substituem as configurações de sessão do servidor, quando definidas.

A tabela a seguir lista os limites de tempo limite de conexão padrão



| Temporizador           | Definição                                                                                                        | Padrão de API do servidor HTTP | Configurável como toda a API do servidor HTTP | Configurável como específico do aplicativo |
|-----------------|-------------------------------------------------------------------------------------------------------------------|-------------------------|--------------------------------------|--------------------------------------|
| IdleConnection  | A conexão expirou enquanto permanece ociosa.                                                                        | 120 s                 | Sim                                  | Limitado                              |
| HeaderWait      | A conexão expirou enquanto aguardava a API do servidor HTTP analisar o cabeçalho.                                 | 120 s                 | Sim                                  | Limitado                              |
| EntityBody      | A conexão expirou enquanto aguardava a chegada do corpo da entidade de solicitação.                                       | 120 s                 | Não                                   | Sim                                  |
| DrainEntityBody | A conexão expirou enquanto aguardava a API do servidor HTTP drenar o corpo da entidade em uma conexão Keep-Alive. | 120 s                 | Não                                   | Sim                                  |
| MinSendRate     | A conexão expirou porque a taxa de envio da resposta foi mais lenta do que o padrão de 150 bytes/s.               | 150 s                 | Não                                   | Sim                                  |
| Fila de Solicitação    | A conexão expirou porque a solicitação permaneceu na fila de solicitações antes de o aplicativo ter sido coletada.     | 120 bytes/s           | Não                                   | Sim                                  |



 

 

 




