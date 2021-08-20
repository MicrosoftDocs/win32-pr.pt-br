---
title: DirectWrite de renderização
description: DirectWrite de renderização
ms.assetid: e8099fac-b5d7-4fb1-b06d-a6e85da0d1dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa640b8963c427b9eaf1d17fd3e4691115a3965d477c5076deb1f5eb05a569db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070586"
---
# <a name="rendering-directwrite"></a>DirectWrite de renderização

## <a name="rendering-options"></a>Opções de renderização

o texto com formatação descrita por apenas um objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) pode ser renderizado com [Direct2D](../direct2d/direct2d-portal.md), no entanto, há mais algumas opções para renderizar um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

A cadeia de caracteres descrita por um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) pode ser renderizada usando os métodos abaixo.

## <a name="1-render-using-direct2d"></a>1. renderizar usando Direct2D

para renderizar um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) usando Direct2D, use o método [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , conforme mostrado no código a seguir.


```C++
pRT_->DrawTextLayout(
    origin,
    pTextLayout_,
    pBlackBrush_
    );

```



para obter uma visão mais detalhada do desenho de um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) usando [Direct2D](../direct2d/direct2d-portal.md), consulte [Introdução com DirectWrite](getting-started-with-directwrite.md).

## <a name="2-render-using-a-custom-text-renderer"></a>2. renderizar usando um processador de texto personalizado.

Você renderiza com um renderizador personalizado usando o método [**bruto IDWriteTextLayout::D**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) , que usa uma interface de retorno de chamada derivada de [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) como um argumento, conforme mostrado no código a seguir.


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



O método [**RAW IDWriteTextLayout::D**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) chama os métodos do retorno de chamada do processador personalizado fornecido por você. Os métodos [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)e [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) executam as funções de desenho.

[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) declara métodos para desenhar uma execução de glifo, sublinhado, tachado e objetos embutidos. Cabe ao aplicativo implementar esses métodos. A criação de um renderizador de texto personalizado permite que o aplicativo aplique efeitos adicionais ao renderizar texto, como um preenchimento ou uma estrutura de tópicos personalizada. um renderizador de texto personalizado de exemplo está incluído no [exemplo de Olá, Mundo de DirectWrite](/samples/browse/?redirectedfrom=MSDN-samples).

## <a name="3-render-cleartype-to-a-gdi-surface"></a>3. renderizar ClearType para uma superfície GDI.

A renderização em uma superfície GDI é, na verdade, um exemplo de uso de um renderizador de texto personalizado. No entanto, parte do trabalho é feita para você na forma da interface [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) .

Para criar essa interface, use o método [**IDWriteGdiInterop:: CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) .

O método [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) do seu renderizador de texto personalizado chama o método [**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) para desenhar os glifos. O processamento dos objetos sublinhados, tachados e embutidos deve ser feito pelo seu renderizador personalizado.

A interface [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) é processada para um DC (contexto de dispositivo) na memória. Você Obtém um identificador para esse controlador de domínio usando o método [**IDWriteBitmapRenderTarget:: GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) .


```C++
memoryHdc = g_pBitmapRenderTarget->GetMemoryDC();
```



Depois que o desenho for executado, o controlador de domínio de memória do objeto [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) deverá ser copiado para a superfície GDI de destino.

> [!Note]  
> você também tem a opção de transferir o bitmap para outro tipo de superfície, como uma superfície de GDI+.

 


```C++
// Transfer from DWrite's rendering target to the window.
BitBlt(
    hdc,
    0, 0,
    size.cx, size.cy,
    memoryHdc,
    0, 0, 
    SRCCOPY | NOMIRRORBITMAP
    );
```



> [!Note]  
> Seu aplicativo tem a responsabilidade de renderizar tudo na janela no final. Isso inclui texto e elementos gráficos. Há uma penalidade de desempenho para isso. Além disso, o processamento para um controlador de domínio de memória não é acelerado por hardware GDI.

 

Para obter uma visão geral mais detalhada de interoperação com GDI, consulte [interoperação com GDI](interoperating-with-gdi.md).

## <a name="4-render-grayscale-text-transparently-to-a-gdi-surface-windows-8-and-later"></a>4. renderizar texto em escala de cinza de forma transparente para uma superfície GDI. (Windows 8 e posterior)

a partir do Windows 8, você pode renderizar o texto em escala de cinza de forma transparente para uma superfície GDI para melhorar o desempenho. Para fazer isso, você precisa:

1.  Limpe o DC de memória para transparente.
2.  Renderizar o texto para o HDC de memória usando anti-aliasing em escala de cinza ( \_ \_ escala de cinza do modo AntiAlias de texto DWRITE \_ \_ ).
3.  Use a função [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) para renderizar a memória HDC de forma transparente na parte superior do HDC de destino final.
4.  Repita quantas vezes forem necessárias (digamos, uma vez por execução de glifo) e entre outros gráficos podem ser renderizados diretamente para o HDC de destino final sem ser substituído pela função [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) .


```C++
pRT_->SetTextAntialiasMode(DWRITE_TEXT_ANTIALIAS_MODE_GRAYSCALE);

pRT_->DrawTextLayout(
    origin,
    pTextLayout_,
    pBlackBrush_
    );

BLENDFUNCTION blendFunction = { 0 };  
blendFunction.BlendOp = AC_SRC_OVER;  
blendFunction.SourceConstantAlpha = 255;  
blendFunction.AlphaFormat = AC_SRC_ALPHA;

AlphaBlend(  
        hdc,  
        0, 0,  
        width, height,  
        pRT_->GetMemoryDC(),  
        0, 0,  
        width, height,  
        blendFunction  
        );

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderizar usando Direct2D](rendering-by-using-direct2d.md)
</dt> <dt>

[Renderizar usando um renderizador de texto personalizado](how-to-implement-a-custom-text-renderer.md)
</dt> <dt>

[Renderizar para uma superfície GDI](render-to-a-gdi-surface.md)
</dt> <dt>

[Interoperação com GDI](interoperating-with-gdi.md)
</dt> </dl>

 

 