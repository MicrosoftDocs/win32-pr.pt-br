---
description: Este tópico descreve como exibir o progresso do trabalho de impressão para o usuário e dar a eles a opção de cancelar um trabalho de impressão que está atualmente em andamento.
ms.assetid: 2b7a0ab7-bf7e-473d-ab43-8b79478d4453
title: Como exibir o progresso do trabalho de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9effc778f6affaba5b53cbd96a7a428ea5554d8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789921"
---
# <a name="how-to-display-the-print-job-progress"></a><span data-ttu-id="b74c2-103">Como exibir o progresso do trabalho de impressão</span><span class="sxs-lookup"><span data-stu-id="b74c2-103">How To: Display the Print Job Progress</span></span>

<span data-ttu-id="b74c2-104">Este tópico descreve como exibir o progresso do trabalho de impressão para o usuário e dar a eles a opção de cancelar um trabalho de impressão que está atualmente em andamento.</span><span class="sxs-lookup"><span data-stu-id="b74c2-104">This topic describes how to display the print job progress to the user and give them the option to cancel a print job that is currently in progress.</span></span>

## <a name="overview"></a><span data-ttu-id="b74c2-105">Visão geral</span><span class="sxs-lookup"><span data-stu-id="b74c2-105">Overview</span></span>

<span data-ttu-id="b74c2-106">Um procedimento de caixa de diálogo de progresso de impressão normalmente executa as funções a seguir.</span><span class="sxs-lookup"><span data-stu-id="b74c2-106">A print progress dialog procedure typically performs the following functions.</span></span>

-   <span data-ttu-id="b74c2-107">Exibir o progresso do trabalho de impressão para o usuário.</span><span class="sxs-lookup"><span data-stu-id="b74c2-107">Display print job progress to the user.</span></span>
-   <span data-ttu-id="b74c2-108">Inicie o thread de processamento de impressão.</span><span class="sxs-lookup"><span data-stu-id="b74c2-108">Start the print processing thread.</span></span>
-   <span data-ttu-id="b74c2-109">Exibir um botão de **cancelamento** para que o usuário possa interromper um trabalho de impressão antes de ser concluído.</span><span class="sxs-lookup"><span data-stu-id="b74c2-109">Display a **Cancel** button so the user can stop a print job before it finishes.</span></span>

<span data-ttu-id="b74c2-110">Estritamente falando, a única coisa que o procedimento da caixa de diálogo de progresso da impressão deve fazer é exibir o progresso do trabalho de impressão para o usuário.</span><span class="sxs-lookup"><span data-stu-id="b74c2-110">Strictly speaking, the only thing that the print progress dialog box procedure must do is display the print job progress to the user.</span></span> <span data-ttu-id="b74c2-111">No entanto, como as outras duas funções na lista anterior estão fortemente relacionadas, elas também foram incluídas neste módulo.</span><span class="sxs-lookup"><span data-stu-id="b74c2-111">However, because the other two functions in the preceding list are closely related, they have also been included in this module.</span></span>

## <a name="displaying-print-job-progress"></a><span data-ttu-id="b74c2-112">Exibindo o progresso do trabalho de impressão</span><span class="sxs-lookup"><span data-stu-id="b74c2-112">Displaying Print Job Progress</span></span>

<span data-ttu-id="b74c2-113">Um procedimento de caixa de diálogo de progresso de impressão manipula as seguintes mensagens de janela.</span><span class="sxs-lookup"><span data-stu-id="b74c2-113">A print progress dialog box procedure handles the following window messages.</span></span>

-   <span data-ttu-id="b74c2-114">**INITDIALOG do WM \_**</span><span class="sxs-lookup"><span data-stu-id="b74c2-114">**WM\_INITDIALOG**</span></span>

    <span data-ttu-id="b74c2-115">Inicializa os controles que a caixa de diálogo usa.</span><span class="sxs-lookup"><span data-stu-id="b74c2-115">Initializes the controls that the dialog box uses.</span></span>

-   <span data-ttu-id="b74c2-116">**WM \_ SETcursor**</span><span class="sxs-lookup"><span data-stu-id="b74c2-116">**WM\_SETCURSOR**</span></span>

    <span data-ttu-id="b74c2-117">Define o cursor para um ponteiro quando o usuário é capaz de cancelar um trabalho de impressão e para o cursor de espera quando o trabalho de impressão está em um ponto em que não pode ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="b74c2-117">Sets the cursor to a pointer when the user is able to cancel a print job, and to the wait cursor when the print job is at a point where it cannot be cancelled.</span></span>

-   <span data-ttu-id="b74c2-118">**impressão de \_ início de impressão do usuário \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b74c2-118">**USER\_PRINT\_START\_PRINTING**</span></span>

    <span data-ttu-id="b74c2-119">Define os parâmetros da barra de progresso para o trabalho de impressão e cria o thread de impressão para iniciar o processamento do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="b74c2-119">Sets the progress bar parameters for the print job, and creates the printing thread to start processing the print job.</span></span>

    <span data-ttu-id="b74c2-120">Esta é uma mensagem de janela específica do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b74c2-120">This is an application-specific window message.</span></span>

-   <span data-ttu-id="b74c2-121">**comando do WM \_ – IDCANCEL**</span><span class="sxs-lookup"><span data-stu-id="b74c2-121">**WM\_COMMAND - IDCANCEL**</span></span>

    <span data-ttu-id="b74c2-122">Define o evento de cancelamento para instruir o thread de processamento de impressão a cancelar o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="b74c2-122">Sets the cancel event to tell the print processing thread to cancel the print job.</span></span>

-   <span data-ttu-id="b74c2-123">**\_atualização do \_ status de impressão do usuário \_**</span><span class="sxs-lookup"><span data-stu-id="b74c2-123">**USER\_PRINT\_STATUS\_UPDATE**</span></span>

    <span data-ttu-id="b74c2-124">Atualiza a barra de progresso e o texto de status para mostrar o estado atual do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="b74c2-124">Updates the progress bar and status text to show the current state of the print job.</span></span>

    <span data-ttu-id="b74c2-125">Esta é uma mensagem de janela específica do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b74c2-125">This is an application-specific window message.</span></span>

-   <span data-ttu-id="b74c2-126">**\_fechamento de impressão do usuário \_**</span><span class="sxs-lookup"><span data-stu-id="b74c2-126">**USER\_PRINT\_CLOSING**</span></span>

    <span data-ttu-id="b74c2-127">Define o texto de status de fechamento na caixa de diálogo progresso para indicar que o trabalho de impressão está sendo fechado.</span><span class="sxs-lookup"><span data-stu-id="b74c2-127">Sets the closing status text in the progress dialog box to indicate that the print job is closing.</span></span>

    <span data-ttu-id="b74c2-128">Esta é uma mensagem de janela específica do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b74c2-128">This is an application-specific window message.</span></span>

-   <span data-ttu-id="b74c2-129">**impressão do usuário \_ \_ concluída**</span><span class="sxs-lookup"><span data-stu-id="b74c2-129">**USER\_PRINT\_COMPLETE**</span></span>

    <span data-ttu-id="b74c2-130">Exibe a mensagem "trabalho de impressão concluído" para o usuário e libera identificadores e eventos que foram usados neste trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="b74c2-130">Displays the "Print job complete" message to the user, and releases handles and events that were used in this print job.</span></span>

    <span data-ttu-id="b74c2-131">Esta é uma mensagem de janela específica do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b74c2-131">This is an application-specific window message.</span></span>

 

 



