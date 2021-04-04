---
title: Efeitos (Direct2D)
description: Uma visão geral dos efeitos de Direct2D.
ms.assetid: 1446BDA9-AD4C-472C-8F1D-82ABC1880E13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd29a4b2968e91bd0d516a74ec01538f69821bb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007915"
---
# <a name="effects"></a><span data-ttu-id="334dd-103">Efeitos</span><span class="sxs-lookup"><span data-stu-id="334dd-103">Effects</span></span>

## <a name="what-are-direct2d-effects"></a><span data-ttu-id="334dd-104">O que são efeitos de Direct2D?</span><span class="sxs-lookup"><span data-stu-id="334dd-104">What are Direct2D effects?</span></span>

<span data-ttu-id="334dd-105">Você pode usar Direct2D para aplicar um ou mais efeitos de alta qualidade a uma imagem ou a um conjunto de imagens.</span><span class="sxs-lookup"><span data-stu-id="334dd-105">You can use Direct2D to apply one or more high quality effects to an image or a set of images.</span></span> <span data-ttu-id="334dd-106">As APIs de efeitos são criadas no [Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features) e aproveitam os recursos de GPU para o processamento de imagens.</span><span class="sxs-lookup"><span data-stu-id="334dd-106">The effects APIs are built on [Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features) and take advantage of GPU features for image processing.</span></span> <span data-ttu-id="334dd-107">Você pode encadear efeitos em um grafo de efeito e compor ou misturar a saída de efeitos.</span><span class="sxs-lookup"><span data-stu-id="334dd-107">You can chain effects in an effect graph and compose or blend the output of effects.</span></span>

<span data-ttu-id="334dd-108">Um efeito de Direct2D executa uma tarefa de geração de imagens, como alterar o brilho, saturação uma imagem ou criar uma sombra.</span><span class="sxs-lookup"><span data-stu-id="334dd-108">A Direct2D effect performs an imaging task, like changing brightness, de-saturating an image, or creating a drop shadow.</span></span> <span data-ttu-id="334dd-109">Os efeitos podem aceitar zero ou mais imagens de entrada, expor várias propriedades que controlam sua operação e gerar uma única imagem de saída.</span><span class="sxs-lookup"><span data-stu-id="334dd-109">Effects can accept zero or more input images, expose multiple properties that control their operation, and generate a single output image.</span></span>

<span data-ttu-id="334dd-110">Cada efeito cria um grafo de transformação interno composto por transformações individuais.</span><span class="sxs-lookup"><span data-stu-id="334dd-110">Each effect creates an internal transform graph made up of individual transforms.</span></span> <span data-ttu-id="334dd-111">Cada transformação representa uma única operação de imagem.</span><span class="sxs-lookup"><span data-stu-id="334dd-111">Each transform represents a single image operation.</span></span> <span data-ttu-id="334dd-112">A principal finalidade de uma transformação é alojar os sombreadores que são executados para cada pixel de saída.</span><span class="sxs-lookup"><span data-stu-id="334dd-112">The main purpose of a transform is to house the shaders that are executed for each output pixel.</span></span> <span data-ttu-id="334dd-113">Esses sombreadores podem incluir sombreadores de pixel, sombreadores de vértice, o estágio de mistura de uma GPU e sombreadores de computação.</span><span class="sxs-lookup"><span data-stu-id="334dd-113">These shaders can include pixel shaders, vertex shaders, the blend stage of a GPU, and compute shaders.</span></span>

<span data-ttu-id="334dd-114">Os [efeitos internos](built-in-effects.md) [Direct2D](./direct2d-portal.md) e os efeitos personalizados que você pode fazer usando a [API de efeitos personalizados](custom-effects.md) funcionam dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="334dd-114">Both the [Direct2D](./direct2d-portal.md) [built-in effects](built-in-effects.md) and custom effects you can make using the [custom effects API](custom-effects.md) work this way.</span></span>

