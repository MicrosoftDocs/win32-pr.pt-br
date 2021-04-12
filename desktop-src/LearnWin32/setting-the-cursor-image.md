---
title: Definindo a imagem do cursor
description: Definindo a imagem do cursor
ms.assetid: FB223131-19AE-41DD-87DE-73992AE2A0CA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3bc993b7566dee1fa47bd2b53c270ad0e4f64b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454009"
---
# <a name="setting-the-cursor-image"></a><span data-ttu-id="d419f-103">Definindo a imagem do cursor</span><span class="sxs-lookup"><span data-stu-id="d419f-103">Setting the Cursor Image</span></span>

<span data-ttu-id="d419f-104">O *cursor* é a imagem pequena que mostra o local do mouse ou outro dispositivo apontador.</span><span class="sxs-lookup"><span data-stu-id="d419f-104">The *cursor* is the small image that shows the location of the mouse or other pointing device.</span></span> <span data-ttu-id="d419f-105">Muitos aplicativos alteram a imagem do cursor para fornecer comentários ao usuário.</span><span class="sxs-lookup"><span data-stu-id="d419f-105">Many applications change the cursor image to give feedback to the user.</span></span> <span data-ttu-id="d419f-106">Embora não seja necessário, ele adiciona um pouco de polonês ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d419f-106">Although it is not required, it adds a nice bit of polish to your application.</span></span>

<span data-ttu-id="d419f-107">O Windows fornece um conjunto de imagens de cursor padrão, chamadas *cursores do sistema*.</span><span class="sxs-lookup"><span data-stu-id="d419f-107">Windows provides a set of standard cursor images, called *system cursors*.</span></span> <span data-ttu-id="d419f-108">Isso inclui a seta, a mão, o I-feixe, a ampulheta (que agora é um círculo girando) e outros.</span><span class="sxs-lookup"><span data-stu-id="d419f-108">These include the arrow, the hand, the I-beam, the hourglass (which is now a spinning circle), and others.</span></span> <span data-ttu-id="d419f-109">Esta seção descreve como usar os cursores do sistema.</span><span class="sxs-lookup"><span data-stu-id="d419f-109">This section describes how to use the system cursors.</span></span> <span data-ttu-id="d419f-110">Para tarefas mais avançadas, como a criação de cursores personalizados, consulte [cursores](/windows/desktop/menurc/cursors).</span><span class="sxs-lookup"><span data-stu-id="d419f-110">For more advanced tasks, such as creating custom cursors, see [Cursors](/windows/desktop/menurc/cursors).</span></span>

<span data-ttu-id="d419f-111">Você pode associar um cursor a uma classe de janela definindo o membro **hCursor** da estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) ou [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) .</span><span class="sxs-lookup"><span data-stu-id="d419f-111">You can associate a cursor with a window class by setting the **hCursor** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) or [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) structure.</span></span> <span data-ttu-id="d419f-112">Caso contrário, o cursor padrão será a seta.</span><span class="sxs-lookup"><span data-stu-id="d419f-112">Otherwise, the default cursor is the arrow.</span></span> <span data-ttu-id="d419f-113">Quando o mouse se move sobre uma janela, a janela recebe uma mensagem do [**WM \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) (a menos que outra janela tenha capturado o mouse).</span><span class="sxs-lookup"><span data-stu-id="d419f-113">When the mouse moves over a window, the window receives a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message (unless another window has captured the mouse).</span></span> <span data-ttu-id="d419f-114">Neste ponto, ocorre um dos seguintes eventos:</span><span class="sxs-lookup"><span data-stu-id="d419f-114">At this point, one of the following events occurs:</span></span>

