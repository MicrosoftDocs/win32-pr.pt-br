---
title: Como aplicar efeitos a primitivos
description: Este tópico mostra como aplicar uma série de efeitos a primitivos Direct2D e DirectWrite.
ms.assetid: 9782C22E-5D4C-494D-A0B1-19474C2CA900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aafb171c20c567d1fbd6385d23cc3b2925efc154
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366433"
---
# <a name="how-to-apply-effects-to-primitives"></a><span data-ttu-id="acb86-103">Como aplicar efeitos a primitivos</span><span class="sxs-lookup"><span data-stu-id="acb86-103">How to Apply Effects to Primitives</span></span>

<span data-ttu-id="acb86-104">Este tópico mostra como aplicar uma série de efeitos a primitivos [Direct2D](./direct2d-portal.md) e [DirectWrite](direct2d-and-directwrite.md) .</span><span class="sxs-lookup"><span data-stu-id="acb86-104">This topic shows how to apply a series of effect to [Direct2D](./direct2d-portal.md) and [DirectWrite](direct2d-and-directwrite.md) primitives.</span></span>

<span data-ttu-id="acb86-105">Você pode usar a [API de efeitos Direct2D](effects-overview.md) para aplicar grafos de efeito a primitivos renderizados pelo [Direct2D](./direct2d-portal.md) para uma imagem.</span><span class="sxs-lookup"><span data-stu-id="acb86-105">You can use the [Direct2D effects API](effects-overview.md) to apply effect graphs to primitives rendered by [Direct2D](./direct2d-portal.md) to an image.</span></span> <span data-ttu-id="acb86-106">O exemplo aqui tem dois retângulos arredondados e o texto "Direct2D".</span><span class="sxs-lookup"><span data-stu-id="acb86-106">The example here has two rounded rectangles and the text "Direct2D".</span></span> <span data-ttu-id="acb86-107">Use Direct2D para desenhar os retângulos e [DirectWrite](direct2d-and-directwrite.md) para desenhar o texto.</span><span class="sxs-lookup"><span data-stu-id="acb86-107">Use Direct2D to draw the rectangles and [DirectWrite](direct2d-and-directwrite.md) to draw the text.</span></span>

![retângulos com o texto "Direct2D" em.](images/direct2d-rounded.png)

<span data-ttu-id="acb86-109">Usando [efeitos de Direct2D](effects-overview.md), você pode fazer com que essa imagem fique parecida com a próxima imagem.</span><span class="sxs-lookup"><span data-stu-id="acb86-109">Using [Direct2D effects](effects-overview.md), you can make this image look like the next image.</span></span> <span data-ttu-id="acb86-110">Aplique o [Desfoque Gaussiano](gaussian-blur.md), a [Iluminação especular ponto](specular-lighting.md), a [composição aritmética](arithmetic-composite.md)e os efeitos [compostos](composite.md) para os primitivos 2D para criar a imagem aqui.</span><span class="sxs-lookup"><span data-stu-id="acb86-110">Apply the [Gaussian Blur](gaussian-blur.md), [Point Specular Lighting](specular-lighting.md), [Arithmetic Composite](arithmetic-composite.md), and [Composite](composite.md) effects to the 2D primitives to create the image here.</span></span>

![retângulos com o texto "Direct2D" dentro de depois que vários efeitos são aplicados.](images/direct2d-svg.png)

<span data-ttu-id="acb86-112">Depois de renderizar os retângulos e o texto em uma superfície intermediária, você pode usá-los como entrada para objetos [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) no grafo de imagem.</span><span class="sxs-lookup"><span data-stu-id="acb86-112">After you render the rectangles and text to a intermediate surface, you can use this as input for [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) objects in the image graph.</span></span>