<span data-ttu-id="334dd-115">Há uma variedade de [efeitos internos](built-in-effects.md) de categorias como aquelas aqui.</span><span class="sxs-lookup"><span data-stu-id="334dd-115">There are a range of [built-in effects](built-in-effects.md) from categories like the ones here.</span></span> <span data-ttu-id="334dd-116">Consulte a seção de [efeitos internos](built-in-effects.md) para obter uma lista completa.</span><span class="sxs-lookup"><span data-stu-id="334dd-116">See the [Built-in Effects](built-in-effects.md) section for a full list.</span></span>

-   [<span data-ttu-id="334dd-117">Filtragem</span><span class="sxs-lookup"><span data-stu-id="334dd-117">Filtering</span></span>](built-in-effects.md)
-   [<span data-ttu-id="334dd-118">Composição e mesclagem</span><span class="sxs-lookup"><span data-stu-id="334dd-118">Composition and Blending</span></span>](built-in-effects.md)
-   [<span data-ttu-id="334dd-119">Transparência</span><span class="sxs-lookup"><span data-stu-id="334dd-119">Transparency</span></span>](built-in-effects.md)
-   [<span data-ttu-id="334dd-120">Cor</span><span class="sxs-lookup"><span data-stu-id="334dd-120">Color</span></span>](built-in-effects.md)
-   [<span data-ttu-id="334dd-121">Iluminação e estilização</span><span class="sxs-lookup"><span data-stu-id="334dd-121">Lighting and Stylizing</span></span>](built-in-effects.md)
-   [<span data-ttu-id="334dd-122">Transformando e dimensionando</span><span class="sxs-lookup"><span data-stu-id="334dd-122">Transforming and Scaling</span></span>](built-in-effects.md)
-   [<span data-ttu-id="334dd-123">Fontes</span><span class="sxs-lookup"><span data-stu-id="334dd-123">Sources</span></span>](built-in-effects.md)

<span data-ttu-id="334dd-124">Você pode aplicar efeitos a qualquer bitmap, incluindo: imagens carregadas pelo [Windows Imaging Component (WIC)](/windows/desktop/wic/-wic-api), primitivas desenhadas por [Direct2D](./direct2d-portal.md), texto de [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)ou cenas renderizadas pelo [Direct3D](/windows/desktop/direct3d10/d3d10-graphics).</span><span class="sxs-lookup"><span data-stu-id="334dd-124">You can apply effects to any bitmap, including: images loaded by the [Windows Imaging Component (WIC)](/windows/desktop/wic/-wic-api), primitives drawn by [Direct2D](./direct2d-portal.md), text from [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal), or scenes rendered by [Direct3D](/windows/desktop/direct3d10/d3d10-graphics).</span></span>

