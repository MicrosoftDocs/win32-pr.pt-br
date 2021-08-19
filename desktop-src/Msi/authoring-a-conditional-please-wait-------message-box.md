---
description: O exemplo a seguir ilustra como autor de uma caixa de mensagem condicional que é exibida e avisa o usuário de que uma tarefa em segundo plano ainda está em execução sempre que o usuário ativa um controle exibido prematuramente.
ms.assetid: 4a99a96b-50c2-42eb-82ad-acdfa186a71f
title: Como autor de um "Aguarde. . ." Caixa de mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f7abc26254b9656ca3d522fa7458ded30fbf09cc20a39a9f960e7509bee8a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086356"
---
# <a name="authoring-a-conditional-please-wait-message-box"></a>Como autor de um "Aguarde..." condicional Caixa de mensagem

O exemplo a seguir ilustra como autor de uma caixa de mensagem condicional que é exibida e avisa o usuário de que uma tarefa em segundo plano ainda está em execução sempre que o usuário ativa um controle exibido prematuramente.

O exemplo também ilustra como [o SpawnWaitDialog ControlEvent](spawnwaitdialog-controlevent.md) geralmente pode ser usado para proteger um controle que dispara uma ação dependente da conclusão de uma tarefa em segundo plano.

Neste exemplo, [](selection-dialog.md) uma Caixa de Diálogo de Seleção que contém três controles de botão de push rotulados Como Instalar **Agora,** **Avançar** e Custo **do** Disco é exibida para o usuário durante o processo de instalação. No entanto, o instalador também executa uma tarefa de custo de espaço em disco em segundo plano ao exibir essa caixa de diálogo. O autor deseja proteger esses botões contra a ativação e deseja que uma caixa de mensagem "Aguarde" seja pop-up se o usuário clicar em qualquer um dos botões antes que o custo seja concluído. O autor também deseja que essa caixa de mensagem contenha um **botão** Cancelar e desaparecer assim que a tarefa em segundo plano for concluída.

**Para exibir uma caixa de diálogo solicitando que o usuário aguarde enquanto o custo do disco em segundo plano é concluído**

1.  Use os recursos de autor do instalador para adicionar uma nova caixa de diálogo modal, chamada **WaitForCosting**, à [tabela Dialog](dialog-table.md). A caixa de diálogo deve exibir uma cadeia de caracteres de texto que diz "Aguarde enquanto o custo do espaço em disco for concluído".
2.  Adicione um único controle de botão de push a essa caixa de diálogo, **rotulado Cancelar**, ao autorá-lo na [tabela Controle](control-table.md).
3.  **Vincule** o botão Cancelar push a um ControlEvent que fecha a caixa de **diálogo WaitForCosting** por meio da com a adoção de [um EndDialog ControlEvent](enddialog-controlevent.md) na [tabela ControlEvent](controlevent-table.md). De acordo com o argumento do evento EndDialog Control como Exit.
4.  Vincule [um SpawnWaitDialog ControlEvent](spawnwaitdialog-controlevent.md) aos controles existentes do botão de **push** Instalar **Agora,** Avançar e Custo do Disco exibidos na caixa [de diálogo Seleção.](selection-dialog.md) De definir o argumento deste ControlEvent na tabela ControlEvent como a caixa de **diálogo WaitForCosting** e definir a expressão na coluna Condição da tabela como: [**CostingComplete**](costingcomplete.md) =1.

 

 



