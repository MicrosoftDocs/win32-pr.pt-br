---
title: Como criar um botão
description: Para criar botões dinamicamente, use a função CreateWindow ou CreateWindowEx. Este tópico demonstra como usar a função CreateWindow para criar um botão de ação padrão.
ms.assetid: A8C56D09-90A3-4C70-9907-61390521D1DA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dadc53f91f773e5fce9e29bdf1ae50cc59bfdfd
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104008628"
---
# <a name="how-to-create-a-button"></a><span data-ttu-id="b2637-104">Como criar um botão</span><span class="sxs-lookup"><span data-stu-id="b2637-104">How to Create a Button</span></span>

<span data-ttu-id="b2637-105">Para criar botões dinamicamente, use a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="b2637-105">To create buttons dynamically, you use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="b2637-106">Este tópico demonstra como usar a função **CreateWindow** para criar um botão de ação padrão.</span><span class="sxs-lookup"><span data-stu-id="b2637-106">This topic demonstrates how to use the **CreateWindow** function to create a default push button.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="b2637-107">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="b2637-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="b2637-108">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="b2637-108">Technologies</span></span>

-   [<span data-ttu-id="b2637-109">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="b2637-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="b2637-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="b2637-110">Prerequisites</span></span>

-   <span data-ttu-id="b2637-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="b2637-111">C/C++</span></span>
-   <span data-ttu-id="b2637-112">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="b2637-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="b2637-113">Instruções</span><span class="sxs-lookup"><span data-stu-id="b2637-113">Instructions</span></span>


<span data-ttu-id="b2637-114">Use a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) para criar um controle de botão.</span><span class="sxs-lookup"><span data-stu-id="b2637-114">Use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function to create a button control.</span></span>

<span data-ttu-id="b2637-115">No exemplo de C++ a seguir, o parâmetro de *\_ HWND m* é o identificador para a janela pai.</span><span class="sxs-lookup"><span data-stu-id="b2637-115">In the following C++ example, the *m\_hwnd* parameter is the handle to the parent window.</span></span> <span data-ttu-id="b2637-116">O estilo de [**\_ DEFPUSHBUTTON BS**](button-styles.md) especifica que um botão de push padrão deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="b2637-116">The [**BS\_DEFPUSHBUTTON**](button-styles.md) style specifies that a default push button should be created.</span></span> <span data-ttu-id="b2637-117">Observe que os valores de tamanho e posição devem ser especificados porque o uso de **\_ USEDEFAULT de PV** para um botão define os valores como zero.</span><span class="sxs-lookup"><span data-stu-id="b2637-117">Note that the size and position values must be specified because using **CW\_USEDEFAULT** for a button sets the values to zero.</span></span>


```C++
HWND hwndButton = CreateWindow( 
    L"BUTTON",  // Predefined class; Unicode assumed 
    L"OK",      // Button text 
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_DEFPUSHBUTTON,  // Styles 
    10,         // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu.
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed.
```



## <a name="related-topics"></a><span data-ttu-id="b2637-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b2637-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2637-119">Sobre os botões</span><span class="sxs-lookup"><span data-stu-id="b2637-119">About Buttons</span></span>](about-buttons.md)
</dt> <dt>

[<span data-ttu-id="b2637-120">Referência de controle de botão</span><span class="sxs-lookup"><span data-stu-id="b2637-120">Button Control Reference</span></span>](bumper-button-button-control-reference.md)
</dt> <dt>

[<span data-ttu-id="b2637-121">Usando botões</span><span class="sxs-lookup"><span data-stu-id="b2637-121">Using Buttons</span></span>](using-buttons.md)
</dt> <dt>

[<span data-ttu-id="b2637-122">Botão</span><span class="sxs-lookup"><span data-stu-id="b2637-122">Button</span></span>](buttons.md)
</dt> </dl>

 

 