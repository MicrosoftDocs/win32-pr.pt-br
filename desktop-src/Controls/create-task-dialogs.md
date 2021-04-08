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
# <a name="how-to-create-task-dialogs"></a><span data-ttu-id="f2500-103">Como criar caixas de diálogo de tarefas</span><span class="sxs-lookup"><span data-stu-id="f2500-103">How to Create Task Dialogs</span></span>

<span data-ttu-id="f2500-104">Uma caixa de diálogo de tarefa é criada e mostrada usando a função [**TaskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog) ou a função [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="f2500-104">A task dialog is created and shown by using either the [**TaskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog) function or the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="f2500-105">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="f2500-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f2500-106">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="f2500-106">Technologies</span></span>

-   [<span data-ttu-id="f2500-107">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="f2500-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="f2500-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="f2500-108">Prerequisites</span></span>

-   <span data-ttu-id="f2500-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="f2500-109">C/C++</span></span>
-   <span data-ttu-id="f2500-110">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="f2500-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="f2500-111">Instruções</span><span class="sxs-lookup"><span data-stu-id="f2500-111">Instructions</span></span>

### <a name="taskdialog"></a><span data-ttu-id="f2500-112">TaskDialog</span><span class="sxs-lookup"><span data-stu-id="f2500-112">TaskDialog</span></span>

<span data-ttu-id="f2500-113">A função **TaskDialog** é adequada para caixas de diálogo simples que apresentam informações textuais e solicitam uma escolha padrão.</span><span class="sxs-lookup"><span data-stu-id="f2500-113">The **TaskDialog** function is suitable for simple dialog boxes that present textual information and ask for a standard choice.</span></span> <span data-ttu-id="f2500-114">Esta função de criação não oferece suporte a barras de progresso, caixas de seleção, rodapés, botões de expansão/recolhimento, botões personalizados ou botões de opção.</span><span class="sxs-lookup"><span data-stu-id="f2500-114">This creation function does not support progress bars, check boxes, footers, expand/collapse buttons, custom buttons, or radio buttons.</span></span>

### <a name="taskdialogindirect"></a><span data-ttu-id="f2500-115">TaskDialogIndirect</span><span class="sxs-lookup"><span data-stu-id="f2500-115">TaskDialogIndirect</span></span>

<span data-ttu-id="f2500-116">A função **TaskDialogIndirect** é mais potente, dando suporte a todos os elementos de interface disponíveis e também permite que você capture eventos em um procedimento de retorno de chamada para que seu aplicativo possa atualizar uma barra de progresso ou responder a um clique de um hiperlink ou botão.</span><span class="sxs-lookup"><span data-stu-id="f2500-116">The **TaskDialogIndirect** function is more powerful, supporting all available interface elements and also enabling you to capture events in a callback procedure so that your application can update a progress bar or respond to a click of a hyperlink or button.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2500-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f2500-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2500-118">Usando caixas de diálogo de tarefas</span><span class="sxs-lookup"><span data-stu-id="f2500-118">Using Task Dialogs</span></span>](using-task-dialogs.md)
</dt> </dl>

 

 




