---
title: Como criar controles SysLink
description: Você implementa os hiperlinks do controle SysLink por meio de marcação na cadeia de caracteres de inicialização do controle ou enviando a ele uma \_ mensagem SETITEM do LM.
ms.assetid: CEE02A87-D85A-4F4D-931D-2B1371320814
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77aa5c5ff3348f35f9c67cb34bea0cc495d403ef
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641938"
---
# <a name="how-to-create-syslink-controls"></a><span data-ttu-id="233e4-103">Como criar controles SysLink</span><span class="sxs-lookup"><span data-stu-id="233e4-103">How to Create SysLink Controls</span></span>

<span data-ttu-id="233e4-104">Você implementa os hiperlinks do controle SysLink por meio de marcação na cadeia de caracteres de inicialização do controle ou enviando a ele uma mensagem [**\_ SETITEM do LM**](lm-setitem.md) .</span><span class="sxs-lookup"><span data-stu-id="233e4-104">You implement the SysLink control's hyperlinks through markup in the control's initialization string, or by sending it a [**LM\_SETITEM**](lm-setitem.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="233e4-105">Antes de criar controles SysLink, você deve chamar a função [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , especificando a \_ classe de link ICC \_ .</span><span class="sxs-lookup"><span data-stu-id="233e4-105">Before creating SysLink controls, you must call the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, specifying the ICC\_LINK\_CLASS.</span></span>

 

<span data-ttu-id="233e4-106">Para criar um SysLink, chame a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando a classe da janela do [**\_ link WC**](common-control-window-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="233e4-106">To create a SysLink, call the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the [**WC\_LINK**](common-control-window-classes.md) window class.</span></span> <span data-ttu-id="233e4-107">O parâmetro *lpWindowName* que é comum a essas funções especifica um ponteiro para uma cadeia de caracteres terminada em zero que contém o texto marcado para exibição.</span><span class="sxs-lookup"><span data-stu-id="233e4-107">The *lpWindowName* parameter that is common to these functions specifies a pointer to a zero-terminated string that contains the marked-up text to display.</span></span> <span data-ttu-id="233e4-108">Para estilos de janela específicos para controles SysLink, consulte [estilos de controle Syslink](syslink-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="233e4-108">For window styles particular to SysLink controls, see [SysLink Control Styles](syslink-control-styles.md).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="233e4-109">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="233e4-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="233e4-110">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="233e4-110">Technologies</span></span>

-   [<span data-ttu-id="233e4-111">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="233e4-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="233e4-112">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="233e4-112">Prerequisites</span></span>

-   <span data-ttu-id="233e4-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="233e4-113">C/C++</span></span>
-   <span data-ttu-id="233e4-114">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="233e4-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="233e4-115">Instruções</span><span class="sxs-lookup"><span data-stu-id="233e4-115">Instructions</span></span>

### <a name="create-a-syslink-control"></a><span data-ttu-id="233e4-116">Criar um controle SysLink</span><span class="sxs-lookup"><span data-stu-id="233e4-116">Create a SysLink Control</span></span>

<span data-ttu-id="233e4-117">O código de exemplo a seguir cria um controle SysLink que exibe dois hiperlinks.</span><span class="sxs-lookup"><span data-stu-id="233e4-117">The following example code creates a SysLink control that displays two hyperlinks.</span></span> <span data-ttu-id="233e4-118">O primeiro hiperlink é uma URL da Internet e o segundo é definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="233e4-118">The first hyperlink is an Internet URL, and the second is application-defined.</span></span>


```C++
HWND CreateSysLink(HWND hDlg, HINSTANCE hInst, RECT rect)
{
    return CreateWindowEx(0, WC_LINK, 
        L"For more information, <A HREF=\"https://www.microsoft.com\">click here</A> " \
        L"or <A ID=\"idInfo\">here</A>.", 
        WS_VISIBLE | WS_CHILD | WS_TABSTOP, 
        rect.left, rect.top, rect.right, rect.bottom, 
        hDlg, NULL, hInst, NULL);
}
```



## <a name="remarks"></a><span data-ttu-id="233e4-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="233e4-119">Remarks</span></span>

<span data-ttu-id="233e4-120">Supõe-se que [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) já foi chamado.</span><span class="sxs-lookup"><span data-stu-id="233e4-120">It is assumed that [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) has already been called.</span></span>

<span data-ttu-id="233e4-121">A especificação do estilo [**WS \_ TabStop**](/windows/desktop/winmsg/window-styles) garante que o usuário poderá selecionar um link alternando-o para ele e pressionando a tecla Enter.</span><span class="sxs-lookup"><span data-stu-id="233e4-121">Specifying the [**WS\_TABSTOP**](/windows/desktop/winmsg/window-styles) style ensures that the user will be able to select a link by tabbing to it and pressing the Enter key.</span></span>

<span data-ttu-id="233e4-122">A versão 6 do ComCtl32.dll dá suporte apenas a Unicode.</span><span class="sxs-lookup"><span data-stu-id="233e4-122">Version 6 of ComCtl32.dll supports Unicode only.</span></span> <span data-ttu-id="233e4-123">Portanto, você não pode criar versões ANSI de controles SysLink – somente Unicode.</span><span class="sxs-lookup"><span data-stu-id="233e4-123">Therefore, you cannot create ANSI versions of SysLink controls—only Unicode.</span></span>

## <a name="related-topics"></a><span data-ttu-id="233e4-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="233e4-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="233e4-125">Usando controles SysLink</span><span class="sxs-lookup"><span data-stu-id="233e4-125">Using SysLink Controls</span></span>](/windows/desktop/Controls/using-syslink-controls)
</dt> <dt>

<span data-ttu-id="233e4-126">[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="233e4-126">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 