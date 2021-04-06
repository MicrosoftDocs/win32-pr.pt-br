---
description: Implementando IWICBitmapSource
ms.assetid: d092e9e5-c041-42f5-84c8-0af52bb5c810
title: Implementando IWICBitmapSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c88e2f7dfd073405f9de8c82b2ce6d9592b241a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662755"
---
# <a name="implementing-iwicbitmapsource"></a>Implementando IWICBitmapSource

## <a name="iwicbitmapsource"></a>IWICBitmapSource

[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) é importante para trabalhar com imagens de uma perspectiva do aplicativo. Ele representa a abstração de nível mais alto para uma origem de imagem e todas as interfaces do Windows Imaging Component (WIC) que representam uma imagem, incluindo [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)e todas as interfaces de transformação ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)e [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) são derivadas dela. Em qualquer momento específico, um objeto **IWICBitmapSource** pode ou não ser apoiado por um bitmap real na memória. Isso permite um processamento muito eficiente por um aplicativo, pois uma imagem pode ser tratada como uma abstração. As operações de transformação podem ser encadeadas em um pipeline de transformação sem consumir recursos de memória até que o aplicativo esteja pronto para renderizar ou imprimir a imagem e, nesse momento, ele invoca o método [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) na transformação final para obter um bitmap na memória da imagem com as transformações selecionadas aplicadas.

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

De uma perspectiva de codec, os métodos [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) são implementados no objeto decodificador de quadro. Esses métodos são descritos em implementando IWICBitmapSource, juntamente com os outros métodos em [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), que é derivado de **IWICBitmapSource**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Implementando IWICBitmapCodecProgressNotification (decodificador)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[Implementando IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



