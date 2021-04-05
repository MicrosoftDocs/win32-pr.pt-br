---
title: Como criar um controle de tecla de atalho
description: Este tópico demonstra como criar um controle de tecla de atalho. Você cria um controle de tecla quente usando a função CreateWindowEx, especificando a classe de janela de classe de tecla de atalho \_ .
ms.assetid: A6723D4E-B8F6-4365-8FCD-99B73D2C0470
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 498005efcdfbbf001283551bbeea4906ebc854cf
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103824077"
---
# <a name="how-to-create-a-hot-key-control"></a><span data-ttu-id="21bd6-104">Como criar um controle de tecla de atalho</span><span class="sxs-lookup"><span data-stu-id="21bd6-104">How to Create a Hot Key Control</span></span>

<span data-ttu-id="21bd6-105">Este tópico demonstra como criar um controle de tecla de atalho.</span><span class="sxs-lookup"><span data-stu-id="21bd6-105">This topic demonstrates how to create a hot key control.</span></span> <span data-ttu-id="21bd6-106">Você cria um controle de tecla quente usando a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando a classe de janela de classe de tecla de atalho \_ .</span><span class="sxs-lookup"><span data-stu-id="21bd6-106">You create a hot key control by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the HOTKEY\_CLASS window class.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="21bd6-107">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="21bd6-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="21bd6-108">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="21bd6-108">Technologies</span></span>

-   [<span data-ttu-id="21bd6-109">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="21bd6-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="21bd6-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="21bd6-110">Prerequisites</span></span>

-   <span data-ttu-id="21bd6-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="21bd6-111">C/C++</span></span>
-   <span data-ttu-id="21bd6-112">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="21bd6-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="21bd6-113">Instruções</span><span class="sxs-lookup"><span data-stu-id="21bd6-113">Instructions</span></span>


<span data-ttu-id="21bd6-114">Antes de criar o controle de teclas de acesso, verifique se a DLL de controles comuns está carregada.</span><span class="sxs-lookup"><span data-stu-id="21bd6-114">Before you create the hot key control, ensure that the common controls DLL is loaded.</span></span>

<span data-ttu-id="21bd6-115">No exemplo de código C++ a seguir, a função definida pelo aplicativo chama a função [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) para carregar a DLL de controle comum.</span><span class="sxs-lookup"><span data-stu-id="21bd6-115">In the following C++ code example, the application-defined function calls the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function to load the common control DLL.</span></span> <span data-ttu-id="21bd6-116">Em seguida, ele chama a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando a classe de janela de **\_ classe de tecla de atalho** para criar um controle de tecla de atalho.</span><span class="sxs-lookup"><span data-stu-id="21bd6-116">Then it calls the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the **HOTKEY\_CLASS** window class, to create a hot key control.</span></span> <span data-ttu-id="21bd6-117">Ele usa as mensagens [**hkm \_ SetRules**](hkm-setrules.md) e [**hkm \_**](hkm-sethotkey.md) set para inicializar o controle e retorna um identificador para o controle.</span><span class="sxs-lookup"><span data-stu-id="21bd6-117">It uses the [**HKM\_SETRULES**](hkm-setrules.md) and [**HKM\_SETHOTKEY**](hkm-sethotkey.md) messages to initialize the control and returns a handle to the control.</span></span>

<span data-ttu-id="21bd6-118">Esse controle de teclas de acesso não permite que o usuário escolha uma tecla de atalho que seja uma única chave não modificada, nem permite que o usuário escolha apenas SHIFT e uma chave.</span><span class="sxs-lookup"><span data-stu-id="21bd6-118">This hot key control does not allow the user to choose a hot key that is a single unmodified key, nor does it permit the user to choose only SHIFT and a key.</span></span> <span data-ttu-id="21bd6-119">Essas regras impedem efetivamente que o usuário escolha uma tecla de atalho que pode ser inserida acidentalmente ao digitar o texto.</span><span class="sxs-lookup"><span data-stu-id="21bd6-119">These rules effectively prevent the user from choosing a hot key that might be entered accidentally while typing text.</span></span>



```C++
// Creates a hot key control and sets rules and default settings for it.
// 
// Returns the handle of the hot key control. 
//
// Parameter
//     hwndDlg - Handle of the parent window (dialog box). 
// 
// Global variable 
//     g_hinst - Handle of the application instance. 

extern HINSTANCE g_hinst; 

HWND WINAPI InitializeHotkey(HWND hwndDlg) 
{ 
    HWND hwndHot = NULL;
    
    // Ensure that the common control DLL is loaded. 
    INITCOMMONCONTROLSEX icex;  //declare an INITCOMMONCONTROLSEX Structure
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC = ICC_HOTKEY_CLASS;   //set dwICC member to ICC_HOTKEY_CLASS    
                                     // this loads the Hot Key control class.
    InitCommonControlsEx(&icex);  
 
    hwndHot = CreateWindowEx(0,                        // no extended styles 
                             HOTKEY_CLASS,             // class name 
                             TEXT(""),                 // no title (caption) 
                             WS_CHILD | WS_VISIBLE,    // style 
                             15, 10,                   // position 
                             200, 20,                  // size 
                             hwndDlg,                  // parent window 
                             NULL,                     // uses class menu 
                             g_hinst,                  // instance 
                             NULL);                    // no WM_CREATE parameter 
 
    SetFocus(hwndHot); 
 
    // Set rules for invalid key combinations. If the user does not supply a
    // modifier key, use ALT as a modifier. If the user supplies SHIFT as a 
    // modifier key, use SHIFT + ALT instead.
    SendMessage(hwndHot, 
                HKM_SETRULES, 
                (WPARAM) HKCOMB_NONE | HKCOMB_S,   // invalid key combinations 
                MAKELPARAM(HOTKEYF_ALT, 0));       // add ALT to invalid entries 
 
    // Set CTRL + ALT + A as the default hot key for this window. 
    // 0x41 is the virtual key code for 'A'. 
    SendMessage(hwndHot, 
                HKM_SETHOTKEY, 
                MAKEWORD(0x41, HOTKEYF_CONTROL | HOTKEYF_ALT), 
                0); 
 
    return hwndHot; 
}
```



## <a name="related-topics"></a><span data-ttu-id="21bd6-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="21bd6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21bd6-121">Referência de controle de teclas de acesso</span><span class="sxs-lookup"><span data-stu-id="21bd6-121">Hot Key Control Reference</span></span>](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[<span data-ttu-id="21bd6-122">Sobre os controles de tecla de atalho</span><span class="sxs-lookup"><span data-stu-id="21bd6-122">About Hot Key Controls</span></span>](hot-key-controls.md)
</dt> <dt>

[<span data-ttu-id="21bd6-123">Usando controles de tecla quente</span><span class="sxs-lookup"><span data-stu-id="21bd6-123">Using Hot Key Controls</span></span>](using-hot-key-controls.md)
</dt> </dl>

 

 