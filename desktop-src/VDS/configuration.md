---
description: Visão geral da configuração
ms.assetid: 5cdc21a1-ff55-4c36-8106-b045256778ce
title: Visão geral da configuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4db13827bf08ee65ed8015f0c19ba2980a9a71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920841"
---
# <a name="configuration-overview"></a>Visão geral da configuração

\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Se você não estiver familiarizado com os objetos definidos pelo VDS, consulte o modelo de [objeto do VDS](vds-object-model.md).

A complexidade da configuração de um disco virtual pode variar de muito simples para ajustado. Os discos virtuais corporativos, gratuitos e sem cuidado definem três perspectivas de configuração típicas. Cada perspectiva apresenta requisitos um pouco diferentes:

-   Discos virtuais sem cuidado são levemente configurados, talvez apenas para automatizar o particionamento e a formatação de novos discos, ou para criar temporariamente um volume espelhado para migrar dados de um disco para outro sem tempo de inatividade. Esses discos são bons para computadores notebook e outros sistemas com um ou alguns discos.
-   Os discos virtuais livres do próprio atendimento fornecem armazenamento que aparece autoconfigurável, auto-recuperação e disponível; usa volumes distribuídos e LUNs para obter um melhor desempenho; usa volumes espelhados e LUNs para obter melhor disponibilidade; e usa pacotes para tornar os modos de falha limpos e contidos. Esse nível de configuração é ideal ao substituir discos do sistema antigos, pequenos e lentos por discos novos, grandes e rápidos é a rotina. Ele também é ideal para espelhamento de dados com Hot Sparing automatizado — um único eixo sobressalente pode proteger muitos eixos. Para obter detalhes, consulte [Hot Sparing](hot-sparing.md).

    SANs de pequena escala dependem da flexibilidade e da automação oferecidas por esse nível de configuração, como os dispositivos NAS (armazenamento anexado à rede). Discos virtuais livres da própria simplificam a tarefa de consolidar o armazenamento de aplicativos — por exemplo, o armazenamento para SQL e Exchange — sem consolidar os servidores.

-   Os discos virtuais corporativos contêm configurações corporativas muito grandes ou complexas com requisitos adicionais específicos do site ou do aplicativo. Os administradores ajustam o subsistema de armazenamento para um único aplicativo que pode ser executado com pouca frequência, como um trabalho mensal de relatórios em lote em um sistema de transação de ordem demorada. Os discos virtuais corporativos devem ser dimensionados, mostrar a atividade em tempo real do subsistema de armazenamento e atender aos requisitos de administradores práticos.

Para obter informações adicionais sobre espelhos, faixas e outras opções de configuração no VDS, consulte [Associação de volume e LUN](volume-and-lun-binding.md). Uma técnica de configuração avançada, chamada de empilhamento, permite combinar as configurações associadas aos volumes e LUNs existentes. Para obter detalhes, consulte [empilhamento de configuração](configuration-stacking.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Serviço de Disco Virtual](virtual-disk-service-portal.md)
</dt> <dt>

[Modelo de objeto VDS](vds-object-model.md)
</dt> <dt>

[Hot Sparing](hot-sparing.md)
</dt> <dt>

[Associação de volume e LUN](volume-and-lun-binding.md)
</dt> <dt>

[Empilhamento de configuração](configuration-stacking.md)
</dt> </dl>

 

 
