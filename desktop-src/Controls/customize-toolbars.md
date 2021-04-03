---
title: Como personalizar barras de ferramentas
description: A maioria dos aplicativos baseados no Windows usa controles da barra de ferramentas para fornecer aos usuários acesso conveniente à funcionalidade do programa.
ms.assetid: 0CE2988E-D887-433B-BFB2-5F3442E8E1B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091451a139cf846b1106916f28c165d6640699eb
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "104007264"
---
# <a name="how-to-customize-toolbars"></a><span data-ttu-id="a8fb7-103">Como personalizar barras de ferramentas</span><span class="sxs-lookup"><span data-stu-id="a8fb7-103">How to Customize Toolbars</span></span>

<span data-ttu-id="a8fb7-104">A maioria dos aplicativos baseados no Windows usa controles da barra de ferramentas para fornecer aos usuários acesso conveniente à funcionalidade do programa.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-104">Most Windows-based applications use toolbar controls to provide users with convenient access to the program functionality.</span></span> <span data-ttu-id="a8fb7-105">No entanto, as barras de ferramentas estáticas têm algumas deficiências — por exemplo, pouco espaço para exibir efetivamente todas as ferramentas disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-105">However, static toolbars have some shortcomings—such as too little space to effectively display all the available tools.</span></span> <span data-ttu-id="a8fb7-106">A solução para esse problema é tornar as barras de ferramentas do aplicativo personalizáveis pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-106">The solution to this problem is to make your application's toolbars user-customizable.</span></span> <span data-ttu-id="a8fb7-107">Em seguida, os usuários podem optar por exibir apenas as ferramentas de que precisam e podem organizá-los de uma forma que se adaptem ao seu organizador de trabalho pessoal.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-107">Then, users can choose to display only the tools they need, and they can organize them in a way that suits their personal workstyle.</span></span>

> [!Note]  
> <span data-ttu-id="a8fb7-108">As barras de ferramentas nas caixas de diálogo não podem ser personalizadas.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-108">Toolbars in dialog boxes cannot be customized.</span></span>

 

<span data-ttu-id="a8fb7-109">Para habilitar a personalização, inclua o sinalizador estilo de controles comuns de [**ccs \_ ajustável**](common-control-styles.md) ao criar o controle da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-109">To enable customization, include the [**CCS\_ADJUSTABLE**](common-control-styles.md) common controls style flag when you create the toolbar control.</span></span> <span data-ttu-id="a8fb7-110">Há duas abordagens básicas para a personalização:</span><span class="sxs-lookup"><span data-stu-id="a8fb7-110">There are two basic approaches to customization:</span></span>

-   <span data-ttu-id="a8fb7-111">A caixa de diálogo personalização.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-111">The customization dialog box.</span></span> <span data-ttu-id="a8fb7-112">Essa caixa de diálogo fornecida pelo sistema é a abordagem mais simples.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-112">This system-provided dialog box is the simplest approach.</span></span> <span data-ttu-id="a8fb7-113">Ele fornece aos usuários uma interface gráfica do usuário que permite adicionar, excluir ou mover ícones.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-113">It gives users a graphical user interface that allows them to add, delete, or move icons.</span></span>
-   <span data-ttu-id="a8fb7-114">Ferramentas de arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-114">Dragging and dropping tools.</span></span> <span data-ttu-id="a8fb7-115">A implementação da funcionalidade de arrastar e soltar permite aos usuários mover ferramentas para outro local na barra de ferramentas ou excluí-las arrastando-as para fora da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-115">Implementing drag-and-drop functionality allows users to move tools to another location on the toolbar or delete them by dragging them off the toolbar.</span></span> <span data-ttu-id="a8fb7-116">Ele fornece aos usuários uma maneira rápida e fácil de organizar sua barra de ferramentas, mas não permite que elas adicionem ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-116">It provides users a quick and easy way to organize their toolbar, but does not allow them to add tools.</span></span>

<span data-ttu-id="a8fb7-117">Você pode implementar uma das abordagens ou ambas, dependendo das necessidades do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-117">You can implement either approach or both, depending on the needs of the application.</span></span> <span data-ttu-id="a8fb7-118">Nenhuma dessas duas abordagens à personalização fornece um mecanismo interno, como um botão cancelar ou desfazer, para retornar a barra de ferramentas ao estado anterior.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-118">Neither of these two approaches to customization provides a built-in mechanism, such as a Cancel or Undo button, to return the toolbar to its former state.</span></span> <span data-ttu-id="a8fb7-119">Você deve usar explicitamente a API de controle da barra de ferramentas para armazenar o estado de prepersonalização da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-119">You must explicitly use the toolbar control API to store the toolbar's precustomization state.</span></span> <span data-ttu-id="a8fb7-120">Se necessário, você pode usar essas informações armazenadas posteriormente para restaurar a barra de ferramentas ao seu estado original.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-120">If necessary, you can later use this stored information to restore the toolbar to its original state.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a8fb7-121">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="a8fb7-121">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a8fb7-122">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="a8fb7-122">Technologies</span></span>

