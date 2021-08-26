---
description: Acompanhamento de COM+
ms.assetid: ad3bdeb5-f303-411a-abfb-ccde3f9a86b9
title: Acompanhamento de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 069d910f0c559776125342b861e71566fb20f45231f960b1c1dcb18262171926
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029486"
---
# <a name="com-tracking"></a>Acompanhamento de COM+

O serviço de acompanhamento COM+ permite que você crie seus próprios programas administrativos e de diagnóstico que acompanham o status e o desempenho da execução de aplicativos COM+. O acompanhamento COM+ fornece informações estatísticas sobre o uso de aplicativos COM+, bem como informações de status, como se uma instância de aplicativo de servidor COM+ está em pausa ou foi reciclada. As ferramentas podem usar informações de acompanhamento no monitoramento de diagnóstico ou para fins de exibição. Por exemplo, a ferramenta administrativa Serviços de Componentes usa o acompanhamento COM+ para exibir o status das instâncias de aplicativo COM+ nas pastas Aplicativos COM+ e Processos em Execução.

O acompanhamento COM+ calcula e atualiza periodicamente um conjunto de métricas comumente usadas, disponibilizando essas informações para programas que precisam delas. É semelhante à Instrumentação COM+ no sentido de que ambos os serviços coletam dados automaticamente de instâncias de aplicativo COM+ e disponibilizam esses dados para os consumidores. No entanto, há algumas diferenças importantes entre esses serviços, tanto na funcionalidade fornecida quanto no uso típico. A tabela a seguir resume essas diferenças.



| Instrumentação COM+                                                                                                                                                                                                   | Acompanhamento de COM+                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dados finos. O serviço de instrumentação COM+ notifica os assinantes registrados de eventos discretos individuais (por exemplo, método chamado, objeto destruído) que ocorrem em uma instância de aplicativo COM+.<br/> | Dados agregados. O acompanhamento COM+ calcula e atualiza periodicamente métricas usadas para o status e o desempenho de instâncias de aplicativo COM+.<br/> |
| Os assinantes de eventos normalmente calculam as métricas por conta própria, usando algoritmos e políticas ad hoc.<br/>                                                                                                           | As métricas são calculadas automaticamente pelo serviço de acompanhamento COM+. Todos os consumidores têm os mesmos dados, sem suporte para métricas personalizadas.<br/>                |
| Depois de registrar uma assinatura, o consumidor não recebe nenhuma informação sobre uma instância de aplicativo COM+ até que um evento ocorra.<br/>                                                                    | Os dados de acompanhamento de todas as instâncias de aplicativo COM+ podem ser recuperados a qualquer momento.<br/>                                                                         |
| Dá suporte apenas a um mecanismo de assinatura baseado em eventos COM+ para consumidores.<br/>                                                                                                                                     | Dá suporte a um mecanismo de assinatura baseado em eventos COM+ e à sondagem em uma interface de servidor local COM.<br/>                                                  |
| Exemplos                                                                                                                                                                                                               |                                                                                                                                                                   |
| Notificações quando um método é chamado ou retorna.<br/>                                                                                                                                                           | Tempo médio de resposta de chamada, número de chamadas de método que tiveram êxito ou falharam em um período de tempo recente, número de objetos atualmente em uma chamada de método.<br/>     |
| Notificações quando um objeto é adicionado ou obtido do pool de objetos.<br/>                                                                                                                                  | Número de objetos no pool, número total de objetos.<br/>                                                                                                |
| Notificações quando um aplicativo de servidor COM+ é iniciado, pausado ou reciclado.<br/>                                                                                                                               | Status do processo de aplicativo do servidor COM+ (por exemplo, se ele está em pausa ou reciclado).<br/>                                                         |
| Notificações de eventos de início, preparação, anulação e commit da transação.<br/>                                                                                                                                      | Não há equivalência.<br/>                                                                                                                                         |
| Notificações de tentativas de autenticação de nível de chamada de método bem-sucedidas e com falha.<br/>                                                                                                                           | Não há equivalência.<br/>                                                                                                                                         |



 

