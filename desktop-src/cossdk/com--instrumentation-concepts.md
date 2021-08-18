---
description: O serviço de instrumentação COM+ permite que você crie seus próprios programas de registro em log e gerenciamento de eventos COM+ quando quiser exibir várias métricas de desempenho para seus componentes COM+.
ms.assetid: 07f68734-a382-4fe5-86af-90805f61c68d
title: Conceitos de instrumentação COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160a546c07ea4204f1f4da3ba4c56c76a6eed6b52a8d397d470d0bc34b76adc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549502"
---
# <a name="com-instrumentation-concepts"></a>Conceitos de instrumentação COM+

O serviço de instrumentação COM+ permite que você crie seus próprios programas de registro em log e gerenciamento de eventos COM+ quando quiser exibir várias métricas de desempenho para seus componentes COM+. A instrumentação COM+ também pode ser usada para configurar eventos definidos pelo usuário e converter eventos COM+ em um formato VSA (Analisador Visual Studio) quando você estiver atualizando pacotes MTS que estão recebendo eventos MTS.

> [!Note]  
> A partir Windows Server 2003, somente os administradores têm privilégios de acesso de leitura para os logs de rastreamento para eventos do sistema.

 

Ao assinar os eventos publicados pelo editor de eventos do sistema, os clientes podem implementar as interfaces de [instrumentação COM+](com--instrumentation-interfaces.md) para receber notificações para uma variedade de métricas de desempenho COM+, como informações sobre objetos COM+, aplicativos COM+ e serviços COM+específicos. As métricas são publicadas no cliente usando o serviço de eventos [COM+,](com--events.md)um sistema LCE (eventos de adoção fóssida) que armazena informações de eventos de diferentes publicações em um armazenamento de eventos no catálogo COM+.

> [!Note]  
> A instrumentação COM+ não garante a entrega de um evento.

 

Cada métrica tem um timestamp que indica a hora em que a métrica foi gerada, não a hora em que ela foi expedida ou recebida. O cliente pode correlacionar o timestamp e descobrir o custo da execução de um aplicativo COM+, o custo de uma transação executada dentro de um aplicativo COM+ ou o custo de uma chamada de método dentro de um aplicativo COM+.

Você também pode usar o serviço instrumentação COM+ para filtrar as informações de métricas de desempenho específicas que você deseja ver. Por exemplo, ao assinar uma interface ou método de instrumentação COM+, você pode especificar propriedades para a assinatura na estrutura [**COMSVCSEVENTINFO,**](/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo) como a ID do aplicativo (**membro guidApp)** ou a ID do processo (**membro dwPid).**

Quando a ID do aplicativo é especificada, você recebe apenas as métricas do aplicativo especificado. Quando a ID do processo é especificada, você recebe métricas do aplicativo de servidor e dos aplicativos de biblioteca especificados que são carregados nesse processo. O usuário pode especificar a ID do aplicativo e a ID do processo, mas a ID do aplicativo deve ser a do aplicativo de servidor em execução no processo com a ID do processo especificada. Se nenhum deles for especificado, o usuário receberá métricas de todos os aplicativos de servidor e biblioteca.

As métricas de instrumentação COM+ fornecem informações suficientes para que o aplicativo de monitoramento as correlacione com as métricas do sistema operacional para análise de desempenho, planejamento de capacidade e modelagem e previsão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interfaces de instrumentação COM+](com--instrumentation-interfaces.md)
</dt> </dl>

 

 



