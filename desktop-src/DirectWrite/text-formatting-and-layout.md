---
title: Layout e formatação de texto
description: O DirectWrite fornece duas interfaces para formatar o texto IDWriteTextFormat e IDWriteTextLayout.
ms.assetid: a68963a6-e486-4881-8ad6-873173396fca
keywords:
- DirectWrite, formatação de texto
- DirectWrite, layout
- DirectWrite, interface IDWriteTextFormat
- DirectWrite, interface IDWriteTextLayout
- Interface IDWriteTextFormat
- Interface IDWriteTextLayout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30fcf884c15015af2645c32e217d3b4a6b433554
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162385"
---
# <a name="text-formatting-and-layout"></a>Layout e formatação de texto

O [DirectWrite](direct-write-portal.md) fornece duas interfaces para formatar texto: [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout). **IDWriteTextFormat** descreve apenas o formato de texto e é usado em casos em que uma cadeia de caracteres inteira deve ter o mesmo tamanho de fonte, estilo, peso e assim por diante. Por outro lado, **IDWriteTextLayout** encapsula uma cadeia de caracteres de texto e a formatação para os intervalos especificados da cadeia de caracteres. Este documento descreve cada interface e seus usos. Para obter mais informações sobre a criação e os métodos dessas interfaces, consulte as páginas de referência do [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e do [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

Este documento contém as seguintes partes:

-   [IDWriteTextFormat](#modifying-an-idwritetextformat)
    -   [Modificando um IDWriteTextFormat](#modifying-an-idwritetextformat)
-   [IDWriteTextLayout](#idwritetextlayout)
    -   [Formatando um intervalo de texto](#formatting-a-range-of-text)
    -   [Opções de renderização](#rendering-options)

## <a name="idwritetextformat"></a>IDWriteTextFormat

Um objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) é usado para:

-   Descreva o formato de uma cadeia de caracteres inteira ao renderizar. Para renderizar uma cadeia de caracteres com vários formatos, use um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .
-   Especifique o formato de texto padrão ao criar um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

Para criar um objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , use o método [**IDWriteFactory:: CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) e especifique a família de fontes, a coleção de fontes, a espessura da fonte, o tamanho da fonte (em DIPs) e o nome da localidade.

### <a name="modifying-an-idwritetextformat"></a>Modificando um IDWriteTextFormat

Depois que uma interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) é criada, alguns valores não podem ser alterados: a família de fontes, a coleção, o peso e o tamanho, bem como o nome da localidade. Para alterar esses valores, um novo objeto **IDWriteTextFormat** deve ser criado.

O [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) permite que você altere as propriedades acima sem recriar a ação. O [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) permite que você faça alterações de formato que se apliquem ao texto inteiro, como alinhamento de texto. Se você quiser aplicar formatação a intervalos de caracteres específicos, faça isso usando um **IDWriteTextLayout**.

[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) fornece métodos para definir o alinhamento de texto, direção de fluxo, parada de tabulação incremental, espaçamento de linha, alinhamento de parágrafo, corte e quebra automática de texto. Essas propriedades podem ser alteradas a qualquer momento após a criação do objeto **IDWriteTextFormat** .

## <a name="idwritetextlayout"></a>IDWriteTextLayout

A interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , ao contrário de [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat), representa um bloco de texto e a formatação associada. **IDWriteTextFormat** representa informações de formatação inicial. O exemplo a seguir mostra como criar um objeto **IDWriteTextLayout** usando [**IDWriteFactory:: CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout).


```C++
// Create a text layout using the text format.
if (SUCCEEDED(hr))
{
    RECT rect;
    GetClientRect(hwnd_, &rect); 
    float width  = rect.right  / dpiScaleX_;
    float height = rect.bottom / dpiScaleY_;

    hr = pDWriteFactory_->CreateTextLayout(
        wszText_,      // The string to be laid out and formatted.
        cTextLength_,  // The length of the string.
        pTextFormat_,  // The text format to apply to the string (contains font information, etc).
        width,         // The width of the layout box.
        height,        // The height of the layout box.
        &pTextLayout_  // The IDWriteTextLayout interface pointer.
        );
}

```



O texto em um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) não pode ser alterado depois que o objeto é criado. Para alterar o texto, você deve excluir o objeto existente e criar um novo objeto **IDWriteTextLayout** .

Você pode usar um [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) para formatar os intervalos de texto especificados. O **IDWriteTextLayout** também fornece métodos para alterar o estilo e o peso da fonte e adicionar recursos de fonte OpenType e teste de clique. Para obter mais informações e uma lista completa de métodos, consulte a página de referência do [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

### <a name="formatting-a-range-of-text"></a>Formatando um intervalo de texto

O [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) fornece vários métodos para formatar intervalos de texto. Cada um desses métodos usa uma estrutura de [**\_ \_ intervalo de texto DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) como um parâmetro para especificar a posição do texto inicial dentro da cadeia de caracteres e o comprimento do intervalo a ser formatado. O exemplo a seguir mostra como definir a espessura da fonte de um intervalo de texto para negrito.


```C++
// Set the font weight to bold for the first 5 letters.
DWRITE_TEXT_RANGE textRange = {0, 5};

if (SUCCEEDED(hr))
{
    hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
}

```



### <a name="rendering-options"></a>Opções de renderização

O texto com formatação descrita por apenas um objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) pode ser renderizado com [Direct2D](../direct2d/direct2d-portal.md), no entanto, há mais algumas opções para renderizar um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

A cadeia de caracteres descrita por um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) pode ser renderizada usando os métodos abaixo.

1.  [Renderizar usando Direct2D](rendering-by-using-direct2d.md).
2.  [Renderizar usando um processador de texto personalizado](how-to-implement-a-custom-text-renderer.md).
3.  [Renderizar para uma superfície GDI](render-to-a-gdi-surface.md).

 

 