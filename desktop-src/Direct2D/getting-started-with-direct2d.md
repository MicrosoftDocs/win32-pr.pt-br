---
title: Direct2D TUTORIAIS
description: resume as etapas necessárias para desenhar com Direct2D e fornece código de exemplo.
ms.assetid: 19d9ad76-b1e3-449f-8582-e00287b05874
keywords:
- Direct2D, exemplo de código de retângulo de desenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f9c4f7ee6ca99feb3cf7169a59ce73ff3b8f8c62c08ddad88b9e5acf5d9a814
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260057"
---
# <a name="direct2d-quickstart"></a>Direct2D TUTORIAIS

Direct2D é uma API de modo imediato, de código nativo para criar gráficos 2d. este tópico ilustra como usar Direct2D em um aplicativo Win32 típico para desenhar em um **HWND**.

> [!Note]  
> se você quiser criar um aplicativo de Windows Store que usa Direct2D, consulte o tópico guia de [início rápido do Direct2D para Windows 8](direct2d-quickstart-with-device-context.md) .

 

Este tópico contém as seguintes seções:

-   [Desenhando um retângulo simples](#drawing-a-simple-rectangle)
-   [etapa 1: incluir cabeçalho de Direct2D](#step-1-include-direct2d-header)
-   [Etapa 2: criar um ID2D1Factory](#step-2-create-an-id2d1factory)
-   [Etapa 3: criar um ID2D1HwndRenderTarget](#step-3-create-an-id2d1hwndrendertarget)
-   [Etapa 4: criar um pincel](#step-4-create-a-brush)
-   [Etapa 5: desenhar o retângulo](#step-5-draw-the-rectangle)
-   [Etapa 6: liberar recursos](#step-6-release-resources)
-   [criar um aplicativo Direct2D simples](#create-a-simple-direct2d-application)
-   [Tópicos relacionados](#related-topics)

## <a name="drawing-a-simple-rectangle"></a>Desenhando um retângulo simples

Para desenhar um retângulo usando [GDI](/windows/desktop/gdi/windows-gdi), você pode manipular a mensagem do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) , conforme mostrado no código a seguir.


```C++
switch(message)
{

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            BeginPaint(hwnd, &ps);

            // Obtain the size of the drawing area.
            RECT rc;
            GetClientRect(
                hwnd,
                &rc
            );          

            // Save the original object
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
            );

            // Create a pen.            
            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);

            // Select the pen.
            SelectObject(ps.hdc, blackPen);

            // Draw a rectangle.
            Rectangle(
                ps.hdc, 
                rc.left + 100, 
                rc.top + 100, 
                rc.right - 100, 
                rc.bottom - 100);   

            DeleteObject(blackPen);

            // Restore the original object
            SelectObject(ps.hdc, original);

            EndPaint(hwnd, &ps);
        }
        return 0;

// Code for handling other messages. 
```



o código para desenhar o mesmo retângulo com Direct2D é semelhante: ele cria recursos de desenho, descreve uma forma para desenhar, desenha a forma e libera os recursos de desenho. As seções a seguir descrevem cada uma dessas etapas em detalhes.

## <a name="step-1-include-direct2d-header"></a>etapa 1: incluir cabeçalho de Direct2D

Além dos cabeçalhos necessários para um aplicativo Win32, inclua o cabeçalho d2d1. h.

## <a name="step-2-create-an-id2d1factory"></a>Etapa 2: criar um ID2D1Factory

uma das primeiras coisas que qualquer Direct2D exemplo faz é criar um [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).


```C++
ID2D1Factory* pD2DFactory = NULL;
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_SINGLE_THREADED,
    &pD2DFactory
    );
```



A interface [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) é o ponto de partida para usar Direct2D; use um **ID2D1Factory** para criar Direct2D recursos.

Ao criar uma fábrica, você pode especificar se ela é de vários ou de thread único. (Para obter mais informações sobre fábricas com vários threads, consulte os comentários na [**página de referência do ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) Este exemplo cria uma fábrica de thread único.

Em geral, seu aplicativo deve criar a fábrica uma vez e mantê-la para a vida útil do aplicativo.

## <a name="step-3-create-an-id2d1hwndrendertarget"></a>Etapa 3: criar um ID2D1HwndRenderTarget

Depois de criar uma fábrica, use-a para criar um destino de renderização.


```C++


// Obtain the size of the drawing area.
RECT rc;
GetClientRect(hwnd, &rc);

// Create a Direct2D render target          
ID2D1HwndRenderTarget* pRT = NULL;          
HRESULT hr = pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(
        hwnd,
        D2D1::SizeU(
            rc.right - rc.left,
            rc.bottom - rc.top)
    ),
    &pRT
);
```



Um destino de renderização é um dispositivo que pode executar operações de desenho e criar recursos de desenho dependentes de dispositivo, como pincéis. Tipos diferentes de destinos de renderização renderizam para diferentes dispositivos. O exemplo anterior usa um [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), que é renderizado para uma parte da tela.

Quando possível, um destino de renderização usa a GPU para acelerar as operações de renderização e criar recursos de desenho. Caso contrário, o destino de renderização usa a CPU para processar instruções de renderização e criar recursos. (Você pode modificar esse comportamento usando os sinalizadores [**de \_ \_ \_ tipo de destino d2d1 render**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) ao criar o destino render.)

O método [**CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) usa três parâmetros. O primeiro parâmetro, uma estrutura de [**\_ Propriedades de \_ destino \_ de renderização d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) , especifica opções de exibição remotas, se deve forçar o destino de renderização a renderizar para software ou hardware e o DPI. O código neste exemplo usa a função auxiliar [**d2d1:: RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties) para aceitar Propriedades de destino de renderização padrão.

O segundo parâmetro, uma estrutura de [**\_ \_ \_ \_ Propriedades de destino de d2d1 HWND**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) , especifica o **HWND** para o qual o conteúdo é renderizado, o tamanho inicial do destino de renderização (em pixels) e suas [**Opções de apresentação**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_present_options). Este exemplo usa a função auxiliar [**d2d1:: HwndRenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties) para especificar um HWND e um tamanho inicial. Ele usa opções de apresentação padrão.

O terceiro parâmetro é o endereço do ponteiro que recebe a referência de destino de renderização.

Quando você cria um destino de renderização e a aceleração de hardware está disponível, você aloca recursos na GPU do computador. Ao criar um destino de renderização uma vez e mantê-lo o mais longo possível, você obterá benefícios de desempenho. Seu aplicativo deve criar destinos de renderização uma vez e mantê-los durante a vida útil do aplicativo ou até que o erro de [**\_ \_ destino de recriação de D2DERR**](direct2d-error-codes.md) seja recebido. Quando receber esse erro, você precisará recriar o destino de renderização (e todos os recursos que ele criou).

## <a name="step-4-create-a-brush"></a>Etapa 4: criar um pincel

Como uma fábrica, um destino de renderização pode criar recursos de desenho. Neste exemplo, o destino de renderização cria um pincel.


```C++
ID2D1SolidColorBrush* pBlackBrush = NULL;
if (SUCCEEDED(hr))
{
            
    pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        ); 
}
```



Um pincel é um objeto que pinta uma área, como o traço de uma forma ou o preenchimento de uma geometria. O pincel neste exemplo pinta uma área com uma cor sólida predefinida, preta.

Direct2D também fornece outros tipos de pincéis: pincéis de gradiente para pintar gradientes lineares e radiais e um pincel de bitmap para pintura com bitmaps e padrões.

Algumas APIs de desenho fornecem canetas para desenhar contornos e pincéis para preencher formas. Direct2D é diferente: ele não fornece um objeto pen, mas usa um pincel para desenhar contornos e preencher formas. Ao desenhar contornos, use a interface [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) com um pincel para controlar as operações de traçado de caminho.

Um pincel só pode ser usado com o destino de renderização que o criou e com outros destinos de renderização no mesmo domínio de recurso. Em geral, você deve criar pincéis uma vez e remantê-las para a vida útil do destino de renderização que as criou. [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) é a exceção solitário; Como é relativamente barato criar, você pode criar um **ID2D1SolidColorBrush** toda vez que desenhar um quadro, sem qualquer impacto perceptível no desempenho. Você também pode usar um único **ID2D1SolidColorBrush** e apenas alterar sua cor toda vez que usá-lo.

## <a name="step-5-draw-the-rectangle"></a>Etapa 5: desenhar o retângulo

Em seguida, use o destino de renderização para desenhar o retângulo.


```C++
 
pRT->BeginDraw();

pRT->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

HRESULT hr = pRT->EndDraw();  
```



O método [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) usa dois parâmetros: o retângulo a ser desenhado e o pincel a ser usado para pintar o contorno do retângulo. Opcionalmente, você também pode especificar as opções largura do traço, padrão de tracejado, junção de linha e extremidade de fim.

Você deve chamar o método [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) antes de emitir qualquer comando de desenho, e deve chamar o método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) depois de concluir a emissão de comandos de desenho. O método **EndDraw** retorna um **HRESULT** que indica se os comandos de desenho foram bem-sucedidos.

## <a name="step-6-release-resources"></a>Etapa 6: liberar recursos

Quando não houver mais quadros para desenhar, ou quando você receber o erro [**de \_ \_ destino de recriação de D2DERR**](direct2d-error-codes.md) , libere o destino de renderização e todos os dispositivos que ele criou.


```C++
 
SafeRelease(pRT);
SafeRelease(pBlackBrush);
```



quando o aplicativo tiver terminado de usar Direct2D recursos (como quando está prestes a sair), libere a fábrica de Direct2D.


```C++
 
SafeRelease(pD2DFactory);
```



## <a name="create-a-simple-direct2d-application"></a>criar um aplicativo Direct2D simples

o código neste tópico mostra os elementos básicos de um aplicativo Direct2D. Para resumir, o tópico omite a estrutura do aplicativo e o código de tratamento de erros que é característica de um aplicativo bem escrito. para obter um passo a passo mais detalhado que mostra o código completo para criar um aplicativo Direct2D simples e demonstra as melhores práticas de design, consulte [criando um aplicativo simples de Direct2D](direct2d-quickstart.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[criando um aplicativo simples de Direct2D](direct2d-quickstart.md)
</dt> </dl>

 

 