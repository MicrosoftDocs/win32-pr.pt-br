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
# <a name="how-to-get-user-input-from-a-task-dialog"></a><span data-ttu-id="3d630-103">Como obter entrada do usuário de uma caixa de diálogo de tarefas</span><span class="sxs-lookup"><span data-stu-id="3d630-103">How to Get User Input from a Task Dialog</span></span>

<span data-ttu-id="3d630-104">Para concluir uma tarefa, os usuários enviam os detalhes da tarefa para o aplicativo Configurando os controles dentro da caixa de diálogo de tarefa e clicando em um botão de comando (normalmente **OK**).</span><span class="sxs-lookup"><span data-stu-id="3d630-104">To complete a task, users submit the task details to the application by configuring the controls within the task dialog, and then clicking a command button (usually **OK**).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="3d630-105">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="3d630-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="3d630-106">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="3d630-106">Technologies</span></span>

-   [<span data-ttu-id="3d630-107">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="3d630-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="3d630-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="3d630-108">Prerequisites</span></span>

-   <span data-ttu-id="3d630-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="3d630-109">C/C++</span></span>
-   <span data-ttu-id="3d630-110">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="3d630-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="3d630-111">Instruções</span><span class="sxs-lookup"><span data-stu-id="3d630-111">Instructions</span></span>

### <a name="getting-user-input-from-a-task-dialog"></a><span data-ttu-id="3d630-112">Obtendo entrada do usuário de uma caixa de diálogo de tarefa</span><span class="sxs-lookup"><span data-stu-id="3d630-112">Getting User Input from a Task Dialog</span></span>

<span data-ttu-id="3d630-113">Você pode identificar o botão que foi clicado examinando o parâmetro *pnButton* da função de chamada.</span><span class="sxs-lookup"><span data-stu-id="3d630-113">You can identify the button that was clicked by examining the *pnButton* parameter of the calling function.</span></span> <span data-ttu-id="3d630-114">Você também pode identificar o botão de opção selecionado do parâmetro *pnRadioButton* de [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)e o estado da caixa de seleção de verificação do parâmetro *pfVerificationFlagChecked* .</span><span class="sxs-lookup"><span data-stu-id="3d630-114">You can also identify the selected radio button from the *pnRadioButton* parameter of [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect), and the state of the verification check box from the *pfVerificationFlagChecked* parameter.</span></span>

<span data-ttu-id="3d630-115">Clica em botões e hiperlinks são recebidos pela função [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) na forma de [TDN \_ Button \_ clicked](tdn-button-clicked.md) e [TDN \_ Hyperlink \_ clicou](tdn-hyperlink-clicked.md) em notificações.</span><span class="sxs-lookup"><span data-stu-id="3d630-115">Clicks on buttons and hyperlinks are received by the [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) function in the form of [TDN\_BUTTON\_CLICKED](tdn-button-clicked.md) and [TDN\_HYPERLINK\_CLICKED](tdn-hyperlink-clicked.md) notifications.</span></span> <span data-ttu-id="3d630-116">Se sua função de retorno de chamada retornar S \_ OK após manipular uma notificação de botão, a caixa de diálogo de tarefa será fechada e o identificador de comando do botão será retornado em *pnButton*.</span><span class="sxs-lookup"><span data-stu-id="3d630-116">If your callback function returns S\_OK after handling a button notification, the task dialog closes and the command identifier of the button is returned in *pnButton*.</span></span> <span data-ttu-id="3d630-117">Se você retornar S \_ false ou não tiver uma função de retorno de chamada, a caixa de diálogo de tarefa permanecerá aberta.</span><span class="sxs-lookup"><span data-stu-id="3d630-117">If you return S\_FALSE, or do not have a callback function, the task dialog remains open.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d630-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3d630-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d630-119">Usando caixas de diálogo de tarefas</span><span class="sxs-lookup"><span data-stu-id="3d630-119">Using Task Dialogs</span></span>](using-task-dialogs.md)
</dt> </dl>

 

 