<span data-ttu-id="334dd-125">Com efeitos Direct2Ds, você pode escrever seus próprios efeitos que podem ser usados para seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="334dd-125">With Direct2D effects you can write your own effects that you can use for your applications.</span></span> <span data-ttu-id="334dd-126">Uma estrutura de efeito personalizada permite que você use recursos de GPU, como sombreadores de pixel, sombreadores de vértice e a unidade de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="334dd-126">A custom effect framework allows you to use GPU features such as pixel shaders, vertex shaders, and the blending unit.</span></span> <span data-ttu-id="334dd-127">Você também pode incluir outros efeitos internos ou personalizados em seu efeito personalizado.</span><span class="sxs-lookup"><span data-stu-id="334dd-127">You can also include other built-in or custom effects in your custom effect.</span></span> <span data-ttu-id="334dd-128">A estrutura para criar efeitos personalizados é a mesma que foi usada para criar os efeitos internos do [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="334dd-128">The framework for building custom effects is the same one that was used to create the built-in effects of [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="334dd-129">A [API do autor do efeito Direct2D](custom-effects.md) fornece um conjunto de interfaces para criar e registrar efeitos.</span><span class="sxs-lookup"><span data-stu-id="334dd-129">The [Direct2D effect author API](custom-effects.md) provides a set of interfaces to create and register effects.</span></span>

### <a name="more-effects-topics"></a><span data-ttu-id="334dd-130">Tópicos de mais efeitos</span><span class="sxs-lookup"><span data-stu-id="334dd-130">More effects topics</span></span>

<span data-ttu-id="334dd-131">O restante deste tópico explica os conceitos básicos de efeitos de Direct2D, como a aplicação de um efeito a uma imagem.</span><span class="sxs-lookup"><span data-stu-id="334dd-131">The rest of this topic explains the basics of Direct2D effects, like applying an effect to an image.</span></span> <span data-ttu-id="334dd-132">A tabela aqui contém links para tópicos adicionais sobre efeitos.</span><span class="sxs-lookup"><span data-stu-id="334dd-132">The table here has links to additional topics about effects.</span></span>

| <span data-ttu-id="334dd-133">Tópico</span><span class="sxs-lookup"><span data-stu-id="334dd-133">Topic</span></span>                                                                                                                    | <span data-ttu-id="334dd-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="334dd-134">Description</span></span>                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="334dd-135">Vinculação de Sombreador de Efeito</span><span class="sxs-lookup"><span data-stu-id="334dd-135">Effect Shader Linking</span></span>](effect-shader-linking.md)<br/>                                                            | <span data-ttu-id="334dd-136">O Direct2D usa uma otimização chamada vinculação de sombreador de efeito que combina vários efeitos que a renderização de gráfico passa em uma única passagem.</span><span class="sxs-lookup"><span data-stu-id="334dd-136">Direct2D uses an optimization called effect shader linking which combines multiple effect graph rendering passes into a single pass.</span></span><br/>                                               |
| [<span data-ttu-id="334dd-137">Efeitos personalizados</span><span class="sxs-lookup"><span data-stu-id="334dd-137">Custom effects</span></span>](custom-effects.md)<br/>                                                                          | <span data-ttu-id="334dd-138">Mostra como escrever seus próprios efeitos personalizados usando HLSL padrão.</span><span class="sxs-lookup"><span data-stu-id="334dd-138">Shows you how to write your own custom effects using standard HLSL.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="334dd-139">Como carregar uma imagem em efeitos de Direct2D usando o fileescolhidor</span><span class="sxs-lookup"><span data-stu-id="334dd-139">How to load an image into Direct2D Effects using the FilePicker</span></span>](load-a-id2d1image-using-the-filepicker.md)<br/> | <span data-ttu-id="334dd-140">Mostra como usar o [**Windows:: Storage::P ickers:: FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) para carregar uma imagem em efeitos Direct2D.</span><span class="sxs-lookup"><span data-stu-id="334dd-140">Shows how to use the [**Windows::Storage::Pickers::FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) to load an image into Direct2D effects.</span></span><br/>                                      |
| [<span data-ttu-id="334dd-141">Como salvar o conteúdo do Direct2D em um arquivo de imagem</span><span class="sxs-lookup"><span data-stu-id="334dd-141">How to save Direct2D content to an image file</span></span>](save-direct2d-content-to-an-image-file.md)<br/>                   | <span data-ttu-id="334dd-142">Este tópico mostra como usar o [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) para salvar o conteúdo na forma de um [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) em um arquivo de imagem codificado, como JPEG.</span><span class="sxs-lookup"><span data-stu-id="334dd-142">This topic shows how to use [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) to save content in the form of an [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) to an encoded image file such as JPEG.</span></span><br/> |
| [<span data-ttu-id="334dd-143">Como aplicar efeitos a primitivos</span><span class="sxs-lookup"><span data-stu-id="334dd-143">How to Apply Effects to Primitives</span></span>](how-to-apply-effects-to-primitives.md)<br/>                                  | <span data-ttu-id="334dd-144">Este tópico mostra como aplicar uma série de efeitos a primitivos [Direct2D](./direct2d-portal.md) e [DirectWrite](direct2d-and-directwrite.md) .</span><span class="sxs-lookup"><span data-stu-id="334dd-144">This topic shows how to apply a series of effect to [Direct2D](./direct2d-portal.md) and [DirectWrite](direct2d-and-directwrite.md) primitives.</span></span><br/>                           |
| [<span data-ttu-id="334dd-145">Controlando a precisão e recorte numérico em grafos de efeito</span><span class="sxs-lookup"><span data-stu-id="334dd-145">Controlling Precision and Numerical Clipping in Effect Graphs</span></span>](precision-and-clipping-in-effect-graphs.md)<br/>  | <span data-ttu-id="334dd-146">Os aplicativos que processam efeitos usando Direct2D devem tomar cuidado para atingir o nível desejado de qualidade e previsibilidade em relação à precisão numérica.</span><span class="sxs-lookup"><span data-stu-id="334dd-146">Applications that render effects using Direct2D must take care to achieve the desired level of quality and predictability with respect to numerical precision.</span></span> <br/>                    |

## <a name="applying-an-effect-to-an-image"></a><span data-ttu-id="334dd-147">Aplicando um efeito a uma imagem</span><span class="sxs-lookup"><span data-stu-id="334dd-147">Applying an effect to an image</span></span>

<span data-ttu-id="334dd-148">Você pode usar a API de efeitos Direct2D para aplicar transformações a imagens.</span><span class="sxs-lookup"><span data-stu-id="334dd-148">You can use the Direct2D effects API to apply transforms to images.</span></span>

> [!Note]  
> <span data-ttu-id="334dd-149">Este exemplo supõe que você já tenha objetos [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) e [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) criados.</span><span class="sxs-lookup"><span data-stu-id="334dd-149">This example assumes that you already have [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) and [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) objects created.</span></span> <span data-ttu-id="334dd-150">Para obter mais informações sobre como criar esses objetos, consulte [como carregar uma imagem em efeitos de Direct2D usando o Fileseparar e os](load-a-id2d1image-using-the-filepicker.md) [dispositivos e contextos de dispositivo](devices-and-device-contexts.md).</span><span class="sxs-lookup"><span data-stu-id="334dd-150">For more information on creating these objects see [How to load an image into Direct2D effects using the FilePicker](load-a-id2d1image-using-the-filepicker.md) and [Devices and Device Contexts](devices-and-device-contexts.md).</span></span>

 

1.  <span data-ttu-id="334dd-151">Declare uma variável [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) e, em seguida, crie um efeito de [origem de bitmap](bitmap-source.md) usando o método [**ID2DDeviceContext:: createeffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) .</span><span class="sxs-lookup"><span data-stu-id="334dd-151">Declare an [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) variable and then create a [bitmap source](bitmap-source.md) effect using the [**ID2DDeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method.</span></span>

    ```C++
        ComPtr<ID2D1Effect> bitmapSourceEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect));
    ```

    

2.  <span data-ttu-id="334dd-152">Defina a Propriedade BitmapSource para a origem do bitmap do WIC usando o [**ID2D1Effect:: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)).</span><span class="sxs-lookup"><span data-stu-id="334dd-152">Set the BitmapSource property to the WIC bitmap source using the [**ID2D1Effect::SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)).</span></span>

    ```C++
            DX::ThrowIfFailed(m_bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, m_wicBitmapSource.Get()));
    ```

    

