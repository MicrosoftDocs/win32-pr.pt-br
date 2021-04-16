---
description: Este tópico apresenta fontes de bitmap, um componente principal do Windows Imaging Component (WIC) que representa os pixels de bitmap de uma imagem.
ms.assetid: cff0c088-ca22-4d55-9cf0-9cbe9803923e
title: Visão geral de fontes de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910bfc253798058639b98a1d1beaacec9bd4d1bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461074"
---
# <a name="bitmap-sources-overview"></a>Visão geral de fontes de bitmap

Este tópico apresenta fontes de bitmap, um componente principal do Windows Imaging Component (WIC) que representa os pixels de bitmap de uma imagem.

Este tópico inclui as seções a seguir.

-   [Fontes de bitmap](#bitmap-sources-overview)
-   [Quadros de bitmap](#bitmap-frames)
-   [Bitmaps](#bitmap-sources-overview)
-   [Transformar fontes de bitmap](#transform-bitmap-sources)
-   [Conversores de formato de pixel e de contexto de cor](#pixel-format-and-color-context-converters)
-   [Desenho de fontes de bitmap](#drawing-bitmap-sources)
-   [Tópicos relacionados](#related-topics)

## <a name="bitmap-sources"></a>Fontes de bitmap

O componente [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) é o bloco de construção básico do WIC e representa um único conjunto de pixels. Uma origem de bitmap pode ser um quadro individual de uma imagem de multiquadro ou pode ser o resultado de uma transformação executada em uma origem de bitmap. A interface **IWICBitmapSource** é a base de muitas das interfaces primárias do WIC, como o quadro do decodificador [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) e as fontes de bitmap de transformação, como o [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator).

A tabela a seguir descreve os diferentes componentes de origem de bitmap fornecidos pelo WIC.



| Fontes de bitmap                                                    | Descrição                                                          |
|-------------------------------------------------------------------|----------------------------------------------------------------------|
| [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) | Representa um quadro de imagem de decodificador.                                    |
| [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)                       | Fornece gravação e representação na memória para fontes de bitmap. |
| [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)         | Corta uma origem de bitmap para um retângulo desejado.                        |
| [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) | Inverte e/ou gira uma origem de bitmap para uma orientação desejada.       |
| [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)           | Dimensiona uma origem de bitmap para um tamanho desejado.                            |
| [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)       | Transforma o contexto de cor de uma fonte de bitmap.                     |
| [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)     | Converte o formato de pixel de uma fonte de bitmap.                        |



 

## <a name="bitmap-frames"></a>Quadros de bitmap

O [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) mais comum é o [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode). Essa interface é usada para acessar os dados reais de bitmap de um formato de imagem. Muitos formatos de imagem dão suporte apenas a um único quadro de bitmap, enquanto outros formatos, como GIF e TIFF, dão suporte a vários quadros por imagem.

Para obter um exemplo de como obter quadros de bitmap de uma imagem, consulte o tópico [como recuperar os quadros de uma imagem](https://www.bing.com/search?q=How+to+Retrieve+the+Frames+of+an+Image) .

## <a name="bitmaps"></a>Bitmaps

Um [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) adiciona os conceitos de gravação e estática na memória a fontes de bitmap. Os bitmaps do WIC permitem que os usuários acessem diretamente os pixels de uma fonte de bitmap. Esse acesso direto é fornecido pelo método [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) e dá suporte a qualquer combinação de acesso de leitura e/ou gravação para os pixels de bitmap. O método **Lock** bloqueia o retângulo de bitmap especificado e fornece um objeto [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) para acessar os pixels.

Para obter um exemplo usando objetos [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) e [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) , consulte o tópico [como modificar os pixels de uma fonte de bitmap](-wic-bitmapsources-howto-modifypixels.md) .

## <a name="transform-bitmap-sources"></a>Transformar fontes de bitmap

O WIC fornece várias interfaces [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) que transformam os dados de pixel. Especificamente, o WIC fornece transformações de origem de bitmap para dimensionar, recortar, girar e inverter dados de pixel. Essas transformações de origem de bitmap são [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)e [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator). Cada uma dessas fontes de bitmap tem um método para inicializar e criar uma nova origem de bitmap transformada. Por exemplo, o **IWICBitmapClipper** inclui o método [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize) . Esse método inicializa a origem do bitmap do Clipper com os dados de pixel recortados da fonte de bitmap de entrada no [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)determinado.

Os tópicos de instruções a seguir demonstram usos diferentes das fontes de bitmap de transformação.

-   [Como dimensionar uma fonte de bitmap](-wic-bitmapsources-howto-scale.md)
-   [Como recortar uma fonte de bitmap](-wic-bitmapsources-howto-clip.md)
-   [Como inverter e girar uma fonte de bitmap](-wic-bitmapsources-howto-flipandrotate.md)

## <a name="pixel-format-and-color-context-converters"></a>Conversores de formato de pixel e de contexto de cor

O WIC também fornece fontes de bitmap convertendo o formato de pixel e o contexto de cor de uma fonte de bitmap. O WIC fornece o [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) e o [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) para essas operações.

[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) converte uma determinada origem de bitmap de um formato de pixel para outro.

Para obter um exemplo usando o [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter), consulte o tópico [como desenhar uma fonte de bitmap usando o Direct2D](-wic-bitmapsources-howto-drawusingd2d.md) .

## <a name="drawing-bitmap-sources"></a>Desenho de fontes de bitmap

O WIC é uma tecnologia de codec de imagem ainda e é usado para gerenciar metadados e dados de imagem e não fornece inerentemente uma maneira de renderizar imagens. No entanto, as fontes de bitmap podem ser desenhadas usando várias tecnologias de gráficos do Windows, como Direct2D, Windows Graphics Device Interface (GDI) e Windows GDI+. Cada uma dessas tecnologias tem um nível diferente de interoperabilidade com o WIC. O Direct2D fornece interoperabilidade direta por meio da interface [ID2D1Bitmap](../direct2d/render-targets-overview.md) e do método [ID2D1RenderTarget:: CreateBitmapFromWicBitmap](../direct2d/id2d1rendertarget-createbitmapfromwicbitmap.md) enquanto GDI e GDI+ exigem que os usuários copiem os pixels de origem de bitmap em [bitmaps](../gdi/bitmaps.md).

O exemplo a seguir demonstra como desenhar fontes de bitmap usando Direct2D.

-   [Como desenhar uma fonte de bitmap usando o Direct2D](-wic-bitmapsources-howto-drawusingd2d.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Visão geral da codificação](-wic-creating-encoder.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
