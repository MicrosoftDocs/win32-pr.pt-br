---
description: Na infraestrutura do WMI, o serviço WMI (Winmgmt) é o componente do sistema operacional que atua como o mediador entre os aplicativos de gerenciamento e os provedores de dados WMI. O repositório WMI é uma área de armazenamento para dados estáticos relacionados ao WMI.
ms.assetid: 6ef157be-fb75-4453-bc20-4568a3dc18c0
ms.tgt_platform: multiple
title: Infraestrutura WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2bc4492c7d26f422705863609a2e0ec19af5eb930e0aa80f4fd8bb8c26bea4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757326"
---
# <a name="wmi-infrastructure"></a>Infraestrutura WMI

Na infraestrutura do WMI, o serviço WMI (Winmgmt) é o componente do sistema operacional que atua como o mediador entre os aplicativos de gerenciamento e os [*provedores*](gloss-p.md)de dados WMI. O [*repositório WMI*](gloss-w.md) é uma área de armazenamento para dados estáticos relacionados ao WMI.

O serviço WMI é implementado como um processo de serviço dentro de um processo de host de serviço compartilhado (SVCHOST). Para obter mais informações, consulte [provedor de hospedagem e segurança](provider-hosting-and-security.md).

O serviço WMI é iniciado quando o primeiro aplicativo de gerenciamento ou script faz uma chamada para conectar-se a um namespace WMI. Dependendo da configuração, o serviço WMI pode desligar ou entrar em um perfil de memória insuficiente quando não está sendo chamado por um aplicativo de gerenciamento.

O serviço WMI interage com aplicativos de gerenciamento por meio da interface COM. Quando um aplicativo faz uma solicitação por meio da interface, o WMI determina se a solicitação é para dados estáticos ou dinâmicos. Se a solicitação envolver dados estáticos, como o nome de um objeto gerenciado, o WMI recuperará os dados do repositório. Se a solicitação envolver dados dinâmicos, como a quantidade de memória que um objeto gerenciado está usando no momento, o WMI passará a solicitação para um provedor.

Os provedores registram seu local com o serviço WMI, que permite ao WMI rotear solicitações de dados. Um provedor também registra o suporte para operações específicas, como recuperação de dados, modificação, exclusão, enumeração ou processamento de consulta. O serviço WMI usa as informações de registro do provedor para corresponder às solicitações do aplicativo com o provedor apropriado. O WMI também usa as informações de registro para carregar e descarregar provedores, conforme necessário. Quando um provedor termina de processar uma solicitação, o provedor retorna o resultado para o serviço WMI. Em seguida, o WMI encaminha o resultado para o aplicativo por meio da interface COM. Para obter mais informações, consulte [fornecendo dados ao WMI](providing-data-to-wmi.md).

O WMI usa o ETW ( [rastreamento de eventos](/windows/desktop/ETW/event-tracing-portal) ) para registrar a atividade do serviço WMI.

Como a infraestrutura manipula todo o tráfego entre os provedores e os aplicativos de gerenciamento, a infraestrutura fornece os seguintes recursos:

-   Suporte à notificação de eventos

    Para obter mais informações, consulte [monitorando eventos](monitoring-events.md).

-   Suporte à linguagem de consulta

    Para obter mais informações, consulte [consultando com WQL](querying-with-wql.md).

-   Suporte de segurança

    Para obter mais informações, consulte [mantendo a segurança do WMI](maintaining-wmi-security.md).

-   Script de acesso a dados do contador de desempenho

    Para obter mais informações, consulte [monitorando dados de desempenho](monitoring-performance-data.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Arquitetura do WMI](wmi-architecture.md)
</dt> </dl>

 

 
