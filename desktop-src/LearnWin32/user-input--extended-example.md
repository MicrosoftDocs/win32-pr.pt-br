---
title: Exemplo estendido de entrada do usuário
description: .
ms.assetid: A408E0EC-E0A7-4F18-BFCA-21D28007FACC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdde7f14dda356d0f65103c77e3b73c2f0de50a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104557104"
---
# <a name="user-input-extended-example"></a><span data-ttu-id="fbb8f-103">Entrada do usuário: exemplo estendido</span><span class="sxs-lookup"><span data-stu-id="fbb8f-103">User Input: Extended Example</span></span>

<span data-ttu-id="fbb8f-104">Vamos combinar tudo o que aprendemos sobre a entrada do usuário para criar um programa simples de desenho.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-104">Let's combine everything that we have learned about user input to create a simple drawing program.</span></span> <span data-ttu-id="fbb8f-105">Aqui está uma captura de tela do programa:</span><span class="sxs-lookup"><span data-stu-id="fbb8f-105">Here is a screen shot of the program:</span></span>

![captura de tela do programa de desenho](images/input03.png)

<span data-ttu-id="fbb8f-107">O usuário pode desenhar reticências em várias cores diferentes e selecionar, mover ou excluir reticências.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-107">The user can draw ellipses in several different colors, and select, move, or delete ellipses.</span></span> <span data-ttu-id="fbb8f-108">Para manter a interface do usuário simples, o programa não permite que o usuário selecione as cores da elipse.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-108">To keep the UI simple, the program does not let the user select the ellipse colors.</span></span> <span data-ttu-id="fbb8f-109">Em vez disso, o programa percorre automaticamente uma lista predefinida de cores.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-109">Instead, the program automatically cycles through a predefined list of colors.</span></span> <span data-ttu-id="fbb8f-110">O programa não oferece suporte a formas diferentes de elipses.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-110">The program does not support any shapes other than ellipses.</span></span> <span data-ttu-id="fbb8f-111">Obviamente, esse programa não ganhará nenhum prêmio de software de gráficos.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-111">Obviously, this program will not win any awards for graphics software.</span></span> <span data-ttu-id="fbb8f-112">No entanto, ele ainda é um exemplo útil para aprender com o.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-112">However, it is still a useful example to learn from.</span></span> <span data-ttu-id="fbb8f-113">Você pode baixar o código-fonte completo do [exemplo de desenho simples](simple-drawing-sample.md).</span><span class="sxs-lookup"><span data-stu-id="fbb8f-113">You can download the complete source code from [Simple Drawing Sample](simple-drawing-sample.md).</span></span> <span data-ttu-id="fbb8f-114">Esta seção abordará apenas alguns destaques.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-114">This section will just cover some highlights.</span></span>

