---
description: O COM+ tenta evitar situações em que esses caminhos de erro devem ser executados em um servidor.
ms.assetid: 0de125a2-2e91-49b9-a903-6c2e173e22a2
title: Conceitos de portas de Low-Memory COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b4c34e10dcb18a88566d1bc45bb6751e500767c34a2e17cf8cdf12f0f1930c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129169"
---
# <a name="com-low-memory-activation-gates-concepts"></a>Conceitos de portas de Low-Memory COM+

Em geral, a sincronização não é necessária quando você tem um STA (single-threaded apartment) porque o apartment fornece a sincronização para você. A sincronização se torna importante quando você tem um MTA (apartment multithread) e um objeto de thread livre. No passado, objetos de thread livre tinham que lidar com o bloqueio. Você pode eliminar a necessidade de usar o bloqueio definindo o atributo de sincronização para um componente.

Problemas de confiabilidade geralmente ocorrem quando os recursos de um servidor não podem reagir com eficiência às cargas de pico. Quando um servidor não tem recursos físicos suficientes para atender à demanda de pico, ele pode esgotar a memória virtual. Isso se tornará um problema se o código do usuário ou o código do sistema não tratar corretamente as falhas de alocação de memória. O servidor começa a ficar lento e, à medida que a memória é esgotada, as alocações de memória falham. O servidor executa caminhos de erro para lidar com as falhas de alocação. Se um caminho de erro contiver um bug no sistema ou no código do usuário em execução no servidor, será extremamente difícil interceptá-lo e lidar com segurança.

O COM+ tenta evitar situações em que esses caminhos de erro devem ser executados em um servidor. Por meio do recurso de portões de ativação de memória baixa, o COM+ monitora proativamente a carga de memória no sistema e garante que uma quantidade razoável de memória está disponível antes de executar o código do usuário. Se o percentual de memória virtual disponível para o aplicativo ficar abaixo de um limite fixo, a ativação falhará antes que um aplicativo ou objeto do servidor COM+ seja criado (conforme mostrado na ilustração abaixo). Ao falhar nessas ativações que normalmente seriam executados, o recurso portas de ativação de memória baixa minimiza os problemas associados às alocações de memória no código do usuário, o que melhora significativamente a confiabilidade do sistema.

![Diagrama que mostra a relação entre um aplicativo COM+ e uma porta de ativação de memória baixa.](images/ada5ef02-f2b1-46bb-b0fc-fe7d65f31b43.png)

O recurso de portões de ativação de memória baixa aplica-se somente a componentes COM configurados instalados em um aplicativo COM+.

## <a name="how-the-low-memory-activation-gates-feature-works"></a>Como funciona o recurso Low-Memory portas de ativação

O recurso de portões de ativação de memória baixa usa um nível de limite fixo diferente, dependendo do tipo de ativação. Ao criar um aplicativo de servidor COM+, o COM+ permitirá a ativação se mais de 10% da memória virtual estiver disponível. Se menos de 10% estiver disponível, o COM+ fará uma alocação de teste para descobrir se o arquivo de paging pode ser expandido para acomodar a nova carga de memória. Se o arquivo de paging for expandido, o aplicativo de servidor será criado. Se o arquivo de paging não puder ser expandido, a ativação falhará e a memória não será alocada.

O processo é semelhante ao criar um objeto . Nesse caso, o COM+ permitirá a ativação se mais de 5% da memória virtual estiver disponível. Se menos de 5% estiver disponível, COM+ prosseguirá com uma alocação de teste. Novamente, se a alocação de teste expandir o arquivo de paging, o objeto será criado. Caso não seja, a ativação falhará.

No momento, os níveis de limite fixos para portões de ativação de memória baixa não são configuráveis. Por esse motivo, não há tarefas associadas a esse recurso.

 

 



