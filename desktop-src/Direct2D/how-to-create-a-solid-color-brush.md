---
title: Como criar um pincel de cor sólida
description: Mostra como criar um pincel de cor sólida usando Direct2D.
ms.assetid: 70700b82-2294-46be-b1c0-fc89def441e2
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: bc6fbf5df42386f5e0e5a843a1906d36d4fc8c71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917386"
---
# <a name="how-to-create-a-solid-color-brush"></a><span data-ttu-id="03a28-103">Como criar um pincel de cor sólida</span><span class="sxs-lookup"><span data-stu-id="03a28-103">How to Create a Solid Color Brush</span></span>

<span data-ttu-id="03a28-104">Para criar um pincel de cor sólida, use o método [**ID2DRenderTarget:: CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) e especifique a cor com a qual você deseja pintar.</span><span class="sxs-lookup"><span data-stu-id="03a28-104">To create a solid color brush, use the [**ID2DRenderTarget::CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method and specify the color with which you want to paint.</span></span> <span data-ttu-id="03a28-105">Algumas das sobrecargas de **CreateSolidColorBrush** também permitem que você especifique a opacidade do pincel.</span><span class="sxs-lookup"><span data-stu-id="03a28-105">Some of the **CreateSolidColorBrush** overloads also enable you to specify the opacity of the brush.</span></span>

<span data-ttu-id="03a28-106">O código a seguir mostra como criar um pincel amarelo-verde sólido para preencher um quadrado e um pincel preto sólido para desenhar a estrutura de tópicos do quadrado.</span><span class="sxs-lookup"><span data-stu-id="03a28-106">The following code shows how to create a solid yellow-green brush to fill a square, and a solid black brush to draw the outline of the square.</span></span> <span data-ttu-id="03a28-107">O código produz a saída mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="03a28-107">The code produces the output shown in the following illustration.</span></span>

![ilustração de um retângulo preenchido com uma cor verde amarela sólida](images/brushes-ovw-solidcolor.png)

1.  <span data-ttu-id="03a28-109">Declare dois ponteiros [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) : um para pintar em preto e outro para pintar verde amarelo.</span><span class="sxs-lookup"><span data-stu-id="03a28-109">Declare two [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) pointers: one for painting black and one for painting yellow green.</span></span>
    ```C++
        ID2D1SolidColorBrush *m_pBlackBrush;
        ID2D1SolidColorBrush *m_pYellowGreenBrush;
    ```

    

2.  <span data-ttu-id="03a28-110">Chame o método [**CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) para criar os pincéis:</span><span class="sxs-lookup"><span data-stu-id="03a28-110">Call the [**CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method to create the brushes:</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateSolidColorBrush(
            D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
            &m_pBlackBrush
            );
    }

    // Create a solid color brush with its rgb value 0x9ACD32.
    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateSolidColorBrush(
            D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
            &m_pYellowGreenBrush
            );
    }
    ```

    

3.  <span data-ttu-id="03a28-111">Chame o método [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) para pintar o interior do retângulo com o pincel verde amarelo e o método [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) para pintar o contorno do retângulo com o pincel preto:</span><span class="sxs-lookup"><span data-stu-id="03a28-111">Call the [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) method to paint the interior of the rectangle with the yellow green brush and the [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method to paint the outline of the rectangle with the black brush:</span></span>
    ```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pYellowGreenBrush);
    m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="03a28-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="03a28-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03a28-113">Referência de Direct2D</span><span class="sxs-lookup"><span data-stu-id="03a28-113">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 