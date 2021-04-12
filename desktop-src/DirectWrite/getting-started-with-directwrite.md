---
title: Tutorial Introdução com DirectWrite
description: Este documento mostra como usar DirectWrite e Direct2D para criar texto simples que contém um único formato e, em seguida, o texto que contém vários formatos.
ms.assetid: cc2758d7-3f47-452a-8d81-3f777fe490ec
keywords:
- DirectWrite, tutorial
- DirectWrite, tutorial de introdução
- DirectWrite, Direct2D
- Direct2D
- DirectWrite, interface IDWriteTextLayout
- Interface IDWriteTextLayout
- DirectWrite, interface IDWriteTypography
- Interface IDWriteTypography
- DirectWrite, interface IDWriteTextFormat
- Interface IDWriteTextFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fb385ff78650a16599a32d76d7c51ba575de47
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294302"
---
# <a name="tutorial-getting-started-with-directwrite"></a>Tutorial: Introdução com DirectWrite

Este documento mostra como usar [DirectWrite](direct-write-portal.md) e [Direct2D](rendering-by-using-direct2d.md) para criar texto simples que contém um único formato e, em seguida, o texto que contém vários formatos.

Este tutorial contém as seguintes partes:

-   [Código-fonte](#source-code)
-   [Desenho de texto simples](#drawing-simple-text)
    -   [Parte 1: declare os recursos DirectWrite e Direct2D.](#part-1-declare-directwrite-and-direct2d-resources)
    -   [Parte 2: criar recursos independentes de dispositivo.](#part-2-create-device-independent-resources)
    -   [Parte 3: criar Device-Dependent recursos.](#part-3-create-device-dependent-resources)
    -   [Parte 4: desenhar texto usando o método DrawText Direct2D.](#part-4-draw-text-by-using-the-direct2d-drawtext-method)
    -   [Parte 5: renderizar o conteúdo da janela usando Direct2D](#part-5-render-the-window-contents-using-direct2d)
-   [Desenhar texto com vários formatos.](#drawing-text-with-multiple-formats)
    -   [Parte 1: criar uma interface IDWriteTextLayout.](#part-1-create-an-idwritetextlayout-interface)
    -   [Parte 2: aplicando a formatação com IDWriteTextLayout.](#part-2-applying-formatting-with-idwritetextlayout)
    -   [Parte 3: adicionando recursos tipográficos com IDWriteTypography.](#part-3-adding-typographic-features-with-idwritetypography)
    -   [Parte 4: desenhar texto usando o método Direct2D DrawTextLayout.](#part-4-draw-text-using-the-direct2d-drawtextlayout-method)

## <a name="source-code"></a>Código-fonte

O código-fonte mostrado nesta visão geral é obtido do [exemplo de Olá, mundo DirectWrite](/samples/browse/?redirectedfrom=MSDN-samples). Cada parte é implementada em uma classe separada (SimpleText e multiformattedtext) e é exibida em uma janela filho separada. Cada classe representa uma janela do Microsoft Win32. Além do método *WndProc* , cada classe contém os seguintes métodos:



| Função                              | Descrição                                                                                         |
|---------------------------------------|-----------------------------------------------------------------------------------------------------|
| **CreateDeviceIndependentResources**  | Cria recursos independentes de dispositivo, para que eles possam ser reutilizados em qualquer lugar.                      |
| **DiscardDeviceIndependentResources** | Libera os recursos independentes do dispositivo depois que eles não são mais necessários.                          |
| **CreateDeviceResources**             | Cria recursos, como pincéis e destinos de renderização, que estão vinculados a um dispositivo específico.        |
| **DiscardDeviceResources**            | Libera os recursos dependentes do dispositivo depois que eles não são mais necessários.                            |
| **DrawD2DContent**                    | Usa [Direct2D](../direct2d/direct2d-portal.md) para renderizar para a tela.                              |
| **DrawText**                          | Desenha a cadeia de texto usando [Direct2D](../direct2d/direct2d-portal.md).                            |
| **OnResize**                          | Redimensiona o destino de renderização [Direct2D](../direct2d/direct2d-portal.md) quando o tamanho da janela é alterado. |



 

Você pode usar o exemplo fornecido ou usar as instruções a seguir para adicionar [DirectWrite](direct-write-portal.md) e [Direct2D](rendering-by-using-direct2d.md) ao seu próprio aplicativo Win32. Para obter mais informações sobre o exemplo e os arquivos de projeto associados, consulte o [exemplo DirectWriteHelloWorld](/samples/browse/?redirectedfrom=MSDN-samples).

## <a name="drawing-simple-text"></a>Desenho de texto simples

Esta seção mostra como usar [DirectWrite](direct-write-portal.md) e [Direct2D](../direct2d/direct2d-portal.md) para renderizar texto simples que tem um único formato, como mostrado na captura de tela a seguir.

![captura de tela de "Olá, mundo usando DirectWrite!" em um único formato](images/simplecropped.png)

O desenho de texto simples na tela requer quatro componentes:

-   Uma cadeia de caracteres a ser renderizada.
-   Uma instância de [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).
-   As dimensões da área para conter o texto.
-   Um objeto que pode renderizar o texto. Neste tutorial. Você usa um destino de renderização [Direct2D](../direct2d/direct2d-portal.md) .

A interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) descreve o nome, o tamanho, o peso, o estilo e a ampliação da família de fontes usados para formatar o texto e descreve as informações de localidade. **IDWriteTextFormat** também define métodos para definir e obter as seguintes propriedades:

-   O espaçamento da linha.
-   O alinhamento do texto em relação às bordas esquerda e direita da caixa de layout.
-   O alinhamento de parágrafo em relação à parte superior e inferior da caixa de layout.
-   A direção de leitura.
-   A granularidade de corte de texto para texto que estoura a caixa de layout.
-   A parada de tabulação incremental.
-   A direção do fluxo de parágrafo.

A interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) é necessária para o desenho de texto que usa os dois processos descritos neste documento.

Antes de criar um objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) ou qualquer outro objeto [DirectWrite](direct-write-portal.md) , você precisa de uma instância [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) . Você usa um **IDWriteFactory** para criar instâncias **IDWriteTextFormat** e outros objetos DirectWrite. Para obter uma instância de fábrica, use a função [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) .

### <a name="part-1-declare-directwrite-and-direct2d-resources"></a>Parte 1: declare os recursos DirectWrite e Direct2D.

Nesta parte, você declara os objetos que serão usados posteriormente para criar e exibir texto como membros de dados privados de sua classe. Todas as interfaces, funções e tipos de datatipos para [DirectWrite](direct-write-portal.md) são declaradas no arquivo de cabeçalho *dwrite. h* e aquelas para [Direct2D](../direct2d/direct2d-portal.md) são declaradas no *d2d1. h*; Se você ainda não fez isso, inclua esses cabeçalhos em seu projeto.

1.  Em seu arquivo de cabeçalho de classe (SimpleText. h), declare ponteiros para as interfaces [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) e [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) como membros privados.
    ```C++
    IDWriteFactory* pDWriteFactory_;
    IDWriteTextFormat* pTextFormat_;
    
    ```

    

2.  Declare membros para manter a cadeia de texto a ser renderizada e o comprimento da cadeia de caracteres.
    ```C++
    const wchar_t* wszText_;
    UINT32 cTextLength_;
    
    ```

    

3.  Declare ponteiros para as interfaces [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)e [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) para renderizar o texto com [Direct2D](../direct2d/direct2d-portal.md).
    ```C++
    ID2D1Factory* pD2DFactory_;
    ID2D1HwndRenderTarget* pRT_;
    ID2D1SolidColorBrush* pBlackBrush_;
    
    ```

    

### <a name="part-2-create-device-independent-resources"></a>Parte 2: criar recursos independentes de dispositivo.

O [Direct2D](rendering-by-using-direct2d.md) fornece dois tipos de recursos: recursos dependentes de dispositivo e recursos independentes de dispositivo. Os recursos dependentes do dispositivo são associados a um dispositivo de renderização e não funcionam mais se esse dispositivo for removido. Os recursos independentes de dispositivo, por outro lado, podem durar o escopo do seu aplicativo.

Os recursos do [DirectWrite](direct-write-portal.md) são independentes de dispositivo.

Nesta seção, você cria os recursos independentes do dispositivo que são usados pelo seu aplicativo. Esses recursos devem ser liberados com uma chamada para o método **Release** da interface.

Alguns dos recursos que são usados precisam ser criados apenas uma vez e não estão vinculados a um dispositivo. A inicialização desses recursos é colocada no método *SimpleText:: CreateDeviceIndependentResources* , que é chamado ao inicializar a classe.

1.  Dentro do método *SimpleText:: CreateDeviceIndependentResources* no arquivo de implementação de classe (SimpleText. cpp), chame a função [**D2D1CreateFactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) para criar uma interface [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , que é a interface de fábrica raiz para todos os objetos [Direct2D](../direct2d/direct2d-portal.md) . Você usa a mesma fábrica para criar uma instância de outros recursos de Direct2D.
    ```C++
    hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &pD2DFactory_
        );
    
    ```

    

2.  Chame a função [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) para criar uma interface [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) , que é a interface de fábrica raiz para todos os objetos [DirectWrite](direct-write-portal.md) . Você usa a mesma fábrica para criar uma instância de outros recursos de DirectWrite.
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory_)
            );
    }
    
    ```

    

3.  Inicialize a cadeia de texto e armazene seu comprimento.

    ```C++
    wszText_ = L"Hello World using  DirectWrite!";
    cTextLength_ = (UINT32) wcslen(wszText_);
    
    ```

    

4.  Crie um objeto de interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) usando o método [**IDWriteFactory:: CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) . O **IDWriteTextFormat** especifica a fonte, o peso, a ampliação, o estilo e a localidade que serão usados para renderizar a cadeia de texto.
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTextFormat(
            L"Gabriola",                // Font family name.
            NULL,                       // Font collection (NULL sets it to use the system font collection).
            DWRITE_FONT_WEIGHT_REGULAR,
            DWRITE_FONT_STYLE_NORMAL,
            DWRITE_FONT_STRETCH_NORMAL,
            72.0f,
            L"en-us",
            &pTextFormat_
            );
    }
    
    ```

    

5.  Centralize o texto horizontal e verticalmente chamando os métodos [**IDWriteTextFormat:: SetTextAlign**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) e [**IDWriteTextFormat:: SetParagraphAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) .
    ```C++
    // Center align (horizontally) the text.
    if (SUCCEEDED(hr))
    {
        hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    }

    if (SUCCEEDED(hr))
    {
        hr = pTextFormat_->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    }
    
    ```

    

Nesta parte, você inicializou os recursos independentes do dispositivo que são usados pelo seu aplicativo. Na próxima parte, você inicializa os recursos dependentes do dispositivo.

### <a name="part-3-create-device-dependent-resources"></a>Parte 3: criar Device-Dependent recursos.

Nesta parte, você cria um [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) e um [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) para renderizar seu texto.

Um destino de renderização é um objeto Direct2D que cria recursos de desenho e renderiza comandos de desenho para um dispositivo de renderização. Um [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) é um destino de renderização que é renderizado para um **HWND**.

Um dos recursos de desenho que um destino de renderização pode criar é um pincel para contornos de pintura, preenchimentos e texto. Um [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) pinta com uma cor sólida.

As interfaces [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) e [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) estão associadas a um dispositivo de renderização quando são criadas e devem ser liberadas e recriadas se o dispositivo se tornar inválido.

1.  Dentro do método SimpleText:: CreateDeviceResources, verifique se o ponteiro de destino de renderização é **nulo**. Se for, recupere o tamanho da área de renderização e crie um [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) desse tamanho. Use o **ID2D1HwndRenderTarget** para criar um [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).
    ```C++
    RECT rc;
    GetClientRect(hwnd_, &rc);

    D2D1_SIZE_U size = D2D1::SizeU(rc.right - rc.left, rc.bottom - rc.top);

    if (!pRT_)
    {
        // Create a Direct2D render target.
        hr = pD2DFactory_->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(
                    hwnd_,
                    size
                    ),
                &pRT_
                );

        // Create a black brush.
        if (SUCCEEDED(hr))
        {
            hr = pRT_->CreateSolidColorBrush(
                D2D1::ColorF(D2D1::ColorF::Black),
                &pBlackBrush_
                );
        }
    }
    
    ```

    

2.  No método SimpleText::D iscardDeviceResources, libere o pincel e o destino de renderização.
    ```C++
    SafeRelease(&pRT_);
    SafeRelease(&pBlackBrush_);
    
    ```

    

Agora que você criou um destino de renderização e um pincel, você pode usá-los para renderizar seu texto.

### <a name="part-4-draw-text-by-using-the-direct2d-drawtext-method"></a>Parte 4: desenhar texto usando o método DrawText Direct2D.

1.  No método SimpleText::D rawText da sua classe, defina a área para o layout de texto recuperando as dimensões da área de renderização e crie um retângulo de [Direct2D](../direct2d/direct2d-portal.md) que tenha as mesmas dimensões.
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  Use o método [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) e o objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) para renderizar o texto na tela. O método **ID2D1RenderTarget::D rawtext** usa os seguintes parâmetros:
    -   Uma cadeia de caracteres a ser renderizada.
    -   Um ponteiro para uma interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) .
    -   Um retângulo de layout [Direct2D](../direct2d/direct2d-portal.md) .
    -   Um ponteiro para uma interface que expõe [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

### <a name="part-5-render-the-window-contents-using-direct2d"></a>Parte 5: renderizar o conteúdo da janela usando Direct2D

Para renderizar o conteúdo da janela usando [Direct2D](../direct2d/direct2d-portal.md) quando uma mensagem de pintura for recebida, faça o seguinte:

1.  Crie os recursos dependentes do dispositivo chamando o método SimpleText:: CreateDeviceResources implementado na parte 3.
2.  Chame o método [**ID2D1HwndRenderTarget:: BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) do destino render.
3.  Limpe o destino de renderização chamando o método [**ID2D1HwndRenderTarget:: Clear**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) .
4.  Chame o método SimpleText::D rawText, implementado na parte 4.
5.  Chame o método [**ID2D1HwndRenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) do destino de renderização.
6.  Se for necessário, descarte os recursos dependentes do dispositivo para que eles possam ser recriados quando a janela for redesenhada.


```C++
hr = CreateDeviceResources();

if (SUCCEEDED(hr))
{
    pRT_->BeginDraw();

    pRT_->SetTransform(D2D1::IdentityMatrix());

    pRT_->Clear(D2D1::ColorF(D2D1::ColorF::White));

    // Call the DrawText method of this class.
    hr = DrawText();

    if (SUCCEEDED(hr))
    {
        hr = pRT_->EndDraw(
            );
    }
}

if (FAILED(hr))
{
    DiscardDeviceResources();
}

```



A classe SimpleText é implementada em SimpleText. h e SimpleText. cpp.

## <a name="drawing-text-with-multiple-formats"></a>Desenhar texto com vários formatos.

Esta seção mostra como usar [DirectWrite](direct-write-portal.md) e [Direct2D](../direct2d/direct2d-portal.md) para renderizar texto com vários formatos, conforme mostrado na captura de tela a seguir.

![captura de tela de "Olá, mundo usando DirectWrite!", com algumas partes em diferentes estilos, tamanhos e formatos](images/multiformattedcropped.png)

O código desta seção é implementado como a classe multiformattedtext no [exemplo DWriteHelloWorld](/samples/browse/?redirectedfrom=MSDN-samples). Ele se baseia nas etapas da seção anterior.

Para criar texto com vários formatos, use a interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) além da interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) introduzida na seção anterior. A interface **IDWriteTextLayout** descreve a formatação e o layout de um bloco de texto. Além da formatação padrão especificada por um objeto **IDWriteTextFormat** , a formatação de intervalos específicos de texto pode ser alterada usando **IDWriteTextLayout**. Isso inclui o nome, o tamanho, o peso, o estilo, a ampliação, o tachado e o sublinhado da família de fontes.

O [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) também fornece métodos de teste de clique. As métricas de teste de colisão retornadas por esses métodos são relativas à caixa de layout especificada quando o objeto de interface **IDWriteTextLayout** é criado usando o método [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) da interface [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .

A interface [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) é usada para adicionar recursos de tipografia [OpenType](../intl/opentype-font-format.md) opcionais a um layout de texto, como traços violentos e conjuntos de texto estilísticos alternativos. Recursos tipográficos podem ser adicionados a um intervalo específico de texto dentro de um layout de texto chamando o método [**AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) da interface **IDWriteTypography** . Esse método recebe uma estrutura de [**\_ \_ recursos de fonte DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) como um parâmetro que contém uma constante de enumeração de **marca de \_ \_ recurso \_ de fonte DWRITE** e um parâmetro de execução **UINT32** . Uma lista de recursos OpenType registrados pode ser encontrada no [registro de marca de layout OpenType](https://www.microsoft.com/typography/otspec/features_ae.htm) em Microsoft.com. Para obter as constantes de enumeração DirectWrite equivalentes, consulte **\_ marca de \_ recurso \_ de fonte DWRITE**.

### <a name="part-1-create-an-idwritetextlayout-interface"></a>Parte 1: criar uma interface IDWriteTextLayout.

1.  Declare um ponteiro para uma interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) como membro da classe multiformattedtext.
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  No final do método multiformattedtext:: CreateDeviceIndependentResources, crie um objeto de interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chamando o método [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) . A interface **IDWriteTextLayout** fornece recursos de formatação adicionais, como a capacidade de aplicar formatos diferentes a partes selecionadas de texto.
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

    

### <a name="part-2-applying-formatting-with-idwritetextlayout"></a>Parte 2: aplicando a formatação com IDWriteTextLayout.

A formatação, como o tamanho da fonte, o peso e o sublinhado, pode ser aplicada a subcadeias de texto a serem exibidas usando a interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

1.  Defina o tamanho da fonte para a subcadeia de caracteres "di" de "DirectWrite" como 100, declarando um [**\_ \_ intervalo de texto DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) e chamando o método [**IDWriteTextLayout:: setfonts**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontsize) .
    ```C++
    // Format the "DirectWrite" substring to be of font size 100.
    if (SUCCEEDED(hr))
    {
        DWRITE_TEXT_RANGE textRange = {20,        // Start index where "DirectWrite" appears.
                                        6 };      // Length of the substring "Direct" in "DirectWrite".
        hr = pTextLayout_->SetFontSize(100.0f, textRange);
    }
    ```

    

2.  Sublinhar a subcadeia de caracteres "DirectWrite" chamando o método [**IDWriteTextLayout::**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) ondele.
    ```C++
    // Format the word "DWrite" to be underlined.
    if (SUCCEEDED(hr))
    {
        
        DWRITE_TEXT_RANGE textRange = {20,      // Start index where "DirectWrite" appears.
                                       11 };    // Length of the substring "DirectWrite".
        hr = pTextLayout_->SetUnderline(TRUE, textRange);
    }
    ```

    

3.  Defina a espessura da fonte como negrito para a subcadeia de caracteres "DirectWrite" chamando o método [**IDWriteTextLayout:: setespessuradafonte**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontweight) .
    ```C++
    if (SUCCEEDED(hr))
    {
        // Format the word "DWrite" to be bold.
        DWRITE_TEXT_RANGE textRange = {20,
                                       11 };
        hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
    }
    ```

    

### <a name="part-3-adding-typographic-features-with-idwritetypography"></a>Parte 3: adicionando recursos tipográficos com IDWriteTypography.

1.  Declare e crie um objeto de interface [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) chamando o método [**IDWriteFactory:: createtypography**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtypography) .
    ```C++
    // Declare a typography pointer.
    IDWriteTypography* pTypography = NULL;

    // Create a typography interface object.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTypography(&pTypography);
    }
    
    ```

    

2.  Adicione um recurso de fonte declarando um objeto de [**\_ \_ recurso de fonte DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) que tem o conjunto estilístico 7 especificado e chamando o método [**IDWriteTypography:: AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) .
    ```C++
    // Set the stylistic set.
    DWRITE_FONT_FEATURE fontFeature = {DWRITE_FONT_FEATURE_TAG_STYLISTIC_SET_7,
                                       1};
    if (SUCCEEDED(hr))
    {
        hr = pTypography->AddFontFeature(fontFeature);
    }
    
    ```

    

3.  Defina o layout de texto para usar a tipografia sobre a cadeia de caracteres inteira declarando uma variável de [**\_ \_ intervalo de texto DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) e chamando o método [**IDWriteTextLayout:: settypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) e passando o intervalo de texto.
    ```C++
    if (SUCCEEDED(hr))
    {
        // Set the typography for the entire string.
        DWRITE_TEXT_RANGE textRange = {0,
                                       cTextLength_};
        hr = pTextLayout_->SetTypography(pTypography, textRange);
    }
    
    ```

    

4.  Defina a nova largura e a altura do objeto de layout de texto no método multiformattedtext:: OnResize.
    ```C++
    if (pTextLayout_)
    {
        pTextLayout_->SetMaxWidth(static_cast<FLOAT>(width / dpiScaleX_));
        pTextLayout_->SetMaxHeight(static_cast<FLOAT>(height / dpiScaleY_));
    }
    ```

    

### <a name="part-4-draw-text-using-the-direct2d-drawtextlayout-method"></a>Parte 4: desenhar texto usando o método Direct2D DrawTextLayout.

Para desenhar o texto com as configurações de layout de texto especificadas pelo objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , altere o código no método multiformattedtext::D rawtext para usar [**IDWriteTextLayout::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).

1.  Delcare uma variável de [**d2d1 do \_ ponto \_ 2F**](../direct2d/d2d1-point-2f.md) e defina-a como o ponto superior esquerdo da janela.
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  Desenhe o texto na tela chamando o método [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) do destino de renderização [Direct2D](../direct2d/direct2d-portal.md) e passando o ponteiro [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

A classe multiformattedtext é implementada em multiformattedtext. h e multiformattedtext. cpp.

 

 