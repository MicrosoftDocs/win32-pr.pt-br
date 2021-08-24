---
title: Efeitos (Direct2D)
description: Uma visão geral dos Direct2D efeitos.
ms.assetid: 1446BDA9-AD4C-472C-8F1D-82ABC1880E13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe0a88ff64721fc32955416dcfe108b1c9e87f7565a67fc2e1d8192a1eaf369d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317976"
---
# <a name="effects"></a>Efeitos

## <a name="what-are-direct2d-effects"></a>Quais são Direct2D efeitos?

Você pode usar Direct2D para aplicar um ou mais efeitos de alta qualidade a uma imagem ou um conjunto de imagens. As APIs de efeitos são criadas [no Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features) e aproveitam os recursos de GPU para processamento de imagem. Você pode encadear efeitos em um grafo de efeito e compor ou combinar a saída de efeitos.

Um Direct2D de imagem executa uma tarefa de geração de imagens, como alterar o brilho, des saturar uma imagem ou criar uma sombra. Os efeitos podem aceitar zero ou mais imagens de entrada, expor várias propriedades que controlam sua operação e gerar uma única imagem de saída.

Cada efeito cria um grafo de transformação interno com base em transformação individuais. Cada transformação representa uma única operação de imagem. A principal finalidade de uma transformação é a casa dos sombreadores que são executados para cada pixel de saída. Esses sombreadores podem incluir sombreadores de pixel, sombreadores de vértice, o estágio de mesclagem de uma GPU e sombreadores de computação.

Os [Direct2D](./direct2d-portal.md) [efeitos integrados](built-in-effects.md) e os efeitos personalizados que você pode fazer usando a [API de efeitos personalizados](custom-effects.md) funcionam dessa maneira.

Há uma variedade de [efeitos integrados de](built-in-effects.md) categorias como aquelas aqui. Consulte a [seção Efeitos integrados](built-in-effects.md) para ver uma lista completa.

-   [Filtragem](built-in-effects.md)
-   [Composição e mesclagem](built-in-effects.md)
-   [Transparência](built-in-effects.md)
-   [Cor](built-in-effects.md)
-   [Iluminação e estilização](built-in-effects.md)
-   [Transformação e dimensionamento](built-in-effects.md)
-   [Fontes](built-in-effects.md)

Você pode aplicar efeitos a qualquer bitmap, incluindo: imagens carregadas pelo [WIC (Componente](/windows/desktop/wic/-wic-api)de Imagens do Windows), primitivos desenhados por [Direct2D](./direct2d-portal.md), texto do [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)ou cenas renderizadas [pelo Direct3D.](/windows/desktop/direct3d10/d3d10-graphics)

Com Direct2D, você pode escrever seus próprios efeitos que você pode usar para seus aplicativos. Uma estrutura de efeito personalizado permite que você use recursos de GPU, como sombreadores de pixel, sombreadores de vértice e a unidade de combinação. Você também pode incluir outros efeitos personalizados ou integrados em seu efeito personalizado. A estrutura para criar efeitos personalizados é a mesma que foi usada para criar os efeitos integrados do [Direct2D](./direct2d-portal.md). A [API Direct2D de autor do](custom-effects.md) efeito Direct2D fornece um conjunto de interfaces para criar e registrar efeitos.

### <a name="more-effects-topics"></a>Tópicos de mais efeitos

O restante deste tópico explica os conceitos básicos Direct2D efeitos, como aplicar um efeito a uma imagem. A tabela aqui tem links para tópicos adicionais sobre efeitos.

| Tópico                                                                                                                    | Descrição                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Vinculação de Sombreador de Efeito](effect-shader-linking.md)<br/>                                                            | Direct2D usa uma otimização chamada vinculação de sombreador de efeito que combina a renderização de grafo de vários efeitos passa em uma única passagem.<br/>                                               |
| [Efeitos personalizados](custom-effects.md)<br/>                                                                          | Mostra como escrever seus próprios efeitos personalizados usando HLSL padrão.<br/>                                                                                                                |
| [Como carregar uma imagem em efeitos Direct2D usando o FilePicker](load-a-id2d1image-using-the-filepicker.md)<br/> | Mostra como usar o [**Windows::Armazenamento::P ickers::FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) para carregar uma imagem em Direct2D efeitos.<br/>                                      |
| [Como salvar o conteúdo do Direct2D em um arquivo de imagem](save-direct2d-content-to-an-image-file.md)<br/>                   | Este tópico mostra como usar [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) para salvar o conteúdo na forma de [**um ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) em um arquivo de imagem codificado, como JPEG.<br/> |
| [Como aplicar efeitos a primitivos](how-to-apply-effects-to-primitives.md)<br/>                                  | Este tópico mostra como aplicar uma série de efeitos a Direct2D [e](./direct2d-portal.md) [DirectWrite](direct2d-and-directwrite.md) primitivos.<br/>                           |
| [Controlando a precisão e o recorte numérico em grafos de efeito](precision-and-clipping-in-effect-graphs.md)<br/>  | Os aplicativos que renderizam efeitos usando Direct2D devem ter cuidado para atingir o nível desejado de qualidade e previsibilidade em relação à precisão numérica. <br/>                    |

