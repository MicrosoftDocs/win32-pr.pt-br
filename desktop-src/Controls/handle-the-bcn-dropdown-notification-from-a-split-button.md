---
title: Manipular notificações de BCN_DROPDOWN de SplitButtons
description: Este tópico descreve uma possível maneira de responder à notificação de \_ lista suspensa BCN em um procedimento de caixa de diálogo.
ms.assetid: 847DD645-AE29-4F62-BC32-F235BA409E1E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a368dd28c5347f438feff75fbddb129a420caae7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084945"
---
# <a name="how-to-handle-the-bcn_dropdown-notification-from-a-split-button"></a><span data-ttu-id="75a39-103">Como manipular a \_ notificação suspensa BCN de um botão de divisão</span><span class="sxs-lookup"><span data-stu-id="75a39-103">How to Handle the BCN\_DROPDOWN Notification from a Split Button</span></span>

<span data-ttu-id="75a39-104">Este tópico descreve uma possível maneira de responder à notificação [de \_ lista suspensa BCN](bcn-dropdown.md) em um procedimento de caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="75a39-104">This topic describes one possible way of responding to the [BCN\_DROPDOWN](bcn-dropdown.md) notification in a dialog procedure.</span></span>

<span data-ttu-id="75a39-105">O aplicativo C++ recupera as coordenadas do cliente do botão do cabeçalho de notificação e as converte em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="75a39-105">The C++ application retrieves the client coordinates of the button from the notification header and converts them to screen coordinates.</span></span> <span data-ttu-id="75a39-106">Em seguida, ele cria um menu pop-up e o exibe na parte inferior do botão.</span><span class="sxs-lookup"><span data-stu-id="75a39-106">It then creates a popup menu and displays it at the bottom of the button.</span></span> <span data-ttu-id="75a39-107">Para manter o exemplo simples, os atalhos de teclado não são implementados para o menu.</span><span class="sxs-lookup"><span data-stu-id="75a39-107">To keep the example simple, keyboard shortcuts are not implemented for the menu.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="75a39-108">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="75a39-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="75a39-109">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="75a39-109">Technologies</span></span>

-   [<span data-ttu-id="75a39-110">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="75a39-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="75a39-111">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="75a39-111">Prerequisites</span></span>

-   <span data-ttu-id="75a39-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="75a39-112">C/C++</span></span>
-   <span data-ttu-id="75a39-113">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="75a39-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="75a39-114">Instruções</span><span class="sxs-lookup"><span data-stu-id="75a39-114">Instructions</span></span>

### <a name="step-1-wait-for-the-bcn_dropdown-notification"></a><span data-ttu-id="75a39-115">Etapa 1: aguardar a notificação da *\_ lista suspensa BCN* .</span><span class="sxs-lookup"><span data-stu-id="75a39-115">Step 1: Wait for the *BCN\_DROPDOWN* notification.</span></span>


```C++
case BCN_DROPDOWN:
{
    NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
    if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
    {
```



### <a name="step-2-get-the-screen-coordinates-of-the-button"></a><span data-ttu-id="75a39-116">Etapa 2: obter as coordenadas de tela do botão.</span><span class="sxs-lookup"><span data-stu-id="75a39-116">Step 2: Get the screen coordinates of the button.</span></span>

<span data-ttu-id="75a39-117">Use a função [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) para converter as coordenadas da janela da borda inferior esquerda do botão para as coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="75a39-117">Use the [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) function to convert the window coordinates of the button's lower left edge to screen coordinates.</span></span>


```C++
POINT pt;
pt.x = pDropDown->rcButton.left;
pt.y = pDropDown->rcButton.bottom;
ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
```



### <a name="step-3-create-a-menu-and-add-items"></a><span data-ttu-id="75a39-118">Etapa 3: criar um menu e adicionar itens.</span><span class="sxs-lookup"><span data-stu-id="75a39-118">Step 3: Create a menu and add items.</span></span>

<span data-ttu-id="75a39-119">Use a função [**CreatePopupMenu**](/windows/desktop/api/winuser/nf-winuser-createpopupmenu) para criar um menu.</span><span class="sxs-lookup"><span data-stu-id="75a39-119">Use the [**CreatePopupMenu**](/windows/desktop/api/winuser/nf-winuser-createpopupmenu) function to create a menu.</span></span> <span data-ttu-id="75a39-120">Use a função [**AppendMenu**](/windows/desktop/menurc/u) para adicionar itens ao menu.</span><span class="sxs-lookup"><span data-stu-id="75a39-120">Use the [**AppendMenu**](/windows/desktop/menurc/u) function to add items to the menu.</span></span> <span data-ttu-id="75a39-121">IDC \_ MENUCOMMAND1 e IDC \_ MENUCOMMAND2 são constantes definidas pelo aplicativo para comandos de menu.</span><span class="sxs-lookup"><span data-stu-id="75a39-121">IDC\_MENUCOMMAND1 and IDC\_MENUCOMMAND2 are application-defined constants for menu commands.</span></span>


```C++
HMENU hSplitMenu = CreatePopupMenu();
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
```



### <a name="step-4-display-the-menu"></a><span data-ttu-id="75a39-122">Etapa 4: exibir o menu.</span><span class="sxs-lookup"><span data-stu-id="75a39-122">Step 4: Display the menu.</span></span>

<span data-ttu-id="75a39-123">A função [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) exibe um menu de atalho no local especificado e controla a seleção de itens no menu.</span><span class="sxs-lookup"><span data-stu-id="75a39-123">The [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) function displays a shortcut menu at the specified location and tracks the selection of items on the menu.</span></span>


```C++
TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
```



## <a name="complete-example"></a><span data-ttu-id="75a39-124">Exemplo completo</span><span class="sxs-lookup"><span data-stu-id="75a39-124">Complete example</span></span>


```C++
case WM_NOTIFY:
    switch (((LPNMHDR)lParam)->code)
    {
        case BCN_DROPDOWN:
        {
            NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
            if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
            {

                // Get screen coordinates of the button.
                POINT pt;
                pt.x = pDropDown->rcButton.left;
                pt.y = pDropDown->rcButton.bottom;
                ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
        
                // Create a menu and add items.
                HMENU hSplitMenu = CreatePopupMenu();
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
        
                // Display the menu.
                TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
                return TRUE;
            }
            break;
        }
    }
    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="75a39-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="75a39-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75a39-126">\_Código de notificação da lista suspensa BCN</span><span class="sxs-lookup"><span data-stu-id="75a39-126">BCN\_DROPDOWN Notification Code</span></span>](bcn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="75a39-127">Sobre os botões</span><span class="sxs-lookup"><span data-stu-id="75a39-127">About Buttons</span></span>](about-buttons.md)
</dt> <dt>

[<span data-ttu-id="75a39-128">Referência de controle de botão</span><span class="sxs-lookup"><span data-stu-id="75a39-128">Button Control Reference</span></span>](bumper-button-button-control-reference.md)
</dt> <dt>

[<span data-ttu-id="75a39-129">Usando botões</span><span class="sxs-lookup"><span data-stu-id="75a39-129">Using Buttons</span></span>](using-buttons.md)
</dt> <dt>

[<span data-ttu-id="75a39-130">Botão</span><span class="sxs-lookup"><span data-stu-id="75a39-130">Button</span></span>](buttons.md)
</dt> </dl>

 

 