3.  <span data-ttu-id="334dd-153">Declare uma variável [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) e crie o efeito de [Desfoque Gaussiano](gaussian-blur.md) .</span><span class="sxs-lookup"><span data-stu-id="334dd-153">Declare an [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) variable and then create the [gaussian blur](gaussian-blur.md) effect.</span></span>

    ```C++
        ComPtr<ID2D1Effect> gaussianBlurEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect));
    ```

    

4.  <span data-ttu-id="334dd-154">Defina a entrada para receber a imagem do efeito de origem do bitmap.</span><span class="sxs-lookup"><span data-stu-id="334dd-154">Set the input to receive the image from the bitmap source effect.</span></span> <span data-ttu-id="334dd-155">Defina o valor de desfoque o método [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) e a propriedade de desvio padrão.</span><span class="sxs-lookup"><span data-stu-id="334dd-155">Set the blur amount the [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method and the standard deviation property.</span></span>

    ```C++
        gaussianBlurEffect->SetInputEffect(0, bitmapSourceEffect.Get());

        DX::ThrowIfFailed(gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 6.0f));
    ```

    

5.  <span data-ttu-id="334dd-156">Use o contexto do dispositivo para desenhar a saída da imagem resultante.</span><span class="sxs-lookup"><span data-stu-id="334dd-156">Use the device context to draw the resulting image output.</span></span>

    ```C++
        m_d2dContext->BeginDraw();

        m_d2dContext->Clear(D2D1::ColorF(D2D1::ColorF::CornflowerBlue));

        // Draw the blurred image.
        m_d2dContext->DrawImage(gaussianBlurEffect.Get());

        HRESULT hr = m_d2dContext->EndDraw();
    ```

    

    <span data-ttu-id="334dd-157">O método [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) deve ser chamado entre as chamadas [**ID2DDeviceContext:: BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) e [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) , como outras operações de renderização Direct2D.</span><span class="sxs-lookup"><span data-stu-id="334dd-157">The [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) method must be called between the [**ID2DDeviceContext::BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) and [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) calls like other Direct2D render operations.</span></span> <span data-ttu-id="334dd-158">O **DrawImage** pode pegar uma imagem ou a saída de um efeito e renderizá-la na superfície de destino.</span><span class="sxs-lookup"><span data-stu-id="334dd-158">**DrawImage** can take an image or the output of an effect and render it to the target surface.</span></span>

## <a name="spatial-transforms"></a><span data-ttu-id="334dd-159">Transformações espaciais</span><span class="sxs-lookup"><span data-stu-id="334dd-159">Spatial Transforms</span></span>

<span data-ttu-id="334dd-160">O Direct2D fornece efeitos internos que podem transformar imagens em espaço 2D e 3D, bem como no dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="334dd-160">Direct2D provides built-in effects that can transform images in 2D and 3D space, as well as scaling.</span></span> <span data-ttu-id="334dd-161">Os efeitos de escala e transformação oferecem vários níveis de qualidade, como: vizinho mais próximo, linear, cúbico, com várias amostras lineares, anisotropic e cúbico de alta qualidade.</span><span class="sxs-lookup"><span data-stu-id="334dd-161">The scale and transform effects offer various quality levels like: nearest neighbor, linear, cubic, multi-sample linear, anisotropic, and high quality cubic.</span></span>

> [!Note]  
> <span data-ttu-id="334dd-162">O modo anisotropic gera mipmaps ao dimensionar, no entanto, se você definir a propriedade **armazenada em cache** como true nos efeitos que são inseridos na transformação, o mipmaps não será gerado toda vez para imagens suficientemente pequenas.</span><span class="sxs-lookup"><span data-stu-id="334dd-162">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to the transform the mipmaps won't be generated every time for sufficiently small images.</span></span>

 


```C++
ComPtr<ID2D1Effect> affineTransformEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect));

affineTransformEffect->SetInput(0, bitmap.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F(0.9f, -0.1f,  0.1f, 0.9f, 8.0f, 45.0f);
DX::ThrowIfFailed(affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(affineTransformEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="334dd-163">Esse uso do efeito de transformação afim 2D gira o bitmap levemente no sentido anti-horário.</span><span class="sxs-lookup"><span data-stu-id="334dd-163">This use of the 2D affine transform effect rotates the bitmap counterclockwise slightly.</span></span>



| <span data-ttu-id="334dd-164">Antes</span><span class="sxs-lookup"><span data-stu-id="334dd-164">Before</span></span>                                                            |
|-------------------------------------------------------------------|
| ![efeito de afinidade 2D antes da imagem.](images/default-before.jpg)      |
| <span data-ttu-id="334dd-166">After (após)</span><span class="sxs-lookup"><span data-stu-id="334dd-166">After</span></span>                                                             |
| ![efeito de afinidade 2D após imagem.](images/21-2daffinetransform.png) |



 

## <a name="compositing-images"></a><span data-ttu-id="334dd-168">Composição de imagens</span><span class="sxs-lookup"><span data-stu-id="334dd-168">Compositing images</span></span>

<span data-ttu-id="334dd-169">Alguns efeitos aceitam várias entradas e as compõem em uma imagem resultante.</span><span class="sxs-lookup"><span data-stu-id="334dd-169">Some effects accept multiple inputs and composite them into one resulting image.</span></span>

<span data-ttu-id="334dd-170">Os efeitos compostos compostos e aritméticos internos fornecem vários modos, para obter mais informações, consulte o tópico [composto](composite.md) .</span><span class="sxs-lookup"><span data-stu-id="334dd-170">The built-in composite and arithmetic composite effects provide various modes, for more info see the [composite](composite.md) topic.</span></span> <span data-ttu-id="334dd-171">O efeito de [Blend](blend.md) tem uma variedade de modos acelerados de GPU disponíveis.</span><span class="sxs-lookup"><span data-stu-id="334dd-171">The [blend](blend.md) effect has a variety of GPU accelerated modes available.</span></span>


```C++
ComPtr<ID2D1Effect> compositeEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect));

