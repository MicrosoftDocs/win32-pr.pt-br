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
# <a name="effects"></a>Efeitos

## <a name="what-are-direct2d-effects"></a>O que são efeitos de Direct2D?

Você pode usar Direct2D para aplicar um ou mais efeitos de alta qualidade a uma imagem ou a um conjunto de imagens. As APIs de efeitos são criadas no [Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features) e aproveitam os recursos de GPU para o processamento de imagens. Você pode encadear efeitos em um grafo de efeito e compor ou misturar a saída de efeitos.

Um efeito de Direct2D executa uma tarefa de geração de imagens, como alterar o brilho, saturação uma imagem ou criar uma sombra. Os efeitos podem aceitar zero ou mais imagens de entrada, expor várias propriedades que controlam sua operação e gerar uma única imagem de saída.

Cada efeito cria um grafo de transformação interno composto por transformações individuais. Cada transformação representa uma única operação de imagem. A principal finalidade de uma transformação é alojar os sombreadores que são executados para cada pixel de saída. Esses sombreadores podem incluir sombreadores de pixel, sombreadores de vértice, o estágio de mistura de uma GPU e sombreadores de computação.

Os [efeitos internos](built-in-effects.md) [Direct2D](./direct2d-portal.md) e os efeitos personalizados que você pode fazer usando a [API de efeitos personalizados](custom-effects.md) funcionam dessa maneira.

Há uma variedade de [efeitos internos](built-in-effects.md) de categorias como aquelas aqui. Consulte a seção de [efeitos internos](built-in-effects.md) para obter uma lista completa.

-   [Filtragem](built-in-effects.md)
-   [Composição e mesclagem](built-in-effects.md)
-   [Transparência](built-in-effects.md)
-   [Cor](built-in-effects.md)
-   [Iluminação e estilização](built-in-effects.md)
-   [Transformando e dimensionando](built-in-effects.md)
-   [Fontes](built-in-effects.md)

Você pode aplicar efeitos a qualquer bitmap, incluindo: imagens carregadas pelo [Windows Imaging Component (WIC)](/windows/desktop/wic/-wic-api), primitivas desenhadas por [Direct2D](./direct2d-portal.md), texto de [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)ou cenas renderizadas pelo [Direct3D](/windows/desktop/direct3d10/d3d10-graphics).

Com efeitos Direct2Ds, você pode escrever seus próprios efeitos que podem ser usados para seus aplicativos. Uma estrutura de efeito personalizada permite que você use recursos de GPU, como sombreadores de pixel, sombreadores de vértice e a unidade de mesclagem. Você também pode incluir outros efeitos internos ou personalizados em seu efeito personalizado. A estrutura para criar efeitos personalizados é a mesma que foi usada para criar os efeitos internos do [Direct2D](./direct2d-portal.md). A [API do autor do efeito Direct2D](custom-effects.md) fornece um conjunto de interfaces para criar e registrar efeitos.

### <a name="more-effects-topics"></a>Tópicos de mais efeitos

O restante deste tópico explica os conceitos básicos de efeitos de Direct2D, como a aplicação de um efeito a uma imagem. A tabela aqui contém links para tópicos adicionais sobre efeitos.

| Tópico                                                                                                                    | Descrição                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Vinculação de Sombreador de Efeito](effect-shader-linking.md)<br/>                                                            | O Direct2D usa uma otimização chamada vinculação de sombreador de efeito que combina vários efeitos que a renderização de gráfico passa em uma única passagem.<br/>                                               |
| [Efeitos personalizados](custom-effects.md)<br/>                                                                          | Mostra como escrever seus próprios efeitos personalizados usando HLSL padrão.<br/>                                                                                                                |
| [Como carregar uma imagem em efeitos de Direct2D usando o fileescolhidor](load-a-id2d1image-using-the-filepicker.md)<br/> | Mostra como usar o [**Windows:: Storage::P ickers:: FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) para carregar uma imagem em efeitos Direct2D.<br/>                                      |
| [Como salvar o conteúdo do Direct2D em um arquivo de imagem](save-direct2d-content-to-an-image-file.md)<br/>                   | Este tópico mostra como usar o [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) para salvar o conteúdo na forma de um [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) em um arquivo de imagem codificado, como JPEG.<br/> |
| [Como aplicar efeitos a primitivos](how-to-apply-effects-to-primitives.md)<br/>                                  | Este tópico mostra como aplicar uma série de efeitos a primitivos [Direct2D](./direct2d-portal.md) e [DirectWrite](direct2d-and-directwrite.md) .<br/>                           |
| [Controlando a precisão e recorte numérico em grafos de efeito](precision-and-clipping-in-effect-graphs.md)<br/>  | Os aplicativos que processam efeitos usando Direct2D devem tomar cuidado para atingir o nível desejado de qualidade e previsibilidade em relação à precisão numérica. <br/>                    |

## <a name="applying-an-effect-to-an-image"></a>Aplicando um efeito a uma imagem

Você pode usar a API de efeitos Direct2D para aplicar transformações a imagens.

> [!Note]  
> Este exemplo supõe que você já tenha objetos [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) e [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) criados. Para obter mais informações sobre como criar esses objetos, consulte [como carregar uma imagem em efeitos de Direct2D usando o Fileseparar e os](load-a-id2d1image-using-the-filepicker.md) [dispositivos e contextos de dispositivo](devices-and-device-contexts.md).

 

