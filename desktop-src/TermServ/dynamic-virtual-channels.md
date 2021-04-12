---
title: Canais virtuais dinâmicos
description: As APIs de canal virtual dinâmico (DVC) estendem as APIs de canal virtual existentes para Serviços de Área de Trabalho Remota, conhecidas como APIs de SVC (canal virtual estático).
ms.assetid: bddf0048-482d-40f3-a973-9d7bc15be8fa
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3181c0960b50289846018c3ace773a8351cb20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363955"
---
# <a name="dynamic-virtual-channels"></a>Canais virtuais dinâmicos

As APIs de canal virtual dinâmico (DVC) estendem as APIs de canal virtual existentes para Serviços de Área de Trabalho Remota, conhecidas como APIs de SVC (canal virtual estático). As APIs DVC resolvem várias limitações que existiam em APIs SVC entre o cliente e o servidor, como:

-   Um número limitado de canais
-   Reconstrução de pacote

As APIs do DVC ajudarão você a implementar módulos no lado do servidor e do cliente de uma conexão Serviços de Área de Trabalho Remota que se comunicam entre si.

Como muitas outras arquiteturas de cliente/servidor, uma conexão é estabelecida com base em uma parte de dados comumente acordada, conhecida como um ponto de extremidade. Um exemplo semelhante é o TCP/IP, em que um ponto de extremidade é estabelecido por meio de uma combinação de endereço IP do servidor e o nome da porta. Outro exemplo são pipes nomeados, em que um ponto de extremidade é uma combinação do nome do servidor e do nome do pipe. Em uma conexão Serviços de Área de Trabalho Remota, há apenas dois lados envolvidos. Portanto, o ponto de extremidade consiste em uma cadeia de caracteres arbitrária simples que identifica exclusivamente a conexão. Assim como TCP/IP e pipes nomeados, várias conexões podem iniciar com o mesmo nome de ponto de extremidade. Nesse sentido, as conexões não têm nomes; apenas um ouvinte que aguarda solicitações de entrada no ponto de extremidade.

As APIs DVC consistem no seguinte:

-   APIs de cliente

    Essas APIs estão disponíveis no cliente de Conexão de Área de Trabalho Remota (RDC) como um plug-in. O lado do cliente está no modo passivo, onde ele escuta conexões de entrada, mas não estabelece ativamente uma conexão.

-   APIs de servidor

    Essas APIs iniciam ativamente a conexão.

Para obter informações sobre como gravar um módulo de canal virtual dinâmico (DVC), consulte [detalhes de implementação do DVC](dvc-implementation-details.md).

 

 