Embora o acompanhamento COM+ seja mais limitado em termos de escopo de dados e flexibilidade para calcular métricas, as métricas que ele fornece devem ser suficientes para uma ampla variedade de programas administrativos e de diagnóstico. O uso do acompanhamento COM+, quando possível, pode simplificar o design desses programas. Além disso, o uso do acompanhamento COM+ em sistemas de produção pode ter um impacto significativamente menor no desempenho, tornando-o mais apropriado para ferramentas de monitoramento em tempo real.

## <a name="how-com-tracking-collects-data"></a>Como o acompanhamento com+ coleta dados

Quando um processo de aplicativo de servidor COM+ é iniciado, o COM+ registra o processo com o servidor *rastreador*, um componente do aplicativo do sistema. Componentes em aplicativos e serviços de biblioteca COM+ sem contextos de SWC (componentes) também são suportados pelo acompanhamento. Quando um componente de biblioteca ou contexto SWC é criado em um processo, o COM+ registra o processo com o servidor rastreador se ele ainda não foi registrado.

O COM+ atualiza estatísticas para um processo rastreado quando determinados eventos ocorrem no processo, como a criação de um objeto ou a conclusão de uma chamada de método. Os dados atualizados são enviados periodicamente para o servidor rastreador, momento em que eles se tornam disponíveis para os consumidores. O servidor rastreador também é responsável por calcular algumas das métricas usadas pelos recursos de monitoramento de travamento e reciclagem de aplicativos COM+. Esses dados também estão disponíveis para os consumidores.

Os dados de acompanhamento são organizados de acordo com o processo que gerou os dados. Os dados no nível de aplicativos ou componentes COM+ individuais no processo também estão disponíveis para consumidores que precisam dessas informações.

## <a name="events-versus-polling"></a>Eventos versus Sondagem

O rastreamento COM+ dá suporte a dois mecanismos para um consumidor obter dados de acompanhamento do servidor rastreador, um mecanismo de assinatura baseado em eventos COM+ e uma interface de servidor local COM.

Programas que precisam ser notificados periodicamente com dados de acompanhamento atualizados podem registrar uma assinatura para a interface de evento [**IComTrackingInfoEvents.**](/windows/desktop/api/ComSvcs/nn-comsvcs-icomtrackinginfoevents) Aproximadamente a cada três segundos, o servidor rastreador chama o método [**IComTrackingInfoEvents::OnNewTrackingInfo**](/windows/desktop/api/ComSvcs/nf-comsvcs-icomtrackinginfoevents-onnewtrackinginfo) de cada assinante, enviando os dados de rastreamento mais recentes na forma de um objeto de coleção. Esse objeto implementa a interface [**IComTrackingInfoCollection**](/windows/desktop/api/ComSvcs/nn-comsvcs-icomtrackinginfocollection) e os assinantes podem navegar por essa coleção para encontrar os dados em que estão interessados.

Por vários motivos, pode fazer mais sentido para um programa sondar o servidor rastreador em busca de dados. Por exemplo, uma ferramenta de monitoramento pode precisar de atualizações com muito menos frequência do que um programa que exibe o status em uma interface do usuário. Além disso, um programa pode usar apenas uma pequena parte dos dados de acompanhamento disponíveis para o sistema (por exemplo, uma ferramenta só pode monitorar o desempenho de instâncias de um único aplicativo COM+). O modelo de assinatura envia a cada assinante os dados de acompanhamento de todos os aplicativos COM+ em cada notificação e é responsabilidade do assinante localizar os dados que deseja. Por fim, os eventos COM+ são um mecanismo de notificação de eventos de melhor esforço. Os serviços de entrega de mensagens confiáveis não são fornecidos e não é possível que um assinante detecte que o servidor rastreador falhou ao enviar uma notificação.

Um programa que precisa de maior controle sobre sua recuperação de dados de acompanhamento pode usar a interface [**IGetAppTrackerData**](/windows/desktop/api/ComSvcs/nn-comsvcs-igetapptrackerdata) do servidor rastreador.

 

 




