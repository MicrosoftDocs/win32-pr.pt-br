---
description: Suporte para IWICDevelopRaw
ms.assetid: 8e8ff65b-0849-42e0-924e-2a7c61d4b1bb
title: Suporte para IWICDevelopRaw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa39aa339a3cd21c7ffa848a5ab1fe2dd6426981
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170858"
---
# <a name="support-for-iwicdevelopraw"></a>Suporte para IWICDevelopRaw

Para permitir que os aplicativos ofereçam suporte ao processamento bruto, os autores de codec são altamente incentivados a implementar todos os parâmetros de [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw). Para o Windows 7, o Windows Imaging Component (WIC) precisará de suporte para todos os [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw). Se o formato de arquivo não oferecer suporte a todos esses parâmetros, você deverá revisar o formato do arquivo de imagem.

Para habilitar o processamento bruto básico em aplicativos, os codecs devem dar suporte a ajustes de exposição (ExposureCompensationSupport) e cor (como KelvinWhitePointSupport e TintSupport). Além disso, a saída para espaços de cores e formatos de pixel específicos é altamente recomendável. O suporte para outros ajustes é, é claro, incentivado e é necessário para o Windows 7.

O codec bruto deve fornecer suporte básico para rotação de imagem e visualização rápida. A rotação pode ser especificada de duas maneiras distintas:

-   Método [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) . Esse método define o ângulo de rotação desejado para a saída de chamadas subsequentes para [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels).
-   Método [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) . O chamador pode definir a opção dstTransform para indicar o ângulo de rotação desejado.

Essas duas abordagens diferem das seguintes maneiras:

-   Somente as configurações de [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) podem ser mantidas entre instâncias do objeto decodificador.
-   [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) aplica-se somente a essa chamada específica; Não há nenhuma persistência de nenhum tipo.
-   O [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) fornece um controle refinado muito maior em rotação. [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) é restrito a incrementos de 90 graus.

Se a rotação for especificada em [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) e [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), o efeito de rotação será cumulativo. Por exemplo, se [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) especificar uma rotação de 25 graus e [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) especificar uma rotação de 90 graus, o seguinte deverá acontecer:

-   As chamadas para [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) devem aplicar uma rotação de 25 graus (ou seja, apenas o valor especificado em [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)).
-   Chamadas para [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) com uma quantidade de dstTransform de 90 resultam em uma rotação de 115 graus (25 + 90).
-   Novamente, apenas a rotação de 25 graus especificada por meio de [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) pode ser persistente.

No Windows Vista, os métodos [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) e [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)::[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) permitem que os chamadores obtenham miniaturas inseridas e imagens de visualização, respectivamente. Elas destinam-se a retornar visualizações e miniaturas pré-calculados do fluxo de arquivos de imagem. Gerar visualizações ou miniaturas "instantaneamente" resulta em um baixo desempenho no Windows Explorer e no Visualizador de fotos. O codec também deve fornecer uma maneira de retornar uma imagem de resolução de tela atualizada rapidamente quando os usuários estiverem fazendo controle interativo das configurações de processamento.

As chamadas para [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**setrenderingmode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) determinarão quais chamadas subsequentes para [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) retornam (favorecendo a velocidade ou a qualidade). Além disso, a interface IWICBitmapSourceTransform pode ser usada para determinar se a redução de resolução é necessária e pode aumentar o desempenho quando ela pode ser aplicada. A fidelidade de cor de todas as imagens deve ser comparável. Quando são feitas alterações nas configurações de processamento, todas essas renderizações devem refletir as alterações.

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

 

 



