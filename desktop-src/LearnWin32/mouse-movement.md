---
title: Movimento do mouse
description: Movimento do mouse
ms.assetid: 54366E9B-470A-4155-8A5F-425BAC8AC1A5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14176310882651cdeb2939d0db55368ff133ea11
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "105810479"
---
# <a name="mouse-movement"></a>Movimento do mouse

Quando o mouse se move, o Windows posta uma mensagem [**\_ MOUSEMOVE do WM**](/windows/desktop/inputdev/wm-mousemove) . Por padrão, o **WM \_ MOUSEMOVE** vai para a janela que contém o cursor. Você pode substituir esse comportamento *capturando* o mouse, que é descrito na próxima seção.

A [**mensagem \_ MOUSEMOVE do WM**](/windows/desktop/inputdev/wm-mousemove) contém os mesmos parâmetros que as mensagens para cliques do mouse. Os 16 bits mais baixos de *lParam* contêm a coordenada x e os próximos 16 bits contêm a coordenada y. Use as macros [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**Get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para desempacotar as coordenadas do *lParam*. O parâmetro *wParam* contém um **ou** mais bits de sinalizadores, indicando o estado dos outros botões do mouse mais as teclas Shift e Ctrl. O código a seguir obtém as coordenadas do mouse do *lParam*.


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



Lembre-se de que essas coordenadas estão em pixels, não em DIPs (pixels independentes de dispositivo). Posteriormente neste tópico, veremos o código que converte entre as duas unidades.

Uma janela também pode receber uma mensagem do [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) se a posição do cursor mudar em relação à janela. Por exemplo, se o cursor estiver posicionado sobre uma janela e o usuário ocultar a janela, a janela receberá mensagens do **WM \_ MOUSEMOVE** , mesmo que o mouse não tenha se movido. Uma consequência desse comportamento é que as coordenadas do mouse podem não mudar entre as mensagens **\_ MOUSEMOVE do WM** .

## <a name="capturing-mouse-movement-outside-the-window"></a>Captura do movimento do mouse fora da janela

Por padrão, uma janela para de receber mensagens do [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) se o mouse passar para a borda da área do cliente. Mas, para algumas operações, talvez seja necessário controlar a posição do mouse além desse ponto. Por exemplo, um programa de desenho pode permitir que o usuário arraste o retângulo de seleção para além da borda da janela, conforme mostrado no diagrama a seguir.

![uma ilustração de captura do mouse.](images/input01.png)

Para receber mensagens de movimentação do mouse após a borda da janela, chame a função [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) . Depois que essa função for chamada, a janela continuará a receber mensagens do [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) enquanto o usuário mantiver pelo menos um botão do mouse pressionado, mesmo se o mouse se mover para fora da janela. A janela de captura deve ser a janela em primeiro plano e apenas uma janela pode ser a janela de captura por vez. Para liberar a captura do mouse, chame a função [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) .

Normalmente, você usaria [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) e [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) da seguinte maneira.

1.  Quando o usuário pressiona o botão esquerdo do mouse, chame [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) para começar a capturar o mouse.
2.  Responder às mensagens do mouse-mover.
3.  Quando o usuário libera o botão esquerdo do mouse, chame [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture).

## <a name="example-drawing-circles"></a>Exemplo: círculos de desenho

Vamos estender o programa de círculo do [módulo 3](module-3---windows-graphics.md) habilitando o usuário a desenhar um círculo com o mouse. Comece com o programa de [exemplo de círculo Direct2D](direct2d-circle-sample.md) . Modificaremos o código neste exemplo para adicionar desenho simples. Primeiro, adicione uma nova variável de membro à `MainWindow` classe.


```C++
    D2D1_POINT_2F           ptMouse;
```



Essa variável armazena a posição do mouse para baixo enquanto o usuário está arrastando o mouse. No `MainWindow` Construtor, inicialize as variáveis *Ellipse* e *ptMouse* .


```C++
    MainWindow() : pFactory(NULL), pRenderTarget(NULL), pBrush(NULL),
        ellipse(D2D1::Ellipse(D2D1::Point2F(), 0, 0)),
        ptMouse(D2D1::Point2F())
    {
    }
```



Remova o corpo do `MainWindow::CalculateLayout` método; ele não é necessário para este exemplo.


```C++
    void    CalculateLayout() { }
```



Em seguida, declare os manipuladores de mensagens para o botão esquerdo inferior, o botão esquerdo para cima e as mensagens de movimentação do mouse.


```C++
    void    OnLButtonDown(int pixelX, int pixelY, DWORD flags);
    void    OnLButtonUp();
    void    OnMouseMove(int pixelX, int pixelY, DWORD flags);
```



As coordenadas do mouse são dadas em pixels físicos, mas o Direct2D espera pixels independentes de dispositivo (DIPs). Para tratar as configurações de alto DPI corretamente, você deve converter as coordenadas de pixel em DIPs. Para obter mais discussões sobre DPI, consulte [dpi e Device-Independent pixels](dpi-and-device-independent-pixels.md). O código a seguir mostra uma classe auxiliar que converte pixels em DIPs.


```C++
class DPIScale
{
    static float scaleX;
    static float scaleY;

public:
    static void Initialize(ID2D1Factory *pFactory)
    {
        FLOAT dpiX, dpiY;
        pFactory->GetDesktopDpi(&dpiX, &dpiY);
        scaleX = dpiX/96.0f;
        scaleY = dpiY/96.0f;
    }

    template <typename T>
    static D2D1_POINT_2F PixelsToDips(T x, T y)
    {
        return D2D1::Point2F(static_cast<float>(x) / scaleX, static_cast<float>(y) / scaleY);
    }
};

float DPIScale::scaleX = 1.0f;
float DPIScale::scaleY = 1.0f;
```



Chame `DPIScale::Initialize` em seu manipulador de [**\_ criação do WM**](/windows/desktop/winmsg/wm-create) , depois de criar o objeto de fábrica Direct2D.


```C++
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        DPIScale::Initialize(pFactory);
        return 0;
```



Para obter as coordenadas do mouse em DIPs das mensagens do mouse, faça o seguinte:

1.  Use as macros [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**Get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para obter as coordenadas de pixel. Essas macros são definidas em WindowsX. h, portanto, lembre-se de incluir esse cabeçalho em seu projeto.
2.  Chame `DPIScale::PixelsToDipsX` e `DPIScale::PixelsToDipsY` para converter pixels em DIPs.

Agora, adicione os manipuladores de mensagens ao seu procedimento de janela.


```C++
    case WM_LBUTTONDOWN: 
        OnLButtonDown(GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), (DWORD)wParam);
        return 0;

    case WM_LBUTTONUP: 
        OnLButtonUp();
        return 0;

    case WM_MOUSEMOVE: 
        OnMouseMove(GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), (DWORD)wParam);
        return 0;
```



Por fim, implemente os próprios manipuladores de mensagens.

### <a name="left-button-down"></a>Botão esquerdo para baixo

Para a mensagem de botão esquerdo para baixo, faça o seguinte:

1.  Chame [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) para começar a capturar o mouse.
2.  Armazene a posição do clique do mouse na variável *ptMouse* . Essa posição define o canto superior esquerdo da caixa delimitadora para a elipse.
3.  Redefina a estrutura da elipse.
4.  Chame [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect). Essa função força a janela a ser redesenhada.


```C++
void MainWindow::OnLButtonDown(int pixelX, int pixelY, DWORD flags)
{
    SetCapture(m_hwnd);
    ellipse.point = ptMouse = DPIScale::PixelsToDips(pixelX, pixelY);
    ellipse.radiusX = ellipse.radiusY = 1.0f; 
    InvalidateRect(m_hwnd, NULL, FALSE);
}
```



### <a name="mouse-move"></a>Movimentação do mouse

Para a mensagem mouse-move, verifique se o botão esquerdo do mouse está inoperante. Se for, recalcule a elipse e repinte a janela. No Direct2D, uma elipse é definida pelo ponto central e raios x e y. Desejamos desenhar uma elipse que se ajuste à caixa delimitadora definida pelo ponto do mouse (*ptMouse*) e da posição atual do cursor (*x*, *y*), de modo que um pouco de aritmética seja necessário para localizar a largura, a altura e a posição da elipse.

O código a seguir recalcula a elipse e, em seguida, chama [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) para redesenhar a janela.

![Diagrama que mostra uma elipse com raio x e y.](images/input02.png)


```C++
void MainWindow::OnMouseMove(int pixelX, int pixelY, DWORD flags)
{
    if (flags & MK_LBUTTON) 
    { 
        const D2D1_POINT_2F dips = DPIScale::PixelsToDips(pixelX, pixelY);

        const float width = (dips.x - ptMouse.x) / 2;
        const float height = (dips.y - ptMouse.y) / 2;
        const float x1 = ptMouse.x + width;
        const float y1 = ptMouse.y + height;

        ellipse = D2D1::Ellipse(D2D1::Point2F(x1, y1), width, height);

        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



### <a name="left-button-up"></a>Botão esquerdo para cima

Para a mensagem de botão esquerdo, basta chamar [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) para liberar a captura do mouse.


```C++
void MainWindow::OnLButtonUp()
{
    ReleaseCapture(); 
}
```



## <a name="next"></a>Avançar

[Outras operações do mouse](other-mouse-operations.md)

 

 