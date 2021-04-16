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
# <a name="user-input-extended-example"></a>Entrada do usuário: exemplo estendido

Vamos combinar tudo o que aprendemos sobre a entrada do usuário para criar um programa simples de desenho. Aqui está uma captura de tela do programa:

![captura de tela do programa de desenho](images/input03.png)

O usuário pode desenhar reticências em várias cores diferentes e selecionar, mover ou excluir reticências. Para manter a interface do usuário simples, o programa não permite que o usuário selecione as cores da elipse. Em vez disso, o programa percorre automaticamente uma lista predefinida de cores. O programa não oferece suporte a formas diferentes de elipses. Obviamente, esse programa não ganhará nenhum prêmio de software de gráficos. No entanto, ele ainda é um exemplo útil para aprender com o. Você pode baixar o código-fonte completo do [exemplo de desenho simples](simple-drawing-sample.md). Esta seção abordará apenas alguns destaques.

As elipses são representadas no programa por uma estrutura que contém os dados da elipse ([**\_ elipse d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) e a cor ([**d2d1 \_ cor \_ F**](/windows/desktop/Direct2D/d2d1-color-f)). A estrutura também define dois métodos: um método para desenhar a elipse e um método para executar testes de clique.


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



O programa usa o mesmo pincel de cor sólida para desenhar o preenchimento e a estrutura de tópicos para cada elipse, alterando a cor conforme necessário. No Direct2D, a alteração da cor de um pincel de cor sólida é uma operação eficiente. Portanto, o objeto de pincel de cor sólida dá suporte a um método [**setColor**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) .

As reticências são armazenadas em um contêiner de **lista** STL:


```C++
    list<shared_ptr<MyEllipse>>             ellipses;
```



> [!Note]  
> **o \_ PTR compartilhado** é uma classe de ponteiro inteligente que foi adicionada ao C++ no TR1 e formalizada em C + + 0x. O Visual Studio 2010 adiciona suporte para r **\_ pt compartilhado** e outros recursos do C + + 0x. Para obter mais informações, consulte [explorando novos recursos de C++ e MFC no Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) na *msdn Magazine*. (Esse recurso pode não estar disponível em alguns idiomas e países.)

 

O programa tem três modos:

-   Modo de desenho. O usuário pode desenhar novas elipses.
-   Modo de seleção. O usuário pode selecionar uma elipse.
-   Modo de arrastar. O usuário pode arrastar uma elipse selecionada.

O usuário pode alternar entre o modo de desenho e o modo de seleção usando os mesmos atalhos de teclado descritos em [tabelas de aceleração](accelerator-tables.md). No modo de seleção, o programa alternará para o modo de arrastar se o usuário clicar em uma elipse. Ele volta para o modo de seleção quando o usuário libera o botão do mouse. A seleção atual é armazenada como um iterador na lista de reticências. O método auxiliar `MainWindow::Selection` retorna um ponteiro para a elipse selecionada ou o valor **nullptr** se não houver nenhuma seleção.


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



A tabela a seguir resume os efeitos da entrada do mouse em cada um dos três modos.



| Entrada do mouse      | Modo de Desenho                                          | Modo de seleção                                                                                                                               | Modo de arrastar                  |
|------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| Botão esquerdo para baixo | Defina a captura do mouse e comece a desenhar uma nova elipse. | Libere a seleção atual e execute um teste de clique. Se uma elipse for atingida, Capture o cursor, selecione a elipse e alterne para o modo de arrastar. | Nenhuma ação.                 |
| Movimentação do mouse       | Se o botão esquerdo estiver inativo, redimensione a elipse.    | Nenhuma ação.                                                                                                                                   | Mova a elipse selecionada. |
| Botão esquerdo para cima   | Pare de desenhar a elipse.                          | Nenhuma ação.                                                                                                                                   | Alternar para o modo de seleção.  |



 

O método a seguir na `MainWindow` classe trata as mensagens do [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) .


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



As coordenadas do mouse são passadas para esse método em pixels e, em seguida, convertidas em DIPs. É importante não confundir essas duas unidades. Por exemplo, a função [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) usa pixels, mas os testes de desenho e de clique em uso ficam DIPs. A regra geral é que as funções relacionadas à entrada do Windows ou do mouse usam pixels, enquanto Direct2D e DirectWrite usam DIPs. Sempre teste seu programa em uma configuração de alto DPI e lembre-se de marcar seu programa como com reconhecimento de DPI. Para obter mais informações, consulte [dpi e Device-Independent pixels](dpi-and-device-independent-pixels.md).

Este é o código que manipula as mensagens [**\_ MOUSEMOVE do WM**](/windows/desktop/inputdev/wm-mousemove) .


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



A lógica para redimensionar uma elipse foi descrita anteriormente, na seção [exemplo: círculos de desenho](mouse-movement.md). Observe também a chamada para [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect). Isso garante que a janela seja repintada. O código a seguir manipula mensagens do [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) .


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



Como você pode ver, os manipuladores de mensagens para entrada do mouse têm código de ramificação, dependendo do modo atual. Esse é um design aceitável para esse programa bastante simples. No entanto, ele pode rapidamente se tornar muito complexo se novos modos forem adicionados. Para um programa maior, uma arquitetura MVC (Model-View-Controller) pode ser um design melhor. Nesse tipo de arquitetura, o *controlador*, que manipula a entrada do usuário, é separado do *modelo*, que gerencia os dados do aplicativo.

Quando o programa muda de modos, o cursor é alterado para fornecer comentários ao usuário.


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



E, finalmente, lembre-se de definir o cursor quando a janela receber uma mensagem do [**WM \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) :


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



## <a name="summary"></a>Resumo

Neste módulo, você aprendeu a manipular a entrada do mouse e do teclado; como definir atalhos de teclado; e como atualizar a imagem do cursor para refletir o estado atual do programa.

 

 