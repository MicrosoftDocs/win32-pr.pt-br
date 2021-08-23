---
description: o tópico apresenta o decodificador de bitmap, um componente de codec do core Windows Imaging component (WIC) usado para decodificar arquivos de imagem de um fluxo.
ms.assetid: 9dc8d2ec-5cc5-45fa-8a4d-5bdc3072c90c
title: Visão geral da decodificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14300c9857702ceff5f07fcc127a4ef4182f9e77ad46f0598edc12abf91f240
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711390"
---
# <a name="decoding-overview"></a>Visão geral da decodificação

o tópico apresenta o decodificador de bitmap, um componente de codec do core Windows Imaging component (WIC) usado para decodificar arquivos de imagem de um fluxo.

Este tópico inclui as seções a seguir.

-   [Introdução](#introduction)
-   [Decodificadores de bitmap nativos](#native-bitmap-decoders)
-   [Criando um decodificador de bitmap](#creating-a-bitmap-decoder)
-   [Extensibilidade do decodificador](#decoder-extensibility)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

Os decodificadores de bitmap podem ser exibidos como o contêiner externo de uma imagem digital e fornecem acesso a propriedades globais e quadros de imagem. Alguns formatos de imagem dão suporte a miniaturas globais, visualizações, contextos de cor ou metadados, enquanto outros fornecem essas propriedades somente no nível do quadro. No entanto, observe que muitos dos formatos de imagem padrão não dão suporte a essas propriedades globais. Assim, muitas das implementações de codecs nativos fornecidas pelo WIC não dão suporte à maioria dessas propriedades globais. Consulte a tabela na seção decodificadores de bitmap nativos deste tópico para obter informações sobre o suporte a propriedades globais.

No WIC, os decodificadores de bitmap são representados pela interface [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e fornecem acesso a essas propriedades globais do bitmap e, mais importante, aos quadros que ele contém. A interface [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) representa um quadro de bitmap individual e é discutida em detalhes na [visão geral de fontes de bitmap](-wic-bitmapsources.md).

## <a name="native-bitmap-decoders"></a>Decodificadores de bitmap nativos

O WIC fornece várias implementações nativas da interface [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) para os formatos de imagem da Web padrão e o formato de foto HD de alto alcance dinâmico. A tabela a seguir lista os decodificadores nativos disponíveis, o nome do identificador de classe e o suporte para propriedades globais. Embora um recurso possa não dar suporte a uma propriedade como miniaturas no nível global, o formato da imagem pode dar suporte a essas propriedades no nível de quadro individual.



| Formato de imagem | Nome do CLSID            | Miniaturas | Visualizações | Contextos de cor | Metadados |
|--------------|-----------------------|------------|----------|----------------|----------|
| BMP          | \_WICBMPDECODER CLSID  | Não         | Não       | Não             | Não       |
| GIF          | \_WICGIFDECODER CLSID  | Não         | Não       | Não             | Sim      |
| ICO          | \_WICICODECODER CLSID  | Não         | Não       | Não             | Não       |
| JPEG         | \_WICJPEGDECODER CLSID | Não         | Não       | Não             | Não       |
| PNG          | \_WICPNGDECODER CLSID  | Não         | Não       | Não             | Não       |
| TIFF         | \_WICTIFFDECODER CLSID | Não         | Não       | Não             | Não       |
| Foto de HD     | \_WICWMPDECODER CLSID  | Não         | Sim      | Não             | Não       |



 

## <a name="creating-a-bitmap-decoder"></a>Criando um decodificador de bitmap

Para decodificar uma imagem usando o WIC, primeiro você precisa criar uma instância de [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) para o formato de imagem de destino. A instância do decodificador permite que você acesse as propriedades globais e os metadados, se houver suporte, bem como os quadros de imagem. O WIC Imaging Factory, [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), fornece vários métodos para criar decodificadores de bitmap. Os métodos de fábrica a seguir são fornecidos para criar decodificadores de bitmap.

-   [**CreateDecoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder)
-   [**CreateDecoderFromFileHandle**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle)
-   [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename)
-   [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)

O código a seguir demonstra como criar um decodificador de bitmap usando um nome de arquivo de imagem e recuperar o primeiro quadro da imagem.


```C++
   // Create a decoder
   IWICBitmapDecoder *pDecoder = NULL;

   hr = m_pIWICFactory->CreateDecoderFromFilename(
       szFileName,                      // Image to be decoded
       NULL,                            // Do not prefer a particular vendor
       GENERIC_READ,                    // Desired read access to the file
       WICDecodeMetadataCacheOnDemand,  // Cache metadata when needed
       &pDecoder                        // Pointer to the decoder
       );

   // Retrieve the first frame of the image from the decoder
   IWICBitmapFrameDecode *pFrame = NULL;

   if (SUCCEEDED(hr))
   {
       hr = pDecoder->GetFrame(0, &pFrame);
   }
```



## <a name="decoder-extensibility"></a>Extensibilidade do decodificador

Um dos principais recursos do WIC é uma estrutura de extensibilidade que permite que os desenvolvedores de codecs desenvolvam seus próprios codecs de imagem e obtenham o mesmo suporte de plataforma que as implementações nativas de codecs de imagem. Um único conjunto consistente de interfaces é usado para todo o processamento de imagem, independentemente do formato da imagem. Qualquer aplicativo que use o WIC Obtém o suporte automático para novos formatos de imagem assim que o codec é instalado. Para obter mais informações sobre o desenvolvimento de codecs, consulte os tópicos em [desenvolvimento de componentes](-wic-component-development.md). Para obter mais informações sobre o desenvolvimento de decodificadores, consulte [implementando um Decodificador WIC-Enabled](-wic-implementingwicdecoder.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Windows Visão geral do componente de geração de imagens](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Visão geral da codificação](-wic-creating-encoder.md)
</dt> <dt>

[Desenvolvimento de componentes](-wic-component-development.md)
</dt> </dl>

 

 



