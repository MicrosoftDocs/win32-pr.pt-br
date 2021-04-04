---
title: Como executar testes de clique em um layout de texto
description: Fornece um breve tutorial sobre como adicionar testes de clique a um aplicativo DirectWrite que exibe o texto usando a interface IDWriteTextLayout.
ms.assetid: ef30c931-10f6-4317-b2ea-b446990778b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ca80ac641920c4e63c08f4cbb0fd9e24eb7b2d
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103930226"
---
# <a name="how-to-perform-hit-testing-on-a-text-layout"></a>Como executar testes de clique em um layout de texto

Fornece um breve tutorial sobre como adicionar testes de clique a um aplicativo [DirectWrite](direct-write-portal.md) que exibe o texto usando a interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

O resultado deste tutorial é um aplicativo que sublinha o caractere que é clicado pelo botão esquerdo do mouse, conforme mostrado na captura de tela a seguir.

![captura de tela de "clique neste texto"](images/hittest.png)

Este "como" contém as seguintes partes:

- [Etapa 1: criar um layout de texto.](#step-1-create-a-text-layout)
- [Etapa 2: adicionar um método OnClick.](#step-2-add-an-onclick-method)
- [Etapa 3: executar testes de clique.](#step-3-perform-hit-testing)
- [Etapa 4: sublinhar o texto clicado.](#step-4-underline-the-clicked-text)
- [Etapa 5: manipular a mensagem do WM \_ LBUTTONDOWN.](/windows)

## <a name="step-1-create-a-text-layout"></a>Etapa 1: criar um layout de texto.

Para começar, você precisará de um aplicativo que usa um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . Se você já tiver um aplicativo que exibe texto com um layout de texto, vá para a etapa 2.

Para adicionar um layout de texto, você deve fazer o seguinte:

1. Declare um ponteiro para uma interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) como um membro da classe.

    ```cpp
    IDWriteTextLayout* pTextLayout_;
    ```

2. No final do método **CreateDeviceIndependentResources** , crie um objeto de interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chamando o método [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .

    ```cpp
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

3. Em seguida, você deve alterar a chamada para o método [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) para [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , conforme mostrado no código a seguir.

    ```cpp
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    ```

## <a name="step-2-add-an-onclick-method"></a>Etapa 2: adicionar um método OnClick.

Agora, adicione um método à classe que usará a funcionalidade de teste de clique do layout de texto.

1. Declare um método **onclick** no arquivo de cabeçalho de classe.

    ```cpp
    void OnClick(
        UINT x,
        UINT y
        );
    ```

2. Defina um método **onclick** no arquivo de implementação de classe.

   ```cpp
    void DemoApp::OnClick(UINT x, UINT y)
    {    
    }
    ```

## <a name="step-3-perform-hit-testing"></a>Etapa 3: executar testes de clique.

Para determinar onde o usuário clicou no layout de texto, usaremos o método [**IDWriteTextLayout:: HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) .

Adicione o seguinte ao método **onclick** que você definiu na etapa 2.

1. Declare as variáveis que passaremos como parâmetros para o método.

    ```cpp
    DWRITE_HIT_TEST_METRICS hitTestMetrics;
    BOOL isTrailingHit;
    BOOL isInside; 
    ```

    O método [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) gera os parâmetros a seguir.

    | Variável         | Descrição                                                                                                                             |
    |------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
    | *hitTestMetrics* | A geometria está totalmente colocando o local de teste de clique.                                                                                     |
    | *isinterna*       | Indica se o local do teste de clique está dentro da cadeia de texto ou não. Quando FALSE, a posição mais próxima da borda do texto é retornada. |
    | *isTrailingHit*  | Indica se o local do teste de clique está no lado da esquerda ou no canto à direita do caractere.                                        |

2. Chame o método [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) do objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

    ```cpp
    pTextLayout_->HitTestPoint(
                    (FLOAT)x, 
                    (FLOAT)y,
                    &isTrailingHit,
                    &isInside,
                    &hitTestMetrics
                    );
    ```

    O código neste exemplo passa as variáveis *x* e *y* para a posição sem qualquer modificação. Isso pode ser feito neste exemplo porque o layout de texto tem o mesmo tamanho que a janela e é originado no canto superior esquerdo da janela. Se esse não for o caso, você precisaria determinar as coordenadas em relação à origem do layout do texto.

## <a name="step-4-underline-the-clicked-text"></a>Etapa 4: sublinhar o texto clicado.

Adicione o seguinte ao **onclick** que você definiu na etapa 2, após a chamada para o método [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) .

```cpp
if (isInside == TRUE)
{
    BOOL underline;

    pTextLayout_->GetUnderline(hitTestMetrics.textPosition, &underline);

    DWRITE_TEXT_RANGE textRange = {hitTestMetrics.textPosition, 1};

    pTextLayout_->SetUnderline(!underline, textRange);
}
```

Esse código faz o seguinte.

1. Verifica se o ponto de teste de clique estava dentro do texto usando a variável *isinterna* .
2. O membro **textPosition** da estrutura *hitTestMetrics* contém o índice de base zero do caractere clicado.

    Obtém o sublinhado deste caractere, passando esse valor para o método [**IDWriteTextLayout:: getabaixo**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) .

3. Declara uma variável [**de \_ \_ intervalo de texto DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) com a posição inicial definida como **hitTestMetrics. textPosition** e um comprimento de 1.
4. Alterna o sublinhado usando o método [**IDWriteTextLayout::**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) ontern.

Depois de definir o sublinhado, Redesenhe o texto chamando o método **DrawD2DContent** da classe.

```cpp
DrawD2DContent();
```

## <a name="step-5-handle-the-wm_lbuttondown-message"></a>Etapa 5: manipular a mensagem do WM \_ LBUTTONDOWN.

Por fim, adicione a mensagem do **WM \_ LBUTTONDOWN** ao manipulador de mensagens para seu aplicativo e chame o método **onclick** da classe.

```cpp
case WM_LBUTTONDOWN:
    {
        int x = GET_X_LPARAM(lParam); 
        int y = GET_Y_LPARAM(lParam);

        pDemoApp->OnClick(x, y);
    }
    break;
```

**Obter \_ As macros x \_ lParam** e **Get \_ x \_ lParam** são declaradas no arquivo de cabeçalho windowsx. h. Eles recuperam facilmente a posição x e y do clique do mouse.
