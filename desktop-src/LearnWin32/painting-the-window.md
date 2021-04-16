---
title: Pintando a janela
description: Você criou sua janela. Agora você deseja mostrar algo dentro dele. Na terminologia do Windows, isso é chamado de pintura da janela. Para misturar metáforas, uma janela é uma tela em branco, esperando que você a preencha.
ms.assetid: db97a4c9-7592-42d1-a5de-9c468169eefc
ms.topic: article
ms.date: 08/16/2019
ms.openlocfilehash: f0f9d5c2759ea1735e370eb258743364980daee8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104567073"
---
# <a name="painting-the-window"></a><span data-ttu-id="f56c4-106">Pintando a janela</span><span class="sxs-lookup"><span data-stu-id="f56c4-106">Painting the Window</span></span>

<span data-ttu-id="f56c4-107">Você criou sua janela.</span><span class="sxs-lookup"><span data-stu-id="f56c4-107">You've created your window.</span></span> <span data-ttu-id="f56c4-108">Agora você deseja mostrar algo dentro dele.</span><span class="sxs-lookup"><span data-stu-id="f56c4-108">Now you want to show something inside it.</span></span> <span data-ttu-id="f56c4-109">Na terminologia do Windows, isso é chamado de pintura da janela.</span><span class="sxs-lookup"><span data-stu-id="f56c4-109">In Windows terminology, this is called painting the window.</span></span> <span data-ttu-id="f56c4-110">Para misturar metáforas, uma janela é uma tela em branco, esperando que você a preencha.</span><span class="sxs-lookup"><span data-stu-id="f56c4-110">To mix metaphors, a window is a blank canvas, waiting for you to fill it.</span></span>

<span data-ttu-id="f56c4-111">Às vezes, o programa começará a pintar para atualizar a aparência da janela.</span><span class="sxs-lookup"><span data-stu-id="f56c4-111">Sometimes your program will initiate painting to update the appearance of the window.</span></span> <span data-ttu-id="f56c4-112">Em outras ocasiões, o sistema operacional o notificará de que você deve redesenhar uma parte da janela.</span><span class="sxs-lookup"><span data-stu-id="f56c4-112">At other times, the operating system will notify you that you must repaint a portion of the window.</span></span> <span data-ttu-id="f56c4-113">Quando isso ocorre, o sistema operacional envia a janela uma mensagem do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="f56c4-113">When this occurs, the operating system sends the window a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span> <span data-ttu-id="f56c4-114">A parte da janela que deve ser pintada é chamada de *região de atualização*.</span><span class="sxs-lookup"><span data-stu-id="f56c4-114">The portion of the window that must be painted is called the *update region*.</span></span>

