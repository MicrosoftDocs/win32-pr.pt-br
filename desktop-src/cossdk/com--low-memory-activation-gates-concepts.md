---
description: O COM+ tenta evitar situações em que esses caminhos de erro precisam ser executados em um servidor.
ms.assetid: 0de125a2-2e91-49b9-a903-6c2e173e22a2
title: Conceitos de retransmissores de ativação do COM+ Low-Memory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b4c34e10dcb18a88566d1bc45bb6751e500767c34a2e17cf8cdf12f0f1930c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129169"
---
# <a name="com-low-memory-activation-gates-concepts"></a>Conceitos de retransmissores de ativação do COM+ Low-Memory

Geralmente, a sincronização não é necessária quando você tem um STA (single-threaded apartment) porque o apartamento fornece a sincronização para você. A sincronização se torna importante quando você tem um MTA (multithreaded apartment) e um objeto de thread livre. No passado, os objetos de thread livre tinham que lidar com o bloqueio. Você pode eliminar a necessidade de usar o bloqueio definindo o atributo de sincronização para um componente.

Os problemas de confiabilidade geralmente ocorrem quando os recursos de um servidor não podem reagir com eficiência às cargas de pico. Quando um servidor não tem recursos físicos suficientes para atender à demanda de pico, ele pode esgotar a memória virtual. Isso se tornará um problema se o código do usuário ou o código do sistema não tratar corretamente falhas de alocação de memória. O servidor começa a ficar lento e, à medida que a memória é esgotada, as alocações de memória falham. O servidor executa caminhos de erro para lidar com as falhas de alocação. Se um caminho de erro contiver um bug no sistema ou no código do usuário em execução no servidor, será extremamente difícil interceptar e lidar com segurança.

O COM+ tenta evitar situações em que esses caminhos de erro precisam ser executados em um servidor. Por meio do recurso de Gates de ativação de memória baixa, o COM+ monitora a carga de memória no sistema de forma proativa e garante que uma quantidade razoável de memória esteja disponível antes da execução do código do usuário. Se a porcentagem de memória virtual disponível para o aplicativo ficar abaixo de um limite fixo, a ativação falhará antes de um aplicativo de servidor COM+ ou objeto ser criado (conforme mostrado na ilustração abaixo). Ao falhar essas ativações que normalmente seriam executadas, o recurso de Gates de ativação de baixa memória minimiza os problemas associados às alocações de memória no código do usuário, o que melhora significativamente a confiabilidade do sistema.

![Diagrama que mostra a relação entre um aplicativo COM+ e um portão de ativação de baixa memória.](images/ada5ef02-f2b1-46bb-b0fc-fe7d65f31b43.png)

O recurso Gates de ativação de memória baixa se aplica somente aos componentes COM configurados que estão instalados em um aplicativo COM+.

## <a name="how-the-low-memory-activation-gates-feature-works"></a>Como funciona o recurso Low-Memory Activation Gates

O recurso de Gates de ativação de memória baixa usa um nível de limite fixo diferente dependendo do tipo de ativação. Ao criar um aplicativo de servidor do COM+, o COM+ permitirá a ativação se mais de 10% da memória virtual estiver disponível. Se menos de 10 por cento estiver disponível, o COM+ fará uma alocação de teste para descobrir se o arquivo de paginação pode ser expandido para acomodar a nova carga de memória. Se o arquivo de paginação for expandido, o aplicativo do servidor será criado. Se o arquivo de paginação não puder ser expandido, a ativação falhará e a memória não será alocada.

O processo é semelhante ao criar um objeto. Nesse caso, o COM+ permitirá a ativação se mais de 5% da memória virtual estiver disponível. Se menos de 5% estiver disponível, o COM+ continuará com uma alocação de teste. Novamente, se a alocação de teste expandir o arquivo de paginação, o objeto será criado. Caso contrário, a ativação falhará.

Os níveis de limite fixo para Gates de ativação de memória insuficiente atualmente não são configuráveis. Por esse motivo, não há tarefas associadas a esse recurso.

 

 



