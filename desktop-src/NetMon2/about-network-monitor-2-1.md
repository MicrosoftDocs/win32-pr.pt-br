---
description: Monitor de Rede é um componente do Microsoft Systems Management Server (SMS) usado para detectar e solucionar problemas em LANs, WANs e Links seriais que executam o Microsoft Remote Access Server (RAS).
ms.assetid: bd273439-daa2-4263-8f12-28ec988beea0
title: Sobre o Monitor de Rede 2,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f447f4763e0c73dc0dcac4cf719a0bad4b61f073
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010988"
---
# <a name="about-network-monitor-21"></a>Sobre o Monitor de Rede 2,1

Monitor de Rede é um componente do Microsoft Systems Management Server (SMS) usado para detectar e solucionar problemas em LANs, WANs e Links seriais que executam o Microsoft Remote Access Server (RAS). O Monitor de Rede fornece análise de dados de rede após a captura.

Na análise após a captura, o tráfego de rede é salvo em um arquivo de captura proprietário, para que os dados capturados possam ser analisados posteriormente. Nesse caso, a análise pode estar na forma de [*analisadores*](p.md) de protocolo que selecionam tipos de quadro de rede específicos e exibindo os dados de quadro na interface do usuário do monitor de rede; ou a análise pode estar na forma de [*especialistas*](e.md) examinando os dados da rede e exibindo um relatório (os especialistas também podem manipular os dados da rede).

Monitor de Rede fornece os seguintes tipos de funcionalidade:

-   Captura dados de rede em modo em tempo real ou atrasado.
-   Fornece recursos de filtragem ao capturar dados.
-   Usa especialistas e analisadores para análise detalhada posterior à captura.

Para obter mais informações sobre Monitor de Rede recursos, consulte:

-   [Arquitetura de expert e parser](expert-and-parser-architecture.md)
-   [Especialistas](experts.md)
-   [Analisadores](parsers.md)
-   [Provedores de pacotes de rede](network-packet-providers.md)
-   [BLOBs de Monitor de Rede](network-monitor-blobs.md)
-   [Página referência de evento](event-reference-page.md)
-   [Filtros de captura](capture-filters.md)

**Windows Vista:** Monitor de Rede 2,1 e anteriores não têm suporte nesta plataforma.

 

 



