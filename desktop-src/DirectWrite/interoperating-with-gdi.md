---
title: Interoperação com GDI
description: O DirectWrite fornece um caminho de migração do e de alguma interoperabilidade com o modelo de fonte da GDI, bem como interfaces para renderização de texto em um bitmap que pode ser desenhado em uma janela.
ms.assetid: fb73e07b-60fb-4726-bd5b-c14d61ace186
keywords:
- Interoperação DirectWrite, GDI
- DirectWrite, interoperabilidade
- interoperabilidade
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41c7c99e6bfac0aabddd4a1568b64cd425ccb25b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007590"
---
# <a name="interoperating-with-gdi"></a>Interoperação com GDI

O [DirectWrite](direct-write-portal.md) fornece um caminho de migração do e de alguma interoperabilidade com o modelo de fonte da GDI, bem como interfaces para renderização de texto em um bitmap que pode ser desenhado em uma janela.

Esta visão geral contém as seguintes partes:

-   [Introdução](#introduction)
-   [Parte 1: IDWriteGdiInterop](#part-1-idwritegdiinterop)
-   [Parte 2: objetos Font](#part-2-font-objects)
-   [Parte 3: renderizando](#part-3-rendering)

## <a name="introduction"></a>Introdução

O [DirectWrite](direct-write-portal.md) fornece métodos para converter entre a estrutura LOGFONT do GDI e as interfaces de fonte DirectWrite. Isso permite que você use GDI para algumas ou toda a enumeração e seleção de fontes, aproveitando a funcionalidade e o desempenho aprimorados do DirectWrite. DirectWrite também tem interfaces para renderização em um bitmap se você quiser exibir texto em uma superfície GDI.

## <a name="part-1-idwritegdiinterop"></a>Parte 1: IDWriteGdiInterop

A interface [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) é usada para converter entre as estruturas de fonte GDI e as interfaces de fonte [DirectWrite](direct-write-portal.md) e também para criar um objeto [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) . Obtenha um objeto **IDWriteGdiInterop** usando o método [**IDWriteFactory:: GetGdiInterop**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getgdiinterop) , conforme mostrado no código a seguir.


```C++
// Create a GDI interop interface.
if (SUCCEEDED(hr))
{
    hr = g_pDWriteFactory->GetGdiInterop(&g_pGdiInterop);
}
```



## <a name="part-2-font-objects"></a>Parte 2: objetos Font

O GDI usa a estrutura LOGFONT para armazenar informações sobre a fonte e o estilo de texto. O método [**IDWriteGdiInterop:: CreateFontFromLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont) converterá uma estrutura LOGFONT em um objeto [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) , como visto no código a seguir.


```C++
// Convert to a DirectWrite font.
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateFontFromLOGFONT(&lf, &pFont);
}
```



No entanto, o [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) não encapsula todas as mesmas informações que um LOGFONT. Uma estrutura LOGFONT contém o tamanho da fonte, o peso, o estilo, o sublinhado, o riscado, o nome da face da fonte e outras informações. Os objetos **IDWriteFont** contêm informações sobre uma fonte e seu peso e estilo, mas não o tamanho da fonte, sublinhado e assim por diante. Com o [DirectWrite](direct-write-portal.md), elementos de informações de formatação como esses são encapsulados por um objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) ou, para intervalos de texto específicos, um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

Você tem a opção de converter um [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) em um LOGFONT usando o [**IDWriteGdiInterop:: ConvertFontToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont).

## <a name="part-3-rendering"></a>Parte 3: renderizando

Para renderizar o texto DirectWrite em uma superfície GDI, use um processador de texto personalizado. Consulte o tópico [renderizar em uma superfície GDI](render-to-a-gdi-surface.md) .

 

 