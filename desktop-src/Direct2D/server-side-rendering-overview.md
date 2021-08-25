---
title: Usando Direct2D para Server-Side Rendering
description: Descreve o uso de Direct2D para renderização do lado do servidor.
ms.assetid: 12bf4f14-d86f-40ff-b3d3-15ffb3bd7300
keywords:
- Direct2D, renderização do lado do servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65991d2437939ce7f1d218022e0c3c57649405a18e2c1b9d073635b5b37d1a2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917187"
---
# <a name="using-direct2d-for-server-side-rendering"></a>Usando Direct2D para Server-Side Rendering

Direct2D é adequado para aplicativos gráficos que exigem renderização do lado do servidor no Windows Server. Esta visão geral descreve as noções básicas do uso Direct2D para renderização do lado do servidor. Ele contém as seções a seguir:

-   [Requisitos para Server-Side Rendering](#requirements-for-server-side-rendering)
-   [Opções para APIs disponíveis](#options-for-available-apis)
    -   [Gdi](#gdi)
    -   [GDI+](#gdi)
    -   [Direct2D](#using-direct2d-for-server-side-rendering)
-   [Como usar o Direct2D para Server-Side Rendering](#how-to-use-direct2d-for-server-side-rendering)
    -   [Renderização de software](#software-rendering)
    -   [Multithread](#multithreading)
    -   [Gerando um arquivo bitmap](#generating-a-bitmap-file)
-   [Conclusão](#conclusion)
-   [Tópicos relacionados](#related-topics)

## <a name="requirements-for-server-side-rendering"></a>Requisitos para Server-Side Rendering

Veja a seguir um cenário típico para um servidor de gráficos: gráficos e gráficos são renderizados em um servidor e entregues como bitmaps em resposta a solicitações da Web. O servidor pode estar equipado com uma placa gráfica de baixo nível ou nenhuma placa gráfica.

Esse cenário revela três requisitos de aplicativo. Primeiro, o aplicativo deve lidar com várias solicitações simultâneas com eficiência, especialmente em servidores multicore. Em segundo lugar, o aplicativo deve usar a renderização de software ao executar em servidores com uma placa gráfica de baixo nível ou nenhuma placa gráfica. Por fim, o aplicativo deve ser executado como um serviço na Sessão 0 para que ele não exige que um usuário seja conectado. Para obter mais informações sobre a Sessão 0, consulte Impacto do isolamento da sessão [0](https://www.microsoft.com/whdc/system/sysinternals/Session0Changes.mspx)em serviços e drivers no Windows .

## <a name="options-for-available-apis"></a>Opções para APIs disponíveis

Há três opções para renderização do lado do servidor: GDI, GDI+ e Direct2D. Assim como GDI e GDI+, Direct2D é uma API de renderização 2D nativa que dá aos aplicativos mais controle sobre o uso de dispositivos gráficos. Além disso, Direct2D dá suporte exclusivamente a uma fábrica de thread único e multithread. As seções a seguir comparam cada API em termos de qualidade de desenho e renderização multithread do lado do servidor.

### <a name="gdi"></a>GDI

Ao Direct2D e GDI+, o GDI não dá suporte a recursos de desenho de alta qualidade. Por exemplo, a GDI não dá suporte à suavização para criar linhas suaves e tem apenas suporte limitado para transparência. Com base nos resultados do teste de desempenho de gráficos no Windows 7 e no Windows Server 2008 R2, o Direct2D é dimensionado com mais eficiência do que a GDI, apesar da reformulação de bloqueios na GDI. Para obter mais informações sobre esses resultados de teste, consulte [Desempenho gráfico Windows 7 .](/archive/blogs/e7/engineering-windows-7-graphics-performance)

Além disso, os aplicativos que usam GDI são limitados a 10.240 alças GDI por processo e 65536 alças GDI por sessão. O motivo é que, Windows usa um WORD de 16 bits para armazenar o índice de alças para cada sessão.

### <a name="gdi"></a>GDI+

Embora GDI+ seja compatível com antialiasing e combinação alfa para desenho de alta qualidade, o principal problema com o GDI+ para cenários de servidor é que ele não dá suporte à execução na Sessão 0. Como a Sessão 0 dá suporte apenas a funcionalidades não interativas, as funções que interagem direta ou indiretamente com dispositivos de exibição receberão erros. Exemplos específicos de funções incluem não apenas aqueles que lidam com dispositivos de exibição, mas também aqueles que lidam indiretamente com drivers de dispositivo.

Semelhante à GDI, GDI+ é limitado por seu mecanismo de bloqueio. Os mecanismos de bloqueio no GDI+ são os mesmos no Windows 7 e Windows Server 2008 R2 como nas versões anteriores.

### <a name="direct2d"></a>Direct2D

Direct2D é uma API de gráficos 2D acelerada por hardware e modo imediato que fornece renderização de alto desempenho e alta qualidade. Ele oferece uma fábrica de thread único e multithread e o dimensionamento linear da renderização de software com curso.

Para fazer isso, Direct2D define uma interface de fábrica raiz. Como regra, um objeto criado em uma fábrica só pode ser usado com outros objetos criados na mesma fábrica. O chamador pode solicitar um fábrica de thread único ou multithread quando ele é criado. Se uma fábrica de thread único for solicitada, nenhum bloqueio de threads será executado. Se o chamador solicitar uma fábrica multithreaded, um bloqueio de thread de toda a fábrica será adquirido sempre que uma chamada for feita em Direct2D.

Além disso, o bloqueio de threads no Direct2D é mais granular do que no GDI e GDI+, de modo que o aumento do número de threads tenha impacto mínimo sobre o desempenho.

## <a name="how-to-use-direct2d-for-server-side-rendering"></a>Como usar o Direct2D para Server-Side Rendering

As seções a seguir descrevem como usar a renderização de software, como usar idealmente uma fábrica de thread único e multithread e como desenhar e salvar um desenho complexo em um arquivo.

### <a name="software-rendering"></a>Renderização de software

Os aplicativos do lado do servidor usam a renderização de software criando o destino de renderização [IWICBitmap,](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) com o tipo de destino de renderização definido como D2D1 RENDER TARGET TYPE SOFTWARE ou \_ \_ \_ \_ D2D1 \_ RENDER TARGET TYPE \_ \_ \_ DEFAULT. Para obter mais informações sobre destinos de renderização [IWICBitmap,](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) consulte o [**método ID2D1Factory::CreateWicBitmapRenderTarget;**](id2d1factory-createwicbitmaprendertarget.md) Para obter mais informações sobre os tipos de destino de renderização, [**consulte D2D1 \_ RENDER TARGET \_ \_ TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type).

### <a name="multithreading"></a>Multithreading

Saber como criar e compartilhar fábricas e renderizar destinos entre threads pode afetar significativamente o desempenho de um aplicativo. As três figuras a seguir mostram três abordagens variadas. A abordagem ideal é mostrada na figura 3.

![diagrama de multithreading direct2d com um único destino de renderização.](images/server-side-rendering-1.png)

Na figura 1, threads diferentes compartilham a mesma fábrica e o mesmo destino de renderização. Essa abordagem pode levar a resultados imprevisíveis em casos em que vários threads alteram simultaneamente o estado do destino de renderização compartilhado, como configurar simultaneamente a matriz de transformação. Como o bloqueio interno no Direct2D não sincroniza um recurso compartilhado, como destinos de renderização, essa abordagem pode fazer com que a chamada [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) falhe no thread 1, pois, no thread 2, a **chamada BeginDraw** já está usando o destino de renderização compartilhado.

![diagrama de multithreading direct2d com vários destinos de renderização.](images/server-side-rendering-2.png)

Para evitar os resultados imprevisíveis encontrados na Figura 1, a Figura 2 mostra uma fábrica multithread com cada thread com seu próprio destino de renderização. Essa abordagem funciona, mas funciona efetivamente como um aplicativo de thread único. O motivo é que o bloqueio em toda a fábrica se aplica somente ao nível da operação de desenho e, consequentemente, todas as chamadas de desenho na mesma fábrica são serializadas. Como resultado, o thread 1 é bloqueado ao tentar inserir uma chamada de desenho, enquanto o thread 2 está no meio da execução de outra chamada de desenho.

![Diagrama de multithreading direct2d com várias fábricas e vários destinos de renderização.](images/server-side-rendering-3.png)

A Figura 3 mostra a abordagem ideal, em que uma fábrica de thread único e um destino de renderização de thread único são usados. Como nenhum bloqueio é executado ao usar uma fábrica de thread único, as operações de desenho em cada thread podem ser executadas simultaneamente para obter o desempenho ideal.

### <a name="generating-a-bitmap-file"></a>Gerando um arquivo bitmap

Para gerar um arquivo bitmap usando a renderização de software, use um destino de renderização [IWICBitmap.](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) Use um [IWICStream](/windows/win32/api/wincodec/nn-wincodec-iwicstream) para gravar o bitmap em um arquivo. Use [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) para codificar o bitmap em um formato de imagem especificado. O exemplo de código a seguir mostra como desenhar e salvar a imagem a seguir em um arquivo.

![imagem de saída de exemplo.](images/saveasimagefile-sample.png)

Este exemplo de código primeiro cria [um IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) e um [destino de renderização IWICBitmap.](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) Em seguida, ele renderiza um desenho com algum texto, uma geometria de caminho que representa um vidro de hora e um vidro de hora transformado em um bitmap WIC. Em seguida, [ele usa IWICStream::InitializeFromFilename](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefromfilename) para salvar o bitmap em um arquivo. Se o aplicativo precisar salvar o bitmap na memória, use [IWICStream::InitializeFromMemory.](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefrommemory) Por fim, ele usa [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) para codificar o bitmap.


```C++
// Create an IWICBitmap and RT
static const UINT sc_bitmapWidth = 640;
static const UINT sc_bitmapHeight = 480;
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateBitmap(
        sc_bitmapWidth,
        sc_bitmapHeight,
        GUID_WICPixelFormat32bppBGR,
        WICBitmapCacheOnLoad,
        &pWICBitmap
        );
}

// Set the render target type to D2D1_RENDER_TARGET_TYPE_DEFAULT to use software rendering.
if (SUCCEEDED(hr))
{
    hr = pD2DFactory->CreateWicBitmapRenderTarget(
        pWICBitmap,
        D2D1::RenderTargetProperties(),
        &pRT
        );
}

// Create text format and a path geometry representing an hour glass. 
if (SUCCEEDED(hr))
{
    static const WCHAR sc_fontName[] = L"Calibri";
    static const FLOAT sc_fontSize = 50;

    hr = pDWriteFactory->CreateTextFormat(
        sc_fontName,
        NULL,
        DWRITE_FONT_WEIGHT_NORMAL,
        DWRITE_FONT_STYLE_NORMAL,
        DWRITE_FONT_STRETCH_NORMAL,
        sc_fontSize,
        L"", //locale
        &pTextFormat
        );
}
if (SUCCEEDED(hr))
{
    pTextFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    pTextFormat->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    hr = pD2DFactory->CreatePathGeometry(&pPathGeometry);
}
if (SUCCEEDED(hr))
{
    hr = pPathGeometry->Open(&pSink);
}
if (SUCCEEDED(hr))
{
    pSink->SetFillMode(D2D1_FILL_MODE_ALTERNATE);

    pSink->BeginFigure(
        D2D1::Point2F(0, 0),
        D2D1_FIGURE_BEGIN_FILLED
        );

    pSink->AddLine(D2D1::Point2F(200, 0));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(150, 50),
            D2D1::Point2F(150, 150),
            D2D1::Point2F(200, 200))
        );

    pSink->AddLine(D2D1::Point2F(0, 200));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(50, 150),
            D2D1::Point2F(50, 50),
            D2D1::Point2F(0, 0))
        );

    pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

    hr = pSink->Close();
}
if (SUCCEEDED(hr))
{
    static const D2D1_GRADIENT_STOP stops[] =
    {
        {   0.f,  { 0.f, 1.f, 1.f, 1.f }  },
        {   1.f,  { 0.f, 0.f, 1.f, 1.f }  },
    };

    hr = pRT->CreateGradientStopCollection(
        stops,
        ARRAYSIZE(stops),
        &pGradientStops
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(100, 0),
            D2D1::Point2F(100, 200)),
        D2D1::BrushProperties(),
        pGradientStops,
        &pLGBrush
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        );
}
if (SUCCEEDED(hr))
{
    // Render into the bitmap.
    pRT->BeginDraw();
    pRT->Clear(D2D1::ColorF(D2D1::ColorF::White));
    D2D1_SIZE_F rtSize = pRT->GetSize();

    // Set the world transform to a 45 degree rotation at the center of the render target
    // and write "Hello, World".
    pRT->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45,
            D2D1::Point2F(
                rtSize.width / 2,
                rtSize.height / 2))
            );

    static const WCHAR sc_helloWorld[] = L"Hello, World!";
    pRT->DrawText(
        sc_helloWorld,
        ARRAYSIZE(sc_helloWorld) - 1,
        pTextFormat,
        D2D1::RectF(0, 0, rtSize.width, rtSize.height),
        pBlackBrush);

    // Reset back to the identity transform.
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(0, rtSize.height - 200));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(rtSize.width - 200, 0));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    hr = pRT->EndDraw();
}

if (SUCCEEDED(hr))
{
    // Save the image to a file.
    hr = pWICFactory->CreateStream(&pStream);
}

WICPixelFormatGUID format = GUID_WICPixelFormatDontCare;

// Use InitializeFromFilename to write to a file. If there is need to write inside the memory, use InitializeFromMemory. 
if (SUCCEEDED(hr))
{
    static const WCHAR filename[] = L"output.png";
    hr = pStream->InitializeFromFilename(filename, GENERIC_WRITE);
}
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateEncoder(GUID_ContainerFormatPng, NULL, &pEncoder);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Initialize(pStream, WICBitmapEncoderNoCache);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->CreateNewFrame(&pFrameEncode, NULL);
}
// Use IWICBitmapFrameEncode to encode the bitmap into the picture format you want.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Initialize(NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetSize(sc_bitmapWidth, sc_bitmapHeight);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetPixelFormat(&format);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->WriteSource(pWICBitmap, NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Commit();
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Commit();
}

```



## <a name="conclusion"></a>Conclusão

Como visto acima, o uso de Direct2D para renderização do lado do servidor é simples e simples. Além disso, ele fornece renderização altamente paralelizável e de alta qualidade que pode ser executado em ambientes de baixo privilégio do servidor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Direct2D Referência](reference.md)
</dt> </dl>

 

 