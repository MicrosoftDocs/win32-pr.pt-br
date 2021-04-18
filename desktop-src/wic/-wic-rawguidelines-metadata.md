---
description: Suporte a metadados
ms.assetid: f3b4a3d9-a353-4af8-9998-cb7da7a062b7
title: Suporte a metadados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32499a88bd9cc12186629476f4d9f32a6e811858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812163"
---
# <a name="metadata-support"></a>Suporte a metadados

Os formatos BRUTOs também devem dar suporte aos cenários comuns de leitura e gravação de metadados para imagens no Windows. A Microsoft desenvolveu um conjunto de provedores de metadados nativos para o arquivo de imagem exchangável (EXIF), o IPTC (International Telecommunications Council) e os metadados da XMP (plataforma de metadados extensível) que são atualmente invocados apenas para contêineres TIFF e JPEG. Se a imagem bruta for armazenada em um desses formatos de contêiner, é recomendável usar os provedores de metadados internos do Windows. No entanto, o autor do codec é responsável por configurar isso corretamente. Para arquivos BRUTOs que não são baseados em um contêiner TIFF, pode ser necessário implementar os gravadores EXIF, IPTC ou XMP porque os leitores e gravadores internos esperam que os dados estejam em conformidade com as especificações de layout de EXIF, IPTC e XMP no disco. Os autores de codec também podem implementar seus próprios provedores para qualquer metadado personalizado.

Devido à arquitetura do Windows Imaging Component (WIC), os gravadores de metadados podem ser invocados somente por meio de uma instância de um codificador de imagem. Portanto, os proprietários de formato bruto devem criar pelo menos um codificador "stub" [**WICRawParameterSet. WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) , mesmo que a codificação real de pixels em um formato bruto não seja implementada. O autor do codec deve invocar os manipuladores de metadados apropriados:

-   [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) no decodificador e no decodificador de quadro, conforme apropriado.
-   [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) tanto no codificador quanto no codificador de quadros, conforme apropriado.

Para dar suporte a todos os cenários previstos em aplicativos de geração de imagens no Windows Vista, é recomendável que os fornecedores de codecs suportam o seguinte no mínimo:

-   Leitura de EXIF
-   Gravação parcial de EXIF (para permitir que as atualizações capturem data e hora)
-   XMP de leitura e gravação (incluindo opcionalmente IPTC core para XMP)
-   Leitura e gravação de IPTC IIMv4

A maior parte do acesso aos metadados (leitura e gravação) no Windows Vista ocorre por meio da interface [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) ou [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) . Portanto, para participar das experiências de metadados do Windows Vista, os autores de codec BRUTOs devem implementar os métodos [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) e [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .

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

 

 