<span data-ttu-id="acb86-113">Neste exemplo, defina a imagem original como a entrada para o [efeito de desfoque gaussiano](gaussian-blur.md) e, em seguida, defina a saída do Desfoque como a entrada para o [efeito de iluminação especular de ponto](specular-lighting.md).</span><span class="sxs-lookup"><span data-stu-id="acb86-113">In this example, set the original image as the input to the [Gaussian Blur effect](gaussian-blur.md) and then set the output of the blur as the input for the [Point Specular Lighting effect](specular-lighting.md).</span></span> <span data-ttu-id="acb86-114">O resultado desse efeito é então composto com a imagem original duas vezes para obter a imagem final que é processada para a janela.</span><span class="sxs-lookup"><span data-stu-id="acb86-114">The result of this effect is then composited with the original image twice to get the final image that is rendered to the window.</span></span>

<span data-ttu-id="acb86-115">Aqui está um diagrama do gráfico de imagem.</span><span class="sxs-lookup"><span data-stu-id="acb86-115">Here is a diagram of the image graph.</span></span>

![diagrama de gráfico de efeito.](images/effect-graph.png)

<span data-ttu-id="acb86-117">Esse grafo de efeito consiste em quatro objetos [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) , cada um representando um efeito interno diferente.</span><span class="sxs-lookup"><span data-stu-id="acb86-117">This effect graph consists of four [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) objects, each representing a different built-in effect.</span></span> <span data-ttu-id="acb86-118">Você pode criar e conectar efeitos personalizados da mesma maneira, depois de registrá-los usando [**ID1D1Factory1:: RegisterEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring).</span><span class="sxs-lookup"><span data-stu-id="acb86-118">You can create and connect custom effects in the same way, after you register them using [**ID1D1Factory1::RegisterEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring).</span></span> <span data-ttu-id="acb86-119">O código aqui cria os efeitos, define as propriedades e conecta o gráfico de efeito mostrado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="acb86-119">The code here creates the effects, sets the properties, and connects the effect graph shown earlier.</span></span>