1.  Declare uma variável [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) e, em seguida, crie um efeito de [origem de bitmap](bitmap-source.md) usando o método [**ID2DDeviceContext:: createeffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) .

    ```C++
        ComPtr<ID2D1Effect> bitmapSourceEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect));
    ```

    

2.  Defina a Propriedade BitmapSource para a origem do bitmap do WIC usando o [**ID2D1Effect:: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)).

    ```C++
            DX::ThrowIfFailed(m_bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, m_wicBitmapSource.Get()));
    ```

    

3.  Declare uma variável [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) e crie o efeito de [Desfoque Gaussiano](gaussian-blur.md) .

    ```C++
        ComPtr<ID2D1Effect> gaussianBlurEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect));
    ```

    

4.  Defina a entrada para receber a imagem do efeito de origem do bitmap. Defina o valor de desfoque o método [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) e a propriedade de desvio padrão.

    ```C++
        gaussianBlurEffect->SetInputEffect(0, bitmapSourceEffect.Get());

        DX::ThrowIfFailed(gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 6.0f));
    ```

    

5.  Use o contexto do dispositivo para desenhar a saída da imagem resultante.

    ```C++
        m_d2dContext->BeginDraw();

        m_d2dContext->Clear(D2D1::ColorF(D2D1::ColorF::CornflowerBlue));

        // Draw the blurred image.
        m_d2dContext->DrawImage(gaussianBlurEffect.Get());

        HRESULT hr = m_d2dContext->EndDraw();
    ```

    

    O método [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) deve ser chamado entre as chamadas [**ID2DDeviceContext:: BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) e [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) , como outras operações de renderização Direct2D. O **DrawImage** pode pegar uma imagem ou a saída de um efeito e renderizá-la na superfície de destino.

## <a name="spatial-transforms"></a>Transformações espaciais

O Direct2D fornece efeitos internos que podem transformar imagens em espaço 2D e 3D, bem como no dimensionamento. Os efeitos de escala e transformação oferecem vários níveis de qualidade, como: vizinho mais próximo, linear, cúbico, com várias amostras lineares, anisotropic e cúbico de alta qualidade.

> [!Note]  
> O modo anisotropic gera mipmaps ao dimensionar, no entanto, se você definir a propriedade **armazenada em cache** como true nos efeitos que são inseridos na transformação, o mipmaps não será gerado toda vez para imagens suficientemente pequenas.

 


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



Esse uso do efeito de transformação afim 2D gira o bitmap levemente no sentido anti-horário.



| Antes                                                            |
|-------------------------------------------------------------------|
| ![efeito de afinidade 2D antes da imagem.](images/default-before.jpg)      |
| After (após)                                                             |
| ![efeito de afinidade 2D após imagem.](images/21-2daffinetransform.png) |



 

## <a name="compositing-images"></a>Composição de imagens

Alguns efeitos aceitam várias entradas e as compõem em uma imagem resultante.

Os efeitos compostos compostos e aritméticos internos fornecem vários modos, para obter mais informações, consulte o tópico [composto](composite.md) . O efeito de [Blend](blend.md) tem uma variedade de modos acelerados de GPU disponíveis.


```C++
ComPtr<ID2D1Effect> compositeEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect));

compositeEffect->SetInput(0, bitmap.Get());
compositeEffect->SetInput(1, bitmapTwo.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



O efeito composto combina imagens de várias maneiras diferentes de acordo com o modo especificado.

## <a name="pixel-adjustments"></a>Ajustes de pixel

Há alguns efeitos Direct2Ds internos que permitem alterar os dados de pixel. Por exemplo, o efeito de matriz de cor pode ser usado para alterar a cor de uma imagem.


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



Esse código usa a imagem e altera a cor, conforme mostrado nas imagens de exemplo aqui.



| Antes                                                          |
|-----------------------------------------------------------------|
| ![efeito de matriz de cor antes da imagem.](images/default-before.jpg) |
| After (após)                                                           |
| ![efeito da matriz de cores após a imagem.](images/15-colormatrix.png)  |



 

Consulte a seção de [efeitos internos de cor](how-to-create-a-solid-color-brush.md) para obter mais informações.

## <a name="building-effect-graphs"></a>Criando grafos de efeito

Você pode encadear efeitos em conjunto para transformar imagens. Por exemplo, o código aqui aplica uma sombra e uma transformação 2D e, em seguida, compõe os resultados juntos.


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



Este é o conjunto de resultados.

![saída de efeito de sombra.](images/effect-overview-shadow.png)

Os efeitos tomam objetos [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) como entrada. Você pode usar um [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) porque a interface é derivada de **ID2D1Image**. Você também pode usar a [**saída ID2D1Effect::**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput) getpara obter a saída de um objeto [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) como um **ID2D1Image** ou usar o método **SetInputEffect** , que converte a saída para você. Na maioria dos casos, um grafo de efeito consiste em objetos **ID2D1Effect** encadeados diretamente, o que facilita a aplicação de vários efeitos a uma imagem para criar visuais atraentes.

Consulte [como aplicar efeitos a primitivos](how-to-apply-effects-to-primitives.md) para obter mais informações.

## <a name="related-topics"></a>Tópicos relacionados

[Exemplo de efeitos de imagem básica do Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20basic%20image%20effects%20sample)

[Efeitos internos](built-in-effects.md)