---
description: Visão geral da configuração
ms.assetid: 5cdc21a1-ff55-4c36-8106-b045256778ce
title: Visão geral da configuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b742cb5ca2f287cd8b50b9f248d0ebec1174bfd71b59f0630bd9fb98864309c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007946"
---
# <a name="configuration-overview"></a>Visão geral da configuração

\[Começando com Windows 8 e Windows Server 2012, a interface COM do Serviço de Disco [Virtual](virtual-disk-service-portal.md) é superada pelo [Windows Armazenamento API de Gerenciamento](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Se você não estiver familiarizado com os objetos definidos pelo VDS, consulte o [Modelo de Objeto VDS](vds-object-model.md).

A complexidade de configuração de um disco virtual pode variar de muito simples a ajustada. Discos virtuais empresariais sem cuidado, sem cuidado e empresariais definem três perspectivas de configuração típicas. Cada perspectiva apresenta requisitos um pouco diferentes:

-   Os discos virtuais sem cuidado são configurados de forma leve, talvez apenas para automatizar o particionamento e a formatação de novos discos ou criar temporariamente um volume espelhado para migrar dados de um disco para outro sem tempo de inatividade. Esses discos são bons para computadores de notebook e outros sistemas com um ou alguns discos.
-   Os discos virtuais gratuitos fornecem armazenamento que aparece autoconfigurando, autorrecontrolando e disponível; usa volumes e LUNs em faixa para obter um melhor desempenho; usa volumes espelhados e LUNs para obter melhor disponibilidade; e usa pacotes para tornar os modos de falha limpos e contidos. Esse nível de configuração é ideal ao substituir discos do sistema antigos, pequenos e lentos por discos novos, grandes e rápidos. Ele também é ideal para espelhamento de dados com esparso automatizado – um único eixo sobressalente pode proteger muitos eixos. Para obter detalhes, [consulte Hot Sparing](hot-sparing.md).

    As SANs de pequena escala dependem da flexibilidade e da automação oferecidas por esse nível de configuração, assim como os dispositivos NAS (redes conectadas Armazenamento). Os discos virtuais gratuitos simplificam a tarefa de consolidar o armazenamento de aplicativos , por exemplo, o armazenamento para SQL e Exchange– sem consolidar os servidores.

-   Enterprise discos virtuais contêm configurações empresariais muito grandes ou complexas com requisitos adicionais específicos do site ou específicos do aplicativo. Os administradores ajustam o subsistema de armazenamento para um único aplicativo que pode ser executado apenas com pouca experiência, como um trabalho de relatório em lotes mensal em um sistema de transações de solicitação. Enterprise discos virtuais devem ser dimensionadas, mostrar a atividade em tempo real do subsistema de armazenamento e atender aos requisitos de administradores de mãos ativas.

Para obter informações adicionais sobre espelhos, faixas e outras opções de configuração no VDS, consulte [Volume e Associação de LUN.](volume-and-lun-binding.md) Uma técnica de configuração avançada, chamada empilhamento, permite combinar as configurações associadas a volumes e LUNs existentes. Para obter detalhes, consulte [Empilhamento de configuração.](configuration-stacking.md)

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

 

 
