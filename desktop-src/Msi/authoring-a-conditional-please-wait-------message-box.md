---
description: O exemplo a seguir ilustra como criar uma caixa de mensagem condicional que abre e avisa ao usuário que uma tarefa em segundo plano ainda está em execução sempre que o usuário ativa um controle exibido prematuramente.
ms.assetid: 4a99a96b-50c2-42eb-82ad-acdfa186a71f
title: Criação de "Aguarde. . ." Caixa de mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c5f0cb1e4f1a0224c3b71d42d6fc63c1940483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505798"
---
# <a name="authoring-a-conditional-please-wait-message-box"></a>Criando uma condicional "Aguarde..." Caixa de mensagem

O exemplo a seguir ilustra como criar uma caixa de mensagem condicional que abre e avisa ao usuário que uma tarefa em segundo plano ainda está em execução sempre que o usuário ativa um controle exibido prematuramente.

O exemplo também ilustra como a [SpawnWaitDialog ControlEvent,](spawnwaitdialog-controlevent.md) geralmente pode ser usada para proteger um controle que dispara uma ação dependente da conclusão de uma tarefa em segundo plano.

Neste exemplo, uma [caixa de diálogo de seleção](selection-dialog.md) que contém três controles de botão de ação rotulados como **instalar agora**, **próximo** e **custo de disco** é exibida para o usuário durante o processo de instalação. No entanto, o instalador também executa uma tarefa de custo de espaço em disco em segundo plano enquanto exibe essa caixa de diálogo. O autor deseja proteger esses botões da ativação e deseja que a caixa de mensagem "Aguarde" seja exibida se o usuário clicar em algum dos botões antes de o custo ser concluído. O autor também quer que essa caixa de mensagem contenha um botão de **cancelamento** e desapareça assim que a tarefa em segundo plano for concluída.

**Para exibir uma caixa de diálogo solicitando que o usuário aguarde enquanto o custo do disco em segundo plano é concluído**

1.  Use os recursos de criação do instalador para adicionar uma nova caixa de diálogo modal, chamada **WaitForCosting**, à [tabela de diálogo](dialog-table.md). A caixa de diálogo deve exibir uma cadeia de texto que diga "Aguarde enquanto o custo do espaço em disco é concluído".
2.  Adicione um único controle de botão de ação a essa caixa de diálogo, rotulada **Cancelar**, criando-o na [tabela de controle](control-table.md).
3.  Vincule o botão **Cancelar** Push a um ControlEvent, que fecha a caixa de diálogo **WaitForCosting** criando um [EndDialog ControlEvent,](enddialog-controlevent.md) na [tabela ControlEvent,](controlevent-table.md). Defina o argumento do evento de controle EndDialog a ser encerrado.
4.  Vincule um [SpawnWaitDialog ControlEvent,](spawnwaitdialog-controlevent.md) aos controles de botão de ação **instalar agora**, **próximo** e **custo de disco** exibidos na caixa de [diálogo seleção](selection-dialog.md) . Defina o argumento desse ControlEvent, na tabela ControlEvent, como a caixa de diálogo **WaitForCosting** e defina a expressão na coluna condição da tabela como: [**CostingComplete**](costingcomplete.md) = 1.

 

 