<span data-ttu-id="f56c4-115">Na primeira vez em que uma janela é mostrada, toda a área do cliente da janela deve ser pintada.</span><span class="sxs-lookup"><span data-stu-id="f56c4-115">The first time a window is shown, the entire client area of the window must be painted.</span></span> <span data-ttu-id="f56c4-116">Portanto, você sempre receberá pelo menos uma mensagem do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) quando mostrar uma janela.</span><span class="sxs-lookup"><span data-stu-id="f56c4-116">Therefore, you will always receive at least one [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message when you show a window.</span></span>

![ilustração mostrando a região de atualização de uma janela](images/painting01.png)

<span data-ttu-id="f56c4-118">Você só é responsável por pintar a área do cliente.</span><span class="sxs-lookup"><span data-stu-id="f56c4-118">You are only responsible for painting the client area.</span></span> <span data-ttu-id="f56c4-119">O quadro ao redor, incluindo a barra de título, é pintado automaticamente pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f56c4-119">The surrounding frame, including the title bar, is automatically painted by the operating system.</span></span> <span data-ttu-id="f56c4-120">Depois de terminar a pintura da área do cliente, desmarque a região de atualização, que informa ao sistema operacional que ele não precisa enviar outra mensagem do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) até que algo seja alterado.</span><span class="sxs-lookup"><span data-stu-id="f56c4-120">After you finish painting the client area, you clear the update region, which tells the operating system that it does not need to send another [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message until something changes.</span></span>

<span data-ttu-id="f56c4-121">Agora suponha que o usuário mova outra janela para que ela oculte uma parte da sua janela.</span><span class="sxs-lookup"><span data-stu-id="f56c4-121">Now suppose the user moves another window so that it obscures a portion of your window.</span></span> <span data-ttu-id="f56c4-122">Quando a parte obscurecida se tornar visível novamente, essa parte será adicionada à região de atualização e sua janela receberá outra mensagem de [**\_ pintura do WM**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="f56c4-122">When the obscured portion becomes visible again, that portion is added to the update region, and your window receives another [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span>

![ilustração que mostra como a região de atualização muda quando duas janelas se sobrepõem](images/painting02.png)

<span data-ttu-id="f56c4-124">A região de atualização também será alterada se o usuário alongar a janela.</span><span class="sxs-lookup"><span data-stu-id="f56c4-124">The update region also changes if the user stretches the window.</span></span> <span data-ttu-id="f56c4-125">No diagrama a seguir, o usuário alonga a janela para a direita.</span><span class="sxs-lookup"><span data-stu-id="f56c4-125">In the following diagram, the user stretches the window to the right.</span></span> <span data-ttu-id="f56c4-126">A área exposta recentemente no lado direito da janela é adicionada à região de atualização:</span><span class="sxs-lookup"><span data-stu-id="f56c4-126">The newly exposed area on the right side of the window is added to the update region:</span></span>

![ilustração que mostra como a região de atualização é alterada quando uma janela é redimensionada](images/painting03.png)

<span data-ttu-id="f56c4-128">Em nosso primeiro programa de exemplo, a rotina de pintura é muito simples.</span><span class="sxs-lookup"><span data-stu-id="f56c4-128">In our first example program, the painting routine is very simple.</span></span> <span data-ttu-id="f56c4-129">Ele apenas preenche toda a área do cliente com uma cor sólida.</span><span class="sxs-lookup"><span data-stu-id="f56c4-129">It just fills the entire client area with a solid color.</span></span> <span data-ttu-id="f56c4-130">Ainda assim, esse exemplo é suficiente para demonstrar alguns dos conceitos importantes.</span><span class="sxs-lookup"><span data-stu-id="f56c4-130">Still, this example is enough to demonstrate some of the important concepts.</span></span>

```C++
switch (uMsg)
{
    case WM_PAINT:
    {
        PAINTSTRUCT ps;
        HDC hdc = BeginPaint(hwnd, &ps);

        // All painting occurs here, between BeginPaint and EndPaint.

        FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));

        EndPaint(hwnd, &ps);
    }
    return 0;
}
```

<span data-ttu-id="f56c4-131">Inicie a operação de pintura chamando a função [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) .</span><span class="sxs-lookup"><span data-stu-id="f56c4-131">Start the painting operation by calling the [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) function.</span></span> <span data-ttu-id="f56c4-132">Essa função preenche a estrutura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) com informações sobre a solicitação Repaint.</span><span class="sxs-lookup"><span data-stu-id="f56c4-132">This function fills in the [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure with information on the repaint request.</span></span> <span data-ttu-id="f56c4-133">A região de atualização atual é fornecida no membro **rcPaint** de **PAINTSTRUCT**.</span><span class="sxs-lookup"><span data-stu-id="f56c4-133">The current update region is given in the **rcPaint** member of **PAINTSTRUCT**.</span></span> <span data-ttu-id="f56c4-134">Essa região de atualização é definida em relação à área do cliente:</span><span class="sxs-lookup"><span data-stu-id="f56c4-134">This update region is defined relative to the client area:</span></span>

![ilustração mostrando a origem da área do cliente](images/painting04.png)

<span data-ttu-id="f56c4-136">No seu código de pintura, você tem duas opções básicas:</span><span class="sxs-lookup"><span data-stu-id="f56c4-136">In your painting code, you have two basic options:</span></span>

- <span data-ttu-id="f56c4-137">Pinte toda a área do cliente, independentemente do tamanho da região de atualização.</span><span class="sxs-lookup"><span data-stu-id="f56c4-137">Paint the entire client area, regardless of the size of the update region.</span></span> <span data-ttu-id="f56c4-138">Qualquer coisa que esteja fora da região de atualização é recortada.</span><span class="sxs-lookup"><span data-stu-id="f56c4-138">Anything that falls outside of the update region is clipped.</span></span> <span data-ttu-id="f56c4-139">Ou seja, o sistema operacional o ignora.</span><span class="sxs-lookup"><span data-stu-id="f56c4-139">That is, the operating system ignores it.</span></span>
- <span data-ttu-id="f56c4-140">Otimizar pintando apenas a parte da janela dentro da região de atualização.</span><span class="sxs-lookup"><span data-stu-id="f56c4-140">Optimize by painting just the portion of the window inside the update region.</span></span>

<span data-ttu-id="f56c4-141">Se você sempre pintar toda a área do cliente, o código será mais simples.</span><span class="sxs-lookup"><span data-stu-id="f56c4-141">If you always paint the entire client area, the code will be simpler.</span></span> <span data-ttu-id="f56c4-142">No entanto, se você tiver uma lógica de pintura complicada, poderá ser mais eficiente ignorar as áreas fora da região de atualização.</span><span class="sxs-lookup"><span data-stu-id="f56c4-142">If you have complicated painting logic, however, it can be more efficient to skip the areas outside of the update region.</span></span>

<span data-ttu-id="f56c4-143">A linha de código a seguir preenche a região de atualização com uma única cor, usando a cor de plano de fundo da janela definida pelo sistema (**\_ janela de cores**).</span><span class="sxs-lookup"><span data-stu-id="f56c4-143">The following line of code fills the update region with a single color, using the system-defined window background color (**COLOR\_WINDOW**).</span></span> <span data-ttu-id="f56c4-144">A cor real indicada pela **\_ janela de cores** depende do esquema de cores atual do usuário.</span><span class="sxs-lookup"><span data-stu-id="f56c4-144">The actual color indicated by **COLOR\_WINDOW** depends on the user's current color scheme.</span></span>

```C++
FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
```

<span data-ttu-id="f56c4-145">Os detalhes de [**FillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) não são importantes para este exemplo, mas o segundo parâmetro fornece as coordenadas do retângulo a preencher.</span><span class="sxs-lookup"><span data-stu-id="f56c4-145">The details of [**FillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) are not important for this example, but the second parameter gives the coordinates of the rectangle to fill.</span></span> <span data-ttu-id="f56c4-146">Nesse caso, passamos toda a região de atualização (o membro **rcPaint** de [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)).</span><span class="sxs-lookup"><span data-stu-id="f56c4-146">In this case, we pass in the entire update region (the **rcPaint** member of [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)).</span></span> <span data-ttu-id="f56c4-147">Na primeira mensagem do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) , toda a área do cliente precisa ser pintada, portanto, **rcPaint** conterá toda a área do cliente.</span><span class="sxs-lookup"><span data-stu-id="f56c4-147">On the first [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message, the entire client area needs to be painted, so **rcPaint** will contain the entire client area.</span></span> <span data-ttu-id="f56c4-148">Em mensagens **de \_ pintura do WM** subsequentes, **rcPaint** pode conter um retângulo menor.</span><span class="sxs-lookup"><span data-stu-id="f56c4-148">On subsequent **WM\_PAINT** messages, **rcPaint** might contain a smaller rectangle.</span></span>

<span data-ttu-id="f56c4-149">A função [**FillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) faz parte do Graphics Device Interface (GDI), que tem gráficos do Windows alimentados por muito tempo.</span><span class="sxs-lookup"><span data-stu-id="f56c4-149">The [**FillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) function is part of the Graphics Device Interface (GDI), which has powered Windows graphics for a very long time.</span></span> <span data-ttu-id="f56c4-150">No Windows 7, a Microsoft introduziu um novo mecanismo de gráficos, chamado Direct2D, que dá suporte a operações gráficas de alto desempenho, como aceleração de hardware.</span><span class="sxs-lookup"><span data-stu-id="f56c4-150">In Windows 7, Microsoft introduced a new graphics engine, named Direct2D, which supports high-performance graphics operations, such as hardware acceleration.</span></span> <span data-ttu-id="f56c4-151">O Direct2D também está disponível para o Windows Vista por meio da [atualização de plataforma para Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md) e windows Server 2008 por meio da atualização de plataforma para o windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="f56c4-151">Direct2D is also available for Windows Vista through the [Platform Update for Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md) and for Windows Server 2008 through the Platform Update for Windows Server 2008.</span></span> <span data-ttu-id="f56c4-152">(A GDI ainda tem suporte total.)</span><span class="sxs-lookup"><span data-stu-id="f56c4-152">(GDI is still fully supported.)</span></span>

<span data-ttu-id="f56c4-153">Depois de terminar a pintura, chame a função [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) .</span><span class="sxs-lookup"><span data-stu-id="f56c4-153">After you are done painting, call the [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) function.</span></span> <span data-ttu-id="f56c4-154">Essa função limpa a região de atualização, que sinaliza ao Windows que a janela concluiu a pintura em si.</span><span class="sxs-lookup"><span data-stu-id="f56c4-154">This function clears the update region, which signals to Windows that the window has completed painting itself.</span></span>

## <a name="next"></a><span data-ttu-id="f56c4-155">Avançar</span><span class="sxs-lookup"><span data-stu-id="f56c4-155">Next</span></span>

[<span data-ttu-id="f56c4-156">Fechando a janela</span><span class="sxs-lookup"><span data-stu-id="f56c4-156">Closing the Window</span></span>](closing-the-window.md)