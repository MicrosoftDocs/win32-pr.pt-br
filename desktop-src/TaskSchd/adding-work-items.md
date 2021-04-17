---
title: Adicionando itens de trabalho
description: Há duas maneiras de adicionar itens de trabalho ao Tasksfolder agendado. Você pode criar um novo item de trabalho dentro da pasta ou pode adicionar um item de trabalho existente à pasta.
ms.assetid: fad5e813-a2e9-40af-97a9-4f92debf1808
keywords:
- Agendador de Tarefas de itens de trabalho, adicionando
- tarefas Agendador de Tarefas, adicionando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 722f776fd36933995cfd9b5a85612b52dae63f7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105758395"
---
# <a name="adding-work-items"></a>Adicionando itens de trabalho

Há duas maneiras de adicionar [*itens de trabalho*](w.md) ao [*Tasksfolder agendado*](s.md). Você pode criar um novo item de trabalho dentro da pasta ou pode adicionar um item de trabalho existente à pasta.

> [!Note]  
> Atualmente, somente objetos de tarefa podem ser adicionados à pasta tarefas agendadas. Ao adicionar uma tarefa, você deve saber os identificadores para a classe de tarefa e a interface de tarefa [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).

 

Você cria novos itens de trabalho chamando o método [**ITaskScheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) . Esse método cria um novo objeto de item de trabalho usando o nome que você fornece e adiciona o item de trabalho à pasta tarefas agendadas. Quando você cria um novo item de trabalho, o Agendador de Tarefas aloca a memória necessária para o novo objeto.

Para adicionar itens de trabalho existentes à pasta tarefas agendadas, chame o método [**ITaskScheduler:: AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) . Ao chamar esse método, você deve criar o objeto.

Os nomes fornecidos para itens de trabalho devem ser exclusivos na pasta tarefas agendadas. Se já existir um item de trabalho com o mesmo nome quando você chamar o método [**ITaskScheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) ou o método [**ITaskScheduler:: AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) , o método retornará um erro de **\_ arquivo \_ de erro** . Para obter mais informações, consulte [criando uma tarefa usando o exemplo NewWorkItem](creating-a-task-using-newworkitem-example.md).

 

 




