---
title: Como usar controles de pager
description: Esta seção descreve como implementar o controle de pager em seu aplicativo.
ms.assetid: 5703FE4B-987E-49DA-9741-F8B45AD26467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586bfff0c8d8097c4b0e861506bb73f55467b711
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008448"
---
# <a name="how-to-use-pager-controls"></a><span data-ttu-id="c85ad-103">Como usar controles de pager</span><span class="sxs-lookup"><span data-stu-id="c85ad-103">How to Use Pager Controls</span></span>

<span data-ttu-id="c85ad-104">Esta seção descreve como implementar o controle de pager em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c85ad-104">This section describes how to implement the pager control in your application.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c85ad-105">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="c85ad-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c85ad-106">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="c85ad-106">Technologies</span></span>

-   [<span data-ttu-id="c85ad-107">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="c85ad-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="c85ad-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="c85ad-108">Prerequisites</span></span>

-   <span data-ttu-id="c85ad-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="c85ad-109">C/C++</span></span>
-   <span data-ttu-id="c85ad-110">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="c85ad-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="c85ad-111">Instruções</span><span class="sxs-lookup"><span data-stu-id="c85ad-111">Instructions</span></span>

### <a name="initialize-a-pager-control"></a><span data-ttu-id="c85ad-112">Inicializar um controle de pager</span><span class="sxs-lookup"><span data-stu-id="c85ad-112">Initialize a Pager Control</span></span>

<span data-ttu-id="c85ad-113">Para usar o controle de pager, você deve chamar a função [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) com o \_ sinalizador de classe ICC PAGESCROLLER \_ definido no membro **dwICC** da estrutura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) .</span><span class="sxs-lookup"><span data-stu-id="c85ad-113">To use the pager control, you must call the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function with the ICC\_PAGESCROLLER\_CLASS flag set in the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

### <a name="create-a-pager-control"></a><span data-ttu-id="c85ad-114">Criar um controle de pager</span><span class="sxs-lookup"><span data-stu-id="c85ad-114">Create a Pager Control</span></span>

<span data-ttu-id="c85ad-115">Use o [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou a API [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para criar um controle de pager.</span><span class="sxs-lookup"><span data-stu-id="c85ad-115">Use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) API to create a pager control.</span></span> <span data-ttu-id="c85ad-116">O nome da classe para o controle é [**WC \_ PAGESCROLLER**](common-control-window-classes.md), que é definido em commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="c85ad-116">The class name for the control is [**WC\_PAGESCROLLER**](common-control-window-classes.md), which is defined in Commctrl.h.</span></span> <span data-ttu-id="c85ad-117">O estilo [**PGS \_ na horizontal**](pager-control-styles.md) é usado para criar um pager horizontal e o estilo [**\_ Vert PGS**](pager-control-styles.md) é usado para criar um pager vertical.</span><span class="sxs-lookup"><span data-stu-id="c85ad-117">The [**PGS\_HORZ**](pager-control-styles.md) style is used to create a horizontal pager, and the [**PGS\_VERT**](pager-control-styles.md) style is used to create a vertical pager.</span></span> <span data-ttu-id="c85ad-118">Como esse é um controle filho, o [**estilo \_ filho WS**](/windows/desktop/winmsg/window-styles) também deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="c85ad-118">Because this is a child control, the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) style should also be used.</span></span>

<span data-ttu-id="c85ad-119">Depois que o controle de pager for criado, você provavelmente desejará atribuir uma janela contida a ele.</span><span class="sxs-lookup"><span data-stu-id="c85ad-119">After the pager control is created, you will most likely want to assign a contained window to it.</span></span> <span data-ttu-id="c85ad-120">Se a janela contida for uma janela filho, você deverá tornar a janela filho um filho do controle de pager para que o tamanho e a posição sejam calculados corretamente.</span><span class="sxs-lookup"><span data-stu-id="c85ad-120">If the contained window is a child window, you should make the child window a child of the pager control so that the size and position will be calculated correctly.</span></span> <span data-ttu-id="c85ad-121">Em seguida, atribua a janela ao controle de pager com [**a \_ mensagem do PGM**](pgm-setchild.md) .</span><span class="sxs-lookup"><span data-stu-id="c85ad-121">You then assign the window to the pager control with the [**PGM\_SETCHILD**](pgm-setchild.md) message.</span></span> <span data-ttu-id="c85ad-122">Lembre-se de que essa mensagem não altera realmente a janela pai da janela contida; Ele simplesmente atribui a janela contida.</span><span class="sxs-lookup"><span data-stu-id="c85ad-122">Be aware that this message does not actually change the parent window of the contained window; it simply assigns the contained window.</span></span> <span data-ttu-id="c85ad-123">Se a janela contida for um dos controles comuns, ela deverá ter o estilo [**\_ myresize da CCS**](common-control-styles.md) para impedir que o controle tente se redimensionar para o tamanho do controle de pager.</span><span class="sxs-lookup"><span data-stu-id="c85ad-123">If the contained window is one of the common controls, it must have the [**CCS\_NORESIZE**](common-control-styles.md) style to prevent the control from attempting to resize itself to the pager control's size.</span></span>