## <a name="applying-an-effect-to-an-image"></a>Aplicando um efeito a uma imagem

Você pode usar a API Direct2D efeitos para aplicar as transformação a imagens.

> [!Note]  
> Este exemplo pressupõe que você já tenha [**os objetos ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) [e IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) criados. Para obter mais informações sobre como criar esses objetos, consulte Como carregar uma imagem em Direct2D usando o [FilePicker](load-a-id2d1image-using-the-filepicker.md) [e dispositivos e contextos de dispositivo.](devices-and-device-contexts.md)

 

1.  Declare uma [**variável ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) e crie um efeito de origem [bitmap](bitmap-source.md) usando o [**método ID2DDeviceContext::CreateEffect.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect)

    ```C++
        ComPtr<ID2D1Effect> bitmapSourceEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect));
    ```

    

2.  De definir a propriedade BitmapSource como a origem do bitmap WIC usando [**o ID2D1Effect::SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)).

    ```C++
            DX::ThrowIfFailed(m_bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, m_wicBitmapSource.Get()));
    ```

    

3.  Declare uma [**variável ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) e crie o efeito [de desfoque gaussiano.](gaussian-blur.md)

    ```C++
        ComPtr<ID2D1Effect> gaussianBlurEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect));
    ```

    

4.  De definir a entrada para receber a imagem do efeito de origem do bitmap. De definir a quantidade de desfoque [**do método SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) e a propriedade de desvio padrão.

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

    

    O [**método DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) deve ser chamado entre as chamadas [**ID2DDeviceContext::BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) e [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) como outras Direct2D de renderização. **DrawImage** pode pegar uma imagem ou a saída de um efeito e renderizar para a superfície de destino.

## <a name="spatial-transforms"></a>Transformações espaciais

Direct2D fornece efeitos integrados que podem transformar imagens em espaço 2D e 3D, bem como dimensionamento. Os efeitos de escala e transformação oferecem vários níveis de qualidade, como: vizinho mais próximo, linear, cúbica, multi amostra linear, aniso e cubo de alta qualidade.

> [!Note]  
> No entanto, o modo aniso gerará mipmaps ao dimensionar, se você definir a propriedade **Em** cache como true nos efeitos que são de entrada para a transformação, os mipmaps não serão gerados toda vez para imagens suficientemente pequenas.

 


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



Esse uso do efeito de transformação de afinidade 2D gira um pouco o bitmap no sentido anti-horário.



| Antes                                                            |
|-------------------------------------------------------------------|
| ![Efeito de afinidade 2d antes da imagem.](images/default-before.jpg)      |
| Depois                                                             |
| ![Efeito de afinidade 2d após a imagem.](images/21-2daffinetransform.png) |



 

## <a name="compositing-images"></a>Composição de imagens

Alguns efeitos aceitam várias entradas e as composição em uma imagem resultante.

Os efeitos compostos e aritméticos integrados fornecem vários modos. Para obter mais informações, consulte o [tópico composto.](composite.md) O [efeito](blend.md) blend tem uma variedade de modos acelerados de GPU disponíveis.


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

Há alguns efeitos de Direct2D que permitem alterar os dados de pixel. Por exemplo, o efeito da matriz de cores pode ser usado para alterar a cor de uma imagem.


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



Esse código pega a imagem e altera a cor, conforme mostrado nas imagens de exemplo aqui.



| Antes                                                          |
|-----------------------------------------------------------------|
| ![efeito da matriz de cores antes da imagem.](images/default-before.jpg) |
| Depois                                                           |
| ![efeito da matriz de cores após a imagem.](images/15-colormatrix.png)  |



 

Consulte a [seção efeitos integrados de cor](how-to-create-a-solid-color-brush.md) para obter mais informações.

## <a name="building-effect-graphs"></a>Criando grafos de efeito

Você pode encadear efeitos juntos para transformar imagens. Por exemplo, o código aqui aplica uma sombra e uma transformação 2D e, em seguida, composição dos resultados juntos.


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

Os efeitos [**levam os objetos ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) como entrada. Você pode usar um [**ID2D1Bitmap porque**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) a interface é derivada de **ID2D1Image**. Você também pode usar [**o ID2D1Effect::GetOutput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput) para obter a saída de um objeto [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) como **um ID2D1Image** ou usar o **método SetInputEffect,** que converte a saída para você. Na maioria dos casos, um grafo de efeito consiste em **objetos ID2D1Effect** diretamente encadeados, o que facilita a aplicação de vários efeitos a uma imagem para criar visuais atraentes.

Confira [Como aplicar efeitos a primitivos para](how-to-apply-effects-to-primitives.md) obter mais informações.

## <a name="related-topics"></a>Tópicos relacionados

[Direct2D exemplo de efeitos de imagem básicos](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20basic%20image%20effects%20sample)

[Efeitos integrados](built-in-effects.md)