---
title: Como recuperar e definir uma tecla de atalho
description: Este tópico demonstra como recuperar ou definir a combinação de teclas para um controle de tecla de atalho.
ms.assetid: F3643196-F847-4EE4-97ED-75AF52D4FF8D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d453433917c211bc787f70a5d9344f1a477858e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "105750313"
---
# <a name="how-to-retrieve-and-set-a-hot-key"></a><span data-ttu-id="a819b-103">Como recuperar e definir uma tecla de atalho</span><span class="sxs-lookup"><span data-stu-id="a819b-103">How to Retrieve and Set a Hot Key</span></span>

<span data-ttu-id="a819b-104">Este tópico demonstra como recuperar ou definir a combinação de teclas para um controle de tecla de atalho.</span><span class="sxs-lookup"><span data-stu-id="a819b-104">This topic demonstrates how to retrieve or set the key combination for a hot key control.</span></span> <span data-ttu-id="a819b-105">A [**mensagem \_ settecla hkm**](hkm-sethotkey.md) permite que um aplicativo defina a combinação de teclas de acesso para um controle de tecla de atalho.</span><span class="sxs-lookup"><span data-stu-id="a819b-105">The [**HKM\_SETHOTKEY**](hkm-sethotkey.md) message allows an application to set the hot key combination for a hot key control.</span></span> <span data-ttu-id="a819b-106">Os aplicativos usam a mensagem [**hkm \_ getteclaize**](hkm-gethotkey.md) para recuperar o código de chave virtual e os sinalizadores de modificador da tecla de atalho escolhida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="a819b-106">Applications use the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message to retrieve the virtual key code and modifier flags of the hot key that is chosen by the user.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a819b-107">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="a819b-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a819b-108">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="a819b-108">Technologies</span></span>

-   [<span data-ttu-id="a819b-109">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="a819b-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a819b-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="a819b-110">Prerequisites</span></span>

-   <span data-ttu-id="a819b-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="a819b-111">C/C++</span></span>
-   <span data-ttu-id="a819b-112">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="a819b-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a819b-113">Instruções</span><span class="sxs-lookup"><span data-stu-id="a819b-113">Instructions</span></span>


<span data-ttu-id="a819b-114">Use a mensagem [**hkm \_ getteclaize**](hkm-gethotkey.md) para recuperar o código de chave virtual e as chaves de modificador que descrevem uma tecla de atalho escolhida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="a819b-114">Use the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message to retrieve the virtual key code and modifier keys that describe a hot key chosen by the user.</span></span> <span data-ttu-id="a819b-115">Use a mensagem [**hkm \_ autotecla**](hkm-sethotkey.md) para definir esses valores para uma tecla de acesso.</span><span class="sxs-lookup"><span data-stu-id="a819b-115">Use the [**HKM\_SETHOTKEY**](hkm-sethotkey.md) message to set those values for a hot key.</span></span>

<span data-ttu-id="a819b-116">No exemplo de código C++ a seguir, a função definida pelo aplicativo usa a mensagem [**hkm \_ gettecla de atalho**](hkm-gethotkey.md) para recuperar uma combinação de teclas de um controle de tecla quente e, em seguida, usa a mensagem de [**\_ settecla do WM**](/windows/desktop/inputdev/wm-sethotkey) para definir uma tecla de acesso global.</span><span class="sxs-lookup"><span data-stu-id="a819b-116">In the following C++ code example, the application-defined function uses the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message to retrieve a key combination from a hot key control and then uses the [**WM\_SETHOTKEY**](/windows/desktop/inputdev/wm-sethotkey) message to set a global hot key.</span></span> <span data-ttu-id="a819b-117">Observe que você não pode definir uma tecla de acesso global para uma janela que tenha o estilo de janela [**\_ filho do WS**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="a819b-117">Note that you cannot set a global hot key for a window that has the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) window style.</span></span>



```C++
// Retrieves the hot key from the hot key control and sets it as
// the hot key for the application's main window. 
//
// Parameters 
//     hwndHot  - Handle of the hot key control. 
//     hwndMain - Handle of the main window. 

BOOL WINAPI ProcessHotkey(HWND hwndHot, HWND hwndMain) 
{ 
    WORD wHotkey;  

    // Retrieve the hot key (virtual key code and modifiers). 
    wHotkey = (WORD) SendMessage(hwndHot, HKM_GETHOTKEY, 0, 0); 
    
    // Use the result as wParam for WM_SETHOTKEY. 
    SendMessage(hwndMain, WM_SETHOTKEY, wHotkey, 0); 
    return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="a819b-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a819b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a819b-119">Referência de controle de teclas de acesso</span><span class="sxs-lookup"><span data-stu-id="a819b-119">Hot Key Control Reference</span></span>](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[<span data-ttu-id="a819b-120">Sobre os controles de tecla de atalho</span><span class="sxs-lookup"><span data-stu-id="a819b-120">About Hot Key Controls</span></span>](hot-key-controls.md)
</dt> <dt>

[<span data-ttu-id="a819b-121">Usando controles de tecla quente</span><span class="sxs-lookup"><span data-stu-id="a819b-121">Using Hot Key Controls</span></span>](using-hot-key-controls.md)
</dt> </dl>

 

 