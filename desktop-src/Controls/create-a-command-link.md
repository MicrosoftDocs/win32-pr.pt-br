---
title: Como criar um link de comando
description: Este tópico descreve uma maneira de criar um link de comando.
ms.assetid: F342075B-2D3B-40E0-B657-E1C57EDC2E3A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8024a7f060a7bae3779b9ec9ebec40bd81c74bb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454401"
---
# <a name="how-to-create-a-command-link"></a><span data-ttu-id="0298f-103">Como criar um link de comando</span><span class="sxs-lookup"><span data-stu-id="0298f-103">How to Create a Command Link</span></span>

<span data-ttu-id="0298f-104">Este tópico descreve uma maneira de criar um link de comando.</span><span class="sxs-lookup"><span data-stu-id="0298f-104">This topic describes one way to create a command link.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="0298f-105">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="0298f-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="0298f-106">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="0298f-106">Technologies</span></span>

-   [<span data-ttu-id="0298f-107">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="0298f-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="0298f-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="0298f-108">Prerequisites</span></span>

-   <span data-ttu-id="0298f-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="0298f-109">C/C++</span></span>
-   <span data-ttu-id="0298f-110">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="0298f-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="0298f-111">Instruções</span><span class="sxs-lookup"><span data-stu-id="0298f-111">Instructions</span></span>

### <a name="step-1-create-an-instance-of-the-command-link-button"></a><span data-ttu-id="0298f-112">Etapa 1: criar uma instância do botão de link de comando.</span><span class="sxs-lookup"><span data-stu-id="0298f-112">Step 1: Create an instance of the command link button.</span></span>

<span data-ttu-id="0298f-113">No exemplo de código C++ a seguir, a constante de estilo [**BS \_ COMMANDLINK**](button-styles.md) especifica o botão como um botão de link de comando.</span><span class="sxs-lookup"><span data-stu-id="0298f-113">In the following C++ code example, the style constant [**BS\_COMMANDLINK**](button-styles.md) specifies the button as a command link button.</span></span>


```C++
HWND hwndCommandLink = CreateWindow(
    L"BUTTON",  // Predefined class; Unicode assumed
    L"",        // Text will be defined later
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_COMMANDLINK,  // Styles
    200,        // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed
```



### <a name="step-2-set-the-command-link-label-and-explanation-text"></a><span data-ttu-id="0298f-114">Etapa 2: definir o rótulo de link de comando e o texto de explicação</span><span class="sxs-lookup"><span data-stu-id="0298f-114">Step 2: Set the command link label and explanation text</span></span>

<span data-ttu-id="0298f-115">Use a função [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para definir o rótulo do link de comando e o texto suplementar por meio da mensagem do [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext) e da mensagem do [**BCM \_ setnote**](bcm-setnote.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="0298f-115">Use the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to set the command link label and supplementary text via the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message and the [**BCM\_SETNOTE**](bcm-setnote.md) message, respectively.</span></span>


```C++
SendMessage(hwndCommandLink, WM_SETTEXT, 0, (LPARAM)L"Command link");
SendMessage(hwndCommandLink, BCM_SETNOTE, 0, (LPARAM)L"with note");
```



## <a name="related-topics"></a><span data-ttu-id="0298f-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0298f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0298f-117">Sobre os botões</span><span class="sxs-lookup"><span data-stu-id="0298f-117">About Buttons</span></span>](about-buttons.md)
</dt> <dt>

[<span data-ttu-id="0298f-118">Referência de controle de botão</span><span class="sxs-lookup"><span data-stu-id="0298f-118">Button Control Reference</span></span>](bumper-button-button-control-reference.md)
</dt> <dt>

[<span data-ttu-id="0298f-119">Usando botões</span><span class="sxs-lookup"><span data-stu-id="0298f-119">Using Buttons</span></span>](using-buttons.md)
</dt> <dt>

[<span data-ttu-id="0298f-120">Botão</span><span class="sxs-lookup"><span data-stu-id="0298f-120">Button</span></span>](buttons.md)
</dt> </dl>

 

 