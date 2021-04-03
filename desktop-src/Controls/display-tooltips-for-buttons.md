---
title: Como exibir dicas de ferramentas para botões
description: Quando você especifica o \_ estilo de dicas de ferramenta TBSTYLE, a barra de ferramentas cria e gerencia um controle ToolTip. O controle ToolTip é ocultado e aparece somente quando os usuários movem o ponteiro sobre um botão da barra de ferramentas e deixam-o lá por aproximadamente um segundo.
ms.assetid: 0383DB63-A10E-4235-A974-AB21551E086B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb37de7c21c904673a1f656533497130d50bd8f7
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103823613"
---
# <a name="how-to-display-tooltips-for-buttons"></a><span data-ttu-id="a3be7-104">Como exibir dicas de ferramentas para botões</span><span class="sxs-lookup"><span data-stu-id="a3be7-104">How to Display Tooltips for Buttons</span></span>

<span data-ttu-id="a3be7-105">Quando você especifica o estilo de [**\_ dicas de ferramenta TBSTYLE**](toolbar-control-and-button-styles.md) , a barra de ferramentas cria e gerencia um controle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="a3be7-105">When you specify the [**TBSTYLE\_TOOLTIPS**](toolbar-control-and-button-styles.md) style, the toolbar creates and manages a tooltip control.</span></span> <span data-ttu-id="a3be7-106">O controle ToolTip é ocultado e aparece somente quando os usuários movem o ponteiro sobre um botão da barra de ferramentas e deixam-o lá por aproximadamente um segundo.</span><span class="sxs-lookup"><span data-stu-id="a3be7-106">The tooltip control is hidden and appears only when users move the pointer over a toolbar button and leave it there for approximately one second.</span></span>

<span data-ttu-id="a3be7-107">Seu aplicativo pode fornecer texto ao controle ToolTip em qualquer uma das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="a3be7-107">Your application can supply text to the tooltip control in any one of the following ways:</span></span>