<span data-ttu-id="fbb8f-115">As elipses são representadas no programa por uma estrutura que contém os dados da elipse ([**\_ elipse d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) e a cor ([**d2d1 \_ cor \_ F**](/windows/desktop/Direct2D/d2d1-color-f)).</span><span class="sxs-lookup"><span data-stu-id="fbb8f-115">Ellipses are represented in the program by a structure that contains the ellipse data ([**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) and the color ([**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f)).</span></span> <span data-ttu-id="fbb8f-116">A estrutura também define dois métodos: um método para desenhar a elipse e um método para executar testes de clique.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-116">The structure also defines two methods: a method to draw the ellipse, and a method to perform hit testing.</span></span>


```C++
struct MyEllipse
{
    D2D1_ELLIPSE    ellipse;
    D2D1_COLOR_F    color;

    void Draw(ID2D1RenderTarget *pRT, ID2D1SolidColorBrush *pBrush)
    {
        pBrush->SetColor(color);
        pRT->FillEllipse(ellipse, pBrush);
        pBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black));
        pRT->DrawEllipse(ellipse, pBrush, 1.0f);
    }

    BOOL HitTest(float x, float y)
    {
        const float a = ellipse.radiusX;
        const float b = ellipse.radiusY;
        const float x1 = x - ellipse.point.x;
        const float y1 = y - ellipse.point.y;
        const float d = ((x1 * x1) / (a * a)) + ((y1 * y1) / (b * b));
        return d <= 1.0f;
    }
};
```



<span data-ttu-id="fbb8f-117">O programa usa o mesmo pincel de cor sólida para desenhar o preenchimento e a estrutura de tópicos para cada elipse, alterando a cor conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-117">The program uses the same solid-color brush to draw the fill and outline for every ellipse, changing the color as needed.</span></span> <span data-ttu-id="fbb8f-118">No Direct2D, a alteração da cor de um pincel de cor sólida é uma operação eficiente.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-118">In Direct2D, changing the color of a solid-color brush is an efficient operation.</span></span> <span data-ttu-id="fbb8f-119">Portanto, o objeto de pincel de cor sólida dá suporte a um método [**setColor**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) .</span><span class="sxs-lookup"><span data-stu-id="fbb8f-119">So, the solid-color brush object supports a [**SetColor**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) method.</span></span>

<span data-ttu-id="fbb8f-120">As reticências são armazenadas em um contêiner de **lista** STL:</span><span class="sxs-lookup"><span data-stu-id="fbb8f-120">The ellipses are stored in an STL **list** container:</span></span>


```C++
    list<shared_ptr<MyEllipse>>             ellipses;
```



> [!Note]  
> <span data-ttu-id="fbb8f-121">**o \_ PTR compartilhado** é uma classe de ponteiro inteligente que foi adicionada ao C++ no TR1 e formalizada em C + + 0x.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-121">**shared\_ptr** is a smart-pointer class that was added to C++ in TR1 and formalized in C++0x.</span></span> <span data-ttu-id="fbb8f-122">O Visual Studio 2010 adiciona suporte para r **\_ pt compartilhado** e outros recursos do C + + 0x.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-122">Visual Studio 2010 adds support for **shared\_pt** r and other C++0x features.</span></span> <span data-ttu-id="fbb8f-123">Para obter mais informações, consulte [explorando novos recursos de C++ e MFC no Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) na *msdn Magazine*.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-123">For more information, see [Exploring New C++ and MFC Features in Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) in *MSDN Magazine*.</span></span> <span data-ttu-id="fbb8f-124">(Esse recurso pode não estar disponível em alguns idiomas e países.)</span><span class="sxs-lookup"><span data-stu-id="fbb8f-124">(This resource may not be available in some languages and countries.)</span></span>

 

<span data-ttu-id="fbb8f-125">O programa tem três modos:</span><span class="sxs-lookup"><span data-stu-id="fbb8f-125">The program has three modes:</span></span>

-   <span data-ttu-id="fbb8f-126">Modo de desenho.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-126">Draw mode.</span></span> <span data-ttu-id="fbb8f-127">O usuário pode desenhar novas elipses.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-127">The user can draw new ellipses.</span></span>
-   <span data-ttu-id="fbb8f-128">Modo de seleção.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-128">Selection mode.</span></span> <span data-ttu-id="fbb8f-129">O usuário pode selecionar uma elipse.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-129">The user can select an ellipse.</span></span>
-   <span data-ttu-id="fbb8f-130">Modo de arrastar.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-130">Drag mode.</span></span> <span data-ttu-id="fbb8f-131">O usuário pode arrastar uma elipse selecionada.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-131">The user can drag a selected ellipse.</span></span>

<span data-ttu-id="fbb8f-132">O usuário pode alternar entre o modo de desenho e o modo de seleção usando os mesmos atalhos de teclado descritos em [tabelas de aceleração](accelerator-tables.md).</span><span class="sxs-lookup"><span data-stu-id="fbb8f-132">The user can switch between draw mode and selection mode by using the same keyboard shortcuts described in [Accelerator Tables](accelerator-tables.md).</span></span> <span data-ttu-id="fbb8f-133">No modo de seleção, o programa alternará para o modo de arrastar se o usuário clicar em uma elipse.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-133">From selection mode, the program switches to drag mode if the user clicks on an ellipse.</span></span> <span data-ttu-id="fbb8f-134">Ele volta para o modo de seleção quando o usuário libera o botão do mouse.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-134">It switches back to selection mode when the user releases the mouse button.</span></span> <span data-ttu-id="fbb8f-135">A seleção atual é armazenada como um iterador na lista de reticências.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-135">The current selection is stored as an iterator into the list of ellipses.</span></span> <span data-ttu-id="fbb8f-136">O método auxiliar `MainWindow::Selection` retorna um ponteiro para a elipse selecionada ou o valor **nullptr** se não houver nenhuma seleção.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-136">The helper method `MainWindow::Selection` returns a pointer to the selected ellipse, or the value **nullptr** if there is no selection.</span></span>


```C++
    list<shared_ptr<MyEllipse>>::iterator   selection;
     
    shared_ptr<MyEllipse> Selection() 
    { 
        if (selection == ellipses.end()) 
        { 
            return nullptr;
        }
        else
        {
            return (*selection);
        }
    }

    void    ClearSelection() { selection = ellipses.end(); }
```



<span data-ttu-id="fbb8f-137">A tabela a seguir resume os efeitos da entrada do mouse em cada um dos três modos.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-137">The following table summarizes the effects of mouse input in each of the three modes.</span></span>



| <span data-ttu-id="fbb8f-138">Entrada do mouse</span><span class="sxs-lookup"><span data-stu-id="fbb8f-138">Mouse Input</span></span>      | <span data-ttu-id="fbb8f-139">Modo de Desenho</span><span class="sxs-lookup"><span data-stu-id="fbb8f-139">Draw Mode</span></span>                                          | <span data-ttu-id="fbb8f-140">Modo de seleção</span><span class="sxs-lookup"><span data-stu-id="fbb8f-140">Selection Mode</span></span>                                                                                                                               | <span data-ttu-id="fbb8f-141">Modo de arrastar</span><span class="sxs-lookup"><span data-stu-id="fbb8f-141">Drag Mode</span></span>                  |
|------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span data-ttu-id="fbb8f-142">Botão esquerdo para baixo</span><span class="sxs-lookup"><span data-stu-id="fbb8f-142">Left button down</span></span> | <span data-ttu-id="fbb8f-143">Defina a captura do mouse e comece a desenhar uma nova elipse.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-143">Set mouse capture and start to draw a new ellipse.</span></span> | <span data-ttu-id="fbb8f-144">Libere a seleção atual e execute um teste de clique.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-144">Release the current selection and perform a hit test.</span></span> <span data-ttu-id="fbb8f-145">Se uma elipse for atingida, Capture o cursor, selecione a elipse e alterne para o modo de arrastar.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-145">If an ellipse is hit, capture the cursor, select the ellipse, and switch to drag mode.</span></span> | <span data-ttu-id="fbb8f-146">Nenhuma ação.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-146">No action.</span></span>                 |
| <span data-ttu-id="fbb8f-147">Movimentação do mouse</span><span class="sxs-lookup"><span data-stu-id="fbb8f-147">Mouse move</span></span>       | <span data-ttu-id="fbb8f-148">Se o botão esquerdo estiver inativo, redimensione a elipse.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-148">If the left button is down, resize the ellipse.</span></span>    | <span data-ttu-id="fbb8f-149">Nenhuma ação.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-149">No action.</span></span>                                                                                                                                   | <span data-ttu-id="fbb8f-150">Mova a elipse selecionada.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-150">Move the selected ellipse.</span></span> |
| <span data-ttu-id="fbb8f-151">Botão esquerdo para cima</span><span class="sxs-lookup"><span data-stu-id="fbb8f-151">Left button up</span></span>   | <span data-ttu-id="fbb8f-152">Pare de desenhar a elipse.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-152">Stop drawing the ellipse.</span></span>                          | <span data-ttu-id="fbb8f-153">Nenhuma ação.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-153">No action.</span></span>                                                                                                                                   | <span data-ttu-id="fbb8f-154">Alternar para o modo de seleção.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-154">Switch to selection mode.</span></span>  |



 

<span data-ttu-id="fbb8f-155">O método a seguir na `MainWindow` classe trata as mensagens do [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) .</span><span class="sxs-lookup"><span data-stu-id="fbb8f-155">The following method in the `MainWindow` class handles [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) messages.</span></span>


```C++
void MainWindow::OnLButtonDown(int pixelX, int pixelY, DWORD flags)
{
    const float dipX = DPIScale::PixelsToDipsX(pixelX);
    const float dipY = DPIScale::PixelsToDipsY(pixelY);

    if (mode == DrawMode)
    {
        POINT pt = { pixelX, pixelY };

        if (DragDetect(m_hwnd, pt))
        {
            SetCapture(m_hwnd);
        
            // Start a new ellipse.
            InsertEllipse(dipX, dipY);
        }
    }
    else
    {
        ClearSelection();

        if (HitTest(dipX, dipY))
        {
            SetCapture(m_hwnd);

            ptMouse = Selection()->ellipse.point;
            ptMouse.x -= dipX;
            ptMouse.y -= dipY;

            SetMode(DragMode);
        }
    }
    InvalidateRect(m_hwnd, NULL, FALSE);
}
```



<span data-ttu-id="fbb8f-156">As coordenadas do mouse são passadas para esse método em pixels e, em seguida, convertidas em DIPs.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-156">Mouse coordinates are passed to this method in pixels, and then converted to DIPs.</span></span> <span data-ttu-id="fbb8f-157">É importante não confundir essas duas unidades.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-157">It is important not to confuse these two units.</span></span> <span data-ttu-id="fbb8f-158">Por exemplo, a função [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) usa pixels, mas os testes de desenho e de clique em uso ficam DIPs.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-158">For example, the [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) function uses pixels, but drawing and hit-testing use DIPs.</span></span> <span data-ttu-id="fbb8f-159">A regra geral é que as funções relacionadas à entrada do Windows ou do mouse usam pixels, enquanto Direct2D e DirectWrite usam DIPs.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-159">The general rule is that functions related to windows or mouse input use pixels, while Direct2D and DirectWrite use DIPs.</span></span> <span data-ttu-id="fbb8f-160">Sempre teste seu programa em uma configuração de alto DPI e lembre-se de marcar seu programa como com reconhecimento de DPI.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-160">Always test your program at a high-DPI setting, and remember to mark your program as DPI-aware.</span></span> <span data-ttu-id="fbb8f-161">Para obter mais informações, consulte [dpi e Device-Independent pixels](dpi-and-device-independent-pixels.md).</span><span class="sxs-lookup"><span data-stu-id="fbb8f-161">For more information, see [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).</span></span>

<span data-ttu-id="fbb8f-162">Este é o código que manipula as mensagens [**\_ MOUSEMOVE do WM**](/windows/desktop/inputdev/wm-mousemove) .</span><span class="sxs-lookup"><span data-stu-id="fbb8f-162">Here is the code that handles [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages.</span></span>


```C++
void MainWindow::OnMouseMove(int pixelX, int pixelY, DWORD flags)
{
    const float dipX = DPIScale::PixelsToDipsX(pixelX);
    const float dipY = DPIScale::PixelsToDipsY(pixelY);

    if ((flags & MK_LBUTTON) && Selection())
    { 
        if (mode == DrawMode)
        {
            // Resize the ellipse.
            const float width = (dipX - ptMouse.x) / 2;
            const float height = (dipY - ptMouse.y) / 2;
            const float x1 = ptMouse.x + width;
            const float y1 = ptMouse.y + height;

            Selection()->ellipse = D2D1::Ellipse(D2D1::Point2F(x1, y1), width, height);
        }
        else if (mode == DragMode)
        {
            // Move the ellipse.
            Selection()->ellipse.point.x = dipX + ptMouse.x;
            Selection()->ellipse.point.y = dipY + ptMouse.y;
        }
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



<span data-ttu-id="fbb8f-163">A lógica para redimensionar uma elipse foi descrita anteriormente, na seção [exemplo: círculos de desenho](mouse-movement.md).</span><span class="sxs-lookup"><span data-stu-id="fbb8f-163">The logic to resize an ellipse was described previously, in the section [Example: Drawing Circles](mouse-movement.md).</span></span> <span data-ttu-id="fbb8f-164">Observe também a chamada para [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span><span class="sxs-lookup"><span data-stu-id="fbb8f-164">Also note the call to [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span></span> <span data-ttu-id="fbb8f-165">Isso garante que a janela seja repintada.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-165">This makes sure that the window is repainted.</span></span> <span data-ttu-id="fbb8f-166">O código a seguir manipula mensagens do [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) .</span><span class="sxs-lookup"><span data-stu-id="fbb8f-166">The following code handles [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) messages.</span></span>


```C++
void MainWindow::OnLButtonUp()
{
    if ((mode == DrawMode) && Selection())
    {
        ClearSelection();
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
    else if (mode == DragMode)
    {
        SetMode(SelectMode);
    }
    ReleaseCapture(); 
}
```



<span data-ttu-id="fbb8f-167">Como você pode ver, os manipuladores de mensagens para entrada do mouse têm código de ramificação, dependendo do modo atual.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-167">As you can see, the message handlers for mouse input all have branching code, depending on the current mode.</span></span> <span data-ttu-id="fbb8f-168">Esse é um design aceitável para esse programa bastante simples.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-168">That is an acceptable design for this fairly simple program.</span></span> <span data-ttu-id="fbb8f-169">No entanto, ele pode rapidamente se tornar muito complexo se novos modos forem adicionados.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-169">However, it could quickly become too complex if new modes are added.</span></span> <span data-ttu-id="fbb8f-170">Para um programa maior, uma arquitetura MVC (Model-View-Controller) pode ser um design melhor.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-170">For a larger program, a model-view-controller (MVC) architecture might be a better design.</span></span> <span data-ttu-id="fbb8f-171">Nesse tipo de arquitetura, o *controlador*, que manipula a entrada do usuário, é separado do *modelo*, que gerencia os dados do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-171">In this kind of architecture, the *controller*, which handles user input, is separated from the *model*, which manages application data.</span></span>

<span data-ttu-id="fbb8f-172">Quando o programa muda de modos, o cursor é alterado para fornecer comentários ao usuário.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-172">When the program switches modes, the cursor changes to give feedback to the user.</span></span>


```C++
void MainWindow::SetMode(Mode m)
{
    mode = m;

    // Update the cursor
    LPWSTR cursor;
    switch (mode)
    {
    case DrawMode:
        cursor = IDC_CROSS;
        break;

    case SelectMode:
        cursor = IDC_HAND;
        break;

    case DragMode:
        cursor = IDC_SIZEALL;
        break;
    }

    hCursor = LoadCursor(NULL, cursor);
    SetCursor(hCursor);
}
```



<span data-ttu-id="fbb8f-173">E, finalmente, lembre-se de definir o cursor quando a janela receber uma mensagem do [**WM \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) :</span><span class="sxs-lookup"><span data-stu-id="fbb8f-173">And finally, remember to set the cursor when the window receives a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message:</span></span>


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



## <a name="summary"></a><span data-ttu-id="fbb8f-174">Resumo</span><span class="sxs-lookup"><span data-stu-id="fbb8f-174">Summary</span></span>

<span data-ttu-id="fbb8f-175">Neste módulo, você aprendeu a manipular a entrada do mouse e do teclado; como definir atalhos de teclado; e como atualizar a imagem do cursor para refletir o estado atual do programa.</span><span class="sxs-lookup"><span data-stu-id="fbb8f-175">In this module, you learned how to handle mouse and keyboard input; how to define keyboard shortcuts; and how to update the cursor image to reflect the current state of the program.</span></span>

 

 