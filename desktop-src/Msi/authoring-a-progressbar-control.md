---
description: Windows Installer contém a funcionalidade para exibir um indicador de progresso em uma caixa de diálogo de exibição de ação.
ms.assetid: cfc2d974-4f2d-4f52-9835-eab1dc091c9b
title: Criando um controle ProgressBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b872ed2dd36fb8ed04ee48fd69e4680fce002a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828059"
---
# <a name="authoring-a-progressbar-control"></a>Criando um controle ProgressBar

Windows Installer contém a funcionalidade para exibir um indicador de progresso em uma caixa de diálogo de exibição de ação. O [controle ProgressBar](progressbar-control.md) representa graficamente a instalação de componentes individuais e relata o tempo total decorrido relativo ao tempo restante ou o tempo total aproximado restante até que a instalação seja concluída.

Para determinar o tempo total previsto para a instalação, o instalador acompanhará o total de tiques de progresso antecipados por cada ação durante a geração do script de execução. Quando a geração de script for concluída, o total de tiques de andamento será armazenado e a instalação começará.

Mensagens de progresso detalhando o número decorrido de tiques de progresso são enviadas para o manipulador de mensagens ativas, pois cada ação no script é executada. Em cada mensagem de progresso, o instalador transmite um [ControlEvent, de regressão](setprogress-controlevent.md) para a caixa de diálogo ativa no momento. A sequência de interface do usuário deve ser criada para criar a caixa de diálogo de exibição de ação durante a execução do script para receber as mensagens ControlEvent, do instalador.

Quando a caixa de diálogo Exibir ação recebe um ControlEvent, de regressão, ele verifica a [tabela EventMappings](eventmapping-table.md) para todos os controles que se inscreverem no ControlEvent,. O controle ProgressBar na caixa de diálogo de exibição de ação é assinado com o atributo de controle de progresso especificado na coluna atributos. O atributo de controle Progress especifica que o controle ProgressBar receberá os valores "ticksSoFar" e "totalTicks" junto com o ControlEvent, de setProgress. O controle de barra de progresso usa essas informações para avançar a barra gráfica da esquerda para a direita para uma instalação e da direita para a esquerda para uma operação de [reversão](rollback-installation.md) .

Além disso, o instalador transmite um [ControlEvent, de permanência](timeremaining-controlevent.md) em cada mensagem de progresso. O tempo total restante para a instalação é determinado pela primeira vez que calcula a taxa de execução, que é o número total de tiques decorridos dividido pelo tempo total desde que a instalação começou. O total de tiques restantes dividido pela taxa de execução fornece o tempo aproximado restante.

Quando a caixa de diálogo Exibir ação recebe o ControlEvent, do timecontinueing, ele examina novamente a tabela EventMappings para todos os controles que forem assinados. Para exibir o tempo restante, um controle de [texto](text-control.md) deve ser assinado para o timecontinueing ControlEvent, com o atributo de [controle timepersisting](timeremaining-control-attribute.md) especificado na coluna atributos.

O controle de texto assinado consulta a [tabela UIText](uitext-table.md) para uma cadeia de caracteres de modelo com parâmetros chamada "timecontinueing". Essa cadeia de caracteres tem dois parâmetros, \[ 1 \] para minutos e \[ 2 \] para segundos. O controle de texto converte cada valor em minutos e segundos, avalia a cadeia de caracteres do modelo que está permanecendo e atualiza o controle de texto com as novas informações.

Se o nível de exibição da interface do usuário for definido como básico ou inferior, o instalador exibirá uma caixa de diálogo padrão contendo uma barra de progresso e um campo de texto de permanência. Para obter mais informações, consulte [níveis de interface do usuário](user-interface-levels.md).

 

 



