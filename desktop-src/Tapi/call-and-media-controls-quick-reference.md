---
description: A tabela a seguir lista as interfaces COM da TAPI versão 3 por categoria em ordem de importância.
ms.assetid: fafb6d6e-934e-4942-8b90-dacb7ba09752
title: Referência rápida de controles de mídia e chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ed3105612205d6d516b8d0c5e4f0a7bf9719b3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105760170"
---
# <a name="call-and-media-controls-quick-reference"></a>Referência rápida de controles de mídia e chamada

\[ As [interfaces IPConf MSP](ipconf-msp-interfaces.md) não estão disponíveis para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A tabela a seguir lista as interfaces COM da TAPI versão 3 por categoria em ordem de importância. As interfaces são agrupadas de acordo com os cinco objetos básicos de controle de chamada da TAPI 3: TAPI, endereço, terminal, Call e CallHub. As interfaces restantes são agrupadas de acordo com as interfaces de distribuição automática de chamada (AD), que fornecem funcionalidade de centro de chamadas; interfaces do enumerador e objetos autônomos.



| Agrupamentos de interface                                          | Descrição                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interfaces de objeto TAPI](tapi-object-interfaces.md)         | O objeto TAPI é o objeto principal para a TAPI 3.                                                                                                                                                                                                              |
| [Interfaces de objeto de endereço](address-object-interfaces.md)   | O objeto address representa uma entidade que pode fazer ou receber chamadas. As interfaces e os métodos associados permitem que um aplicativo obtenha e defina informações relativas ao endereço, como se ele tem suporte à ID do chamador.                             |
| [Interfaces de objeto de terminal](terminal-object-interfaces.md) | O objeto terminal representa o coletor ou a origem no término ou ponto de origem de uma chamada. As interfaces e os métodos associados permitem que um aplicativo obtenha e defina informações relacionadas ao terminal, como, por exemplo, se ele está em uso no momento. |
| [Interfaces de objeto de chamada](call-object-interfaces.md)         | O objeto de chamada representa uma chamada e é criado quando uma chamada entra em existência. As interfaces e os métodos associados obtêm e definem informações relacionadas à chamada, como o estado de chamada atual.                                                           |
| [Interfaces de objeto de telefone](phone-object-interfaces.md)       | O objeto de telefone é a entidade que representa o dispositivo de telefone real e todos os seus controles.                                                                                                                                                             |
| [Interfaces MSP IPConf](ipconf-msp-interfaces.md)           | O IP Conferencing MSP implementa várias interfaces para controle de participante que são expostas no objeto de chamada.                                                                                                                                          |
| [Interfaces de objeto CallHub](callhub-object-interfaces.md)   | O objeto CallHub representa uma exibição de terceiros de uma chamada de várias partes. As interfaces e os métodos associados obtêm e definem informações relacionadas à chamada, como se o Hub de chamadas está ativo.                                                          |
| [Interfaces do enumerador](enumerator-interfaces.md)           | Interfaces de enumerador padrão COM.                                                                                                                                                                                                                         |
| [Interfaces de evento](./event-interfaces.md)            | As interfaces de evento também são mostradas com seus agrupamentos de funções ou objetos.                                                                                                                                                                                |
| [Objetos autônomos](stand-alone-objects.md)               | Os objetos autônomos diversos da TAPI 3 fornecem interfaces e métodos para operações como a telefonia assistida ou manipulação de eventos.                                                                                                                    |



 

 

 
