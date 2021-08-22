---
description: Suporte para IWICDevelopRaw
ms.assetid: 8e8ff65b-0849-42e0-924e-2a7c61d4b1bb
title: Suporte para IWICDevelopRaw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6436eb9d9422da6f5a29c196df10c97014df6beff178bb584b70e45d207dd50d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709726"
---
# <a name="support-for-iwicdevelopraw"></a>Suporte para IWICDevelopRaw

Para permitir que os aplicativos deem suporte ao processamento RAW, os autores de codec são incentivados a implementar todos os parâmetros de [**IWICDevelopRaw.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) Por Windows 7, Windows WIC (componente de imagens) exigirá suporte para todos os [**IWICDevelopRaw.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) Se o formato de arquivo não dá suporte a todos esses parâmetros, você deve revisar o formato de arquivo de imagem.

Para habilitar o processamento RAW básico em aplicativos, os codecs devem dar suporte a ajustes à exposição (ExposureCompensationSupport) e à cor (como GatesWhitePointSupport e TintSupport). Além disso, a saída para espaços de cores específicos e formatos de pixel é altamente recomendada. O suporte para outros ajustes é, obviamente, incentivado e é necessário para Windows 7.

O codec RAW deve fornecer suporte básico para rotação de imagem e visualização rápida. A rotação pode ser especificada de duas maneiras distintas:

-   [**Método IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRotation.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) Esse método define o ângulo de rotação desejado para a saída de chamadas subsequentes para [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels).
-   [**Método IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) O chamador pode definir a opção dstTransform para indicar o ângulo de rotação desejado.

Essas duas abordagens diferem das seguintes maneiras:

-   Somente [**as configurações de IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) podem ser persistida entre instâncias do objeto do decodificador.
-   [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) aplica-se somente a essa chamada específica; não há persistência de nenhum tipo.
-   [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) fornece um controle muito mais fino na rotação. [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) é restrito a incrementos de 90 graus.

Se a rotação for especificada em [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) e [**IWICBitmapSourceTransform,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)o efeito de rotação será cumulativo. Por exemplo, se [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) especificar uma rotação de 25 graus e [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) especificar uma rotação de 90 graus, o seguinte deverá acontecer:

-   Chamadas para [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) devem aplicar uma rotação de 25 graus (ou seja, somente a quantidade especificada em [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)).
-   Chamadas para [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) com uma quantidade dstTransform de 90, em seguida, resultam em uma rotação de 115 graus (25 + 90).
-   Novamente, somente a rotação de 25 graus especificada por [**meio de IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) pode ser persistida.

No Windows Vista, os métodos [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) e [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder):: Os métodos [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) permitem que os chamadores recebam miniaturas inseridas e imagens de visualização, respectivamente. Eles se destinam a retornar visualizações pré-calculadas e miniaturas do fluxo de arquivos de imagem. Gerar visualizações ou miniaturas "em tempo real" resulta em baixo desempenho no Windows Explorer e Visualizador de Fotos. O codec também deve fornecer uma maneira de retornar uma imagem de resolução de tela atualizada rapidamente quando os usuários estão fazendo controle interativo das configurações de processamento.

Chamadas para [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) determinarão quais chamadas subsequentes para [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) retornam (favorecendo velocidade ou qualidade). Além disso, a interface IWICBitmapSourceTransform pode ser usada para determinar se o downsampling é necessário e pode aumentar o desempenho quando ele pode ser aplicado. A fidelidade de cores de todas as imagens deve ser comparável. Quando são feitas alterações nas configurações de processamento, todas essas renderizações devem refletir as alterações.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Windows Visão geral do componente de imagens](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Diretrizes do WIC para formatos de imagem RAW da câmera](-wic-rawguidelines.md)
</dt> <dt>

[Como escrever um codec WIC-Enabled código](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