compositeEffect->SetInput(0, bitmap.Get());
compositeEffect->SetInput(1, bitmapTwo.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="334dd-172">O efeito composto combina imagens de várias maneiras diferentes de acordo com o modo especificado.</span><span class="sxs-lookup"><span data-stu-id="334dd-172">The composite effect combines images in various different ways according to the mode you specify.</span></span>

## <a name="pixel-adjustments"></a><span data-ttu-id="334dd-173">Ajustes de pixel</span><span class="sxs-lookup"><span data-stu-id="334dd-173">Pixel adjustments</span></span>

<span data-ttu-id="334dd-174">Há alguns efeitos Direct2Ds internos que permitem alterar os dados de pixel.</span><span class="sxs-lookup"><span data-stu-id="334dd-174">There are a few built-in Direct2D effects that allow you to alter the pixel data.</span></span> <span data-ttu-id="334dd-175">Por exemplo, o efeito de matriz de cor pode ser usado para alterar a cor de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="334dd-175">For example, the color matrix effect can be used to change the color of an image.</span></span>


```C++
ComPtr<ID2D1Effect> colorMatrixEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1ColorMatrix, &colorMatrixEffect));

colorMatrixEffect->SetInput(0, bitmap.Get());

D2D1_MATRIX_5X4_F matrix = D2D1::Matrix5x4F(0, 0, 1, 0,   0, 1, 0, 0,   1, 0, 0, 0,   0, 0, 0, 1,   0, 0, 0, 0);
DX::ThrowIfFailed(colorMatrixEffect->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, matrix));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(colorMatrixEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="334dd-176">Esse código usa a imagem e altera a cor, conforme mostrado nas imagens de exemplo aqui.</span><span class="sxs-lookup"><span data-stu-id="334dd-176">This code takes the image and alters the color as shown in the example images here.</span></span>



| <span data-ttu-id="334dd-177">Antes</span><span class="sxs-lookup"><span data-stu-id="334dd-177">Before</span></span>                                                          |
|-----------------------------------------------------------------|
| ![efeito de matriz de cor antes da imagem.](images/default-before.jpg) |
| <span data-ttu-id="334dd-179">After (após)</span><span class="sxs-lookup"><span data-stu-id="334dd-179">After</span></span>                                                           |
| ![efeito da matriz de cores após a imagem.](images/15-colormatrix.png)  |



 

<span data-ttu-id="334dd-181">Consulte a seção de [efeitos internos de cor](how-to-create-a-solid-color-brush.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="334dd-181">See the [color built-in effects](how-to-create-a-solid-color-brush.md) section for more info.</span></span>

## <a name="building-effect-graphs"></a><span data-ttu-id="334dd-182">Criando grafos de efeito</span><span class="sxs-lookup"><span data-stu-id="334dd-182">Building effect graphs</span></span>

<span data-ttu-id="334dd-183">Você pode encadear efeitos em conjunto para transformar imagens.</span><span class="sxs-lookup"><span data-stu-id="334dd-183">You can chain effects together to transform images.</span></span> <span data-ttu-id="334dd-184">Por exemplo, o código aqui aplica uma sombra e uma transformação 2D e, em seguida, compõe os resultados juntos.</span><span class="sxs-lookup"><span data-stu-id="334dd-184">For example, the code here applies a shadow and a 2D transform, then composites the results together.</span></span>


```C++
ComPtr<ID2D1Effect> shadowEffect;
ComPtr<ID2D1Effect> affineTransformEffect;
ComPtr<ID2D1Effect> compositeEffect;

DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Shadow, &shadowEffect));
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect));
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect));

