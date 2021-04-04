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
# <a name="how-to-perform-hit-testing-on-a-text-layout"></a><span data-ttu-id="e41df-103">Como executar testes de clique em um layout de texto</span><span class="sxs-lookup"><span data-stu-id="e41df-103">How to Perform Hit Testing on a Text Layout</span></span>

<span data-ttu-id="e41df-104">Fornece um breve tutorial sobre como adicionar testes de clique a um aplicativo [DirectWrite](direct-write-portal.md) que exibe o texto usando a interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="e41df-104">Provides a short tutorial about how to add hit testing to a [DirectWrite](direct-write-portal.md) application that displays text by using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface.</span></span>

<span data-ttu-id="e41df-105">O resultado deste tutorial é um aplicativo que sublinha o caractere que é clicado pelo botão esquerdo do mouse, conforme mostrado na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e41df-105">The result of this tutorial is an application that underlines the character that is clicked on by the left mouse button, as shown in the following screen shot.</span></span>

![captura de tela de "clique neste texto"](images/hittest.png)

<span data-ttu-id="e41df-107">Este "como" contém as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="e41df-107">This how to contains the following parts:</span></span>

- [<span data-ttu-id="e41df-108">Etapa 1: criar um layout de texto.</span><span class="sxs-lookup"><span data-stu-id="e41df-108">Step 1: Create a Text Layout.</span></span>](#step-1-create-a-text-layout)
- [<span data-ttu-id="e41df-109">Etapa 2: adicionar um método OnClick.</span><span class="sxs-lookup"><span data-stu-id="e41df-109">Step 2: Add an OnClick method.</span></span>](#step-2-add-an-onclick-method)
- [<span data-ttu-id="e41df-110">Etapa 3: executar testes de clique.</span><span class="sxs-lookup"><span data-stu-id="e41df-110">Step 3: Perform Hit Testing.</span></span>](#step-3-perform-hit-testing)
- [<span data-ttu-id="e41df-111">Etapa 4: sublinhar o texto clicado.</span><span class="sxs-lookup"><span data-stu-id="e41df-111">Step 4: Underline the Clicked Text.</span></span>](#step-4-underline-the-clicked-text)
- [<span data-ttu-id="e41df-112">Etapa 5: manipular a mensagem do WM \_ LBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="e41df-112">Step 5: Handle the WM\_LBUTTONDOWN message.</span></span>](/windows)

## <a name="step-1-create-a-text-layout"></a><span data-ttu-id="e41df-113">Etapa 1: criar um layout de texto.</span><span class="sxs-lookup"><span data-stu-id="e41df-113">Step 1: Create a Text Layout.</span></span>

<span data-ttu-id="e41df-114">Para começar, você precisará de um aplicativo que usa um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="e41df-114">To begin, you will need an application that uses an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span> <span data-ttu-id="e41df-115">Se você já tiver um aplicativo que exibe texto com um layout de texto, vá para a etapa 2.</span><span class="sxs-lookup"><span data-stu-id="e41df-115">If you already have an application that displays text with a text layout, go to Step 2.</span></span>

<span data-ttu-id="e41df-116">Para adicionar um layout de texto, você deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e41df-116">To add a text layout you must do the following:</span></span>

1. <span data-ttu-id="e41df-117">Declare um ponteiro para uma interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) como um membro da classe.</span><span class="sxs-lookup"><span data-stu-id="e41df-117">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the class.</span></span>

    ```cpp
    IDWriteTextLayout* pTextLayout_;
    ```

2. <span data-ttu-id="e41df-118">No final do método **CreateDeviceIndependentResources** , crie um objeto de interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chamando o método [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .</span><span class="sxs-lookup"><span data-stu-id="e41df-118">At the end of the **CreateDeviceIndependentResources** method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span>

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

3. <span data-ttu-id="e41df-119">Em seguida, você deve alterar a chamada para o método [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) para [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="e41df-119">Then, you must change the call to the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method to [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) as shown in the following code.</span></span>

    ```cpp
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    ```

## <a name="step-2-add-an-onclick-method"></a><span data-ttu-id="e41df-120">Etapa 2: adicionar um método OnClick.</span><span class="sxs-lookup"><span data-stu-id="e41df-120">Step 2: Add an OnClick method.</span></span>

<span data-ttu-id="e41df-121">Agora, adicione um método à classe que usará a funcionalidade de teste de clique do layout de texto.</span><span class="sxs-lookup"><span data-stu-id="e41df-121">Now add a method to the class that will use the hit testing functionality of the text layout.</span></span>

1. <span data-ttu-id="e41df-122">Declare um método **onclick** no arquivo de cabeçalho de classe.</span><span class="sxs-lookup"><span data-stu-id="e41df-122">Declare an **OnClick** method in the class header file.</span></span>

    ```cpp
    void OnClick(
        UINT x,
        UINT y
        );
    ```

2. <span data-ttu-id="e41df-123">Defina um método **onclick** no arquivo de implementação de classe.</span><span class="sxs-lookup"><span data-stu-id="e41df-123">Define an **OnClick** method in the class implementation file.</span></span>

   ```cpp
    void DemoApp::OnClick(UINT x, UINT y)
    {    
    }
    ```

## <a name="step-3-perform-hit-testing"></a><span data-ttu-id="e41df-124">Etapa 3: executar testes de clique.</span><span class="sxs-lookup"><span data-stu-id="e41df-124">Step 3: Perform Hit Testing.</span></span>

<span data-ttu-id="e41df-125">Para determinar onde o usuário clicou no layout de texto, usaremos o método [**IDWriteTextLayout:: HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) .</span><span class="sxs-lookup"><span data-stu-id="e41df-125">To determine where the user has clicked the text layout we will use the [**IDWriteTextLayout::HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method.</span></span>

<span data-ttu-id="e41df-126">Adicione o seguinte ao método **onclick** que você definiu na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="e41df-126">Add the following to the **OnClick** method that you defined in Step 2.</span></span>

1. <span data-ttu-id="e41df-127">Declare as variáveis que passaremos como parâmetros para o método.</span><span class="sxs-lookup"><span data-stu-id="e41df-127">Declare the variables we will pass as parameters to the method.</span></span>

    ```cpp
    DWRITE_HIT_TEST_METRICS hitTestMetrics;
    BOOL isTrailingHit;
    BOOL isInside; 
    ```

    <span data-ttu-id="e41df-128">O método [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) gera os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="e41df-128">The [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method outputs the following parameters.</span></span>

    | <span data-ttu-id="e41df-129">Variável</span><span class="sxs-lookup"><span data-stu-id="e41df-129">Variable</span></span>         | <span data-ttu-id="e41df-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="e41df-130">Description</span></span>                                                                                                                             |
    |------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="e41df-131">*hitTestMetrics*</span><span class="sxs-lookup"><span data-stu-id="e41df-131">*hitTestMetrics*</span></span> | <span data-ttu-id="e41df-132">A geometria está totalmente colocando o local de teste de clique.</span><span class="sxs-lookup"><span data-stu-id="e41df-132">The geometry fully enclosing the hit-test location.</span></span>                                                                                     |
    | <span data-ttu-id="e41df-133">*isinterna*</span><span class="sxs-lookup"><span data-stu-id="e41df-133">*isInside*</span></span>       | <span data-ttu-id="e41df-134">Indica se o local do teste de clique está dentro da cadeia de texto ou não.</span><span class="sxs-lookup"><span data-stu-id="e41df-134">Indicates whether the hit-test location is inside the text string or not.</span></span> <span data-ttu-id="e41df-135">Quando FALSE, a posição mais próxima da borda do texto é retornada.</span><span class="sxs-lookup"><span data-stu-id="e41df-135">When FALSE, the position nearest the text's edge is returned.</span></span> |
    | <span data-ttu-id="e41df-136">*isTrailingHit*</span><span class="sxs-lookup"><span data-stu-id="e41df-136">*isTrailingHit*</span></span>  | <span data-ttu-id="e41df-137">Indica se o local do teste de clique está no lado da esquerda ou no canto à direita do caractere.</span><span class="sxs-lookup"><span data-stu-id="e41df-137">Indicates whether the hit-test location is at the leading or the trailing side of the character.</span></span>                                        |

2. <span data-ttu-id="e41df-138">Chame o método [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) do objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="e41df-138">Call the [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method of the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

    ```cpp
    pTextLayout_->HitTestPoint(
                    (FLOAT)x, 
                    (FLOAT)y,
                    &isTrailingHit,
                    &isInside,
                    &hitTestMetrics
                    );
    ```

    <span data-ttu-id="e41df-139">O código neste exemplo passa as variáveis *x* e *y* para a posição sem qualquer modificação.</span><span class="sxs-lookup"><span data-stu-id="e41df-139">The code in this example passes the *x* and *y* variables for the position without any modification.</span></span> <span data-ttu-id="e41df-140">Isso pode ser feito neste exemplo porque o layout de texto tem o mesmo tamanho que a janela e é originado no canto superior esquerdo da janela.</span><span class="sxs-lookup"><span data-stu-id="e41df-140">This can be done in this example because the text layout is the same size as the window and originates in the upper-left corner of the window.</span></span> <span data-ttu-id="e41df-141">Se esse não for o caso, você precisaria determinar as coordenadas em relação à origem do layout do texto.</span><span class="sxs-lookup"><span data-stu-id="e41df-141">If this was not the case, you would have to determine the coordinates in relation to the origin of the text layout.</span></span>

## <a name="step-4-underline-the-clicked-text"></a><span data-ttu-id="e41df-142">Etapa 4: sublinhar o texto clicado.</span><span class="sxs-lookup"><span data-stu-id="e41df-142">Step 4: Underline the Clicked Text.</span></span>

<span data-ttu-id="e41df-143">Adicione o seguinte ao **onclick** que você definiu na etapa 2, após a chamada para o método [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) .</span><span class="sxs-lookup"><span data-stu-id="e41df-143">Add the following to the **OnClick** you defined in Step 2, after the call to the [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method.</span></span>

```cpp
if (isInside == TRUE)
{
    BOOL underline;

    pTextLayout_->GetUnderline(hitTestMetrics.textPosition, &underline);

    DWRITE_TEXT_RANGE textRange = {hitTestMetrics.textPosition, 1};

    pTextLayout_->SetUnderline(!underline, textRange);
}
```

<span data-ttu-id="e41df-144">Esse código faz o seguinte.</span><span class="sxs-lookup"><span data-stu-id="e41df-144">This code does the following.</span></span>

1. <span data-ttu-id="e41df-145">Verifica se o ponto de teste de clique estava dentro do texto usando a variável *isinterna* .</span><span class="sxs-lookup"><span data-stu-id="e41df-145">Checks if the hit-test point was inside the text using the *isInside* variable.</span></span>
2. <span data-ttu-id="e41df-146">O membro **textPosition** da estrutura *hitTestMetrics* contém o índice de base zero do caractere clicado.</span><span class="sxs-lookup"><span data-stu-id="e41df-146">The **textPosition** member of the *hitTestMetrics* structure contains the zero-based index of the character clicked.</span></span>

    <span data-ttu-id="e41df-147">Obtém o sublinhado deste caractere, passando esse valor para o método [**IDWriteTextLayout:: getabaixo**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) .</span><span class="sxs-lookup"><span data-stu-id="e41df-147">Gets the underline for this character by passing this value to the [**IDWriteTextLayout::GetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) method.</span></span>

3. <span data-ttu-id="e41df-148">Declara uma variável [**de \_ \_ intervalo de texto DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) com a posição inicial definida como **hitTestMetrics. textPosition** e um comprimento de 1.</span><span class="sxs-lookup"><span data-stu-id="e41df-148">Declares a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) variable with the start position set to **hitTestMetrics.textPosition** and a length of 1.</span></span>
4. <span data-ttu-id="e41df-149">Alterna o sublinhado usando o método [**IDWriteTextLayout::**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) ontern.</span><span class="sxs-lookup"><span data-stu-id="e41df-149">Toggles the underline by using the [**IDWriteTextLayout::SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) method.</span></span>

<span data-ttu-id="e41df-150">Depois de definir o sublinhado, Redesenhe o texto chamando o método **DrawD2DContent** da classe.</span><span class="sxs-lookup"><span data-stu-id="e41df-150">After setting the underline, redraw the text by calling the **DrawD2DContent** method of the class.</span></span>

```cpp
DrawD2DContent();
```

## <a name="step-5-handle-the-wm_lbuttondown-message"></a><span data-ttu-id="e41df-151">Etapa 5: manipular a mensagem do WM \_ LBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="e41df-151">Step 5: Handle the WM\_LBUTTONDOWN message.</span></span>

<span data-ttu-id="e41df-152">Por fim, adicione a mensagem do **WM \_ LBUTTONDOWN** ao manipulador de mensagens para seu aplicativo e chame o método **onclick** da classe.</span><span class="sxs-lookup"><span data-stu-id="e41df-152">Finally, add the **WM\_LBUTTONDOWN** message to the message handler for your application and call the **OnClick** method of the class.</span></span>

```cpp
case WM_LBUTTONDOWN:
    {
        int x = GET_X_LPARAM(lParam); 
        int y = GET_Y_LPARAM(lParam);

        pDemoApp->OnClick(x, y);
    }
    break;
```

<span data-ttu-id="e41df-153">**Obter \_ As macros x \_ lParam** e **Get \_ x \_ lParam** são declaradas no arquivo de cabeçalho windowsx. h.</span><span class="sxs-lookup"><span data-stu-id="e41df-153">**GET\_X\_LPARAM** and **GET\_X\_LPARAM** macros are declared in the windowsx.h header file.</span></span> <span data-ttu-id="e41df-154">Eles recuperam facilmente a posição x e y do clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="e41df-154">They easily retrieve the x and y position of the mouse click.</span></span>