### <a name="process-pager-control-notifications"></a><span data-ttu-id="c85ad-124">Notificações de controle do pager de processo</span><span class="sxs-lookup"><span data-stu-id="c85ad-124">Process Pager Control Notifications</span></span>

<span data-ttu-id="c85ad-125">No mínimo, é necessário processar a notificação [PGN \_ CALCSIZE](pgn-calcsize.md) .</span><span class="sxs-lookup"><span data-stu-id="c85ad-125">At a minimum, it is necessary to process the [PGN\_CALCSIZE](pgn-calcsize.md) notification.</span></span> <span data-ttu-id="c85ad-126">Se você não processar essa notificação e inserir um valor para a largura ou a altura, as setas de rolagem no controle de pager não serão exibidas.</span><span class="sxs-lookup"><span data-stu-id="c85ad-126">If you do not process this notification and enter a value for the width or height, the scroll arrows in the pager control will not be displayed.</span></span> <span data-ttu-id="c85ad-127">Isso ocorre porque o controle de pager usa a largura ou a altura fornecida na \_ notificação PGN CALCSIZE para determinar o tamanho "ideal" da janela contida.</span><span class="sxs-lookup"><span data-stu-id="c85ad-127">This is because the pager control uses the width or height supplied in the PGN\_CALCSIZE notification to determine the "ideal" size of the contained window.</span></span>

<span data-ttu-id="c85ad-128">O exemplo a seguir demonstra como processar o caso de notificação [PGN \_ CALCSIZE](pgn-calcsize.md) .</span><span class="sxs-lookup"><span data-stu-id="c85ad-128">The following example demonstrates how to process the [PGN\_CALCSIZE](pgn-calcsize.md) notification case.</span></span> <span data-ttu-id="c85ad-129">Neste exemplo, a janela contida é um controle ToolBar que contém um número desconhecido de botões em um tamanho desconhecido.</span><span class="sxs-lookup"><span data-stu-id="c85ad-129">In this example, the contained window is a toolbar control that contains an unknown number of buttons at an unknown size.</span></span> <span data-ttu-id="c85ad-130">O exemplo mostra como usar a mensagem de [**TB \_ getmaxsize**](tb-getmaxsize.md) para determinar o tamanho de todos os itens na barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="c85ad-130">The example shows how to use the [**TB\_GETMAXSIZE**](tb-getmaxsize.md) message to determine the size of all of the items in the toolbar.</span></span> <span data-ttu-id="c85ad-131">Em seguida, o exemplo coloca a largura de todos os itens no membro **iWidth** da estrutura [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) que é passada para a notificação.</span><span class="sxs-lookup"><span data-stu-id="c85ad-131">The example then places the width of all of the items into the **iWidth** member of the [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) structure that is passed to the notification.</span></span>


```C++
case PGN_SCROLL:{

    LPNMPGSCROLL pScroll = (LPNMPGSCROLL)lParam;
 
    switch(pScroll->iDir){
     
        case PGF_SCROLLLEFT:
        case PGF_SCROLLRIGHT:
        case PGF_SCROLLUP:
        case PGF_SCROLLDOWN:
     
            pScroll->iScroll = 20;
        
            break;
        }
    }
  
return 0;
```



## <a name="related-topics"></a><span data-ttu-id="c85ad-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c85ad-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c85ad-133">Usando controles de pager</span><span class="sxs-lookup"><span data-stu-id="c85ad-133">Using Pager Controls</span></span>](using-pager-controls.md)
</dt> <dt>

<span data-ttu-id="c85ad-134">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="c85ad-134">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 