1.  <span data-ttu-id="acb86-120">Crie o efeito de [Desfoque Gaussiano](gaussian-blur.md) usando o método [**ID2D1DeviceContext:: createeffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) e especificando o CLSID apropriado.</span><span class="sxs-lookup"><span data-stu-id="acb86-120">Create the [Gaussian blur](gaussian-blur.md) effect using the [**ID2D1DeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method and specifying the proper CLSID.</span></span> <span data-ttu-id="acb86-121">Os CLSIDs para os efeitos internos são definidos em d2d1effects. h.</span><span class="sxs-lookup"><span data-stu-id="acb86-121">The CLSIDs for the built-in effects are defined in d2d1effects.h.</span></span> <span data-ttu-id="acb86-122">Em seguida, você define o desvio padrão do Desfoque usando o método [**ID2D1Effect:: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) .</span><span class="sxs-lookup"><span data-stu-id="acb86-122">You then set the standard deviation of the blur using the [**ID2D1Effect::SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method.</span></span>

    ```C++
    // Create the Gaussian Blur Effect
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect)
        );

    // Set the blur amount
    DX::ThrowIfFailed(
        gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, sc_gaussianBlurStDev)
        );
    ```

    

    <span data-ttu-id="acb86-123">O efeito de [Desfoque Gaussiano](gaussian-blur.md) desfoca todos os canais da imagem, incluindo o canal alfa.</span><span class="sxs-lookup"><span data-stu-id="acb86-123">The [Gaussian blur](gaussian-blur.md) effect blurs all of the channels of the image, including the alpha channel.</span></span>

2.  <span data-ttu-id="acb86-124">Crie o efeito de [Iluminação especular](point-specular.md) e defina as propriedades.</span><span class="sxs-lookup"><span data-stu-id="acb86-124">Create the [specular lighting](point-specular.md) effect and set the properties.</span></span> <span data-ttu-id="acb86-125">A posição da luz é um vetor de 3 valores de ponto flutuante, portanto, você deve declará-lo como uma variável separada e passá-lo para o método [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) .</span><span class="sxs-lookup"><span data-stu-id="acb86-125">The position of the light is a vector of 3 floating point values, so you must declare it as a separate variable and pass it to the [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method.</span></span>

    ```C++
    // Create the Specular Lighting Effect
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1PointSpecular, &specularLightingEffect)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_LIGHT_POSITION, sc_specularLightPosition)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SPECULAR_EXPONENT, sc_specularExponent)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SURFACE_SCALE, sc_specularSurfaceScale)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SPECULAR_CONSTANT, sc_specularConstant)
        );
    ```

    

    <span data-ttu-id="acb86-126">O efeito de [Iluminação especular](point-specular.md) usa o canal alfa da entrada para criar um mapa de altura para a iluminação.</span><span class="sxs-lookup"><span data-stu-id="acb86-126">The [specular lighting](point-specular.md) effect uses the alpha channel of the input to create a height map for the lighting.</span></span>

3.  <span data-ttu-id="acb86-127">Há dois efeitos compostos diferentes que você pode usar o efeito [composto](composite.md) e a [composição aritmética](arithmetic-composite.md).</span><span class="sxs-lookup"><span data-stu-id="acb86-127">There are two different composite effects that you can use the [composite](composite.md) effect and the [arithmetic composite](arithmetic-composite.md).</span></span> <span data-ttu-id="acb86-128">Esse grafo de efeito usa ambos.</span><span class="sxs-lookup"><span data-stu-id="acb86-128">This effect graph uses both.</span></span>

    <span data-ttu-id="acb86-129">Crie o efeito [composto](composite.md) e defina o modo como d2d1 de \_ origem do modo composto \_ \_ \_ em, que gera a interseção entre as imagens de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="acb86-129">Create the [composite](composite.md) effect and set the mode to D2D1\_COMPOSITE\_MODE\_SOURCE\_IN, which outputs the intersection of the source and destination images.</span></span>

    <span data-ttu-id="acb86-130">O efeito [composto aritmético](arithmetic-composite.md) compõe as duas imagens de entrada com base em uma fórmula definida pelo World Wide Web CONSORTIUM (W3C) para o padrão SVG (gráfico de vetor escalonável).</span><span class="sxs-lookup"><span data-stu-id="acb86-130">The [arithmetic composite](arithmetic-composite.md) effect composes the two input images based on a formula defined by the World Wide Web Consortium (W3C) for the Scalable Vector Graphics (SVG) standard.</span></span> <span data-ttu-id="acb86-131">Crie uma composição aritmética e defina os coeficientes para a fórmula.</span><span class="sxs-lookup"><span data-stu-id="acb86-131">Create arithmetic composite and set the coefficients for the formula.</span></span>

    ```C++
    // Create the Composite Effects
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect)
        );

    DX::ThrowIfFailed(
        compositeEffect->SetValue(D2D1_COMPOSITE_PROP_MODE, D2D1_COMPOSITE_MODE_SOURCE_IN)
        );

    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1ArithmeticComposite, &m_arithmeticCompositeEffect)
        );

    DX::ThrowIfFailed(
        m_arithmeticCompositeEffect->SetValue(D2D1_ARITHMETICCOMPOSITE_PROP_COEFFICIENTS, sc_arithmeticCoefficients)
        );
    ```

    

    <span data-ttu-id="acb86-132">Os coeficientes para o efeito [composto aritmético](arithmetic-composite.md) são mostrados aqui.</span><span class="sxs-lookup"><span data-stu-id="acb86-132">The coefficients for the [arithmetic composite](arithmetic-composite.md) effect are shown here.</span></span>

    ```C++
    D2D1_VECTOR_4F sc_arithmeticCoefficients   = D2D1::Vector4F(0.0f, 1.0f, 1.0f, 0.0f);
    ```

    

    <span data-ttu-id="acb86-133">Nesse gráfico de efeito, os dois efeitos compostos levam a saída dos outros efeitos e da superfície intermediária como entradas e os compõe.</span><span class="sxs-lookup"><span data-stu-id="acb86-133">In this effect graph, both of the composite effects take the output of the other effects and the intermediate surface as inputs and composites them.</span></span>

4.  <span data-ttu-id="acb86-134">Por fim, você conecta os efeitos para formar o grafo definindo as entradas para as imagens e os bitmaps apropriados.</span><span class="sxs-lookup"><span data-stu-id="acb86-134">Finally, you connect the effects to form the graph by setting the inputs to the proper images and bitmaps.</span></span>

    <span data-ttu-id="acb86-135">O primeiro efeito, [Desfoque Gaussiano](gaussian-blur.md), recebe sua entrada da superfície intermediária para a qual você renderiza os primitivos.</span><span class="sxs-lookup"><span data-stu-id="acb86-135">The first effect, [Gaussian blur](gaussian-blur.md), receives its input from the intermediate surface that you rendered the primitives to.</span></span> <span data-ttu-id="acb86-136">Você define a entrada usando o método [**ID2D1Effect:: SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) e especifica o índice de um objeto [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) .</span><span class="sxs-lookup"><span data-stu-id="acb86-136">You set the input using the [**ID2D1Effect::SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) method and specifying the index of an [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) object.</span></span> <span data-ttu-id="acb86-137">O desfoque gaussiano e os efeitos de [Iluminação especular](point-specular.md) têm apenas uma única entrada.</span><span class="sxs-lookup"><span data-stu-id="acb86-137">The Gaussian blur and [specular lighting](point-specular.md) effects have only a single input.</span></span> <span data-ttu-id="acb86-138">O efeito de iluminação especular usa o canal alfa desfocado do Desfoque Gaussiano</span><span class="sxs-lookup"><span data-stu-id="acb86-138">The specular lighting effect uses the blurred alpha channel of the Gaussian blur</span></span>

    <span data-ttu-id="acb86-139">Os [efeitos compostos composto e](composite.md) [aritmético](arithmetic-composite.md) têm várias entradas.</span><span class="sxs-lookup"><span data-stu-id="acb86-139">The [composite](composite.md) and [arithmetic composite](arithmetic-composite.md) effects have multiple inputs.</span></span> <span data-ttu-id="acb86-140">Para garantir que as imagens sejam colocadas juntas na ordem correta, você deve especificar o índice correto para cada imagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="acb86-140">To make sure the images are put together in the right order, you must specify the correct index for each input image.</span></span>

    ```C++
    // Connect the graph.
    // Apply a blur effect to the original image.
    gaussianBlurEffect->SetInput(0, m_inputImage.Get());

    // Apply a specular lighting effect to the result.
    specularLightingEffect->SetInputEffect(0, gaussianBlurEffect.Get());

    // Compose the original bitmap under the output from lighting and blur.
    compositeEffect->SetInput(0, m_inputImage.Get());
    compositeEffect->SetInputEffect(1, specularLightingEffect.Get());

    // Compose the original bitmap under the output from lighting and blur.
    m_arithmeticCompositeEffect->SetInput(0, m_inputImage.Get());
    m_arithmeticCompositeEffect->SetInputEffect(1, compositeEffect.Get());
    ```

    

5.  <span data-ttu-id="acb86-141">Passe o objeto de efeito de [composição aritmético](arithmetic-composite.md) para o método [**ID2DDeviceContext::D RawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) e ele processa e desenha a saída do grafo.</span><span class="sxs-lookup"><span data-stu-id="acb86-141">Pass the [arithmetic composite](arithmetic-composite.md) effect object into the [**ID2DDeviceContext::DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) method and it processes and draws the output of the graph.</span></span>

    ```C++
        // Draw the output of the effects graph.
        m_d2dContext->DrawImage(
            m_arithmeticCompositeEffect.Get(),
            D2D1::Point2F(
                (size.width - sc_inputBitmapSize.width) / 2,
                (size.height - sc_inputBitmapSize.height) / 2 + sc_offset
                )
            );
    ```

    

 

 