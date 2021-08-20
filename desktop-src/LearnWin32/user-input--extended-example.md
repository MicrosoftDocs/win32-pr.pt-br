---
title: User Input Extended Example description: User Input: Extended Example ms.assetid: A408E0EC-E0A7-4F18-BFCA-21D28007FACC ms.topic: article ms.date: 31/05/2018
---

# <a name="user-input-extended-example"></a>Entrada do usuário: exemplo estendido

Vamos combinar tudo o que aprendemos sobre a entrada do usuário para criar um programa de desenho simples. Aqui está uma captura de tela do programa:

![captura de tela do programa de desenho](images/input03.png)

O usuário pode desenhar re elipses em várias cores diferentes e selecionar, mover ou excluir reellipses. Para manter a interface do usuário simples, o programa não permite que o usuário selecione as cores da elipse. Em vez disso, o programa passa automaticamente por uma lista predefinida de cores. O programa não dá suporte a nenhuma forma diferente de reellipses. Obviamente, esse programa não receberá nenhum prêmio para software gráfico. No entanto, ainda é um exemplo útil para aprender. Você pode baixar o código-fonte completo do [Exemplo de Desenho Simples.](simple-drawing-sample.md) Esta seção abrange apenas alguns destaques.

As re elipses são representadas no programa por uma estrutura que contém os dados de elipse ([**D2D1 \_ ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) e a cor ([**D2D1 \_ COLOR \_ F**](/windows/desktop/Direct2D/d2d1-color-f)). A estrutura também define dois métodos: um método para desenhar a elipse e um método para executar testes de acerto.


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



O programa usa o mesmo pincel de cor sólida para desenhar o preenchimento e o contorno de cada elipse, alterando a cor conforme necessário. No Direct2D, alterar a cor de um pincel de cor sólida é uma operação eficiente. Portanto, o objeto de pincel de cor sólida dá suporte a [**um método SetColor.**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor)

As reellipses são armazenadas em um contêiner de lista **STL:**


```C++
    list<shared_ptr<MyEllipse>>             ellipses;
```



> [!Note]  
> **shared \_ ptr** é uma classe de ponteiro inteligente que foi adicionada ao C++ em TR1 e formalizada em C++0x. Visual Studio 2010 adiciona suporte para **\_ pt** r compartilhado e outros recursos do C++0x. Para obter mais informações, consulte [Explorando novos recursos do C++ e do MFC no Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) na *MSDN Magazine.* (Esse recurso pode não estar disponível em alguns idiomas e países.)

 

O programa tem três modos:

-   Modo de desenho. O usuário pode desenhar novas reellipses.
-   Modo de seleção. O usuário pode selecionar uma elipse.
-   Modo de arrastar. O usuário pode arrastar uma elipse selecionada.

O usuário pode alternar entre o modo de desenho e o modo de seleção usando os mesmos atalhos de teclado descritos em [Tabelas de Acelerador.](accelerator-tables.md) No modo de seleção, o programa alterna para o modo de arrastar se o usuário clicar em uma elipse. Ele alterna de volta para o modo de seleção quando o usuário libera o botão do mouse. A seleção atual é armazenada como um iterador na lista de reellipses. O método auxiliar retornará um ponteiro para a elipse selecionada ou o `MainWindow::Selection` valor **nullptr** se não houver nenhuma seleção.


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
| Botão esquerdo para baixo | De configurar a captura do mouse e começar a desenhar uma nova elipse. | Libere a seleção atual e execute um teste de acerto. Se uma elipse for atingida, capture o cursor, selecione a elipse e alternar para o modo de arrastar. | Nenhuma ação.                 |
| Movimentação do mouse       | Se o botão esquerdo estiver inoossado, resize a elipse.    | Nenhuma ação.                                                                                                                                   | Mova a elipse selecionada. |
| Botão esquerdo para cima   | Pare de desenhar a elipse.                          | Nenhuma ação.                                                                                                                                   | Alternar para o modo de seleção.  |



 

O método a seguir na `MainWindow` classe lida com mensagens WM [**\_ LBUTTONDOWN.**](/windows/desktop/inputdev/wm-lbuttondown)


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



As coordenadas do mouse são passadas para esse método em pixels e convertidas em DIPs. É importante não confundir essas duas unidades. Por exemplo, a [**função DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) usa pixels, mas o desenho e o teste de acerto usam DIPs. A regra geral é que as funções relacionadas às janelas ou à entrada do mouse usam pixels, enquanto Direct2D e DirectWrite usam DIPs. Sempre teste seu programa em uma configuração de alto DPI e lembre-se de marcar seu programa como com conhecimento de DPI. Para obter mais informações, [consulte DPI e Device-Independent Pixels](dpi-and-device-independent-pixels.md).

Este é o código que lida com [**mensagens WM \_ MOUSEMOVE.**](/windows/desktop/inputdev/wm-mousemove)


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



A lógica para reenviar uma elipse foi descrita anteriormente, na seção [Exemplo: Desenhando círculos.](mouse-movement.md) Observe também a chamada para [**InvalidateRect.**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) Isso garante que a janela seja repintada. O código a seguir lida com [**mensagens \_ WM LBUTTONUP.**](/windows/desktop/inputdev/wm-lbuttonup)


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



Como você pode ver, os manipuladores de mensagens para entrada do mouse têm código de ramificação, dependendo do modo atual. Esse é um design aceitável para esse programa bastante simples. No entanto, isso poderá se tornar muito complexo rapidamente se novos modos são adicionados. Para um programa maior, uma arquitetura MVC (model-view-controller) pode ser um design melhor. Nesse tipo de arquitetura, o *controlador*, que lida com a entrada do usuário, é separado do *modelo*, que gerencia os dados do aplicativo.

Quando o programa alterna os modos, o cursor muda para dar comentários ao usuário.


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



E, por fim, lembre-se de definir o cursor quando a janela receber uma [**mensagem WM \_ SETCURSOR:**](/windows/desktop/menurc/wm-setcursor)


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

 

 
