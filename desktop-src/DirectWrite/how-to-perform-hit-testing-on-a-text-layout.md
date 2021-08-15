---
title: Como executar testes de acerto em um layout de texto
description: Fornece um breve tutorial sobre como adicionar testes de DirectWrite aplicativo que exibe texto usando a interface IDWriteTextLayout.
ms.assetid: ef30c931-10f6-4317-b2ea-b446990778b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d42967b069a7a5008de75c1cecb453a6158857eb2b05d2dd0298584a67cef69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816561"
---
# <a name="how-to-perform-hit-testing-on-a-text-layout"></a>Como executar testes de acerto em um layout de texto

Fornece um breve tutorial sobre como adicionar testes de DirectWrite [aplicativo](direct-write-portal.md) que exibe texto usando a interface [**IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)

O resultado deste tutorial é um aplicativo que sublinha o caractere que é clicado pelo botão esquerdo do mouse, conforme mostrado na captura de tela a seguir.

![captura de tela de "clique neste texto"](images/hittest.png)

Este é o exemplo de como conter as seguintes partes:

- [Etapa 1: Criar um layout de texto.](#step-1-create-a-text-layout)
- [Etapa 2: Adicionar um método OnClick.](#step-2-add-an-onclick-method)
- [Etapa 3: Executar teste de acerto.](#step-3-perform-hit-testing)
- [Etapa 4: sublinhar o texto clicado.](#step-4-underline-the-clicked-text)
- [Etapa 5: manipular a mensagem WM \_ LBUTTONDOWN.](/windows)

## <a name="step-1-create-a-text-layout"></a>Etapa 1: Criar um layout de texto.

Para começar, você precisará de um aplicativo que usa um [**objeto IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) Se você já tiver um aplicativo que exibe texto com um layout de texto, vá para Etapa 2.

Para adicionar um layout de texto, você deve fazer o seguinte:

1. Declare um ponteiro para uma interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) como um membro da classe .

    ```cpp
    IDWriteTextLayout* pTextLayout_;
    ```

2. No final do método **CreateDeviceIndependentResources,** crie um objeto de interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chamando o [**método CreateTextLayout.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout)

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

3. Em seguida, você deve alterar a chamada para o método [**ID2D1RenderTarget::D rawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) para [**ID2D1RenderTarget::D rawTextLayout,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) conforme mostrado no código a seguir.

    ```cpp
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    ```

## <a name="step-2-add-an-onclick-method"></a>Etapa 2: Adicionar um método OnClick.

Agora, adicione um método à classe que usará a funcionalidade de teste de acerto do layout de texto.

1. Declare um **método OnClick** no arquivo de header de classe.

    ```cpp
    void OnClick(
        UINT x,
        UINT y
        );
    ```

2. Defina um **método OnClick** no arquivo de implementação de classe.

   ```cpp
    void DemoApp::OnClick(UINT x, UINT y)
    {    
    }
    ```

## <a name="step-3-perform-hit-testing"></a>Etapa 3: Executar teste de acerto.

Para determinar onde o usuário clicou no layout de texto, vamos usar o [**método IDWriteTextLayout::HitTestPoint.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint)

Adicione o seguinte ao **método OnClick** que você definiu na Etapa 2.

1. Declare as variáveis que passaremos como parâmetros para o método .

    ```cpp
    DWRITE_HIT_TEST_METRICS hitTestMetrics;
    BOOL isTrailingHit;
    BOOL isInside; 
    ```

    O [**método HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) saída os parâmetros a seguir.

    | Variável         | Descrição                                                                                                                             |
    |------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
    | *hitTestMetrics* | A geometria que inclui totalmente o local de teste de acerto.                                                                                     |
    | *isInside*       | Indica se o local de teste de acerto está dentro da cadeia de caracteres de texto ou não. Quando FALSE, a posição mais próxima da borda do texto é retornada. |
    | *isTrailingHit*  | Indica se o local de teste de acerto está no lado à esquerda ou à direita do caractere.                                        |

2. Chame o [**método HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) do [**objeto IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)

    ```cpp
    pTextLayout_->HitTestPoint(
                    (FLOAT)x, 
                    (FLOAT)y,
                    &isTrailingHit,
                    &isInside,
                    &hitTestMetrics
                    );
    ```

    O código neste exemplo passa as *variáveis x* e *y* para a posição sem nenhuma modificação. Isso pode ser feito neste exemplo porque o layout de texto é do mesmo tamanho que a janela e se origina no canto superior esquerdo da janela. Se esse não fosse o caso, você teria que determinar as coordenadas em relação à origem do layout de texto.

## <a name="step-4-underline-the-clicked-text"></a>Etapa 4: sublinhar o texto clicado.

Adicione o seguinte ao **OnClick que você** definiu na Etapa 2, após a chamada para o [**método HitTestPoint.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint)

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

1. Verifica se o ponto de teste de acerto estava dentro do texto usando a *variável isInside.*
2. O **membro textPosition** da estrutura *hitTestMetrics* contém o índice baseado em zero do caractere clicado.

    Obtém o sublinhado desse caractere passando esse valor para o [**método IDWriteTextLayout::GetUnderline.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline)

3. Declara uma [**variável DWRITE \_ TEXT \_ RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) com a posição inicial definida como **hitTestMetrics.textPosition** e um comprimento de 1.
4. Alterna o sublinhado usando o [**método IDWriteTextLayout::SetUnderline.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline)

Depois de definir o sublinhado, redesenhar o texto chamando o **método DrawD2DContent** da classe .

```cpp
DrawD2DContent();
```

## <a name="step-5-handle-the-wm_lbuttondown-message"></a>Etapa 5: manipular a mensagem WM \_ LBUTTONDOWN.

Por fim, adicione **a mensagem WM \_ LBUTTONDOWN** ao manipulador de mensagens para seu aplicativo e chame o **método OnClick** da classe .

```cpp
case WM_LBUTTONDOWN:
    {
        int x = GET_X_LPARAM(lParam); 
        int y = GET_Y_LPARAM(lParam);

        pDemoApp->OnClick(x, y);
    }
    break;
```

**GET \_ As \_** macros X LPARAM **e GET X \_ \_ LPARAM** são declaradas no arquivo de header windowsx.h. Eles recuperam facilmente as posições x e y do clique do mouse.