-   <span data-ttu-id="d419f-115">O aplicativo define o cursor e o procedimento de janela retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="d419f-115">The application sets the cursor and the window procedure returns **TRUE**.</span></span>
-   <span data-ttu-id="d419f-116">O aplicativo não faz nada e passa o [**WM \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="d419f-116">The application does nothing and passes [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="d419f-117">Para definir o cursor, um programa faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d419f-117">To set the cursor, a program does the following:</span></span>

1.  <span data-ttu-id="d419f-118">Chama [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) para carregar o cursor na memória.</span><span class="sxs-lookup"><span data-stu-id="d419f-118">Calls [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) to load the cursor into memory.</span></span> <span data-ttu-id="d419f-119">Essa função retorna um identificador para o cursor.</span><span class="sxs-lookup"><span data-stu-id="d419f-119">This function returns a handle to the cursor.</span></span>
2.  <span data-ttu-id="d419f-120">Chama [**SetCursor**](/windows/desktop/api/winuser/nf-winuser-setcursor) e passa na alça do cursor.</span><span class="sxs-lookup"><span data-stu-id="d419f-120">Calls [**SetCursor**](/windows/desktop/api/winuser/nf-winuser-setcursor) and passes in the cursor handle.</span></span>

<span data-ttu-id="d419f-121">Caso contrário, se o aplicativo passar o [**WM \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), a função **DefWindowProc** usará o seguinte algoritmo para definir a imagem do cursor:</span><span class="sxs-lookup"><span data-stu-id="d419f-121">Otherwise, if the application passes [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), the **DefWindowProc** function uses the following algorithm to set the cursor image:</span></span>

1.  <span data-ttu-id="d419f-122">Se a janela tiver um pai, encaminhe a mensagem do [**WM \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) para o pai a ser manipulado.</span><span class="sxs-lookup"><span data-stu-id="d419f-122">If the window has a parent, forward the [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message to the parent to handle.</span></span>
2.  <span data-ttu-id="d419f-123">Caso contrário, se a janela tiver um cursor de classe, defina o cursor para o cursor de classe.</span><span class="sxs-lookup"><span data-stu-id="d419f-123">Otherwise, if the window has a class cursor, set the cursor to the class cursor.</span></span>
3.  <span data-ttu-id="d419f-124">Se não houver um cursor de classe, defina o cursor para o cursor de seta.</span><span class="sxs-lookup"><span data-stu-id="d419f-124">If there is no class cursor, set the cursor to the arrow cursor.</span></span>

<span data-ttu-id="d419f-125">A função [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) pode carregar um cursor personalizado de um recurso ou um dos cursores do sistema.</span><span class="sxs-lookup"><span data-stu-id="d419f-125">The [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) function can load either a custom cursor from a resource, or one of the system cursors.</span></span> <span data-ttu-id="d419f-126">O exemplo a seguir mostra como definir o cursor para o cursor da mão do sistema.</span><span class="sxs-lookup"><span data-stu-id="d419f-126">The following example shows how to set the cursor to the system hand cursor.</span></span>


```C++
    hCursor = LoadCursor(NULL, cursor);
    SetCursor(hCursor);
```



<span data-ttu-id="d419f-127">Se você alterar o cursor, a imagem do cursor será redefinida na próxima movimentação do mouse, a menos que você intercepte a mensagem do [**WM \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) e defina o cursor novamente.</span><span class="sxs-lookup"><span data-stu-id="d419f-127">If you change the cursor, the cursor image resets on the next mouse move, unless you intercept the [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message and set the cursor again.</span></span> <span data-ttu-id="d419f-128">O código a seguir mostra como manipular o **WM \_ SetCursor**.</span><span class="sxs-lookup"><span data-stu-id="d419f-128">The following code shows how to handle **WM\_SETCURSOR**.</span></span>


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



<span data-ttu-id="d419f-129">Esse código primeiro verifica os 16 bits inferiores de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="d419f-129">This code first checks the lower 16 bits of *lParam*.</span></span> <span data-ttu-id="d419f-130">Se for `LOWORD(lParam)` igual a **HTCLIENT**, significa que o cursor está sobre a área do cliente da janela.</span><span class="sxs-lookup"><span data-stu-id="d419f-130">If `LOWORD(lParam)` equals **HTCLIENT**, it means the cursor is over the client area of the window.</span></span> <span data-ttu-id="d419f-131">Caso contrário, o cursor está sobre a área que não é do cliente.</span><span class="sxs-lookup"><span data-stu-id="d419f-131">Otherwise, the cursor is over the nonclient area.</span></span> <span data-ttu-id="d419f-132">Normalmente, você só deve definir o cursor para a área do cliente e deixar o Windows definir o cursor para a área não cliente.</span><span class="sxs-lookup"><span data-stu-id="d419f-132">Typically, you should only set the cursor for the client area, and let Windows set the cursor for the nonclient area.</span></span>

## <a name="next"></a><span data-ttu-id="d419f-133">Avançar</span><span class="sxs-lookup"><span data-stu-id="d419f-133">Next</span></span>

[<span data-ttu-id="d419f-134">Entrada do usuário: exemplo estendido</span><span class="sxs-lookup"><span data-stu-id="d419f-134">User Input: Extended Example</span></span>](user-input--extended-example.md)

 

 