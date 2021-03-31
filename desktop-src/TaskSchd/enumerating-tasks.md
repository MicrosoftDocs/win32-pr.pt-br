---
title: Enumerando tarefas
description: Agendador de Tarefas 1,0 fornece um objeto de enumeração para enumerar as tarefas na pasta tarefas agendadas.
ms.assetid: ccd140a1-06f6-4e6b-afa6-f7ac9b9ff904
keywords:
- Enumerando tarefas Agendador de Tarefas
- Enumerando tarefas Agendador de Tarefas, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81dda98cf40bc1ea360d20bcf13084faa692aa22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005813"
---
# <a name="enumerating-tasks"></a>Enumerando tarefas

Agendador de Tarefas 1,0 fornece um objeto de enumeração para enumerar as tarefas na [*pasta tarefas agendadas*](s.md).

> [!Note]  
> Para um computador com Windows Server 2003, Windows XP ou Windows 2000 para criar, monitorar ou controlar tarefas em um computador com Windows Vista, determinadas operações devem ser concluídas no computador com Windows Vista. Para obter mais informações, consulte [Tarefas](tasks.md).

 

## <a name="using-the-enumeration-object"></a>Usando o objeto de enumeração

A interface [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) desse objeto fornece métodos para enumerar as tarefas na pasta, redefinir a sequência de enumeração para o início da lista, ignorar tarefas e fazer uma cópia do objeto de enumeração atual para uso posterior.

Para obter informações sobre como enumerar as tarefas na pasta tarefas agendadas, consulte [**IEnumWorkItems:: Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next).

Para obter informações sobre como redefinir a enumeração para o início da lista, consulte [**IEnumWorkItems:: Reset**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-reset).

Para obter informações sobre como ignorar tarefas, consulte [**IEnumWorkItems:: Skip**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-skip).

Para obter informações sobre como fazer uma cópia do objeto de enumeração atual, consulte [**IEnumWorkItems:: clone**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-clone).

Para obter um exemplo de como enumerar as tarefas na pasta tarefas agendadas, consulte o [exemplo enumerando tarefas](enumerating-tasks-example.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Informações da tarefa Agendador de Tarefas 1,0](task-scheduler-1-0-task-informatation.md)
</dt> </dl>

 

 




