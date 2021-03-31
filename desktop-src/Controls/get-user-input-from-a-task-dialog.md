---
title: Como obter entrada do usuário de uma caixa de diálogo de tarefas
description: Para concluir uma tarefa, os usuários enviam os detalhes da tarefa para o aplicativo Configurando os controles dentro da caixa de diálogo de tarefa e clicando em um botão de comando (normalmente OK).
ms.assetid: 73CD8FBF-95C9-43C8-B9D8-3823840C23A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd53c8051747187123821211ac7e17c9915b5fd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917732"
---
# <a name="how-to-get-user-input-from-a-task-dialog"></a>Como obter entrada do usuário de uma caixa de diálogo de tarefas

Para concluir uma tarefa, os usuários enviam os detalhes da tarefa para o aplicativo Configurando os controles dentro da caixa de diálogo de tarefa e clicando em um botão de comando (normalmente **OK**).

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="getting-user-input-from-a-task-dialog"></a>Obtendo entrada do usuário de uma caixa de diálogo de tarefa

Você pode identificar o botão que foi clicado examinando o parâmetro *pnButton* da função de chamada. Você também pode identificar o botão de opção selecionado do parâmetro *pnRadioButton* de [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)e o estado da caixa de seleção de verificação do parâmetro *pfVerificationFlagChecked* .

Clica em botões e hiperlinks são recebidos pela função [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) na forma de [TDN \_ Button \_ clicked](tdn-button-clicked.md) e [TDN \_ Hyperlink \_ clicou](tdn-hyperlink-clicked.md) em notificações. Se sua função de retorno de chamada retornar S \_ OK após manipular uma notificação de botão, a caixa de diálogo de tarefa será fechada e o identificador de comando do botão será retornado em *pnButton*. Se você retornar S \_ false ou não tiver uma função de retorno de chamada, a caixa de diálogo de tarefa permanecerá aberta.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando caixas de diálogo de tarefas](using-task-dialogs.md)
</dt> </dl>

 

 