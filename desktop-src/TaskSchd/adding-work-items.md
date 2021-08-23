---
title: Adicionando itens de trabalho
description: Há duas maneiras de adicionar itens de trabalho àfolder Tarefas Agendadas. Você pode criar um novo item de trabalho dentro da pasta ou pode adicionar um item de trabalho existente à pasta.
ms.assetid: fad5e813-a2e9-40af-97a9-4f92debf1808
keywords:
- itens de trabalho Agendador de Tarefas , adicionando
- tarefas Agendador de Tarefas , adicionando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc964b620a01b0f1114240dcb11f275fa8faffc37e8264d8854cb60191628943
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621156"
---
# <a name="adding-work-items"></a>Adicionando itens de trabalho

Há duas maneiras de adicionar itens [*de trabalho*](w.md) [*àpasta Tarefas Agendadas*](s.md). Você pode criar um novo item de trabalho dentro da pasta ou pode adicionar um item de trabalho existente à pasta.

> [!Note]  
> Atualmente, somente objetos de tarefa podem ser adicionados à pasta Tarefas Agendadas. Ao adicionar uma tarefa, você deve conhecer os identificadores para a classe de tarefa e a interface de tarefa [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).

 

Crie novos itens de trabalho chamando o [**método ITaskScheduler::NewWorkItem.**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) Esse método cria um novo objeto de item de trabalho usando o nome que você fornece e adiciona o item de trabalho à pasta Tarefas Agendadas. Quando você cria um novo item de trabalho, o Agendador de Tarefas aloca a memória necessária para o novo objeto.

Para adicionar itens de trabalho existentes à pasta Tarefas Agendadas, chame o método [**ITaskScheduler::AddWorkItem.**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) Ao chamar esse método, você deve criar o objeto .

Os nomes que você fornece para itens de trabalho devem ser exclusivos na pasta Tarefas Agendadas. Se um item de trabalho com o mesmo nome já existir quando você chamar o método [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) ou o método [**ITaskScheduler::AddWorkItem,**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) o método retornará um **erro ERROR FILE \_ \_ EXISTS.** Para obter mais informações, consulte [Criando uma tarefa usando NewWorkItem Example](creating-a-task-using-newworkitem-example.md).

 

 




