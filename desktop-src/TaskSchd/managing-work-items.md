---
title: Manipulando itens de trabalho
description: A interface IScheduledWorkItem fornece métodos para recuperar e definir propriedades de item de trabalho; Criando, recuperando e excluindo gatilhos para itens de trabalho (a definição do gatilho deve ser feita com o método settrigger ITaskTrigger); e para executar, encerrar e excluir o item de trabalho. Observação para as propriedades de um tipo específico de item de trabalho, consulte a interface para esse tipo de objeto. Por exemplo, você não pode definir o nível de prioridade de um item de trabalho; no entanto, você pode usar os métodos da interface ITask para recuperar e definir a prioridade de uma tarefa.
ms.assetid: 8aedf96d-e43d-4aac-ad8c-860379209f95
keywords:
- Agendador de Tarefas de itens de trabalho, gerenciando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33680d04da9d34f54085d182ed61edda9e8b232f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641411"
---
# <a name="manipulating-work-items"></a>Manipulando itens de trabalho

A interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) fornece métodos para recuperar e definir propriedades de item de trabalho; criar, recuperar e excluir gatilhos para itens de trabalho (definir o gatilho deve ser feito com o método [**ITaskTrigger:: settrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) ); e para executar, encerrar e excluir o item de trabalho.

> [!Note]  
> Para as propriedades de um tipo específico de item de trabalho, consulte a interface para esse tipo de objeto. Por exemplo, você não pode definir o nível de prioridade de um item de trabalho; no entanto, você pode usar os métodos da interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) para recuperar e definir a prioridade de uma tarefa.

 

Sempre que você modificar um item de trabalho, deverá chamar o objeto [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para salvar o item de trabalho modificado em disco. A interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) é uma interface com padrão que é suportada pela interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .

| Para obter exemplos de                                                            | Consulte                                                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| Recuperando propriedades que se aplicam a todos os tipos de itens de trabalho                | [Recuperando exemplos de propriedade de item de trabalho](retrieving-work-item-property-examples.md) |
| Definindo propriedades que se aplicam a todos os tipos de itens de trabalho                   | [Definindo exemplos de propriedade de item de trabalho](setting-work-item-property-examples.md)       |
| Executando uma tarefa conhecida                                                       | [Iniciando um exemplo de tarefa](starting-a-task-example.md)                               |
| Finalizando uma tarefa em execução                                                 | [Finalizando um exemplo de tarefa](terminating-a-task-example.md)                         |
| Criando um novo gatilho para uma tarefa conhecida                                    | [Criando um novo gatilho](creating-a-new-trigger.md)                                 |
| Criando um gatilho ocioso baseado em evento para uma tarefa conhecida                      | [Criando um exemplo de gatilho de ociosidade](creating-an-idle-trigger-example.md)             |
| Recuperando a cadeia de caracteres de gatilho de todos os gatilhos associados a uma tarefa conhecida | [Exemplo de recuperação de cadeias de caracteres de gatilho](retrieving-trigger-strings-example.md)         |



 

 

 