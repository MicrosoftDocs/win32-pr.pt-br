---
title: Enumerando tarefas e exibindo informações de tarefas
description: A exibição de informações sobre uma tarefa, como o nome da tarefa, o estado ou a última vez que a tarefa foi executada, é feita pela enumeração por meio de tarefas em execução ou pelas tarefas em uma pasta de tarefas e pela exibição das informações desejadas.
ms.assetid: a0305089-89ff-42b7-b3f1-99a6484d2e5e
keywords:
- Enumerando tarefas Agendador de Tarefas
- Exemplos de Agendador de Tarefas Agendador de Tarefas, enumerando tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e4c1bbad0a1fa8892e38a001ff54e665f0c144
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634828"
---
# <a name="enumerating-tasks-and-displaying-task-information"></a>Enumerando tarefas e exibindo informações de tarefas

A exibição de informações sobre uma tarefa, como o nome da tarefa, o estado ou a última vez que a tarefa foi executada, é feita pela enumeração por meio de tarefas em execução ou pelas tarefas em uma pasta de tarefas e pela exibição das informações desejadas.

## <a name="accessing-properties-of-registered-tasks"></a>Acessando Propriedades de tarefas registradas

Para exibir o valor da propriedade de uma tarefa registrada, você deve se conectar ao serviço de Agendador de Tarefas e obter uma instância da pasta de tarefas que contém as tarefas das quais você deseja obter informações. Em seguida, você obtém uma coleção de todas as tarefas registradas na pasta tarefa. Em seguida, você enumerará cada tarefa registrada e obterá e exibirá um valor de propriedade para cada tarefa.

## <a name="accessing-properties-of-running-tasks"></a>Acessando Propriedades de tarefas em execução

Para exibir o valor da propriedade de uma tarefa em execução, você deve se conectar ao serviço de Agendador de Tarefas e obter uma coleção de todas as tarefas em execução (incluindo ou excluindo tarefas ocultas). Em seguida, você enumerará cada tarefa em execução e obterá e exibirá um valor de propriedade para cada tarefa.

## <a name="example"></a>Exemplo

Os exemplos a seguir enumeram tarefas e exibem o nome e o estado das tarefas:

-   [Exibindo nomes e Estados de tarefas (scripts)](displaying-task-names-and-state--scripting-.md)
-   [Exibindo nomes e estado da tarefa (C++)](displaying-task-names-and-state--c---.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Agendador de Tarefas](using-the-task-scheduler.md)
</dt> </dl>

 

 




