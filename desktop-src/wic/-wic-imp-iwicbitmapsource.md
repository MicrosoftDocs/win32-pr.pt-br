---
description: Implementando IWICBitmapSource
ms.assetid: d092e9e5-c041-42f5-84c8-0af52bb5c810
title: Implementando IWICBitmapSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b7ffd73271e8e159eea825ed40c24347ec2af98f0edbfa9ecc0d5ac584df23b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965015"
---
# <a name="implementing-iwicbitmapsource"></a>Implementando IWICBitmapSource

## <a name="iwicbitmapsource"></a>Iwicbitmapsource

[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) é importante para trabalhar com imagens de uma perspectiva de aplicativo. Ele representa a abstração de nível mais alto para uma fonte de imagem e todas as interfaces do WIC (Componente de Imagens do Windows) que representam uma imagem, incluindo [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)e todas as interfaces de transformação [**(IWICBitmapScaler,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) [**IWICBitmapClipper,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)e [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) são derivadas dela. A qualquer momento específico, um **objeto IWICBitmapSource** pode ou não ser apoiado por um bitmap real na memória. Isso permite um processamento muito eficiente por um aplicativo, pois uma imagem pode ser tratada como uma abstração. As operações de transformação podem ser encadeadas em um pipeline de transformação sem consumir recursos de memória até que o aplicativo esteja pronto para renderizar ou imprimir a imagem, momento em que ele invoca o método [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) na transformação final para obter um bitmap na memória da imagem com as transformação selecionadas aplicadas.

``` syntax
interface IWICBitmapSource : IUnknown
{
   // Required methods
   HRESULT GetSize ( UINT *puiWidth, UINT *puiHeight );
   HRESULT GetPixelFormat ( WICPixelFormatGUID *pPixelFormat );
   HRESULT GetResolution ( double *pDpiX, double *pDpiY );
   HRESULT CopyPixels ( const WICRect *prc,
      UINT cbStride,
      UINT cbBufferSize, 
      BYTE *pbBuffer );
   // Optional method
   HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

De uma perspectiva codec, os métodos [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) são implementados no objeto de decodificador de quadro. Esses métodos são descritos em Implementando IWICBitmapSource, juntamente com os outros métodos em [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), que é derivado de **IWICBitmapSource**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[**Iwicbitmapdecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[**Iwicbitmapsource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[**Iwicbitmapframedecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Implementando IWICBitmapCodecProgressNotification (Decoder)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[Implementando IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[Como escrever um codec WIC-Enabled código](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Visão geral do componente de imagens](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



