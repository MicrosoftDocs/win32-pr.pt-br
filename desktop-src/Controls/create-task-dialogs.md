---
title: Como criar caixas de diálogo de tarefas
description: Uma caixa de diálogo de tarefa é criada e mostrada usando a função TaskDialog ou a função TaskDialogIndirect.
ms.assetid: CCEFF52F-D501-4145-9799-0A9C529017E1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ea8e3097454505acccf60c7cba3ef56c637af0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005092"
---
# <a name="how-to-create-task-dialogs"></a>Como criar caixas de diálogo de tarefas

Uma caixa de diálogo de tarefa é criada e mostrada usando a função [**TaskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog) ou a função [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="taskdialog"></a>TaskDialog

A função **TaskDialog** é adequada para caixas de diálogo simples que apresentam informações textuais e solicitam uma escolha padrão. Esta função de criação não oferece suporte a barras de progresso, caixas de seleção, rodapés, botões de expansão/recolhimento, botões personalizados ou botões de opção.

### <a name="taskdialogindirect"></a>TaskDialogIndirect

A função **TaskDialogIndirect** é mais potente, dando suporte a todos os elementos de interface disponíveis e também permite que você capture eventos em um procedimento de retorno de chamada para que seu aplicativo possa atualizar uma barra de progresso ou responder a um clique de um hiperlink ou botão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando caixas de diálogo de tarefas](using-task-dialogs.md)
</dt> </dl>

 

 