shadowEffect->SetInput(0, bitmap.Get());
affineTransformEffect->SetInputEffect(0, shadowEffect.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F::Translation(20, 20));

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

compositeEffect->SetInputEffect(0, affineTransformEffect.Get());
compositeEffect->SetInput(1, bitmap.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="334dd-185">Este é o conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="334dd-185">Here is the result.</span></span>

![saída de efeito de sombra.](images/effect-overview-shadow.png)

<span data-ttu-id="334dd-187">Os efeitos tomam objetos [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) como entrada.</span><span class="sxs-lookup"><span data-stu-id="334dd-187">Effects take [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) objects as input.</span></span> <span data-ttu-id="334dd-188">Você pode usar um [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) porque a interface é derivada de **ID2D1Image**.</span><span class="sxs-lookup"><span data-stu-id="334dd-188">You can use an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) because the interface is derived from **ID2D1Image**.</span></span> <span data-ttu-id="334dd-189">Você também pode usar a [**saída ID2D1Effect::**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput) getpara obter a saída de um objeto [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) como um **ID2D1Image** ou usar o método **SetInputEffect** , que converte a saída para você.</span><span class="sxs-lookup"><span data-stu-id="334dd-189">You can also use the [**ID2D1Effect::GetOutput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput) to get the output of an [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) object as an **ID2D1Image** or use the **SetInputEffect** method, which converts the output for you.</span></span> <span data-ttu-id="334dd-190">Na maioria dos casos, um grafo de efeito consiste em objetos **ID2D1Effect** encadeados diretamente, o que facilita a aplicação de vários efeitos a uma imagem para criar visuais atraentes.</span><span class="sxs-lookup"><span data-stu-id="334dd-190">In most cases an effect graph consists of **ID2D1Effect** objects directly chained together, which makes it easy to apply multiple effects to an image to create compelling visuals.</span></span>

<span data-ttu-id="334dd-191">Consulte [como aplicar efeitos a primitivos](how-to-apply-effects-to-primitives.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="334dd-191">See [How to apply effects to primitives](how-to-apply-effects-to-primitives.md) for more info.</span></span>

## <a name="related-topics"></a><span data-ttu-id="334dd-192">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="334dd-192">Related topics</span></span>

[<span data-ttu-id="334dd-193">Exemplo de efeitos de imagem básica do Direct2D</span><span class="sxs-lookup"><span data-stu-id="334dd-193">Direct2D basic image effects sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20basic%20image%20effects%20sample)

[<span data-ttu-id="334dd-194">Efeitos internos</span><span class="sxs-lookup"><span data-stu-id="334dd-194">Built-in Effects</span></span>](built-in-effects.md)