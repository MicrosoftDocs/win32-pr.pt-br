---
description: Requisitos do método de interface
ms.assetid: 8c2afeb3-3e0b-4f8a-a2f4-df7c9ce4b098
title: Requisitos do método de interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9cabe02900fa789773f4104cf282ab326bd4930
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749521"
---
# <a name="interface-method-requirements"></a>Requisitos do método de interface

Nem todo método em cada interface deve ter uma implementação. Por exemplo, alguns codecs têm metadados globais, miniaturas ou contextos de cores, enquanto outros codecs os fornecem apenas em uma base por quadro. Se os autores de codec fornecerem esses somente por quadro, eles precisarão implementar apenas [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) / [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) ou ColorContexts, ou implementar os métodos [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) ou [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) em [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) e [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) em vez de em [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder). Da mesma forma, alguns codecs não usam formatos indexados e, portanto, não são necessários para implementar os métodos [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) e [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) . Portanto, esses métodos são opcionais e são deixados para a critério do criador do codec. A maioria dos outros métodos são necessários.

Para o Windows 7, [**obtenha**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) / [**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) e [**obter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) / [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) são necessários e devem ser implementados nas classes de nível de contêiner ou nas classes de nível de quadro. Se o formato do arquivo de imagem não der suporte a visualizações ou miniaturas em qualquer um desses locais, você deverá revisar o formato do arquivo de imagem para fornecer esse suporte.

Quando um método não é implementado, é importante retornar um erro apropriado para que o chamador possa determinar que o recurso solicitado não tem suporte. Por exemplo, se os autores de codec não oferecerem suporte a miniaturas de nível de contêiner, eles deverão retornar [WINCODEC \_ Err \_ CODECNOTHUMBNAIL](-wic-codec-error-codes.md) quando um aplicativo chamar [**GetThumbnail**](-wic-codec-iwicbitmapdecoder-getthumbnail-proxy.md)e, se eles não tiverem uma paleta, deverão retornar [WINCODEC \_ Err \_ PALETTEUNAVAILABLE](-wic-codec-error-codes.md). Se não existir nenhum código de [ \_ erro WINCODEC](-wic-codec-error-codes.md) adequado, o codec deverá retornar E \_ NOTIMPL para métodos não implementados.

As tabelas a seguir listam os métodos obrigatórios e opcionais para cada interface do Windows Imaging Component (WIC).

[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)



Obrigatório

[**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability)

[**Inicializar**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize)

[**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat)

[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo)

[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount)

[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe)

Opcional

¹ [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)

[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)²

[**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts)

[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader)

[**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)



 

¹ necessário se o formato de arquivo de imagem oferecer suporte a visualizações em nível de contêiner. Se esse não for o caso, você é altamente incentivado a revisar o formato de arquivo de imagem para dar suporte a isso. Se implementado aqui, um [**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) correspondente será necessário na classe de codificação no nível de contêiner.

² necessário aqui ou na classe de decodificação de nível de quadro, dependendo de onde o formato de arquivo de imagem armazena miniaturas. Se for implementado aqui, um [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) correspondente será necessário na classe de codificação no nível de contêiner.

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)



Obrigatório

[**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts)

[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader)

[**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize)

[**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)

[**Resolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution)

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)

Opcional

[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)¹

[**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)



 

¹ precisou aqui ou na classe de decodificação de nível de contêiner, dependendo de onde o formato de arquivo de imagem armazena miniaturas. Se for implementado aqui, um [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) correspondente será necessário na classe de codificador de nível de quadro.

[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)



Obrigatório

[**GetContainerFormat**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat)

[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount)

[**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex)

[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator)



 

[**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)



Obrigatório

[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform)

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels)

Opcional

[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize)

[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat)



 

[**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)

Consulte [suporte para IWICDevelopRaw](./-wic-rawguidelines-iwicdevelopraw.md), mais adiante neste documento.

[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)



Obrigatório

[**Inicializar**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

[**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getcontainerformat)

[**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo)

[**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)

[**Compromisso**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

Opcional

¹ de [**Visualização**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview)

[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)²

[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setcolorcontexts)

[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter)

[**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette)



 

¹ necessário se o formato de arquivo de imagem der suporte a visualizações em nível de quadro.

² necessário aqui ou na classe de codificação no nível do quadro, dependendo de onde o formato do arquivo de imagem armazena miniaturas. Se for implementado aqui, um [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) correspondente será necessário na classe de decodificação de nível de contêiner.

[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)



Obrigatório

[**Inicializar**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

[**Size**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize)

[**SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat)

[**Resolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution)

[**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels)

[**Gravação**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource)

[**Compromisso**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

Opcional

¹ [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail)

[**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette)



 

¹ precisou aqui ou na classe de codificação no nível do contêiner, dependendo de onde o formato do arquivo de imagem armazena miniaturas. Se for implementado aqui, um [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) correspondente será necessário na classe de decodificação no nível do quadro.

[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)



Obrigatório

[**InitializeFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader)

[**AddWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter)

[**GetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex)

[**SetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex)

[**RemoveWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex)



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Diretrizes do WIC para formatos de imagem bruta de câmera](-wic-rawguidelines.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
