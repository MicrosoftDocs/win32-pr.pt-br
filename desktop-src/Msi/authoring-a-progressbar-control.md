---
description: Windows O instalador contém a funcionalidade para exibir um indicador de progresso em uma caixa de diálogo de exibição de ação.
ms.assetid: cfc2d974-4f2d-4f52-9835-eab1dc091c9b
title: Como autor de um controle ProgressBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1074744220bde8734fe0cd1f65aa1037ff1f0cb26763a11845a7ea7f1b58e507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066156"
---
# <a name="authoring-a-progressbar-control"></a>Como autor de um controle ProgressBar

Windows O instalador contém a funcionalidade para exibir um indicador de progresso em uma caixa de diálogo de exibição de ação. O [controle ProgressBar](progressbar-control.md) representa graficamente a instalação de componentes individuais e relata o tempo total decorrido em relação ao tempo restante ou o tempo total aproximado restante até que a instalação seja concluída.

Para determinar o tempo total previsto para a instalação, o instalador rastreia os tiques de progresso totais previstos por cada ação durante a geração do script de execução. Quando a geração de script é concluída, o total de tiques de progresso é armazenado e a instalação é iniciada.

As mensagens de progresso que detalham o número de tiques de progresso decorrido são enviadas ao manipulador de mensagens ativas conforme cada ação no script é executada. Em cada mensagem de progresso, o instalador transmite [um ControlEvent SetProgress](setprogress-controlevent.md) para a caixa de diálogo ativa no momento. A sequência de interface do usuário deve ser criado para criar a caixa de diálogo de exibição de ação durante a execução do script para receber as mensagens SetProgress ControlEvent do instalador.

Quando a caixa de diálogo de exibição de ação recebe um ControlEvent SetProgress, ela verifica a tabela [EventMapping](eventmapping-table.md) em busca de todos os controles que assinam o ControlEvent. O controle ProgressBar na caixa de diálogo de exibição de ação é inscrito com o atributo de controle Progresso especificado na coluna Atributos. O atributo Controle de Progresso especifica que o controle ProgressBar receberá os valores "ticksSoFar" e "totalTicks" juntamente com o ControlEvent SetProgress. O controle de barra de progresso usa essas informações para avançar a barra gráfica da esquerda para a direita para uma instalação e da direita para a esquerda para uma operação [de reação.](rollback-installation.md)

Além disso, o instalador transmite um [TimeRemaining ControlEvent](timeremaining-controlevent.md) em cada mensagem de progresso. O tempo total restante para a instalação é determinado primeiro calculando a taxa de execução, que é o número total de tiques decorridos dividido pelo tempo total desde o início da instalação. O total de tiques restantes divididos pela taxa de execução fornece o tempo aproximado restante.

Quando a caixa de diálogo de exibição de ação recebe o TimeRemaining ControlEvent, ele procura novamente na tabela EventMapping todos os controles inscritos. Para exibir o tempo restante, um controle Text deve ser inscrito no TimeRemaining ControlEvent com o atributo de controle [TimeRemaining](timeremaining-control-attribute.md) especificado na coluna Atributos. [](text-control.md)

O controle Texto inscrito consulta a tabela [UIText](uitext-table.md) para uma cadeia de caracteres de modelo com parâmetros chamada "TimeRemaining". Essa cadeia de caracteres tem dois parâmetros, \[ 1 \] para minutos e \[ 2 para \] segundos. O controle Texto converte cada valor em minutos e segundos, avalia a cadeia de caracteres de modelo TimeRemaining e atualiza o controle de texto com as novas informações.

Se o nível de exibição da interface do usuário estiver definido como básico ou inferior, o instalador exibirá uma caixa de diálogo padrão contendo uma barra de progresso e o campo de texto TimeRemaining. Para obter mais informações, consulte [Interface do Usuário níveis .](user-interface-levels.md)

 

 