-   [<span data-ttu-id="a8fb7-123">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="a8fb7-123">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a8fb7-124">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="a8fb7-124">Prerequisites</span></span>

-   <span data-ttu-id="a8fb7-125">C/C++</span><span class="sxs-lookup"><span data-stu-id="a8fb7-125">C/C++</span></span>
-   <span data-ttu-id="a8fb7-126">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="a8fb7-126">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a8fb7-127">Instruções</span><span class="sxs-lookup"><span data-stu-id="a8fb7-127">Instructions</span></span>

### <a name="customization-dialog-box"></a><span data-ttu-id="a8fb7-128">Caixa de diálogo personalização</span><span class="sxs-lookup"><span data-stu-id="a8fb7-128">Customization Dialog Box</span></span>

<span data-ttu-id="a8fb7-129">A caixa de diálogo personalização é fornecida pelo controle barra de ferramentas para fornecer aos usuários uma maneira simples de adicionar, mover ou excluir ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-129">The customization dialog box is provided by the toolbar control to give users a simple way to add, move, or delete tools.</span></span> <span data-ttu-id="a8fb7-130">Os usuários podem iniciá-lo clicando duas vezes na barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-130">Users can launch it by double-clicking the toolbar.</span></span> <span data-ttu-id="a8fb7-131">Os aplicativos podem iniciar a caixa de diálogo de personalização programaticamente enviando o controle Toolbar a uma mensagem de [**\_ personalização de TB**](tb-customize.md) .</span><span class="sxs-lookup"><span data-stu-id="a8fb7-131">Applications can launch the customization dialog box programmatically by sending the toolbar control a [**TB\_CUSTOMIZE**](tb-customize.md) message.</span></span>

<span data-ttu-id="a8fb7-132">A ilustração a seguir mostra um exemplo da caixa de diálogo personalização da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-132">The following illustration shows an example of the toolbar customization dialog box.</span></span>

![captura de tela de uma janela com uma barra de ferramentas de três itens e uma caixa de diálogo com listas dos botões da barra de ferramentas disponível e atual](images/tb-customdlg.png)

<span data-ttu-id="a8fb7-134">As ferramentas na caixa de listagem à direita são aquelas atualmente na barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-134">The tools in the list box on the right are those currently on the toolbar.</span></span> <span data-ttu-id="a8fb7-135">Inicialmente, essa lista conterá as ferramentas que você especificar ao criar a barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-135">Initially, this list will contain the tools that you specify when you create the toolbar.</span></span> <span data-ttu-id="a8fb7-136">A caixa de listagem à esquerda contém as ferramentas que estão disponíveis para adicionar à barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-136">The list box in the left contains the tools that are available to add to the toolbar.</span></span> <span data-ttu-id="a8fb7-137">Seu aplicativo é responsável por preencher essa lista (diferente de com o separador, que aparece automaticamente).</span><span class="sxs-lookup"><span data-stu-id="a8fb7-137">Your application is responsible for populating that list (other than with the Separator, which appears automatically).</span></span>

<span data-ttu-id="a8fb7-138">O controle Toolbar notifica seu aplicativo de que ele está iniciando uma caixa de diálogo de personalização enviando a janela pai um código de notificação [tbn \_ BEGINADJUST](tbn-beginadjust.md) seguido por um código de notificação [tbn \_ INITCUSTOMIZE](tbn-initcustomize.md) .</span><span class="sxs-lookup"><span data-stu-id="a8fb7-138">The toolbar control notifies your application that it is launching a customization dialog box by sending its parent window a [TBN\_BEGINADJUST](tbn-beginadjust.md) notification code followed by a [TBN\_INITCUSTOMIZE](tbn-initcustomize.md) notification code.</span></span> <span data-ttu-id="a8fb7-139">Na maioria dos casos, o aplicativo não precisa responder a esses códigos de notificação.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-139">In most cases, the application does not need to respond to these notification codes.</span></span> <span data-ttu-id="a8fb7-140">No entanto, se você não quiser que a caixa de diálogo Personalizar barra de ferramentas exiba um botão ajuda, manipule TBN \_ INITCUSTOMIZE retornando TBNRF \_ HIDEHELP.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-140">However, if you do not want the Customize Toolbar dialog box to display a Help button, handle TBN\_INITCUSTOMIZE by returning TBNRF\_HIDEHELP.</span></span>

<span data-ttu-id="a8fb7-141">O controle ToolBar, em seguida, coleta as informações necessárias para inicializar a caixa de diálogo enviando três séries de códigos de notificação, na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="a8fb7-141">The toolbar control then collects the information it needs to initialize the dialog box by sending three series of notification codes, in the following order:</span></span>

-   <span data-ttu-id="a8fb7-142">Um código de notificação [tbn \_ QUERYINSERT](tbn-queryinsert.md) para cada botão na barra de ferramentas para determinar onde os botões podem ser inseridos.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-142">A [TBN\_QUERYINSERT](tbn-queryinsert.md) notification code for each button on the toolbar to determine where buttons can be inserted.</span></span> <span data-ttu-id="a8fb7-143">Retorne **false** para impedir que um botão seja inserido à esquerda do botão especificado na mensagem de notificação.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-143">Return **FALSE** to prevent a button from being inserted to the left of the button specified in the notification message.</span></span> <span data-ttu-id="a8fb7-144">Se você retornar **false** para todos os \_ códigos de notificação tbn QUERYINSERT, a caixa de diálogo não será exibida.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-144">If you return **FALSE** to all TBN\_QUERYINSERT notification codes, the dialog box will not be displayed.</span></span>
-   <span data-ttu-id="a8fb7-145">Um código de notificação [tbn \_ QUERYDELETE](tbn-querydelete.md) para cada ferramenta que está atualmente na barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-145">A [TBN\_QUERYDELETE](tbn-querydelete.md) notification code for each tool that is currently on the toolbar.</span></span> <span data-ttu-id="a8fb7-146">Retorna **true** se uma ferramenta puder ser excluída ou **false** se não.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-146">Return **TRUE** if a tool can be deleted, or **FALSE** if not.</span></span>
-   <span data-ttu-id="a8fb7-147">Uma série de códigos de notificação [tbn \_ GETBUTTONINFO](tbn-getbuttoninfo.md) para popular a lista de botões disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-147">A series of [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md) notification codes to populate the list of available buttons.</span></span> <span data-ttu-id="a8fb7-148">Para adicionar um botão à lista, preencha a estrutura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) que é passada com o código de notificação e retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-148">To add a button to the list, fill in the [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that is passed with the notification code and return **TRUE**.</span></span> <span data-ttu-id="a8fb7-149">Quando você não tiver mais ferramentas para adicionar, retorne **false**.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-149">When you have no more tools to add, return **FALSE**.</span></span> <span data-ttu-id="a8fb7-150">Observe que você pode retornar informações para botões que já estão na barra de ferramentas; esses botões não serão adicionados à lista.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-150">Note that you can return information for buttons that are already on the toolbar; these buttons will not be added to the list.</span></span>

<span data-ttu-id="a8fb7-151">A caixa de diálogo é exibida e o usuário pode começar a personalizar a barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-151">The dialog box is then displayed, and the user can begin to customize the toolbar.</span></span>

<span data-ttu-id="a8fb7-152">Quando a caixa de diálogo estiver aberta, seu aplicativo poderá receber uma variedade de códigos de notificação, dependendo das ações do usuário:</span><span class="sxs-lookup"><span data-stu-id="a8fb7-152">When the dialog box is open, your application can receive a variety of notification codes, depending on the user's actions:</span></span>

-   <span data-ttu-id="a8fb7-153">[Tbn \_ QUERYINSERT](tbn-queryinsert.md).</span><span class="sxs-lookup"><span data-stu-id="a8fb7-153">[TBN\_QUERYINSERT](tbn-queryinsert.md).</span></span> <span data-ttu-id="a8fb7-154">O usuário alterou o local de uma ferramenta na barra de ferramentas ou adicionou uma ferramenta.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-154">The user has changed the location of a tool on the toolbar or added a tool.</span></span> <span data-ttu-id="a8fb7-155">Retorne **false** para impedir que a ferramenta seja inserida nesse local.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-155">Return **FALSE** to prevent the tool from being inserted at that location.</span></span>
-   <span data-ttu-id="a8fb7-156">[Tbn \_ DELETINGBUTTON](tbn-deletingbutton.md).</span><span class="sxs-lookup"><span data-stu-id="a8fb7-156">[TBN\_DELETINGBUTTON](tbn-deletingbutton.md).</span></span> <span data-ttu-id="a8fb7-157">O usuário está prestes a remover uma ferramenta da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-157">The user is about to remove a tool from the toolbar.</span></span>
-   <span data-ttu-id="a8fb7-158">[Tbn \_ CUSTHELP](tbn-custhelp.md).</span><span class="sxs-lookup"><span data-stu-id="a8fb7-158">[TBN\_CUSTHELP](tbn-custhelp.md).</span></span> <span data-ttu-id="a8fb7-159">O usuário clicou no botão ajuda.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-159">The user has clicked the Help button.</span></span>
-   <span data-ttu-id="a8fb7-160">[Tbn \_ TOOLBARCHANGE](tbn-toolbarchange.md).</span><span class="sxs-lookup"><span data-stu-id="a8fb7-160">[TBN\_TOOLBARCHANGE](tbn-toolbarchange.md).</span></span> <span data-ttu-id="a8fb7-161">O usuário adicionou, moveu ou excluiu uma ferramenta.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-161">The user has added, moved, or deleted a tool.</span></span>
-   <span data-ttu-id="a8fb7-162">[Tbn \_ REDEFINIR](tbn-reset.md).</span><span class="sxs-lookup"><span data-stu-id="a8fb7-162">[TBN\_RESET](tbn-reset.md).</span></span> <span data-ttu-id="a8fb7-163">O usuário clicou no botão redefinir.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-163">The user has clicked the Reset button.</span></span>

<span data-ttu-id="a8fb7-164">Depois que a caixa de diálogo for destruída, seu aplicativo receberá um código de notificação [tbn \_ endadjust](tbn-endadjust.md) .</span><span class="sxs-lookup"><span data-stu-id="a8fb7-164">After the dialog box is destroyed, your application will receive a [TBN\_ENDADJUST](tbn-endadjust.md) notification code.</span></span>

<span data-ttu-id="a8fb7-165">O exemplo de código a seguir mostra uma maneira de implementar a personalização da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-165">The following code example shows one way to implement toolbar customization.</span></span>


```C++
// The buttons are stored in an array of TBBUTTON structures. 
//
// Constants such as STD_FILENEW are identifiers for the 
// built-in bitmaps that have already been assigned as the toolbar's 
// image list.
//
// Constants such as IDM_NEW are application-defined command identifiers.

TBBUTTON allButtons[] = 
    {
        { MAKELONG(STD_FILENEW,  ImageListID), IDM_NEW,   TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"New" },
        { MAKELONG(STD_FILEOPEN, ImageListID), IDM_OPEN,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Open"},
        { MAKELONG(STD_FILESAVE, ImageListID), IDM_SAVE,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Save"},
        { MAKELONG(STD_CUT,      ImageListID), IDM_CUT,   TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Cut" },
        { MAKELONG(STD_COPY,     ImageListID), IDM_COPY,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Copy"},
        { MAKELONG(STD_PASTE,    ImageListID), IDM_PASTE, TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Paste"}
    };

// The following appears in the window's message handler.

case WM_NOTIFY: 
    {
        switch (((LPNMHDR)lParam)->code) 
        {
        
        case TBN_GETBUTTONINFO:  
            {
                LPTBNOTIFY lpTbNotify = (LPTBNOTIFY)lParam;

                // Pass the next button from the array. There is no need to filter out buttons
                // that are already used—they will be ignored.
                
                int buttonCount = sizeof(allButtons) / sizeof(TBBUTTON);
                
                if (lpTbNotify->iItem < buttonCount)
                {
                    lpTbNotify->tbButton = allButtons[lpTbNotify->iItem];
                    return TRUE;
                }
                
                else
                
                {
                    return FALSE;  // No more buttons.
                }
            }
            
            break;

            case TBN_QUERYINSERT:
            
            case TBN_QUERYDELETE:
                return TRUE; 
        }
    }
```



### <a name="dragging-and-dropping-tools"></a><span data-ttu-id="a8fb7-166">Ferramentas de arrastar e soltar</span><span class="sxs-lookup"><span data-stu-id="a8fb7-166">Dragging and Dropping Tools</span></span>

<span data-ttu-id="a8fb7-167">Os usuários também podem reorganizar os botões em uma barra de ferramentas pressionando a tecla SHIFT e arrastando o botão para outro local.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-167">Users can also rearrange the buttons on a toolbar by pressing the SHIFT key and dragging the button to another location.</span></span> <span data-ttu-id="a8fb7-168">O processo de arrastar e soltar é manipulado automaticamente pelo controle da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-168">The drag-and-drop process is handled automatically by the toolbar control.</span></span> <span data-ttu-id="a8fb7-169">Ele exibe uma imagem fantasma do botão conforme ele é arrastado e reorganiza a barra de ferramentas depois que ela é descartada.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-169">It displays a ghost image of the button as it is dragged, and rearranges the toolbar after it is dropped.</span></span> <span data-ttu-id="a8fb7-170">Os usuários não podem adicionar botões dessa maneira, mas eles podem excluir um botão, removendo-o da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-170">Users cannot add buttons in this way, but they can delete a button by dropping it off the toolbar.</span></span>

<span data-ttu-id="a8fb7-171">Embora o controle Toolbar normalmente faça essa operação automaticamente, ele também envia os dois códigos de notificação do seu aplicativo: [tbn \_ QUERYDELETE](tbn-querydelete.md) e [tbn \_ QUERYINSERT](tbn-queryinsert.md).</span><span class="sxs-lookup"><span data-stu-id="a8fb7-171">Although the toolbar control normally does this operation automatically, it also sends your application two notification codes: [TBN\_QUERYDELETE](tbn-querydelete.md) and [TBN\_QUERYINSERT](tbn-queryinsert.md).</span></span> <span data-ttu-id="a8fb7-172">Para controlar o processo de arrastar e soltar, manipule esses códigos de notificação da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a8fb7-172">To control the drag-and-drop process, handle these notification codes as follows:</span></span>

-   <span data-ttu-id="a8fb7-173">O código de notificação [tbn \_ QUERYDELETE](tbn-querydelete.md) é enviado assim que o usuário tenta mover o botão, antes que o botão fantasma seja exibido.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-173">The [TBN\_QUERYDELETE](tbn-querydelete.md) notification code is sent as soon as the user attempts to move the button, before the ghost button is displayed.</span></span> <span data-ttu-id="a8fb7-174">Retorne **false** para impedir que o botão seja movido.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-174">Return **FALSE** to prevent the button from being moved.</span></span> <span data-ttu-id="a8fb7-175">Se você retornar **true**, o usuário poderá mover a ferramenta ou excluí-la removendo-a da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-175">If you return **TRUE**, the user will be able to either move the tool or delete it by dropping it off the toolbar.</span></span> <span data-ttu-id="a8fb7-176">Se uma ferramenta puder ser movida, ela poderá ser excluída.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-176">If a tool can be moved, it can be deleted.</span></span> <span data-ttu-id="a8fb7-177">No entanto, se o usuário excluir uma ferramenta, o controle Toolbar enviará ao seu aplicativo um código de notificação [tbn \_ DELETINGBUTTON](tbn-deletingbutton.md) , no ponto em que você pode optar por reinserir o botão em seu local original, cancelando assim a exclusão.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-177">However, if the user deletes a tool, the toolbar control will send your application a [TBN\_DELETINGBUTTON](tbn-deletingbutton.md) notification code, at which point you can choose to reinsert the button at its original location, thereby canceling the deletion.</span></span>
-   <span data-ttu-id="a8fb7-178">O código de notificação [tbn \_ QUERYINSERT](tbn-queryinsert.md) é enviado quando o usuário tenta soltar o botão na barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-178">The [TBN\_QUERYINSERT](tbn-queryinsert.md) notification code is sent when the user attempts to drop the button on the toolbar.</span></span> <span data-ttu-id="a8fb7-179">Para impedir que o botão que está sendo movido seja Descartado à esquerda do botão especificado na notificação, retorne **false**.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-179">To prevent the button that is being moved from being dropped to the left of the button specified in the notification, return **FALSE**.</span></span> <span data-ttu-id="a8fb7-180">Esse código de notificação não será enviado se o usuário descartar a ferramenta para fora da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-180">This notification code is not sent if the user drops the tool off the toolbar.</span></span>

<span data-ttu-id="a8fb7-181">Se o usuário tentar arrastar um botão sem também pressionar a tecla SHIFT, o controle Toolbar não tratará a operação de arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-181">If the user attempts to drag a button without also pressing the SHIFT key, the toolbar control will not handle the drag-and-drop operation.</span></span> <span data-ttu-id="a8fb7-182">No entanto, ele enviará ao seu aplicativo um código de notificação [tbn \_ BEGINDRAG](tbn-begindrag.md) para indicar o início de uma operação de arrastar e um código de notificação do [tbn \_ endarraste](tbn-enddrag.md) para indicar o final.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-182">However, it will send your application a [TBN\_BEGINDRAG](tbn-begindrag.md) notification code to indicate the start of a drag operation, and a [TBN\_ENDDRAG](tbn-enddrag.md) notification code to indicate the end.</span></span> <span data-ttu-id="a8fb7-183">Se você quiser habilitar essa forma de arrastar e soltar, seu aplicativo deverá lidar com esses códigos de notificação, fornecer a interface do usuário necessária e modificar a barra de ferramentas para refletir as alterações.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-183">If you want to enable this form of drag-and-drop, your application must handle these notification codes, provide the necessary user interface, and modify the toolbar to reflect any changes.</span></span>

### <a name="saving-and-restoring-toolbars"></a><span data-ttu-id="a8fb7-184">Salvando e restaurando barras de ferramentas</span><span class="sxs-lookup"><span data-stu-id="a8fb7-184">Saving and Restoring Toolbars</span></span>

<span data-ttu-id="a8fb7-185">No processo de personalização de uma barra de ferramentas, seu aplicativo pode precisar salvar informações para que você possa restaurar a barra de ferramentas para seu estado original.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-185">In the process of customizing a toolbar, your application might need to save information so that you can restore the toolbar to its original state.</span></span> <span data-ttu-id="a8fb7-186">Para iniciar o salvamento ou a restauração de um estado de barra de ferramentas, envie a barra de ferramentas para uma mensagem [**\_ SAVERESTORE TB**](tb-saverestore.md) com o *lParam* definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-186">To initiate saving or restoring a toolbar state, send the toolbar control a [**TB\_SAVERESTORE**](tb-saverestore.md) message with the *lParam* set to **TRUE**.</span></span> <span data-ttu-id="a8fb7-187">O valor de *lParam* dessa mensagem Especifica se você está solicitando uma operação de salvamento ou de restauração.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-187">The *lParam* value of this message specifies whether you are requesting a save or a restore operation.</span></span> <span data-ttu-id="a8fb7-188">Depois que a mensagem é enviada, há duas maneiras de lidar com a operação de salvar/restaurar:</span><span class="sxs-lookup"><span data-stu-id="a8fb7-188">After the message is sent, there are two ways to handle the save/restore operation:</span></span>

-   <span data-ttu-id="a8fb7-189">Com os controles comuns [versão 4,72](common-control-versions.md) e anteriores, você deve implementar um manipulador [tbn \_ GETBUTTONINFO](tbn-getbuttoninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="a8fb7-189">With common controls [version 4.72](common-control-versions.md) and earlier, you must implement a [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md) handler.</span></span> <span data-ttu-id="a8fb7-190">O controle Toolbar envia esse código de notificação para solicitar informações sobre cada botão à medida que ele é restaurado.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-190">The toolbar control sends this notification code to request information about each button as it is restored.</span></span>
-   <span data-ttu-id="a8fb7-191">A versão 5,80 inclui uma opção salvar/restaurar.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-191">Version 5.80 includes a save/restore option.</span></span> <span data-ttu-id="a8fb7-192">No início do processo e, como cada botão é salvo ou restaurado, seu aplicativo receberá um código de notificação [tbn \_ Save](tbn-save.md) ou [tbn \_ Restore](tbn-restore.md) .</span><span class="sxs-lookup"><span data-stu-id="a8fb7-192">At the beginning of the process, and as each button is saved or restored, your application will receive a [TBN\_SAVE](tbn-save.md) or [TBN\_RESTORE](tbn-restore.md) notification code.</span></span> <span data-ttu-id="a8fb7-193">Para usar essa opção, você deve implementar manipuladores de notificação para fornecer as informações de bitmap e estado necessárias para salvar ou restaurar com êxito o estado da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-193">To use this option, you must implement notification handlers to provide the bitmap and state information that is needed to successfully save or restore the toolbar state.</span></span>

<span data-ttu-id="a8fb7-194">Os Estados da barra de ferramentas são salvos em um fluxo de dados que consiste em blocos de dados definidos por shell alternando com blocos de dados definidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-194">Toolbar states are saved in a data stream that consists of blocks of Shell-defined data alternating with blocks of application-defined data.</span></span> <span data-ttu-id="a8fb7-195">Um bloco de dados de cada tipo é armazenado para cada botão, juntamente com um bloco opcional de dados globais que os aplicativos podem posicionar no início do fluxo.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-195">One data block of each type is stored for each button, along with an optional block of global data that applications can place at the beginning of the stream.</span></span> <span data-ttu-id="a8fb7-196">Durante o processo de salvamento, o manipulador de [ \_ salvamento do tbn](tbn-save.md) adiciona os blocos definidos pelo aplicativo ao fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-196">During the save process, your [TBN\_SAVE](tbn-save.md) handler adds the application-defined blocks to the data stream.</span></span> <span data-ttu-id="a8fb7-197">Durante o processo de restauração, o manipulador de [ \_ restauração tbn](tbn-restore.md) lê cada bloco e fornece ao shell as informações necessárias para reconstruir a barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-197">During the restore process, the [TBN\_RESTORE](tbn-restore.md) handler reads each block and gives the Shell the information it needs to reconstruct the toolbar.</span></span>

### <a name="how-to-handle-a-tbn_save-notification"></a><span data-ttu-id="a8fb7-198">Como lidar com uma notificação de salvamento de TBN \_</span><span class="sxs-lookup"><span data-stu-id="a8fb7-198">How to Handle a TBN\_SAVE Notification</span></span>

<span data-ttu-id="a8fb7-199">O primeiro código de notificação [tbn \_ Save](tbn-save.md) é enviado no início do processo de salvamento.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-199">The first [TBN\_SAVE](tbn-save.md) notification code is sent at the beginning of the save process.</span></span> <span data-ttu-id="a8fb7-200">Antes que todos os botões sejam salvos, os membros da estrutura [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) são definidos conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-200">Before any buttons are saved, the members of the [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) structure are set as shown in the following table.</span></span>



| <span data-ttu-id="a8fb7-201">Membro</span><span class="sxs-lookup"><span data-stu-id="a8fb7-201">Member</span></span>       | <span data-ttu-id="a8fb7-202">Configuração</span><span class="sxs-lookup"><span data-stu-id="a8fb7-202">Setting</span></span>                                                                                                                                                                                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8fb7-203">**iItem**</span><span class="sxs-lookup"><span data-stu-id="a8fb7-203">**iItem**</span></span>    | <span data-ttu-id="a8fb7-204">– 1</span><span class="sxs-lookup"><span data-stu-id="a8fb7-204">–1</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="a8fb7-205">**cbData**</span><span class="sxs-lookup"><span data-stu-id="a8fb7-205">**cbData**</span></span>   | <span data-ttu-id="a8fb7-206">A quantidade de memória necessária para dados definidos por shell.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-206">The amount of memory needed for Shell-defined data.</span></span>                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="a8fb7-207">**cButtons**</span><span class="sxs-lookup"><span data-stu-id="a8fb7-207">**cButtons**</span></span> | <span data-ttu-id="a8fb7-208">O número de botões.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-208">The number of buttons.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="a8fb7-209">**pData**</span><span class="sxs-lookup"><span data-stu-id="a8fb7-209">**pData**</span></span>    | <span data-ttu-id="a8fb7-210">A quantidade calculada de memória necessária para dados definidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-210">The calculated amount of memory needed for application-defined data.</span></span> <span data-ttu-id="a8fb7-211">Normalmente, você inclui alguns dados globais, além de dados para cada botão.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-211">Typically, you include some global data, plus data for each button.</span></span> <span data-ttu-id="a8fb7-212">Adicione esse valor a **cbData** e aloque memória suficiente para o **pData** para manter tudo.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-212">Add that value to **cbData** and allocate enough memory to **pData** to hold it all.</span></span>                                                                                                                      |
| <span data-ttu-id="a8fb7-213">**pCurrent**</span><span class="sxs-lookup"><span data-stu-id="a8fb7-213">**pCurrent**</span></span> | <span data-ttu-id="a8fb7-214">O primeiro byte não utilizado no fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-214">The first unused byte in the data stream.</span></span> <span data-ttu-id="a8fb7-215">Se você não precisar de informações da barra de ferramentas global, defina **pCurrent**  =  **pData** para que ele aponte para o início do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-215">If you do not require global toolbar information, set **pCurrent** = **pData** so that it points to the start of the data stream.</span></span> <span data-ttu-id="a8fb7-216">Se você precisar de informações da barra de ferramentas global, armazene-as em **pData** e, em seguida, defina **pCurrent** para o início da parte não usada do fluxo de dados antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-216">If you do require global toolbar information, store it at **pData**, then set **pCurrent** to the beginning of the unused portion of the data stream before returning.</span></span> |



 

<span data-ttu-id="a8fb7-217">Se você quiser adicionar algumas informações globais da barra de ferramentas, coloque-as no início do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-217">If you want to add some global toolbar information, put it at the start of the data stream.</span></span> <span data-ttu-id="a8fb7-218">Avance **pCurrent** até o final dos dados globais para que ele aponte para o início da parte não utilizada do fluxo de dados e retorne.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-218">Advance **pCurrent** to the end of the global data so that it points to the beginning of the unused portion of the data stream, and return.</span></span>

<span data-ttu-id="a8fb7-219">Depois de retornar, o Shell começa a salvar as informações do botão.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-219">After you return, the Shell starts saving button information.</span></span> <span data-ttu-id="a8fb7-220">Ele adiciona os dados definidos por Shell para o primeiro botão em **pCurrent** e, em seguida, avança **pCurrent** para o início da parte não utilizada.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-220">It adds the Shell-defined data for the first button at **pCurrent** and then advances **pCurrent** to the start of the unused portion.</span></span>

<span data-ttu-id="a8fb7-221">Depois que cada botão é salvo, um código de notificação [tbn \_ Save](tbn-save.md) é enviado e [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) é retornado com esses membros definidos da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-221">After each button is saved, a [TBN\_SAVE](tbn-save.md) notification code is sent and [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) is returned with these members set as follows.</span></span>



| <span data-ttu-id="a8fb7-222">Membro</span><span class="sxs-lookup"><span data-stu-id="a8fb7-222">Member</span></span>                       | <span data-ttu-id="a8fb7-223">Configuração</span><span class="sxs-lookup"><span data-stu-id="a8fb7-223">Setting</span></span>                                                                                                                                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8fb7-224">**iItem**</span><span class="sxs-lookup"><span data-stu-id="a8fb7-224">**iItem**</span></span>                    | <span data-ttu-id="a8fb7-225">O índice de base zero do número do botão.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-225">The zero-based index of the button number.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="a8fb7-226">**pCurrent**</span><span class="sxs-lookup"><span data-stu-id="a8fb7-226">**pCurrent**</span></span>                 | <span data-ttu-id="a8fb7-227">Um ponteiro para o primeiro byte não utilizado no fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-227">A pointer to the first unused byte in the data stream.</span></span> <span data-ttu-id="a8fb7-228">Se você quiser armazenar informações adicionais sobre o botão, armazene-o no local apontado por **pCurrent** e atualize **pCurrent** para apontar para a primeira parte não utilizada do fluxo de dados depois disso.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-228">If you want to store additional information about the button, store it at the location pointed to by **pCurrent** and update **pCurrent** to point to the first unused portion of the data stream after that.</span></span> |
| [<span data-ttu-id="a8fb7-229">**TBBUTTON**</span><span class="sxs-lookup"><span data-stu-id="a8fb7-229">**TBBUTTON**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) | <span data-ttu-id="a8fb7-230">Uma estrutura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) que descreve o botão que está sendo salvo.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-230">A [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure that describes the button that is being saved.</span></span>                                                                                                                                                                              |



 

<span data-ttu-id="a8fb7-231">Ao receber o código de notificação, você deve extrair as informações específicas de cada botão de que precisa do [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton).</span><span class="sxs-lookup"><span data-stu-id="a8fb7-231">When you receive the notification code, you should extract any button-specific information you need from [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton).</span></span> <span data-ttu-id="a8fb7-232">Lembre-se de que, ao adicionar um botão, você pode usar o membro **dwData** de **TBBUTTON** para armazenar dados específicos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-232">Remember that when you add a button, you can use the **dwData** member of **TBBUTTON** to hold application-specific data.</span></span> <span data-ttu-id="a8fb7-233">Carregue seus dados no fluxo de dados em **pCurrent**.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-233">Load your data into the data stream at **pCurrent**.</span></span> <span data-ttu-id="a8fb7-234">Avance **pCurrent** até o final de seus dados, apontando novamente para o início da parte não utilizada do fluxo e retorne.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-234">Advance **pCurrent** to the end of your data, again pointing to the beginning of the unused portion of the stream, and return.</span></span>

<span data-ttu-id="a8fb7-235">Em seguida, o Shell vai para o botão Avançar, adiciona suas informações a **pData**, avança **PCurrent**, carrega [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)e envia outro código de notificação de [tbn \_ salvar](tbn-save.md) .</span><span class="sxs-lookup"><span data-stu-id="a8fb7-235">The Shell then goes to the next button, adds its information to **pData**, advances **pCurrent**, loads [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton), and sends another [TBN\_SAVE](tbn-save.md) notification code.</span></span> <span data-ttu-id="a8fb7-236">Esse processo continua até que todos os botões sejam salvos.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-236">This process continues until all buttons are saved.</span></span>

### <a name="restoring-saved-toolbars"></a><span data-ttu-id="a8fb7-237">Restaurando barras de ferramentas salvas</span><span class="sxs-lookup"><span data-stu-id="a8fb7-237">Restoring Saved Toolbars</span></span>

<span data-ttu-id="a8fb7-238">O processo de restauração basicamente reverte o processo de salvamento.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-238">The restore process basically reverses the save process.</span></span> <span data-ttu-id="a8fb7-239">No início, seu aplicativo receberá um código de notificação [tbn \_ Restore](tbn-restore.md) com o membro **iItem** da estrutura [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) definida como – 1.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-239">At the beginning, your application will receive a [TBN\_RESTORE](tbn-restore.md) notification code with the **iItem** member of the [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) structure set to –1.</span></span> <span data-ttu-id="a8fb7-240">O membro **cbData** é definido como o tamanho de **pData** e **cButtons** é definido como o número de botões.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-240">The **cbData** member is set to the size of **pData**, and **cButtons** is set to the number of buttons.</span></span>

<span data-ttu-id="a8fb7-241">Seu manipulador de notificação deve extrair as informações globais que foram colocadas no início de **pData** durante a gravação e avançar **pCurrent** até o início do primeiro bloco de dados definidos por shell.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-241">Your notification handler should extract the global information that was placed at the beginning of **pData** during the save, and advance **pCurrent** to the start of the first block of Shell-defined data.</span></span> <span data-ttu-id="a8fb7-242">Defina **cBytesPerRecord** como o tamanho dos blocos de dados usados para salvar os dados do botão.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-242">Set **cBytesPerRecord** to the size of the data blocks you used to save the button data.</span></span> <span data-ttu-id="a8fb7-243">Defina **cButtons** como o número de botões e retorne.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-243">Set **cButtons** to the number of buttons, and return.</span></span>

<span data-ttu-id="a8fb7-244">O próximo [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) é para o primeiro botão.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-244">The next [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) is for the first button.</span></span> <span data-ttu-id="a8fb7-245">O membro **pCurrent** aponta para o início do primeiro bloco de dados de botão e **iItem** é definido como o índice de botão.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-245">The **pCurrent** member points to the start of your first block of button data, and **iItem** is set to the button index.</span></span> <span data-ttu-id="a8fb7-246">Extraia esses dados e **pCurrent** avançados.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-246">Extract that data and advance **pCurrent**.</span></span> <span data-ttu-id="a8fb7-247">Carregue os dados em [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)e retorne.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-247">Load the data into [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton), and return.</span></span> <span data-ttu-id="a8fb7-248">Para omitir um botão da barra de ferramentas restaurada, defina o membro **idCommand** de **TBBUTTON** como zero.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-248">To omit a button from the restored toolbar, set the **idCommand** member of **TBBUTTON** to zero.</span></span> <span data-ttu-id="a8fb7-249">O Shell repetirá o processo para os botões restantes.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-249">The Shell will repeat the process for the remaining buttons.</span></span> <span data-ttu-id="a8fb7-250">Além das mensagens [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) e **NMTBRESTORE** , você também pode usar mensagens como [tbn \_ Reset](tbn-reset.md) para salvar e restaurar uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-250">In addition to the [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) and **NMTBRESTORE** messages, you can also use messages such as [TBN\_RESET](tbn-reset.md) to save and restore a toolbar.</span></span>

<span data-ttu-id="a8fb7-251">O exemplo de código a seguir salva uma barra de ferramentas antes de ser personalizada e a restaura se o aplicativo receber uma mensagem de [ \_ redefinição de tbn](tbn-reset.md) .</span><span class="sxs-lookup"><span data-stu-id="a8fb7-251">The following code example saves a toolbar before it is customized, and restores it if the application receives a [TBN\_RESET](tbn-reset.md) message.</span></span>


```C++
int               i;
LPNMHDR           lpnmhdr;
static int        nResetCount;
static LPTBBUTTON lpSaveButtons;
LPARAM            lParam;

switch( lpnmhdr->code)
{
    case TBN_BEGINADJUST: // Begin customizing the toolbar.
    {
        LPTBNOTIFY  lpTB = (LPTBNOTIFY)lparam;
       
        // Allocate memory for the button information.
        
        nResetCount   = SendMessage(lpTB->hdr.hwndFrom, TB_BUTTONCOUNT, 0, 0);
        lpSaveButtons = (LPTBBUTTON)GlobalAlloc(GPTR, sizeof(TBBUTTON) * nResetCount);
      
        // In case the user presses reset, save the current configuration 
        // so the original toolbar can be restored.
        
        for(i = 0; i < nResetCount; i++)
        {
            SendMessage(lpTB->hdr.hwndFrom, 
                        TB_GETBUTTON, i, 
                        (LPARAM)(lpSaveButtons + i));
        }
    }
    
    return TRUE;
   
    case TBN_RESET:
    {
        LPTBNOTIFY lpTB = (LPTBNOTIFY)lparam;
        
        int nCount, i;
    
        // Remove all of the existing buttons, starting with the last one.
        
        nCount = SendMessage(lpTB->hdr.hwndFrom, TB_BUTTONCOUNT, 0, 0);
        
        for(i = nCount - 1; i >= 0; i--)
        {
            SendMessage(lpTB->hdr.hwndFrom, TB_DELETEBUTTON, i, 0);
        }
      
        SendMessage(lpTB->hdr.hwndFrom,      // Restore the saved buttons.
                    TB_ADDBUTTONS, 
                    (WPARAM)nResetCount, 
                    (LPARAM)lpSaveButtons);
    }
    
    return TRUE;
   
    case TBN_ENDADJUST:                // Free up the memory you allocated.
        GlobalFree((HGLOBAL)lpSaveButtons);
        
        return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="a8fb7-252">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a8fb7-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8fb7-253">Usando controles da barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="a8fb7-253">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

[<span data-ttu-id="a8fb7-254">**Valores de índice da imagem do botão padrão da barra de ferramentas**</span><span class="sxs-lookup"><span data-stu-id="a8fb7-254">**Toolbar Standard Button Image Index Values**</span></span>](toolbar-standard-button-image-index-values.md)
</dt> <dt>

<span data-ttu-id="a8fb7-255">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="a8fb7-255">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




