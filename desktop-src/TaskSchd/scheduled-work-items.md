---
title: Itens de trabalho agendados
description: O Agendador de Tarefas usa dois termos para descrever o que pode agendar itens de trabalho e tarefas.
ms.assetid: 6ca182c3-eba8-43dd-bf2e-27dd972e3cf8
keywords:
- Agendador de Tarefas de itens de trabalho
- Agendador de Tarefas de itens de trabalho, em comparação com as tarefas
- tarefas Agendador de Tarefas
- tarefas Agendador de Tarefas, em comparação com itens de trabalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d19455b6d1402439403629aa5f6fca81621571fc90d9e6d8b204e741c5129414
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080426"
---
# <a name="scheduled-work-items"></a>Itens de trabalho agendados

O Agendador de Tarefas usa dois termos para descrever o que ele pode agendar: itens de trabalho e tarefas. Desses dois termos, o [*item de trabalho*](w.md) é um termo mais geral que descreve qualquer tipo de item que possa ser agendado. Um *item de trabalho* pode ser qualquer item que o serviço de Agendador de tarefas é executado por vez que é especificado pelos gatilhos do item.

Por outro lado, uma [*tarefa*](t.md) é um tipo específico de item de trabalho. Atualmente, o único tipo de item de trabalho agendado com suporte é uma tarefa.

A interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) contém métodos que têm suporte de todos os tipos de itens de trabalho agendados. Por exemplo, as informações da conta, os tempos de execução e os comentários definidos pelo aplicativo são propriedades que podem ser aplicadas a todos os tipos de itens de trabalho. Essas propriedades podem ser definidas e recuperadas por meio da interface **IScheduledWorkItem** .

A interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) contém métodos que têm suporte apenas por tarefas.

Os métodos da interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) são herdados atualmente pela interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) e, no futuro, serão herdados por outras interfaces de item de trabalho.

| Para obter exemplos de                                              | Consulte                                                                                        |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| Criando uma nova tarefa.                                         | [Criando uma tarefa usando o exemplo NewWorkItem](creating-a-task-using-newworkitem-example.md) |
| Executando uma tarefa existente.                                    | [Iniciando um exemplo de tarefa](starting-a-task-example.md)                                     |
| Recuperando propriedades que se aplicam a todos os tipos de itens de trabalho. | [Recuperando exemplos de propriedade de item de trabalho](retrieving-work-item-property-examples.md)       |
| Definindo propriedades que se aplicam a todos os tipos de itens de trabalho.    | [Definindo exemplos de propriedade de item de trabalho](setting-work-item-property-examples.md)             |



 

 

 