-   <span data-ttu-id="a3be7-108">Defina o texto da dica de ferramenta como o membro **isastring** da estrutura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) para cada botão.</span><span class="sxs-lookup"><span data-stu-id="a3be7-108">Set the tooltip text as the **iString** member of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure for each button.</span></span> <span data-ttu-id="a3be7-109">Você também deve enviar uma [**mensagem \_ SETMAXTEXTROWS TB**](tb-setmaxtextrows.md) e definir o máximo de linhas de texto como 0, para que o texto não apareça como o rótulo do botão, e não como uma dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="a3be7-109">You must also send a [**TB\_SETMAXTEXTROWS**](tb-setmaxtextrows.md) message and set the maximum text rows to 0, so that the text does not appear as the button label rather than as a tooltip.</span></span>
-   <span data-ttu-id="a3be7-110">Crie a barra de ferramentas com o estilo de [**\_ lista TBSTYLE**](toolbar-control-and-button-styles.md) e defina o estilo estendido [**TBSTYLE \_ ex \_ MIXEDBUTTONS**](toolbar-extended-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a3be7-110">Create the toolbar with the [**TBSTYLE\_LIST**](toolbar-control-and-button-styles.md) style and then set the [**TBSTYLE\_EX\_MIXEDBUTTONS**](toolbar-extended-styles.md) extended style.</span></span> <span data-ttu-id="a3be7-111">Os rótulos são mostrados apenas para botões que têm o estilo de [**\_ texto BTNS**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a3be7-111">Labels are shown only for buttons that have the [**BTNS\_SHOWTEXT**](toolbar-control-and-button-styles.md) style.</span></span> <span data-ttu-id="a3be7-112">Para botões que não têm esse estilo, é mostrada uma dica de ferramenta que contém o texto do botão.</span><span class="sxs-lookup"><span data-stu-id="a3be7-112">For buttons that do not have this style, a tooltip is shown that contains the button text.</span></span>
-   <span data-ttu-id="a3be7-113">Responda ao código de notificação [TTN \_ GETDISPINFO](ttn-getdispinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="a3be7-113">Respond to the [TTN\_GETDISPINFO](ttn-getdispinfo.md) notification code.</span></span>
-   <span data-ttu-id="a3be7-114">Responda ao código de notificação [tbn \_ GETINFOTIP](tbn-getinfotip.md) .</span><span class="sxs-lookup"><span data-stu-id="a3be7-114">Respond to the [TBN\_GETINFOTIP](tbn-getinfotip.md) notification code.</span></span>

<span data-ttu-id="a3be7-115">Um aplicativo que precisa enviar mensagens diretamente para o controle ToolTip pode recuperar o identificador para o controle usando a mensagem [**TB \_ GetToolTips**](tb-gettooltips.md) .</span><span class="sxs-lookup"><span data-stu-id="a3be7-115">An application that needs to send messages directly to the tooltip control can retrieve the handle to the control by using the [**TB\_GETTOOLTIPS**](tb-gettooltips.md) message.</span></span> <span data-ttu-id="a3be7-116">Um aplicativo pode substituir o controle ToolTip de uma barra de ferramentas por outro controle ToolTip usando a mensagem [**TB \_ SetToolTips**](tb-settooltips.md) .</span><span class="sxs-lookup"><span data-stu-id="a3be7-116">An application can replace the tooltip control of a toolbar with another tooltip control by using the [**TB\_SETTOOLTIPS**](tb-settooltips.md) message.</span></span>

<span data-ttu-id="a3be7-117">A maneira mais flexível de fornecer texto de dica de ferramenta é responder ao código de notificação [TTN \_ GETDISPINFO](ttn-getdispinfo.md) ou [tbn \_ GETINFOTIP](tbn-getinfotip.md) enviado pelo controle Toolbar para seu pai na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a3be7-117">The most flexible way of supplying tooltip text is to respond to the [TTN\_GETDISPINFO](ttn-getdispinfo.md) or [TBN\_GETINFOTIP](tbn-getinfotip.md) notification code sent by the toolbar control to its parent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <span data-ttu-id="a3be7-118">Para [TTN \_ GETDISPINFO](ttn-getdispinfo.md), o parâmetro *lParam* inclui um ponteiro para uma estrutura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) (também definida como **LPTOOLTIPTEXT**) que especifica o identificador de comando do botão para o qual o texto de ajuda é necessário.</span><span class="sxs-lookup"><span data-stu-id="a3be7-118">For [TTN\_GETDISPINFO](ttn-getdispinfo.md), the *lParam* parameter includes a pointer to an [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure (also defined as **LPTOOLTIPTEXT**) that specifies the command identifier of the button for which Help text is needed.</span></span> <span data-ttu-id="a3be7-119">Esse identificador está no membro **NMTTDISPINFO. HDR. idFrom** .</span><span class="sxs-lookup"><span data-stu-id="a3be7-119">This identifier is in the **NMTTDISPINFO.hdr.idFrom** member.</span></span> <span data-ttu-id="a3be7-120">Um aplicativo pode copiar o texto de ajuda para a estrutura, especificar o endereço de uma cadeia de caracteres que contém o texto da ajuda ou especificar o identificador de instância e o manipulador de recursos de um recurso de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a3be7-120">An application can copy the Help text to the structure, specify the address of a string containing the Help text, or specify the instance handle and resource identifier of a string resource.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a3be7-121">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="a3be7-121">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a3be7-122">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="a3be7-122">Technologies</span></span>

-   [<span data-ttu-id="a3be7-123">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="a3be7-123">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a3be7-124">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="a3be7-124">Prerequisites</span></span>

-   <span data-ttu-id="a3be7-125">C/C++</span><span class="sxs-lookup"><span data-stu-id="a3be7-125">C/C++</span></span>
-   <span data-ttu-id="a3be7-126">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="a3be7-126">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a3be7-127">Instruções</span><span class="sxs-lookup"><span data-stu-id="a3be7-127">Instructions</span></span>

### <a name="display-a-tooltip-for-a-button"></a><span data-ttu-id="a3be7-128">Exibir uma dica de ferramenta para um botão</span><span class="sxs-lookup"><span data-stu-id="a3be7-128">Display a Tooltip for a Button</span></span>

<span data-ttu-id="a3be7-129">O código de exemplo a seguir manipula o código de notificação da dica de ferramenta [TTN \_ GETDISPINFO](ttn-getdispinfo.md) fornecendo texto de identificadores de recurso.</span><span class="sxs-lookup"><span data-stu-id="a3be7-129">The following example code handles the [TTN\_GETDISPINFO](ttn-getdispinfo.md) tooltip notification code by providing text from resource identifiers.</span></span>


```C++
case WM_NOTIFY: 
            
    switch (((LPNMHDR) lParam)->code) 
    {
    
    case TTN_GETDISPINFO: 
        { 
            LPTOOLTIPTEXT lpttt = (LPTOOLTIPTEXT)lParam; 
            
            // Set the instance of the module that contains the resource.
            lpttt->hinst = g_hInst; 
            
            UINT_PTR idButton = lpttt->hdr.idFrom;
            
            switch (idButton) 
            { 
            case IDM_NEW: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_NEW); 
                break; 
                
            case IDM_OPEN: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_OPEN); 
                break; 
                
            case IDM_SAVE: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_SAVE); 
                break; 
            } 
            
            break; 
        } 
    }
    return TRUE;
```



## <a name="related-topics"></a><span data-ttu-id="a3be7-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a3be7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3be7-131">Usando controles da barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="a3be7-131">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="a3be7-132">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="a3be7-132">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




